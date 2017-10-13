# Exercise_04_chapter 1_1.5
***
## Abstract
Employ the Euler method to compute the solution to exercise 1.5 of Chapter one. And then compare the results with the exact solution to exercise 1.5. It turns out that for this case Euler method is capable of giving the exact result.
## Background
- A decay problem with two types of nuclei A and B, but now suppose that nuclei of type A decay into ones of type B, while nuclei of type B decay into ones of type A. A better analogy would be a resonance in which a system can tunnel or move back and forth between two states A and B which have equal energies.
- Now we assume that the two types of decay are characterized by the same time contant, ![](http://latex.codecogs.com/gif.latex?\tau), with ![](http://latex.codecogs.com/gif.latex?N_A$) and ![](http://latex.codecogs.com/gif.latex?N_B$) representing the numbers of nuclei, as functions of time.And they satisfy the following corresponding rate equations:

    ![](http://latex.codecogs.com/gif.latex?\frac{dN_{A}}{dt}=\frac{N_{B}}{\tau}-\frac{N_{A}}{\tau}),

    ![](http://latex.codecogs.com/gif.latex?\frac{dN_{B}}{dt}=\frac{N_{A}}{\tau}-\frac{N_{B}}{\tau}),

- Compute the solution to the function relation between ![](http://latex.codecogs.com/gif.latex?N_A$) and ![](http://latex.codecogs.com/gif.latex?N_B$) in the case that the initial values and various parameters are both defined.
## The main body
- Substitute the differential with the difference:

    ![](http://latex.codecogs.com/gif.latex?\frac{N_{A}(i+1)-N_{A}(i)}{dt}=\frac{N_{B}(i)}{\tau}-\frac{N_{A}(i)}{\tau}),

    ![](http://latex.codecogs.com/gif.latex?\frac{N_{B}(i+1)-N_{B}(i)}{dt}=\frac{N_{A}(i)}{\tau}-\frac{N_{B}(i)}{\tau}),

- Iteration:

    ![](http://latex.codecogs.com/gif.latex?N_{A}(i+1)=N_{A}(i)+\frac{dt}{\tau}\left(N_{B}(i)-N_{A}(i)\right)),

    ![](http://latex.codecogs.com/gif.latex?N_{B}(i+1)=N_{B}(i)+\frac{dt}{\tau}\left(N_{A}(i)-N_{B}(i)\right)),

As long as the time step is selected narrowly enough, the result will actually gets close to that of the exact solution as possible as we expected. Here I give [the source code](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/resource_code_01.py) of the program that employs the Euler method to compute the solution of the exercise 1.5.  

- Print the initial values and parameters:

    ![](http://latex.codecogs.com/gif.latex?N_{A}(0)=100),

    ![](http://latex.codecogs.com/gif.latex?N_{B}(0)=0),

    ![](http://latex.codecogs.com/gif.latex?\tau=1s),

    ![](http://latex.codecogs.com/gif.latex?dt=0.1s)

- The output:
The following chart presents the results, in which the dotted lines show the output of numerical solution in comparison with the exact analytic solution, which is described with the solid line.

![chapter1](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/chapter1.png)

Here is [the relevant data](https://github.com/Ogatayoru/compuational_physics_N2015301020145/blob/master/data_01).

- Analysis
the exact analytic solution:

   ![](http://latex.codecogs.com/gif.latex?N_{A}(t)=\frac{1}{2}\left(N_{A}(0)+N_{B}(0)+\left(N_{A}(0)-N_{B}(0)\right)e^{-\frac{2t}{\tau}}\right)),

   ![](http://latex.codecogs.com/gif.latex?N_{B}(t)=\frac{1}{2}\left(N_{A}(0)+N_{B}(0)-\left(N_{A}(0)-N_{B}(0)\right)e^{-\frac{2t}{\tau}}\right)),

So we compare the exact solution with the numerical results, and it's easy to figure out the accuracy of numerical results.
From the chart, we can see, the numerical results do not actually fit perfectly the exact solution.

## Conclusion
Employing Euler method can handle the differtial equations to some degree.
## Acknowledgement
Thanks for the source code from seniors.
