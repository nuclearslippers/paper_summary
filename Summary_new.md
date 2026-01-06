# 新出论文总结

本文档主要记录新出的论文（包括大量ArXiv预印本），主要是学习思路和方法，其具体水平还有待时间检验。

## 目录
| 简称 | 发表信息 | 核心贡献描述 | 具体信息 | 传感器 | 其他 |
|-----|--------------|----------------------------------|----------|--------------|------|
| RobMOT+ | ArXiv 2025.5 | 提出动态调整运动模型的思路 | [查看](#RobMOT+) | 3D+2D |  |
| DIMM | ArXiv 2025.5 | IMM改进，强化学习计算转换矩阵，各个方向进行拆分 | [查看](#DIMM) | 3D（未提到传感器） |  |



## 论文详情

<a name="RobMOT+"></a>
### TOWARDS ACCURATE STATE ESTIMATION: KALMAN FILTER  INCORPORATING MOTION DYNAMICS FOR 3D MULTI-OBJECT  TRACKING
- 发表信息: ArXiv 2025.5
- 未开源

#### 核心贡献描述
说是动态模型，不如说是动态调整模型的参数。作者首先使用一个基座运动模型：Jerk模型（一直建模到加加速度）。然后给速度，加速度，加加速度一个权重，通过调整权重来实现模型的动态调整。
而权重的获得，理想情况下是通过目标真实运动状态的差分（及高级差分）获得的。但是真实状态不可得，作者使用去噪的观测值来近似真实状态，从而计算出差分。此外，并非简单差分就是权重，还设置了一个高斯分布，以及归一化来获得权重。

#### 学习收获
作者的运动模型，实质上就是CV,CA,JERK。但是没有考虑到转向模型。不过思路可以借鉴学习，也就是通过后续的真值来动态调整运动模型。
对比作者的上一篇工作，提升真的不高。

<hr style="height: 4px; border: none; background: black;">

<a name="DIMM"></a>
### DIMM: Decoupled Multi-hierarchy Kalman Filter for 3D Object Tracking
- 发表信息: ArXiv 2025.5
- 未开源

#### 核心贡献描述

#### 学习收获

<hr style="height: 4px; border: none; background: black;">





<a name="模板"></a>
### 模板
- 发表信息: 
- 未开源

#### 核心贡献描述

#### 学习收获

<hr style="height: 4px; border: none; background: black;">