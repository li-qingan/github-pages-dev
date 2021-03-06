---
layout: post
title:  "主办 2018 Workshop on Storage and Neural Network Accelerators"
date:   2018-5-21 8:01:59 +0800
categories: Workshop
---
2018 Workshop on Storage and Neural Network Accelerators

# Program

时间：2018年5月21日，星期一

地点：湖北省武汉市，武汉大学，计算机学院E202会议室

联系人：李清安 qingan@whu.edu.cn

| Time | Title & Speaker |
| :- | :- |
|8:30 - 9:00 |大学的创新之路 <br>*Prof. Kuo Tai-Wei, National Taiwan University (台湾大学)*
|9:00 - 9:30	| System Innovation for Mobile & IoT Applications<br>*Prof. Hsiu Pi-Cheng, Academia Sinica, Taiwan (台湾中央研究院)*
|9:30 - 10:00 |	KVSSD: Close Integration of LSM Trees and Flash Translation Layer for Write-Efficient KV Store<br>*Prof. Chang Li-Pin, National Chiao Tung University (台湾交通大学)*
|10:00 - 10:20 |	Break
|10:20 - 10:40	| Energy Efficient Neural Network Accelerators for IoT Applications<br>*Prof. Liu Yong-Pan, Tshinghua University (清华大学)*
|10:40 - 11:00	| File Fragmentation in Mobile Devices: Measurement, Evaluation, and Treatment<br>*Prof. Xue Jason Chun, City University of Hongkong (香港城市大学)*
|11:00 - 11:20 | A Peripheral Circuit Reuse Structure Integrated with a Retimed Data Flow for Low Power RRAM Crossbar-based CNN<br>*Prof. Qiu Ke-Ni, Capital Normal University (首都师范大学)*
|11:20-11:40 |	Applying Multiple Level Cell to Non-volatile FPGAs<br>*Prof. Zhao Meng-Ying, Shandong University (山东大学)*


# Program details

## Kuo Tai-Wei, National Taiwan University

### Title

大学的创新之路

### Abstract

大学创新教育需要挑战与突破以往教学的领域和既有框架，不仅应补足学生较缺乏创意与创新思维的领域课程，更应该培育与激发学生具备创业家精神，甚至借由执行创业的平台，让创新专案借此萌芽。而它的成功与否也在于如何根植于一个适当的创新创意创业生态体系，结合「创业家论坛」等活动，连结新创青年与创业前辈之间的连结，整合校外资源，提供经验传承与资源分享，形成属于大学新创的特色社群。

### Bio

Dr. Kuo is an ACM Fellow and an IEEE Fellow and is now an executive committee member of the IEEE Technical Committee on Real-Time Systems and the Vice Chair of SIGAPP. He also served as a member in the IEEE Fellow Evaluation Committee (Computer Society, 2011, 2013). He received the TECO Award in 2015, the Distinguished Research Award from the ROC National Science Council/Ministry of Science and Technology in 2003, 2011, and 2014, the Distinguished EE Professor Award from the Chinese Institute of Electrical Engineering in 2007, the ROC Ten Young Outstanding Persons Award in 2004, the Young Research Investigators Award from Academia Sinica, Taiwan, ROC, in 2001, and the Investigative Research Award from the Pan Wen Yuan Foundation, Taiwan, ROC, in 1999, and received teaching awards from the National Taiwan University in 2003, 2004, 2005, 2010, 2011, 2012, 2014, and 2015, including the Distinguished Teaching Award (top 1%; 2005). Prof. Kuo was a chair of the Embedded Systems Group of the Networked Communication Program Office and served as an independent board director of the Genesys Logic and the MStar Semiconductor, leading companies in IC designs for display, smartphones, wireless communication, USB, and flash-memory controllers and with the total annual revenue over 1 billion US dollars. He is the Program Director of the Computer Science Division of the ROC National Science Council/Ministry of Science and Technology since January 2013.

## Hsiu Pi-Cheng, Academia Sinica, Taiwan
### Title

System Innovation for Mobile & IoT Applications

### Abstract

Mobile computing has led to paradigm shifts in user behavior, application semantics, and device features. However, hasty software solutions that borrow legacy designs directly from conventional operating systems developed originally for desktops are not suitable for mobile systems intended for smartphones, tablets, wearables, or IoT devices, particularly in conjunction with cloud computing. We have been conducting scientific and engineering research to seek to affect the future designs of mobile and IoT systems. In this talk, I will give our research landscape and present several original design concepts for cloud-based energy saving services, user-centric mobile systems, and multi-device IoT applications. I will also demonstrate our prototype implementations on CHT hicloud, Android smartphones, and TI embedded devices to validate the practicality of the designs.

### Bio

Pi-Cheng Hsiu received the Ph.D. degree in computer science and information engineering from National Taiwan University, Taiwan, in 2009. He is currently a Research Fellow and Deputy Director of the Research Center for Information Technology Innovation (CITI), where he leads the Embedded and Mobile Computing Laboratory (EMCLab), and is also a Joint Research Fellow with the Institute of Information Science (IIS), Academia Sinica, Taiwan. He was a Visiting Scholar with the Department of Computer Science, University of Illinois at Urbana-Champaign, USA, in 2007. Dr. Hsiu joined CITI as an Assistant Research Fellow in 2009, and was promoted to an Associate Research Fellow in 2013 and to a Research Fellow in 2018. He serves as an Associate Editor of the ACM Transactions on Cyber-Physical Systems and in the Organizing/Program Committees of many international conferences in his field, such as IEEE/ACM ISLPED. His research interests include embedded systems, mobile systems, and real-time systems. He is a senior member of the IEEE and a senior member of the ACM.

## Chang Li-Pin, National Chiao Tung University
### Title

KVSSD: Close Integration of LSM Trees and Flash Translation Layer for Write-Efficient KV Store

### Abstract

Log-Structured-Merge (LSM) trees are a writeoptimized data structure for lightweight, high-performance KeyValue (KV) store. Solid State Disks (SSDs) provide acceleration of KV operations on LSM trees. However, this hierarchical design involves multiple software layers, including the LSM tree, host file system, and Flash Translation Layer (FTL), causing cascading write amplifications. We propose KVSSD, a close integration of LSM trees and the FTL, to manage write amplifications from different layers. KVSSD exploits the FTL mapping mechanism to implement copy-free compaction of LSM trees, and it enables direct data allocation in flash memory for efficient garbage collection. In our experiments, compared to the hierarchical design, our KVSSD reduced the write amplification by 88% and improved the throughput by 347%

### Bio

Li-Pin Chang received a M.S.E and a Ph.D. degree in Computer Science and Information Engineering from National Taiwan University, Taiwan, in 1997 and 2003, respectively. He is currently a Professor at Department of Computer Science, National Chiao Tung University, Taiwan. He was a visiting scholar with Fulbright Scholarship in University of Minnesota in 2015. His research interest involves operating systems, storage systems, non-volatile memory, and mobile devices.

## 刘勇攀, 清华大学
### Title

Energy Efficient Neural Network Accelerators for IoT Applications

### Abstract

In this talk, two energy efficient neural network accelerators will be presented for low power IoT applications. The first accelerator proposes a kernel-optimized CNN architecture and an online training FC architecture. A 3x3 kernel-optimized architecture is implemented as a proof-of-concept, and the energy efficiency of which is 4.01x better than the state-of-the-art CNN processor. Furthermore, the proposed online training architecture further reduces parameters update operations by five orders of magnitude for IoT applications. Silicon implementation shows that the energy efficient can be up to 3.77Tops/W. The second accelerator aims at the energy harvesting wearable IoT devices. The accelerator employs RRAM-based nonvolatile logics (NVL) with self-write-termination scheme and low-power processing-in-memory (PIM) to achieve energy-efficient computing against frequent power-off situations. A test chip was fabricated in 150nm CMOS process using HfO RRAM. It achieves 462GOPs/J energy efficiency at 20MHz clock frequency.

### Bio

Dr. Yongpan Liu is an associate professor in Tsinghua University. He has been a visiting scholar at Penn State University and City University of Hong Kong. He is a key member of Tsinghua-Rohm Research Center and Research Center of Future ICs. His research interests include low power design, emerging circuits and systems and design automation. He published over 100 papers and designed several sensor chips, including the first nonvolatile processor (THU1010N). He is an IEEE senior member and served on TPC of (DAC, ASP-DAC, ISLPED, A-SSCC, ICCD, VLSI-D, VLSI-DAT, etc) and has received Design Contest Awards from (ISLPED2012, ISLPED2013), IEEE Micro Top Pick 2016 and best paper awards of HPCA2015 and ASP-DAC2017 and Under 40 Innovation Award of DAC 2017. He served as the publicity co-chair of ICCD15,16 and the exhibition chair of A-SSCC15 and one of the founders of Asia Workshop on Smart Sensor System.

## Xue Jason Chun, City University of Hong Kong

### Title

File Fragmentation in Mobile Devices: Measurement, Evaluation, and Treatment

### Abstract

Mobile devices, such as smartphones, have become a necessity in our daily life. However, users may notice that after being used for a long time, mobile devices begin to exhibit sluggish response. Based on an empirical study on a collection of aged smartphones, this work identified that file fragmentation is among the key factors that contribute to the progressive degradation of response time. This study takes a three-step approach: First, this study designed a set of reproducible file-system aging processes based on User-Interface (UI) script replay. Through the aging processes, it confirmed that file fragmentation quickly emerged, and SQLite files were among the most severely fragmented files. Second, based on the workloads of a selection of popular mobile applications, this study observed that file fragmentation did impact on user-perceived latencies. Specifically, the launching time of Chrome on an aged file system was 79% slower than it was on a pristine file system. Third, this study evaluated existing treatments of file fragmentation, including space preallocation, and file defragmentation to understand their efficacies and limitations. This study also evaluated a state-of-the-art defragmenter to show its advantage over the existing methods.

### Bio

Dr. Chun Jason Xue is an Associate Professor at City University of Hong Kong Computer Science Department. His research interests include non-volatile memories, embedded and realtime systems. He is currently Associate Editor for ACM Transaction on Embedded Computing Systems, Associate Editor for ACM Transaction on CPS, Associated Editor for ACM Transaction on Storage. He was the TPC co-chair for LCTES 2015, TPC co-char for ISVLSI 2016, and has served as TPC members in premiere conferences such as DAC, DATE, RTSS, RTAS, CODES, EMSOFT and ISLPED.
## 邱柯妮, 首都师范大学

### Title

A Peripheral Circuit Reuse Structure Integrated with a Retimed Data Flow for Low Power RRAM Crossbar-based CNN

### Abstract

Convolutional computations implemented in RRAM crossbar-based Computing System (RCS) demonstrate the outstanding advantages of high performance and low power. However, current designs are energy-unbalanced among the three parts of RRAM crossbar computation, peripheral circuits and memory accesses, and the latter two factors can significantly limit the potential gains of RCS. Addressing the problem of high power overhead of peripheral circuits in RCS, this paper proposes a Peripheral Circuit Unit (PeriCU)-Reuse scheme to meet power budgets in energy constrained embedded systems. The underlying idea is to put the expensive ADCs/DACs onto spotlight and arrange multiple convolution layers to be sequentially served by the same PeriCU. In the solution, the first step is to determine the number of PeriCUs which are organized by cycle frames. Inside a cycle frame, the layers are computed in parallel inter-PeriCUs while sequentially intra-PeriCU. Furthermore, a layer retiming technique is exploited to further improve the energy of RCS by assigning two adjacent layers within the same PeriCU so as to bypass the energy consuming memory accesses. The experiments of five convolutional applications validate that the PeriCU-Reuse scheme integrated with the retiming technique can efficiently meet variable power budgets, and further reduce energy consumption efficiently.

### Bio

Dr. Keni Qiu is currently a Research Associate Professor of the College of Information Engineering at the Capital Normal University. Her research interests include HW/SW co-design for embedded system architecture, non-volatile memory, non-volatile processors and processing-in-memory. She has published papers in the prestigious conferences and journals such as DAC, DATE, ICCD, TC, TCAD, TECS and so on. She won the Best Paper Awards in ICCD’16 and ICESS’17, the Finalist in ISLPED’17 Design Contest.

## 赵梦莹, 山东大学

### Title

Applying Multiple Level Cell to Non-volatile FPGAs

### Abstract

Static random access memory (SRAM) based field programmable gate arrays (FPGAs) are currently facing challenges of limited capacity and high leakage power. To solve this problem, non-volatile memory (NVM) is proposed as the alternative to build non-volatile FPGAs (NVFPGAs). Even though the feasibility of NVFPGA has been confirmed, the utilization of multiple level cells (MLC) has not been fully exploited yet. In this talk, I will introduce our exploration on applying MLC to NVFPGAs. Specifically, we study architecture of MLC based NVFPGAs, and propose five cluster structures, as well as the corresponding working mode supported by MLC based clusters.

### Bio

Mengying Zhao received B.E. degree in School of Computer Science and Technology from Shandong University, China in July 2011, and Ph.D. degree in Department of Computer Science, City University of Hong Kong in July 2015. She is now an Assistant Professor in School of Computer Science and Technology in Shandong University. Her research interests include computer architecture, embedded and real-time systems, and non-volatile memory.