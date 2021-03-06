# exercise_05_chapter2.Cannon Shell
***
## Abstract
For this case, we employ numerical approach to calculate the flight path of the cannon shell. And to exactly explain the problem, here we will analyse the cannon shell model by two steps.
## Background
- It's a realistic projectile motion in the model of cannon shell.
- In the case, the launching point of cannon shell serves as the coordinate origin. And the same time, we take the facters like effects of gravitational acceleration and the wind resistance into consideration as well.
- Among which, gravitational accelaration concerns the height of flight and the effect of wind resistence then relates to the air density.
## The Main Body
##### Step one
- Suppose the sea level as the initial launch altitude of cannon shell and the direction of projectile flight on the horizontal x-axis against the vertical direction of sea level on the vertical Y-axis; The shell velocity is defined as v, the X-axis component of which is ![](http://latex.codecogs.com/gif.latex?v_{x}) and the Y-axis component of which is ![](http://latex.codecogs.com/gif.latex?v_{y}). The angle between the velocity direction and the X-axis is ![](http://latex.codecogs.com/gif.latex?\theta).Finally, we suppose the initial velocity as ![](http://latex.codecogs.com/gif.latex?v_{0}). And here, we have to give some exactparameters: the mass of cannon shell is m, the force of wind resistence is ![](http://latex.codecogs.com/gif.latex?F_{d}), the gravatational accelaration is g.
- Applying Newton second law:
   
     ![](http://latex.codecogs.com/gif.latex?m\frac{dv_{x}}{dt}=F_{d,x}=F_{d}\cos\theta=m\frac{dv_{y}}{dt}=F_{d,y}-mg=F_{d}\sin\theta-mg=F_{d}\frac{v_{y}}{v}-mg)
     
- As for the wind resistence:
     
     ![](http://latex.codecogs.com/gif.latex?F_{d}=-B_{2}v^2)
     
     in which,  ![](http://latex.codecogs.com/gif.latex?B_{2}) is the drag coefficient of wind over the sea level nearby.
- Then 

     ![](http://latex.codecogs.com/gif.latex?m\frac{dv_{x}}{dt}=-B_{2}vv_{x})
     
     ![](http://latex.codecogs.com/gif.latex?m\frac{dv_{y}}{dt}=-B_{2}vv_{y}-mg)
- Using Taylor's expansion on ![](http://latex.codecogs.com/gif.latex?v_{x}(t)) and ![](http://latex.codecogs.com/gif.latex?v_{y}(t))：
 
     ![](http://latex.codecogs.com/gif.latex?v_{x}(t+\Delta{t})=v_{x}(t)+\frac{dv_{x}}{dt}\Delta{t})
     
     ![](http://latex.codecogs.com/gif.latex?v_{y}(t+\Delta{t})=v_{y}(t)+\frac{dv_{y}}{dt}\Delta{t})
- Solving the resulting equations simultaneously
 
     ![](http://latex.codecogs.com/gif.latex?v_{x}(t+\Delta{t})=v_{x}(t)-\frac{B_{2}vv_{x}}{m}\Delta{t})
     
     ![](http://latex.codecogs.com/gif.latex?v_{y}(t+\Delta{t})=v_{y}(t)-\frac{B_{2}vv_{y}+mg}{m}\Delta{t})
     
     among which, ![](http://latex.codecogs.com/gif.latex?v=\left({v_{x}}^2+{v_{y}}^2\right)^{1/2})
- Thus
     
     ![](http://latex.codecogs.com/gif.latex?v_{x,i+1}=v_{x,i}-\frac{B_{2}vv_{x,i}}{m}\Delta{t})
     
     ![](http://latex.codecogs.com/gif.latex?v_{y,i+1}=v_{y,i}-\frac{B_{2}vv_{y,i}+mg}{m}\Delta{t})
     
     with the recurrence relation, we can calculate punchs of velocities at different moment after the launch of cannon shell.
- Then we're also capable of giving the recurrence relation of displacement:
     
     ![](http://latex.codecogs.com/gif.latex?x_{i+1}=x_{i}+v_{x,i}\Delta{t})
     
     ![](http://latex.codecogs.com/gif.latex?y_{i+1}=y_{i}+v_{y,i}\Delta{t})
     
##### step two
- Take the relation into consideration between the gravitational acceleration g and height,
 
     ![](http://latex.codecogs.com/gif.latex?g=G\frac{M_{earth}}{(R_{earth}+h)^2})
 
     in which, ![](http://latex.codecogs.com/gif.latex?R_{earth}) is the earth radius, h is the altitude. The gravitational acceration near the earth surface ![](http://latex.codecogs.com/gif.latex?g_{0}=9.8m/s^2),the earth radius we take is 6400km.
- Then at any altitude, we can caculate the gravitational acceleration:
     
     ![](http://latex.codecogs.com/gif.latex?g_{h}=\frac{6400000^2}{(6400000+h)^2}g_{0})
     
- As for the effects of wind resistence, the air density alters along with the change of heights of cannon shell, as the result of which the alterations of wind resistence occurs. About the air density,we take:

     ![](http://latex.codecogs.com/gif.latex?\rho=\rho_{0}(1-\frac{ah}{T_{0}})^\alpha)
      
     ![](http://latex.codecogs.com/gif.latex?a\approx6.5\times10^{-3},\alpha\approx2.5)
     
- So

     ![](http://latex.codecogs.com/gif.latex?v_{x,i+1}=v_{x,i}-(1-\frac{ay_{i}}{T_{0}})^{\alpha}\frac{B_{2}vv_{x,i}}{m}\Delta{t})
     
     ![](http://latex.codecogs.com/gif.latex?v_{y,i+1}=v_{y,i}-\frac{B_{2}(1-\frac{ay_{i}}{T_{0}})^{\alpha}vv_{y,i}+mg_{0}\frac{6400000^2}{(6400000+y_{i})^2}}{m}\Delta{t})
     
## Conclusion 
- Here you can find the [source code](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/exercise05_resource_code.py).
- The following chart is the result after the code runs.![chart](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/pacture05.png)
## Analysis
- The approach ignores the effect occured by Coriolis force， which is engendered from the earth rotation.
- Applying this program, it's acessed to the perfect angle which guarantees the longest range of cannon shell.
## Acknowledgement
Thanks for the source code from the seniors.
