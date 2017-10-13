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
     
     
      
     
