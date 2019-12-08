---
title: csapp course
layout: defaultCourse
---

# Datalab 实验

这个实验帮助学生练习和掌握整型和浮点型数据的二进制表示及基本运算。在这个实验中，学生需要修改一个名为bits.c的C文件。该文件中包含多个空的方法体。学生需要在这些方法体中填写代码，使得每个方法都能够分别实现一个特定的数学函数，比如“绝对值”。在实现过程中，还有一些别的约束。比如，整型函数的实现中，学生只能使用顺序执行的C代码和限定的算术及逻辑操作符。

学生使用下列三种工具来说检查他们的工作；教师使用同样的工具来评估。

dlc：“data lab compiler”，该工具用于检查学生的代码实现是否满足指定的约束。
btest：该工具用于检查学生的代码实现是否正确。
driver.pl：这是一个驱动程序，能够调用dlc和btest来检查学生的代码实现，并自动评分。


## 实验内容
你需要完成bits.c文件中所有function框架的实现，以满足该function对应注释所要求的功能需求和编程约束。

### 示例
```C 
/*
bitAnd - x&y using only ~ and |
Example: bitAnd(6, 5) = 4
Legal ops: ~ |
Max ops: 8
Rating: 1
*/

int bitAnd(int x, int y) {
return 0;
}
```

        
    
Function框架前的注释描述了该function所要实现的功能，以及编程约束。就上述例子而言：

- 功能：实现 x&y
- Example：该function测试用例的示例
- Legal ops：允许使用的C语言操作符仅为~和|
- Max ops：允许使用的操作符的总个数的上限
- Rating：该function的难度等级，也是该function对应的分值
- 实验任务：将函数体中的“return 0；”修改成具体的代码段，以实现功能需求和编程约束。
- 实验要求
除了function框架前的注释，还有一些通用的约束（请认真阅读bits.c文件中的注释要求），比如：

    - 整型函数
        - 不能使用控制结构，比如if, do, while, for, switch等等。
        - 不能使用宏。
        - 不能定义新的函数。
        - 不能调用别的函数。
        - 不能使用别的运算符，比如：&&，||, -, ?:等等。
        - 不能使用类型转换。
        - 不能使用数组、结构、联合类型。
        - 不能使用全局变量。
        - 整型字面常量不能超过[0, 255]的范围。
    - 浮点型函数
        - 不能使用宏。
        - 不能定义新的函数。
        - 不能调用其他函数。
        - 不能使用类型转换。
        - 不能使用数组、结构和联合类型。
        - 不能使用所有的浮点类型和浮点运算符。

## 实验环境说明
### 平台与语言
- C语言
- Linux (建议64 bit Ubuntu16.04LTS及以上)

### 说明：

- data-lab实验在32位机器上不需要修改，在64位机器上需要修改Makefile（后文有说明）；其余实验可以在64位机器上正常运行。
- 建议安装虚拟机或者尝试WSL（Windows Subsystem for Linux）。

## 实验数据
实验所需的文件和代码都在一个压缩文件:datalab-handout.tar中，解压缩后，其目录如下:

- README: 实验说明文件，请在开始实验前仔细阅读。
- Makefile: 生成btest、fshow、ishow等相关工具的Makefile文件。
- bits.c: 学生需要修改的文件，包含一系列用于完成指定功能的function的代码框架。每个function框架前面有详细的注释，这些注释说明了实现该框架的具体要求。学生需要根据这些要求实现每个function框架。
- bits.h: bits.c所需头文件，不需要修改。
- btest.h, decl.c, tests.c, btest.c：用于生成btest工具，该工具用于测试实验结果是否满足功能正确。
- ishow.c: 用于生成ishow工具，该工具查看整型数据的二进制表示。
- fshow.c：用于生成fshow工具，该工具查看浮点数据的二进制表示。
- driver.pl: 该工具调用dlc和btest，对bits.c自动评分。提交之前可以据此提前预知自己的分数。
### 说明：

Makefile默认生成目标平台为32位机器y，如果实验平台为64位机器，需要将Makefile中的CFLAGS选项“-m32”修改为“-m64”。

## 实验的提交
请将包含函数实现代码的bits.c文件重命名为“学号-bits.c”文件，并提交。提交之前请务必利用实验工具进行检查。只有同时满足功能需求和编程约束的函数实现才能获得对应的评分。评分过程利用自动工具完成，因此，除非工具环境存在问题，否则不接受主观评分和申诉。

检查你的代码！！！
有3个实验工具可以帮助你依次检查完成的代码。README文件中有详细的说明。
### dlc 工具
- 使用dlc检查实现代码是否符合实验要求中的编程约束。
下列命令检查bits.c是否满足编程约束：

./dlc bits.c
    
- 下列命令可以打印出每个函数使用的操作符数目：

./dlc -e bits.c
    
- 下列命令可以查看更多命令选项：

./dlc -h
    
### btest 工具
- 通过dlc检查之后，再使用btest检查实现代码是否满足功能需求。
下列命令编译生成btest工具：

make
    
- 下列命令检查bits.c中所有函数的功能正确性：

./btest
    
- btest工具有很多别的选项，可以辅助学生调试自己的方法。比如，下列命令只测试函数bitXor，并且指定输入的两个参数为7和0xf，该命令会返回相应信息。

./btest -f bitXor -1 7 -2 -xf
    
- 说明： 每次修改bits.c后，需要利用make重新生成btest工具。

3. driver.pl工具
- 利用driver.pl预先评估自己的得分
下列命令会自动调用dlc和btest，同时考虑运行性能，从而评估得分。

./driver.pl
## 可能的问题及解决方法
问题：在64位机器上运行，可能遇到该问题：fatal error: sys/cdefs.h no such file or directory

解决方法： sudo apt install libc6-dev-i386