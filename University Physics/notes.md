<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>

<!-- TOC -->

- [大学物理笔记](#大学物理笔记)
    - [多普勒效应](#多普勒效应)
    - [驻波(stationary wave)](#驻波stationary-wave)
    - [第九章 &emsp; Relativistic Mechanics 相对论力学](#第九章-emsp-relativistic-mechanics-相对论力学)
        - [9.1 &emsp;伽利略变换](#91-emsp伽利略变换)
        - [9.2 &emsp;洛伦兹变换 Lorentz Transformation](#92-emsp洛伦兹变换-lorentz-transformation)
        - [9.3 &emsp;时空图和孪生paradox](#93-emsp时空图和孪生paradox)
        - [9.4 &emsp;相对论运动学](#94-emsp相对论运动学)
        - [9.5 &emsp; 相对论动力学(Relativistic Dynamics)](#95-emsp-相对论动力学relativistic-dynamics)
    - [期末考试大致内容](#期末考试大致内容)
    - [Project Proposal](#project-proposal)
    - [第十章 温度](#第十章-温度)
        - [10.1 Equilibruim state](#101-equilibruim-state)
        - [10.2 Thermal equilibruim and temperature](#102-thermal-equilibruim-and-temperature)
        - [10.4 物态方程](#104-物态方程)
    - [第十一章 热力学第一定律](#第十一章-热力学第一定律)
        - [11.1 功,内能和热力学第一定律](#111-功内能和热力学第一定律)
        - [11.3 热容和比热容(Heat capacity and specific heat capacity)](#113-热容和比热容heat-capacity-and-specific-heat-capacity)
        - [11.4 Free expansion and internal energy of gas](#114-free-expansion-and-internal-energy-of-gas)
        - [11.5 Adiabatic equation](#115-adiabatic-equation)
        - [11.6 卡诺循环](#116-卡诺循环)
    - [第十二章 热力学第二定律](#第十二章-热力学第二定律)
        - [12.1 内容](#121-内容)
        - [12.2 卡诺定理](#122-卡诺定理)
        - [12.3 熵与熵原理](#123-熵与熵原理)
        - [12.4 热力学势](#124-热力学势)

<!-- /TOC -->

# 大学物理笔记
## 多普勒效应

source:$v_s$, observer:$v_O$,distance $L$

issued at $t=0,x=0$, recieved at $t_1',L+v_Ot_1'$

issued at $t=T,x=v_ST$, received at $t_2',L+v_Ot_2'$

由运动学:
$$
    v_Pt_1'=L+v_Ot_1'\\
    v_P(t_2'-T)=L+v_Ot_2'-v_ST
$$
于是
$$
\begin{aligned}
        t_1'&=\frac{L}{v_P-v_O}\\
    t_2'&=\frac{L}{v_P-v_O}+\frac{v_P-v_S}{v_P-v_O}T\\
    T'&=t_2'-t_1'=\frac{v_P-v_S}{v_P-v_O}T\\
    \nu'&=\frac{v_P-v_O}{v_P-v_S}\nu
\end{aligned}

$$

Discussion:

$v_O>v_S$(including $v_S\leq0$):separating, $\nu'<\nu$, Doppler redshift

$v_S>v_O$(including $v_O\leq0$):approaching, $\nu'>\nu$, Doppler blueshift

靠近:频率变高;远离:频率变低


考虑波源的运动与波振面的运动(supersonic speed $v_S>v_p$)

马赫锥:$sin\theta=\frac{v_P}{v_S}$

## 驻波(stationary wave)

- 推导

由$kx-\omega t-\phi=const$,求导得 $v=\frac{\omega}{k}$

$$
    \begin{aligned}
        u_1 &= Acos(kx-\omega t-\phi)\\
        u_2 &= Acos(kx+\omega t)\\
         &=Acos(k(x+\frac{\omega}{k}t)) \\
        从而u_1+u_2 &= 2Acos(kx-\frac{\phi}{2})cos(wt+\frac{\phi    }{2})\\
    \end{aligned}
    \tag{1}
$$
令 $(u_1+u_2)_{x=0}=0$,得 $\phi=\pi$;
令 $(u_1+u_2)_{x=L}=0$,得 $L=\frac{n\pi}{k}=\frac{n\lambda}{2}$
$$
    
$$
注意 $\lambda=T\cdot v_P=\frac{2\pi}{\omega}\cdot \frac{\omega}{k}=\frac{2\pi}{k}$, $k=\frac{2\pi}{\lambda},\omega=vk$,有
$$
    \begin{aligned}
        f &= \frac{\omega}{2\pi}=\frac{kv}{2\pi}=n \frac{v}{2L} \\
         &=f_n \\
         &=nf_1 \\
        % &= \\
    \end{aligned}
$$
波节(node),波腹(antinode)的定义

- 半波损失

fixed hard boundary; from high spped to low speed

由$(1)$式,令 $(u_1+u_2)_{x=0}=0$,得 $\phi=\pi$,即为在固定端的相差


## 第九章 &emsp; Relativistic Mechanics 相对论力学

### 9.1 &emsp;伽利略变换
- 观测者:一套矫正好的时钟,可记录 $x,y,z,t$
- 结果 $t_A'-t_B'=t_A-t_B$,$x_A'-x_B'=x_A-x_B-u(t_A-t_B)$
  
  同时测量:$x_A'-x_B'=x_A-x_B$

  速度直接叠加,加速度不变

- Galileo's relativity: 力学定律在不同惯性参考系中相同
- 电学:不满足麦克斯韦方程组

### 9.2 &emsp;洛伦兹变换 Lorentz Transformation

- Two basic principles of Special Theory of Relativity
  - 所有惯性参考系中物理定律相同(力学,电学等)
  - 光速不变
- 推导

假定变换为线性变换(考虑匀速直线运动);

待定系数:

$$
    \begin{aligned}
        x' &= a_{11}x+a_{12}y+a_{13}z+a_{14}t\\
        y' &= y\\
        z' &= z\\
    \end{aligned}
$$

For arbitrary y,z if $x'=0$,$x=ut$;则 
$$
x'=a_{11}(u)(x-ut),a_{11}(0)=1
\tag{1.1}
$$

By the priciple of relativity, we have
$$
    x=a_{11}(-u)(x'+ut'),带入(1.1),有\\
    t'=f(x,x'(u,t))=a_{44}t+a_{41}x
$$
从而
$$
    \begin{aligned}
        x' &= a(x-ut)\\
        t' &= b(t-ex)\\
    \end{aligned}
    \tag{1.2}
$$
解得 $x=\frac{1}{\Delta}(bx'+aut')$

与 $x=a_{11}(-u)(x'+ut')$比较,得 $a=b$

考虑光速不变:假设 $t=t'=0$时在原点发出光信号,有
$$
    x^2+y^2+z^2=c^2t^2\\
    x'^2+y'^2+z'^2=c^2t'^2
$$

代入 $(1.2)$式,有
$$
    \begin{aligned}
        e &= \frac{u}{c^2}\\
        a &= \frac{1}{\sqrt{1-\beta^2}}=\gamma=\sqrt{1-\frac{v^2}{c^2}}\\
        其中\beta &= \frac{u}{c}\\
    \end{aligned}
$$

完整的变换关系为
$$
    \begin{aligned}
        x' &= \gamma(x-ut)\\
        y' &= y\\
        z' &= z\\
        t' &= \gamma(t-\frac{u}{c^2}x)\\
    \end{aligned}

$$

考虑事件对 $(x_1',t_1'),(x_2',t_2')$,洛伦兹变换是
$$
    \begin{aligned}
        \Delta x' &= \gamma(\Delta x-u\Delta t)\\
        \Delta y' &= \Delta y\\
        \Delta z' &= \Delta z\\
        \Delta t' &= \gamma(\Delta t-\frac{u}{c^2}\Delta x)\\
    \end{aligned}

    \tag{1.3}

$$

- 讨论
  - 逆变换: $u\to-u$ &emsp;直接根据相对性原理
  - Invariance of spacetime interval 时空间隔不变:$(\Delta s)^2=(c\Delta t)^2-(\Delta x)^2-(\Delta y)^2-(\Delta z)^2=(\Delta s')^2$
  - 伽利略变换:时间归时间 空间归空间 &emsp;时间空间分别不变

- 事件对
  - 光信号联系: $(c\Delta t)^2=(\Delta x)^2,\Delta s=0$
  - 固有时间间隔与固有空间间隔

- Simultaneous measurement $\Delta x'=\ell_0$ in $S'(\Delta t'=0)$ 形成一个事件

    the same pair of events in S:
$$
    \begin{aligned}
        \Delta x &= \gamma(\Delta x'+u\Delta t')=\gamma\Delta x'=\gamma \ell_0\\
        \Delta t &= \gamma(\Delta t+\frac{u}{c^2}\Delta x')\not=0\\
    \end{aligned}
    同时的相对性
$$
  也即 $\ell=\ell_0\sqrt{1-\frac{v^2}{c^2}}=\frac{\ell_0}{\gamma}$

- 用光速不变推出钟慢:

$$
\begin{aligned}
    \Delta t'&=\frac{2L_0}{c}\\
    (\frac{u\Delta t}{2})^2+L_0^2&=(\frac{c\Delta t}{2})^2(用到光速不变)\\
    \Delta t=\frac{2L_0}{\sqrt{c^2-u^2}}&=\frac{2L_0/c}{\sqrt{1-\beta^2}}=\gamma\Delta t'
\end{aligned}



$$
- 用光速不变推出尺缩:

$$
    \begin{aligned}
        c\Delta t_1 &= L+u\Delta t_1,c\Delta t_2=L-u\Delta t_2\\
        \Delta t &= \Delta t_1+\Delta t_2=\frac{L}{c+u}+\frac{L}{c-u}=\frac{2L}{c}\frac{1}{1-\beta^2}\\
        \Delta t' &= \frac{2L_0}{c}=\gamma \Delta t\\
        \frac{2L_0}{c\gamma} &= \frac{2L}{c}\frac{1}{1-\beta^2}\\
        于是L&=\frac{L_0}{\gamma}
    \end{aligned}
$$

- 因果律及信号传播(Causality and signal speed)
  - An event $P(x_P,t_P)$ causes an event $Q(x_Q,t_Q)$. 信号传输速度 
  $$
  v_S=\frac{x_Q-x_P}{t_Q-t_P}=\frac{\Delta x}{\Delta t}
  $$

   在 $S'(u)$系中时间间隔为
   $$
       \Delta t'=\gamma\Delta t(1-\frac{uv_S}{c^2})
   $$
   为保证先后次序,必须有
   $$
       1-\frac{uv_S}{c^2}<0\\
       则v_S<c
   $$

- 光多普勒效应
  - 由$(1.3),\Delta t=\sqrt{\frac{1+\beta}{1-\beta}}\Delta t'$
  - redshift: $\nu_0=\sqrt{\frac{1-\beta}{1+\beta}}\nu_e$

- 波动方程: 用洛伦兹变换恰好符合(洛伦兹不变)

### 9.3 &emsp;时空图和孪生paradox
- Minkowski Space
  - 洛伦兹变换在时空图中的体现
- Twin paradox: 在宇宙飞船加速,减速的过程中经历了非惯性系
- Pole-barn Paradox: 火车进隧道;火车系:隧道收缩;地面系:火车收缩
  - 涉及同时的相对性:看能否在地面系同时关上前门和后门(火车系觉得没有同时)
  - 地面系的观测者觉得能关进去,在火车系的观测者看来后门早就关起来了
- Visual Apperance
  - 球不变 &emsp;立方体转过一个角度

### 9.4 &emsp;相对论运动学
- 速度变换公式(求导可得)

$$

    \begin{aligned}
        v_x' &= \frac{v_x-u}{1-v_x\dfrac{u}{c^2}}\\
        v_y' &= \frac{v_y}{\gamma(1-v_x\dfrac{u}{c^2})}\\
        v_z' &= \frac{v_z}{\gamma(1-v_x\dfrac{u}{c^2})}\\
    \end{aligned}
$$

### 9.5 &emsp; 相对论动力学(Relativistic Dynamics)
- 广义相对论: 引力场,非惯性系
- 讨论$m,p,F,E_k,a$
- Discuss a completely inelastic collision(保持动量守恒)
  - In $S'(-u):u,-u\to0,0$
  - In $S:v_x,0\to u,u$; &emsp; $v_x=\dfrac{u+u}{1+u\frac{u}{c^2}}(9.5.1)$ &emsp; 
  - 而 $m\dfrac{u+u}{1+\frac{uu}{c^2}}+m\times0\not=2mu$,动量守恒不成立.
  - 假定 $m\equiv m(v),m_0\equiv m(0)$,有
$$
    \begin{aligned}
        m(v_x)+m_0 &= m_{total}(u)\\
        m(v_x)\cdot v_x+m_0\cdot0 &= m_t(u)u\\
         &= [m(v_x)+m_0]u\\
        求得 m(v_x) &= \frac{m_0}{\frac{v_x}{u}-1}\\
    \end{aligned}
$$
由 $(9.5.1)$,$\dfrac{v_x}{u}-1=\sqrt{1-\beta^2}$,则 $m(v)=\gamma m_0$. 于是

$$
    \begin{aligned}
        p &= \gamma m_0v\\
        E_k &=\int F\cdot dx=\int\frac{d}{dt}(mv)\cdot dx=\int v\cdot d(mv) \\
        而 d(mv) &=vdm+mdv  \\
        则 E_k &= \int(v^2dm+mvdv)\\
    \end{aligned}
$$
考虑 $m^2(1-\frac{v^2}{c^2})=m_0^2,m^2(c^2-v^2)=m_0^2c^2$,两边微分得
$$
    c^22mdm-v^22mdm-m^22vdv=0,\\
    c^2dm-v^2dm-mdv=0,c^2dm=v^2dm+mdv
$$
于是
$$
    \begin{aligned}
        E_k &= \int c^2dm=mc^2-m_0c^2\\
         &= m_0c^2\Big[\frac{1}{\sqrt{1-\dfrac{v^2}{c^2}}}-1\Big]\\
         &=(\gamma-1)m_0c^2 \\
    \end{aligned}
$$


- 讨论
  - 牛顿力学中
$$
    E_k=\int v\cdot d(mv)=\int mv\cdot dv=\frac{1}{2}mv^2
$$
- - 相对论中,mass-energy &emsp; $E=mc^2=E_k+m_0c^2$
- - 已知动能求速度: $\gamma=\dfrac{E_k}{m_0c^2}+1$
- 相对论能量-动量关系
  - $E=\sqrt{c^2p^2+m_0^2c^4}$
  - 若 $m_0=0,E=cp,p=\dfrac{E}{c}$
  - 若 $cp<<m_0c^2$,泰勒展开后得到牛顿力学.

## 期末考试大致内容
- 相对论运动学: 速度的变换
- 理想气体(或给定气体的状态方程) 等温膨胀,绝热等过程, 功和热, 内能等
- 理想气体的性质: 速度,平均动能等
- 过程中温度的变化,熵的变化
- 过程中 __亥姆霍兹自由能变__, 求平衡态(可能有数学上求导等)
- 比热容, 温度. 
- 相变 三相点.

## Project Proposal
- structure
  - Template
  - Guideline
- how and where
- basics of thesis writing
- deadline


## 第十章 温度
### 10.1 Equilibruim state
- 
  |System|exchange|
  |----|----|
  |isolated|$\times$|
  |closed|energy|
  |open|energy&matter|
- Thermodynamic Equilibruim state: 宏观状态不随时间改变,除非外界条件发生变化.
- description of equilibruim state: state variables
  - extensive quantity: $F(n\ systems)=nF(1\ system)$
  - intensive quantity: $F(n\ systems)=F(1\ system)$
- relaxation time $\tau$: 恢复平衡所用时间
- Quasi-static process 准静态过程: $t>>\tau$, 每一点都是平衡态, 可以在状态图上画出. 
- No-dissipative, quasi-static process is reversible. (无耗散准静态过程是可逆的); All natural process(自发过程) is irreversible.
  - 系统和外界同时恢复初态
### 10.2 Thermal equilibruim and temperature
- The zeroth law of thermodynamics: 热平衡的传递性(热平衡的系统有共同性质)
- 温度: 衡量热平衡的一种物理性质
- 各种温标

### 10.4 物态方程
- 微分的常见写法 $\big(\dfrac{\partial U}{\partial V}\big)_T\ ,\ \big(\dfrac{\partial U}{\partial V}\big)_P\ .$ 保持右下标不变
- $P,V,T不独立,f(P,V,T)=0\to U(T,P)=U(T,V(P,T))=U(T,V)=0$
- 等压线膨胀系数 $a_\ell=\dfrac{1}{L}\dfrac{\partial L}{\partial T}_p$; $\alpha_V=\dfrac{1}{V}\big(\dfrac{\partial V}{\partial T}\big)_P=\dfrac{1}{L^3}\big(\dfrac{\partial L^3}{\partial T}\big)_P=3\alpha_\ell$
- 等温线膨胀系数 $\kappa_T=-\dfrac{1}{V} \dfrac{\partial V}{\partial p}_T$
- 体积变化方程

$$
\begin{aligned}
    
    \frac{dV}{V}&=\frac{1}{V}\big(\dfrac{\partial V}{\partial T}\big)_pdT+\frac{1}{V}\big(\dfrac{\partial V}{\partial p}\big)_Tdp=\alpha_V(T)dT-\kappa_T(p)dp\\
    &(全微分)\\
    ln\frac{V}{V_0}&=\alpha_V\Delta T-\kappa_T\Delta p\\
    V&=V_0(1+\alpha_V\Delta T-\kappa_T\Delta p)
\end{aligned}
$$
- Van der Waal's equation

$$
    \big[p+a(\frac{n}{V})^2\big](V-nb)=nRT
$$
推导: 对1mol理想气体:
$$
\begin{aligned}
    
    p=\frac{RT}{V_m}&\leftarrow\frac{RT}{V_m-b}(相互作用,体积减小)\\
    &\leftarrow \frac{RT}{V_m-b}-\frac{a}{V^2}(相互作用,压强减小,体积越小作用力越大)
\end{aligned}
$$

## 第十一章 热力学第一定律
### 11.1 功,内能和热力学第一定律
- 准静态过程压活塞 $\bar{d}W=-p\bar{d}V$, $W=-\displaystyle\int_{V_i}^{V_f}pdV$ (依赖于 $P-V$图上的路径,不是全微分)
- 绝热功: Internal energy function $\Delta U=U_B-U_A\equiv W_{BA}\equiv-W_{AB}$(用与路径无关的绝热功定义内能变化)
- 非绝热功: $\Delta U=W+Q$外界做的功和外界传给内部的热量; 微分 $dU=\bar{d}Q+\bar{d}W$(功和热不是全微分,与路径有关)

### 11.3 热容和比热容(Heat capacity and specific heat capacity)
- $C=\lim\limits_{\Delta T \to0}\dfrac{\Delta Q}{\Delta T}$; specific: $C_m=\dfrac{C}{n}$
  - $C=0$: 绝热(adiabatic)过程, $\Delta Q=0$
  - $C=\infty$: 等温(isothermal)过程,$\Delta T=0$
- $C_V=\lim\limits_{\Delta T\to 0}(\dfrac{\Delta Q}{\Delta T})_V=\lim\limits_{\Delta T\to 0}(\dfrac{\Delta U}{\Delta T})_V=\big(\dfrac{\partial U}{\partial T}\big)_V$
- $C_P=\lim\limits_{\Delta T\to 0}(\dfrac{\Delta Q}{\Delta T})_p=\lim\limits_{\Delta T\to 0}(\dfrac{\Delta U+p\Delta V}{\Delta T})_p=\big(\dfrac{\partial (U+pV)}{\partial T}\big)_p\equiv \big(\dfrac{\partial H}{\partial T}\big)_p$, $H=U+pV$: enthalpy, 焓
- ratio of specific heat: $\gamma=\dfrac{C_p}{C_V}$
- heat capacity of ideal gases


    | monatomic ideal gas|$C_V=\frac{3}{2}nR$|
    |----|----|
    | 双原子 ideal gas|$C_V=\frac{5}{2}nR$|
    | 三原子 ideal gas|$C_V=\frac{6}{2}nR$|
### 11.4 Free expansion and internal energy of gas

- Case of free expansion

$$
    \begin{aligned}
        U &= U(T,V)\\
        dU &= \big(\dfrac{\partial U}{\partial T}\big)_VdT+\big(\dfrac{\partial U}{\partial V}\big)_TdV\\
        T &= T(U,V)\\
        dU &= \big(\dfrac{\partial U}{\partial T}\big)_V[\big(\dfrac{\partial T}{\partial U}\big)_VdU+\big(\dfrac{\partial T}{\partial V}\big)_UdV]+\big(\dfrac{\partial U}{\partial V}\big)_TdV \\
        &对照左右,得\\
        \big(\dfrac{\partial U}{\partial T}\big)_V\big(\dfrac{\partial T}{\partial U}\big)_V&=1\\
        \big(\dfrac{\partial U}{\partial V}\big)_T&=-\big(\dfrac{\partial U}{\partial T}\big)_V \big(\dfrac{\partial T}{\partial V}\big)_U=-C_V\big(\dfrac{\partial T}{\partial V}\big)_U\to焦耳系数=0(理想气体)\\
        故U&=U(T)
    \end{aligned}
$$
- 焦耳的实验非常不严谨
- 理想气体:
$$
    \begin{aligned}
        dU(T) &= \frac{dU}{dT}dT=C_VdT\\
        U &= U_0+C_VT\\
        dQ &= dU-dW=C_VdT+pdV\\
        理想气体:d(pV)&=d(nRT)\\
        pdV+Vdp&=nRdT,pdV=nRdT-Vdp\\
        dQ &= (C_V+nR)dT-Vdp\\
        C_p&=C_V+nR\to C_V=\frac{nR}{\gamma-1}, C_p=\frac{\gamma nR}{\gamma-1}
    \end{aligned}
$$
### 11.5 Adiabatic equation
$$
    \begin{aligned}
        dQ &= dU-dW, \\
         &= C_VdT+pdV\\
        C_VdT+pdV &= 0\\
        又Vdp+pdV &=nRdT=(\gamma-1)C_VdT \\
    \end{aligned}
$$
&emsp;&emsp;消去 $dT$,得
$$
    \begin{aligned}
        Vdp+\gamma pdV &= 0\\
        \frac{dp}{p}+\gamma\frac{dV}{V} &= 0\\
        lnp+\gamma lnV &= C\\
        pV^\gamma &= C\\
    \end{aligned}
$$
&emsp;&emsp;由 $\gamma>1$, 绝热线比等温线陡峭
- adiabatic work

$$
\begin{aligned}
    
    W_S&=-\int_{V_1}^{V_2}pdV=-C\int_{V_1}^{V_2}\frac{dV}{V^\gamma}=\frac{C}{\gamma-1}(\frac{V_2}{V_2^\gamma}-\frac{V_1}{V_1^\gamma})\\
    &=\frac{1}{\gamma-1}(p_2V_2-p_1V_1)\\
    &=\frac{nR}{\gamma-1}(T_2-T_1)\\
    &=C_V(T_2-T_1)=\Delta U
\end{aligned}
$$
- 声音的传播: 绝热

### 11.6 卡诺循环
- 高温热源 $T_1$等温膨胀$\to$绝热膨胀$\to$低温热源 $T_2$等温压缩$\to$绝热压缩
- $T_1, U=U(T_1)=const$ 热机吸热,做功
- $T_2$ 热机放热
- 整个循环: $\Delta U=0, \Delta Q_{12}+\Delta Q_{34}-\Delta W=0$

$$
\begin{aligned}
    效率\eta&=\frac{\Delta W}{\Delta Q_{12}}=\frac{\Delta Q_{12}+\Delta Q_{34}}{\Delta Q_{12}}=\frac{Q_1-Q_2}{Q_1}\\
    &(考察做功过程中的放热Q_2,\ 放热越多效率越低)\\
    等温过程:Q_1&=\Delta W_{12}=\int_{V_1}^{V_2}pdV=\int_{V_1}^{V_2}\frac{nRT_1}{V}dV=nRT_1ln\frac{V_2}{V_1}\\
    Q_2&=-\Delta Q_{34}=nRT_2ln\frac{V_3}{V_4}\\
    \eta&=1-\frac{T_2ln\frac{V_3}{V_4}}{T_1ln\frac{V_2}{V_1}}\\
    2\to3:&T_1V_2^{\gamma-1}=T_2V_3^{\gamma-1}\\
    4\to1:&T_1V_1^{\gamma-1}=T_2V_4^{\gamma-1}\\
    \eta&=1-\frac{T_2}{T_1}
\end{aligned}
$$
要学会将此推导推广到其他热机上
- 可逆过程: 外界不可逆
- 逆卡诺循环: 从低温热源吸热 到高温热源被做功,放热

## 第十二章 热力学第二定律
### 12.1 内容
- No process is possible whose sole result is the absorption of heat from a reservoir and the conversion of this heat into work.
- No process is possible whose sole result is the transfer of heat from a cooler to a hotter body.
- 自发过程具有方向性

### 12.2 卡诺定理
- 任何热机效率不超过可逆热机
- 证明: 任意热机做功驱动可逆热机的逆过程, 反证法与热二矛盾

### 12.3 熵与熵原理
- 熵的引入


假设$Q_2<0$为放热:

$$
    \begin{aligned}
        效率不大于卡诺热机:\eta_A &= 1+\frac{Q_2}{Q_1}\leq1-\frac{T_2}{T_1}\\
        \sum_{i=1}^2\frac{Q_i}{T_i} &\leq 0\\
        一般过程:  \sum_{i=1}^n\frac{Q_i}{T_i} &\leq 0 (系统与很多热源接触)\\
        \oint\frac{dQ}{T} &\leq0\\(取等:可逆过程,考虑&Q_i\to-Q_i )\\
        (环路&积分)\\
        写作全微分: \frac{\bar{d}Q}{T}&\equiv dS\\
        S_B-S_A&=\int_A^B\Big(\frac{dQ}{T}\Big)_R
    \end{aligned}
$$
若环路中包含不可逆过程: 

$$
    \begin{aligned}
      \displaystyle\oint\Big(\frac{dQ}{T}\Big)&<0\\
        \int_A^B\Big(\frac{dQ}{T}\Big)_{IR}+\int_A^B\Big(\frac{dQ}{T}\Big)_{R} &<0 \\
         \int_A^B\Big(\frac{dQ}{T}\Big)_{IR}-\int_B^A\Big(\frac{dQ}{T}\Big)_{R} &<0 \\
         S_B-S_A&>\int_A^B\Big(\frac{dQ}{T}\Big)_{IR} \\
         \int_A^BdS&> \int_A^B\Big(\frac{dQ}{T}\Big)_{IR}\\
         dS&>\Big(\frac{dQ}{T}\Big)_{IR}
    \end{aligned}
$$
- 熵原理: 任何过程: $dS\geq\dfrac{dQ}{T}$
  - 绝热过程: $dQ=0$; 可逆: $dS=0$, isentropic 等熵过程
  - 孤立系统: $dS\geq0$; 非平衡趋于平衡: 熵增加; 平衡态: 宏观特征不变,熵最大
- 热二的另一种形式: The entropy of an isolated system never decreases.
  - 从单一热源吸热的熵变: $\Delta S=\dfrac{\Delta Q}{T}=\dfrac{-Q}{T}<0$,矛盾!
  - 两热源 $T_1>T_2$, $T_1$吸热, $T_2$放热: $\Delta S=\dfrac{Q}{T_1}-\dfrac{Q}{T_2}<0$, 矛盾!


- 克劳修斯不等式的证明:
考虑多热源与单一热源 $T_0$由多个卡诺机联合:
  - 系统作循环过程,分别与热源 $T_i$交换 $Q_i$的热量
  - $T_0\to T_i$之间加上卡诺热机
  - $T_0\to Q_{0i}$
  - Carnot engines: $\dfrac{Q_{0i}}{T_0}=\dfrac{Q_i}{T_i}$
  - 对整个辅助系统: $T_i$,系统,热机不变, 热源 $T_0$ 放热,对外做功. 第一定律: $\sum\limits_{n=1}^n Q_{0i}=\sum\limits_{n=1}^n W_i$
  - 第二定律: 没有真正做功 $\sum\limits_{n=1}^n Q_{0i}=T_0 \sum\limits_{n=1}^n\dfrac{Q_i}{T_i}=\sum\limits_{n=1}^n W_i\leq0$

- 求熵变
  - 理想气体

$$
    \begin{aligned}
        dS &= \frac{1}{T}(dU+pdV)(第一定律)\\
         &= C_V\frac{dT}{T}+nR\frac{dV}{V}(第二类曲线积分)\\
        S_f-S_i &= C_vln\frac{T_f}{T_i}+nRln\frac{V_f}{V_i}\\
        S &= C_vlnT+nRlnV+S_0\\
        状态函数: S(T,V) &= C_vlnT+nRlnV+S_0\\
    \end{aligned}
$$
- - - Free expansion from $V\to2V(T=const)$:用熵作为状态函数来求: $\Delta S=nRln2>0$, irreversible
  - 热库reservior $\Delta S=\displaystyle\int\dfrac{dQ}{T}=\dfrac{\Delta Q}{T}$吸热熵增,放热熵减
  - 由准静态过程连接的状态: $\Delta S=\displaystyle\int_i^f\dfrac{dQ}{T},dQ=C_pdT\ /\ C_VdT$
  - 由不可逆过程联系的: 找到相应的可逆过程(如不可逆的自由膨胀转化为等温过程) $\Delta S=\dfrac{1}{T}\int pdV=nRln\dfrac{V_f}{V_i}$
  - 混合: $\Delta S=\displaystyle\int_{T_1}^{T_f}\frac{m_1c_1dT}{T}+\int_{T_2}^{T_f}\frac{m_2c_2dT}{T}$
     - 吉布斯佯谬: 相同气体混合

- 再探功与热
  - 做功: 有广义距离: 电热丝,搅拌,微波炉等; 
  - 但这些功只能转化为热,熵也就增加了$\Rightarrow$耗散功; 只要有耗散,就不可逆
- 熵的微观解释: $S=k_BlnW, W$: 微观状态数
  - 自由膨胀到两倍体积: $N$个粒子, $W=2^NW_0,\ \Delta S=k_BNln2$
  - 熵: 广延量: 微观状态用乘法原理计算, $lnW$可加
  - 习题 $(12.9)$:棋盘密度最大:平衡状态


### 12.4 热力学势
- 内能的计算
$$
    \begin{aligned}
        dQ &= TdS\\
        dU &= TdS-pdV+\mu dn\\
        &(fundamental\ equation\ of\ thermodynamics)\\
        &(\mu dn代表与外界的物质交换,\ \mu指化学势)\\
        \big(\dfrac{\partial U}{\partial S}\big)_{V,n} &= T,
        \big(\dfrac{\partial U}{\partial V}\big)_{S,n} = -p,
        \big(\dfrac{\partial U}{\partial n}\big)_{S,V} =\mu\\
        U是广延量:&\\
        &U(\lambda S,\lambda V, \lambda n)=\lambda U(S,V,n)\\
        两边对\lambda求导数:&\\
        &\big(\dfrac{\partial U}{\partial (\lambda S)}\big)S+\big(\dfrac{\partial U}{\partial (\lambda V)}\big)+\big(\dfrac{\partial U}{\partial (\lambda n)}\big)_n=U\\
        令\lambda=1:&\\
        &U=TS-pV+\mu n

    \end{aligned}
$$
欧拉齐次函数定理:设 $f(x_1,x_2,\cdots,x_n)$是$k$次函数,
$$
    \begin{aligned}
        f(\lambda x_1,\lambda x_2,\cdots,\lambda x_n) &= \lambda^kf(x_1,x_2,\cdots,x_n)\\
        \sum\limits_{n=1}^n \frac{\partial f}{\partial(\lambda x_i)}\frac{\partial(\lambda x_i)}{\partial \lambda} &=k\lambda^{k-1}f(x_1,x_2,\cdots,x_n)\\
        令\lambda=1,得&\\ \sum\limits_{n=1}^n \frac{\partial f}{\partial x_i}x_i&=kf(x_1,x_2,\cdots,x_n) \\
    \end{aligned}
$$
- 其他热力学势的引入
$$
    \begin{aligned}
        dU &= TdS-pdV-Vdp+Vdp+\mu dn\\
        d(U+pV) &= TdS+Vdp+\mu dn\equiv dH\\&(\sim reaction\ heat, enthopy)\\
        % &= \\
        % &= \\
        dU &= TdS-pdV+\mu dn-TdS-SdT\\
        d(U-TS) &= -SdT-pdV+\mu dn\equiv dF\\&(\sim useful\ work,\ Helmholtz\ free\ energy)\\
        d(U-TS+pV) &=-SdT+Vdp+\mu dn\equiv dG \\
         &(Gibbs\ free\ energy) \\
        G&=F+pV=H-TS(free\ enthopy)\\
        F&=U-TS
    \end{aligned}
$$
Legendre变换: 
$$
    \begin{aligned}
        df &= udx+vdy,\ 是x与y的函数\\
        g &= f-ux\\
        dg &= df-udx-xdu\\
         &= udx+vdy-udx-xdu\\
         &=-xdu+vdy, 是u与y的函数
    \end{aligned}
$$
- - 化学势的求法: $\mu= \big(\dfrac{\partial G}{\partial n}\big)_{T,p}$,摩尔吉布斯自由能

$$
    \begin{aligned}
        G &= \big(\dfrac{\partial G}{\partial n}\big)_{T,p}n=\mu n\\
        dG &= nd\mu+\mu dn\\
        nd\mu &=-SdT+Vdp \\
        d\mu &= -S_mdT+V_mdp\\
        &(S_m:摩尔熵,V_m:摩尔体积)\\
    \end{aligned}
$$
- 麦克斯韦关系

$$
    \begin{aligned}
    U(S,V,n)&=TS-pV+\mu n\\
        \frac{\partial}{\partial p}(\frac{\partial G}{\partial T}) &=\frac{\partial}{\partial T}(\frac{\partial G}{\partial p})=\frac{\partial^2G}{\partial T\partial p} \\
        -\big(\dfrac{\partial S}{\partial p}\big)_{T,n} &= \big(\dfrac{\partial V}{\partial T}\big)_{p,n}\\
        &(也可从全微分理解)\\
        dU &= TdS-pdV\\
         &=T\Big[\big(\dfrac{\partial S}{\partial T}\big)_VdT+\big(\dfrac{\partial S}{\partial V}\big)_TdV-pdV\Big] \\
         由dF=-SdT-pdV,结合&麦克斯韦关系:\\
         &=T\Big[\big(\dfrac{\partial S}{\partial T}\big)_VdT+\big(\dfrac{\partial p}{\partial T}\big)_VdV-pdV\Big] \\
         考虑C_V=T \big(\dfrac{\partial S}{\partial T}\big)_V:&\\
         &=C_VdT+T\big(\dfrac{\partial p}{\partial T}\big)_VdV-pdV\\
         \big(\dfrac{\partial U}{\partial V}\big)_T&=T \big(\dfrac{\partial p}{\partial T}\big)_V-p
    \end{aligned}
$$
- Criteria of thermodynamics equilibrium

$$
    \begin{aligned}
         \Delta S_t&=\Delta S+\Delta S_0=\Delta S-\dfrac{\Delta Q}{T_0}\\ &where\ Q\ is\ released\ to\ the\ system \\
         &=\Delta S-\frac{\Delta U-\Delta W-\mu\Delta n}{T_0}\geq0 \\
        \Delta U &\leq T_0\Delta S+\Delta W+\mu \Delta n \\
        (\Delta U)_{S,V,n}&\leq0\\
        \Delta F &= \Delta(U-TS)\leq -S\Delta T-p\Delta V+\mu\Delta n\\
        (\Delta F)_{T,V,n}&\leq0\\
        \Delta G&=\Delta(F=pV)\leq -S\Delta T+V\Delta p+\mu\Delta n\\
        (\Delta G)_{T,p,n}&\leq0
    \end{aligned}
$$
- 热力学势的物理意义
  - $(\Delta H)_p=\Delta U+p\Delta V=\Delta Q$,化学反应中等压过程的反应热. $\Delta H>0$: endothermic 吸热; $\Delta H<0$: exothermic 放热
  - 等温最大功与亥姆霍兹自由能

$$
    \begin{aligned}
        \Delta S_t &= \Delta S+\Delta S_r\\
         &= \Delta S-\frac{\Delta Q}{T_0}\geq0\\
         \Delta Q&=\Delta U-\Delta W \\
         \Delta W&\geq\Delta U-T_0\Delta S =\Delta F\\
         \Delta W_{对外}=-\Delta W&\leq-\Delta F
    \end{aligned}
$$
- - 额外功与吉布斯自由能
