

# lecture 4

## 1. backgrounds

## 2 . practical Op amps

## 3. ideal op Amps

​          $\downarrow$

Assumption $\begin{cases}a=\infty\\R_{in}=\infty(R_i)\\R_out=0\end{cases}$

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/D01068F8686DDDB34FF67110C4A7CD19.jpg" alt="img" style="zoom:75%;" />

## Ideal Op Amps

virtual short  

$$\begin{cases}A=\infty\\linear region:V_0=A(V_p-V_n)\\V_0:finite  number\end{cases}$$



virual open 

虚断（针对电流）
$$
\begin{cases}
R_i=0\\
i_p=-in=\frac{V_p-V_n}{R_i}=0\\
i_p=i_n=0
\end{cases}
$$
<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/E54E2A1C50FDC337968E495314D52E1D.jpg" alt="img" style="zoom:67%;" />

## applications(Assume Linear region)

### 1. inverting amplifier 反向比例放大器

![img](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/3EE264360879698446EC70503E798960.png)

### 2. Non-inverting Amplifier 正向比例放大器

![img](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/DD6AC1C55CF1AA18CBF59FC305864D15.png)

### 3. Voltage follower 电压跟随器

![img](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/97BA6C90313AA3C07D04BC47BE116F8D.png)

### 4. Summing Amplifier 加法器

![img](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/7550AC370C62881EDA410AE927083B58.png)
$$
\frac{v_1-0}{R_1}+\frac{V_2-0}{R_2}+\frac{v_3-0}{R_3}+\frac{V_0-0}{Rf}=0
$$

### 5. Difference Amplifier减法器

![img](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/358D0575141C5C4DE07180760706E9C4.png)

![img](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/E66723EBA95DFE4DCDACCEAE1421D7D4.jpg)

## note

1.线性区/饱和区

2.在1.情况下正确使用虚断虚断条件

3.负反馈

 ## 负反馈

简单理解：输出连接输入反向输入端

本质理解：输出端小扰动对输入端端影响是增强还是减弱该扰动

![img](https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/45F24A85F4204B0C6DF7D40637524393.jpg)

