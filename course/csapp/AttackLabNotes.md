---
title: csapp course
layout: defaultCourse
---

## Attack-lab实验介绍

<a href="http://csapp.cs.cmu.edu/3e/bomblab.pdf">点击下载cmu官网实验说明详情</a>

这个实验帮助学生练习和掌握机器级程序的基本原理，以及一些通用的调试和反向工程技巧。shell code = exploit code + padding + return address + more stuff

## Phase-1: 
跟教材上例子类似，只需要修改返回地址到touch1，不需要额外exploit代码。

| Return addr to test：RetTest  |
|  ---  |
| ... |
|  buf-k-1  |
|  buf-k-2  |
| ... |
|  buf-0 |
||

1. 找到目标代码touch1的地址 Addr-1
2. 构造shell code, 将Addr-1填入到RetTest位置
- 注意：需要先将Addr-1转换成对应的ascii字符，然后，gets函数会将其解码成对应的ascii值。

## Phase-2:
在Phase-1的基础上，需要传递cookie参数。
1. 将buf_0所在的地址（exploit code的地址）填入到RetTest位置
2. exploit code如下：
```asm
    movq cookie, %rdi
    pushq Addr-2
    ret
```
3. 需要传递参数cookie到rdi
4. 找到目标代码touch2的地址 Addr-2，利用push+ret实现跳转到touch2（有没有别的方法，比如，ret+填充？）

## Phase-3:
在Phase-1的基础上，需要传递参数；并且参数是cookie的内存地址。
1. 找到目标代码touch2的地址 Addr-3
2. 需要在shell code中填入cookie
3. 跳转到Addr-2之前，需要传递参数&cookie到rdi
- 注意：因为后续的hexmatch函数的frame会重用getbuf的frame的地址，从而覆盖buf中的值；之后还需要访问cookie。所以cookie必须放在重用范围之外。
- 方案1：如果buf的空间有限，则通过more stuff将cookie填充到一个安全地址；然后在exploit code中，将该地址传递到rdi。
  
  
```asm
    movq &cookie, %rdi
    pushq Addr-3
    ret
```

  - 方案2：如果buf的空间足够装更多的exploit code，可以在exploit code中，先将cookie的值存入到一个安全的地址，然后将该地址传递到rdi寄存器。
```asm
    movabsq cookie, %r
    movq %r, [mem]
    leaq [mem], %rdi
    pushq Addr-3
    ret
```

## Phase-4:
    在Phase-2的基础上，需要传递参数，且参数是cookie；且只能基于Return方式进行攻击，即shell code = padding + gadgets
1. 通过填充+pop实现参数传递，即，将cookie的值填充到栈上，然后利用pop指令传递到rdi。
2. 通过ret+填充地址，跳转到touch2.

```asm
    popq %rdi # 需要填充cookie到栈顶位置
```
3. 查找popq %rdi; ret的片段地址。如果没有，可以换成等价的popq %r; movq %r, %rdi; ret
4. 查找ret;的片段地址
5. 构造gadgets

| Layout out |
| --- |
| Addr of touch2 |
| # Addr of Ret; 此步骤不可用！？ |
| cookie |
| Addr of popq gadget |
| ... |
|  buf-k-1  |
|  buf-k-2  |
| ... |
|  buf-0 |
||

## Phase-5:

在Phase-3的基础上，需要传递参数，且参数是cookie的内存地址；且只能基于Return方式进行攻击。
1. 参数cookie需要通过填充，存储在栈上。
2. 因为栈地址总在变，所以需要获取当前栈顶指针+cookie的偏移。当前栈顶指针可以用movq %rsp, %r获得，偏移需要外部填充+pop获得。
3. 根据rsp和偏移，利用lea指令，可以获得cookie的运行时地址；然后传递给rdi。lea指令使用了固定的%rm，%rn，所以需要利用多个mov指令分别将栈顶指针和偏移传递给对应的寄存器。
4. 利用填充+ret，调用touch3函数。


