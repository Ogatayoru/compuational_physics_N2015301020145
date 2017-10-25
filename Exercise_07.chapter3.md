## Abstract
With Euler-cromer method to write programs, we are capable of studying the laws of single pendulum movement with linear factor. The following case neglects the effcts arising from the damping and the situation where there exists the driving force.
## Background
In an ideal case, the friction is ignored and the angle the string makes with the vertical is assumed to be small. Such a pendulum undergoes what is known as simple harmonic oscilation.
## The main body 
With the analysis of force condition,we can employ Newton's second law to give the dynamic equation of single pendulum:
```math
\frac{d^2\theta}{dt^2}=-\frac{g}{l}\sin{\theta}
```
in which, `$\theta$` is the angle the single pendulum has turned, g is the gravitational acceleration,l is the length the single pendulum measures.
Meanwhile, the palstance `$\omega$` satisfies the formula below:
```math
\frac{d\theta}{dt}=\omega
```
Combine the two euations above:
```math
\begin{cases}
\frac{d\omega}{dt}=-\frac{g}{l}\sin{\theta}\\
\\
\frac{d\theta}{dt}=\omega
\end{cases}
```
Using Euler-Cromer method to write program,we must convert it into recursive formula:
```math
\begin{cases}
\omega_{i+1}=\omega_{i}-\frac{g}{l}\sin{\theta_i}\Delta{t}\\
\theta_{i+1}=\theta_{i}+\omega_{i}\Delta{t}\\
t_{i+1}=t_{i}+\Delta{t}
\end{cases}
```
By giving some initial parameters and conditions, we can figure out a series of `$\theta$` and `$\omega$` at different time in use of the recursive formula. To link the points, we can draw the graph describing `$\theta$`-t、`$\omega$`-t and `$\omega$`-`$\theta$`.

Here is the source code.
## Analysis
First, we give the length l=1.0m, the total time t=10s and time step dt=0.04s. Considering that the maximum amplitude of sigle pendulum depends on the initial angle where we release the single pendulum, naturally we can affect the maximum amplitude through altering the release angle. Here we temporarily set the initial angel `$\theta_0$`=0.2rad, and then we get the following `$\theta$`-t graph:

![image](http://note.youdao.com/favicon.ico)

It fits well linear approximation result out of the small range where we set the initial angel, which allows the approximation relation `$\sin{\theta}\approx\theta$` to make sense quite well.

Then we rase the initial angel to 0.5rad:

![image](http://note.youdao.com/favicon.ico)
 
It's easy to find the dynamic cycle of single pendulum changes. The result is distinguished from the simple harmonic approximation, where the dynamic cycle (`$T=\sqrt\frac{l}{g}$`) ha nothing to do with the initial angel. Next, we rase the initial angel to 1.0rad:

![image](http://note.youdao.com/favicon.ico)

## Conclusion
Comparing the three graph above, we have to give such a conclusion that the cycle of single pendulum rases along with the increase of the initial angle we set. While, we ignore the damping and driving force ao that the movement of single pendulum is still seen as a periodic motion.
## Ackkownledgement
Thanks for the souce code from the seniors.