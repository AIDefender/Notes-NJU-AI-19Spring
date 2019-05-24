<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>

## 极限
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
## 空间解几
- 求曲线$x^2+y^2+z^2=6,x+y+z=0$在(1,-2,1)处的切线方程
  
  直线的方向向量:$(\frac{dx}{dx},\frac{dy}{dx},\frac{dz}{dx})$

  两式对x求偏导:$2x+2y\frac{dy}{dx}+2z\frac{dz}{dx}=0$

  $1+\frac{dy}{dx}+\frac{dz}{dx}=0$

  带入数值,求出$\frac{dy}{dx},\frac{dz}{dx}$
  - 不一定要写出参数方程再做 把他们看成$x$的函数

- 求椭球面$\frac{x^2}{a^2}+\frac{y^2}{b^2}+\frac{z^2}{c^2}=1$在$M(x_0,y_0,z_0)$点的切平面方程

  法向量:$(F_x,F_y,F_z),$即$(\frac{2x}{a^2},\frac{2y}{b^2},\frac{2z}{c^2})$

  故切平面方程为$\frac{2x_0}{a^2}(x-x_0)+\frac{2y_0}{b^2}(y-y_0)+\frac{2z_0}{c^2}(z-z_0)=0$

## 函数极值
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

## 计算重积分
- $I=\displaystyle\iint\limits_D\sqrt{1-y^2}dxdy$
  - 注意偶函数的对称性
- $I=\displaystyle\int_0^1dy\int_y^0\frac{y}{\sqrt{1+x^3}}dx$
  - 交换积分次序:$I=\displaystyle\int_0^1dx\int_0^x\frac{y}{\sqrt{1+x^3}}dy=\int_0^1\frac{x^2}{2\sqrt{1+x^3}}dx$
- 求曲面$z=xy,z=0,x+y=1$所围立体的体积
  - $I=\displaystyle\iint\limits_Ddxdy\int_0^{xy}dz$