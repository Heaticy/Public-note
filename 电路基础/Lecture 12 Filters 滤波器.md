## Lecture 12 Filters 滤波器

1.Definition

Circuit designed to retain certain frequency range but discard or attenuate others.

Low-pass filter 低通

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220523094233195.png" alt="image-20220523094233195" style="zoom: 80%;" />

High-pass filter 高通

![image-20220523094301050](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220523094301050.png)

Band-pass filter 带通

![image-20220523094316729](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220523094316729.png)

Band-reject filter 带阻(陷波)

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220523094352417.png" alt="image-20220523094352417" style="zoom: 33%;" />

## 2.passive Filters 无源滤波器

A filter is passive if it only consists of passive elemeents RLC

### 2.1 First order RC low-pass filter

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220523094822914.png" alt="image-20220523094822914" style="zoom: 50%;" />
$$
H(w)=\frac{\widetilde V_0}{\widetilde V_i}=\frac{\frac1{jwC}}{R+\frac1 {jwC}}=\frac1 {1+jwRC}=\frac1{1+j\frac w{w_0}}
$$
<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220523095120702.png" alt="image-20220523095120702" style="zoom:50%;" />

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220523095156135.png" alt="image-20220523095156135" style="zoom:33%;" />



## 2.2 First-order RC High pass Filter

![image-20220525082651862](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525082651862.png)
$$
H_R(w)=\frac{\widetilde v_0}{\widetilde v_i}=\frac{R}{R+\frac1{jwC}}
$$
<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525082952312.png" alt="image-20220525082952312" style="zoom: 50%;" />

## 2.4 RLC filters

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525084018101.png" alt="image-20220525084018101" style="zoom:50%;" />
$$
\widetilde{I}=\frac{\widetilde{V_S}}{R+jwL+\frac1{jwC}}
$$
![image-20220525084530398](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525084530398.png)

![image-20220525084639407](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525084639407.png)

![image-20220525090005481](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525090005481.png)

![image-20220525090152422](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525090152422.png)

## 3 Active Filters 有源滤波器


$$
limitation\ of\ passive\ filters.\\
\begin{cases}
limited\ gain增益限制\\
may\ require\ bulky\ and\ expensive\ inductor电感太大太贵了\\
output\ influenced\ by\ the\ load负载影响滤波器
\end{cases}\  \
$$
<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525091358134.png" alt="image-20220525091358134" style="zoom:50%;" />

![image-20220525092036324](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525092036324.png)

![image-20220525092357712](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525092357712.png)

![image-20220525093208812](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525093208812.png)

![image-20220525095501107](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525095501107.png)

![image-20220525095336900](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220525095336900.png)