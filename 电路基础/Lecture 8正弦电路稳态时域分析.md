# Lecture 8 正弦电路稳态时域分析

[TOC]

![image-20220425174426678](https://s2.loli.net/2022/04/25/PVFo7RI5TptKCjB.png)

$$V_S(t)=V_mcos(wt+\phi)$$,Find steady state current i(t)

Method 1:(From Lec.5)
$$
\begin{cases}
\displaystyle\frac{di(t)}{dt}+\frac{R}{L}i(t)=V_mcos(wt+\phi)
\\i(t)|_{t=0^+}=i(t)|_{t=0}
\end{cases}\ \ \ \ \ \ 用一阶电路微分方程的方法解
$$
Method 2:(From Lec.7)
$$
L\frac{di(t)}{dt}+Ri(t)=V_mcos(wt+\phi)\xrightarrow{Phasor\ Domain}L(jw\widetilde I)+R\widetilde I=V_m\ang\phi
\\\Longrightarrow\widetilde I=\frac{V_m\ang\phi}{R+jwL}\Longrightarrow i(t)=xxx
$$
**Method 3:(From Lec.8)**

Equvalent to Method 2.

用某种类似于欧姆定律的定律$$\\\Longrightarrow\widetilde I=\frac{V_m\ang\phi}{R+jwL}$$

## 1.phasor Relation ships for resistor,inductor&capacitor(RLC)

### 1.1 Resistor 

$$
V(t)=Ri(t)&&&&&&\widetilde{V}=R\widetilde{I}\\
If\ i(t)=I_mcos(wt+\phi)&&&\Longrightarrow&&&\widetilde{V}=I_m\ang\phi
\\V(t)=RI_mcos(wt+\phi)&&&&&&\widetilde{V}=RI_m\ang\phi
$$

### 1.2 Inductor

$$
V(t)=L\frac{di(t)}{dt}&&&&&&\widetilde{V}=jwL\widetilde{I}\\
V(t)=-wLI_msin(wt+\phi)&&&\Longrightarrow&&&\widetilde{I}=I_m\ang\phi
\\V(t)=wLI_mcos(wt+\phi+90\degree)&&&&&&\widetilde{V}=wLI_m\ang\phi+90\degree=jwLI_m\ang\phi
$$

### 1.3 Capacitor

$$
i(t)=C\frac{dV(t)}{dt}&&&&&&\widetilde{I}=jwC\widetilde{V}\\
i(t)=-CwV_msin(wt+\phi)&&&\Longrightarrow&&&\widetilde{V}=V_m\ang\phi
\\i(t)=CwV_mcos(wt+\phi+90\degree)&&&&&&\widetilde{I}=jwCV_m\ang\phi+90\degree
$$

### 1.4. Impedance/admittance 阻抗/导纳

Define $\displaystyle z=\frac{\widetilde{V}}{\widetilde{I}},z=R,z=jwL,z=\frac{1}{jwC}$

phasors allow us to express the relationship between current and voltage using a formula like Ohm’s law

在正弦稳态电路中，可像电阻一样表示电感电容，并像电阻一样进行电路分析

$$z=R+jX\longleftrightarrow Y=G+jB$$

impedance阻抗=resistance电阻+reactance电抗

admittance导纳=conductance电导+suceptance电纳

Note:

1.Impedance is not a phasor,but usually a complex number.

2.Impedance is a function of w

![image-20220425095443905](https://s2.loli.net/2022/04/25/ypfJcEZrD4Qb8IK.png)

## 2.Kichhoff’s Laws in phasor Domain.

#### 2.1phasor Domain KVL:

Let $V_1(t),V_2(t),···,V_m(t)$be the voltages around a closed loop

$\widetilde{V_1},\widetilde{V_2},\widetilde{V_3},\widetilde{V_4},···\widetilde{V_n}$are correspongding phasor
$$
then:\widetilde{V_1}+\widetilde{V_2}+\widetilde{V_3}+···+\widetilde{V_n}=0
$$
Proof: From the domain KVL:

$$V_1(t)+V_{2}(t)+V_3(t)+···V_n(t)=0$$

$$Let V_i(t)=V_{mi}cos(wt+\phi)$$

$$V_{m1}cos(wt+\phi)+V_{m2}cos(wt+\phi)+···+V_{mn}cos(wt+\phi)=0$$

$$\Leftrightarrow Re(V_{m1}e^{j\phi}e^{jwt})+Re(V_{m2}e^{j\phi_2}\cdot e^{jwt})+···+Re(V_{mn}e^{jwt})=0$$

$$\Leftrightarrow Re[(\widetilde{V_1}+\widetilde{V_2}+···+\widetilde{V_n})e^{jwt}]=0$$

$$\widetilde{V_1}+\widetilde{V_2}+···+\widetilde{V_n}=0$$



#### 2.2phasor Domain KCL:

Let $I_1(t),I_2(t),···,I_m(t)$be the voltages around a closed loop

$\widetilde{I_1},\widetilde{I_2},\widetilde{I_3},\widetilde{I_4},···\widetilde{I_n}$are correspongding phasor
$$
then:\widetilde{I_1}+\widetilde{I_2}+···+\widetilde{I_n}=0
$$
Proof: From the domain KCL:

$$I_1(t)+I_{2}(t)+I_3(t)+···I_n(t)=0$$

$$Let I_i(t)=I_{mi}cos(wt+\phi)$$

$$I_{m1}cos(wt+\phi)+I_{m2}cos(wt+\phi)+···+I_{mn}cos(wt+\phi)=0$$

$$\Leftrightarrow Re(I_{m1}e^{j\phi}e^{jwt})+Re(I_{m2}e^{j\phi_2}\cdot e^{jwt})+···+Re(I_{mn}e^{jwt})=0$$

$$\Leftrightarrow Re[(\widetilde{I_1}+\widetilde{I_2}+···+\widetilde{I_n})e^{jwt}]=0$$

$$\widetilde{I_1}+\widetilde{I_2}+···+\widetilde{I_n}=0$$



![image-20220427090318114](C:\Users\lcf\AppData\Roaming\Typora\typora-user-images\image-20220427090318114.png)

4.general ac phasor analysis

Rrocedure:

Step 1:

![image-20220427095405885](C:\Users\lcf\AppData\Roaming\Typora\typora-user-images\image-20220427095405885.png)



