# Lecture 6 second-order circuits 二阶电路时域分析

[TOC]

## 1.Review : step response of RC circuit

<img src="https://s2.loli.net/2022/03/23/uB28sLeRyC6zaoN.png" alt="image-20220323115919974" style="zoom:33%;" />

$$
\Rightarrow How\ about\ RLC\ circuit?
$$
<img src="https://s2.loli.net/2022/03/23/rJOK93IgkdCNfwt.png" alt="image-20220323165524501" style="zoom:50%;" />

$$
V_c(0-)=V_0\\
\begin {cases}
i_L(t)=C\frac{dV_C(t)}{dt}\\
V_s-RiL(t)-L\frac{di_L(t)}{dt}-V_c(t)=0
\end{cases}
$$

$$
\Longrightarrow RC\frac{dV_c(t)}{dt}+LC\frac{d^2V_c(t)}{dt^2}+V_C(t)=V_S
$$

## 2.Natural response (source-free)

### 2.1 series RLC circuit.    $V_c(0-)=V_0,i_L(0-)=I_0(t\geq0)$

solution: 

step 1:t=0-$V(0-)=V_0,i_L(0^-)=I_0$,

step 2:t=0+$V(0+)=V_C(0-)=V_0,i_L(0^+)=I_L(0^-)=I_0$
$$
\frac{d^2V_c(t)}{dt^2}+\frac{RdV_c(t)}{Ldt}+\frac{1}{LC}V_c(t)=0\\
\frac{d^2V_c(t)}{dt^2}+p\frac{dV_c(t)}{dt}+qV_c(t)=0\\
where\ p=\frac{R}{L},q=\frac{1}{LC}
$$
To solve the above $2^{nd}$-order ordinary differential equation (ODE)

Let $V_C(t)=Ae^{st}$(A is a CONST)
$$
\Longrightarrow As^2e^{st}+p\cdot Ase^{st}+qAe^{st}=0\Longrightarrow Ae^{st}(s^2+ps+q)=0
$$
If we select S.s.t.$s^2+ps+q=0,V_c(t)=Ae^{st}\ satisfied\ the\ ODE.$

**3 cases **on the roots of $s^2+ps+q=0$($\displaystyle s=\frac{-p\pm\sqrt{p^2-4q}}{2}=-\frac{R}{2L}\pm\sqrt{(\frac{R}{2L})^2-\frac{1}{LC}}$)

### case 1 Overdamped “过阻尼”（S1$\neq$S2,real number)

In this case $(\frac{R}{2L})^2-\frac{1}{LC}>0$

Let $\alpha=\frac{R}{2L}$,$\omega_0=\frac{1}{\sqrt{LC}}\Rightarrow S_1=-\alpha+\sqrt{\alpha^2-\omega_0^2}<0$

​                                               $S_2=-\alpha-\sqrt{\alpha^2-\omega_0^2}<0$

$V_c(t)=A_1e^{S_1t}+A_2e^{S_2t}$**where $A_1,A_2$can be found using two initial conditions.**

### case 2:”critically Damped”. 临界阻尼（$S_1=S_2$,real number)

$$
(\frac{R}{2L})^2-\frac{1}{LC}=0\Rightarrow \alpha=\frac{R}{2L}=\omega_0\ \ \  ,S_1=-\alpha+\sqrt{\alpha^2-\omega_0^2}=0
$$

​                                                                                                     $S_2=-\alpha-\sqrt{\alpha^2-\omega_0^2}=0$    

$$
\Longrightarrow S_1=S_2=-\alpha
$$

$V_C(t)=Ae^{st}=A_1e^{-\alpha t}+A_2e^{-\alpha t}???$不完整的根的表达式

$\Longrightarrow$In this case we**cannot** simply use $V_C(t)=A_1e^{S_1t}+A_2e^{S_2t}=Ae^{st}=Ae^{-\alpha t}$

另一个根如何寻找？

$$\displaystyle\frac{d^2V_c(t)}{dt^2}+\frac{RdV_c(t)}{Ldt}+\frac{1}{LC}V_c(t)=0,\alpha=\frac{R}{2L}=\omega_0$$
$$
\Longrightarrow \frac{d^2V_c(t)}{dt^2}+2\alpha\frac{dV_C(t)}{dt}+\alpha^2V_c(t)=0
\\\Rightarrow (\frac{d^2V_c(t)}{dt^2}+\alpha\frac{dV_c(t)}{dt})+(\alpha\frac{V_c(t)}{dt}+\alpha^2V_c(t))=0
$$

$$
\Longrightarrow \frac{d}{dt}(\frac{dV_c(t)}{dt}+\alpha V_c(t))+\alpha(dV_c(t)+\alpha V_c(t))=0
\\\Longrightarrow \frac{d}{dt}u(t)+\alpha u(t)=0 \Rightarrow u(t)=A_1e^{-\alpha t}
\\\Longrightarrow\frac{dV_c(t)}{dt}+\alpha V_c(t)=A_1e^{-\alpha t}
\\\Longrightarrow V_c(t)e^{\alpha t}=A_1t+A_2
\\\Longrightarrow V_c(t)=(A_1t+A_2)e^{-\alpha t}
$$

### Case 3 “Underdamped”欠阻尼（S1,2，complex number）

$$
(\frac{R}{2L})^2-\frac{1}{LC}<0,\Rightarrow -\alpha\pm\sqrt{(\omega_0^2-\alpha^2)\cdot(-1)}=-\alpha\pm j\omega_d,where\ \omega_d=\sqrt{\omega_0^2-\alpha^2}
$$

#### Method 1

$$
(C_1e^{S_1t}+C_2e^{S_2t})=(C_1e^{S_1t}+C_2e^{S_2t})^{*}
\\\Longrightarrow (C_1e^{-\alpha t+jw_dt}+C_2e^{-\alpha t-jw_dt})\\=(C_1^*\cdot e^{-\alpha t}\cdot e^{-jw_dt}+C_2^*e^{-\alpha t} e^{j\omega _dt})
\\\Rightarrow C_1=C_2^*,Let C_1=x+yj,C_2=x-yj.\\
\cos\omega dt=\frac{e^{jt}+e^{-jt}}{2}
\\\sin\omega dt=\frac{e^{jt}-e^{-jt}}{2}
\\V_C(t)=C_1e^{S_1t}+C_2e^{S_2t}
\\=(x+yj)e^{-\alpha t+jw_dt}+(x-yj)e^{^{-\alpha t-j\omega dt}}
\\=xe^{-\alpha t}(e^{j\omega_dt}+e^{-jw_dt})+yje^{-\alpha t }(e^{jw_dt}-e^{-jw_dt})
\\=e^{-\alpha t}(2x\cdot\cos w_dt-2\cdot y\sin w_dt)
\\=e^{-\alpha t}(A_1\cos w_dt+A_2\sin w_dt)
$$

#### Method 2

$$
V_c=C_1e^{(-\alpha+j\omega d)t}+C_2e^{(-\alpha-j\omega d)t}
$$

[引理,y=a+bi是y’’+py’+qy=0的解，则a与b均是其解]

（p,q is real number)
$$
Proof:(a+bi)’’+p(a+bi)’+q(a+bi)=0\\
\Longrightarrow(a''+pa'+qa)+(b''+pb'+qb)i=0
\\\Longrightarrow \begin{cases}
a''+pa'+qa=0
\\b''+pb'+qb=0
\end{cases}\Longrightarrow\ a,b均是其解
$$
So $e^{(-\alpha \pm jw_d)t}$是原方程的解（由$S_{1,2}=-\alpha\pm j\omega_d得到$）

$\Rightarrow$实部虚部都是解：$e^{-\alpha t}\cdot e^{\pm j\omega_d t}$

real:$e^{-\alpha t}\cos w_dt$

imag:$e^{-\alpha t}\sin w_dt$
$$
V_c(t)=A_1e^{-\alpha t}\cos w_dt+A_2e^{-\alpha t}\sin w_dt
$$

### Summary:series RLC network(natural response)

Gradual loss of intial stored energy $\alpha=\frac{R}{2L},\omega_0=\frac{1}{\sqrt{LC}}$
$$
\begin{cases}
case1:overdamped,\alpha>\omega_0\Rightarrow R>2\sqrt{\frac{L}{C}},\\V_c(t)=A_1e^{S_1t}+A_2e^{S_2t}\\ S_{1,2}=-\alpha\pm\sqrt{\alpha^2-\omega_0^2}\\
\\case2:critically\ damped,,\alpha=\omega_0\Rightarrow R=2\sqrt{\frac{L}{C}}\\V_c(t)=(A_1t+A_2)e^{-\alpha t}\\S_{1,2}=-\alpha\\ 
\\case3:underdamped\ \alpha<\omega_0\Rightarrow R<2\sqrt{\frac{L}{C}},\\V_c(t)=e^{-\alpha t}(A_1\cos w_dt+A_2\sin w_dt)\\w_d=\sqrt{\omega_0^2-\alpha^2}
\end{cases}
$$

$$
V_c(t)=A_1e^{-\alpha t}\cos w_dt+A_2e^{-\alpha t}\sin w_dt
$$



![image-20220328083646461](https://s2.loli.net/2022/03/28/zjBtku13Dx48dOg.png)

![image-20220328084501142](https://s2.loli.net/2022/03/28/uczxI8rw1le4F6M.png)

![image-20220328085208682](https://s2.loli.net/2022/03/28/Ox2nW38TDrX5Ljg.png)

### 2.2 parallel RLC circuit

### ![image-20220328110221332](https://s2.loli.net/2022/03/28/RNhQJoHD1kGV5es.png)

$$
\frac{d^2i_c(t)}{dt^2}+\frac{di_c(t)}{RCdt}+\frac{1}{LC}i_c(t)=0\\
\frac{d^2i_c(t)}{dt^2}+p\frac{di_c(t)}{dt}+qi_c(t)=0\\
where\ p=\frac{R}{L},q=\frac{1}{LC}
$$

$$
\alpha=\frac{1}{2RC},\omega_0=\frac{1}{\sqrt{LC}}
$$


$$
\begin{cases}
case1:overdamped,\alpha>\omega_0\\i_L(t)=A_1e^{S_1t}+A_2e^{S_2t}\\ S_{1,2}=-\alpha\pm\sqrt{\alpha^2-\omega_0^2}\\
\\case2:critically\ damped,,\alpha=\omega_0\\i_L(t)=(A_1t+A_2)e^{-\alpha t}\\S_{1,2}=-\alpha\\ 
\\case3:underdamped\ \alpha<\omega_0
\\i_L(t)=e^{-\alpha t}(A_1\cos w_dt+A_2\sin w_dt)\\w_d=\sqrt{\omega_0^2-\alpha^2}
\end{cases}
$$

## 3.Step Response阶跃响应

### 3.1 Series RLC Circuit

![image-20220328091514490](https://s2.loli.net/2022/03/28/OxEDArfBMhJGWT3.png)
$$
\Longrightarrow \frac{d^2V_c(t)}{dt^2}+\frac{R}{L}\frac{dV_c(t)}{dt}+\frac{V_C(t)}{LC}=\frac{V_S}{LC}
$$
statement:

The solution $V_C(t)=V_t(t)+V_{SS}(t),where V_{SS}(t)=V_S=CONST$
$$
V_t(t)has\ the\ same\ formot\ as\ in\ natural\ response
$$

$$
\Longrightarrow \frac{d^2(V_C(t)-V_{S})}{dt^2}+\frac{R}{L}\frac{d(V_C(t)-V_{S})}{dt}+\frac{V_C(t)-V_S}{LC}=0
$$

$$
\begin{cases}
case1:overdamped,\alpha>\omega_0\Rightarrow R>2\sqrt{\frac{L}{C}},\\V_c(t)=A_1e^{S_1t}+A_2e^{S_2t}+V_S\\ S_{1,2}=-\alpha\pm\sqrt{\alpha^2-\omega_0^2}\\
\\case2:critically\ damped,,\alpha=\omega_0\Rightarrow R=2\sqrt{\frac{L}{C}}\\V_c(t)=(A_1t+A_2)e^{-\alpha t}+V_S\\S_{1,2}=-\alpha\\ 
\\case3:underdamped\ \alpha<\omega_0\Rightarrow R<2\sqrt{\frac{L}{C}},\\V_c(t)=e^{-\alpha t}(A_1\cos w_dt+A_2\sin w_dt)+V_S\\w_d=\sqrt{\omega_0^2-\alpha^2}
\end{cases}
$$



![image-20220328093610986](https://s2.loli.net/2022/03/28/d4GtSMDjElbarFO.png)

![image-20220328094940716](https://s2.loli.net/2022/03/28/LgwpS2KF3bD65Uc.png)

## 4. Any excitation 任意激励响应

$$
\frac{d^2y(t)}{dt^2}+2\alpha\frac{dy(t)}{dt}+w_o^2y(t)=f(t)
$$

$$
y=y_p+y_h
\\y_p被称为特解，y_h被称为通解
$$

$$
\large{
Step1: 找到homogeneous\ equation 求出S1，S2}\\
\large{
Step2:由f(t)以及S_{1,2}确认y_p形式}
\\
\large{
Step3:有了y_p 的形式将y_p带入原方程，求出y_p中的所有未知系数}
\\
\large{
Step4:y(t)=y_h+y_p,y(t)中含有两个待定系数A_1,A_2\\}
                use\ initial\ condition\ to\ find A_1,A_2,(I,C)
$$


## 如何求特解？

### 4.1 $$f(t)=e^{rt}P_m(t)$$  

**where r is a real number,$P_m(t)$is plodynomial of degree m**
$$
y_p''+2\alpha y_p'+\omega_0^2y_p=e^{rt}P_m(t)\\
Let\ \ y_p=Q(t)e^{rt}\\
e^{rt}[Q''(t)+2rQ'(t)+r^2Q]+e^{rt}(2\alpha Q'(t)+2\alpha rQ(t))+e^{rt}Q(t)w_0^2=e^{rt}P_m(t)
\\\Rightarrow e^{rt}[Q''(t)+Q'(t)2(r+\alpha)+Q(t)(r^2+2\alpha r+\omega_0^2)]=e^{rt}P_m(t)
\\\Rightarrow Q''(t)+Q'(t)2(r+\alpha)+Q(t)(r^2+2\alpha r+\omega_0^2)=P_m(t)& (1)
$$

#### 4.1.1

$$
r\neq S_{1,2}\Longrightarrow r^2+2\alpha r+\omega_0^2\neq0
$$

$$
So\ we\ can\ select\ Q(t)=Q_m(t)\ s.t.(1)\ is\ satisfied
$$

#### 4.1.2

$$
r= S_{1or2}\Longrightarrow\ r^2+2\alpha r+\omega_0^2=0
$$

为了使得左边是m次多项式，$$Q(t)=Q_{m+1}(t)$$即$Q(t)=tQ_{m}(t)$

#### 4.1.3

$$
r= S_{1}=S_{2}\Longrightarrow \begin{cases} r^2+2\alpha r+\omega_0^2=0
\\r+\alpha=0
\end{cases}
$$

为了使得左边是m次多项式，$$Q(t)=Q_{m+2}(t)$$即$Q(t)=t^2Q_{m}(t)$

#### In general

$$
\begin{cases}
非根:r\neq S_{1,2},y_p=Q_me^{rt}\\
单根:r= S_{1or2},y_p=tQ_me^{rt}\\
重根:r=S_1=S_2,y_p=t^2Q_me^{rt}\\
\end{cases}
$$





### 4.2 $f(t)=e^{rt}(M\cos \omega t+N\sin \omega t)$

**Firstly we only think about $$e^{rt}\cos \omega t$$**

we want to find $y_p$s.t
$$
y_p''+2\alpha y_p'+\omega_0^2y_p=e^{rt}\cos \omega t\\
since\ \ \ \ e^{jwt}=coswt+jsinwt(欧拉公式)\Longrightarrow coswt=e^{jwt}-jsinwt
\\y_p''+2\alpha y_p'+\omega_0^2y_p=e^{rt}(e^{jwt}-jsinwt)
\\y_p''+2\alpha y_p'+\omega_0^2y_p+jsinwt=e^{rt}e^{jwt}

\\
y''+2\alpha y'+\omega_0^2y=e^{rt}e^{jwt}=e^{(r+jw)t}
\\So\ y_p''+2\alpha y_p'+\omega_0^2y_p=e^{rt}\cos \omega t ,where\ y_p=real(y)
$$

$$
\\Q:为什么要用欧拉公式\\
A:可以用第一种情况的结论了\\
let \beta=r+jw\\
y''+2\alpha y'+\omega_0^2y=e^{(r+jw)t}=e^{\beta t}
\\ So\ back\ to\ 4.1 f(t)=e^{rt}P_m(t),where\ m=0\ r=\beta\\
\\
(1)\ \ \ \ \ \ \ \ \ \ \ \ r\pm jw\neq S_{1,2}\Longrightarrow y=Be^{\beta t}\\
\begin{cases} y''+2\alpha y'+w_0^2y=Be^{\beta t}(\beta^2+2\alpha\beta+w_0^2)=e^{\beta t}\\
\beta^2+2\alpha\beta+w_0^2\neq0
\end{cases}

\\B=\frac{1}{\beta^2+2\alpha\beta+w_0^2}=u+jv\\
\Longrightarrow y=(u+jv)e^{(r+jw)t}
\\\\
(2)\ \ \ \ \ \ \ \ \ \ \ \ r\pm jw= S_{1,2}\Longrightarrow y=tBe^{\beta t}\\ 
\begin{cases} y''+2\alpha y'+w_0^2y=tBe^{\beta t}(\beta^2+2\alpha\beta+w_0^2)+2(\alpha+\beta)Be^{\beta t}=e^{\beta t}
\\\beta^2+2\alpha\beta+w_0^2=0
\end{cases}

\\B=\frac{1}{2(\alpha+\beta)}=u+jv\\
\Longrightarrow y=(u+jv)e^{(r+jw)t}

\begin {cases}

r\pm jw\neq S_{1,2},y_p=real(y)=real((u+jv)e^{(r+jw)t})=e^{rt}(B_1coswt+B_2sinwt)
\\r\pm jw=S_{1,2},y_p=real(y)=real(t(u+jv)e^{(r+jw)t})=te^{rt}(B_1coswt+B_2sinwt)
\end{cases}
$$

then $$y_p''+2\alpha y_p'+\omega_0^2y_p=e^{rt}(M\cos \omega t+N\sin \omega t)$$
$$
\Rightarrow\begin {cases}
r\pm jw\neq S_{1,2},y_p=e^{rt}(B_1coswt+B_2sinwt)
\\r\pm jw=S_{1,2},,y_p=te^{rt}(B_1coswt+B_2sinwt)
\end{cases}
$$

### 4.3 $f(t)=f_1(t)+f_2(t)$

$$
\begin{cases}
y_{p1}''+2\alpha y_{p1}'+\omega_0^2y_{p1}=f_1(t)&(1)\\
y_{p2}''+2\alpha y_{p2}'+\omega_0^2y_{p2}=f_2(t)&(2)
\end{cases}
$$

$$
(1)+(2)\Longrightarrow
\\(y_{p1}+y_{p2})''+2\alpha (y_{p1}+y_{p2})'+\omega_0^2(y_{p1}+y_{p2})=f_1(t)+f_2(t)
$$

$$
y_p=y_{p1}+y_{p2}
$$

