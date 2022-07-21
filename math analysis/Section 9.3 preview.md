# Section 9.3 preview

## explicit function(显函数)

$$
y=f(x),z=f(x,y),y=f(\vec x)
$$

## implicit function(隐函数)

$$
F(x,y)=0,F(x,y,z)=0,x^2+y^2=1
$$

implicit function is a function which can’t confirm the relation of x and y in total

### def:

$$
F(x,y)=0\ D\sub \mathbb{R}^2\   \ \ \ function F(x,y)=0\ define\ a\ curve\
\\if\  \forall (x_0,y_0)\in D(F(x_0,y_0)=0)
\\I\times J\sub D,\forall x\in I \ has\ only \ a\ y\in J\ ,\ s.t.F(x,y)=0
\\so\ y=f(x)\ is\ called\ an\ implicit\ function\ determined\ in\ the\ neighborhood(x_0,y_0)
$$

y=f(x)

F(x,y)=0$\rightarrow$F(x,f(x))$\equiv$0

derivate it
$$
F'_x(x,f(x))+F_y'(x,f(x))f'(x)=0
\\\frac{dy}{dx}=-\frac{F_x'(x,y)}{F_y'(x,y)},(F(x,y)=0)
$$


## existence of implicit function 

**theory**:F(x,y) satisfy:

(1)$F(x_0,y_0)=0$

(2)$F(x,y)in\  D=B((x_0,y_0),\delta)\ is\ continous\ and \ have\ contiuous\ partial\ dericatives$

(3)$F_y'(x_,y_0)\neq0$

then exists a rectangle area(a,b)$\times$(c,d)$\subseteq$D,s.t.$\forall x\in(a,b)$function F(x,y)=0 have **only a solution** ,which satisfy $y_0=f(x_0)$

and $y=f(y)$ is contiuous 

also 
$$
\frac{dy}{dx}=f'(x)=-\frac{F'_x(x,y)}{F'_y(x,y)}
$$

**prove**

> since $F_y'(x,y) \neq0$suppose that $F_y'(x,y)>$0,refer to the continuous of $F_y'(x,y)$,exist a neighborhood [a’,b’]$\times$[c,d] which centered on $(x_0, y_0)$.
>
> refer to the Local sign preservation of continuous functions $F_y'(x,y)>$0,for $\forall$(x,y)$\in$[a’,b’]$\times$[c,d].
>
> for $x_0 \in [a',b']$,$F(x_0,y)$ is strictly increasing.
>
> so for $x_0\in[a',b'],F(x_0,c)<F(x_0,y_0)=0<F(x_0,d)$,$x\in [a',b']$
>
> refer to the continuity about x
>
> then $ $F(x,c)<0<F(x,d),x $\in$ [a,b]

## derivablity of implicit function