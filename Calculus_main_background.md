# 1. 高等数学背景知识和辅助组件

## 1.1. 函数特征

* 奇偶性
    * 可以证明,只有一个函数既奇又偶
        $$f(x) = 0$$
    * 可以证明,对于一个奇函数,有
        $$f(0) = 0$$
* 渐近线
    * 两侧水平渐近线可以不同,但最多只有两条水平渐近线;
        $$y = tan^{-1}(x)$$
    * 渐近线可以穿过函数图像;
        $$y = \frac{sin(x)}{x}$$
* 反函数的图像可以通过让原函数的关于直线$y = x$做轴对称得到

## 1.2. 三角学

### 1.2.1. 基础三角函数

1. 三角恒等式

    1. 倍角公式
    $$cos^2(x) = \frac{1}{2}(1+cos(2x))$$
    $$sin^2(x) = \frac{1}{2}(1-cos(2x))$$
    两者可以正向使用也可以反向使用 , 在反向使用升幂时, 如果遇到开根一般需要加上绝对值之后讨论符号.
    一般用于处理单独的$trig^2(x)$或者$1\pm cos(u)$类式子.
    2. 毕达哥拉斯恒等式/勾股定理恒等式
    $$sin^2(x)+cos^2(x) = 1$$
    $$tan^2(x)+1 = sec^2(x)$$
    $$1+cot^2(x) = csc^2(x)$$
    它们一般用于处理类似$1\pm trig^2(x)$类型的式子和分母上有$1\pm trig(x)$(需要乘共轭表达式)的式子.
    3. 积化和差公式
    $$cos(A)cos(B) = \frac{1}{2}(cos(A-B)+cos(A+B))$$
    $$sin(A)sin(B) = \frac{1}{2}(cos(A-B)-cos(A+B))$$
    $$sin(A)cos(B) = \frac{1}{2}(sin(A-B)+sin(A+B))$$
    它们一般用于处理三角函数的乘积式.
    4. 余弦定理
    $$c^2 = a^2+b^2-2abcos(\theta_c)$$
    已知角$\theta$对边c的平方等于其两临边的平方和减去两者与$\theta$的余弦值积的两倍.
    5. 正弦定理
    $$\frac{sin\theta_a}{a} = \frac{sin\theta_b}{b} = \frac{sin\theta_c}{c} = 2r = D $$
    各角正弦值和其对边的比值相同且比值为外接圆直径.
    6. 三角形面积公式
    $$S_{\Delta ABC} = \frac{1}{2}absin\theta_c = \frac{1}{2}bcsin\theta_a = \frac{1}{2}acsin\theta_b $$

2. 三角函数的命名

* ***co-*** 前缀表示互余(complementary),代表着两个函数值相等时,内部的角相加为$\pi /2$.

3. 和角公式 & 倍角公式

* 和角公式
$$sin(A+B) = sinAcosB + cosAsinB$$
$$cos(A+B) = cosAcosB - sinAsinB$$
* 对加减号取反,可以得到另外两个和角公式
* 将 $A = B$ 代入上式,可以得到倍角公式

### 1.2.2. 双曲(三角)函数

1. 六个双曲(三角)函数
$$ sinh(x) = \frac{e^x + e^{-x}}{2}             $$
$$ cosh(x) = \frac{e^x - e^{-x}}{2}             $$
$$ tanh(x) = \frac{e^x + e^{-x}}{e^x - e^{-x}}  $$
$$ csch(x) = \frac{2}{e^x - e^{-x}}             $$
$$ sech(x) = \frac{2}{e^x + e^{-x}}             $$
$$ coth(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}  $$

2. 可以证明,对于双曲三角函数,有类似勾股定理的公式如下:
$$ sinh^2(x) - cosh^2(x) = 1 $$
只不过中间的加号改成了减号.
当然,通过在等号两侧同时除以$sinh^2(x)$ 或者 $cos^2(x)$ , 也可以得到关于tanh(x
) & sech(x) 或者 coth(x) & csch(x)之间的类似关系.

### 1.2.3. 反(基础)三角函数

1. 反三角函数是用截断法对原三角函数限定定义域之后得到的一类函数

2. 它们的定义域,值域和奇偶性如下:

$$ arcsin(x),x\in[-1,1],y\in[-\frac{\pi}{2},\frac{\pi}{2}]                                      , 奇函数$$
$$ arccos(x),x\in[-1,1],y\in[0,\pi]                                                             , 非奇非偶函数$$
$$ arctan(x),x\in R,y\in(-\frac{\pi}{2},\frac{\pi}{2})                                          , 奇函数$$
$$ arsec(x),x\in(-\infty,-1]\cup[1,\infty),y\in[0,\pi] \backslash \{ \frac{\pi}{2} \}           , 非奇非偶函数$$
$$ arccsc(x),x\in (-\infty,-1]\cup[1,\infty),y\in[-\frac{\pi}{2},\frac{\pi}{2}]\backslash\{0\}  , 奇函数$$
$$ arccot(x),x\in R , y\in(0,\pi)                                                               , 非奇非偶函数$$

4. 计算反三角函数+三角函数的嵌套式子  
由于反三角函数是有截断的,所以在使用反函数与原函数相消的特性时,对于反三角函数在外侧的情形,需要注意反函数的值域限制带来的问题.
例如,对于
$$sin^{-1}(sin(\frac{13\pi}{10}))$$
由于$\frac{13\pi}{10}$超出了反正弦函数的值域,所以必须使用三角函数的周期性将正弦函数内的数值映射到$[-\frac{\pi}{2},\frac{\pi}{2}]之间,所以最后实际处理的是$$sin^{-1}sin(-\frac{3\pi}{10})$.

### 1.2.4. 反双曲(三角)函数
由于一般用不到反双曲三角函数,所以这里只简单使用反函数的导数与原函数的导数的对应关系来求解反双曲三角函数的导数:
1. 六个反双曲三角函数的导数如下:
$$\frac{d}{dx}sinh^{-1}(x) = \frac{1}{\sqrt{x^2+1}} , x \in R$$
$$\frac{d}{dx}cosh^{-1}(x) = \frac{1}{\sqrt{x^2-1}} , x > 1  $$
$$\frac{d}{dx}tanh^{-1}(x) = \frac{1}{1-x^2} , x > 1\ or\ x < -1$$
$$\frac{d}{dx}csch^{-1}(x) = -\frac{1}{|x|\sqrt{1+x^2}} , x \neq 0$$
$$\frac{d}{dx}sech^{-1}(x) = -\frac{1}{x\sqrt{1-x^2}} , 0 < x < 1$$
$$\frac{d}{dx}coth^{-1}(x) = \frac{1}{1-x^2} , x>1\ or\ x<-1$$

## 1.3. 连续性与可导性的应用

### 1.3.1. 连续性带来的两个定理

* 介值定理
一般用于证明方程有解.(将所有项置于等号左侧,成一函数)
另外,可以用介值定理证明,奇数次多项式一定有至少一个解,因为在两侧的无穷远处奇数次多项式的函数值必有不同符号(首项决定).

* 最大值与最小值定理
证明连续函数在闭区间上至少有一个最大值和一个最小值.

### 1.3.2. 可导性

* 切线
切线可以与函数图像相交不止一次,但是在切点附近只能有切点一个交点.

* 不可导
证明不可导只需要证明左导数不等于右导数即可.

* 求导公式
$$f'(x) = \lim_{h \to 0} \frac{f(x+h)-f(x)}{h}$$

* 可导性与连续性
前者是后者的充分条件,后者是前者的必要条件.

## 1.4. 反函数相关技术

### 1.4.1. 反函数的判定

1. 对于连续区间 $(a,b)$ 上的函数 $f(x)$ ,判定其有反函数时的条件如下:
    * 对于所有在(a,b)中的x,$f'(x) > 0$或者$f'(x) < 0$恒成立;.
    * 对于所有在(a,b)中的x,$f'(x)>=0$恒成立或$f'(x)<=0$恒成立且对于有限个数的x,f'(x) = 0;

### 1.4.2. 反函数的求导

一般的,函数f(x)的反函数$f^{-1}(x)$的导数可以用如下方式求解:
$$ \frac{df^{-1}(x)}{dx} = \frac{1}{f'(y)} $$

## 1.5. 微分/积分表

$$
\begin{array}{lcl}
\frac{d}{dx}x^a = ax^{a-1} & \int x^adx = \frac{x^{a+1}}{a+1}+C(a\neq -1)\\
\frac{d}{dx}ln(x) = \frac{1}{x} & \int \frac{1}{x}dx = ln|x|+C\\
\frac{d}{dx}e^x = e^x & \int e^xdx = e^x +C\\
\frac{d}{dx}b^x = b^xln(b) & \int b^xdx = \frac{b^x}{ln(b)}+C\\
\frac{d}{dx}sin(x) = cos(x) & \int cos(x)dx = sin(x)+C\\
\frac{d}{dx}cos(x) = -sin(x) & \int sin(x)dx = -cos(x)+C\\
\frac{d}{dx}tan(x) = sec^2(x) & \int sec^2(x)dx = tan(x)+C\\
\frac{d}{dx}csc(x) = -csc(x)cot(x) & \int csc(x)cot(x)dx = -csc(x)+C\\
\frac{d}{dx}sec(x) = sec(x)tan(x) & \int sec(x)tan(x)dx = sec(x)+C\\
\frac{d}{dx}cot(x) = -csc^2(x) & \int csc^2(x)dx = -cot(x)+C\\
\frac{d}{dx}arcsin(x) =  \frac{1}{\sqrt{1-x^2}},-1< x <1 & \int \frac{1}{\sqrt{1-x^2}}dx = arcsin(x)+C\\
\frac{d}{dx}arcsec(x) =  \frac{1}{|x|\sqrt{x^2-1}},x<-1\ or\ x>1 & \int \frac{1}{|x|\sqrt{x^2-1}}dx = arcsec(x)+C\\
\frac{d}{dx}arctan(x) =  \frac{1}{1+x^2}, x \in R & \int \frac{1}{1+x^2}dx = arctan(x)+C\\
\frac{d}{dx}arccos(x) = -\frac{1}{\sqrt{1-x^2}},-1< x <1 & \int \frac{1}{\sqrt{1-x^2}}dx = -arccos(x)+C\\
\frac{d}{dx}arccsc(x) = -\frac{1}{|x|\sqrt{x^2-1}},x<-1\ or\ x>1 & \int \frac{1}{|x|\sqrt{x^2-1}}dx = -arccsc(x)+C\\
\frac{d}{dx}arccot(x) = -\frac{1}{1+x^2},x \in R & \int \frac{1}{1+x^2}dx = -arccot(x)+C\\
\frac{d}{dx}sinh(x) = cosh(x) & \int cosh(x)dx = sinh(x)+C\\
\frac{d}{dx}cosh(x) = sinh(x) & \int sinh(x)dx = cosh(x)+C\\
\frac{d}{dx}tanh(x) = sech^2(x) & \int sech^2(x)dx = tanh(x)+C\\
\frac{d}{dx}csch(x) = -csch(x)coth(x) & \int csch(x)coth(x)dx = -csch(x)+C\\
\frac{d}{dx}sech(x) = -sech(x)tanh(x) & \int sech(x)tanh(x)dx = -sech(x)+C\\
\frac{d}{dx}coth(x) = -csch^2(x) & \int csch^2(x)dx = -coth(x)+C\\
\end{array}
$$

## 1.6. 约化公式表

$$
\begin{array}{lcl}
I_n =tan^n(x) = \frac{1}{n-1}tan^{n-1}(x)-I_{n-2}
\end{array}
$$

## 1.7. 麦克劳林级数表
$$
\begin{array}{lcl}
    1. & \frac{1}{1-x} = 1+x+x^2+x^3+\dots ,& -1< x < 1\\
    2. & ln(1+x) = x-\frac{x^2}{2}+\frac{x^3}{3}-\frac{x^4}{4}+\dots & -1< x \leq 1\\
    3. & arctan(x) = x-\frac{x^3}{3}+\frac{x^5}{5}-\frac{x^7}{7}+\dots & -1\leq x \leq 1\\
    4. & e^x = 1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+\frac{x^4}{4!}+\dots &\\
    5. & sin(x) = x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\dots & \\
    6. & cos(x) = 1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\frac{x^8}{8!}+\dots &\\
    5. & sinh(x) = x+\frac{x^3}{3!}+\frac{x^5}{5!}+\frac{x^7}{7!}+\dots & \\
    6. & cosh(x) = 1+\frac{x^2}{2!}+\frac{x^4}{4!}+\frac{x^6}{6!}+\frac{x^8}{8!}+\dots &\\
    9. & (1+x)^p = 1+\dbinom{p}{1}x+\dbinom{p}{2}x^2+\dbinom{p}{3}x^3+\dbinom{p}{4}x^4+\dots&\\
\end{array}
$$
*9* 中对p的要求是实数即可.

## 1.8. 等比数列和等差数列公式

1. 等比数列前n项和

$$\sum a_n = \frac{a_1(1-q^n)}{1-q}$$

2. 等差数列前n项和

$$\sum a_n = \frac{n(a_1+a_n)}{2},\ a_n = a_1+(n-1)d$$

## 1.9. 绝对值不等式

$$
    \begin{array}{lcl}
        基本式子1:-|a|\leq a \leq |a|\\
        基本式子2:-|b|\leq -b\leq |b|\\
        基本式子3:|a| = |a+b-b| \leq |(a+b)|-|b|\leq |a+b|+|b|\\
        ||a|-|b||\leq |a\pm b|\leq |a|+|b|\\
    \end{array}
$$
## 1.10. 基本不等式

$$\frac{a+b}{2}\geq \sqrt{ab}$$

## 1.11. 圆锥曲线

1. 圆锥曲线的统一(焦线)定义

$$
\begin{array}{lcl}
|PL| = 点到准线距离;\\
|PF| = 点到焦点距离;\\
e = \frac{|d_{PF}|}{|d_{PL}|};\\
0< e <1\ =>\ 椭圆;\\
e=1\ =>\ 抛物线;\\
e>1\ =>\ 双曲线;\\
\end{array}
$$

![](Photos\eclipse-parabola-hyperbola.png "圆锥曲线离心率的由来")
* 注意离心率其实算作一个比值极限.
* 拥有两个顶点和两个焦点的坐标轴称为主坐标轴,另外一个称为次坐标轴.
* 在椭圆或者抛物线中 , $a(半长轴),b(半短轴),c(半焦距)$三者是直角三角形三边关系,但在椭圆中 , a是斜边 , 在双曲线中 , c是斜边.
* 圆锥曲线上的点到两个焦点的距离和(椭圆/抛物线) **/** 差(双曲线)是$2a$.
1. 圆锥曲线的物理特性(光/声)

* 对抛物线 , 所有的入射线其入射角和反射角相同 , 且反射线会经过焦点;(利用可逆性也可以得出焦点发出的线必然会转化为平行线).
    这是探照灯(从焦点出发)和麦克风(从外侧射入)的理论基础.
* 对椭圆 , 从一个焦点发出的线在椭圆上反射之后会汇聚到另一个焦点.
* 对于双曲线 , 从一个焦点发出的线在对侧双曲线分支上反射之后 , 其反射轨迹的反向延长线汇聚在另一焦点上.

## 1.12. 摆线

* 摆线的特性是一个周期内转过的角度对应的弧长和它的水平位移在数值上相等.
* $x = a(t-sint);$
* $y = a(1-cost);$
* 摆线的力学性质;
    * 重力作用下 , 倒置摆线是使物体下落最快的路径.
    * 重力作用下 , 从倒置摆线上的点滑到倒置摆线中端顶点的时间相同.
