---
title: organization course
layout: defaultCourse
---

# Computer Organization课程网站
## 课程内容
本课程介绍计算机的基本概念，包括数据的表示、指令集基础；介绍计算机基本运算的实现，包括整数与浮点数的加减法、乘除法。重点介绍计算机基本部件的设计与实现，包括CPU与存储器的结构与设计。

## 教材
- Patterson, David A., and John L. Hennessy. Computer organization and design MIPS edition: the hardware/software interface. Newnes, 2013.
- 《计算机组成与设计：软硬件接口》第五版
  
## 课程大纲
### 1. Chapter 1

1.2 Eight great ideas

1.3 C code -> assembly code -> binary code

**1.6 Performance: CPI * InstCount * Cycle time**

1.7 Power wall

### 2. Chapter 2
2.2 Arithmetic operations of MIPS

**2.3 Operands of MIPS**

**2.4 Signed and unsigned numbers: integer representation**

**2.5 Instruction representation: 3 types of Insts**

    Fig. 2.6, Fig 2.17


**2.7 Instructions for Making decision**

2.8 Supporting Procedures in MIPS

2.11 Translating and staring a program

2.12 A C Sort example

### 3. Chapter 3

3.3. Multiplication

3.4 Division

**3.5 Floating Point**

3.6 Subword Parallelism

### 4. Chapter 4
4.2 Logic Design Conventions

**4.3 Building a datapath**

**4.5 An Overview of pipelining**

4.9 Exceptions 

4.10 Parallelim via instructions: ILP (pipeline + multi-issue)
### 5. Chapter 5
**5.1 Introduction: Locality**

**5.3 The basics of Cache**

**5.4 Measure cache performance**

**5.7 Virtual memory**

**5.8 A Comman Framework for Memory Hierarchy: caching and virtual memory**

5.14 Cache blocking
### 6. Chapter
6.2 Difficulty in parallel programming

6.3 SISD, SIMD, MISD, SPMD and vector

6.4 hardware multithreading

6.5 multicore

6.12 Multiple processors

## Concept figures
1. Memory Hierachy
![Alt text](https://g.gravizo.com/source/custom_mark10?https%3A%2F%2Fli-qingan.github.io%2Fcourse%2FcomputerOrganization%2Findex.md)
<details> 
<summary></summary>
custom_mark10
digraph graphname{
    {
        node [shape=box]
        regFile[rank =same, label="register file"]
        cache[rank=same, label="cache", fixedsize=true, width=2]
        mem[rank=same, label="memory", fixedsize=true, width=3]
        disk[rank=same, label="disk", fixedsize=true, width=4]
    }

    regFile -> cache [ label="store inst", tailport=sw, headport=nw]
    cache -> mem [label="cache replacement", tailport=sw, headport=nw]
    mem -> disk [ label = "page replacement", tailport=sw, headport=nw]

    disk -> mem [ label="page fault", tailport=ne, headport=se]
    mem -> cache [label ="cache miss", tailport=ne, headport=se]
    cache -> regFile [label="load inst", tailport=ne, headport=se]
}
custom_mark10
</details>



