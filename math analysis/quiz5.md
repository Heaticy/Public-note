![image-20220513214957745](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220513214957745.png)

$$
证否:\iint_{a\leq x\leq b,a\leq y\leq b}e^{f(x)-f(y)}dxdy=\iint_{a\leq x\leq b,a\leq y\leq b}e^{f(y)-f(x)}dxdy\\
\Rightarrow左边=\frac12\iint_{a\leq x\leq b,a\leq y\leq b}(e^{f(x)-f(y)}+e^{f(y)-f(x)})dxdy\\
\geq\iint_{a\leq x\leq b,a\leq y\leq b}dxdy=(b-a)^2=右边\\
即证

$$


![image-20220513220312994](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220513220312994.png)

$$
y=rsin\theta sin\varphi\\
z=rcos\theta\\
\iiint_\Omega((sin\theta cos\varphi+sin\theta sin\varphi-\cos\theta)r+10)r^2sin\theta drd\theta d\varphi\\
\int^{\sqrt3}_0dr\int^\pi_0d\theta\int^{2\pi}_0((sin\theta cos\varphi+sin\theta sin\varphi-\cos\theta)r+10)r^2sin\theta d\varphi\\
=2\pi\int^{\sqrt3}_0dr\int^\pi_0d\theta (-sin\theta cos\theta r+10sin\theta)r^2drd\theta \\
=40\pi \int^{\sqrt{3}}_0r^2dr=\frac{40}{3}\pi3\sqrt3=40\sqrt3\pi
满足题意\\即证

$$