# 电路基础cheatsheet(1.6)-by Heaticy

## 星三角变换

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220616145759433.png" alt="image-20220616145759433" style="zoom: 28%;" />



## 一阶电路响应

​                                                                             解方程法                                                                 三要素法                                  

RC/RL First Order Ciucuits$$\begin{cases}Natural\ Response\begin{cases}\frac{dV(t)}{dt}+p\cdot V(t)=0;\\v(t_0^+)=V(0^+)\end{cases}\ \ \ \Rightarrow V(t)=V(0^+)e^{-pt} \\step\ response\begin{cases}
\frac{dV(t)}{dt}+p\cdot V(t)=q,
\\v(t_0^+)=V(0^+)
\end{cases}\Rightarrow V(\infty)+[V(0^+)-V(\infty)]e^{-pt} \\Any\ Response\begin{cases}\frac{dV(t)}{dt}+p\cdot V(t)=q(t),\\v(t_0^+)=V(0^+)\end{cases}\Longrightarrow V(t)=e^{-pt}[\int q(t)e^{pt}dt+C] \end{cases}$$

## 一阶非线性微分方程$F(x,y,y')=0$

$\displaystyle\frac{dy}{dx}=f(x)g(y)\Longrightarrow y'+p(x)y=q(x)$

$$\displaystyle\\y=e^{-\int p(x)dx}(\int q(x)e^{\int p(x)dx}dx+C)$$

## 量纲

亨利H：L: **$1H=1V·A^{-1}·s=\Omega\cdot s$**.

法拉F：C:  $\displaystyle 1F=1 A·V^{-1}\cdot s=\frac s\Omega$

$$LC=s^2,\sqrt{LC}=s$$

$\displaystyle \tau=RC=\frac{L}{R}=s,\ \ \ \ \ Q=\frac1R\sqrt\frac LC=常数$

## 二阶微分方程的解法$F(t,y,y',y'')=0$

### 通解

$$
ay''+by'+cy=0\Rightarrow y''+py'+qy=0

\\\Delta=p^2-4q
\\
\begin{cases}

case1:overdamped,\Delta>0\\y=A_1e^{S_1t}+A_2e^{S_2t}\\

S_{1,2}=\frac{-p+\sqrt{\Delta}}{2}\\

\\case2:critically\ damped,\Delta=0\\y=(A_1t+A_2)e^{-\frac p{2} t}\\

\\case3:underdamped\ \Delta<0

\\y=e^{-\frac p{2} t}(A_1\cos w_dt+A_2\sin w_dt)\\w_d=\frac{\sqrt{-\Delta}}{2}

\end{cases}\Rightarrow

\begin{cases}
case1:\\
y=A_1e^{S_1t}+A_2e^{S_2t}&\Rightarrow y|_{t=0}=A_1+A_2\\
y'=S_1A_1e^{S_1t}+S_2A_2e^{S_2t}&\Rightarrow y'|_{t=0}=S_1A_1+S_2A_2\\
\\
case2:\\
y=(A_1t+A_2)e^{-\frac p{2} t}&\Rightarrow y|_{t=0}=A_2\\
y'=(A_1(\frac {-p}2)t+A_1+A_2(\frac {-p}2))e^{-\frac p{2} t}&\Rightarrow y|_{t=0}=A_1+A_2(\frac {-p}2)\\
\\
case3:\\
y=(A_1-jA_2)e^{(\frac {-p}2+jw_d)t}&\Rightarrow y|_{t=0}=A_1\\
y'=((-\frac p2A_1+A_2w_d)+(\frac p2A_2+w_dA_1)j)e^{(-\frac p2+jw_d)t}&\Rightarrow y'|_{t=0}=(-\frac p2A_1+A_2w_d)

\end{cases}
$$

## 特解

$$
y''+py'+qy=f(t)\\
$$

### 1.$f(t)=C(常数)$

$$
y_p=\frac C q
$$

### 2. $$f(t)=e^{rt}P_m(t)$$(r是实数,P(m)是多项式)

$$
y_p''+p y_p'+qy_p=e^{rt}P_m(t)\\
Let\ \ y_p=Q(t)e^{rt}\\
\Rightarrow Q''(t)+Q'(t)(2r+p)+Q(t)(r^2+p r+q)=P_m(t)
$$

$$
\begin{cases}
非根:r\neq S_{1,2},y_p=Q_me^{rt}\\
单根:r= S_{1or2},y_p=tQ_me^{rt}\\
重根:r=S_1=S_2,y_p=t^2Q_me^{rt}\\
\end{cases}
$$

### 3 $f(t)=e^{rt}(M\cos \omega t+N\sin \omega t)$

then $y_p''+p y_p'+qy_p=e^{rt}(M\cos \omega t+N\sin \omega t)=(M-Nj)e^{rt+jwt}$
$$
\Rightarrow\begin {cases}
r\pm jw\neq S_{1,2},y_p=e^{rt}(B_1coswt+B_2sinwt)=(B_1-B_2j)e^{rt+jwt}
\\r\pm jw=S_{1,2},,y_p=te^{rt}(B_1coswt+B_2sinwt)=(B_1-B_2j)te^{rt+jwt}
\end{cases}
$$

$$
(1)\ \ \ \ \ \ \ \ \ y_p=Re((B_1-B_2j)e^{rt+jwt})代入\\
(B_1-B_2j)[(r+jw)^2+p(r+jw)+q]=M-Nj\\
(B_1-B_2j)(r^2+pr+q-w^2+(pw+2rw)j)=M-Nj\\
B_1-B_2j=\frac{M-Nj}{(r^2+pr+q-w^2)+(pw+2rw)j}\\
$$

$$
(2)\ \ \ \ \ \ \ \ \ \ \ \ \ \ y_p=(B_1-B_2j)te^{rt+jwt}\\
(B_1-B_2j)[(r+jw)^2+p(r+jw)+q]t+[(r+jw)^2+(r+jw)+p]=M-Nj\\
B_1-B_2j=\frac{M-Nj}{(r^2+r+p-w^2)+(2rw+w)j}
$$

$注意MN和B_1B_2符号\\以上的w全是f(t)中的w,和通解中w=\frac{\sqrt{-\Delta}}2无关!!$

### 4 $f(t)=f_1(t)+f_2(t)$

$$
y_p=y_{p1}+y_{p2}
$$

![image-20220616150042811](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220616150042811.png)

按照标准形式，电流流入同名端，互感的受控源被电流流入正极

和标准形式一个不一样就加一个负号

## 受控源

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220618122646211.png" alt="image-20220618122646211" style="zoom: 33%;" />

## 各种功率

![image-20220616150104464](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220616150104464.png)

### real power 有功功率

$$\displaystyle p(t)=\frac{V_mI_m}2[cos(2wt+\theta_i-\theta_v)+cos(\theta_v-\theta_i)]$$

$$\displaystyle \Rightarrow P=\frac1T\int^T_0p(t)dt=\frac{V_mI_m}2cos(\theta_v-\theta_i)$$

### Reactive power 无功功率

$\displaystyle P_x(t)=P(t)-P_R(t)=\frac{V_mI_m}2sin(\theta_v-\theta_i)\cdot sin(2wt+2\theta_i+\pi)$

$$\displaystyle \Rightarrow Q=\frac1T\int^T_0p_x(t)dt=\frac{V_mI_m}2sin(\theta_v-\theta_i)$$

## 谐振

![image-20220604154726320](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220604154726320.png)

## 变压器(同名端相同n为正,不同n为负)

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220619094118996.png" alt="image-20220619094118996" style="zoom: 25%;" />

将二次电路映射到一次侧从而消去变压器的一般规则是:二次阻抗除以$n^2$,二次电压除以n,二次电流乘以n

将一次电路映射到二次侧从而消去变压器的一般规则是:一次阻抗乘以$n^2$,一次电压乘以n,一次电流除以n

## 三相电路(等负载)

|                                 |                          $\Delta$型                          | Y型                                                          |
| ------------------------------- | :----------------------------------------------------------: | ------------------------------------------------------------ |
| Line Votage                     |  $\widetilde{V_{ab}},\widetilde{V_{bc}},\widetilde{V_{ca}}$  | $\widetilde{V_{ab}},\widetilde{V_{bc}},\widetilde{V_{ca}}$   |
| LIne current                    |      $\widetilde{I_a},\widetilde{I_b},\widetilde{I_c}$       | $\widetilde{I_a},\widetilde{I_b},\widetilde{I_c}$            |
| Phase votage                    |  $\widetilde{V_{AB}},\widetilde{V_{BC}},\widetilde{V_{CA}}$  | $\widetilde{V_{AN}},\widetilde{V_{BN}},\widetilde{V_{CN}}$   |
| phase current                   |                    $I_{AB},I_{BC},I_{CA}$                    | $\widetilde {I_A}\widetilde{I_B}\widetilde{I_C}$             |
| Line voltage V.S. phase voltage | $\widetilde{V_{ab}}=\widetilde{V_{AB}}\\\widetilde{V_{bc}}=\widetilde{V_{BC}}\\\widetilde{V_{ca}}=\widetilde{V_{CA}}\\$ | $\widetilde{V_{AN}}=\frac{1}{\sqrt{3}}\widetilde {V_{ab}}\ang -30\degree\\\widetilde{V_{BN}}=\frac{1}{\sqrt{3}}\widetilde {V_{bc}}\ang -30\degree\\\widetilde{V_{CN}}=\frac{1}{\sqrt{3}}\widetilde {V_{ca}}\ang -30\degree$ |
| Line current V.S. Phase current | $\widetilde {I_{AB}}=\frac{1}{\sqrt 3}\widetilde {I_a}\ang30\degree\\\widetilde{I_{BC}}=\frac{1}{\sqrt 3}\widetilde{I_b}\ang30\degree\\\widetilde{I_{CA}}=\frac{1}{\sqrt 3}\widetilde I_c\ang30\degree\\$ | $\widetilde{I_A}=\widetilde{I_a}\\\widetilde{I_B}=\widetilde{I_b}\\\widetilde{I_C}=\widetilde{I_c}$ |
| phasor diagram                  | <img src="C:\Users\lcf\AppData\Roaming\Typora\typora-user-images\image-20220516083607115.png" alt="image-20220516083607115" style="zoom:25%;" /> | <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220516084324359.png" alt="image-20220516084324359" style="zoom: 50%;" /> |

$\displaystyle P(t)=P_a+P_b+P_c=\frac{3V_mI_m}2cos(\theta_v-\theta_i)$

### Bode plot

|                                                     | magnitude                                                    | phase                                                        |
| --------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| K常数                                               | 20log k                                                      | 0$\degree,\forall w$                                         |
| $(jw)^{\pm N}$                                      | $20(\pm N)dB/dec,\forall w\\passing(w=1,|H|_{dB}=0)$         | 90$\degree\forall w$                                         |
| $(1+j\frac{w}{w_0})^{\pm N}$                        | $20(\pm N)dB/dec.w\geq w_0\\|H|_{dB}=0,w\leq w_0\\passing(w_0,0)|H|_{dB}=0$ | $45\degree(\pm N)deg/dec,0.1w_0\leq w\leq 10w_0\\\ang H(w)=0,w\leq0.1 w_0\\\ang H(w)=90(\pm N)\geq 10w_0\\passing(0.1w_0,0)(10w_0,90(\pm N))$ |
| $[1+2\xi\frac{jw}{w_0}+(\frac{jw}{w_0})^2]^{\pm N}$ | $40(\pm N)dB/dec.w\geq w_0\\|H|_{dB}=0,w\leq w_0,\\passing(w_0,0),|H|_{dB}=0$ | $90\degree(\pm N)deg/dec,0.1w_0\leq w\leq10 w_0\\\angle H(w)=0,w\leq 0.1w_0\\\ang H(w)=180(\pm N),w\geq 10 w_0\\passing(w=0.1w_0,\ang H(w)=0)\\(w=10w_0,\ang H(w)=180(\pm N))$ |

## laplace

$$
\int^{+\infty}_{0^-}f(t)e^{-st} dt=F(S)
$$

|          | 时域f(t)变换                                                 | 频域F(S)变换                                          |
| -------- | ------------------------------------------------------------ | ----------------------------------------------------- |
| 线性变换 | $\mathcal L[a_1f_1(t)+a_2f_2(t)]=a_1F_1(S)+a_2F_2(S)$        | $a_1F_1(S)+a_2F_2(S)=\mathcal L[a_1f_1(t)+a_2f_2(t)]$ |
| 求导     | $\mathcal L[\frac d {dt}f(t)]=SF(s)-f(0^-)\\$                | $F'(S)=-\mathcal{L}[tf(t)]$                           |
| 连续求导 | $\mathcal L[\frac {d^n}{dt^n}d(t)]=S^nF(S)-\sum^n_{k=0}s^kf^{(n-1-k)}(0^-)\\$ | $F^{(n)}=(-1)^n\mathcal L[t^nf(t)]$                   |
| 积分     | $\mathcal L[\int^t_0f(t)dt]=\frac{1}{S}F(S)$                 | $\int^\infty_SF(S)=\mathcal L[\frac{f(t)}dt]$         |
| 平移     | $\displaystyle \mathcal L[f(t-\tau)]=e^{-s\tau}F(S)(\tau>0)$ | $F(s+a)=\mathcal L[e^{-at}f(t)]$                      |
| 缩放     | $\displaystyle\mathcal{L}[f(at)]=\frac{1}{a}F(\frac{s}{a})$  | $F(aS)=\mathcal L[\frac1af(\frac ta)]$                |

###  Initial value&Final value

$$
f(0^-)=\lim_{s\rightarrow \infty}sF(S)\\
f(\infty)=\lim_{s\rightarrow0}sF(s)
$$

## typical Laplace Transforms

| f(t)(t$\geq0$)                                 | F(s)                               |
| ---------------------------------------------- | ---------------------------------- |
| u(t)                                           | $\frac1S$                          |
| $e^{-at}$u(t)                                  | $\displaystyle\frac1{s+a}$         |
| coswt=$\displaystyle \frac{e^{jwt}+e^{-jwt}}2$ | $\displaystyle\frac{s}{s^2+w^2}$   |
| sinwt                                          | $\displaystyle\frac{w}{s^2+w^2}$   |
| u(t-T)                                         | $\displaystyle \frac{e^{-sT}}{s}$  |
| tu(t)                                          | $\displaystyle\frac1{s^2}$         |
| $t^nu(t)$                                      | $\displaystyle\frac {n!}{s^{n+1}}$ |
| $\delta (t)$                                   | 1                                  |

## inverse Laplace Transform拉普拉斯逆变换

### 5.1 Case1 :simple poles 单极点($Pi\neq P_j,\forall i\neq j)$

$$
F(S)=\frac{N(S)}{D(S)}=\frac{K_1}{S+P_1}+\frac{K_2}{S+P_2}+\cdots+\frac{K_n}{S+P_n}\\
f(t)=(K_1e^{-p_1t}+K_2e^{-p_2t}+\cdots+K_ne^{-P_nt})u(t)
$$

##### Reside Method (留数法)

$$
F(s)=\frac{K_1}{S+P_1}+\frac{K_2}{S+P_2}+\cdots+\frac{K_n}{S+P_n}\\
F(S)\cdot(S+P_1)\bigg|_{S-P_1}=K_1\\
\vdots\\
F(S)\cdot(S+P_2)\bigg|_{S-P_n}=K_n\\
$$

##### 5.2 Repeated poles(mutiple roots)重极点

e.g.$F(s)=\displaystyle\frac{N(s)}{P(s)}=\frac{K_1}{s+p}+\frac{K_2}{(s+p)^2}$
$$
Find K_r:F(S)(s+p)^r\bigg|_{s=-p}=K_r\\
 K_{r-1}:\frac d {ds}F(S)(s+p)^r\bigg|_{s=-p}=K_{r-1}\\
 \vdots\\
 K_{r-m}:\frac {d^m} {ds^m}F(S)(s+p)^r\bigg|_{s=-p}=K_{r-m}\\
 \vdots\\
 K_{1}:\frac {d^{r-1}} {ds^{r-1}}F(S)(s+p)^r\bigg|_{s=-p}=K_1\\
 
$$

#### 5.3 Complex poles (conjugate complex roots)

$$
F(S)=\frac{A_1S+A_2}{S^2+as+b}+F_1(S)\\
复数留数法/待定系数法\\
F(S)=\frac{K_1}{S+P}+\frac{K_2}{S+P^*}+F_1(S).\\
F(S)\cdot(S+P)\bigg|_{S-P}=K_1=a-bi\\
F(S)\cdot(S+P*)\bigg|_{S-P^*}=K_2=a+bi\\
\Rightarrow f(t)=K_1e^{-pt}+K_2e^{-P^*t}=K_1e^{-{\alpha+j\beta t}}+K_2e^{-{\alpha-j\beta t}}\\
=Re(K_1e^{-\alpha}(cos\beta t+isin\beta t)+K_2e^{-\alpha}(cos\beta t-isin\beta t))\\
=e^{-\alpha}2a\cos\beta t+e^{-\alpha}2b\sin\beta t
$$

## 元件拉普拉斯变换

| <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220606083824887.png" alt="image-20220606083824887" style="zoom: 33%;" /> | $v(t)=Ri(t)\xRightarrow{\mathcal L}V(S)=RI(S)$               | <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220611155059608.png" alt="image-20220611155059608" style="zoom:33%;" /> |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220606083944102.png" alt="image-20220606083944102" style="zoom: 33%;" /> | $\displaystyle V(t)=L\frac{di(t)}{dt}\xRightarrow {\mathcal L}V(S)=SLI(S)-Li(0^-)$ | <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220606084345164.png" alt="image-20220606084345164" style="zoom: 33%;" /> |
| <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220606084311519.png" alt="image-20220606084311519" style="zoom: 33%;" /> | $\displaystyle i(t)=C\frac{dv(t)}{dt}\xRightarrow {L(·)}\frac{1}{SC}I(S)-\frac{i(0^-)}{C}$ | <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220611155600805.png" alt="image-20220611155600805" style="zoom:33%;" /> |
