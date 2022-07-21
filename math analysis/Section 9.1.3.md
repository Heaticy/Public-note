# Section 9.2 Differential of Multi-Function

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
Pf: \exists M>0,s.t.|\frac{df}{dx}|,|\frac{df}{dy}|\leq M\ on\ D\\
|f(x_0+h,y_0+k)-f(x_0,y_0)|\leq|f(x_0+h,y_0+k)-f(x_0,h)|+|f(x_0+h,y_0)-f(x_0.y_0)|
$$

**refer to Lag MAT**:

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