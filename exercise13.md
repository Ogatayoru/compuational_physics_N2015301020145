## 摘要

解决波动问题，首先要建立波动方程，而后的问题就是在给定边界条件下求解波动方程。本次作业完成课后习题6.6，展示绳波的传播、反射过程。　 　

## 背景
波动现象是自然界十分常见的现象，从弹性波(例如绳波、水波等)到电磁波，再到引力波，波动现象是物理学研究的重要课题。
## 正文

绳波是一维波动问题，在不考虑能量损耗、认为绳是轻柔绳的前提下，绳波由如下波动方程描述： 

![](http://latex.codecogs.com/gif.latex?\frac{\partial^2y}{\partial{t^2}}=c^2\frac{\partial^2y}{\partial{x^2}})

其中$c$是波速。要解出绳波的运动状态，必须给定一定的边界条件。常见的边界条件有自由边界条件和固定边界条件等。为简单起见，这里取固定边界条件，即绳端总是不发生横向位移。对于非端点的元段，则可以让其离散化，然后通过如下的迭代方法逐步求解绳波随时间的演化： 

![](http://latex.codecogs.com/gif.latex?y(i,n+1)=2(1-r^2)y(i,n)-y(i,n-1)+r^2[y(i+1,n)+y(i-1,n))
　　　　 

这里![](http://latex.codecogs.com/gif.latex?r=c\Delta{t}/\Delta{x})，![](http://latex.codecogs.com/gif.latex?t=n\Delta{t})和![](http://latex.codecogs.com/gif.latex?x=i\Delta{x})分别是时间和元段位置坐标。初始条件通过如下方法给出：在连续两个时刻，给出绳波位移，这样即可开始迭代，给出绳波随时间的演化。
### 绳波问题的求解-----绳波随时间的演化

考虑高斯型波包的运动:[源代码](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/code1301)

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/p1.png)

波包叠加的动态图像:[源代码](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/code1302)

![image](https://github.com/computationalphysics2013301020107/computationalphysics_N2013301020107/blob/master/chapter6/14.1.gif)
## 结论

容易看出,在边界出有半波损失,与经典力学中的结论一致。

## 致谢
感谢学长的源代码。
