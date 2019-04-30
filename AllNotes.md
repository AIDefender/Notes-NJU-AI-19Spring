<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>
# 数学分析笔记:2019春学期下半学期
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



## 4.25习题课
### 极限
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
### 空间解几
- 求曲线$x^2+y^2+z^2=6,x+y+z=0$在(1,-2,1)处的切线方程
  
  直线的方向向量:$(\frac{dx}{dx},\frac{dy}{dx},\frac{dz}{dx})$

  两式对x求偏导:$2x+2y\frac{dy}{dx}+2z\frac{dz}{dx}=0$

  $1+\frac{dy}{dx}+\frac{dz}{dx}=0$

  带入数值,求出$\frac{dy}{dx},\frac{dz}{dx}$
  - 不一定要写出参数方程再做 把他们看成$x$的函数

- 求椭球面$\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}=1$在$M(x_0,y_0,z_0)$点的切平面方程

  法向量:$(F_x,F_y,F_z),$即$(\frac{2x}{a^2},\frac{2y}{b^2},\frac{2z}{c^2})$

  故切平面方程为$\frac{2x_0}{a^2}(x-x_0)+\frac{2y_0}{b^2}(y-y_0)+\frac{2z_0}{c^2}(z-z_0)=0$

### 函数极值
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

### 计算重积分
- $I=\displaystyle\iint\limits_D\sqrt{1-y^2}dxdy$
  - 注意偶函数的对称性
- $I=\displaystyle\int_0^1dy\int_y^0\frac{y}{\sqrt{1+x^3}}dx$
  - 交换积分次序:$I=\displaystyle\int_0^1dx\int_0^x\frac{y}{\sqrt{1+x^3}}dy=\int_0^1\frac{x^2}{2\sqrt{1+x^3}}dx$
- 求曲面$z=xy,z=0,x+y=1$所围立体的体积
  - $I=\displaystyle\iint\limits_Ddxdy\int_0^{xy}dz$

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
\iiint\limits_\Omega\frac{\partial{R}}{\partial{z}}dxdydz=\iint\limits_{D_{xy}}dxdy\int_{z_1(x,y)}^{z_2(x,y)}\frac{\partial R}{\partial z}dz=\iint\limits_{D_{xy}}R(x,y,z_2(x,y))-R(x,y,z_1(x,y))dxdy\\
而\oiint\limits_{\Sigma}Rdxdy=\iint\limits_{\Sigma_上}+\iint\limits_{\Sigma_下}=\iint\limits_{D_{xy}}R(x,y,z_2(x,y))-\iint\limits_{D_{xy}}R(x,y,z_1(x,y))dxdy\\
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

证明:
$$
希望把曲线积分(找参数方程)和曲面积分(设法投影)化到同一个东西

设\Sigma:z=z(x,y),将\Sigma投影到xOy面,得到D_{xy},记其边界线为L:x=x(t),y=y(t).\\
而L为\Gamma在xOy面的投影,故\Gamma:x=x(t),y=y(t),z=z(x(t),y(t))\\
于是曲线积分\oint\limits_\Gamma P(x,y,z)dx=\oint_LP(x,y,z(x,y))dx,注意这是平面的曲线积分,由格林公式\\
=\iint\limits_{D_{xy}}-\frac{\partial P}{\partial y}dxdy,这样就把曲线积分化成了二重积分.\\
=\iint\limits_{D_{xy}}-(\frac{\partial P}{\partial x}\times0+\frac{\partial P}{\partial y}+\frac{\partial P}{\partial z}\frac{\partial z}{\partial x})dxdy,由复合求导\\
考虑dxdy=cos\gamma dS,dzdx=cos\beta dS,往证\\
\frac{\partial z}{\partial y}cos\gamma dS=-cos\beta dS\\
只需证\frac{\partial z}{\partial y}cos\gamma =-cos\beta\\
考虑\Sigma:z(x,y)-z=0,\vec{n}=(z_x,z_y,-1),易见\frac{cos\beta}{cos\gamma}=-z_y=\frac{\partial z}{\partial y},从而证明了原命题.
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