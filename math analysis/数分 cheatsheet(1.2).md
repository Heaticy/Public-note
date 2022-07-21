# 数分 cheatsheet 1.2

## 求导和积分

$\displaystyle\tan^2t =\frac{sin^2 t}{cos^2 t}=\frac{1}{cos^2t}-1=\sec^2 t-1$

$\displaystyle \sec x=\tan x \sec x\\ csc'(x)=-\ cotx\csc x$

$\displaystyle \int \sec x=\ln |\sec x+\tan x|+C$

$\displaystyle \int \csc xdx=\ln|\tan \frac x 2|+C=\ln|cscx-\cot x|+C$

$\displaystyle\int tanxdx=-ln|cosx|+C$

$\displaystyle \int cotxdx=ln|sinx|+C$

$\displaystyle \int\frac {dx}{a^2+x^2}=\frac1aarctan\frac xa\\ \int\frac {dx}{a^2-x^2}=\frac 2 a\ln\bigg|\frac{x-a}{x+a}\bigg|$

$\displaystyle\int\sqrt{x^2\pm a^2}dx=\frac12[x\sqrt{x^2\pm a^2}\pm a^2ln\bigg|x+\sqrt {x^2\pm a^2}\bigg|]$

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220615144139690.png" alt="image-20220615144139690" style="zoom: 40%;" />
$$
\int xsinnxdx=\frac{-xcosnx}{n}+\frac{sinnx}{n^2} \ \ \ \ \int xcosnxdx=\frac{xsinnx}{n}+\frac{cosnx}{n^2}\\
\int x^2sinnxdx=-\frac{x^2cosnx}{n}+\frac{2xsinnx}{n^2}+\frac{2cosnx}{n^3}\ \ \ \ \int x^2cosnxdx=\frac{x^2sinnx}{n}+\frac{2xcosnx}{n^2}-\frac{2sinnx}{n^3}
$$

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220615144325153.png" alt="image-20220615144325153" style="zoom:50%;" />

## 积化和差

$$
sin\alpha sin\beta=-\frac{1}{2}[cos(\alpha+\beta)-cos(\alpha-\beta)]\\
cos\alpha cos\beta=\frac{1}{2}[cos(\alpha+\beta)-cos(\alpha-\beta)]\\
sin\alpha cos\beta=\frac{1}{2}[sin(\alpha+\beta)+sin(\alpha-\beta)]\\
cos\alpha sin\beta=\frac{1}{2}[sin(\alpha+\beta)-sin(\alpha-\beta)]
$$

## 部分和

$$
\sum^n_{n=1}sinnx=\frac{cos\frac{1}{2}x-cos(n+\frac{1}{2})x}{2sin\frac{1}{2}x}\\
\sum^n_{n=1}cosnx=\frac{sin(n+\frac{1}{2})x-sin\frac{1}{2}x}{2sin\frac{1}{2}x}=\frac{cos(n+\frac{1}{2})x-cos\frac{1}{2}x}{2cos\frac{1}{2}x}\\
$$


## 幂级数

$$
\frac1{1-x}=\sum^{\infty}_{n=0}x^n,\ \ \ \ \ \ \ \ \frac1{1+x}=\sum^{\infty}_{n=0}(-1)^nx^n\ \ \ \ \ \ \ \ \
e^x=\sum^\infty_{n=0}\frac{x^n}{n!}\\
sinx=\sum^\infty_{n=1}(-1)^n\frac{x^{2n+1}}{(2n+1)!},\ \ \ \ \ \ \ \ \ \ \ \ \ \ 
cosx=\sum^\infty_{n=1}(-1)^n\frac{x^{2n}}{(2n)!}\\
$$

### 华里士公式

![关键词：“华里士公式”](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/v2-28fdb926e4ba3113da4b1ef7fbf8adbf_1440w.jpg)

### 绕X轴的旋转


$$
x′=x\\
y′=ycosθ−zsinθ\\
z′=ysinθ+zcosθ\\
$$

$$
\begin{bmatrix}
    x'\\
    y'\\
    z'
\end{bmatrix}
=\begin{bmatrix}
    1&0&0\\
    0&cos\theta&-sin\theta\\
    0&sin\theta&cos\theta
\end{bmatrix}
\begin{bmatrix}
    x\\
    y\\
    z
\end{bmatrix}
$$

### 绕Y轴的旋转

$$
x′=zsinθ+xcosθ\\
y′=y\\
z′=zcosθ−xsinθ
$$

$$
\begin{bmatrix}
    x'\\
    y'\\
    z'
\end{bmatrix}
=\begin{bmatrix}
    cos\theta&0&sin\theta\\
    0&1&0\\
    -sin\theta&0&cos\theta
\end{bmatrix}
\begin{bmatrix}
    x\\
    y\\
    z
\end{bmatrix}
$$

### 绕Z轴旋转

$$
\begin{bmatrix}
    x'\\
    y'\\
    z'
\end{bmatrix}
=\begin{bmatrix}
cos\theta&-sin\theta&0\\
sin\theta&cos\theta&0\\
0&0&1
\end{bmatrix}
\begin{bmatrix}
    x\\
    y\\
    z
\end{bmatrix}
$$

## 隐函数的可导性

$1\degree 考虑三维空间的一个方程$
$$
F(x,y,z)=0
$$
一般来说,它取定了三维空间的一个曲面

$设z=f(x,y),则$
$$
F_x'+F_z'f_x'=0;F_y'+F_z'f_y'=0\\

\frac{\partial z}{\partial x}=-\frac{F_x'(x,y,z)}{F_z'(x,y,z)},
\frac{\partial y}{\partial x}=-\frac{F_y'(x,y,z)}{F_z'(x,y,z)},
$$

$2\degree 考虑两个方程构成的方程组$
$$
F(x,y,z)=0,G(x,y,z)=0\\
此时这个隐函数只有一个自由度,受到两个约束\\
y=y(x),z=z(x)\\
F(x,y(x),z(x))=0,G(x,y(x),z(x))=0\\
y'(x)=-\frac{F_x'G_z'-F_z'G_z'}{F_y'G'_z-F_z'G'_y}\\
z'(x)=\frac{F_x'G_y'-F_z'G_x'}{F_y'G'_z-F_z'G'_y}\\
$$

$3\degree 四位空间两个方程构成的方程组$
$$
F(x,y,u,v)=0,G(x,y,u,v)=0
$$

$$
\frac{\partial u}{\partial x}=\frac{\displaystyle-\frac{\partial(F,G)}{\partial(x,v)}}{\displaystyle\frac{\partial(F,G)}{\partial(u,v)}};\ \ \ \ \ 
\frac{\partial v}{\partial x}=\frac{\displaystyle-\frac{\partial(F,G)}{\partial(u,x)}}{\displaystyle\frac{\partial(F,G)}{\partial(u,v)}}
$$

$$
\frac{\partial u}{\partial y}=\frac{\displaystyle-\frac{\partial(F,G)}{\partial(y,v)}}{\displaystyle\frac{\partial(F,G)}{\partial(u,v)}};\ \ \ \ \ 
\frac{\partial v}{\partial y}=\frac{\displaystyle-\frac{\partial(F,G)}{\partial(u,y)}}{\displaystyle\frac{\partial(F,G)}{\partial(u,v)}}
$$

## 曲率

$$
\kappa=\frac{\vec r'\times {\vec r''}}{|\vec r'|^3}
$$

### 法向量场

$$
\vec{r_u'}(u,v)\times\vec{r_v'}(u,v)=\frac{\partial(y,z)}{\partial (u,v)}\vec{i}+\frac{\partial (z,x)}{\partial (u,v)}\vec{j}+\frac{\partial (x,y)}{\partial(u,v)}\vec{k}\\
$$

$$
|\vec{r_u'}\times \vec{r_u'}|^2=|\vec{r_u'}|^2|\vec{r_v'}|^2-(\vec{v_u'}\cdot\vec{r_v'})^2\\
E=\vec{r_u'}^2={x'}_u^2+{y'_u}^2+{z'_u}^2\\
F=\vec{r_v'}^2={x'}_v^2+{y'_v}^2+{z'_v}^2\\
G=\vec{r_u'}\cdot\vec{r_v'}=x_u'x_v'+y_u'y_v'+z_u'z_v'\\
|\vec{r_u'}\times \vec{r_v'}|=\sqrt{EF-G^2}\\
单位法向量\vec{n}=\frac{\vec{r_u'}\times \vec{r_v'}}{|\vec{r_u'}\times \vec{r_v'}|}
$$

## 二元函数的微分中值定理

$$
f(x+h,y+k)-f(x,y)=hf_x'(x+\theta h,y+\theta k)+kf'_y(x+\theta h,y+\theta k)
$$

## 二元函数的Taylor展开公式

$$
f(x,y)=f(x_0+h,y_0+k)=\sum^n_{m=0}\frac{1}{m!}\mathcal{D}^mf(x_0,y_0)\\
其中\mathcal{D}=h\frac{\partial }{\partial x}+k\frac{\partial}{\partial y}
$$

##

## 二重积分换元法

$$
\iint_Df(x,y)dxdy=\iint_{D'}f(x(u,v),y(u,v))|\frac{\partial(x,y)}{\partial(u,v)}|\Delta u\Delta v
$$

**特别地**$x=r\cos\theta,y=r\cos\theta$
$$
|\frac{\partial(x,y)}{\partial(u,v)}|=\begin{vmatrix}cos\varphi&sin\varphi\\-rsin\varphi&rcos\varphi\end{vmatrix}=r
$$

## 三重积分换元法

$$
\iiint_Vf(x,y,z)dxdydz
=\iiint_{V'}f(x(u,v,w),y(u,v,w),z(u,v,w))|\frac{\partial(x,y,z)}{\partial(u,v,w)}|du\ dv\ dw
$$

$$
特殊的\begin{cases}
x=rsin\theta\cos\varphi\\
y=rsin\theta\sin\varphi\\
z=rcos\theta
\end{cases}
\Longrightarrow \frac{\partial(x,y,z)}{\partial(r,\theta,\varphi)}=r^2sin\theta
$$

## 数量场在曲线上的积分

$$
\int_L\varphi(x,y,z)ds=\int^{\beta}_{\alpha}\varphi(x(t),y(t),z(t))|\vec v'(t)|dt
\\=\int^{\beta}_{\alpha}\varphi(x(t),y(t),z(t))\sqrt{x'(t)+y'(t)+z'(t)} dt,t\in[\alpha.\beta]
$$

## 向量场在曲线上的积分

$$
L_{AB}:\vec r=\vec r(t)=x(t)\vec i+y(t)\vec j+z(t)\vec k,\alpha\leq t\leq \beta
\\向量场\vec v=P(x,y,z)\vec i+Q(x,y,z)\vec j +z(t)\vec k,

\\则\int_{AB}\vec v\cdot d\vec r=\int^{\beta}_\alpha[Px'(t)+Qy'(t)+Rz'(t)]dt
\\其中\vec v'不是曲线的法向量而是曲线的切向量（方向向量）
$$

### 格林公式

若D是有限条逐段光滑的封闭曲线L围成的平面闭区域（L=$\partial D$),$$\vec v=P(x,y)\vec i+Q(x,y)\vec j$$则
$$
\oint_{\partial D}Pdx+Qdy=\iint_D (\frac{\partial Q}{\partial x }-\frac{\partial P}{\partial y})dxdy
$$
其中曲线积分的方向为L=$\partial D$的逆时针方向

**注意,D的内部不能有任何瑕点,必须把瑕点绕开**(一般用半径为r的小邻域)

### 格林公式推论11.6

设D是满足Green 定理中条件的 区域，$$\sigma(D)$$表示D的面积，$\partial D$为D的边界

则
$$
\sigma (D)=\frac12\oint_{\part D}(-ydx+xdy)=\oint_{\part D}(-ydx)=\oint_{\part D}xdy.
$$

## 数量场在曲面上的积分

### 法向量场

$$
\vec r_u'(u,v)\times\vec r_v'(u,v)=\frac{\partial(y,z)}{\part(u,z)}\vec i+\frac{\part(z,x)}{\part(u,v)}\vec j+\frac{\part(x,y)}{\part(u,v)}\vec k\\
=|\vec {r'}_u'|^2|\vec r_u'|^2-(\vec r_u'\cdot\vec r_v')^2
\\E=\vec {r'}_u^2={x'}_u^2+{y'}_u^2+{z'}_u^2
\\G=\vec {r'}_v^2={x'}_v^2+{y'}_v^2+{z'}_v^2
\\F=\vec {r'}_u\cdot\vec{r'}_v=x_u'x_v'+y'_uy_v'+z_u'z_v'\\
\vec{r'}_u\times\vec{r'}_v=\sqrt{EG-F^2}
\\记\vec n=\frac{\vec{r'}_u\times\vec{r'}_v}{|\vec{r'}_u\times\vec{r'}_v|}为单位法向量
$$



### 计算

$$
\iint_S\varphi(x,y,z)dS=\iint_D\varphi(x(u,v),y(u,v),z(u,v))\sqrt{EG-F^2}dudv
\\特别地，当u，v是x,y时=\iint_D\varphi(x,y,z(x,y))\sqrt{1+z^2_x+z^2_y}dxdy\\
特别地,当x=Rsin\theta cos\varphi,y=Rsin\theta sin\varphi,z=Rcos\theta时,dS=R^2sin\theta d\theta d\varphi
$$

## 向量场在曲面上的积分

## 计算

1. $对于已知参数曲面r(u,v)=(x(u,v),y(u,v),z(u,v)),where(u,v)\in D\sub\R^2$

$$
n=\frac{\vec r_u'\times \vec r_v'}{|\vec r_u'\times \vec r_v'|},dS=|\vec r_u'\times \vec r_v'|dudv\\

d\vec S=\vec ndS=\frac{\vec r_u'\times\vec r_v'}{|\vec r_u'\times \vec r_v'|}|\vec r_u'\times \vec r_v'|dudv
=({\vec r_u'\times \vec r_v'})dudv\\
其中\vec r_u'\times \vec r_v'=(\frac{\partial(y,z)}{\partial(u,v)},\frac{\partial(z,x)}{\partial(u,v)},\frac{\partial(x,y)}{\partial(u,v)})
\\原向量场积分转化为二重积分\iint_S\vec v\cdot(\vec r_u'\times \vec r_v')dudv\\
\\\iint_D(P\frac{\partial(y,z)}{\partial(u,v)}+Q\frac{\partial(z,x)}{\partial(u,v)}+R\frac{\partial(x,y)}{\partial(u,v)})dudv
\\
定向问题：检查\vec r_u'\times \vec r_v'=(\frac{\partial(y,z)}{\partial(u,v)},\frac{\partial(z,x)}{\partial(u,v)},\frac{\partial(x,y)}{\partial(u,v)})的方向和题目给的定向是否一致
$$

$$
特殊的，当参数曲面是球坐标的时候，\vec v'_\theta\times\vec v'_\varphi的反向向外
\\\vec r_\theta'\times \vec r_\varphi'=(\frac{\partial(y,z)}{\partial(\theta,\varphi)},\frac{\partial(z,x)}{\partial(\theta,\varphi)},\frac{\partial(x,y)}{\partial(\theta,\varphi)})=(sin^2\theta cos\varphi,sin^2\theta\sin\varphi,cos\theta\sin\theta)
$$



2.对于$\vec v=\vec v(x,y,z),隐函数曲面F(x,y,z)=0$
$$
对隐函数求导得到F_x,F_y,F_z\\
\vec n=\vec n(x,y,z)=\frac{(F_x,F_y,F_z)}{|(F_x,F_y,F_z)|}=(a,b,c)
\\转化为第一类曲面积分\iint_S\vec v \cdot\vec S=\iint_S\vec v \cdot\vec n\cdot dS
\\定向问题：检查\vec n 的方向是否和题目所给的方向一致
$$
注意:**此时的$\vec n$是单位法向量**,此时$dS=|\vec r_u'\times \vec r_v'|dudv$视作数量场的曲面积分

## 高斯定理(散度定理)

### 向量场的曲面积分转化成三重积分

已知光滑向量场$$v(x,y,z)=P(x,y,z)i+Q(x,y,z)j+R(x,y,z)k$$通过空间中V的表面$S=\partial V$
$$
\oiint_S \vec v\cdot d\vec S=\iiint_V(\frac{\part P}{\part x}+\frac{\part Q}{\part y}+\frac{\part R}{\part z})dxdydz\\=\iiint_V\ div\ \vec v\ dV
$$
**注意，和格林公式一样，当S中有瑕点时就不能使用**

## 斯托克斯定理(旋度定理)

$$
rot\vec v=\nabla\times \vec{v}=\\
 \begin{vmatrix}
    i&j&k\\
    \displaystyle\frac{\partial}{\partial x}&\displaystyle\frac{\partial}{\partial y}&\displaystyle\frac{\partial}{\partial z}\\
    P&Q&R
 \end{vmatrix}
$$

### 向量场的曲线积分转化成向量场的曲面积分

设光滑向量场$$v(x,y,z)=P(x,y,z)i+Q(x,y,z)j+R(x,y,z)k$$

**S定向和L定向满足右手定则**
$$
\oint_L Pdx+Qdx+Rdz\\=\iint_S(\frac{\part R}{\part y}-\frac{\part Q}{\part z})dydz+(\frac{\part P}{\part z}-\frac{\part R}{\part x})dzdx+(\frac{\part Q}{\part x}-\frac{\part P}{\part y})dxdy\\=\iint _S\grad \times v \cdot d\vec S
$$

**注意，和格林公式一样，当S中有瑕点时就不能使用**

## 保守场

$$
\nabla \times \vec v=0(v的旋度为0)是保守场,积分与路径无关,且存在一个数量场势函数\varphi\\
s.t.\vec v=\nabla \varphi\\
即v是\varphi的梯度,\varphi的三个偏导对应\vec v 的三个函数
$$

## 无源场

$$
div\vec v=\nabla\cdot \vec v=0(散度为0)\\
是无源场,存在一个向量势\vec \alpha使得 rot\alpha=\vec v
$$

## Fourier 级数

$$
周期函数f(x)可以展开为\\
f(x)=\frac{a_0}{2}+\sum^\infty_{n=1}(a_ncosnx+b_nsinnx)\\
a_n=\frac{1}{\pi}\int^\pi_{-\pi}f(x)cosnxdx\ \ \ \ \ \ \ (n=0,1,2,\cdots)\\
b_n=\frac{1}{\pi}\int^\pi_{-\pi}f(x)sinnxdx\ \ \ \ \ \ \ (n=0,1,2,\cdots)\\
$$

$$
周期函数f(x)可以展开为\\
f(x)=\frac{a_0}{2}+\sum^\infty_{n=1}(a_ncos\frac{n\pi}{l}x+b_nsin\frac{n\pi}{l}x)
\\a_n=\frac{1}{l}\int^l_{-l}f(x)cos\frac{n\pi}{l}xdx\ \ \ \ \ \ \ (n=0,1,2,\cdots)\\
b_n=\frac{1}{\pi}\int^l_{-l}f(x)sin\frac{n\pi}{l}xdx\ \ \ \ \ \ \ (n=0,1,2,\cdots)\
$$


$$
a_n=-\frac{b'_n}{n},b_n=\frac{a_n'}{n}\\
其中a'_n,b_n'是f'(x)的Fourier系数,前提是f'(x)得有傅里叶系数
$$


### 定理12.7(Parseval等式)

$设函数f(x)\in L^2[-\pi,\pi],则f(x)的Fourier级数部分和S_n(x)构成的三角多项式列平方平均收敛于f(x)$

$$
\frac{a_0^2}{2}+\sum^n_{k=1}(a_k^2+b_k^2)=\frac1{\pi}\int^\pi_{-\pi}f^2(x)dx
$$

### 推论12.9

$$
\frac{1}{\pi}\int^{\pi}_{-\pi}f(x)g(x)dx=[\frac{a_0\alpha_0}{2}+\sum^n_{k=1}(\alpha_ka_k+\beta_kb_k)]
$$

### 引理 13.6(第二积分平均值定理)

$设f(x)在[a,b]上可积$
$$
1\degree 如果g(x)在[a,b]上非负且单调递减,那么\exists\varepsilon\in[a,b],S.T.\\
\int^b_af(x)g(x)dx=g(a)\int^\varepsilon_a f(x)dx\\
2\degree 如果g(x)在[a,b]上非负且单调递减,那么存在\eta\in[a,b],S.T.\\
\int^b_af(x)g(x)=g(b)\int^b_af(x)dx\\
3\degree 如果g(x)在[a,b]上单调,那么存在\xi\in[a,b],S.T.\\
\int^b_af(x)g(x)dx=g(a)\int^{\xi}_af(x)dx+g(b)\int^b_\xi f(x)
dx
$$

## 定理13.21

$设函数f(x,u)在I=[a,b]\times[\alpha,\beta]上连续且对u有连续的偏微商,a(u)和b(u)在[\alpha,\beta]上可微,并且$
$$
a\leq a(u)\leq b,a\leq b(u)\leq b,
$$
$则函数\phi在区间[\alpha,\beta]上可微,并有$
$$
\phi'(u)=\int^{b(u)}_{a(u)}\frac{\partial f(x,u)}{\partial u}dx+f(b(u),u)b'(u)-f(a(u),u)a'(u)
$$

