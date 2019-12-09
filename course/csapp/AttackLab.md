---
title: csapp course
layout: defaultCourse
---
## Attack-lab实验介绍

<a href="http://csapp.cs.cmu.edu/3e/attacklab.pdf">点击下载cmu官网实验说明详情</a>

这个实验帮助学生练习和掌握栈的使用约定，并让他们深刻体会如果代码中存在缓冲区漏洞会导致怎样的风险。实验中为每个学生提供了两个定制的二进制文件。其中一个很容易被代码注入攻击，另一个很容易被基于return的编程方法攻击。学生的任务就是利用这两种攻击思路，设计程序输入，以实现缓冲区漏洞攻击。

<font color=blue><a href="csapp.cs.cmu.edu">点击下载参考文档</a></font>

## 实验环境说明
### 平台与语言
- x86-64 Linux
- Gcc (4.8.1以后版本)
### 可能有用的工具
- gdb
- objdump
### 实验数据如何获取
从 <a href="liqingan.cn:15513"><font size=5>指定网站</font></a> 获取实验数据压缩包。需要提供学号和邮箱地址，提交后，会自动下载该学号对应的压缩包。

说明：

每个请求的实验数据包绑定到一个特定的学号，实验进行过程中会自动计算该学号的得分，所以请务必使用自己的数据包。

如果实验数据包丢失，可以重新输入学号和邮箱地址获取。
## 实验数据
实验数据包为一个压缩文件targetN.tar。解压缩后，里面有三个文件：

- ctarget: 一个有代码注入攻击漏洞的二进制文件。
- rtarget: 一个有return-oriented攻击漏洞的二进制文件。
- cookie.txt:
- farm.c: 用于return-oriented编程攻击的源代码。
- hex2raw: 用于生成攻击字符串的工具。
- README：说明该实验数据包绑定到哪位学生。
## 实验结果的提交
如果学生在攻击过程中保持联网，则不需要提交实验结果。学生在攻击过程中，target程序会自动将信息反馈到服务器记录，并实时更新当前得分状况。查看实时得分状况，<a href="liqingan.cn:15513/scoreboard"><font size=5>点击这里</font></a>。

## 郑重说明
凡是用学号领取的实验，服务器上都有记录，每个同学唯一。不要使用别人的target，否则服务器进行答案比较时，会算成0分。因为这种行为系作弊行为，拒绝申诉和二次考核。