# quiz 4

## 李超凡，2021531045

（下面的过程都是markdown代码纯手敲的，有源代码，无抄袭嫌疑）

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
(2)证明：定义A特征值函数f是向量值函数，其中A的自变量受题目条件限制\\
f(a_{ij})=( \eta_1,..\eta_{n-1},a_{11}-\frac{b_1^2}{\eta_1}-\frac{b_2^2}{\eta_2}-...-\frac{b_{n-1}^2}{\eta_{n-1}})\\
其中能变的只有最后一项a_{11}-\frac{b_1^2}{\eta_1}-\frac{b_2^2}{\eta_2}-...-\frac{b_{n-1}^2}{\eta_{n-1}}
\\ [b_1,b_2,b_3\cdots b_{n-1}]=C^T=[a_{12},a_{13},....a_{1n}]
$$

$$
因此向量值函数f(a_{ij})的前n-1项都是常数\eta_1,..\eta_{n-1}
\\
第n项等于\displaystyle \eta_n =a_{11}-\frac{a_{12}^2}{\eta_1}-\frac{a_{13}^2}{\eta_2}-...-\frac{a_{1n}^2}{\eta_{n-1}}
\\f(a_{ij})=( \eta_1,..\eta_{n-1},a_{11}-\frac{a_{12}^2}{\eta_1}-\frac{a_{13}^2}{\eta_2}-...-\frac{a_{1n}^2}{\eta_{n-1}})\\
\frac{\part f}{\part a_{11}}=[0,0,0....0,1]以及\frac{\part f}{\part a_{ij}}=[0,0,0...,0]显然连续\ \ \ \ \ \ \ \ \ (i,j)\geq2\\
例如\frac{\part f}{\part a_{12}}=[0,0,0....0,\frac{2a_{12}}{\eta _1}]\\
设向量中元素为n_i
\\对\forall \varepsilon>0\\
\sum^n_{i=1}\sqrt{(n_{i}-n'_{i})^2}=\sqrt{(n_{n}-n'_{n})^2}=\sqrt{(\frac{2(a_{12}-{a'}_{12})}{\eta_1})^2}<\varepsilon\\
\Longrightarrow \sqrt{(a_{12}-a'_{12})^2}<\frac{\eta_1}{2}\varepsilon
\\
存在一个度量\sum^n_{i=1,j=1}\sqrt{(a_{ij}-a'_{ij})^2}\leq \frac {min\{\eta_1,\eta_2,....\eta_{n-1}\}\varepsilon}{2}时\\
s.t.\sum^n_{i=1}\sqrt{(n_{i}-n'_{i})^2}<\varepsilon\\
$$


$$
\frac{\part f}{\part a_{1n}}=[0,0,0....0,\frac{2a_{1n}}{\eta _n}]是连续的\\
同理
\frac{\part f}{\part a_{n1}}是连续的\\
证得\frac{\part f}{\part a_{ij}}都是连续的(i,j=1,2,3...,n)\\
所以在A的一个小邻域内，向量值函数f是连续可微的
$$







