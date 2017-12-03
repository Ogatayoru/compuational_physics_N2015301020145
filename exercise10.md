## 摘要

LORENZ模型是E.N.LORENZ从气象问题中抽象出来的一个极简化的模型，但仍然能够有效展示混沌现象的产生，并且可以期待一般流体中也会拥有这样的混沌产生机制。

## 背景

Lorenz模型是从流体力学的Navier-Stokes方程在Rayleigh-Benard问题里简化得到的一个方程组，其反映了速度、温度、密度变量随时间演化的规律。

![](http://latex.codecogs.com/gif.latex?\begin{cases}\frac{dx}{dt}=\sigma(y-x)\\\\\frac{dy}{dt}=-xz+rx-y\\\\\frac{dz}{dt}=xy-bz\end{cases})

其中![](http://latex.codecogs.com/gif.latex?x)、![](http://latex.codecogs.com/gif.latex?y)、![](http://latex.codecogs.com/gif.latex?z)表示流体温度、密度、速度，而 ![](http://latex.codecogs.com/gif.latex?r) 反映由温差带来的驱动效果，则 ![](http://latex.codecogs.com/gif.latex?b) 反应流体阻尼。由于上式对实际问题太过简化，故不能期待其能预言正确的物理现象。我们要做的是展示这样简化的模型也能产生混沌现象。这样的方程一般来讲将给出振动解，因而欧拉法可能不适用。然而经过详细讨论可以发现欧拉法在数值求解此问题时仍然给出不错精度的结果。因此下面就采用欧拉法来求解此问题。

## 正文
### LORENZ 模型

LORENZ模型内流体运动显著依赖于驱动，当改变驱动的大小时，即可观察到混沌的产生和消失。下图表明，当驱动幅度较小时，不产生混沌，而驱动幅度大一些时，则产生混沌现象，程序可见 [源代码](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/exercise10)

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/ch3_lorenz_z_vs_t.png)

取 ![](http://latex.codecogs.com/gif.latex?\sigma=10,b=8/3) 时Lorenz模型描述的流体运动，改变 ![](http://latex.codecogs.com/gif.latex?r) 驱动的幅度。(a)(b)所示当驱动幅度较小时，不产生混沌，流体在经过一段暂态过程后进入稳恒对流运动阶段。(c)图所示为 ![](http://latex.codecogs.com/gif.latex?r=29.00) 的强驱动情况，此时流体发生了复杂的混沌运动。

### 相空间的图形

和前面的摆动问题一样，我们可以作出相空间 ![](http://latex.codecogs.com/gif.latex?x)、![](http://latex.codecogs.com/gif.latex?y)、![](http://latex.codecogs.com/gif.latex?z) 的图形，这样更能揭示混沌现象的内在规律性。另外，还可以作出相空间的截面，可以发现这样的截面是与初值无关的。也就是说，尽管混沌现象内禀复杂，其对初值极其敏感，但其相空间截面却与初值无关，是混沌运动的"不变量"，因而尽管不能预言混沌系统随时间演化规律，但其相图在一定程度上是可以预测的。这和之前是同一个程序。

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/10.png)

取 ![](http://latex.codecogs.com/gif.latex?\sigma=10,b=8/3) 时Lorenz模型描述的流体运动，图(a)(b)(c)分别从三个不同方向观察混沌的相空间，而(d)则是取 ![](http://latex.codecogs.com/gif.latex?y=0) 的相空间的截面。

## 致谢

感谢学长的代码。
