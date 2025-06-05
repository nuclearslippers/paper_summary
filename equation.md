# ✒️ 论文公式总结

## 目录
<center>

| 公式名 | 详情 |
| ----- | ----- |
| GIoU | [详情](#GIoU) |
| L2 distance | [详情](#L2-distance) |
| Kalman Filter | [详情](#kf) |
| Extended Kalman Filter | [详情](#ekf) |
</center>


<a id="GIoU"></a>
### GIoU
<center>

$GIoU = IoU_{3d} - \frac{V_c - U}{V_c}$

其中，$V_c$代表能够包含两个框的最小立方体体积。$U$代表两个检测框的交集体积。
</center>

<hr style="height: 4px; border: none; background: black;">

<a id="L2-distance"></a>
### L2 distance
L2距离是简单的欧几里得距离。
<center>

$D_{\text{L2}}(\mathbf{x}, \mathbf{y}) = \sqrt{\sum_{i=1}^n (x_i - y_i)^2}$
</center>

<a id="kf"></a>
### Kalman Filter
Kalman滤波器是一种用于预测和估计动态系统的状态的滤波方法。下面是它在MOT中的常见形式。（CV/CA模型）
<center>

$$
\begin{align*}
x_{\text{pre}} &= A \cdot x \\
P_{\text{pre}} &= A \cdot P \cdot A^T + Q \\
K_k &= P_{\text{pre}} \cdot H^T / (H \cdot P_{\text{pre}} \cdot H^T + R) \\
x &= x_{\text{pre}} + K_k \cdot (z - H \cdot x_{\text{pre}}) \\
P &= (I - K_k \cdot H) \cdot P_{\text{pre}}
\end{align*}
$$
</center>
注意，filterpy库中的实现是略有不同的。对于最后一个公式，它进行了一定的修正。


<hr style="height: 4px; border: none; background: black;">

<a id="ekf"></a>
### Extended Kalman Filter
扩展卡尔曼滤波器是基于普通卡尔曼滤波器的扩展，用于处理非线性系统。其原理是对模型进行泰勒一阶展开，从而处理非线性系统。下面是对常用非线性模型CTRV的扩展卡尔曼滤波器的数学公式。
<center>

$$
\begin{align*}
x_{pre} &=
\begin{bmatrix} 
x_{pre} \\ y_{pre} \\ v_{pre} \\ \theta_{pre} \\ \omega_{pre} 
\end{bmatrix} = 
x + 
\begin{bmatrix} 
\frac{v}{\omega} \left( \sin(\omega \cdot \text{dt} + \theta) - \sin(\theta) \right) \\
\frac{v}{\omega} \left( \cos(\theta) - \cos(\omega \cdot \text{dt} + \theta) \right) \\
0 \\
\omega \cdot \text{dt} \\
0
\end{bmatrix} \\
P_{\text{pre}} &= J \cdot P \cdot J^T + Q \\
K_k &= P_{\text{pre}} \cdot J_h^T / (J_h \cdot P_{\text{pre}} \cdot J_h^T + R) \\
x &= x_{\text{pre}} + K_k \cdot (z - h(x_{\text{pre}})) \\
P &= (I - K_k \cdot J_h) \cdot P_{\text{pre}}
\end{align*}
$$
</center>

