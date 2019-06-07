<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>
# 数学分析笔记:2019春学期下半学期

<!-- TOC -->

- [数学分析笔记:2019春学期下半学期](#数学分析笔记2019春学期下半学期)
    - [期中考前空间解析几何知识点整理](#期中考前空间解析几何知识点整理)
        - [向量](#向量)
        - [空间平面和直线](#空间平面和直线)
        - [空间曲面的方程](#空间曲面的方程)
    - [几类积分的联系](#几类积分的联系)
        - [高斯公式](#高斯公式)
        - [斯托克斯公式](#斯托克斯公式)
    - [第七章 无穷级数](#第七章-无穷级数)
        - [7.1 数项级数](#71-数项级数)
            - [7.1.1 常数项级数](#711-常数项级数)
            - [7.1.2 正项级数($a_n\geq0$)](#712-正项级数a_n\geq0)
            - [7.1.3 一般级数](#713-一般级数)
        - [7.2 函数项级数](#72-函数项级数)
            - [7.2.1 函数列的一致收敛性](#721-函数列的一致收敛性)
            - [7.2.2 函数项级数](#722-函数项级数)
        - [7.3 幂级数](#73-幂级数)
            - [函数的幂级数展开](#函数的幂级数展开)
    - [第四章 常微分方程](#第四章-常微分方程)
        - [4.1 可分离变量的微分方程](#41-可分离变量的微分方程)
        - [4.4 一阶线性微分方程](#44-一阶线性微分方程)
        - [4.5 可降阶的高阶微分方程](#45-可降阶的高阶微分方程)
        - [4.6 高阶线性微分方程](#46-高阶线性微分方程)
        - [4.7 常系数齐次线性方程](#47-常系数齐次线性方程)
        - [4.8 常系数非齐次微分方程](#48-常系数非齐次微分方程)
    - [习题课](#习题课)
        - [4.25习题课](#425习题课)
        - [5.10习题课](#510习题课)
        - [5.24 习题课](#524-习题课)

<!-- /TOC -->

## 期中考前空间解析几何知识点整理
### 向量
- 混合积:$\boldsymbol{a,b,c}$坐标为$(a_1,b_1,c_1),(a_2,b_2,c_2),(a_3,b_3,c_3)$则
$$\boldsymbol{a}\times \boldsymbol{b}\cdot \boldsymbol{c}=
\left|\begin{array}{}
    a_1 & a_2 & a_3 \\
    a_2 & b_2 & a_3 \\
    a_3 & b_3 & c_3
\end{array}\right|$$

- 三向量共面:混合积为零

### 空间平面和直线
- 点到平面的距离: $P_1(x_1,y_1,z_1)$到平面$\pi:Ax+By+Cz+D=0$的距离为:
$$d=\frac{|Ax_1+By_1+Cz_1+D|}{\sqrt{A^2+B^2+C^2}}$$
- 直线的标准方程:
$$\frac{x-x_0}{X}=\frac{y-y_0}{Y}=\frac{z-z_0}{Z}$$
其中$(X,Y,Z)$称为方向系数
- 两直线相交:设直线$\ell_i$过点$M_i(x_i,y_i,z_i)$,方向向量为$(X_i,Y_i,Z_i)(i=1,2)$,则他们相交的充要条件为:
$$\left|\begin{array}{}
    x_2-x_1 & X_1 & X_2\\
    y_2-y_1 & Y_1 & Y_2 \\
    z_2-z_1 & Z_1 & Z_2
\end{array}
\right|=0 $$ 
且他们不相交或重合
- $\ell$与$\pi$平行的充要条件:$AX+BY+CZ=0$且$\ell$上有一点不在$\pi$上
- 异面直线间的距离:
$$d=\frac{|\overrightarrow{M_1M_2}\cdot v_1\times v_2|}{|v_1\times v_2|}$$
(考虑投影到公垂线段上)
### 空间曲面的方程
- 圆柱面: 半径为$r$,母线方向为$\boldsymbol{v}(l,m,n)$,对称轴$\ell_0$过点$M_0(x_0,y_0,z_0)$,则$M(x,y,z)$在此圆柱面上的充要条件是
$$\frac{|\overrightarrow{MM_0}\times \boldsymbol{v}|}{|\boldsymbol{v}|}=r$$
(注意叉乘)
- 圆锥面:设轴的方向向量为$\boldsymbol{v},则$$|cos<\overrightarrow{M_0M},\boldsymbol{v}>|=cos\alpha$




## 几类积分的联系
### 高斯公式
设空间区域$\Omega$由分片光滑的闭曲面$\Sigma$构成,则
$$
\iiint\limits_\Omega(\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z})dxdydz=\oiint\limits_\Sigma Pdydz+Qdzdx+Rdxdy\\
其中P,Q,R:一阶连续可微
$$
证明:
$$
设\Omega的下表面\Sigma_下:z=z_1(x,y),上表面\Sigma_上:z=z_2(x,y)\\

利用三重积分的先一后二和曲面积分的计算,考虑
\iiint\limits_\Omega\frac{\partial{R}}{\partial{z}}dxdydz的穿线,有\\
\begin{aligned}
\iiint\limits_\Omega\frac{\partial{R}}{\partial{z}}dxdydz&=\iint\limits_{D_{xy}}dxdy\int_{z_1(x,y)}^{z_2(x,y)}\frac{\partial R}{\partial z}dz\\
&=\iint\limits_{D_{xy}}R(x,y,z_2(x,y))-R(x,y,z_1(x,y))dxdy\\

而\oiint\limits_{\Sigma}Rdxdy&=\iint\limits_{\Sigma_上}+\iint\limits_{\Sigma_下}\\
&=\iint\limits_{D_{xy}}R(x,y,z_2(x,y))-\iint\limits_{D_{xy}}R(x,y,z_1(x,y))dxdy\\
\end{aligned}\\
从而证明了原命题.
$$

使用Gaussian公式:常加入与坐标平面平行的平面组成封闭平面

eg1:
$$
求I=\iint\limits_\Sigma y^2zdxdy-xzdydz+x^2ydzdx\\
\Sigma:z=x^2+y^2,x^2+y^2=1及坐标面所围曲线的外侧
$$
注意:画好积分区域 主要在第一卦限

so1:
$$
I=\iiint\limits_\Omega(-z+x^2+y^2)dxdydx=\int_o^{\frac{\pi}{2}}d\theta\int_0^1rdr\int_0^{r^2}(-z+r^2)dz
$$

### 斯托克斯公式
考虑三维空间的曲面$\Sigma$,其边界为$\Gamma$,曲线方向取正向,曲面方向取右手螺旋,我们有
$$
\oint_\Gamma P(x,y,z)dx+Q(x,y,z)dy+R(x,y,z)dz=\iint\limits_\Sigma(\frac{\partial R}{\partial y}-\frac{\partial Q}{\partial z})dydz+(\frac{\partial P}{\partial z}-\frac{\partial R}{\partial x})dzdx+(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})dxdy
$$

注意以$\Gamma$为边界的曲面$\Sigma$可能有若干个,可以选择一个比较合适的(有时甚至选择球面比较方便)

行列式记法:
$$
=\iint\limits_\Sigma
\left|\begin{array}{}
    dydz & dzdx & dxdy \\
    \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z} \\
     P& Q &R  \\
\end{array}\right|

$$

证明:
$$
希望把曲线积分(找参数方程)和曲面积分(设法投影)化到同一个东西\\
设\Sigma:z=z(x,y),将\Sigma投影到xOy面,得到D_{xy},记其边界线为L:x=x(t),y=y(t).\\
而L为\Gamma在xOy面的投影,故\Gamma:x=x(t),y=y(t),z=z(x(t),y(t))\\
$$
于是曲线积分
$$
\begin{aligned}
\oint\limits_\Gamma P(x,y,z)dx&=\oint_LP(x,y,z(x,y))dx\\
注意这是平面的曲线积分,由格林公式
&=\iint\limits_{D_{xy}}-\frac{\partial P}{\partial y}dxdy,这样就把曲线积分化成了二重积分\\
由复合求导&=\iint\limits_{D_{xy}}-(\frac{\partial P}{\partial x}\times0+\frac{\partial P}{\partial y}+\frac{\partial P}{\partial z}\frac{\partial z}{\partial x})dxdy,\\
考虑dxdy&=cos\gamma dS,dzdx=cos\beta dS,往证\\
\frac{\partial z}{\partial y}cos\gamma dS&=-cos\beta dS\\
只需证\frac{\partial z}{\partial y}cos\gamma &=-cos\beta\\
考虑\Sigma:z(x,y)-z=0,\vec{n}=(z_x,z_y,-1),易见\frac{cos\beta}{cos\gamma}=-z_y=\frac{\partial z}{\partial y},从而证明了原命题.
\end{aligned}
$$
启示:重视基本含义,基本计算方法

eg2:
$$
求I=\oint\limits_\Gamma(y-z)dx+(z-x)dy+(x-y)dz\\
\Gamma:x^2+y^2=a^2与\frac{x}{a}+\frac{z}{b}=2(a>0,b>0)的交线,方向为从x轴正向看去是逆时针
$$
注意画图的技巧:把zOx面作为纸面

sol2:
$$
考虑\Sigma:\frac{x}{a}+\frac{z}{b}=1,其投影D_{xy}:x^2+y^2\leq a^2\\
I=\iint\limits_\Sigma(-1-1)dydz+(-1-1)dzdx+(-1-1)dxdy\\
=-2\iint\limits_\Sigma(dydz+dzdx+dxdy),它是曲面在坐标面上的投影的面积\\
考虑\Sigma在yOz面上的投影:a^2(1-\frac{z}{b})^2+y^2=a^2,即\frac{y^2}{a^2}+\frac{(z-b)^2}{b^2}=1\\
于是I=-2(\pi ab+0+\pi a^2)
$$



## 第七章 无穷级数
### 7.1 数项级数
#### 7.1.1 常数项级数
- 定义:
  - 给定 $\left\{a_n\right\},a_1+a_2+\dots+a_n+\dots$,或 $\sum\limits_{n=1}^\infty a_n$,简记为 $\sum a_n$
  - 研究问题:收敛/发散
  - 级数的收敛:定义**部分和** $S_n=a_1+a_2+\dots+a_n$,构成**数列 $\{S_n\}$**,其敛散性与原级数的敛散性相同; 研究级数的收敛性需要通过研究数列的收敛性.
  - 收敛级数的余项: $R_n=S-S_n$,其中 $S$为级数的和
- 判断敛散性
  - Cauchy收敛准则:

  $给定\{b_n\},b_n\to b \Leftrightarrow \forall\epsilon>0,\exist N>0,s.t.\forall p \in \mathbb{Z}_+,有对n>N,|b_{n+p}-b_n|<\epsilon$
  - **级数的Cauchy收敛准则**: 

  $级数\sum a_n,部分和S_n收敛 \Leftrightarrow\forall\epsilon>0,\exist N>0,s.t.\forall p \in \mathbb{Z}_+,有对n>N,|S_{n+p}-S_n|=|a_{n+1}+a_{n+2}+\dots+a_{n+p}|<\epsilon$. 要习惯这种 $\epsilon\delta$语言进行证明

  - 调和级数
    - 知道发散,知道发散的阶
    - 应用:随机树:每次只选一个叶子节点向下分,研究随机一个叶子节点的层数: $lnn$
- 收敛级数的性质
  - 线性性
  - 任意改动有限项不影响级数的收敛性
  - $\sum\limits_{n=1}^\infty a_n$收敛 $\Rightarrow$ $\lim\limits_{n\to\infty}a_n=0($证明: $\lim\limits_{n\to\infty}S_n-S_{n+1}=0)$
  - $\sum\limits_{n=1}^\infty a_n$ 收敛 $\Rightarrow$ 任意加括号后级数收敛(反之不成立,反例: $\sum\limits_{n=1}^\infty (-1)^n$)(利用逆否命题:加括号发散 $\Rightarrow$原级数发散)

证明:


$$
    \begin{aligned}
      S_n&=a_1+a_2+\dots+a_n\\
      S_k'&=b_1+b_2+\dots+b_k\\
         &=a_1+a_2+\dots+a_{n_k} \\
         &=S_{n_k},其为S_n的子列,故收敛 \\
    \end{aligned}
$$
Th1:
$$
    ln(1+n)\leq S_n\leq 1+lnn,其中S_n=\sum\limits_{i=1}^n\frac{1}{i}
$$

证明:
$$
对x\in[i,i+1],\frac{1}{i+1}\leq\frac{1}{x}\leq\frac{1}{i}\\
积分,得\frac{1}{i+1}\leq\int_i^{i+1}\frac{1}{x}dx\leq\frac{1}{i}\\
累加,得\sum\limits_{i=1}^n\frac{1}{i+1}\leq\sum\limits_{i=1}^n\int_i^{i+1}\frac{1}{x}dx\leq\sum\limits_{i=1}^n\frac{1}{i}
\\于是S_n\geq\int_1^{n+1}\frac{1}{x}dx=ln(n+1)\\
且\sum\limits_{i=1}^{n-1}\frac{1}{i+1}\leq\int_1^n\frac{1}{x}dx=lnn,则S_n\leq1+lnn.
$$

eg1:

$$
    证明:\sum\limits_{n=1}^\infty\frac{1}{n^2}收敛
$$

证明:
$$
任意\epsilon>0,\exist N=\frac{1}{\epsilon},对\forall p\in\mathbb{Z}_+,当n>N时,\\
    \begin{aligned}
         &|\frac{1}{(n+1)^2}+\frac{1}{(n+2)^2}+\dots+\frac{1}{(n+p)^2}|\\&\leq |\frac{1}{n}-\frac{1}{n+1}+\dots+\frac{1}{n+p-1}-\frac{1}{n+p}|\\
         &=|\frac{1}{n}-\frac{1}{n+p}| \\
         &\leq\frac{1}{n}<\epsilon. \\
    \end{aligned}

由Cauchy收敛准则,级数收敛

$$  

eg2
$$
    \begin{aligned}
         \sum\limits_{n=2}^\infty \frac{1}{\sqrt{n}+1}-\frac{1}{\sqrt{n}-1}  &=  \sum\limits_{n=2}^\infty( \frac{1}{\sqrt{n}+1}-\frac{1}{\sqrt{n}-1} )\\
         &=  \sum\limits_{n=2}^\infty \frac{-2}{n-1}\\
    \end{aligned}
    故其发散

$$

created on 2019-05-09

#### 7.1.2 正项级数($a_n\geq0$)

- 性质
  - $S_n$单调,收敛只需证其有界:
$$
 \sum\limits_{n=1}^\infty a_n收敛 \Leftrightarrow S_n\leq M ,即部分和有上界
 \tag{1}
$$
- 审敛法
  - 比较判别法(根本)
$$
    若 \sum\limits_{n=1}^\infty a_n 与 \sum\limits_{n=1}^\infty b_n为正项级数,且\exist N, \forall n>N, s.t.a_n\leq b_n,则\\1.\sum\limits_{n=1}^\infty b_n收敛\Rightarrow \sum\limits_{n=1}^\infty a_n收敛\\
    2.\sum\limits_{n=1}^\infty a_n发散\Rightarrow \sum\limits_{n=1}^\infty b_n 发散
    \tag{2}
$$
证明:考虑 $(1)$易见
- - 极限形式
$$
     
     
     若 \sum\limits_{n=1}^\infty a_n 与 \sum\limits_{n=1}^\infty b_n为正项级数,且\lim\limits_{n\to\infty}\frac{a_n}{b_n}=\ell\\
$$
$$
    \begin{aligned}
     i)&0<\ell<\infty:敛散性相同\\
     ii)&\ell=0:与(2)相同   \\ 
     iii)&\ell=\infty:与(2)相反
    \end{aligned}
$$
证明: 考虑$\ell-\epsilon\leq\dfrac{a_n}{b_n}\leq\ell+\epsilon$,取 $\epsilon=\dfrac{\ell}{2}$即得

eg1
$$
    \sum\limits_{n=1}^\infty \frac{1}{2^n-n^2}
$$
考虑比较级数 $\sum\limits_{n=1}^\infty \dfrac{1}{2^n}$即可
- - 比值判别法(d'Alembert)
$$
    \sum\limits_{n=1}^\infty a_n为正项级数,若\exist N, \forall n>N,有\\
    i)\frac{a_{n+1}}{a_n}<1:\sum\limits_{n=1}^\infty 收敛\\
    ii)\frac{a_{n+1}}{a_n}\geq1:\sum\limits_{n=1}^\infty a_n发散\\
$$
证明$i)$:
$$
    \begin{aligned}
        a_n &= \frac{a_n}{a_{n-1}}\frac{a_{n-1}}{a_{n-2}}\dots\frac{a_{N+2}}{a_{N+1}}a_{N+1}\\
         &\leq q^{n-N-1}a_{N+1} \\
    \end{aligned}
    其中q\leq1.故原级数收敛.

$$
$ii)$ :考虑必要条件

极限形式:
$$
    \begin{aligned}
        i) & \lim\limits_{n\to\infty}\frac{a_{n+1}}{a_n}=q<1:\sum\limits_{n=1}^\infty a_n收敛 \\
        ii)& \lim\limits_{n\to\infty}\frac{a_{n+1}}{a_n}=q>1:\sum\limits_{n=1}^\infty a_n发散\\
        iii) & \lim\limits_{n\to\infty}\frac{a_{n+1}}{a_n}=q=1:\sum\limits_{n=1}^\infty a_n不能确定\\
    \end{aligned}
$$
$iii)$的反例:$\sum\limits_{n=1}^\infty \dfrac{1}{n}与\sum\limits_{n=1}^\infty \dfrac{1}{n^2}$

若 $\lim\limits_{n\to\infty}\dfrac{a_{n+1}}{a_n}$不存在:考虑上极限

eg2
$$
    \sum\limits_{n=1}^\infty a_n=\frac{1}{2}+\frac{2\times5}{1\times5}+\dots+\frac{2\times5\times8\times\dots\times(3n-2)}{1\times5\times9\times\dots\times(4n-1)}+\cdots
$$
sol2
$$
    \lim\limits_{n\to\infty}\frac{a_{n+1}}{a_n}=\frac{3}{4}<1 收敛
$$
- - 根式判别法(Cauchy)
$$
    \sum\limits_{n=1}^\infty a_n为正项级数,若\exist N, \forall n>N,有
$$
$$
    \begin{aligned}
        i) &\sqrt[n]{a_n}\leq\ell<1 :\sum\limits_{n=1}^\infty a_n收敛 \\
        ii) &\sqrt[n]{a_n}>1: \sum\limits_{n=1}^\infty a_n 发散 \\
    \end{aligned}
$$
证明:$i)a_n\leq\ell^n,\sum\limits_{n=N+1}^\infty a_n\leq \sum\limits_{n=N+1}^\infty \ell^n$,收敛

$ii):a_n>1,则\lim\limits_{n\to\infty}a_n\geq1$,考虑必要条件,发散

极限形式
$$
    \sum\limits_{n=1}^\infty a_n,\lim\limits_{n\to\infty}\sqrt[n]{a_n}=\ell
$$

$$
    \begin{aligned}
        i)&\ell<1: \sum\limits_{n=1}^\infty a_n收敛 \\
        ii) &\ell>1: \sum\limits_{n=1}^\infty a_n发散 \\
        iii) &\ell=1: 不能确定
    \end{aligned}
$$
反例: $a_n=\dfrac{1}{n}$和 $\dfrac{1}{n^2}$

eg3
$$
    \sum\limits_{n=1}^\infty \frac{2+(-1)^n}{2^n}
$$
sol3
$$
    \lim\limits_{n\to\infty} \sqrt[n]{a_n}=\lim\limits_{n\to\infty}\frac{\sqrt[n]{2+(-1)^n}}{2}<1,收敛 
$$
- - 根式与比值判别法的联系:比值判别法有效,根值判别法一定有效
  - trick:有阶乘:用比值;有n次方:根式

$$
    \lim\limits_{n\to\infty}\frac{a_{n+1}}{a_n}=q\leq1\Rightarrow\lim\limits_{n\to\infty}\sqrt[n]{a_n}=q\leq1
$$
证明:
$$
\begin{aligned}
    a_n&=\frac{a_n}{a_{n-1}}\frac{a_{n-1}}{a_{n-2}}\cdots\frac{a_2}{a_1}a_1\\
    \sqrt[n]{a_n}&=\sqrt[n]{\frac{a_n}{a_{n-1}}\frac{a_{n-1}}{a_{n-2}}\cdots\frac{a_2}{a_1}a_1}\to q
\end{aligned}
$$
其中利用了结论 若$\{a_n\}\to a$,则 $\{\sqrt[n]{a_1a_2\cdots a_n}\}\to a$

eg4
$$
    \sum\limits_{n=1}^\infty \frac{x^n}{1+x^{2n}}
$$
sol4 
用根式判别法易见;比值判别法也未尝不可

eg5
$$
    \sum\limits_{n=1}^\infty \frac{(n!)^2}{(2n)!}, \sum\limits_{n=1}^\infty \frac{n^2}{(2+\frac{1}{n})^n}
$$
要利用结论 $\displaystyle\lim\limits_{n\to\infty}.^n\sqrt{n^k}\to1$

- - 积分判别法(有时在$q=1$时可用): 对于
$$
    f(x):[1,+\infty]\to(0,+\infty)且单调递减,则
    \sum\limits_{n=1}^\infty f(n) 与 \int_1^\infty f(x) 同收敛或发散
$$
证明:
$$
    f(n)=\int_{n-1}^nf(n)dx\\
    而对于f(x)\in[n-1,n],f(n)\leq f(x)\leq f(n-1)\\
    从而f(n)=\int_{n-1}^nf(n)dx\leq \int_{n-1}^nf(x)dx\leq \int_{n-1}^n f(n-1)dx=f(n-1) \\
    则\sum\limits_{n=1}^\infty f(n)\leq \int_1^\infty f(x)dx\leq \sum\limits_{n=1}^\infty f(n-1).\\
    再利用比较审敛法易见.
$$
eg6 
$$
    \sum\limits_{n=1}^\infty \frac{1}{n(lnn)^p}
$$
用积分判别法

#### 7.1.3 一般级数
- 交错级数: $\sum\limits_{n=1}^\infty (-1)^{n-1}a_n(a_n>0)$
  - Leibniz: 若 $i):a_n\downarrow ii)a_n\to0(n\to\infty)$,则 $\sum\limits_{n=1}^\infty (-1)^{n-1}a_n$收敛

证明: 采用Cauchy判别法 $\forall \epsilon>0,\exist N s.t. \forall n>N,p\in\mathbb{N}_+,$

$p=2k:$

$$
\begin{aligned}
    
&|a_{n+1}-a_{n+2}+\cdots+(-1)^{p+1}a_{n+2p}|\\
&=a_{n+1}-(a_{n+2}-a_{n+3})-\cdots-(a_{n+2k-2}-a_{n+2k-1})-a_{n+2k}\\
&\leq a_{n+1}<\epsilon(利用a_n\to0和单调性)
\end{aligned}
$$
$p=2k-1:$同理
- 绝对收敛: $\sum\limits_{n=1}^\infty |a_n|$收敛
  - 性质: 绝对收敛$\to$收敛

证明1:
$$
    0\leq a_n+|a_n|\leq2|a_n|\\
    \sum\limits_{n=1}^\infty a_n+|a_n|\leq \sum\limits_{n=1}^\infty 2|a_n|.则易见
$$
证明2: 用Cauchy 见书.
- 条件收敛: $\sum\limits_{n=1}^\infty a_n$收敛,但不绝对收敛.


eg1:判断是否绝对收敛:
$$
    \sum\limits_{n=1}^\infty \frac{\alpha^n}{n!},\sum\limits_{n=1}^\infty (-1)^{n-1}ln(1+\frac{1}{n})
$$

tip: 小不等式 在学习理论证明中有用.(看来这里面也用了不少放缩)
$$
    \begin{aligned}
        ln(1+x) &\leq x(x>-1)\\
        ln(1+x) &\geq x-\frac{x^2}{4}(0<x<1)\\
        1+x &\leq e^x\\
    \end{aligned}
    \tag{7.1.3.1}
$$
eg2:讨论敛散性(用上式):
$$
    \sum\limits_{n=1}^\infty \frac{(-1)^{n-1}}{n^p+(-1)^{n-1}}
$$

eg3:
$$
    f(x)\in C^2(-\delta,\delta),且 \lim\limits_{n \to0}\frac{f(x)}{x}=0. 证明: \sum\limits_{n=1}^\infty f(\frac{1}{n})绝对收敛.
$$
证明:
$$
    易见f(0)=0,f'(0)=0.由泰勒展开:
    \\ f(\frac{1}{n})=f''(\xi)\frac{1}{2n^2},\xi\in[0,\frac{1}{n}]\\
    当\frac{1}{n}=x<\frac{\delta}{2}时,f''(x)有界,|f''(x)|\leq M,则\\
    |f(\frac{1}{n})|\leq\frac{M}{2n^2}.则易见原命题成立.
$$

Th: $f(x)在(-\delta,\delta)$二阶可导. $a_n=f(\dfrac{1}{n})$.则 $\sum\limits_{n=1}^\infty a_n$绝对收敛 $\Leftrightarrow f(0)=f'(0)=0$

eg4
$$
    \sum\limits_{n=1}^\infty \frac{1}{n}-ln(1+\frac{1}{n})
$$
用 $(7.1.3.1)$即可.
- 绝对收敛的性质
  - 可任意重排,都收敛,和一样.(条件收敛不可,考虑调和级数)
  - 设级数 $\sum\limits_{n=1}^\infty a_n$与$\sum\limits_{n=1}^\infty b_n$都绝对收敛,和为 $A, B$, 则级数 $\sum\limits_{n=1}^\infty \sum\limits_{n=1}^k a_kb_{n-k+1}$ 收敛于 $AB$(事实上乘积项按任意次序排列均可)

- (Abel) $\{a_n\}$单调有界, $\sum\limits_{n=1}^\infty b_n$ 收敛, 则 $\sum\limits_{n=1}^\infty a_nb_n$ 收敛.
- (Dirichlet) $\{a_n\}$单调且 $a_n\to0$, $\sum\limits_{n=1}^\infty b_n$ 部分和有界, 则 $\sum\limits_{n=1}^\infty a_nb_n$ 收敛.(可依此证明 Leibniz)

eg:
$$
    \sum\limits_{n=1}^\infty \frac{cosnx}{n}, \sum\limits_{n=1}^\infty \frac{sinnx}{n}
$$

### 7.2 函数项级数
#### 7.2.1 函数列的一致收敛性
- Intuition: 求极限与求积分,求导数能不能交换次序
- 设函数列 $f_1(x),f_2(x),\cdots,f_n(x),\cdots,x\in I$. 如果 $\forall x_0\in D, \lim\limits_{n \to\infty}f_n(x_0)=f(x)$, 则称 $\{f_n\}$在$D$上收敛于 $f$. 若 $D$ 包含所有收敛点,则称其为函数列的收敛域

$\forall \epsilon>0, \exist N=N(\epsilon,x)>0, \forall n>N,|f_n(x)-f(x)|<\epsilon$ (注意与不同$x$取值有关)


eg1: 求 $f_n(x)=x^n$的收敛域

sol1: $|x|<1: f_n(x)\to0,n\to\infty; x=1:收敛; x=-1:不收敛; |x|>1: 发散$.故收敛域为 $(-1,1]$
- 讨论: $f_n(x)$每一项都连续,可导,可积....,极限是否有相应的性质

<br>

- 一致收敛性$f_n(x)\rightrightarrows f(x)$: 设函数列 $f_1(x),f_2(x),\cdots,f_n(x),\cdots,x\in D$,$f_n(x)\rightrightarrows f(x)\Leftrightarrow\forall \epsilon>0, \exist N=N(\epsilon)>0, \forall n>N,|f_n(x)-f(x)|<\epsilon, \forall x\in D$

- 反: $\exist \epsilon>0, \forall N, n>N时,\exist x_n ,|f_n(x_n)-f(x_n)|\geq\epsilon$

eg2: 证明 $f_n(x)=x^n$非一致收敛

sol2:
$$
    |f_n(x)-f(x)|=|x^n|,let\ x_n\ be\ (1-\frac{1}{n})^n\\
    |f_n(x)-f(x)|=1-\frac{1}{n}\geq\frac{1}{2}.
    
$$

- 几何意义: $n>N$时, $y=f_n(x)$被限制在一个小区间之内
- Cauchy判别法: $f_n(x)\rightrightarrows f(x)\Leftrightarrow\forall \epsilon>0, \exist N=N(\epsilon)>0, \forall n,m>N,|f_n(x)-f_m(x)|<\epsilon,\forall x\in D$
- 余项判别法:  $D上,f_n(x)\rightrightarrows f(x)\Leftrightarrow \lim\limits_{n \to\infty}\sup\limits_{x\in D}|f_n(x)-f(x)|=0$

eg3: $f_n(x)=nxe^{-nx^2}$

sol3:
$$
    f(x)=0.\\
    \sup\limits_{x\in D}f_n(x)=\frac{nx}{e^{nx^2}},求导求最大值=\frac{n}{\sqrt{2n}}e^{-\frac{1}{2}}\to\infty\not=0.
$$
故不一致收敛

<br>

- 性质1: $D上,f_n(x)\rightrightarrows f(x) \Rightarrow \lim\limits_{x \to x_0} \lim\limits_{n \to\infty}f_n(x)=\lim\limits_{n \to\infty}\lim\limits_{x \to x_0}f_n(x)=\lim\limits_{x \to x_0}f(x)$
- 性质2: $D上,f_n(x)\rightrightarrows f(x) \Rightarrow \forall n\geq1,f_n(x)$连续,则 $f(x)$连续.
- 性质3: $D上,f_n(x)\rightrightarrows f(x) \Rightarrow \forall n\geq1,f_n(x)$连续,则 $f(x)$可积,且

$$
    \int_a^b \lim\limits_{n \to\infty}f_n(x)=\lim\limits_{n \to\infty}\int_a^bf_n(x)
$$
- 性质4: $f_n(x)在D上可导,f'_n(x)\rightrightarrows f'(x) \Rightarrow \{f_n(x)\}$的极限函数可导,且

$$
    \frac{d}{dx}\lim\limits_{n \to\infty}f_n(x)=\lim\limits_{n \to\infty}\frac{d}{dx}f_n(x)
$$

eg4:验证性质: 

$$
f_n(x)=\dfrac{2x+n}{x+n},x\in[0,b]\\
f_n(x)=x-\frac{x^n}{n}, x\in[0,1]
$$
sol4:

1. 用余项 

#### 7.2.2 函数项级数 
- $\sum\limits_{n=1}^\infty u_n(x)$. 研究部分和函数 $S_n(x)= \sum\limits_{k=1}^n u_k(x)$, 构成函数列 $S_1(x),S_2(x),\cdots,S_n(x),\cdots$. $S_n(x_0)$收敛,称 $\sum\limits_{n=1}^\infty u_n(x)$在 $x=x_0$处收敛. 在集合上收敛,收敛域类似定义.若部分和函数一致收敛,则级数 $\sum\limits_{n=1}^\infty u_n(x)$一致收敛.
- 和函数 $\sum\limits_{n=1}^\infty u_n(x)=S(x)=$ $\lim\limits_{n \to\infty}S_n(x)$  

eg1: $\sum\limits_{n=1}^\infty x^n$的收敛域

- 柯西判别法: 同7.1.1; 必要条件: 通项 $u_n(x)\rightrightarrows0$
- 余项判别法: 同7.1.1;

eg2: $\sum\limits_{n=1}^\infty x^n$在 $x\in(-1,1)$上的一致收敛性

sol2: 当出现 $\sup\limits_{x\in(-1,1)}\dfrac{x^{n+1}}{1-x}$时,无需求导得最小值,只需令 $x=\dfrac{n}{n+1},\sup\limits_{x\in(-1,1)}\dfrac{x^{n+1}}{1-x}\geq \dfrac{(\frac{n}{n+1})^{n+1}}{\frac{1}{n+1}}=(n+1)(1-\dfrac{1}{n+1})^{n+1}\to\infty$,故不一致收敛

- 维尔斯特拉斯判别法: 若 $\sum\limits_{n=1}^\infty M_n$收敛,且 $\forall n\in \mathbb{N}_+\forall x\in D,|u_n(x)|\leq M_n$,则 $\sum\limits_{n=1}^\infty u_n(x)$一致收敛

Intuition: 将函数的上界换为数列

<br>

- 性质
  - 连续性: 若 $u_n(x)$连续,则 $\sum\limits_{n=1}^\infty u_n(x)$连续
  - 逐项可积:  若 $u_n(x)$连续,则 $\sum\limits_{n=1}^\infty u_n(x)$可积,且 $\displaystyle\int_0^x \sum\limits_{n=1}^\infty u_n(x)dx= \sum\limits_{n=1}^\infty \int_0^x u_n(x)dx$
  - 逐项可导: $u_n(x)\in C^{(1)}, \sum\limits_{n=1}^\infty u'_n(x)$一致收敛,则 $S(x)$可导,且 $S'(x)= (\sum\limits_{n=1}^\infty u_n(x))'= \sum\limits_{n=1}^\infty u'_n(x)$
  - 内闭一致收敛: 在区间内任意一个闭区间一致收敛,则上面的性质都可用

eg3: $u_n(x)=\dfrac{1}{n^3}ln(1+n^2x^2)$. 证明: $\sum\limits_{n=1}^\infty u_n(x)$在 $[0,1]$一致收敛

sol3:

Weierstrass: $S_n(x)= \sum\limits_{k=1}^n \dfrac{1}{k^3}ln(1+x^2k^2)\leq\sum\limits_{k=1}^n \dfrac{1}{k^3}ln(1+k^2)$. 考虑 $M_n=\dfrac{1}{n^3}ln(1+n^2)$,易见原命题成立.

同时, $u'_n(x)\leq\dfrac{1}{n^2}$,故 $\sum\limits_{n=1}^\infty u'_n(x)$一致收敛,可知 $S'(x)$

eg4: 证明: $ln(1+x)=x-\dfrac{x^2}{2}+\dfrac{x^3}{3}+\cdots+(-1)^n\dfrac{x^n}{n}$

sol4:

恒成立: $1+x=1-x+x^2-x^3+\cdots+(-1)^{n+1}x^n+\cdots$

两边积分: $\displaystyle\int_0^x \dfrac{1}{1+x}dx=\displaystyle\int_0^x1-x+x^2-x^3+\cdots+(-1)^{n+1}x^n+\cdots$,化为逐项积分易见.

注意为何符合条件



### 7.3 幂级数
- $\sum\limits_{n=1}^\infty a_nx^n$
- $Th(Abel):$
  - $i)$ $\sum\limits_{n=1}^\infty a_nx^n$在 $x=x_0$处收敛,则 $\forall x. |x|<|x_0|,\sum\limits_{n=1}^\infty a_nx^n$收敛
  - $ii)$ $\sum\limits_{n=1}^\infty a_nx^n$在 $x=x_0$处发散,则 $\forall x. |x|>|x_0|,\sum\limits_{n=1}^\infty a_nx^n$发散

证明:

(i) $\sum\limits_{n=1}^\infty a_nx^n$=$\sum\limits_{n=1}^\infty a_nx_0^n(\dfrac{x^n}{x_0^n})$. 由 $\sum\limits_{n=1}^\infty a_nx_0^n$收敛,知 $a_nx_0^n\leq M$有界,又 $(\dfrac{x}{x_0})^n<1$则易见收敛.

(ii) 反证

- 收敛半径$R$ :阻隔收敛与发散 关于原点对称

- 幂级数的收敛性判别法
  - 比式 $\rho= \lim\limits_{n \to\infty}|\dfrac{a_{n+1}}{a_n}|$
    - $0<\rho<\infty: R=\dfrac{1}{\rho}$
    - $\rho=0: R=\infty$
    - $\rho=\infty: R=0$

证明: 用正项级数的比式判别法

$\lim\limits_{n \to\infty}|\dfrac{u_{n+1}}{u_n}|=|x| \lim\limits_{n \to\infty}|\dfrac{a_{n+1}}{a_n}|$,比较其与$1$的大小关系
- - 根式 $\rho= \lim\limits_{n \to\infty}\sqrt[n]{|a_n|}$
    - $0<\rho<\infty: R=\dfrac{1}{\rho}$
    - $\rho=0: R=\infty$
    - $\rho=\infty: R=0$

eg1: 求 $\sum\limits_{n=1}^\infty \dfrac{x^n}{n^2}$的收敛域

sol1: 直接用比式判别法,多一个分情况讨论

eg2: $\sum\limits_{n=1}^\infty \dfrac{x^{2n}}{2^nn}$

注意: Strling 公式

$$
    n!\approx\sqrt{2\pi n}(\frac{n}{e})^n
$$

<br>

- 性质
  - 和函数在 $(-R,R)$连续
  - 若 $\sum\limits_{n=0}^\infty a_nx^n$在 $x=R/-R$收敛,则和函数 $S_n$在该点单边收敛
  - 收敛半径内,和函数可逐项求导,求积分
  - $\sum\limits_{n=0}^\infty a_nx^n$与 $\sum\limits_{n=1}^\infty a_nnx^{n-1}$及 $\sum\limits_{n=0}^\infty a_n\dfrac{1}{n+1}x^{n+1}$有相同的收敛半径

证明: $\forall x\in (-R,R),\exist y\in(-R,R),|x|<|y|. \sum\limits_{n=0}^\infty a_nnx^{n-1}=\sum\limits_{n=0}^\infty a_ny_n\dfrac{n}{y}\dfrac{x^{n-1}}{y^{n-1}}\leq \sum\limits_{n=0}^\infty M\dfrac{n}{y}\dfrac{x^{n-1}}{y^{n-1}}$.这是由于$\sum\limits_{n=0}^\infty a_nx^n$收敛,通项有界.用比式判别法易证其收敛.
- - $S(x)=\sum\limits_{n=0}^\infty a_nx^n$. $S(0)=a_0,S'(x)= \sum\limits_{n=0}^\infty na_nx^{n-1},S'(0)=a_1. a_n=\dfrac{S^{(n)}(0)}{n!}$

eg3 求 $\sum\limits_{n=1}^\infty (-1)^nn^2x^n$

sol1: 收敛半径: $(-1,1)$. 
$$
    \begin{aligned}
         S(x)&=x\sum\limits_{n=1}^\infty (-1)^nnnx^{n-1}=xg(x) \\
         \int_0^xg(t)dt&= \sum\limits_{n=1}^\infty (-1)^nnx^n=xf(x) \\
        \int_0^xf(t)dt &=\frac{-x}{1+x} \\
        求导,f(x) &=-\frac{1}{(1+x)^2},\int_0^xg(t)dt= -\frac{1}{x(1+x)^2}\\
        g(x)&=\cdots,S(x)=xg(x)
    \end{aligned}
$$

#### 函数的幂级数展开
- Taylor级数 $f(x)=f(x_0)+f'(x_0)(x-x_0)+\cdots+f^{(n)}(x_0)\dfrac{(x-x_0)^n}{n!}$

反例: 

$$
\begin{aligned}
    f(x)&=e^{-\frac{1}{x^2}},x\not=0\\
        &=0,x=0
    
\end{aligned}
$$
其求n阶导为0, $S(x)=0$.

- Th: 若 $f(x)$在  $x=x_0$处有任意阶导数, 且对$|x-x_0|<r, \lim\limits_{n \to\infty}R_n(x)=0,$则 $\forall x\in(x_0-r,x_0+r),f(x)=   \sum\limits_{n=1}^\infty f^{(n)}(x_0)\dfrac{(x-x_0)^n}{n!}$

余项的表达式: $R_n(x)=\dfrac{f^{(n+1)}(\xi)}{n!}x^{n+1}$    

eg4 求 $f(x)=ln(1-x)$的幂级数展开

sol4: 用求导等运算


## 第四章 常微分方程
### 4.1 可分离变量的微分方程
- 通解: 包括常数的解, 独立常数的个数与微分方程的阶相同.
- 可分离变量的微分方程(包括变量代换后可分离的)

eg1:
$$
    求\frac{dy}{dx}=3x^2y的通解.
$$
sol1:
$$
    当y\not=0时, \int\frac{1}{y}dy=\int3x^2dx+C, y=Ce^{x^3}(C\not=0)\\
    (通解,但不包括所有解)\\
    当y=0时,C=0;\ 故y=Ce^{x^3}
$$
- 齐次方程

$$
    \frac{dy}{dx}=F(x,y)=\phi(\frac{y}{x})\\
    令u=\frac{y}{x},y'_x=(ux)'=\frac{du}{dx}x+u=\phi(u)\\
    \frac{du}{\phi(u)-u}=\frac{1}{x}dx
$$
eg2:
$$
    (x+\sqrt{x^2+y^2})y'=y
$$
sol2:
$$
    x>0: (1+\sqrt{1+(\frac{y}{x})^2}\frac{dy}{dx}=\frac{y}{x}\\
    或: \frac{dx}{dy}=\frac{x+\sqrt{x^2+y^2}}{y}=\frac{x}{y}+\sqrt{1+(\frac{x}{y})^2}\\令 u=\frac{x}{y},\ x=uy,\frac{dx}{dy}=\frac{du}{dy}y+u=u+\sqrt{1+u^2}
$$
eg3:
$$
    y'=\frac{3x+2y+1}{4x+2y+2}
$$
线性代换,待定系数
### 4.4 一阶线性微分方程
- 形式: $y'+P(x)y=Q(x)$
  - $Q(x)\equiv0$ : 齐次; $y=Ce^{\int-P(x)dx}$
  - 非齐次: 常数变易法(想法: $C\to u(x)$, 令其为方程特解)
$$
    \begin{aligned}
        y' &= u'(x)e^{\int-P(x)dx}+u(x)e^{\int-P(x)dx}(-P(x))\\
         &= u'(x)e^{\int-P(x)dx}-yP(x)\\
        带入原方程: \frac{du}{dx}e^{\int-P(x)dx} &=Q(x)\ (yP(x)一定会被消掉) \\
        u &= \int Q(x)e^{\int P(x)dx}+C\\
        故y&=Ce^{\int-P(x)dx}+e^{\int-P(x)dx}\int Q(x)e^{\int P(x)dx}\\
        &=通解+特解
    \end{aligned}
$$
eg1
$$
    y'-\frac{2}{x+1}y=(x+1)^{\frac{2}{5}}
$$
eg2
$$
  y'=\frac{1}{x+y}  
$$
sol2:

法一: $u=x+y$, 可分离变量

法二: $\dfrac{dx}{dy}=x+y$一阶线性(反函数微分 常用)

eg3(略作变化)
$$
    f(x)=sinx-\int_0^xf(x-t)dt
$$
sol3:
$$
    \int_0^xf(x-t)dt=-\int_0^xf(x-t)d(x-t)=\int_0^xf(u)du;\ 可对x求导
$$
- 伯努利方程 $y'+P(x)y=Q(x)y^n$
$$
    \begin{aligned}
         y'+P(x)y&=Q(x)\\
        y^{-n}y'+P(x)y^{1-n}  &= Q(x)\\
         令z=y^{1-n},&z'=(1-n)y^{-n}y' \\
         z'+(1-n)P(x)z&= Q(x)(1-n)\\
         &(可照常求解)
    \end{aligned}
$$
eg4
$$
    y'+\frac{1}{x}y=alnx\cdot y^2
$$

### 4.5 可降阶的高阶微分方程
- $y^{(n)}=f(x)$ 求$n$次不定积分
- $y''=f(x,y')$: 令 $u=f'$

eg1
$$
    x>-1.\ g'(x)+g(x)-\frac{1}{1+x}\int_0^xg(t)dt=0.\ g(0)=1\\求: i)g'(x); ii) e^{-x}\leq g(x)\leq1, x\geq0
$$
sol:
$$
    证g(x)\geq e^{-x}: f(x)=g(x)-e^{-x}, 求f'(x)
$$
- $y''=f(y,y')$ : 令 $y'=P,y''=\dfrac{dP}{dx}=\dfrac{dp}{dy}\dfrac{dy}{dx}=\dfrac{dp}{dy}p,\Rightarrow pp'=f(y,p)$

### 4.6 高阶线性微分方程
$y^{(n)}+a_1(x)y^{(n-1)}+\cdots+a_n(x)y=f(x)$; $f(x)\equiv0$: 齐次
- 考虑 $y''+P(x)y'+Q(x)y=0$, 若 $y_1=y_1(x), y_2=y_2(x)$是它的解, 则 $y=C_1y_1+C_2y_2$也是它的解. 证明: 利用求导的线性性 $(Cy)''=Cy''$; &emsp; 到 $n$阶也成立
- 函数组线性相关: $k_1y_1(x)+k_2y_2(x)+\cdots+k_ny_n(x)\equiv0, s.t.\ k_1k_2\cdots k_n\not=0$
- $Liouville\ Th$: 若$y_1(x)$是 $y''+P(x)y'+Q(x)y=0$的解,则 $y_2(x)=y_1(x)\displaystyle\int\dfrac{exp(-\int p(x)dx)}{y_1^2(x)}dx$
- 非齐次的情况: $y''+P(x)y'+Q(x)y=f(x)$; &emsp; 若 $y^*=y^*(x)$是它的特解,且 $Y=Y(X)$是对应齐次方程的通解,则 $y=y^*+Y$也是原方程的解. 

### 4.7 常系数齐次线性方程
- $y''+py'+qy=0$; 试探: $y=e^{rx}\Rightarrow r^2e^{rx}+rpe^{rx}+qr^{rx}=(r^2+pr+q)e^{rx}\equiv0,r^2+pr+q=0$; 讨论其根的分布
  - $i) \Delta>0, r_1,r_2, y=C_1e^{r_1x}+C_2e^{r_2x}$
  - $ii) \Delta=0, y=e^{rx}(C_1+C_2x)$
  - $iii) \Delta<0, r_{1,2}=\dfrac{-p\plusmn i\sqrt{-\Delta}}{2}=\alpha\plusmn i\beta, y=e^{\alpha x}(C_1cos\beta x+C_2\sin\beta x)$

eg1:
$$
    y''-2y'+5=0
$$
sol1: 特征方程: $r^2-2r+5=0;\ r_{1,2}=1\plusmn2i;\ y=e^x(C_1cos2x+C_2sin2x)$

eg2:
$$
    z=f(e^xsiny)\ s.t.\ \big(\dfrac{\partial ^2z}{\partial x^2}\big)+\big(\dfrac{\partial ^2z}{\partial y^2}\big)=e^{2x}z. 求f(u)
$$
sol: 依次求二阶导, $\big(\dfrac{\partial ^2z}{\partial x^2}\big)=f''(u)e^{2x}sin^2y+f'(u)e^xsiny, \big(\dfrac{\partial ^2z}{\partial y^2}\big)=f''(u)e^{2x}cos^2y-f'(u)e^xsiny$
故 $f''(u)=f(u)$
- $n$阶的情况: $y^{(n)}+a_1y^{(n-1)}+\cdots+a_ny=0$; &emsp; 特征方程: $r^n+a_1r^{n-1}+\cdots+a_n=0$
  - $i). r$为$k$重实根: $e^{rx}(C_0+C_1x+\cdots+C_{k-1}x^{k-1})$
  - $ii). r$为$k$重复根: $e^{\alpha x}\big[(C_0+C_1x+\cdots+C_{k-1}x^{k-1})cos\beta x+(D_0+D_1x+\cdots+D_{k-1}x^{k-1})sin\beta x\big]$

### 4.8 常系数非齐次微分方程
- $y^{(n)}+a_1(x)y^{(n-1)}+\cdots+a_n(x)y=f(x)$. 可做的情形: $f(x)=e^{\lambda x}P_n(x)$或 $f(x)=e^{\alpha x}(R^{(\ell)(x)}cos\omega x+R^{(r)}(x)sin\omega x)$
- $y^{(n)}+a_1(x)y^{(n-1)}+\cdots+a_n(x)y=e^{\lambda x}P_n(x)$. 
  - 二次的情形:

假设 $y^*=e^{\lambda x}Q(x)$,则 $y'^*=e^{\lambda x}(\lambda Q(x)+Q'(x)),y''^*=\cdots$,带入整理,得 $Q''(x)+(2\lambda+p)Q'(x)+(\lambda^2+p\lambda+q)Q(x)=P_n(x)$

i)$\lambda^2+p\lambda+q\not=0$,待定系数: $Q(x)=b_0+b_1x+\cdots+b_nx^n$,比较系数易得.

ii) $\lambda^2+p\lambda+q=0,2\lambda+p\not=0: Q(x):n+1$次,待定系数: $Q(x)=b_0x+b_1x^2+\cdots+b_nx^{n+1}$

iii) $\lambda^2+p\lambda+q=0,2\lambda+p=0:$待定系数: $Q(x)=b_0x^2+b_1x^3+\cdots+b_nx^{n+2}$

eg1:
$$
    y''+2y'-3y=(3-4x)e^x
$$
sol1:先求通解. $r_1=1,r_2=3$.注意 $\lambda=1$,是特征方程的解但不是重根,故设 $y^*=e^x(Ax+Bx^2)$,带入整理易得.
- - $n$阶的情形 $y^*=e^{\lambda x}x^kQ_n(x)$,其中 $Q_n(x)$与$P_n(x)$次数相同,$k$是$\lambda$为齐次方程特征方程的根的重数
- $f(x)=e^{\alpha x}(R^{(\ell)}(x)cos\beta x+R^{(r)}(x)sin\beta x)$,特解为 $y^*=e^{\alpha x}x^k(R_1(x)cos\beta x+R_2(x)sin\beta x),R_1(x),R_2(x)$的次数为 $max(\ell,r)$,且 $\alpha+\beta i$为 $k$ 重特征根

eg2 
$$
    y''+y=xcos2x
$$
sol2: $y''+y=(xcos2x+0sin2x)e^{0x}$.求对应齐次方程的特征根: $\plusmn i$. $\alpha+\beta i=2i$不是特征根. 故令 $y^*=(Ax+B)cos2x+(Cx+D)sin2x$,解出系数即得.

eg3
$$
    y^{(4)}+2y''+y=sinx
$$





## 习题课
### 4.25习题课
- 极限
<!-- 1. $$\lim\limits_{$\begin{array}
    x \to \infty\\y\to\infty
\end{array}$
 
  }
 $$ -->
1. $\lim\limits_{(x,y) \to (0,0)}x^y$不存在:
    
    两个累次极限不相等

- $f(x,y)=\frac{x^3+y^3}{x^2+y}((x,y)\to(0,0))$
  
  令$y=x$: $f(x,y)\to0$

  令$y=x^2-x^3$: $f(x,y)=\frac{x^3+(x^2-x^3)^3}{x^3}=1+o(1)\to1$
- 证偏导数不连续:把除该点外的偏导数用公式求出
- 空间解几
  - 求曲线$x^2+y^2+z^2=6,x+y+z=0$在(1,-2,1)处的切线方程
  
  直线的方向向量:$(\frac{dx}{dx},\frac{dy}{dx},\frac{dz}{dx})$

  两式对x求偏导:$2x+2y\frac{dy}{dx}+2z\frac{dz}{dx}=0$

  $1+\frac{dy}{dx}+\frac{dz}{dx}=0$

  带入数值,求出$\frac{dy}{dx},\frac{dz}{dx}$
  - 不一定要写出参数方程再做 把他们看成$x$的函数

  - 求椭球面$\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}=1$在$M(x_0,y_0,z_0)$点的切平面方程

  法向量:$(F_x,F_y,F_z),$即$(\frac{2x}{a^2},\frac{2y}{b^2},\frac{2z}{c^2})$

  故切平面方程为$\frac{2x_0}{a^2}(x-x_0)+\frac{2y_0}{b^2}(y-y_0)+\frac{2z_0}{c^2}(z-z_0)=0$

- 函数极值
  - 给定$f(x,y)=2(y-x^2)^2-\frac{1}{7}x^7-y^2$

  (1)求$(x,y)$的极值

  (2)证明:沿(0,0)点的每条直线,(0,0)点都是定义在该直线上的函数$f(x,y)$的极小值点

  (1)      
    $A:f_{xx}^{''},B:f_{xy}^{''},C:f_{yy}^{''}$

    $(0,0)$点:$B^2-AC>0$不能确定是否是极值点,故令$x=0,f(x,y)=y^2$,此时$f(0,0)\leq f(x,y)$,为极小值 

    再令$y=x^2$,$f(x,x^2)=-\frac{1}{7}x^7-x^4\leq0,f(0,0)$为极大值

  (2)       
    令$y=kx(k>0),f(x,kx)=x^2(k^2-4kx-2x^2-\frac{1}{7}x^5)$,当$x\to0$时,$f(x,kx)$恒大于0,$f(0,0)为极小值点$

    若$k=0,f(x,0)=x^4(2-\frac{1}{7}x^3)>0,f(0,0)$为极小值点

- 计算重积分
  - $I=\displaystyle\iint\limits_D\sqrt{1-y^2}dxdy$
    - 注意偶函数的对称性
  - $I=\displaystyle\int_0^1dy\int_y^0\frac{y}{\sqrt{1+x^3}}dx$
    - 交换积分次序:$I=\displaystyle\int_0^1dx\int_0^x\frac{y}{\sqrt{1+x^3}}dy=\int_0^1\frac{x^2}{2\sqrt{1+x^3}}dx$
  - 求曲面$z=xy,z=0,x+y=1$所围立体的体积
    - $I=\displaystyle\iint\limits_Ddxdy\int_0^{xy}dz$



### 5.10习题课
- 第一型曲线积分 
- 第二型曲线积分
  - $\displaystyle\int_{\partial \Omega}Pdx+Qdy=\int_{\partial\Omega}(P,Q)\cdot\vec{n}ds$,其中 $\vec{n}$为曲线在 $(x,y)$点的法向量.
- 曲面面积 &emsp;设 $f:D\to\mathbb{R}$为连续可微函数, $D\subset\mathbb{R}^{n-1}$,则 $graph(f)$为 $\mathbb{R}^n$中超曲面,其面积公式为
$$
\sigma=\int_D  \sqrt{1+||\nabla f||^2}  
$$
- 第二型曲面积分 &emsp;设 $\Sigma$为 $\mathbb{R}^3$中可定向的曲面,其与定向相容的参数表示为
$$
    r(u,v)=(x(u,v),y(u,v),z(u,v)),(u,v)\in\Omega.
$$
则对于定义在 $\Sigma$上的连续向量值函数 $(P,Q,R)$,定义其曲面积分为
$$
    I=\int_\Omega (P\frac{\partial(y,z)}{\partial(u,v)}+Q\frac{\partial(z,x)}{\partial(u,v)}+R\frac{\partial(x,y)}{\partial(u,v)})dudv
$$
eg
$$
    \Phi=\int_\Sigma x^2dy\wedge dz+y^2dz\wedge dx+x^2dx\wedge dy
$$
其中 $\Sigma$为球面 $(x-a)^2+(y-b)^2+(z-c)^2=R^2$,方向为外侧

sol: 进行球坐标变换,计算
$$
    \frac{\partial(y,z)}{\partial(\phi,\theta)}=R^2sin^2\phi cos\theta,等等
$$
考虑定向: $\vec{n}=(x_0-a,y_0-b,z_0-c)=(Rsin\phi cos\theta,Rsin\phi sin\theta,Rcos\phi)$,其与 $\vec{N}$方向相同.

法二: 考虑 
$$
    \vec{v}=(P,Q,R)\\\Phi=\int_\Sigma\vec{v}\cdot\vec{n}d\sigma
$$

- 格林公式
  - 诱导定向: 从法向量转向切向量是逆时针
  - 平面分部积分公式(在偏微分方程中有用)
- 高斯公式
  - 散度: $\vec{X}=(P,Q,R),div \vec{X}=(\dfrac{\partial P}{\partial x},\dfrac{\partial Q}{\partial y},\dfrac{\partial R}{\partial z})$.则高斯公式的散度形式为

$$
    \int_\Omega div\vec{X}dxdydz=\int_{\partial\Omega}\vec{X}\cdot\vec{n}d\sigma
$$
其中 $\vec{n}$为边界曲面的单位外法向量

eg2: 设 $C$为平面上连续可微的闭曲线, $\vec{v}$为固定的向量,证明:
$$
    \int_C\vec{v}\cdot\vec{n}ds=0
$$
其中 $\vec{n}$为 $C$的单位外法向量

sol2: 在 $x(t),y(t)$点,$\vec{n}ds=(\dfrac{y'(t)}{\sqrt{x'^2+y'^2}},\dfrac{-x'(t)}{\sqrt{x'^2+y'^2}})\sqrt{x'^2+y'^2}dt=(dy,-dx)$. 带入原式,用Green公式立得.

eg3:计算积分

$$
    I=\int_{\partial\Omega}(y-z)dx+(z-x)dy+(x-y)dz
$$
其中 $\Omega$为八分之一单位球面(第一卦限),方向为外侧诱导定向  
  
用Stokes公式, $I=\displaystyle-2\int_\Omega dy\wedge dz+dz\wedge dx+dx\wedge dy$,用投影.

### 5.24 习题课
- $\dfrac{1}{n(n+1)(n+2)}=\dfrac{1}{2}(\dfrac{1}{n(n+1)}-\dfrac{1}{(n+1)(n+2)})$, 易于消项
- 注意高尉不等式 $ln(1+x)\geq x-\dfrac{x^2}{4}(0<x<1)$
- $(lnn)^{lnn}=e^{lnnlnlnn}=n^{lnlnn}$
- $\sqrt[n]{n}-1=e^{\frac{1}{n}lnn}-1\sim \dfrac{1}{n}lnn$
- $2^{n^2}=2^{n\times n}=(2^n)^n=2^n\times2^n\times\cdots\times2^n$ 熟悉指数的指数