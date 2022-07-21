# Lecture 9 AC Power Calculation交流功率计算

## 1.Instanteous power 瞬时功率

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220504083423219.png" alt="image-20220504083423219" style="zoom:33%;" />
$$
V(t)=V_mcos(wt+\theta_v)\\
I(t)=I_mcos(wt+\theta_i)\\
$$
Find the power of the source p(t)
$$
P(t)=V(t)I(t)\\
=V_mI_mcos(wt+\theta_v)cos(wt+\theta_i)\\
=\frac{V_mI_m}2[cos(2wt+\theta_t-\theta_v)+cos(\theta_v-\theta_i)]
$$

### Case 1: Resistive load

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220504084909965.png" alt="image-20220504084909965" style="zoom:50%;" />
$$
z=R\\
\theta_v=\theta_i\\
p(t)=\frac{V_mI_m}2cos(2wt+w\theta v)+\frac{V_mI_m}2
$$
<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220504085114238.png" alt="image-20220504085114238" style="zoom: 50%;" />

### case2:pure capacitive load

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220504085400034.png" alt="image-20220504085400034" style="zoom: 50%;" />
$$
z=\frac1{wC}\ang-90\degree\\
\theta_v-\theta_i=-90\degree\Rightarrow\theta_i=\theta_v+90\degree\\
\Rightarrow p(t)=\frac{V_mI_m}2cos(2wt+2\theta v+90\degree)+\frac{V_mI_m}2cos(-90\degree)
$$

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220504085528073.png" alt="image-20220504085528073" style="zoom:50%;" />

### case3：pure inductive load

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220504150218280.png" alt="image-20220504150218280" style="zoom: 50%;" />
$$
z={wL}\ang90\degree\\
\theta_v-\theta_i=90\degree\Rightarrow\theta_i=\theta_v-90\degree\\
\Rightarrow p(t)=\frac{V_mI_m}2cos(2wt+2\theta v-90\degree)+\frac{V_mI_m}2cos(90\degree)
$$




### 2.real power 有功功率

$$\displaystyle p(t)=\frac{V_mI_m}2[cos(2wt+\theta_t-\theta_v)+cos(\theta_v-\theta_i)]$$

$$\displaystyle \Rightarrow p=\frac1T\int^T_0p(t)dt=\frac{V_mI_m}2cos(\theta_v-\theta_i)$$

![image-20220504090828380](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220504090828380.png)



### 3.Reactive power 无功功率”Q“

Definition: The peak instantous power assocreted with the energy storge elments contained in a general load.

储能元件上面产生的瞬时功率

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220504165458031.png" alt="image-20220504165458031" style="zoom: 67%;" />

$$\displaystyle z=R+jX=|z|\ang\theta_v-\theta_i=|z|cos(\theta_v-\theta_i)+j|z|sin(\theta_v-\theta_i)\\i(t)=I_mcos(wt+\theta_i),v(t)=V_mcos(wt+\theta_v)$$
$$
P_R(t)=i^2(t)\cdot R=I_m^2cos^2(wt+\theta_i)\cdot R\\
=I_m^2R[\frac{1+cos(2wt+2\theta_i)}2]\\
=I_m^2|z|cos(\theta_v-\theta_i)\frac{1+cos(2wt+2\theta_i)}2\\
$$

$$
P_x(t)=P(t)-P_R(t)\\
=\frac{V_mI_m}2cos(2wt+\theta_v+\theta_i)+\frac{V_mI_m}2cos(\theta_v-\theta_i)-\frac{V_mI_m}2cos(\theta_v-\theta_i)[1+cos(2wt+2\theta_i)]\\
=\frac{V_mI_m}2sin(\theta_v-\theta_i)\cdot sin(2wt+2\theta_i+\pi)
$$

$$\displaystyle \Rightarrow Q=\frac1T\int^T_0p_x(t)dt=\frac{V_mI_m}2sin(\theta_v-\theta_i)$$


$$
p(t)=\frac{V_mI_m}2cos(2wt+\theta_v+\theta_i)+\frac{V_mI_m}2cos(\theta_v-\theta_i)=P_R(t)+P_x(t)\\
=\frac{V_m\cdot I_m}2[cos(\theta_v-\theta_i)[1+cos(2wt+2\theta_i)]+sin(\theta_v-\theta_v)sin(2wt+2\theta_i+\pi)]
$$


### 物理意义

$$
Real Power(有功功率):\begin{cases}
Average\ of\ p(t)总功率的平均值,或Average\ of\ P_R(t)消耗在电阻上的平均值\\
Peak\ instaneous\ power\ associated\ with\ the\ energy\ dissipation\ dements(oscillating\ part)
\end{cases}
$$

$$Reactive\ power:peak\ instaneous\ power\ associated\ with\ the\ energy\ storage\ elments$$



### 4 complex power,Apporant power and power factor

### 复功率         视在功率 

$$\widetilde V=V_m\ang \theta_v\\\widetilde I=I_m\ang\theta_i\\P=\frac{V_mI_m}2cos(\theta_v-\theta_i),Q=\frac{V_mI_m}2sin(\theta_v-\theta_i)$$



We can observe:

$$\widetilde V\cdot\widetilde I^*=\frac12V_mI_m\ang\theta_v-\theta_i=\frac12cos(\theta_v-\theta_i)+j\frac12V_mI_msin(\theta_V-\theta_i)=P+jQ$$

Define :a single power power metric to include both P & Q

complex power:$$S=\frac12\widetilde V\cdot\widetilde I=\widetilde V_{rms}\cdot\widetilde I_{rms}$$

$$P=Re(s),Q=I_m(s)$$



### 视在功率

Apprent Power:P(t)波动项的峰值

$$S_R=|S|=\frac{V_mI_m}2=V_{rms}I_{rms}$$

Define：power factor

p.f=$$\frac{P}{S_a}=cos(\theta_V-\theta_i)$$
$$
\theta_V-\theta_i=\begin{cases}
>0,current\ lags\ voltage\\
<0,current\ lags\ voltage
\end{cases}
$$
