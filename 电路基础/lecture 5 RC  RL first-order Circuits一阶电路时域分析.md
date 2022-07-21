# lecture 5 RC / RL first-order Circuits一阶电路时域分析

Motivation

Preciously： only static（静态的） analysis on inputs of a circuit

$$\large{Two~assumption}$$
$$
\begin{cases}
Responses~at~time~only\ depend\ on\ inputs\ at\ time t \\
Circuit\ respond\ to\ input\ change\ infintely\ fast
\end{cases}
$$
 $$\rightarrow$$so what if without the two assumptions

## dynamic Analysis

### 1. Energy storage Elements  储能元件

(1)Capacitors
$$
\begin{cases}
passive\ element\\
store\ energy\ in\ electric\ field
\end {cases}
$$

$$
C=\frac{\varepsilon S}{4\pi kd},q=CV
$$

Question:

How do current”flow through”the capacitor?(存在电解质，绝缘)

Through charging and discharge to the two plates



#### V-I characteristic 

$$
\begin{aligned}
i(t)&=\frac{dq(t)}{dt}\\
&=\C\frac{dV(t)}{dt}
\end {aligned}
$$

Or:
$$
v(t)=\frac{1}{C}\int_{t_o}^ti(t)dt+V(t_o)
$$

#### stored Energy 

p(t)= v(t) i(t)=v(t)$C\frac{dV(t)}{dt}$
$$
E=\int_{t_t0}^tP(t)dt=\int_{t_o}^t CV(t)\frac{dV(t)dt}{dt}\\
=\frac{1}{2}CV^2(t)|^t_{t_0}
$$

#### Important Property

Property 1

V(t) cannot change instanteously(电容电压不突变)

If V jump from 0 $\rightarrow V_m$
$$
\frac{dv(t)}{dt}|_{t=t_m}=\infty
$$
This is not possible

#### capacitor in series&parallel

$$
\begin{aligned}
i_S(t)&=C_1\frac{dV_1(t)}{dt}\\
i_S(t)&=C_2\frac{dV_2(t)}{dt}\\
i_S(t)&=C_3\frac{dV_3(t)}{dt}
\end{aligned}
$$

$Vs(t)=V_1(t)+V_2(t)+V_3(t)$$\rightarrow$ 
$$
\begin{aligned}
i_S(t)&=C_{eq}\frac{dV_S(t)}{dt}\\
&=C_{eq}\frac{d(v_1(t)+v_2(t)+v_3(t))}{dt}\\
&=C_{eq}\frac{i_s(t)}{C_1}
+\frac{i_s(t)}{C_1}
+\frac{i_s(t)}{C_1}\\
&=C_{eq} (\frac{1}{C_1}+\frac{1}{C_2}+\frac{1}{C_3})i_S(t)
\end{aligned}
$$

#### Voltage division(in series circuits)

$$
is(t)=C_1\frac{dV_1(t)}{dt}
is(t)+C_2\frac{dV_2(t)}{dt}is(t)+C_3\frac{dV_3(t)}{dt}
$$

$$
\frac{dV_1(t)}{dV2(t)}=\frac{C_2}{C1}
$$

#### current division(in series circuits)

$$
\frac{di_1(t)}{di2(t)}=\frac{C_1}{C2}
$$

### (2)inductor

$$
\begin{cases}
passive\ element\\
stone\ energy\ in\ magnetic\ field
\end{cases}
$$

$$
L=\frac{N^2u}{l}
$$

$$
N·B·S=L·i
$$

$$
v(t)=\frac{d(L·i(t))}{dt}
$$

$$
=L\frac{d_i(t)}{dt}i(t)
$$

$$
i(t)=\frac{1}{L}\int^t_{t_o}V(t)dt+i(t_0)
$$

#### stored Energy

$p(t)=v(t)i(t)$

$$E=\int^t_{t0}p(t)dt$$

$=\frac{1}{2}Li^2(t)-\frac{1}{2}Li^2(t_0)$
$$
v(t)=L\frac{di(t)}{dt}
$$

#### series

$$
L=L_1+L_2+L_3
$$

#### parallel 

$$
\frac{1}{L}=\frac{1}{L_1}+\frac{1}{L_2}+\frac{1}{L_3}
$$

![image-20220314083412746](https://s2.loli.net/2022/03/18/ZcNCxUPADRFE6dV.png)

 

##  Voltage division

$\displaystyle \frac{V_1(t)}{V_2(t)}=\frac{L1\frac{di_s(t)}{dt}}{L_2\frac{di_s(t)}{dt}}$

$\displaystyle \frac{V_1(t)}{ V_2(t)}$=$\displaystyle \frac{L_1}{L_2}$

![image-20220314084335291](https://s2.loli.net/2022/03/18/iBuwvtJf1yLINO8.png)

![image-20220314084703799](https://s2.loli.net/2022/03/18/z6LrKCIpTfGs7J2.png)

![image-20220314084849600](https://s2.loli.net/2022/03/18/OH12lFKo94YMjV7.png)

# Lecture 6 response of a circuit 电路响应

reaction to an abrupt change of a certainw

![image-20220314090226054](https://s2.loli.net/2022/03/18/Nkexqjf9OHFvTYB.png)

## Natural response of RC/RL circuit 自然响应

dedinition:

behavior(i.e current voltage)when stored energy in the inducor or capacitor is releasedto the resistive part of the network

(containing no independent source)**无外加激励源**

![image-20220314085916893](https://s2.loli.net/2022/03/18/OkuyZ9WnFqC13Uo.png)

(1.a)

![image-20220314090029534](https://s2.loli.net/2022/03/18/Pdnyk6lKOpc3TBz.png)

![image-20220314091212800](https://s2.loli.net/2022/03/18/cR4ldLWw2QUGVnZ.png)

#### step 1: At t=0$^-$

$V_c(0-)=V_s,i_c(0-)=0$

(Def of 0-):  $\displaystyle f(0-)=\lim_{t\rightarrow0,t<0}f(t)$

![image-20220314091517036](https://s2.loli.net/2022/03/18/3tJr1pez4xsjgPn.png)

#### step2 :After the switch is moved.(t$\geq0$),switch duration $0^-$~0$^+$(extremely short)

#### V(0+)=?,ic(0+)=?

since $\displaystyle i_c(t)=C\frac{dV_c(t)}{t},If\ v_c(0+)\neq Vc(0-),i_c(t)=C\frac{dV_c(t)}{dt}\approx C \cdot\frac{V_c(0+)-V_c(0-)}{0^+-0^-}=\infty,which\ is\ not\ possible$

Since capaertor voltage cannot change instantously
$$
V_c(0^+)=V_c(0^-)=V_s
$$


![image-20220314140456126](https://s2.loli.net/2022/03/18/1X2TVs9Iv8JbCuf.png)
$$
i_c(0^+)=-\frac{V_c(0^+)}{R}=-\frac{v_s}{R}
$$
![image-20220314140947368](https://s2.loli.net/2022/03/18/3mI7AMsOc6Ulzxg.png)
$$
\begin{cases}
\displaystyle i_c(t)=C\frac{dV_c(t)}{dt}\\
R\cdot i_c(t)+V_c(t)=0
\end{cases}
\Longrightarrow C\cdot R\frac{dV_c(t)}{dt}+V_c(t)=0 \Longrightarrow C\cdot R\frac{dV_c(t)}{V_c(t)}=-dt
$$

$$
\begin{cases}
\displaystyle
\int^t_0C\cdot R\frac{dV_c(t)}{V_c(t)}=\int^t_0-dt
\\V_c(o^+)=V_s
\end{cases}
\Longrightarrow C\cdot R\cdot [lnV_c(t)-lnV_c(0)]=-t\Longrightarrow C\cdot R(ln\frac{V_c(t)}{V_s})=-t
$$

$$
V_c(t)=V_s\cdot e^{\frac{-1}{C\cdot R}t}\Longrightarrow V_c(t)=V_c(0^+)e^{-\frac{t}{\tau}}
$$

![image-20220314155941325](https://s2.loli.net/2022/03/18/XxvCAGPV7ojz2Dq.png)
$$
V_c(t)=V_se\frac{-t}{\tau},\tau=RC
\\e^{-1}\approx 0.37
$$


![image-20220314155804454](https://s2.loli.net/2022/03/18/NDwYa8MbE3svIhq.png)
$$
i_c(t)=-\frac{V_s}{R}e^{\frac{-t}{\tau}}
$$
Note :1$\degree$R$\nearrow$,C$\nearrow\Rightarrow\tau \nearrow$衰减速度$\searrow$
$$
\begin{cases}
R\nearrow:电荷(i_c(t))\downarrow\tau\uparrow
\\\ \ \ \ \ \ \ \ P_R(t)=\frac{V_c^2(t)}{R}
\\C\nearrow:C越大，防止电压突变的能力越强，\tau\uparrow
\end{cases}
$$
2$\degree$电容电压不突变，但是电容电流是可以突变的
$$
i_C(0^-)=0,i_c(0^+)=-\frac{v_s}{R}
$$


![image-20220314095452095](https://s2.loli.net/2022/03/18/vfCeSJ7GRLWahjZ.png)



# lecture 7

### RL circuit

![image-20220316082521794](https://s2.loli.net/2022/03/18/X5v3TQ2r7LIFKwJ.png)

### solution: 

#### step1:before the switch is closed(t<0)

![img](https://s2.loli.net/2022/03/18/crEuAZlYWQKmPfH.png)
$$
V_L(0-)
$$
![image-20220316082925434](https://s2.loli.net/2022/03/18/PchpF8zUL4KRYt3.png)

![image-20220316083138611](https://s2.loli.net/2022/03/18/Irn81hMEWtkNZ9A.png)

## step response of RC/RL circuits (阶跃响应)

Def: Behavior (i.e current voltage) when a DC source os suddenly applied to a circult(注：元件可以有初始储能的)

“step function”阶跃函数 maintain a constant value before a certain time and then change to another constant afterwards.
$$
u(t)=\begin{cases}
0,t<0\\
1,t>0
\end{cases}
$$


eg.express the voltage waveform using u(t)

![image-20220316084339149](https://s2.loli.net/2022/03/18/9S8A1Qp3IC5TKcl.png)
$$
v(t)=10u(t-2)-10u(t-5)\\u是奇异函数
$$

## $V_c(0^-)=v_0$

### (2.a)RC circuit 

![image-20220316084800291](https://s2.loli.net/2022/03/18/pQniC3McOHPjS62.png)

step1: t<0 $V_c(0^-)=v_0$

step2 :t$\geq$0 since capacitor voltage cannot change instantously
$$
V_c(0^+)=V_c(0^-)=V_0\\
\begin{cases}
i_c(t)+c\frac{dV_(t)}{dt}
\\V_s-Ri_c(t)-V_C(t)=0
\end{cases}
$$

$$
\Longrightarrow \frac{dV_c(t)}{dt}+\frac{1}{RC}V_c(t)=\frac{1}{RC}V_s
\\Initial\ cond :V_c(0^+)=V_0

\\\Rightarrow \frac{dV_c(t)}{dt}=\frac{1}{RC}V_s-\frac{1}{RC}V_c(t)
\\\frac{dV_c(t)}{dt}=-\frac{1}{RC}[V_c(t)-V_s]
\\\frac{d[V_c(t)-{\color{red}{V_s}}]}{dt}=-\frac{1}{RC}[V_c(t)-V_s]
\\\frac{d[V_c(t)-V_s]}{V_c(t)-V_s}=-\frac{1}{RC}dt
\\\Longrightarrow\int^{t}_0\frac{d[V_c(t)-V_s]}{V_c(t)-V_s}=\int^{t}_0-\frac{1}{RC}dt
\\\Longrightarrow ln(V_c(t)-V_s)|^t_0=-\frac{1}{RC}(t-0)
\\\Longrightarrow ln\frac{V_c(t)-V_s}{V_c(0^+)-V_s}=-\frac{1}{RC}t
\\\Longrightarrow V_c(t)=V_s+(V_c(0^+)-V_s)e^{(-\frac{t}{RC})}
=V_s+(V_0-V_s)e^{\frac{t}{\tau}}
$$

### Note 1$\degree$:(natural response自然响应 and forced response强制响应)

1$\degree V_c(t)=V_0e^{-\frac{t}{\tau}}+V_s(1-e^{-\frac{t}{\tau}})$

![image-20220316090410919](https://s2.loli.net/2022/03/18/OZphUxu6LMoFED8.png)





### Note2$\degree$:(steady state response稳态响应 and transient response暂态响应)

$$
V_c(t)=V_s+(V_0-V_s)e^{-t/\tau}
\\ V_c(t)=V(\infty)+[v(0^+)-V(\infty)]e^{\frac{t}{\tau}}
$$

​                                                                                                        $\uparrow$                  $\uparrow$

​                                                                                                    稳态响应       暂态响应

![image-20220316094802980](https://s2.loli.net/2022/03/18/5RvBhNXKd2DxOyz.png)



![image-20220316092406596](https://s2.loli.net/2022/03/18/z9fcK5mWabkMpgo.png)

the switch has been in position A for a long time.At t=0 ,the switch moves from A to B find $V_c(t)$

Solution: step1 : before the switch is moved(t<0)

<img src="https://s2.loli.net/2022/03/18/MNkUlXPncHfCt5A.png" alt="image-20220316092559101" style="zoom:50%;" />

$$V_c(0^-)=\frac{24V}{3k\Omega}\times 5k\Omega=15V$$



step 2:after the switch is moved(t$\geq$0)

<img src="https://s2.loli.net/2022/03/18/Yabd8jiJ9h5Dn42.png" alt="image-20220316093100574" style="zoom:33%;" />
$$
V_c(0^+)=V_c(0^-)=15V
\\Also,V_c(\infty)=30V,\tau=RC=4k\Omega\cdot 0.5mF=2s
\\V_c(t)=V_c(\infty)+[V_C(0^+)-V(\infty)]e^{-t/\tau}\\
=30-15e^{-0.5t}V
$$
![image-20220316094052569](https://s2.loli.net/2022/03/18/NWQBwedJRGtbUFf.png)



单位：L,C,R $\tau$
$$
V(t)=L\frac{di(t)}{dt}\Rightarrow V=H\cdot\frac{A}{S}\Rightarrow S=H\frac{A}{V}=H\cdot \frac{1}{\Omega}\\
i(t)=C\frac{dV(t)}{dt}\Rightarrow A=F\frac{V}{S}\Rightarrow F\cdot\frac{V}{A}=F\cdot\Omega\Rightarrow \tau=R\cdot C
$$
![image-20220316095051447](https://s2.loli.net/2022/03/18/S17zHaqmWQucLgv.png)

#  三要素法

How to solve first-order circuits?

1$\degree$for any first-order ciucuit with DC excrtion “三要素法”

$$\rightarrow V(t)=V(\infty)+[V(0^+)-v(\infty)]e^{-\frac{t}{\tau}}$$(以V为例，i类似)

Proof：the differential equation that V(t) should obey is:
$$
\begin{cases}
\frac{dV(t)}{dt}+p\cdot V(t)=q,(p,g=const,p\neq0)
\\v(t=0^+)=V(0^+)
\end{cases}
$$

$$
\color{blue}{p\ const:系统参数常数}\\
\color{blue}{q\ const:系统DC\ excitation}
$$



1$\degree$.why V($\infty$)=$\displaystyle\frac{q}{p}$? This is because $\frac{dV(\infty)}{dt}+pV(\infty)=q$?

2$\degree$For any first-order circuit with any excitation find V(t).

The differential eqution that V(t) should obey is
$$
\begin{cases}\frac{dV(t)}{dt}+p\cdot V(t)=q(t),(p=const,p\neq0)\\v(t_0^+)=V(0^+)\end{cases}
$$

Introduce $e^{pt}$:
$$
e^{pt}\frac{dV(t)}{dt}+pe^{pt}V(t)=q(t)e^{pt}
\Longrightarrow \frac{d[v(t)e^{pt}]}{dt}=q(t)e^{pt}\Longrightarrow V(t)=e^{-pt}[\int q(t)e^{pt}dt+C]，V(t=0+)=V(0^+)to\ find\ C
$$
​                                                                             解方程法                                                                 三要素法                                  

RC/RL First Order Ciucuits$$\begin{cases}Natural\ Response\begin{cases}\frac{dV(t)}{dt}+p\cdot V(t)=0;\\v(t_0^+)=V(0^+)\end{cases}\ \ \ \Rightarrow V(t)=V(0^+)e^{-pt} \\step\ response\begin{cases}
\frac{dV(t)}{dt}+p\cdot V(t)=q,
\\v(t_0^+)=V(0^+)
\end{cases}\Rightarrow V(\infty)+[V(0^+)-V(\infty)]e^{-pt} \\Any\ Response\begin{cases}\frac{dV(t)}{dt}+p\cdot V(t)=q(t),\\v(t_0^+)=V(0^+)\end{cases}\Longrightarrow V(t)=e^{-pt}[\int q(t)e^{pt}dt+C] \end{cases}$$

​                                                                    $$(p,g=const,p\neq0)$$

![image-20220321091540169](https://s2.loli.net/2022/03/22/lw7z682nsODSLv5.png)





![image-20220321092455217](https://s2.loli.net/2022/03/22/VFPZfOv8LmHS7aQ.png)

![image-20220321092938676](https://s2.loli.net/2022/03/22/FjAsUgX92MVuNvq.png)



![image-20220321094225271](https://s2.loli.net/2022/03/22/dMA4Qg8CeuEftzP.png)

![image-20220321095316179](https://s2.loli.net/2022/03/22/AsGM785Lp3eqUVv.png)

![image-20220321095602305](https://s2.loli.net/2022/03/22/MO9Kw8HYbTVgWin.png)
