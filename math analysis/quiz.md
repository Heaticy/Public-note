![image-20220610115101801](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220610115101801.png)

$$
2\pi
$$


![image-20220610115035612](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220610115035612.png)
$\frac{44\pi}{3}$

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220610112945919.png" alt="image-20220610112945919" style="zoom:80%;" />
解:

$$
\nabla\times\vec{F}=0\\
\varphi=xyz\\
拉格朗日乘数法\Rightarrow(\frac{a}{\sqrt{3}},\frac{b}{\sqrt{3}},\frac{a}{\sqrt{3}})
$$

![image-20220610112828152](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220610112828152.png)

解:(1)
$$
|S_n(x)-f(x)|=\sum^{\infty}_{k=n}\frac{ksinkx}{2^{\frac{k}{2}}}<\sum^{\infty}_{k=n}\frac{k|sinkx|}{2^{\frac{k}{2}}}\\
其中\sum^{\infty}_{k=1}\frac{k|sinkx|}{2^{\frac{k}{2}}}\leq\sum^{\infty}_{k=n}\frac{k}{2^{\frac{k}{2}}}\\
由威尔斯特拉斯定理\sum^{\infty}_{k=n}\frac{k|sinkx|}{2^{\frac{k}{2}}}收敛\\
由cauchy收敛准则n\geq N时\sum^{\infty}_{k=n}\frac{k|sinkx|}{2^{\frac{k}{2}}}<\varepsilon\\
\Rightarrow \sum^{n+p}_{k=n}\frac{ksinkx}{2^{\frac{k}{2}}}<\varepsilon
\\所以S_n在R上一致收敛于f_n
$$
 (2)
$$
\sum^{\infty}_{n=1}\frac{nsinnx}{2^{\frac{n}{2}}}\\
F(x)=-\sum^{\infty}_{n=1}\frac{cosnx}{2^{\frac{n}{2}}}\\
=-Re\{\sum^\infty_{n=1}(\frac{e^{ix}}{\sqrt{2}})^n\}=-Re\{\frac{\frac{e^{ix}}{2}}{1-\frac{e^{ix}}{\sqrt{2}}}\}=-Re\{\frac{cosx+isinx}{\sqrt{2}-cosx-isinx}\}\\
=\frac{\sqrt{2}cosx-1}{3-2\sqrt{2}cosx}\\
f=F'=\frac{-5\sqrt{2}sinx}{(3-2\sqrt{2}cosx)^2}\\
x=\frac{-\pi}{4}时,f=5\geq \sqrt{3}
$$

![image-20220610115126273](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220610115126273.png)

解:(1)略略略
$$
(2)1.f'(x)=\sum^\infty_{n=1}\frac{sinncosnx}{n}\\
f'(0)=\sum^\infty_{n=1}\frac{sinn}{n}=\frac{\pi-1}{2}\\
2.\sum^\infty_{n=1}b_n^2=\int^\pi_{-\pi}f^2(x)dx


$$



![image-20220610115134331](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220610115134331.png)


解:
$$
|F(\Delta t)-F(0)|=|\int ^1_0\frac{\Delta tf(x)}{x^2+\Delta t^2}dx-0|\\
=|\int^{\Delta t}_0\frac{\Delta tf(x)}{x^2+\Delta t^2}dx+\int^{1}_{\Delta t}\frac{\Delta tf(x)}{x^2+\Delta t^2}dx|\\
1\degree f(0)\neq0时,不妨设f(0)>0,\forall \varepsilon>0,\exist\delta>0.s.t|x-\delta|<0f(x)>\varepsilon\\
\int^{\Delta t}_0\frac{\Delta tf(x)}{x^2+\Delta t^2}dx\geq\int^{\Delta t}_0\frac{\Delta t\varepsilon}{x^2+\Delta t^2}dx=\varepsilon arctan\frac{x}{\Delta t}\bigg|^{\Delta t}_0=\varepsilon arctan1\\
|\int^{1}_{\Delta t}\frac{\Delta tf(x)}{x^2+\Delta t^2}dx|\leq
|\int^{1}_{\Delta t}\frac{\Delta tf(x)}{x^2+\Delta t^2}dx|\leq
\int^{1}_{\Delta t}|\frac{\Delta tf(x)}{x^2}|dx\\
在[\Delta t,1]上
\frac{f(x)}{x^2}有最大值M\\
\Rightarrow|\int^{1}_{\Delta t}\frac{\Delta tf(x)}{x^2}dx|\leq\Delta tM\\

当\Delta t<\frac\varepsilon{2M}\arctan1时\\
|\int^{1}_{\Delta t}\frac{\Delta tf(x)}{x^2+\Delta t^2}dx|<
\frac{1}{2}\varepsilon arctan1\Rightarrow
\int^{1}_{\Delta t}\frac{\Delta tf(x)}{x^2+\Delta t^2}dx>-\frac{1}{2}\varepsilon arctan1\\
|F(\Delta t)-F(0)|=|\int^{\Delta t}_0\frac{\Delta tf(x)}{x^2+\Delta t^2}dx+\int^{1}_{\Delta t}\frac{\Delta tf(x)}{x^2+\Delta t^2}dx|>\frac{1}{2}\varepsilon\arctan1\\
因此此时\lim_{\Delta t\rightarrow0}F(\Delta t)-f(0)\neq0 即在t=0处不连续\\
2\degree f(0)=0时,\forall \varepsilon>0,\exist\delta>0.s.t|x-\delta|<0f(x)<\varepsilon\\

\int^{\Delta t}_0\frac{\Delta tf(x)}{x^2+\Delta t^2}dx\leq\varepsilon arctan1\\
\int^{1}_{\Delta t}\frac{\Delta tf(x)}{x^2+\Delta t^2}dx<\frac{1}{2}\varepsilon arctan1\\
|F(\Delta t)-F(0)|=|\int^{\Delta t}_0\frac{\Delta tf(x)}{x^2+\Delta t^2}dx+\int^{1}_{\Delta t}\frac{\Delta tf(x)}{x^2+\Delta t^2}dx|<\frac{3}{2}\varepsilon\arctan1\\
因此此时在t=0处连续
$$



![image-20220610115146425](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220610115146425.png)

解:
$$
\int^{\infty}_a f(x)dx\\
导函数不一定连续,分部积分定理失效\\
但是f'(x)可积手动,证明分部积分\\
(xf(x))'=f(x)+xf'(x)\\
xf'(x)可积\\
\int^\infty_af'(x)dx=\int^\infty_af(x)dx+\int^\infty_axf'(x)dx
\\
\int^{\infty}_a f(x)dx=xf(x)\bigg|_a^{\infty}-\int^{\infty}_axf'(x)dx\\
下面证明\lim_{x\rightarrow \infty}xf(x)收敛\\
\\
\lim_{x\rightarrow 0}xf(x)=2f(x)\int^x_\frac{x}{2}dt\leq2\int^x_\frac{x}{2}f(t)dt\xlongequal{cauchy收敛准则}0
$$



![image-20220610115153038](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220610115153038.png)

解:
$$
x\rightarrow 0时\\
\frac{g^2(x)}{x^2}\xlongequal{洛必达}\frac{2g(x)f(x)}{2x}=\frac{2g(x)}{2x}f(0)\xlongequal{洛必达}\frac{f(x)}{1}f(0)=f^2(0)




\\
x\rightarrow \infty时
\\
f(x)在[0,+\infty)上平方可积\Rightarrow f(x)在[0,+\infty)上可积\\
\int^{x}_0f(t)dt\leq\int^{+\infty}_0f(t)dt\leq M\Rightarrow g(x)\leq M\\
\frac{1}{x^2}单调趋于0\\
由Dirichlet判别法可知\int^\infty_0\frac{g^2(x)}{x^2}dx收敛\\

\int^\infty_0 \frac{g^2(x)}{x^2}dx\xlongequal{分部积分}-g^2(x)\frac{1}{x}\bigg|_0^{\infty}+\int^\infty_02g(x)\frac{1}{x}g'(x)dx\\
g^2(x)\leq M^2,g'(x)=f(x)\Rightarrow\\
\int^\infty_0 \frac{g^2(x)}{x^2}dx=\int^\infty_0\frac{g(x)}{x}2f(x)dx\\
由柯西施瓦茨定理:|\lang x,y\rang|^2\leq\lang x,x\rang\cdot\lang y,y\rang\\
(\int^\infty_0 \frac{g^2(x)}{x^2}dx)^2=(\int^\infty_0\frac{g(x)}{x}2f(x)dx)^2\leq\int^\infty_0 \frac{g^2(x)}{x^2}dx\int^\infty_0 4f(x)^2dx\\
\int^\infty_0\frac{g^2(x)}{x}dx\leq4\int^\infty_0f(x)^2dx
$$