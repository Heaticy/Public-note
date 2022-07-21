![image-20220506222229072](C:\Users\lcf\AppData\Roaming\Typora\typora-user-images\image-20220506222229072.png)
$$
证明:f(x_1,x_2.x_3...x_n)=x_1x_2....x_n(\frac1{x_1}+\frac1{x_2}+....\frac1{x_n})\\\varphi(x_1,x_2....x_n)=x_1+x_2+x_3+.....x_n-n=0\\
设F(x_1,x_2,x_3...x_n)=x_1x_2....x_n(\frac1{x_1}+\frac1{x_2}+....\frac1{x_n})+\lambda(x_1+x_2+x_3+...x_n-n)\\
由拉格朗日乘数法\begin{cases}
\displaystyle F'_{x_1}=x_2x_3...x_n(\frac1{x_2}+\frac1{x_3}....\frac1{x_n})+\lambda=0\\
\displaystyle F'_{x_2}=x_1x_3...x_n(\frac1{x_1}+\frac1{x_3}....\frac1{x_n})+\lambda=0\\
\displaystyle F'_{x_1}=x_1x_2...x_n(\frac1{x_1}+\frac1{x_2}....\frac1{x_n})+\lambda=0\\
.\\
.\\
.\\
x_1+x_2+x_3+.....x_n=n
\end{cases}
\\
\begin{cases}
\displaystyle x_3x_4...x_n+x_2x_4...x_n+....+\lambda=0(1)\\
\displaystyle x_3x_4...x_n+x_1x_4...x_n+....+\lambda=0(2)\\
\displaystyle x_2x_4...x_n+x_1x_4...x_n+....+\lambda=0\\
.\\
.\\
.\\
x_1+x_2+x_3+.....x_n=n
\end{cases}
\\由(1)(2)相减
(x_2-x_1)(x_4x_5...x_n+x_3x_5...x_n+.....)=0\\即(x_2-x_1)(\frac1{x_3}+....\frac1{x_n})x_3...x_n=0
\\\because x_n>0 \therefore x_2-x_1=0\\
同理x_2=x_3
\\\therefore x_1=x_2=x_3=x_4=....x_n=1
\\此时函数有极值 f(1,1,1,1....1)=n
\\由题意，函数是基本初等函数，在定义域内连续
\\\lim_{x_1\rightarrow 0}f(x_1,x_2...x_n)=x_2x_3...x_n\leq(\frac1n)^n<1\leq n
\\\therefore 该极值必是极大值
\\\therefore x_1x_2....x_n(\frac1{x_1}+\frac1{x_2}+....\frac1{x_n})\leq n
$$
![image-20220506233318546](C:\Users\lcf\AppData\Roaming\Typora\typora-user-images\image-20220506233318546.png)
$$
(1)证否：设H=MBM^T,H=
\left[
\begin{matrix}
 \eta_1      \\
 &   \eta_2\\
  &  & \ddots & \\
 & & & \eta_{n-1}     \\
\end{matrix}
\right]\\
设N=
\left[ \begin{matrix}
1&0\\0&M
\end{matrix}
\right]\\
NAN^T=
\left[ \begin{matrix}
1&0\\0&M
\end{matrix}
\right ]
\left[ \begin{matrix}
a_{11}&C^T\\C&B
\end{matrix}
\right ]
\left[ \begin{matrix}
1&0\\0&M^T
\end{matrix}
\right ]=
\left[ \begin{matrix}a_{11}&C^T\\C&MBM^T
\end{matrix}
\right ]\\
=\left[ \begin{matrix}a_{11}&C^T\\C&H 
\end{matrix}
\right ]\\
=\left[ 
\begin{matrix}
a_{11}&b_1&b_2&\cdots&b_{n-1}\\ 
 b_1&\eta_1      \\
 b_2&  & \eta_2\\
 \vdots&  && \ddots & \\
 b_{n-1}& & & & \eta_{n-1}     \\
\end{matrix}
\right]
=D\\
|D-\eta_1I|=
\left |
\begin{matrix}
a_{11}-\eta_1&b_1&b_2&\cdots&b_{n-1}\\ 
 b_1&0     \\
 b_2&  & \eta_2-\eta_1\\
 \vdots&  && \ddots & \\
 b_{n-1}& & & & \eta_{n-1}-\eta_1     \\
\end{matrix}
\right |\\=
\left |
\begin{matrix}
a&0&0&\cdots&b_0\\ 
0&0     \\
0&  & \eta_2-\eta_1\\
 \vdots&  && \ddots & \\
0& & & & \eta_{n-1}-\eta_1     \\
\end{matrix}
\right |=0
\\\eta_1是D的特征值
\\同理\eta_i(i=1,2,....n-1)是D的特征值
$$

$$
|D-(a_{11}-\frac{b_1^2}{\eta_1}-\frac{b_2^2}{\eta_2}-...-\frac{b_{n-1}^2}{\eta_{n_1}})I|=0
\\\therefore NAN^T=D=P
\left[
\begin{matrix}
 \eta_1      \\
 &   \eta_2\\
  &  & \ddots & \\
 & & & \eta_{n-1}     \\
 & & & & a_{11}-\frac{b_1^2}{\eta_1}-\frac{b_2^2}{\eta_2}-...-\frac{b_{n-1}^2}{\eta_{n-1}}
\end{matrix}
\right]P^T\\
A=N^TP\left[
\begin{matrix}
 \eta_1      \\
 &   \eta_2\\
  &  & \ddots & \\
 & & & \eta_{n-1}     \\
 & & & & a_{11}-\frac{b_1^2}{\eta_1}-\frac{b_2^2}{\eta_2}-...-\frac{b_{n-1}^2}{\eta_{n-1}}
\end{matrix}
\right]P^TN
\\\therefore \eta_1,..\eta_{n-1},a_{11}-\frac{b_1^2}{\eta_1}-\frac{b_2^2}{\eta_2}-...-\frac{b_{n-1}^2}{\eta_{n-1}}是A的特征值\\
不满足题意，证否
$$

$$
(2)定义A特征值函数f是向量值函数，其中A的自变量受题目条件限制\\
f(a_{ij})=( \eta_1,..\eta_{n-1},a_{11}-\frac{b_1^2}{\eta_1}-\frac{b_2^2}{\eta_2}-...-\frac{b_{n-1}^2}{\eta_{n-1}})\\
其中能变的只有最后一项a_{11}-\frac{b_1^2}{\eta_1}-\frac{b_2^2}{\eta_2}-...-\frac{b_{n-1}^2}{\eta_{n-1}}
\\ [b_1,b_2,b_3\cdots b_{n-1}]=C^T\\
关于M，M是特征向量组成的矩阵，且是正交矩阵\\
M_1=[x_1,x_2,...,x_n]^T\\
BM_1=\lambda M_1\Rightarrow
\left[ \begin{matrix}
m_{11}&m_{12}&\cdots&m_{1n}\\
m_{21}&\ddots\\
\vdots\\
m_{n1}
\end{matrix}\right ]
[x_1,x_2,...,x_n]^T=
\begin{cases}
(m_{11}-\eta_1 )x_1+m_{12}x_2+...+m_{1n}x_n=0\\
m_{21}x_1+(m_{22}-\eta_2) x_2+...+m_{2n}x_n=0\\
\vdots\\
m_{(n-1)1}x_1+m_{(n-1)2}x_2+...+(m_{(n-1)n}-\eta_n)x_n=0\\
x_1^2+x_2^2+x_3^2+...x_n^2=1
\end{cases}
$$

$$
设x_n=m\\
\begin{cases}
(m_{11}-\eta_1 )x_1+m_{12}x_2+...=-m_{1n}m\\
m_{21}x_1+(m_{22}-\eta_2) x_2+...=-m_{2n}m\\
\vdots\\
m_{(n-1)1}x_1+m_{(n-1)2}x_2+...=-(m_{(n-1)n}-\eta_n)m\\
\end{cases}
\\由克拉默法则，x_i=\frac{D_i}{D}=\frac{D_i'm}{D}\\
由于特征向量线性无关，|D|\neq0\\
于是x_i=\frac{x_i}{\sqrt{x_1^2+x_2^2+...x_n^2}}=\frac{D_i}{\sqrt{D_1^2+D_2^2+D_3^2+...D_n^2}},其中D_i都是m_{ij}的多项式\\
b_1=c_1x_1+c_2x_2+...
$$












$$
\sum^n_{i=1}\sqrt{(x_{1k}-x_{2k})^2}\leq \delta
$$
