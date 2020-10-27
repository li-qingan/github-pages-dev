---
title: 论文阅读类选题参考
layout: defaultCourse
---
# 近期论文
## Android内存管理
- Lebeck N, Krishnamurthy A, Levy H M, et al. End the senseless killing: Improving memory management for mobile operating systems[C]//2020 {USENIX} Annual Technical Conference ({USENIX}{ATC} 20). 2020: 873-887.
- Liang Y, Li J, Ausavarungnirun R, et al. Acclaim: Adaptive memory reclaim to improve user experience in android systems[C]//2020 {USENIX} Annual Technical Conference ({USENIX}{ATC} 20). 2020: 897-910.
  
## 性能分析与评估
- Curtsinger C, Berger E D. Stabilizer: Statistically sound performance evaluation[J]. ACM SIGARCH Computer Architecture News, 2013, 41(1): 219-228.
- Curtsinger C, Berger E D. Coz: Finding code that counts with causal profiling[C]//Proceedings of the 25th Symposium on Operating Systems Principles. 2015: 184-197.【不仅找到hot code，而且找到修改点】

# 经典论文
## 内存分配
- Berger E D, Zorn B G, McKinley K S. Reconsidering custom memory allocation[C]//Proceedings of the 17th ACM SIGPLAN conference on Object-oriented programming, systems, languages, and applications. 2002: 1-12.

## 编译器
- Hopper G M. The education of a computer[C]//Proceedings of the 1952 ACM national meeting (Pittsburgh). 1952: 243-249. 【第一个编译器】
- Backus J W, Beeber R J, Best S, et al. The FORTRAN automatic coding system[C]//Papers presented at the February 26-28, 1957, western joint computer conference: Techniques for reliability. 1957: 188-198.【第一个优化编译器】

## 程序语言
- McCarthy J. Recursive functions of symbolic expressions and their computation by machine, Part I[J]. Communications of the ACM, 1960, 3(4): 184-195. 【Lisp & 第一个GC】
- Dijkstra E W. ALGOL-60 translation[M]. Mathematisch Centrum, 1961. 【第一个优化编译器】
-  Hughes J. Why functional programming matters[J]. The computer journal, 1989, 32(2): 98-107.
-  Hall C, Hammond K, Partain W, et al. The Glasgow Haskell compiler: a retrospective[M]//Functional Programming, Glasgow 1992. Springer, London, 1993: 62-71.


## 程序语言运行时系统
-  Boehm H J, Weiser M. Garbage collection in an uncooperative environment[J]. Software: Practice and Experience, 1988, 18(9): 807-820.【保守GC】
-  Wilson P R. Uniprocessor garbage collection techniques[C]//International Workshop on Memory Management. Springer, Berlin, Heidelberg, 1992: 1-42.【GC综述】
-  Bacon D F, Cheng P, Rajan V T. A unified theory of garbage collection[C]//Proceedings of the 19th annual ACM SIGPLAN conference on Object-oriented programming, systems, languages, and applications. 2004: 50-68.【GC统一模型】

## 性能分析与评估
-  Graham S L, Kessler P B, McKusick M K. gprof: A call graph execution profiler (with retrospective)[C]//Best of PLDI. 1982: 49-57.
-  Mytkowicz T, Diwan A, Hauswirth M, et al. Producing wrong data without doing anything obviously wrong![J]. ACM Sigplan Notices, 2009, 44(3): 265-276.

## 计算机体系结构
-  Amdahl G M, Blaauw G A, Brooks F P. Architecture of the IBM System/360[J]. IBM Journal of Research and Development, 1964, 8(2): 87-101. 【第一篇体系结构论文】
-  Liptay J S. Structural aspects of the System/360 Model 85, II: The cache[J]. IBM Systems Journal, 1968, 7(1): 15-21.【第一个cache】

## 多核与并行
-  Moore, Gordon E. "Cramming more components onto integrated circuits." (1965): 114-117. 【摩尔定律】
-  Amdahl G M. Validity of the single processor approach to achieving large scale computing capabilities[C]//Proceedings of the April 18-20, 1967, spring joint computer conference. 1967: 483-485.【亚当定律）
-  Hill M D, Marty M R. Amdahl's law in the multicore era[J]. Computer, 2008, 41(7): 33-38.【亚当定律】

## 软硬件接口
-  Patterson D A, Ditzel D R. The case for the reduced instruction set computer[J]. ACM SIGARCH Computer Architecture News, 1980, 8(6): 25-33.
-  Clark D W, Strecker W D. Comments on" the case for the reduced instruction set computer," by Patterson and Ditzel[J]. ACM SIGARCH Computer Architecture News, 1980, 8(6): 34-38.
-  Jouppi N P, Wall D W. Available instruction-level parallelism for superscalar and superpipelined machines[J]. ACM SIGARCH Computer Architecture News, 1989, 17(2): 272-282.

## 并发
-  Birrell A D. An introduction to programming with threads[M]. Digital Systems Research Center, 1989.
-  ampson B W, Redell D D. Experience with processes and monitors in Mesa[J]. Communications of the ACM, 1980, 23(2): 105-117.
-  Liu T, Curtsinger C, Berger E D. Dthreads: efficient deterministic multithreading[C]//Proceedings of the Twenty-Third ACM Symposium on Operating Systems Principles. 2011: 327-336.

## 操作系统
-  Dijkstra E W. The structure of “THE”-multiprogramming system[J]. Communications of the ACM, 1983, 26(1): 49-52.
-  Corbató F J, Vyssotsky V A. Introduction and overview of the Multics system[C]//Proceedings of the November 30--December 1, 1965, fall joint computer conference, part I. 1965: 185-196.【动态链接、memory as storage，SCM】
-  Ritchie D M. The UNIX System: The Evolution of the UNIX Time‐sharing System[J]. AT&T Bell Laboratories Technical Journal, 1984, 63(8): 1577-1593.
-  Gabriel R. The rise of “worse is better”[J]. Lisp: Good News, Bad News, How to Win Big, 1991, 2(5).【MIT vs Berkeley风格】

## 网络
-  Saltzer J H, Reed D P, Clark D D. End-to-end arguments in system design[J]. ACM Transactions on Computer Systems (TOCS), 1984, 2(4): 277-288.
-  Clark D. The design philosophy of the DARPA Internet protocols[C]//Symposium proceedings on Communications architectures and protocols. 1988: 106-114.
-  Lampson B W. Hints for computer system design[C]//Proceedings of the ninth ACM symposium on Operating systems principles. 1983: 33-48.

## 并发与排队系统
-  Little J D C. OR FORUM—Little's Law as viewed on its 50th anniversary[J]. Operations research, 2011, 59(3): 536-549.
-  Burns B, Grimaldi K, Kostadinov A, et al. Flux: A language for programming high-performance servers[J]. Computer Science Department Faculty Publication Series, 2006: 53.
-  Lamport L. Time, Clocks, and the Ordering of Events in a Distributed System[J]. Communications, 1978.【向量时钟】
-  Flanagan C, Freund S N. FastTrack: efficient and precise dynamic race detection[J]. ACM Sigplan Notices, 2009, 44(6): 121-133. 【竞争检测】

## 安全
-  Lampson B W. A note on the confinement problem[J]. Communications of the ACM, 
-  1973, 16(10): 613-615.
-  Thompson K. Reflections on trusting trust[J]. Communications of the ACM, 1984, 27(8): 761-763. 【图灵奖获奖演说】
-  Dingledine R, Mathewson N, Syverson P. Tor: The second-generation onion router[R]. Naval Research Lab Washington DC, 2004.
-  Rivest R L, Shamir A, Adleman L. A method for obtaining digital signatures and public-key cryptosystems[J]. Communications of the ACM, 1978, 21(2): 120-126.

## 容错
### 容错硬件
-  Patterson D A, Gibson G, Katz R H. A case for redundant arrays of inexpensive disks (RAID)[C]//Proceedings of the 1988 ACM SIGMOD international conference on Management of data. 1988: 109-116.
-  Gibson B S G A. Disk failures in the real world: What does an MTTF of 1,000,000 hours mean to you?[C]. FAST, 2007.

### 容错软件
-  Gray J. Why do computers stop and what can be done about it?[C]//Symposium on reliability in distributed software and database systems. 1986: 3-12.
-  Nauman J, Bartlett W. Jim Gray's Tandem contributions[J]. ACM SIGMOD Record, 2008, 37(2): 41-44.
-  Berger E D, Zorn B G. DieHard: probabilistic memory safety for unsafe languages[J]. Acm sigplan notices, 2006, 41(6): 158-168.

## 分布式系统
-  Shostak R, Pease M, Lamport L. The byzantine generals Leslie L. The part-time parliament[J]. ACM Transactions on Computer Systems, 1998, 16(2): 133-169.
-  problem[J]. ACM Transactions on Programming Languages and Systems, 1982, 4(3): 382-401.
-  Lamport L. Paxos made simple[J]. ACM Sigact News, 2001, 32(4): 18-25.

## 数据库系统
-  DeWitt D, Gray J. Parallel database systems: the future of high performance database systems[J]. Communications of the ACM, 1992, 35(6): 85-98.
-  Dean J, Ghemawat S. MapReduce: a flexible data processing tool[J]. Communications of the ACM, 2010, 53(1): 72-77.
-  Stonebraker M, Abadi D, DeWitt D J, et al. MapReduce and parallel DBMSs: friends or foes?[J]. Communications of the ACM, 2010, 53(1): 64-71.

## 数据中心
-  Brin S, Page L. The anatomy of a large-scale hypertextual web search engine[J]. 1998.【Google】
-  Corbett J C, Dean J, Epstein M, et al. Spanner: Google’s globally distributed database[J]. ACM Transactions on Computer Systems (TOCS), 2013, 31(3): 1-22.【Google+】

## 代码分析
-  Bessey A, Block K, Chelf B, et al. A few billion lines of code later: using static analysis to find bugs in the real world[J]. Communications of the ACM, 2010, 53(2): 66-75.【静态分析】
-  Nethercote N, Seward J. Valgrind: a framework for heavyweight dynamic binary instrumentation[J]. ACM Sigplan notices, 2007, 42(6): 89-100.【动态分析】

## 测试
-  Miller B P, Fredriksen L, So B. An empirical study of the reliability of UNIX utilities[J]. Communications of the ACM, 1990, 33(12): 32-44.
-  Godefroid P, Klarlund N, Sen K. DART: directed automated random testing[C]//Proceedings of the 2005 ACM SIGPLAN conference on Programming language design and implementation. 2005: 213-223.