# Section 9.1.2 Multivariate Function

[TOC]

## Multivariate Function

### Definition

#### Def (Multivariate Function)

$$
f :D(\subseteq \mathbb{R}^n) \rightarrow \mathbb{R}
$$

is a function defined on $D$ .

It is called **multivariate function** ( with $n$ variables )

#### Other Form

It can be written as :
$$
z = f(x_1,x_2,\cdots,x_n)
$$
in cartesian coordinate.

### Two ways of representaion

#### (1) Graph representation

$$
S = \{(x_1,x_2,\cdots,x_n,f(x_1,\cdots,x_n))|(x_1,\cdots,x_n)\in D\}
$$

#### (2) Level set representation（水平集）

$\forall c \in \mathbb{R}$ , $f^{-1}(c) = \{(x_1,x_2,\cdots,x_n)\in D|f(x_1,\cdots,x_n) = c\}$

e.g.1 等温线，等高线......

e.g.2
$$
z = x^2+y^2,(x,y) \in \mathbb{R}
$$
Graph representation :

<img src="https://cdn.jsdelivr.net/gh/HypoxanthineOvO/Picture/202203031045150.png" alt="8C3141F5E0F7F5CCC92172578A0F6B0F" style="zoom:33%;" />

Level Set representation :

<img src="https://cdn.jsdelivr.net/gh/HypoxanthineOvO/Picture/202203031045778.png" alt="976D8C24816BB9FED37EC0893971CACF" style="zoom:33%;" />

### Vector-Valued Function

#### Definition

$$
f:D(\subseteq\mathbb{R}^n)\rightarrow \mathbb{R}^m\\
(x_1,x_2,\cdots,x_n) \mapsto (y_1,\cdots,y_m) = (f_1(x_1,\cdots,x_n),\cdots,f_m(x_1,\cdots,x_n))
$$

Denoted : 
$$
\vec{y} = \vec{f}(\vec{x})
$$

#### Def (Coordinate transformation)

$n = m$ , If $\vec{f}$ is one-to-one , then it's called a **coordinate transformation**.

e.g. 
$$
\mathbb{R}^2 \backslash [0,+\infty) \rightarrow (0,+\infty)\times (0,2\pi)\\
(x,y) \mapsto (r = \sqrt{x^2+y^2},\theta = \arctan \frac{y}{x})
$$


#### Composition of vector-valued finction

$$
f:D(\subseteq \mathbb{R}^n)\rightarrow \mathbb{R}^m\\
g : U(\subseteq \mathbb{R}^m) \rightarrow \mathbb{R}^k\\
f(D)\subseteq U\rightarrow \vec{g}\circ\vec{f}(\vec{x}) = \vec{g}(\vec{f}(\vec{x}))
$$



## Limit And Continuity

### Limit

#### Def (Limit)

##### 01

Let $f:D(\subseteq\mathbb{R}^2)\rightarrow \mathbb{R}$ , $M_0 \in \mathbb{R}^2$ is an accum. point of $D$ .

If for some $a \in\mathbb{R}$ , $\forall \varepsilon > 0,\exists \delta = \delta(\varepsilon ) > 0$ , s.t.$\forall M \in B_-(M_0,\delta)\cap D$
$$
|f(M)-A| < \varepsilon
$$
$\Leftrightarrow$

##### 02

$\forall \varepsilon > 0,\exists \delta = \delta(\varepsilon) > 0$ , s.t. $\forall M = (x,y) \in D$  with :

$(x,y)\neq (x_0,y_0)$ and $|x-x_0|<\delta,|y-y_0|<\delta$ , we have :
$$
|f(x,y) - a | < \varepsilon
$$

#### Denotation

Denoted by :
$$
\lim_{M\rightarrow M_0}f(M)\\
\lim_{x\rightarrow x_0,y\rightarrow y_0} f(x,y)\\
\lim_{\triangle x\rightarrow 0,\triangle y\rightarrow 0}f(x_0+\triangle x,y_0+\triangle y)\\
$$
But :

Don't write it as :
$$
\lim_{x\rightarrow x_0}\lim_{y\rightarrow y_0} f(x,y)
$$
**e.g.1**

Prove that $\displaystyle \lim_{(x,y)\rightarrow (0,0)} \frac{x^2y^2}{x^4+y^2} = 0$

Proof :
$$
|\frac{x^2y^2}{x^4+y^2}| = \frac{x^2|y|}{x^4+y^2}|y|\leq\frac{1}{2}|y| < \varepsilon
$$
$\forall \varepsilon > 0$ , for $\delta = 2\varepsilon$ , $\forall(x,y)\neq (0,0),|x|<\delta,|y|<\delta$

$|f(x,y)<\varepsilon$

So $\displaystyle \lim_{(x,y)\rightarrow (0,0)}f(x,y) = 0$

**e.g.2**

$\displaystyle \lim_{(x,y)\rightarrow (0,0)}\frac{x^3+y^3}{x^2+y^2}$

Proof :
$$
|\frac{x^3+y^3}{x^2+y^2}| < |x|+|y|\\
$$
$\forall \varepsilon > 0$ , for $\delta = \frac12\varepsilon$ , $\forall (x,y)\neq(0,0),|x|<\delta,|y|<\delta,|f(x,y|<|x|+|y|<2\delta = \varepsilon)$ .



#### Theorem (Algebric Operations)

Algebric Operations preserved the limit.

> 对四则运算都成立

#### Theorem (Heine Principle)

Suppose $M_0$ is an accumulation point of $D$ , $f(D(\subseteq\mathbb{R}^2))\rightarrow\mathbb{R}$ , then :
$$
\lim_{M\rightarrow M_0} f(M) = a 
\Leftrightarrow
\forall \{M_n\}_{n = 1,2,\ldots}\subseteq D,M_n\rightarrow M_0(n\rightarrow \infty)\\
\text{We have }\lim_{n\rightarrow\infty}f(M_n) = a
$$


#### Theorem

Suppose $f$ is defined in a punctured neighborhood $B_-(M_0,r)$ of $M_0$ .

$\forall$ continuous curve $\gamma:[0,\delta)\rightarrow B(M_0,r)$ 

with $\gamma(0) = M_0$ and $\gamma((0,\delta))\subseteq B_-(M_0,r)$ , $\displaystyle \lim_{t\rightarrow 0^+}f(\gamma(t)) = a\Leftrightarrow \lim_{M\rightarrow M_0}f(M) = a$.

#### Limit of vector-valued function

$$
\lim_{\vec{x}\rightarrow \vec{x_0}}\vec{f}(\vec{x}) = \vec{a}
\Leftrightarrow
\forall \varepsilon > 0,\exists \delta = \delta(\varepsilon) > 0,s.t.\;\forall \vec{x}\in D\\
0 < |\vec{x}-\vec{x_0}| < \delta\;,\;\rho(\vec{f}(\vec{x}),\vec{a})<\varepsilon
$$

e.g.

![126C0343CD5A92D3BB7597703391D0CA](https://cdn.jsdelivr.net/gh/HypoxanthineOvO/Picture/202203031150375.png)



### Continuity

#### Def ( Continuity )

Let $f :D(\subseteq \mathbb{R}^2)\rightarrow \mathbb{R}$ , $M_0\in D$ .

We say $f$ is continuous at $M_0$ of $\forall \varepsilon > 0,\exists \delta = \delta(\varepsilon) > 0$ :

s.t. $\forall M \in D\cap B(M,\delta)$ , $f(M)-f(M_0) < \varepsilon$

It equal to $\displaystyle \lim_{M\rightarrow M_0}f(M)=f(M_0)$

**e.g.**
$$
f(x,y) = 
\begin{cases} 
\displaystyle \frac{2xy}{x^2+y^2}&(x,y)\neq (0,0)\\
0 & (x,y) = (0,0)
\end{cases}
$$
Since we have proved $\displaystyle \lim_{(x,y)\rightarrow(0,0)}f(x,y)$ does not exist

$\Rightarrow$ $f$ is not continuous at $(0,0)$ 

For $(x_0,y_0)\neq (0,0)$ , $\displaystyle \lim_{(x,y)\rightarrow(x_0,y_0)}\frac{2xy}{x^2+y^2} = \frac{2x_0y_0}{x_0^2+y_0^2} = f(x_0,y_0)$ 

$\Rightarrow$ $f$ is continuous at $(x_0,y_0)$

Another form :
$$
\lim_{\delta\rightarrow 0}\sup_{D\cap B(M,\delta)} |f(M)-f(M_0)| = 0
$$
**e.g.**

Define : 
$$
f(x,y) = 
\begin{cases}
\log(1+xy)^{\frac{1}{xy}},&xy\neq 0\\
1 ,& xy=0
\end{cases}
$$
Study the continuity at $(0,0)$

**Sol :**

Since
$$
\begin{gather}
\lim_{u\rightarrow 1}\log(1+u)^\frac{1}{u} = 1\\
\forall \varepsilon > 0,\exists \delta' = \delta'(\varepsilon) > 0,\text{ s.t. }:\\  
\forall 0 < |u| < \delta',|\log(1+u)^\frac1u -1| < \varepsilon
\end{gather}
$$
Take $\delta = \min\{1,\delta'\}$ , then $\forall |x|,|y| < \delta$ :

$|u| = |xy| < \delta^2 < \delta'$

So : $|\log(1+xy)^\frac{1}{xy}-1| < \varepsilon$

So : $f$ is continuous at $(0,0)$

> 实际上考虑了复合函数：
>
> $f(x,y) = \phi(u),u(x,y) = xy$ :
>
> $u$ is continuous at $u(0,y_0)$



#### Def ( Uniform Continuity )

Let $f$ be defined on $D \subseteq \mathbb{R}^2$ .

$f$ is called uniformly continuous on $D$ if $\forall \varepsilon > 0,\exists \delta = \delta(\varepsilon) > 0$ s.t. :

 $\forall M,M' \in D$ , $\rho(M,M') < \delta$ , we have $|f(M)-f(M')| < \varepsilon$



#### Theorems

1. The continuity is preserved under $+,-,\times$ , and it is preserved for "$/$" if the denominator is not zero.

2. The composition of continuous vector-valued functions is continuous.

   i.e.  if $(x_0,\cdots,x_n)\rightarrow (y_1,\cdots ,y_m)$

   and $(y_1,\cdots,y_m)\rightarrow (z_1,\cdots,z_k)$ are all continuous 

   the $(x_1,\cdots,x_n)\rightarrow (z_1,\cdots,z_k)$

3. ( Intermediate Value Property) 

   Let $f$ be defined on a connected set $D\subseteq \mathbb{R}^2$ and $f$ is continuous on $D$ 

   then : $\forall M_1,M_2 \in D$ , all values between $f(M_1),f(M_2)$ can be achieved.

   More generally , the image of any continuous function connected set is connected.

   > 连通性在连续映射下是保持的

   **Proof**

   Argue by contradiction.

   Suppose $f(D)$ is not connected,

   then $f(D) = E_1 \cup E_2,E_1,E_2 \neq \varnothing,E_1 \cap \bar{E_2} = \varnothing,\bar{E_1}\cap E_2 = \varnothing$ .

   $\Rightarrow D = f^{-1}(E_1)\cup f^{-1}(E_2)\quad f^{-1}(E_1),f^{-1}(E_2) \neq \varnothing$ .

   Let $M_n \in f^{-1}(E_a)$ be a sequence of distinct points s.t $M_n\rightarrow M_{\infty} \in D$

   Then : $f(M_n)\rightarrow f(M_\infty)$ .

   If $f(M_\infty)\not\in E_1\Rightarrow f(M_{\infty})\in E_2$ , and is an accumulation point of $E_1$ 

   Contradiction with $E_2 \cap \bar{E_1} \neq \varnothing\Rightarrow f(M_\infty)\in f^{-1}(E_1)$

   Since $f^{-1}(E_1)$ does not contain any accum. point of $f^{-1}(E_2)$ :

   Contradiction. 

   **e.g.**

   Define a function on $\mathbb{R}^2\backslash\{(0,0)\}$ .

   ![EE19DC33CBF27220306519C701A9157F](https://cdn.jsdelivr.net/gh/HypoxanthineOvO/Picture/202203081038080.png)
   $$
   \theta(x,y) = 
   \begin{cases}
   \arctan \frac{y}{x}&x>0,y\geq 0\\
   \frac{\pi}{2}&x = 0,y > 0\\
   \arctan\frac{y}{x} + \pi & x < 0,y \geq 0\\
   \arctan\frac{y}{x} + \pi & x < 0,y < 0\\
   \frac{3\pi}{2}&x = 0,y < 0\\
   \arctan\frac{y}{x}+2\pi&x > 0,y < 0
   \end{cases}
   $$
   Near to the ray $x = 0$ :

   The function is not continuous.

   

4. The maximum and minimum of continuous function on a bounded closed set can be achieved.

5. ( Canter Thm ) Continuous function on bounded closed set is uniformly continuous.
