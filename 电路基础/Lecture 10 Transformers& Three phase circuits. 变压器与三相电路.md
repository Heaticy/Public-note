# Lecture 10 Transformers& Three phase circuits. 变压器与三相电路

## 1.Base knowledge

### (1)Plugs and sockets 插头和插座

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220509084132014.png" alt="image-20220509084132014" style="zoom:50%;" />

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220509084520941.png" alt="image-20220509084520941" style="zoom:50%;" />

## (2)components of power systems 

![image-20220509085322078](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220509085322078.png)

## 2.Tranformers

### 2.1 self inductance and mutual inductance

#### self inductance自感

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220509085521028.png" alt="image-20220509085521028" style="zoom: 50%;" />
$$
v(t)=N\frac {d \phi(t)}{dt}\\=L\frac{d_i(t)}{dt}\\
\phi(t)=P\cdot N \cdot i(t)\\
\Rightarrow v(t)=N\frac{d(PNi(t))}{dt}=N^2P\frac{di(t)}{dt}=L\frac{di(t)}{dt}\\
磁导P=\frac{uS}{l},u磁导率\  S面积，l长度
\\自感电压的方向：电流流入正极
$$

#### 互感

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220509090223589.png" alt="image-20220509090223589" style="zoom:50%;" />

$$
v_2(t)=N_2\frac {d\phi_2(t)}{dt}\\
=\N_2\frac{d\phi_2(t)}{dt}=N_2\frac{d(p_{21}\cdot N_1 \cdot i_1(t))}{dt}\\
=N_1\cdot N_2\cdot P_{21}\cdot \frac{di_1(t)}{dt}\\
=M_{21}\frac{di_1(t)}{dt}
$$

#### Dot convention

 同名端 

![image-20220509090917679](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220509090917679.png)

**互感的方向，电流流入正极+同名端**



<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220509091415851.png" alt="image-20220509091415851" style="zoom: 67%;" />



### Energy stored in a coupled circuit

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220510151219790.png" alt="image-20220510151219790" style="zoom:33%;" />

$$
v(t)=L\frac{di(t)}{dt}\\
w(t)=\int^t_0 \frac {di_1(t)}{dt}i_1(t)dt=\frac12 i_1^2(t)
$$


<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220510151116112.png" alt="image-20220510151116112" style="zoom: 67%;" />

$$
v_1(t)=L_1\frac{di_1(t)}{dt}+M\frac{di_2(t)}{dt}\ ,\ v_2(t)=L_2\frac{di_2(t)}{dt}+M\frac{di_1(t)}{dt}\\
i_1(0+)=i_2(0+)=0\\
\Longrightarrow w(t)=\int^t_0v_1(t)i_1(t)dt+\int^t_0v_2(t)i_2(t)dt\\
=\int^t_0L\frac{di_1(t)}{dt}i_1(t)dt+\int^t_0L\frac{di_2(t)}{dt}i_2(t)dt+\int^t _0 M\frac{di_2(t)}{dt}i_1dt+\int^t _0 M\frac{di_1(t)}{dt}i_2dt\\
=\frac12L_1i_1^2(t)+\frac 12L_2i_2^2(t)+Mi_1(t)\cdot i_2(t)
$$

#### couping coefficient K 耦合系数

$$
def:K=\frac M{\sqrt{L_1L_2}}\ note:0\leq k\leq 1\\
$$

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220510152202693.png" alt="image-20220510152202693" style="zoom: 67%;" />

$$why,k\leq 1?$$

$$Proof:(w\geq 0)$$

$$
w=\frac12L_1i_1^2(t)+\frac 12L_2i_2^2(t)-Mi_1(t)\cdot i_2(t)\geq 0\\
M\leq \frac12(L_1x(t)+L_2\frac{1}{x(t)})_{min}=\sqrt{L_1L_2}\\
K=\frac{M}{\sqrt{L_1L_2}}\leq 1
$$

### 2.2 Linear transformer

A transformer is gernerally a four-terminel device comprising 2+ magnetic coupled corls.

四端的,包括了两个或者更多个磁耦合的线圈

(linear: if the corls are wound on a magnetically linear materal,i.e permeability u is a constant)

如果线圈被绕在一个线性磁场的材料上面,或者说磁导率是一个常数的材料

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220509094536854.png" alt="image-20220509094536854" style="zoom: 50%;" />

$$
\begin{cases}
\widetilde V_1-(R+jwL_1)\widetilde I_1-jwM\widetilde I_2=0\\
-(R_2+jwL_2+z_1)\widetilde I_2-jwM\widetilde I_1=0\\
\widetilde V_2=-z_L\cdot\widetilde I_2
\end{cases}
$$
解得
$$
\frac{\widetilde V_1}{\widetilde V_2}=\frac{z_L(jwM)}{(R_1+jwL_1)(R_2+jwL_2+z_L)+w^2M^2}\\
\frac{\widetilde I_1}{\widetilde I_2}=\frac{-jwM}{R_2+jwL_2+z_L}
$$


### 2.3 Ideal transformer.
$$
Aussumption\begin{cases}
High\  permeability:\mu\rightarrow\infty\Rightarrow L_1,L_2,M\rightarrow\infty\\
parfect\ couping: K=\frac{M}{\sqrt{L_1L_2}}=1 \leftarrow (\phi 相同)\\
lossles costs:R_1=R_2=0
\end{cases}
$$

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220511083657291.png" alt="image-20220511083657291" style="zoom:50%;" />

1.voltage
$$
\begin{cases}
    V_1(t)=L_1\frac{di_1(t)}{dt}+M\frac{di_2(t)}{dt}\Rightarrow v_1(t)=\sqrt{L_1}\frac{di_1}{dt}+\sqrt{L_2}\frac{di_2(t)}{dt}\sqrt{L_1}\\
    V_2(t)=L_2\frac{di_2(t)}{dt}+M\frac{di_2(t)}{dt}\Rightarrow v_2(t)=\sqrt{L_1}\frac{di_1}{dt}+\sqrt{L_2}\frac{di_1(t)}{dt}\sqrt{L_1}
\end{cases}
\Rightarrow \frac{V_1(t)}{V_2(t)}=\sqrt{\frac{L_1}{L_2}}
$$
2.current
$$
    V_1(t)=L_1\frac{di_1(t)}{dt}+\sqrt{\frac{L_2}{L_1}}\frac{di_2(t)}{dt}\\
$$
3.input impedance(sinsordal steady)
$$
视角1:z_n=\frac{\widetilde{V_1}}{\widetilde{I_1}}=\frac{\widetilde{V_2}/n}{-n\widetilde{I_2}}=\frac{1}{n^2}(-\frac{\widetilde{V_2}}{I_2})=\frac{1}{n^2}z_L\\
\frac{\widetilde{V_2}}{\widetilde{V_1}}=n,\frac{\widetilde{I_2}}{\widetilde{I_1}}=-\frac{1}{n}\\
视角2:
\frac{\widetilde{V_2}}{\widetilde{V_1}}=\frac{z_L(jwM)}{(RL)}\\
\frac{\widetilde I_1}{\widetilde I_2}=\frac{-jwM}{R_2+jwL_2+z_L}=\frac{-jwM}=\frac{-jw\sqrt{L_1L_2}}{jwL_2+z_L}\xrightarrow{L_1,L_2,M\rightarrow \infty,{z_L忽略}}=-\sqrt{\frac{L_1}{L_2}}
$$
![image-20220511090332249](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220511090332249.png)

![image-20220619094118996](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220619094118996.png)

将二次电路映射到一次侧从而消去变压器的一般规则是:二次阻抗除以$n^2$,二次电压除以n,二次电流乘以n

将一次电路映射到二次侧从而消去变压器的一般规则是:一次阻抗乘以$n^2$,一次电压乘以n,二次电流除以n





## 3.Banlanced 3-phase system

- single-phase power supply
  
  same freq,same phase

![image-20220511091604478](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220511091604478.png)

![image-20220511091648352](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220511091648352.png)

![image-20220511091948073](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220511091948073.png)

- Banlanced 3-phase sources(a,b,c)
- Same magnitude,same freq,different phases(symmetric)
- e.g.$\widetilde{V_{an}}=V_P\angle 0\degree,\Rrightarrow\widetilde{V_b}=V_P\angle-120\degree\Rightarrow\widetilde{V_{cn}}=V_p\angle-240\degree$
       

a leads b and b leads c(postive sequence)正序 

## 5.Additional concepts

### 5.1 Line Voltages/currents 线电压/线电流,phase voltages/currents 相电压/相电流

Definition:
$$
line\begin{cases}
  line\ voltage:line-to-line\ voltage(e.g.\widetilde{V_ab})\\
  line\ current:current\ through\ the\ line(e.g.\widetilde{I_a})\\
\end{cases}\\
load/source\begin{cases}
  phase\ voltage:voltage\ across\ each\ branch(e.g\widetilde{V_{AB}})
\end{cases}
$$


<img src="C:\Users\lcf\AppData\Roaming\Typora\typora-user-images\image-20220516081844041.png" alt="image-20220516081844041" style="zoom:50%;" />







<img src="C:\Users\lcf\AppData\Roaming\Typora\typora-user-images\image-20220516082008119.png" alt="image-20220516082008119" style="zoom:50%;" />



![image-20220516082835814](C:\Users\lcf\AppData\Roaming\Typora\typora-user-images\image-20220516082835814.png)









|                                 |                          $\Delta$型                          | Y型                                                          |
| ------------------------------- | :----------------------------------------------------------: | ------------------------------------------------------------ |
| Line Votage                     |  $\widetilde{V_{ab}},\widetilde{V_{bc}},\widetilde{V_{ca}}$  | $\widetilde{V_{ab}},\widetilde{V_{bc}},\widetilde{V_{ca}}$   |
| LIne current                    |      $\widetilde{I_a},\widetilde{I_b},\widetilde{I_c}$       | $\widetilde{I_a},\widetilde{I_b},\widetilde{I_c}$            |
| Phase votage                    |  $\widetilde{V_{AB}},\widetilde{V_{BC}},\widetilde{V_{CA}}$  | $\widetilde{V_{AN}},\widetilde{V_{BN}},\widetilde{V_{CN}}$   |
| phase current                   |                    $I_{AB},I_{BC},I_{CA}$                    | $\widetilde {I_A}\widetilde{I_B}\widetilde{I_C}$             |
| Line voltage V.S. phase voltage | $\widetilde{V_{ab}}=\widetilde{V_{AB}}\\\widetilde{V_{bc}}=\widetilde{V_{BC}}\\\widetilde{V_{ca}}=\widetilde{V_{CA}}\\$ | $\widetilde{V_{AN}}=\frac{1}{\sqrt{3}}\widetilde {V_{ab}}\ang -30\degree\\\widetilde{V_{BN}}=\frac{1}{\sqrt{3}}\widetilde {V_{bc}}\ang -30\degree\\\widetilde{V_{CN}}=\frac{1}{\sqrt{3}}\widetilde {V_{ca}}\ang -30\degree$ |
| Line current V.S. Phase current | $\widetilde {I_{AB}}=\frac{1}{\sqrt 3}\widetilde {I_a}\ang30\degree\\\widetilde{I_{BC}}=\frac{1}{\sqrt 3}\widetilde{I_b}\ang30\degree\\\widetilde{I_{CA}}=\frac{1}{\sqrt 3}\widetilde I_c\ang30\degree\\$ | $\widetilde{I_A}=\widetilde{I_a}\\\widetilde{I_B}=\widetilde{I_b}\\\widetilde{I_C}=\widetilde{I_c}$ |
|                                 | <img src="C:\Users\lcf\AppData\Roaming\Typora\typora-user-images\image-20220516083607115.png" alt="image-20220516083607115" style="zoom:25%;" /> | <img src="C:\Users\lcf\AppData\Roaming\Typora\typora-user-images\image-20220516084324359.png" alt="image-20220516084324359" style="zoom: 50%;" /> |

![image-20220516084339242](C:\Users\lcf\AppData\Roaming\Typora\typora-user-images\image-20220516084339242.png)



### 5.2 Why 3-phase power system?

$$
\widetilde{V_{an}}=V_M\ang\theta_v,
\widetilde{V_{an}}=V_M\ang\theta_v-120\degree,
\widetilde{V_{an}}=V_M\ang\theta_v-240\degree\\

\widetilde{I_{a}}=I_a\ang\theta_v,
\widetilde{I_{b}}=I_b\ang\theta_v-120\degree,
\widetilde{I_{c}}=I_c\ang\theta_v-240\degree\\
\\
Instaneous\ power
\Rightarrow P_a(t)=V_{an}(t)i_a=\frac{V_mI_m}{2}[cos(2wt+\theta_v+\theta_i)+cos(\theta_v+\theta_i)]\\
P_b(t)=\frac{V_mI_m}{2}[cos(2wt+\theta_v+\theta_i-240\degree)+cos(\theta_v+\theta_i)]\\
P_b(t)=\frac{V_mI_m}{2}[cos(2wt+\theta_v+\theta_i-480\degree)+cos(\theta_v+\theta_i)]
\\
P(t)=P_a+P_b+P_c=\frac{3V_mI_m}2cos(\theta_v-\theta_i)
$$

三相是保证功率恒定的最少相数