## Abstract
By means of numerical model, we can trace the baseball limited by some specific initial conditions. Here we take the baseball for instance, yet the actual result is not just confined to the baseball.
## Background
The baseball would get an initial velocity in the assumption that we throw it away, at which it's forced to spin backwards at the same time. Then its rotation brings an initial palstance  ![](http://latex.codecogs.com/gif.latex?\omega). Here we suppose ![](http://latex.codecogs.com/gif.latex?\upsilon_0) and ![](http://latex.codecogs.com/gif.latex?\omega_0) are both gived.
## The Main Body
- **Building numerical model**
    
    First of all, we start with the mechannics analysis of baseball. Employing Newton's second law, it's available to build the dynamics figure of baseball, in which we give its mass about 149g. Also we shall take the following forces into consideration.
    
    - Air-resistence
    
        Generally the air-resistence in the movement  of objects satisfys the equation below: 
        
        ![](http://latex.codecogs.com/gif.latex?F_{drag}=-B_{2}\upsilon^2)
        
        in which, ![](http://latex.codecogs.com/gif.latex?B_2) is drag conefficient. Meanwhile the drag conefficient of baseball fits well the following emprical formula:
        
        ![](http://latex.codecogs.com/gif.latex?\frac{B_2}{m}=0.0039+\frac{0.0058}{1+e^\frac{\upsilon-\upsilon_d}{\Delta}})
        
        in which, ![](http://latex.codecogs.com/gif.latex?\upsilon_d=3.5m/s); ![](http://latex.codecogs.com/gif.latex?\Delta=5m/s), both of them adopt the SL Units.
    - Magnus Force
        
        While objects remain spinning, fluid would affect objects in the form of Magnus force out of difference between fluids surrounding each part of objects, which is defined by the equation below:
        
        ![](http://latex.codecogs.com/gif.latex?\vec{F}_{Magnus}=S_0\vec{\omega}\times\vec{\upsilon})
        
        in which, ![](http://latex.codecogs.com/gif.latex?S_0) is a content, ![](http://latex.codecogs.com/gif.latex?\frac{S_0}{m}\approx4.1\times10^{-4})
    - Lateral Force
        
        Out of diverse roughness of different parts on the surface of baseball, each part is acted upon by different forces, and the the final mechanical effect occurs as the lateral force related to surface of baseball. Here we provide its numerical expression:
        
        ![](http://latex.codecogs.com/gif.latex?\frac{F_{lateral}}{mg}=0.5[\sin(4\theta)-0.25\sin(8\theta)+0.08\sin(12\theta)-0.025\sin(16\theta)])
        
        in which, ![](http://latex.codecogs.com/gif.latex?\theta=\int_{0}^{t}\omega\,d\tau).
- **Numerical Calculation**
    
    - Establishing coordinate system
        
        For convenience, we suppose the baseball starts from the origin in the ![](http://latex.codecogs.com/gif.latex?xOz) plane. Its initial velocity is ![](http://latex.codecogs.com/gif.latex?\upsilon_0). The elevation is ![](http://latex.codecogs.com/gif.latex?(90-\theta)^\circ). 
    - Dynamics Equation
    
        To combine all of above, we can figure out the dynamics equation below:
        
        ![](http://latex.codecogs.com/gif.latex?\frac{dx}{dt}=\upsilon_x)
        
        ![](http://latex.codecogs.com/gif.latex?m\frac{d\upsilon_{x}}{dt}=-B_2\upsilon\upsilon_x-S_0\omega\upsilon_z-F_{lat}\frac{\upsilon_z}{\upsilon})
        
        ![](http://latex.codecogs.com/gif.latex?\frac{dy}{dt}=\upsilon_y)
        
        ![](http://latex.codecogs.com/gif.latex?m\frac{d\upsilon_{y}}{dt}=-B_2\upsilon\upsilon_y)
        
        ![](http://latex.codecogs.com/gif.latex?\frac{dz}{dt}=\upsilon_{z})
        
        ![](http://latex.codecogs.com/gif.latex?m\frac{d\upsilon_{z}}{dt}=-mg-B_2\upsilon\upsilon_z+S_0\omega\upsilon_x+F_{lat}\frac{\upsilon_x}{\upsilon})
        
        ![](http://latex.codecogs.com/gif.latex?\upsilon=\sqrt{{\upsilon_x}^2+{\upsilon_y}^2+{\upsilon_z}^2})
        
        actually, considering the initial conditons, it's easy to find that ![](http://latex.codecogs.com/gif.latex?\upsilon_y=0).
    - [The Source Code](http://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/source_code_exercise2.19).
## Analysis
Suppose the velocity of baseball is high, we fill in the initial conditions: ![](http://latex.codecogs.com/gif.latex?\omega_0=2000rpm![](http://latex.codecogs.com/gif.latex?, ![](http://latex.codecogs.com/gif.latex?\upsilon_0=49m/s), the elevetion is ![](http://latex.codecogs.com/gif.latex?0^\circ), total time is 10s, and time step dt=0.01s. ultimately, the result output is the below:

![image](http://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/exercise2.19z-x.png)

in which, the dotted line express theoretical parabola and the solid line presents the actual parabola of baseball. So we can see, out of the over weight of palstance, Magnus force brings out distinct effect, which causes the posterior curve turns up so obviously that it spreads off the actual parabola more and more excessively.

If we extend the total time to 20s, it's astonishing to find the baseball even is possible to move up !

![image](http://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/exercise2.19z-x02.png)
## Conclusion
When the palstance of baseball is high, Magnus force occurs a distinct effect to its movement, which causes departure of parabola.
## Acknowledgement
Thanks for the source code from the seniors.
