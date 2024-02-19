# proj280-Dynamic-escape-accelerator-for-heterogeneous-SoCs
## 标题

面向异构SoC的动态转义加速器设计与实现

## 项目描述

软硬件结合的异构SoC或FPGA+CPU的异构系统是未来发展方向之一，已有许多产品被用于数据中心等场景进行算法加速。比如Xilinx公司的FPGA+ARM架构SoC，Intel公司的可扩展处理器、苹果公司最新研发的头戴式VR设备Vision Pro也采用了异构系统的方式处理不同需求的数据流。软件（CPU、GPU）与硬件（如FPGA）擅长处理的数据有很大的不同，并行性、时间精度控制上也有较大的差异。但想充分利用好系统中的软硬件资源需要协同软硬件开发人员，研发难度较高。一方面，异构计算套件通常面向软件开发人员进行设计，提供的是软件接口。从硬件开发人员的角度来看，若不针对性的开发软件进行适配则难以充分利用CPU资源。但从整体的角度来看，交互的方式通常都类似，如果每一次都需要软硬件协同开发则会影响效率提高成本。另一方面，软硬件的交互方式较为单一，在硬件中想要使用软件资源，通常只能采用等待的方式，造成流水线断流，不适用于持续大数据流的应用。如何解决上述问题，以低成本的方式将软硬件两者的优势结合可以提高异构SoC的资源利用率，降低产品成本。
 


## 预期目标

技术路线一：设计一种模块，能够在编译时对高级程序代码进行分析，将不同的计算放到FPGA与CPU中，形成FPGA可加载的bitstream与CPU可执行程序，并根据定义的接口规范自动形成信息交互接口。特征是强调增量式与透明，即可以根据当前设备配置的FPGA体积动态、增量配置转义到FPGA上运行的功能，最大化FPGA资源利用；且只要求开发者具备软件开发能力。

技术路线二：设计一种模块，能够针对正在执行或将要执行的软件进行指令级别的分析，将部分计算动态加载到FPGA中。其他特征与技术路线一一致。

## 特征

> 描述项目的特征。 

1. 文档、代码、问题、答疑交互过程都开放和开源的
2. 支持Xilinx公司的异构SoC（如zynq7000等）。


## 已有参考资料

1. Programming and Synthesis for Software-defined FPGA Acceleration: Status and Future Prospects： https://www.sfu.ca/~zhenman/files/J6-TRETS2021-SDA-Survey.pdf
2. Userspace Bypass: Accelerating Syscall-intensive Applications： https://www.usenix.org/system/files/osdi23-zhou-zhe.pdf

## 赛题分类

系统调试/支撑库的设计

## 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的本科生或研究生
- 允许学生参加大赛的多个不同题目，最终自己选择一个题目参与评奖
- 请遵循“2024全国大学生操作系统比赛”的章程和技术方案要求

## 难度

高等

## License

GPL-3.0 License

## 所属赛道

2024全国大学生操作系统比赛的“OS功能挑战”赛道

## 项目导师

- 姓名：吴竞邦
- 单位：北京工商大学
- github ID：[https://github.com/wujingbang](https://github.com/wujingbang)
- email：[wujingbang@btbu.edu.cn](mailto:wujingbang@btbu.edu.cn)
