## 摘要

相比于地球上的物体运动受到显著的空气阻力影响，行星运动是良好的物理观测场所。17世纪开普勒发现行星运动三大定律，而后牛顿又成功地用万有引力定律解释了开普勒定律，行星运动的研究推动了物理学的发展。

## 背景

行星运动可以用牛顿万有引力定律描述,本文讨论双星系统。双星系统在宇宙中最常见也最简单的多体系统。平方反比有心力场中的运动是稳定的。本文顺便探讨对平方反比定律的偏离所带来的影响,可以定性地得到近似的和广义相对论相同的结论。

## 正文

牛顿的万有引力定律给出了两个质点之间的引力相互作用的规律。在太阳系中，行星受到太阳的引力作用为 
![](http://latex.codecogs.com/gif.latex?f_{G}=\frac{GM_{S}M_{P}}{r^2})

此式连同牛顿第二定律，就可以给出行星运动规律。倘若考虑太阳的有限质量，则行星与太阳二体问题也容易解决，只需要把惯性质量![](http://latex.codecogs.com/gif.latex?M_{E})全部换成所谓的约化质量 ![](http://latex.codecogs.com/gif.latex?\mu=\frac{M_{S}M_{P}}{M_{S}+M_{P}})，则仍可形式上地利用牛顿第二定律解决行星相对太阳的运动问题。 

通过简单的积分可以得到行星运动的轨道方程为 
![](http://latex.codecogs.com/gif.latex?r=\frac{l}{1-e\cos{\theta}})
其中,![](http://latex.codecogs.com/gif.latex?l=\frac{L^2}{{\mu}GM_{S}M_{P}}), ![](http://latex.codecogs.com/gif.latex?e) 是轨道离心率，与系统的角动量和能量相关,其取值可以决定轨道性态, ![](http://latex.codecogs.com/gif.latex?e) 大于1为双曲线轨道, ![](http://latex.codecogs.com/gif.latex?e) 等于1为抛物线轨道, ![](http://latex.codecogs.com/gif.latex?e) 小于1为椭圆轨道。由这样的轨道方程就可以给出开普勒的三大定律。需要注意的是，开普勒三定律是牛顿引力理论即平方反比引力的结果，若力不是平方反比的，则开普勒定律就不成立，行星也一般不存在闭合轨道。下面就来逐步研究行星运动问题。

### 双星问题
#### 引力满足平方反比定律

双星问题可以合理地化为单星问题，但星体数量更多时就不能化为简单的运动问题。因此有必要在静止坐标系下直接对双星运动求数值解。我们展示求解结果如下图所示，相应的程序见[源代码](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/exercise11code1)。可以发现，双星运动轨迹高度依赖初始条件。
![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/ch4.png)

图中两星体质量满足![](http://latex.codecogs.com/gif.latex?\frac{M_{1}}{M_{2}}=2)，以不同的初始条件开始运动。左图(a)显示初始条件合适时，双星轨道为圆形，右图(b)显示初始条件偏离成圆条件时，双星轨道为椭圆。

#### 引力偏离平方反比定律

如果引力不是按牛顿引力理论预言的那样为平方反比，即![](http://latex.codecogs.com/gif.latex?f_{G}=\frac{GM_{S}M_{P}}{r^\beta})，其中 ![](http://latex.codecogs.com/gif.latex?\beta\neq2) 这样来讲一般行星轨道将产生进动。我们利用数值方法在不同初始条件下求解此时的行星运动，程序见[源代码](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/exercise11code2)。计算结果如下图所示。

![](http://latex.codecogs.com/gif.latex?\beta=2.06):
![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/2.06.png)

![](http://latex.codecogs.com/gif.latex?\beta=1.94):
![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/1.94.png)

## 结论

可以看出平方反比定律下轨道很稳定,不同初始条件下轨道的形状不同,但都是闭合的椭圆。与 ![](http://latex.codecogs.com/gif.latex?n=2) 偏离一点后,轨道明显不再闭合,而是有一定的进动。此时与广义相对论结论一样,而且离心率越大,进动越明显, 进动速率和离心率大致成线性关系。

## 致谢
感谢学长的源代码。
