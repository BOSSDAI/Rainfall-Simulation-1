Rainfall Simulation
===================

The following is a description of the rainfall simulation problem that our program will solve. In
this problem, we have a 2-dimensional landscape, which is essentially an NxN grid of points.
Each point has an integer elevation associated with it and our program will read from an input
file. In the rainfall simulation, drops of rain will fall onto the points of the 2D landscape. As those rain drops fall, the water will move in two ways: (1) rain drops will absorb into the ground at apoint at a specified rate and (2) rain drops will trickle from a point in the landscape to their neighboring point(s) (north/south/east/west) that have the lowest elevation. Your program will perform time step simulation, simulating what happens across the 2D landscape in each time
step as rain drops fall onto the points, trickle to lower elevation points, and get absorbed into the ground.
Here are some more specific characteristics of the problem. Within a timestep of the rainfall
simulation program, there are 3 things that can happen in the following sequence: (1) a drop of
rain may fall onto a point in the landscape, (2) if there exists any rain drops on a point at a given timestep, some amount will be absorbed into the ground, and (3) if there remains any rain dropson a point at a given timestep, some amount will trickle away to the neighboring point(s) with the lowest elevation. 


Running the program

```C
./rainfall <P> <M> <A> <N> <elevation_file> 
```
* P = # of parallel threads to use. 
* M = # of simulation time steps during which a rain drop will fall on each landscape
point. In other words, 1 rain drop falls on each point during the first M steps of the
simulation. 
* A = absorption rate (specified as a floating point number)
* N = dimension of the landscape (NxN) 