![image-20220520125809933](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220520125809933.png)
$$
证明:由斯托克斯公式I=\iint_S(-1-1)dydz+(-1-1)dzdx+(-1-1)dxdy\\
S对应的单位法向量(-\frac{\sqrt3}{3},-\frac{\sqrt3}{3},-\frac{\sqrt3}{3})\\
=\iint_S2\sqrt 3d\sigma\\
S是x^2+y^2+z^2=a^2在平面x+y+z=0上的截面\\
即I=2S=2\sqrt 3\pi a^2
$$
![image-20220520125837278](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220520125837278.png)
$$
证明:由高斯定理I=\iiint_V(\frac{\part P}{\part x}+\frac{\part Q}{\part y}+\frac{\part R}{\part z})dxdydz-\iint_{S1}\frac{zdxdy}{(x^2+y^2+z^2)^{\frac32}}\\-\iint_{S_2}\frac{rsin\theta cos\varphi dydz+rsin\theta sin\varphi dzdx+rcos\theta dxdy}{r^{3}} S_2是原点附近的一个以r为球心的半球面,方向向内\\
=0-0+\iint (sin^3\theta cos^2\varphi+sin^3\theta sin^2\varphi+cos^2\theta sin\theta)drd\theta\\
=\int^\frac{\pi}2_0d\theta\int^{2\pi}_0 sin\theta d\varphi=2\pi
$$
