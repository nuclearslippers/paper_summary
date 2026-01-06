# 📚 滤波相关论文总结

## 目录表格
|       简称        | 发表信息 | 核心贡献描述                     | 具体信息 |  其他   |
|----------------------|--------------|----------------------------------|-------------|------|
| Dynanet      | TNNLS2021 | kalman引入神经网络       | [查看](#dynanet) | - |
| Kalmannet | TSP2022  | 构建了kalmannet，用来估计KG，噪声未知，模型可以不准确 | [查看](#kalmannet) | - |
| bayesian kalmannet | TSP2025 | 从bayesian角度看待DNN辅助的卡尔曼滤波 | [查看](#bayesian) | - |
| DLBRMOT | TITS2024 | Bi-LSTM来构建运动模型 | [查看](#DLBRMOT) | - |
| ODR | ICRA2021 | - | [查看](#ODR) | 不确定 |
| ESER | IROS2023 | - | [查看](#ESER) | 不确定 |


## DynaNet: Neural Kalman Dynamical Model for Motion Estimation and Prediction
### 🌟 基本信息
- 开源地址：不开源，但是通过关系要到源码了
- 发表信息：IEEE Transactions on Neural Networks and Learning Systems ( Volume: 32, Issue: 12, December 2021)
![基本框架](./frame_work/dynanet.png)


### 🎯 核心内容
- 将卡尔曼滤波扩展到神经网络，一方面有效果，还有一定的理论依据。

### 💡 学习收获

### 😃 其他  
- 陈老师直接给了源码😋，但是一直没复现被批好几回😭



<hr style="height: 4px; border: none; background: black;">

<a id="kalmannet"></a>
## KalmanNet: Neural Network Aided Kalman Filtering for Partially Known Dynamics
### 🌟 基本信息
- 开源地址：https://github.com/KalmanNet/KalmanNet_TSP
- 发表信息：IEEE Transactions on Signal Processing


<hr style="height: 4px; border: none; background: black;">


<a id="bayesian"></a>
## Bayesian KalmanNet: Quantifying Uncertainty in Deep Learning Augmented Kalman Filter
### 🌟 基本信息
- 开源地址：未开源
- 发表信息：IEEE Transactions on Signal Processing 2025


<hr style="height: 4px; border: none; background: black;">

<a id="DLBRMOT"></a>
## Deep Learning-Based Robust Multi-Object Tracking via Fusion of mmWave Radar and Camera Sensors
### 🌟 基本信息
- 开源地址：未开源
- 发表信息：IEEE Transactions on Intelligent Transportation Systems 2024

### 🎯 核心内容
- 融合了mmWave雷达和摄像头，通过深度学习来实现MOT
- 采用了一个基于Bi-LSTM的运动模型


<hr style="height: 4px; border: none; background: black;">

<a id="ODR"></a>
## Out-of-Distribution Robustness with Deep Recursive Filters
### 🌟 基本信息
- 开源地址：未开源
- 发表信息：2021 IEEE International Conference on Robotics and Automation (ICRA)

<hr style="height: 4px; border: none; background: black;">

<a id="ESER"></a>
## Enhancing State Estimation in Robots: A Data-Driven Approach with Differentiable Ensemble Kalman Filters
### 🌟 基本信息
- 开源地址：https://github.com/ir-lab/DEnKF
- 发表信息：2023 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)