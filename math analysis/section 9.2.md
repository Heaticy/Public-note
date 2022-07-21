# Section 9.2 Differential of Multi-Function

[TOC]



- $n = 1$ :
  $$
  f'(x) = \lim_{\triangle x\rightarrow 0}\frac{\triangle y}{\triangle x}
  $$

- $n = 2$ :

  How to make sense $\displaystyle \frac{\triangle f}{\triangle M}$ ?

  > 有很多种方式：偏导数、微分等，是一元导数在不同角度上的拓展。



## Partial Derivatives

### Deinition of Partial Derivatives

#### Def (Partial Defivatives)

Suppose $z = f(x,y)$ is defined in nbhd of $M_0 = (x_0,y_0)$ .

If $f(x,y_0)$ has derivative at $x_0$ :

then we say $f$ has partial derivative with respect to $x$ at $(x_0,y_0)$ . 

This derivative is denoted bt $\displaystyle \frac{\partial f}{\partial x}(x,y_0)$ . 

i.e.
$$
\frac{\partial f}{\partial x}(x_0,y_0) =
\frac{\text{d}}{\text{d}x}\bigg|_{x = x_0}f(x,y_0)
$$
  Similarly , we can define
$$
\frac{\partial f}{\partial y}(x_0,y_0) = 
\frac{\text{d}}{\text{d}y}\bigg|_{y = y_0}f(x_0,y)
$$

#### Geometric  Meaning :

![FF2CE85EEAC14B0B5E4BD01A8B98D418](https://cdn.jsdelivr.net/gh/HypoxanthineOvO/Picture/202203081059224.jpg)



#### Properties

$$
\begin{cases}
\displaystyle \frac{\partial}{\partial x}(f \cdot g) = \frac{\partial f}{\partial x} g + f\frac{\partial g}{\partial x}\\
\displaystyle \frac{\partial}{\partial x}(f \pm g) = \frac{\partial f}{\partial x}\pm \frac{\partial g}{\partial x}
\end{cases}
$$



**e.g.**
$$
f(x,y) = 
\begin{cases}
\displaystyle \frac{2xy}{x^2+y^2} & (x,y)\neq (0,0)\\
0 & (x,y) = (0,0)
\end{cases}
$$
**Sol.**

At $(x,y)\neq (0,0)$ , the first order partial derivatives both exist :
$$
\frac{\partial f}{\partial x} = \frac{2y(x^2+y^2)-2x\cdot 2xy}{(x^2+y^2)^2} = \frac{2y(y^2-x^2)}{(x^2+y^2)^2}
$$

$$
\frac{\partial f}{\partial y} = \frac{2x(x^2-y^2)}{(x^2+y^2)^2}
$$

At $(0,0)$ :
$$
\frac{\partial f}{\partial x} (0,0) = \frac{\text{d}}{\text{d}x} \bigg|_{x=0}f(x,0) = 0
$$

$$
\frac{\partial f}{\partial y}(0,0) = 0
$$

**BUT** $f$ **IS NOT CONTINUOUS AT** $(0,0)$



### High order partial derivatives

#### Def

Suppose $\displaystyle \frac{\partial f}{\partial x}$ is defined in a nbhd of $M_0$ .

- If $\displaystyle \frac{\partial}{\partial x}(\frac{\partial f}{\partial x})$ exists at $M_0$  :

	then we call it the second order partal derivative of $f$ with $x$ .

- If $\displaystyle \frac{\partial}{\partial y}(\frac{\partial f}{\partial x})$ exist at $M_0$ .

	then we call it the mixed second partial derivative of $f$ w.r.t $x \& y$ at $M_0$

- Similarlly we can defined $\displaystyle \frac{\partial}{\partial x}(\frac{\partial f}{\partial y})$ and $\displaystyle \frac{\partial}{\partial y}(\frac{\partial f}{\partial y})$ .



In gerneral , we can define :
$$
\frac{\partial }{\partial x} ( \cdots (\frac{\partial f}{\partial x})\cdots) \triangleq \frac{\partial^k f}{\partial x_1 \cdots \partial x_k}
$$


#### Example of High order partial derivatives

##### Second order partial derivatives


$$
\frac{\partial^2 f}{\partial x^2} = 
\lim_{h\rightarrow 0}\frac{ \frac{\partial f}{\partial x}(x_0+h,y_0)- \frac{\partial f}{\partial x}(x_0,y_0)}{h}\\
= \lim_{h\rightarrow 0} \frac{1}{h} \lim_{k\rightarrow 0}(\frac{f(x_0 + h + k,y_0)-f(x_0 + h,y+0)}{k} = \frac{f(x_0 + k,y_0) - f(x_0,y_0)}{k})\\
= \lim_{h\rightarrow 0}\lim_{k\rightarrow 0} \frac{f(x_0 + h + k,y_0)-f(x_0 + h,y_0) - f(x_0 + k,y_0)+f(x_0,y_0)}{h\cdot k}\\
\frac{\partial^2 f}{\partial x^2}(x_0,y_0) = \frac{\text{d}^2}{\text{d} x^2} \bigg |_{x = x_0}f(x,y_0)
$$


##### Mixed second partial derivatives

$$
\frac{\partial^2 f}{\partial y \partial x} = \frac{\text{d}^2}{\text{d} x^2} \bigg |_{x = x_0}f(x,y_0)\\
= \lim_{k\rightarrow 0} \frac{1}{k} \lim_{h\rightarrow 0}(\frac{1}{h})(f(x_0 + h,y_0 + k)-f(x_0 ,y_0 + k)- f(x_0 + h,y_0) + f(x_0,y_0))\\
= \lim_{h\rightarrow 0}\lim_{k\rightarrow 0} \frac{f(x_0 + h,y_0 + k)-f(x_0 + h,y_0) - f(x_0,y_0 + k)+f(x_0,y_0)}{h\cdot k}\\
$$

##### Question

In general : 
$$
\frac{\partial ^2 f}{\partial x\partial y} = \frac{\partial ^2 f}{\partial y \partial x} \quad \textbf{?}
$$
We have :
$$
\Pi(h,k) =\big( (f(x_0 + h,y_0 + k)-f(x_0 + h,y_0)\big )-\big(f(x_0,y_0 + k)-f(x_0,y_0)\big)\\
= \phi(x_0 + h)-\phi(x_0)\\
= \phi'(x_0 + \theta_1 h)h\\
= \big(\frac{\partial f}{\partial x}(x_0 + \theta_1 h,y_0 + k)-\frac{\partial f}{\partial x}(x_0 + \theta_1 h,y_0)\big)\\
=\frac{\partial ^ 2 f}{\partial y\partial x}(x_0 + \theta_1 h,y_0 + \eta_1 k)kh
$$
for some $\theta_1,\eta_1\in (0,1)$ .

Similarly , by writing 
$$
\Pi(h,k) = \big( f(x_0 + h,y_0 + k) - f(x,y_0 + k)\big)- \big(f(x_0 + h,y_0)-f(x_0,y_0)\big) 
\\= \psi(y_0 + k)
$$
We get $\displaystyle \Pi (h,k) = \frac{\partial^2 f}{\partial x \partial y}(x_0 + \theta_2 h,y_0 + \eta_2 k)hk$

In conclusion

#### Theorem

If $\displaystyle \frac{\partial f}{\partial x\partial y},\frac{\partial^2f}{\partial y \partial x}$ both exist in a nbhd of $M_0$ and they are continuous at $M_0$ 

then : $\displaystyle \frac{\partial f}{\partial x\partial y}(M_0)=\frac{\partial^2f}{\partial y \partial x}(M_0)$



 $$f(x,y)=\begin{cases}\frac{2xy}{x^2+y^2},(x,y)\ne(0,0)\\0,(x,y)=(0,0)\end{cases}$$
$$
\frac{df}{dx}(0,0)=\lim_{h\rightarrow 0}\frac{f(x,0)-f(0,0)}{x}=0
$$

$$
\frac{df}{dx}(x,y)=\frac{2y(x^4+4x^2y^2-y^4)}{(x^2+y^2)^2}
$$

$$
\frac{d^2f}{dx^2}(0,0)=\lim_{h\rightarrow 0}{\frac{df}{dx}(x,0)-\frac{df}{dx}(0.0)}=0
$$

$$
\frac{d^2f}{dy^2}(0,0)=2
$$

$$
\frac{d^2f}{dxdy}(0,0)=2
$$

## Differentiability & Differential

### Def (differentiable)

**Let f: D($\subseteq \mathbb{R}^n$) $\rightarrow\mathbb{R}$be a  multivariate function let $\vec x\in D$ If$\exists$a linear function $A_\vec{x}$ :$R^n\rightarrow R$**
$$
s.t. f(\vec x+\vec h)-f(\vec x)=A_\vec{x}(\vec h)+o(\vec {|h|})
$$
then we say f is differentiable at $\vec x，A_\vec x$ is called the differential of f at $\vec x$

so $f_i$ is differentiable, $df_i|_x$$\mathbb{R}^n\rightarrow \mathbb{R}$ is the differential 

In practice ,we also denote $df_i=dx_i$,i=1,2,·······,n

For a general differentiable function f,$df|_\vec x$$\mathbb{R}^n\rightarrow \mathbb{R}$ is a linear function

So $\exists a_1,a_2,·······，a_n\  s.t. df|(\vec h)=a_1h_1+a_2h_2+······a_nh_n$

we also denote it by $df|\vec x$

If f is differentiable at any $\vec x\in D$,then f is called differentiable on D

Now ,take $d_i$:$\mathbb{R^n\rightarrow R}$ then $\vec x=h_i$ this is a linear function on $\vec h$

$df|_x=a_1dx_1+a_2dx_2+······+a_ndx_n$(in the meaning of linear functions)

**Question: what are the $a_n's$**

Plugging in $\vec h=t\vec e_i$ to the condition of “differentiable”

f($\vec x+t\vec e_i - f(\vec x_)= A_\vec x(t\vec e_i)+o(|t\vec e_i|),|t|\rightarrow 0$

​                              $=t·A(\vec e_i)+o(|t|),|t|\rightarrow 0$,
$$
\lim_{t\rightarrow 0}\frac{f(\vec x+t\vec e_i-f(\vec x))}{t}=A_\vec x(\vec e_i)=df|_\vec x(\vec e_i)=a_i
$$

$$
\frac{df}{dx_i}(\vec x)\ exists,and\ a_i=\frac{df}{dx_i}(\vec x),i=1,2,3·······n
$$

## In conclusion:

Thm: If f is differentiable at $\vec x =(x_1.....x_n)\ then \frac{df}{dx}(\vec x),exists\ for\ all\ i=1,2,3,······n$ 

and $df|_\vec x=\frac{df}{dx_1}dx_1+……+\frac{df}{dx}(\vec x)dx_n$

Interpretation

If f(x,y) is differentiable at ($x_0,y_0$)
$$
f(x,y)=f(x_0.y_0)+f_x'(x_0,y_0)(x-x_0)+f_y'(x_0,y_0)(y-y_0)+o(\sqrt{(x-x_0)^2+(y-y_0)^2})k
$$

## Thm: Suppose $\frac{df}{dx},\frac{df}{dy}$ exist in the open domain D

$$
If \ \frac{df}{dx},\frac{df}{dx} are\ bounded\ on\ D, then\ f\ is\ continuous\ on\ D;\\
If \frac{df}{dx},\frac{df}{df}\ are\ continuous\ on\ D, then\ f\ is\ differentiable\ on D
$$

$$
Pf:(1) \exists M>0,s.t.|\frac{df}{dx}|,|\frac{df}{dy}|\leq M\ on\ D\\
|f(x_0+h,y_0+k)-f(x_0,y_0)|\leq|f(x_0+h,y_0+k)-f(x_0+h,y_0)|+|f(x_0+h,y_0)-f(x_0.y_0)|\\
refer\ to\  Lagrange\ MAT:|f(x_0+h,y_0+k)-f(x_0,y_0)|=|f_y'(x_0+h,y_0+\theta _1k)|\cdot k+|f_x'(x_0+\theta _2 h,y_0)|\cdot h\leq(k+h)M
\\so\ \forall \varepsilon>0  \exists k,h<\delta=\frac{\varepsilon}{2M},\ s.t.|f(x_0+h,y_0+k)-f(x_0,y_0)|<\varepsilon
$$

$$
Pf:(2)||f(x_0+h,y_0+k)-f(x_0,y_0)|\leq|f_y'(x_0+h,y_0+\theta _1k)|\cdot k+|f_x'(x_0+\theta _2 h,y_0)|\cdot h
\\\lim_{(h,k)\rightarrow (0,0)}|f_y'(x+h,y+\theta_1k)-f_y'(x,y)|=0
\\\lim_{(h,k)\rightarrow (0,0)}|f_x'(x+\theta _2h,y)-f_y'(x,y)|=0
\\\lim_{(h,k)\rightarrow (0,0)}\frac{|f(x_0+h,y_0+k)-f(x_0,y_0)-f_x'(x_0,y_0)h-f_y'(x_0,y_0)k|}{\sqrt{x^2+y^2}}=0
$$



## Def(Directional derivative)

$$
If \lim_{t\rightarrow 0}\frac{f(\vec x+t\vec{v})-f(\vec x)}{t}\ exists,we\ say\ f,has\ directional\ derivative\ in\ the\ direction\ of\  \vec c\ at\ \vec x,denote\ it\ by\ \frac{df}{d\vec{v}}
$$

If if is differentiable at $\vec x$ ,so $f(\vec x +t\vec v)=df|_\vec x(t\vec v)+o(|t\vec v|)$,|t$\vec v\ \rightarrow 0$)
$$
\lim_{t\rightarrow 0}\frac{f(\vec x +t\vec v)-f(\vec x)}{t}=df|_\vec x(\vec v)
$$

$$
\frac{df}{d\vec v}(\vec x)=df|_\vec x(\vec v)
$$

In particular $\frac{df}{d\vec e_i}=\frac{df}{dx_i}$is the partial derivative in the $x_i$ variable
$$
\frac{df}{d\vec v}(\vec x)=df|_\vec v =\frac{df}{dx_1}\vec v_1+····+\frac{df}{dx_n}·\vec v_n
$$


## Geometrical intepretation of gradient

$$
e.g f(x,y)=x^2+y^2
f\ is\ differentiable\ everywhere,and\ f(x,y)=\frac{df}{dx}\vec{i}+\frac{df}{dy}\vec j=2x\vec i+2y\vec j
$$

Now ,consider $\vec f:D(\subseteq \mathbb{R}^n\rightarrow \mathbb{R^m})$vector-valved function

If $\Delta\vec y=A_2(\Delta\vec x+o(|\Delta\vec x|))$

for some linear map: $A_\vec x=d\vec f|_x:\mathbb{R^n}\rightarrow\mathbb{R^m}$,then$\vec f$ said to be differentiable of $\vec f$at $\vec x $

 

Choose the Standard bases{$\vec e_1,·····\vec e_n\ of \mathbb R^n$ }

{$\vec y_1,·····\vec y_m\ of \mathbb R^m $}

#### Properties

If $f$ and $g$ are differentiable at $\vec{x}\in D$

1. $\forall \lambda,\mu \in \mathbb{R},\lambda f + \mu g$ is differentiable at $\vec{x}$ , and $\text{d} (\lambda f + \mu g)\bigg|_\vec{x} - \lambda_\cdot \text{d} f\bigg|_\vec{x} + \mu \text{d}g\bigg|_\vec{x}$ 
2. $fg$ is differentiable at $\vec{x}$ and $\text{d} (fg)\bigg|_\vec{x} = f(\vec{x})\text{d} g \bigg|_\vec{x} + g\vec{x} \text{d} f\bigg|_\vec{x}$
3. If $g\vec{x}\neq 0$ , the $\displaystyle \frac{f}{g}$ is diff. at $\vec{x}$ , and $\displaystyle \text{d}(\frac{f}{g})\bigg|_\vec{x} = \frac{\text{d} f \bigg|_\vec{x} g(\vec{x}) - f(\vec{x})\text{d} g \bigg|_\vec{x}}{g^2(\vec{x})}$

**Proof**

$$
\begin{aligned}
fg(\vec{x}+\vec{h})-fg(\vec{x})& = \big(f(\vec{x}+\vec{h})-f\vec{x}  \big)g(\vec{x}+\vec{h}) +f(\vec{x})(g(\vec{x}+\vec{h})-g(\vec{x}))\\
&= (o(\vec{h})+\text{d}f\bigg|_{\vec{x}}(\vec{h}))g(\vec{x}+\vec{h}) + f(\vec{x})(\text{d} g\bigg|_{\vec{x}} (\vec{h})+o(\vec{h}))
\\
&= \text{d}f\bigg|_{\vec{x}} (\vec{h})\big(g(\vec{x})+o(|\vec{h}|)\big) + f(\vec{x})\cdot \text{d}g\bigg|_{\vec{x}}+o(|\vec{h}|)
\end{aligned}
$$




Now , consider $\vec{f} : D(\subseteq \mathbb{R}^n)\rightarrow \mathbb{R}^m$ vector-value function

If 
$$
\triangle y = \mathcal{A}_{\vec{x}}(\triangle \vec{x})+o(|\triangle \vec{x}|),|\triangle x|\rightarrow 0
$$

for some linear map : $\mathcal{A}_{\vec{x}} :\mathbb{R}^n\rightarrow \mathbb{R}^m$ , then $\vec{f}$ is said to be differentiable at $\vec{x}$ , and $\mathcal{A}_{\vec{x}}=\text{d} \vec{f}\bigg|_{\vec{x}}$ is called the diffferential of $\vec{x}$ at $\vec{x}$ .



Choose the standard bases $\{\vec{e_1},\cdots,\vec{e_n}\}$ of $\mathbb{R}^n$ , $\{\vec{\epsilon_1},\cdots,\vec{\epsilon_m}\}$ of $\mathbb{R}^m$

Under them , suppose $\mathcal{A}_{\vec{x}}$ is represented by a $m\times n$ matrix $A_{\vec{x}}  = (a_{ij}),1\leq i \leq m,1 \leq j \leq n$

Then :
$$
\begin{gather}
\begin{pmatrix}
\triangle y_1 \\ \vdots \\ \triangle y_m
\end{pmatrix}
= \begin{pmatrix}
a_{11} & \cdots & a_{1m}\\
\vdots & & \vdots \\
a_{m1} & \cdots & a_{mn}
\end{pmatrix}
\begin{pmatrix}
\triangle x_1 \\ \vdots \\ \triangle x_n
\end{pmatrix}
+ o(|\triangle \vec{x}|) , |\triangle x|\rightarrow 0\\

\end{gather}
$$
Then:
$$
\triangle y_i = 
\begin{pmatrix}
a_{i1} & \cdots & a_{in}
\end{pmatrix}
\begin{pmatrix}
\triangle x_1 \\ \vdots \\ \triangle x_n
\end{pmatrix} + o(|\triangle x|)
$$
i.e. $y_i = y_i(x_1,x_2,\cdots x_n)$ is differentiable for all i.



$\text{d}\vec{f}\bigg|_{\vec{x}}$ is represented by

$$
J_{\vec{x}(\vec{f})} =:
\begin{pmatrix}
\displaystyle 
\frac{\partial f_1}{\partial x_1} & \cdots & \displaystyle\frac{\partial f_m}{\partial x_1}\\
 & \vdots & \\
 \displaystyle \frac{\partial f_m}{\partial x_1} & \cdots & \displaystyle \frac{\partial f_m}{\partial x_n}
\end{pmatrix}
$$

> Jacobian matrix , 雅可比矩阵

**Special case** :

 $n = m$ , $\det J_{\vec{x}}(\vec{f})$ is called Jacobian determinant.（Using in Integeration Thm）



#### Differential of composition function

$\vec{f}:D(\subseteq \mathbb{R}^n)\rightarrow \mathbb{R}^m$ , $\vec{g} : U(\subseteq \mathbb{R}^m)\rightarrow \mathbb{R}^k$ , $\vec{f}(D)\subseteq U$

Suppose : 

$\vec{f}$ is differentiable at $\vec{x}$ , i.e. $\vec{f}(\vec{x}+\vec{h}) = \vec{f}(\vec{x}) + \text{d} \vec{f}\bigg|_\vec{x}(\vec{h}) + o(|\vec{h}|),|\vec{h}|\rightarrow 0$ 

$\vec{g}$ is diff. at $\vec{y} = \vec{f}(\vec{x})$ , i.e. $\vec{g}(\vec{y} + \vec{l}) = \vec{g}(\vec{y}) + \text{d}\vec{g}\bigg|_\vec{y}(\vec{l}) + o(|\vec{l}|),|\vec{l}|\rightarrow 0$ 

Then :
$$
\begin{aligned}
\vec{g}\cdot\vec{f}(\vec{x}+\vec{h}) &= \vec{g}(\vec{y}) + \text{d}\vec{g}\bigg|_\vec{y}(\text{d}\vec{f}\bigg|_\vec{x} (\vec{h}) + o(|\vec{h}|)) + (\text{d}\vec{f}\bigg|_\vec{x}(\vec{h}) + o(|\vec{h}|))\\
&= \vec{g}(\vec{y}) + \text{d}\vec{g}\bigg|_\vec{y}(\text{d}\vec{f}\bigg|_\vec{x}(\vec{h})) + o(|\vec{h}|)\\
&= \vec{g}(\vec{y}) + \text{d}\vec{g}\bigg|_\vec{y} \circ \text{d}\vec{f}\bigg|_\vec{x}(\vec{h}) + o(|\vec{h}|),|\vec{h}|\rightarrow 0
\end{aligned}
$$
So : $\vec{g}\circ\vec{x}$ is differentiable at $\vec{x}$ , and $\text{d}(\vec{g}\circ \vec{f})\bigg|_\vec{x} = \text{d}g\bigg|_{\vec{y} = \vec{f}(\vec{x})} \circ \text{d}\vec{f}\bigg|_\vec{x}$

Q.E.D
