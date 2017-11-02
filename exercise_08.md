## Background
The atmospheric scientist E.N.Lorentz put forward the Lorentz Model on the modern chaotic field in 1963. 
## Abastract
We can study the model by programme, in which we set two of the three parameters in the equations ![](http://latex.codecogs.com/gif.latex?\sigma) and ![](http://latex.codecogs.com/gif.latex?b) as constants. Then we will research how the parameter ![](http://latex.codecogs.com/gif.latex?r) plays its role.
## The main body
Lorentz simplified the Navier-Stokes equations and figured out the three equations below:
```math
\begin{cases}
\frac{dx}{dt}=\sigma(y-x)\\\\
\frac{dy}{dt}=-xz+rx-y\\\\
\frac{dz}{dt}=xy-bz
\end{cases}
```
Here we still follow Lorentz's work, in which `$\sigma$`=10, `$b$`=8/3. Then we start to deal with the three equations by the Runge-Kutta method. We define time `$t$` is at random, and use Runge-Kutta method as the the following:
```math
\begin{cases}
x(t+\Delta{t})=x(t)+f_{x}(x',y',z',t')\Delta{t}\\
y(t+\Delta{t})=y(t)+f_{y}(x',y',z',t')\Delta{t}\\
z(t+\Delta{t})=z(t)+f_{z}(x',y',z',t')\Delta{t}
\end{cases}
```
in which,
```math
\begin{cases}
x'=x(t)+\frac{1}{2}f_{X}(x(t),y(t),z(t),t)\Delta{t}\\
y'=y(t)+\frac{1}{2}f_{y}(x(t),y(t),z(t),t)\Delta{t}\\
z'=z(t)+\frac{1}{2}f_{z}(x(t),y(t),z(t),t)\Delta{t}\\
t'=t+\frac{1}{2}\Delta{t}
\end{cases}
```
among which,
```math
\begin{cases}
f_{x}(x(t),y(t),z(t),t)=\frac{dx}{dt}=\sigma(y-x)\\
f_{y}(x(t),y(t),z(t),t)=\frac{dy}{dt}=-xz+rx-y\\
f_{z}(x(t),y(t),z(t),t)=\frac{dz}{dt}=xy-bz
\end{cases}
```
Then we can draw the graph with the scatters.
Here is the source code.
## Analysis and Conculsion
#### step 1
put the initial values: `$x=1$`, `$y=0$`, `$z=0$`, time step `$dt=0.0001$`, and the total time `$t=50$`. First, we give `$r=5$`, and then the graph output is the below:
 
![image](http://note.youdao.com/favicon.ico)

from the graph, it's easy to find that `$z$` gradually approachs a constant of nonzero along with the falling of amplitude during a short period of time. Then we give `$r=10$` :

![image](http://note.youdao.com/favicon.ico)

Compared with `$r=5$`, it's actual to find `$z$` grows as the similiar rule, while such a approaching period of time inceases and stiil remains stable at a nonzero but lager terminal. Continually, we add `$r$`up to 15 :

![image](http://note.youdao.com/favicon.ico)

Still we increase `$r$` to 20 :

![image](http://note.youdao.com/favicon.ico)

Glancing over the two graphes above, we still are in a position to draw the conclusion that those '`$z$`'s satisfy the common regular pattern all through. Yet, if we input `$r=25$` :

![image](http://note.youdao.com/favicon.ico)

While, it's astonishing to witness that `$z$`'s development departures dramatically the regular pattern previously. Specifically, the value of `$z$` remains constant oscillation as time goes on without the tendency towards just a constant but could be considered as oscillation around a central value even if its amplitude seems unpredictable.
#### step 2
If we rewrite the programme, in which the graph output describes the phase space `$x-z$`. As the above, we firstly give `$r=5$` :

![image](http://note.youdao.com/favicon.ico)

We can see the curve continues to spiral inwards and eventually withdraws to a dot, that is `$z$`'s final constant. Then we add `$r$` up to 10 :

![image](http://note.youdao.com/favicon.ico)

It's exact to find that the rule keeps the same while the time curve retracts spreads and the terminal goes beyond the previous------the same conclusion we arrive at as step 1. Now we input `$r=15$` :

![image](http://note.youdao.com/favicon.ico)

Then `$r=20$` :
 
![image](http://note.youdao.com/favicon.ico)

From the above, the rule begins to be inadequate and the dot curve withdraws to is not that distinct. Finally, we increase `$r$` to 25 :

![image](http://note.youdao.com/favicon.ico)

It's clear that the chaos phenomenon occurs, in which the curve will not ever withdraw to a dot and its rule becomes more unpredictable. Divided by the line `$x=0$`, the whirlpool curves on both sides are asymmetrical with the left more concentrated.
## Acknowledgement
Thanks for the source code from the seniors.
