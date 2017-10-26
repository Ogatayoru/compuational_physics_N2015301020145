## Abstract
With Euler-cromer method to write programs, we are capable of studying the laws of single pendulum movement with linear factor. The following case neglects the effcts arising from the damping and the situation where there exists the driving force.
## Background
In an ideal case, the friction is ignored and the angle the string makes with the vertical is assumed to be small. Such a pendulum undergoes what is known as simple harmonic oscilation.
## The main body 
With the analysis of force condition,we can employ Newton's second law to give the dynamic equation of single pendulum:

![](http://latex.codecogs.com/gif.latex?\frac{d^2\theta}{dt^2}=-\frac{g}{l}\sin{\theta})

in which, ![](http://latex.codecogs.com/gif.latex?\theta) is the angle the single pendulum has turned, g is the gravitational acceleration,l is the length the single pendulum measures.
Meanwhile, the palstance ![](http://latex.codecogs.com/gif.latex?\omega) satisfies the formula below:

![](http://latex.codecogs.com/gif.latex?\frac{d\theta}{dt}=\omega)

Combine the two euations above:

![](http://latex.codecogs.com/gif.latex?\begin{cases}\frac{d\omega}{dt}=-\frac{g}{l}\sin{\theta}\\\\\frac{d\theta}{dt}=\omega\end{cases})

Using Euler-Cromer method to write program,we must convert it into recursive formula:

![](http://latex.codecogs.com/gif.latex?\begin{cases}\omega_{i+1}=\omega_{i}-\frac{g}{l}\sin{\theta_i}\Delta{t}\\\\t_{i+1}=t_{i}+\Delta{t}\\\\\theta_{i+1}=\theta_{i}+\omega_{i}\Delta{t}\end{cases})

By giving some initial parameters and conditions, we can figure out a series of ![](http://latex.codecogs.com/gif.latex?\theta) and ![](http://latex.codecogs.com/gif.latex?\omega) at different time in use of the recursive formula. To link the points, we can draw the graph describing ![](http://latex.codecogs.com/gif.latex?\theta)-t、![](http://latex.codecogs.com/gif.latex?\omega)-t and ![](http://latex.codecogs.com/gif.latex?\omega)-![](http://latex.codecogs.com/gif.latex?\theta).

Here is [the source code](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/exercise_07_code).

## Analysis
First, we give the length l=1.5m, the total time t=10s and time step dt=0.02s. Considering that the maximum amplitude of sigle pendulum depends on the initial angle where we release the single pendulum, naturally we can affect the maximum amplitude through altering the release angle. Here we temporarily set the initial angel ![](http://latex.codecogs.com/gif.latex?\theta_0)=0.1rad, and then we get the following ![](http://latex.codecogs.com/gif.latex?\theta)-t graph:

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/pendulum_53.png)

Here gives [the original data](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/data_53).

It fits well linear approximation result out of the small range where we set the initial angel, which allows the approximation relation ![](http://latex.codecogs.com/gif.latex?\sin{\theta}\approx\theta) to make sense quite well.

Then we rase the initial angel to 0.5rad:

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/pendulum_54.png)
 
Here gives [the original data](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/data_54).

It's easy to find the dynamic cycle of single pendulum changes. The result is distinguished from the simple harmonic approximation, where the dynamic cycle ( ![](http://latex.codecogs.com/gif.latex?T=\sqrt\frac{l}{g}) ) has nothing to do with the initial angel. Next, we rase the initial angel to 1.0rad, 2.0rad and 3.0rad:

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/pendulum_50.png)

Here gives [the original data_1.0rad](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/data_50).

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/pendulum_51.png)

Here gives [the original data_2.0rad](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/data_51).

![image](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/pendulum_52.png)

Here gives [the original data_3.0rad](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/data_52).

## Conclusion
Comparing the three graph above, we have to give such a conclusion that the cycle of single pendulum rases along with the increase of the initial angle we set. While, we ignore the damping and driving force ao that the movement of single pendulum is still seen as a periodic motion.
## Ackkownledgement
Thanks for the souce code from the seniors.
