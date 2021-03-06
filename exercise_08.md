## Background
The atmospheric scientist E.N.Lorentz put forward the Lorentz Model on the modern chaotic field in 1963. 
## Abastract
We can study the model by programme, in which we set two of the three parameters in the equations ![](http://latex.codecogs.com/gif.latex?\sigma) and ![](http://latex.codecogs.com/gif.latex?b) as constants. Then we will research how the parameter ![](http://latex.codecogs.com/gif.latex?r) plays its role.
## The main body
Lorentz simplified the Navier-Stokes equations and figured out the three equations below:

![](http://latex.codecogs.com/gif.latex?\begin{cases}\frac{dx}{dt}=\sigma(y-x)\\\\\frac{dy}{dt}=-xz+rx-y\\\\\frac{dz}{dt}=xy-bz\end{cases})

Here we still follow Lorentz's work, in which ![](http://latex.codecogs.com/gif.latex?\sigma=10),  ![](http://latex.codecogs.com/gif.latex?b=8/3) . Then we start to deal with the three equations by the Runge-Kutta method. We define time ![](http://latex.codecogs.com/gif.latex?t) is at random, and use Runge-Kutta method as the the following:

![](http://latex.codecogs.com/gif.latex?\begin{cases}x(t+\Delta{t})=x(t)+f_{x}(x',y',z',t')\Delta{t}\\\\y(t+\Delta{t})=y(t)+f_{y}(x',y',z',t')\Delta{t}\\\\z(t+\Delta{t})=z(t)+f_{z}(x',y',z',t')\Delta{t}\end{cases})

in which,

![](http://latex.codecogs.com/gif.latex?\begin{cases}x'=x(t)+\frac{1}{2}f_{x}(x(t),y(t),z(t),t)\Delta{t}\\\\y'=y(t)+\frac{1}{2}f_{y}(x(t),y(t),z(t),t)\Delta{t}\\\\z'=z(t)+\frac{1}{2}f_{z}(x(t),y(t),z(t),t)\Delta{t}\\\\t'=t+\frac{1}{2}\Delta{t}\end{cases})

among which,

![](http://latex.codecogs.com/gif.latex?\begin{cases}f_{x}(x(t),y(t),z(t),t)=\frac{dx}{dt}=\sigma(y-x)\\\\f_{y}(x(t),y(t),z(t),t)=\frac{dy}{dt}=-xz+rx-y\\\\f_{z}(x(t),y(t),z(t),t)=\frac{dz}{dt}=xy-bz\end{cases})

Then we can draw the graph with the scatters.
Here is [the source code](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/code_08_01).
## Analysis and Conculsion
#### step 1
put the initial values: ![](http://latex.codecogs.com/gif.latex?x=1),  ![](http://latex.codecogs.com/gif.latex?y=0) , ![](http://latex.codecogs.com/gif.latex?z=0), time step ![](http://latex.codecogs.com/gif.latex?dt=0.0001), and the total time ![](http://latex.codecogs.com/gif.latex?t=50). First, we give ![](http://latex.codecogs.com/gif.latex?r=5), and then the graph output is the below:
 
![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/x1y0z0dt0.0001t50r5t_z.png)

from the graph, it's easy to find that ![](http://latex.codecogs.com/gif.latex?z) gradually approachs a constant of nonzero along with the falling of amplitude during a short period of time. Then we give ![](http://latex.codecogs.com/gif.latex?r=10) :

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/x1y0z0dt0.0001t50r10t_z.png)

Compared with ![](http://latex.codecogs.com/gif.latex?r=5), it's actual to find ![](http://latex.codecogs.com/gif.latex?z) grows as the similiar rule, while such a approaching period of time inceases and stiil remains stable at a nonzero but lager terminal. Continually, we add ![](http://latex.codecogs.com/gif.latex?r) up to 15 :

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/x1y0z0dt0.0001t50r15t_z.png)

Still we increase ![](http://latex.codecogs.com/gif.latex?r) to 20 :

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/x1y0z0dt0.0001t50r20t_z.png)

Glancing over the two graphes above, we still are in a position to draw the conclusion that those '![](http://latex.codecogs.com/gif.latex?z)'s satisfy the common regular pattern all through. Yet, if we input ![](http://latex.codecogs.com/gif.latex?r=25) :

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/x1y0z0dt0.0001t50r25t_z.png)

While, it's astonishing to witness that ![](http://latex.codecogs.com/gif.latex?z)'s development departures dramatically the regular pattern previously. Specifically, the value of ![](http://latex.codecogs.com/gif.latex?z) remains constant oscillation as time goes on without the tendency towards just a constant but could be considered as oscillation around a central value even if its amplitude seems unpredictable.
#### step 2
If we rewrite [the code](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/code_08_02), in which the graph output describes the phase space ![](http://latex.codecogs.com/gif.latex?x-z). As the above, we firstly give ![](http://latex.codecogs.com/gif.latex?r=5) :

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/x1y0z0dt0.0001t50r5.png)

We can see the curve continues to spiral inwards and eventually withdraws to a dot, that is ![](http://latex.codecogs.com/gif.latex?z)'s final constant. Then we add ![](http://latex.codecogs.com/gif.latex?r) up to 10 :

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/x1y0z0dt0.0001t50r10.png)

It's exact to find that the rule keeps the same while the time curve retracts spreads and the terminal goes beyond the previous------the same conclusion we arrive at as step 1. Now we input ![](http://latex.codecogs.com/gif.latex?r=15) :

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/x1y0z0dt0.0001t50r15.png)

Then ![](http://latex.codecogs.com/gif.latex?r=20) :
 
![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/x1y0z0dt0.0001t50r20.png)

From the above, the rule begins to be inadequate and the dot curve withdraws to is not that distinct. Finally, we increase ![](http://latex.codecogs.com/gif.latex?r) to 25 :

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/x1y0z0dt0.0001t50r25.png)

It's clear that the chaos phenomenon occurs, in which the curve will not ever withdraw to a dot and its rule becomes more unpredictable. Divided by the line ![](http://latex.codecogs.com/gif.latex?x=0), the whirlpool curves on both sides are asymmetrical with the left more concentrated.
## Acknowledgement
Thanks for the source code from the seniors.
