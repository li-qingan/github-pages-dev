---
title: 调研类选题参考
layout: defaultCourse
---

## TPU/NPU优化
### 内容建议
- TPU/NPU中的各类并行的分类
- TPU/NPU中的各类并行的实现
- TPU/NPU中各类并行的效果评测或调研,比如指令内并行、指令级并行
- TPU/NPU中各类并行与CPU、GPU的区别
- 不足与展望

## 分支预测算法现状及发展
### 内容建议
分支跳转不仅会导致硬件流水停顿，也会限制指令级和线程级的并发。良好的分支预测方法，会大大改善并行性能。
- 分析已有的硬件分支预测方法及其应用；
- 分析已有的软件分支预测方法及其应用；
- 比较硬件方法与软件方法之间的联系与区别，讨论二者之间的融合趋势；

### 参考
- 《计算机体系结构：一种量化方法》第4版、第6版
- LLVM、GCC中的静态分支预测方法和动态预测方法
- https://easyperf.net/blog/2019/05/06/Estimating-branch-probability
- Wu Y. Optimizing compiler with static prediction of branch probability, branch frequency and function frequency: U.S. Patent 5,655,122[P]. 1997-8-5.

## 内存访问模式识别和预测方法
进程的逻辑地址空间有不同的访问模式，比如栈空间、堆空间的读写区别、冷热区别；OS中的物理页面也有不同的访问模式，比如读写区别、冷热区别；OS中的进程也有不同的访问模式，比如计算密集、访存密集。
- 从上述三种场景中选择1种，调研其现状、应用场合、及未来趋势。

## JIT编译优化
### 内容建议
- Java虚拟机中的JIT优化或Android虚拟机中的JIT优化
- 面临的问题
- 虚拟机中JIT优化的历史与现状
- 详细解释1-2个最感兴趣的优化方法，比如给予Profiling的编译优化方法
- 现有的JIT方法的不足和展望->为何新的Android ART引入AoT编译？
- 
### 参考
- https://en.wikipedia.org/wiki/Just-in-time_compilation
- google/百度： Java JIT, android JIT
- 博客（英文优先）
- 学术论文：google scholar/百度学术

## JIT编译的安全隐患及防范
### 内容建议
- 原因分析
- 安全攻击方法
- 对应的防范方法
- 实验评估
- 
### 参考
https://en.wikipedia.org/wiki/JIT_spraying


## GC环境下的内存泄漏
### 内容建议
1. GC环境下有无内存泄漏？为什么？
2. GC环境下内存泄漏的解决办法有哪些？
3. 具体到一个场景，比如Java应用，或者Android应用，有哪些常见的因素导致内存泄漏？
4. 在该场景下，内存泄漏的解决方法是什么？
5. 结合2和4，你觉得当前场景下，还可以做哪些改进，进一步解决内存泄漏？
6. 实验评估
   
### 参考
- https://medium.com/swlh/an-introduction-to-memory-management-and-memory-leaks-on-android-3dbd66d8a943
- https://android.jlelse.eu/9-ways-to-avoid-memory-leaks-in-android-b6d81648e35e
  
## 一种数据结构或算法的工业级实现
### 内容建议
阅读并理解一种数据结构或者一种算法的源码实现，详细介绍该实现中的几个要点，据此谈谈这些要点对性能、安全等方面的影响；并谈谈自己的收获。
比如，阅读并理解《STL源码剖析》中“4.2 vector”，详细介绍几个vector的实现要点，据此谈谈vector的性能、安全等特点，并提供实验评估；谈谈自己的收获。

### 参考
- 侯捷. STL源码剖析[M]. 华中科技大学出版社, 2002.

## IDE常见优化选项分析
### 内容建议
- 选择一款常用的IDE，找出其中优化有关的选项和配置；
- 解释这些优化有关的选项和配置；
- 尝试分析1-2种主要优化选项背后的优化算法；
- 尝试评估使用几种优化选项前后的效果。
- 比如，分析Visual Studio；IntelliJ IDEA中的优化选项
  
## 协程与线程的性能分析
### 内容建议
介绍协程的概念，以及几种主流的协程实现方式；
分析协程与线程的关系；
尝试写几个测试程序，分别使用协程和线程；
根据测试程序，对比分析协程与线程的性能特点。

### 参考
https://en.wikipedia.org/wiki/Coroutine
## 编译优化算法分析
### 内容建议
- 介绍一种编译优化算法；
- 介绍该算法的历史与后续发展；
- 介绍该优化算法在主流编译器的应用状况；
- 尝试通过实例分析该算法的优化效果。
  
### 参考
- https://gcc.gnu.org/onlinedocs/gcc/Optimize-Options.html
- https://en.wikipedia.org/wiki/Optimizing_compiler
- https://llvm.org/docs/Passes.html

