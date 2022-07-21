# Lecture 7 Phaser 相量

[TOC]



## 1.motivation

Find sinusoidal response:

$$V_s(t)=V_mcos(wt+\phi),i(0^-)=0,$$

<img src="https://s2.loli.net/2022/04/13/t1N9VWxizsulkpa.png" alt="image-20220413151558104" style="zoom:33%;" />

$$Find\ i(t),t\geq0$$

$$Solution:$$
$$
L\frac{di(t)}{dt}+Ri(t)=V_mcos(wt+\phi)
\\\Longrightarrow\frac{di(t)}{dt}+\frac{R}{L}i(t)=\frac{V_m}{L}cos(wt+\phi)(一阶线性微分方程)
\\\frac{d(e^{\frac{R}{L}t}\cdot i(t))}{dt}=\frac{V_m}{L}cos(wt+\phi)\cdot e^{\frac{R}{L}t}
\\\Longrightarrow i(t)=e^{-\frac{R}{L}t}[\int\frac{V_m}{L}cos(wt+\phi)\cdot e^{\frac{R}{L}t}dt+C]
\\assume:Y=\int\frac{V_m}{L}cos(wt+\phi)\cdot e^{\frac{R}{L}t}dt+C
\\分部积分\\
\\Y=\frac{V_m}{L}(\frac{L}{R}e^{\frac{R}{L}t}cos(wt+\phi)-\int -wsin(wt+\phi)\frac{L}{R}e^{\frac{R}{L}t}dt)
\\Y=\frac{V_m}{L}(\frac{L}{R}e^{\frac{R}{L}t}cos(wt+\phi)+\frac{L^2}{R^2}e^{\frac{R}{L}t}wsin(wt+\phi)-\int w^2cos(wt+\phi)\frac{L^2}{R^2}e^{\frac{R}{L}t}dt)
\\
Y=\frac{V_m}{L}cos(wt+\phi)e^{\frac{R}{L}t}+\frac{V_mLw}{R^2}e^{\frac{R}{L}t}sin(wt+\phi)-\frac{w^2L^2}{R^2}Y
\\(1+\frac{w^2L^2}{R^2})Y=\frac{V_m}{R}cos(wt+\phi)e^{\frac{R}{L}t}+\frac{V_mLw}{R^2}e^{\frac{R}{L}t}sin(wt+\phi)\\
(1+\frac{w^2L^2}{R^2})Y=\frac{V_m}{R}[cos(wt+\phi)e^{\frac{R}{L}t}+\frac{Lw}{R}e^{\frac{R}{L}t}sin(wt+\phi)]
\\(1+\frac{w^2L^2}{R^2})Y=\frac{V_m}{R}[\sqrt{1+\frac{L^2w^2}{R^2}}cos(wt+\phi-\theta)\\where\ \ \theta=arctan(\frac{wL}R)
$$

$$
Y=\frac{V_m}{\sqrt{R^2+(wl)^2}}cos(wt+\phi-\theta)e^{\frac{R}{L}t},where \theta=arctan(\frac{wL}{R})
\\\Longrightarrow i(t)=Ce^{-\frac{R}{L}t}+\frac{V_m}{\sqrt{R^2+(wL)^2}}cos(\phi-\theta)\Rightarrow C=\frac{V_m}{\sqrt{R^2+(wL)^2}}cos(\phi-\theta)
\\\Rightarrow i(t)=-\frac{V_m}{\sqrt{R^2+(wL)^2}}cos(\phi-\theta)e^{-\frac{R}{L}t}+\frac{V_m}{\sqrt{(R^2)+(wL)^2}}cos(wt+\phi-\theta)
\\Transient Response\ \ \ \ \ \ \ \ \ \ Steady-state\ response
\\暂态响应 \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \  \ \ \ \ \ \ \ \ \ \ \ \ 稳态响应
$$

**For the steady state response**(关于稳态响应)

(1)sinusoidel正弦波

(2)response freq=source freq

(3)Maguitude /phase of response can differ from the source

## 2.sinusoidel signals

$$v(t)=V_mcos(\omega t+\theta)$$

$$V_m:peak value$$

$$\omega:angular freq$$

$$f=\frac{1}{T}=\frac{\omega}{2\pi}$$

$$V_1=V_mcos(wt+\phi)$$

$$V_2=V_mcos(wt+\phi+\delta)$$

$$V_1\ lags V_2$$

$$V_2\ leadsV_1$$

$$lags:occurs\ later\ in\ time$$

$$leads:occurs\ earlier\ in\ time$$

**Root-mean-square value(RMS)有效值**

Def：RMS value of a current is equal to the value of the direct current that would produce the same average power dissipation in a resistive load.

e.g1:For a periodic function i(t),in one period.
$$
I_{RMS}=\sqrt{\frac{1}{T}\int^t_0i^2(t)dt}
\\V_{RMS}=\sqrt{\frac{1}{T}\int^t_0V^2(t)dt}
$$

## 3 complex number 复数

rectangular form:z=x+jy.

$$Re(z)=x,I_m(z)=y$$

polar form:

$$z=re^{j\phi}=r\ang\phi\xrightarrow[formula]{Euler's}rcos\phi+jrsin\phi$$

note:$$1\degree.e^{j\phi}=cos\phi+j\sin\phi$$

$$2\degree.\large\displaystyle\begin{cases}cos\phi=\frac{e^{j\phi}+e^{-j\phi}}{2}\\sin\phi=\frac{e^{j\phi}-e^{-j\phi}}{2}{}\end{cases}$$

$$3\degree|e^{j\phi}|=1$$

$$4\degree z_1=x_1+jy_1,z_2=x_2+jy_2\Longrightarrow z_1\pm z_2=(x_1\pm x_2)+j(y_1\pm y_2)$$

## 4.phasor     “相量$\neq$向量”

We can use phasor(a complex number) to represent

sinusoids     $$正余弦信号$$

$$\widetilde{v}=V_m\ang\phi$$

$$v(t)=V_mcos(wt+\phi)=V_mRe(e^{j(wt+\phi)})=Re(V_me^{j\phi}\cdot e^{jwt})\xrightarrow{\widetilde{v}=V_m\ang\phi}Re(\widetilde{v}e^{jwt})$$

$$\Longrightarrow v(t)=Re(\widetilde{v}e^{jwt})=V_mcos(wt+\phi)$$

正弦，单频，稳态的线性时不变
$$
e.g.1\ v(t)=-4sin(30t+50\degree)V.Find\ phasor.\\
\\\Rightarrow v(t)=4cos(30t+50\degree+90\degree)V
\\\widetilde{v}=4cos(30t+50\degree+90\degree)V=4\ang140\degree V\\
\\\\e.g.2.\widetilde{v}=-25\ang 40\degree V\  Find\ v(t)\\
\\\widetilde{v}=-25cos(wt+40)V
$$

### Question: If we know $\widetilde{v}$is the phaser of v(t),what is the phasor of $$\frac{dv(t)}{dt},\int v(t)dt$$

$$1.\degree v(t)\rightarrow v\Rightarrow\frac{dv(t)}{dt}$$
$$
proof:\\
v(t)=v_mcos(wt+\phi)\leftrightarrow\widetilde{v}=v_m\ang\phi
\\\frac{dv(t)}{dt}=-wV_msin(wt+\phi)\leftrightarrow wV_m\ang\phi+90\degree
\\=wV_me^{j\phi}\cdot e^{j90\degree}=wj\widetilde{v}
$$

$$\displaystyle 2\degree.v(t)\leftrightarrow \widetilde{v}\Rightarrow\int v(t)dt=\frac{\widetilde{v}}{jw}$$
$$
Proof:v(t)=V_mcos(wt+\phi)\longleftrightarrow\widetilde{v}=V_m\ang\phi
\\\int v(t)dt=\frac{1}{w}V_msin(wt+\phi)=\frac{V_m}{w}cos(wt+\phi-90\degree)
\leftrightarrow\frac{V_m}{w}\ang\phi-90\degree\\
=\frac{V_m}{w}e^{j\phi}\cdot e^{-j90\degree}\\
=-j\frac{V_m}{w}\ang\phi=\frac{V_m}{wj}\ang\phi
$$


### phasor domain 数学原理总结

对于一个正弦稳态激励

![image-20220425091035769](https://s2.loli.net/2022/04/25/8NHw3AgmcPGhyln.png) 

![image-20220425091529941](https://s2.loli.net/2022/04/25/me9IKVhstFX1cx5.png)

![image-20220425092052543](https://s2.loli.net/2022/04/25/yUdeBYZGCRJapvM.png)

 
