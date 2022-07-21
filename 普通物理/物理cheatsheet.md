**R曲率半径:**
$$
1\degree y=y(x),R=\frac{(1+y')^{\frac32}}{y''},2\degree x=x(t),y=y(t)\Rightarrow R=\frac {(x'^2+y'^2)^{\frac32}}{x'y''-x''y'}\ \ \ \ 3\degree r=r(\theta)\Rightarrow R=\frac{(r^2+\dot r^2)^\frac32}{r^2+2\dot r^2-r\ddot r}
$$
三种坐标系下的位移速度加速度形式

|                | 位矢                                           | 速度                                                  | 加速度                                                       |
| -------------- | ---------------------------------------------- | ----------------------------------------------------- | ------------------------------------------------------------ |
| 平面直角坐标系 | $\vec r(t)=x(t)\vec i+y(t)\vec j+z(t)\vec k\\$ | $\vec r(t)=x'(t)\vec i+y'(t)\vec j+z'(t)\vec k\\$     | $\vec r(t)=x''(t)\vec i+y''(t)\vec j+z''(t)\vec k\\$         |
| 自然坐标系     | $\vec r(t)$                                    | $\displaystyle\vec v=v\vec e_t=\frac{ds}{dt}\vec e_t$ | $\displaystyle \vec a=\frac {dv}{dt}\vec{e_t}+v\frac{d\theta}{dt}\vec e_n=\frac{dv}{dt}\vec {e_t}+\frac{v^2}R\vec e_n$ |
| 极坐标系       | $\vec r (t)=r(t)\vec e_r(t)$                   | $\vec v=\dot r\vec e_r+r\dot \theta \vec e_\theta$    | $\vec a =(\ddot r-r\dot\theta^2)\vec e_r+(r\ddot \theta+2r\theta)\vec e_\theta$ |

$S'系相对S系匀速转动时:\vec v=\vec v'+\vec w\times\vec r'\ \ \ \ \ \ \ \vec a=\vec a'+2\vec w\times\vec v'+\vec w\times(\vec w\times\vec r')$

非惯性系:加速度不为0的参考系$\Rightarrow 惯性力\vec F_i=-m\vec a_0$

**转动惯性力**:$f_c=-mR\omega^2(对于转动惯性系中静止的物体使用)$

**科里奥利力**:$\vec{f_c}=2m\vec {v'}\times \vec{\omega}=-2m\vec{\omega} \times \vec{v'}$

质点系的动能可分解成**质心动能与质点系相对质心的动能之和**

一维弹性碰撞 $\displaystyle v_1=\frac{(m_1-m_2)v_{10}+2m_2v_{20}}{m_1+m_2} ,\ \ \ v_2=\frac{(m_2-m_1)v_{20}+2m_2v_{10}}{m_1+m_2}$

**角动量**  质点相对某点的角动量$\vec L=\vec r\times m\vec v$

**特殊的，对于定轴转动刚体的角动量$\vec L=J\vec \omega$**（其中J，$\omega$必须是相对于同一转轴）

相对于任意一点的角动量等于**物体相对于质心的角动量加质心系相对质心的角动量**

- 力矩表示力对物体作用时所产生的转动效应的物理量。力和力臂的向量积为力矩。**力矩不是一个绝对的量，而是相对于参考点O的量**

质点所受力相对参考点O的力矩：$$\vec M=\vec r \times \vec F$$（$$\vec r是质点和参考点O的向量$$）**注意$\vec r$在前**

##### 冲量矩：力矩对时间的积累        $\int^{t_2}_{t_1}Mdt$

力矩的功：$\int^{\theta_2}_{\theta_1}Md\theta$（力矩在空间上的积累）

转动的功能定理：$W=\frac{1}{2}J\omega_2^2-\frac{1}{2}Jw_1^2,E_k=\frac{1}{2}J\omega^2$

机械能守恒定律：$E=E_0+(W_{外力}+W_{非保守内力})$

**质点角动量定理：**质点所受力相对某参考点的力矩等于质点相对于该点角动量的变化率。即：$\displaystyle\vec M=\frac{d\vec L}{dt}=J\frac{d\vec \omega}{dt}=J\beta$

**转动惯量**$J=\int r^2 dm$转动惯量的和选取的轴有关

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220406143447694.png" alt="image-20220406143447694" style="zoom: 25%;" /><img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220406173205546.png" alt="image-20220406173205546" style="zoom: 30%;" />

- 平行轴定理:  设质量为 M 的刚体绕过**质心**的转轴的转动惯量为 Icm ；绕过A点的转轴的转动惯量为 IP；两个转轴互相平行，相距为 d，则：$I_P=I_{cm}+Md^2$    注意：$I_{cm}$一定得是质心轴！

- 垂直轴定理（适用范围：仅限薄片）$I_z=I_x+I_y$      (其中x, y为平面内正交的轴；z 为垂直平面的轴)

**伯努利方程**$p+\frac12 \rho v^2+\rho gh=C$

**机械波**的定义:$\displaystyle \frac{\partial ^2y}{\partial t^2}=u^2\frac{\partial^2y}{\partial x^2}\ \  \ 弦上横波中\frac{\partial^2 y}{\partial t^2}=\frac{F}{\rho}\frac{\partial^2 y}{\partial x^2}\Rightarrow \sqrt{\frac{F}{\rho}}=v=\frac{\lambda}{T}=\frac{\lambda\omega}{2\pi}$

细棒中的纵波波速$v=\sqrt{\frac E\rho},E杨氏模量,\rho 密度$

$对于机械波的单位能量\Delta E=\Delta E_k+\Delta E_p=\frac12\mu\Delta x(\frac{\partial y}{\partial t})^2+\frac12 F\Delta x(\frac{\partial y}{\partial x})^2\\
对于行波y=A cos(wt-kx)\ \Delta E_k=\frac12\mu\Delta x \omega^2A^2sin^2(wt-kx),
\Delta E_p=\frac12F\Delta x k^2A^2sin^2(wt-kx),\xRightarrow{\frac{\omega}{k}=\sqrt{\frac{F}{\mu}}\\}\Delta E_k=E_p$

$对于驻波y=Acos(\frac{2\pi}{\lambda}x)coswt,\begin{cases}
\Delta E_k=\frac12\rho\Delta x\frac{\partial^2y}{\partial t^2}=\frac12\rho\Delta x A^2w^2cos^2(\frac{2\pi}{\lambda}x)sin^2wt,\\  \Delta E_p=\frac12 F\Delta x\frac{\partial^2 y}{\partial ^2 x}=\frac12 F\Delta x A^2\frac{2\pi}{\lambda}^2sin^2(\frac{2\pi}{\lambda}x)cos^2wt \end{cases}\xRightarrow{\sqrt{\frac{F}{\rho}}=v=\frac{\lambda}{T}=\frac{\lambda\omega}{2\pi}}
\begin{cases}\Delta E_k=\frac12\rho\Delta x A^2w^2cos^2(\frac{2\pi}{\lambda}x)sin^2wt \\
\Delta E_p=\frac12\rho\Delta x A^2w^2sin^2(\frac{2\pi}{\lambda}x)cos^2wt \end{cases}\\$

多普勒效应:$\displaystyle f_L=\frac {v-v_L}{v-v_s}f_s,s\rightarrow source$

时间膨胀效应:$\displaystyle\Delta t=\frac{\Delta t_0}{\sqrt{1-(\frac{u}{c})^2}}$,动尺缩短效应:$\displaystyle l=l_0\sqrt{1-(\frac{u}{c})^2}$

质能关系:$\displaystyle E=mc^2,m=\frac{m_0}{\sqrt{1-(\frac{u}{c})^2}}$
相对论动能:$E_k=E-E_0=mc^2-m_0c^2$,动量和能量关系:$E^2=(m_0c^2)^2+p^2c^2$

| 洛伦兹坐标变换                                           | 洛伦兹时间变换                                               | 洛伦兹速度变换式                                             | 洛伦兹时间间隔变换式                                         | 洛伦兹距离间隔变换式                                         |
| -------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| $\displaystyle x'=\frac{x-ut}{\sqrt{1-(\frac{u}{c})^2}}$ | $t'=\frac{\displaystyle t-\frac{ux}{c^2}}{\displaystyle \sqrt{1-(\frac{u}{c})^2}}$ | $\displaystyle u_x'=\frac{u_x-u}{\displaystyle 1-\frac{uu_x}{c^2}}$ | $\Delta t'=\frac{\displaystyle\Delta t-\frac u{c^2}\Delta x }{\displaystyle \sqrt{1-(\frac{u}{c})^2}}$ | $\displaystyle \Delta x'=\frac{\Delta x-u\Delta t}{\sqrt{1-(\frac{u}{c})^2}}$ |
| $\displaystyle x=\frac{x'+ut}{\sqrt{1-(\frac{u}{c})^2}}$ | $t=\frac{\displaystyle t'+\frac{ux}{c^2}}{\displaystyle \sqrt{1-(\frac{u}{c})^2}}$ | $\displaystyle u_x=\frac{u_x'+u}{\displaystyle 1+\frac{uu_x}{c^2}}$ | $\Delta t=\frac{\displaystyle\Delta t+\frac u{c^2}\Delta x }{\displaystyle \sqrt{1-(\frac{u}{c})^2}}$ | $\displaystyle \Delta x'=\frac{\Delta x+u\Delta t}{\sqrt{1-(\frac{u}{c})^2}}$ |

$\displaystyle \frac{1}{2}m(v^2)_{av}=\frac{3nRT}{2N}=\frac{3}{2}kT,k=\frac{R}{N_A}=1.380662\times10^{-23}J\cdot K^{-1},R=8.314J\cdot K^{-1}\cdot mol^{-1}$

<img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220601221757124.png" alt="image-20220601221757124" style="zoom: 20%;" /> <img src="https://heaticy-1310163554.cos.ap-shanghai.myqcloud.com/markdown/image-20220601232132678.png" alt="image-20220601232132678" style="zoom: 23%;" />




理想气体在平衡态(P，V，T）下的熵$S=vC_VlnT+vRlnV+S_0$

（1）温度越高，分子热运动越激烈、无序，熵越大。

（2）体积越大，分子在位置空间分布越分散，系统包含的微观状态越多，墒越大。

热力学第二定律,一个孤立系统的熵不会减小,$S_{环境}+S_{系统}\geq 0$
即克莱修斯不等式$\oint \frac {dQ}{T}\geq 0$(其中,dQ是系统与温度为T的热源接触时所吸收的能量)

环境熵变$\displaystyle S_{环境}=\frac{Q_{环境}}{T_{环境}}=\frac{-Q_{系统}}{T_{环境}}$
