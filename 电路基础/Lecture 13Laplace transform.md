# Lecture 13 laplace Transform

 $\large 拉普拉斯变换$

## 1.Motivation

![image-20220530082740281](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220530082740281.png)

## 2.Introduction of Laplace transform

“Power series”幂级数
$$
x^0,x^1,x^2,\cdots x^n
$$
$\displaystyle \Rightarrow \sum^{\infty}_{n=0}a(n)x^n=A(x)$


$$
a(n)\longrightarrow A(x)\\
1\longrightarrow \frac1 {1-x},|x|<1\\
\frac1{n!}\longrightarrow e^x
$$
Continuous analog:

n=0,1,2$\cdots\longrightarrow t\leq t< +\infty$
$$
\int^{+\infty}_{0^-}a(t)x^t dt=A(X)\\
x^t=(e^{lnx})^t(0<x<1)\\
令s=lnx\\
\int^{+\infty}_{0^-}f(t)e^{-st} dt=F(S)(即拉普拉斯变换)\\
$$
$注:input f(t)\xrightarrow{transform} outputF(s)\\input f(t)\xrightarrow{operator} outputg(t)$

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220530084744867.png" alt="image-20220530084744867" style="zoom: 33%;" />
$$
Note:1\degree f(t):0\leq t<\infty\\
\Rightarrow 设f(t)=0(t<0)\\
2\degree f(t)\leftrightarrow F(s)
$$

### 3.1 Laplace transform(linear)

$$
\mathcal L[a_1f_1(t)+a_2f_2(t)]=a_1\mathcal{L}[f_1(t)]+a_2\mathcal{L}[f_2(t)]
$$



### 3.2 time Differentiation

$$
\mathcal L[\frac d {dt}f(t)]=SF(s)-f(0^-)\\
$$

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220530090010188.png" alt="image-20220530090010188" style="zoom: 25%;" />

$$
\mathcal L[\frac {d^n}{dt^n}d(t)]=S^nF(S)-\sum^n_{k=0}s^kf^{(n-1-k)}(0^-)\\
$$
> $$
Proof:\mathcal L[\frac {d^n}{dt^n}f(t)]=\mathcal {L}(\frac{d}{dt}[\frac {d^{n-1}}{dt^{n-1}}f(t)])\\
=S\cdot \mathcal L[\frac {d^{n-1}}{dt^{n-1}}f(t)]-f^{(n-1)}(0^-)\\
=S\cdot \mathcal L[\frac {d^{n-2}}{dt^{n-2}}f(t)]-S^{n-1}f(0^-)-S^{n-2}f^{(1)}(0^-)-S^{n-2}f(0^-)-S^{n-2}f^{(2)}(0^-)\\=S^nF(S)-\sum^n_{k=0}s^kf^{(n-1-k)}(0^-)
 > $$

### 3.3 time integration(时域积分)

$$
\mathcal L[\int^t_0f(t)dt]=\frac{1}{S}F(S)
$$



### 3.4 time shift(时域平移)

$\displaystyle L[f(t-\tau)]=e^{-s\tau}F(S)(\tau>0)$

> Proof:
> $$
> \int^\infty_{0-}f(t-\tau)e^{-st}dt\\
> =\int^\infty_{0-}f(t-\tau)\cdot e^{-s(t-\tau)}e^{-s\tau}d(t-\tau)\\
> =e^{-s\tau}F(s)
> $$

### 3.5 Frequency shift(频域平移)

$$
F(s+a)=\mathcal L[e^{-at}f(t)]
$$

### 3.6 Frequency differentiation(频域求导)

$$
F'(S)=-\mathcal{L}[tf(t)]
$$

### 3.7 Frequency integraton

$$
\int^\infty_SF(S)=\mathcal L[\frac{f(t)}dt]
$$

### 3.8 Scaling

$$
\mathcal{L}[f(at)]=\frac{1}{a}F(\frac{s}{a})
$$
### 3.9 Initial value

$$
f(0^-)=\lim_{s\rightarrow \infty}sF(S)
$$

### 3.10 Final value

$$
f(\infty)=\lim_{s\rightarrow0}sF(s)
$$



## 4.typical Laplace Transforms

| f(t)(t$\geq0$)                                 | F(s)                              |
| ---------------------------------------------- | --------------------------------- |
| u(t)                                           | $\frac1S$                         |
| $e^{-at}$u(t)                                  | $\displaystyle\frac1{s+a}$        |
| coswt=$\displaystyle \frac{e^{jwt}+e^{-jwt}}2$ | $\displaystyle\frac{s}{s^2+w^2}$  |
| sinwt                                          | $\displaystyle\frac{w}{s^2+w^2}$  |
| u(t-T)                                         | $\displaystyle \frac{e^{-sT}}{s}$ |
| tu(t)                                          | $\displaystyle\frac1{s^2}$        |
| $t^nu(t)$                                      | $\frac {n!}{s^{n+1}}$             |

### 4.1 u(t)

$$
\mathcal L[u(t)]=\int_{0^-}^{\infty}u(T)
$$

### 4.2 coswt



### 4.4 tu(t)

$$
\mathcal L[tu(s)]=-(\frac{1}S)'=-(-1)\frac1{s^2}=\frac{1}{s^2}\\
$$

### 4.5 $t^nu(t)$

$$
\mathcal L(t^n u(t))=\int^{\infty}_{0^-}t^ne^{-st}dt=-\frac1s[t^ne^{-st}|^{\infty}_{0^-}\int ^{\infty}_{0-}t^{n-1}dt]\\
=\frac ns\int^{\infty}_{0^-}t^{n-1}e^{-st}dt
$$



## 5.inverse Laplace Transform拉普拉斯逆变换

$$
定义 f(t)=\frac1{2\pi j}\int^{j+\infty}_{j-\infty}F(s)e^{st}ds\ 太复杂\\
$$

一般我们把F(S)拆成几部分，然后查表匹配.

### 5.1 Case1 :simple poles 单极点($Pi\neq P_j,\forall i\neq j)$

$$
F(S)=\frac{N(S)}{D(S)}=\frac{K_1}{S+P_1}+\frac{K_2}{S+P_2}+\cdots+\frac{K_n}{S+P_n}\\
f(t)=(K_1e^{-p_1t}+K_2e^{-p_2t}+\cdots+K_ne^{-P_nt})u(t)
$$

![image-20220601090029179](D:\lcf\Pictures\markdown\Lecture 13Laplace transform\image-20220601090029179.png)

##### Method 2:Reside Method (留数法)

$$
F(s)=\frac{K_1}{S+P_1}+\frac{K_2}{S+P_2}+\cdots+\frac{K_n}{S+P_n}\\
F(S)\cdot(S+P_1)=K_1+(\frac{K_2}{S+P_2}+\cdots+\frac{K_n}{S+P_n})(S+P_1)
$$

##### 5.2 Repeated poles(mutiple roots)重极点

(Assume r repeated poleds at s=-p)

e.g.$F(s)=\frac{N(s)}{P(s)}=\frac{K_1}{s+p}+\frac{K_2}{(s+p)^2}$

![image-20220601091922200](D:\lcf\Pictures\markdown\Lecture 13Laplace transform\image-20220601091922200.png)

![image-20220601092859343](D:\lcf\Pictures\markdown\Lecture 13Laplace transform\image-20220601092859343.png)

#### 5.3 Complex poles (conjugate complex roots)

$$
F(S)=\frac{A_1S+A_2}{S^2+as+b}+F_1(S)\\
method1:"Residue\ method"\\
F(S)=\frac{K_1}{S+P}+\frac{K_2}{S+P^*}+F_1(S).\\
\Rightarrow f(t)=K_1^{-pt}+K_2e^{-P^*t}
$$

![image-20220601095134135](D:\lcf\Pictures\markdown\Lecture 13Laplace transform\image-20220601095134135.png)

![image-20220601095222071](D:\lcf\Pictures\markdown\Lecture 13Laplace transform\image-20220601095222071.png)

![image-20220601095652912](D:\lcf\Pictures\markdown\Lecture 13Laplace transform\image-20220601095652912.png)

## 6.application to integredifferentiel equations


$$
\frac {d^2v(t)}{dt^2}+6\frac{dv(t)}{dt}+8v(t)=2u(t)\\
v(Q)=1,v'(0^-)=-2
$$
![image-20220606083244191](D:\lcf\Pictures\markdown\Lecture 13Laplace transform\image-20220606083244191.png)

## 7.Laplace transform in circuit analysis

| <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220606083824887.png" alt="image-20220606083824887" style="zoom: 33%;" /> | $v(t)=Ri(t)\xRightarrow{\mathcal L}V(S)=RI(S)$               | <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220611155059608.png" alt="image-20220611155059608" style="zoom:33%;" /> |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220606083944102.png" alt="image-20220606083944102" style="zoom: 33%;" /> | $\displaystyle V(t)=L\frac{di(t)}{dt}\xRightarrow {\mathcal L}V(S)=SLI(S)-Li(0^-)$ | <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220606084345164.png" alt="image-20220606084345164" style="zoom: 33%;" /> |
| <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220606084311519.png" alt="image-20220606084311519" style="zoom: 33%;" /> | $\displaystyle i(t)=C\frac{dv(t)}{dt}\xRightarrow {L(·)}\frac{1}{SC}I(S)-\frac{i(0^-)}{C}$ | <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220611155600805.png" alt="image-20220611155600805" style="zoom:33%;" /> |

![image-20220606084956062](D:\lcf\Pictures\markdown\Lecture 13Laplace transform\image-20220606084956062.png)

![image-20220606090819898](D:\lcf\Pictures\markdown\Lecture 13Laplace transform\image-20220606090819898.png)

![image-20220606091849161](D:\lcf\Pictures\markdown\Lecture 13Laplace transform\image-20220606091849161.png)

![image-20220606092907752](D:\lcf\Pictures\markdown\Lecture 13Laplace transform\image-20220606092907752.png)