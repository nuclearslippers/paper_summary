# 📚 移动机器人上的多目标追踪论文总结

问题描述：移动机器人限定了后续算法不能依赖深度神经网络，而是采用一些传统建模/滤波的方法。多目标追踪旨在将多个目标（可能是障碍物）进行更好的状态。

## 目录表格
|       简称        | 发表信息 | 核心贡献描述                     | 具体信息 | 传感器       |  其他   |
|----------------------|--------------|----------------------------------|----------|--------------|------|
| Onboard      | IRCA2024 | 小型机器人上的目标感知       | [查看](#onboard) | camera | - |

<a id="onboard"></a>
## Onboard Dynamic-Object Detection and Tracking for Autonomous Robot Navigation With RGB-D Camera
### 🌟 基本信息
- 开源地址：https://github.com/Zhefan-Xu/onboard_detector
- 发表信息：IEEE Robotics and Automation Letters 2024-01

### 🎯 核心内容
- 首先，文章声明自己方法的适用场景是基于深度相机的小型移动机器人，因此不适用于需要深度学习的方法。
- 其次，作者提出这样场景下存在的问题：1.算力不足。2.FOV有限，近处的目标和远处的目标都较难识别。3.检测的噪声的影响非常大。
- 针对上述问题，文章给出了解决方案。1.两个简单的检测方法同时进行（UDepth,DBSCAN），附带一个可选的简单神经网络模型。2.采用了新的基于特征的数据关联方法进行卡尔曼滤波的追踪。这个特征其实只是添加了目标的尺度这些信息。3.提出了如何分辨动静目标的方法。

<hr style="height: 4px; border: none; background: black;">