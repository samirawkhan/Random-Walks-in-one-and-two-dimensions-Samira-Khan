# Random-Walks-in-one-and-two-dimensions-Samira-Khan
### Introduction:
Freshwater lakes that have water flowing in (tributaries) and out (outlets) are characterized by a “residence time” – the average time that an individual molecule of water, or another dissolved substance, spends in the lake. This quantity is key when predicting the timescale over which pollutants, for instance, will affect a lake’s ecosystem. The residence time can vary enormously, depending on the volume and other characteristics of the lake – for instance two of the Great Lakes, Lake Erie and Lake Superior have residence times of 2 years and 200 years, respectively. Lake Vostok in Antarctica has a residence time of 13,000 years.The motion of an individual molecule in a large lake can be characterized as diffusive. The motion of a diffusing particle is often described as a random walk, since at each point in time the direction in which the particle moves comes from random collisions with its surrounding atoms and molecules. For simplicity, a random walk is often modelled on a lattice, where the particle is confined to move along the points of the grid. In this problem set, you will look at a random walk on a finite, one-dimensional line of points, and then on a two-dimensional square grid of points. The molecule whose motion you are modeling (the “tracer particle”) will begin at a point (simulating the location of a pollutant’s inflow), and move according to a set of rules described below. There will be another point in the system that is absorbing (simulating an outlet from the lake). The obvious question to ask is how long, on average, it takes for the tracer to move from the source of the spill to the outlet.

### Simulating a random walk in one dimension.
Physicists often model motion using a lattice or grid to simplify the calculation. To start, you will use a one-dimensional line of points running from $x$ = −50 to x = +50, with grid points at each integer value of x. The tracer particle will start at x = −50, and you will simulate it diffusing back and forth on the line, randomly, until it hits the other end at $x$ = +50 – at that instant, the simulation will stop, since this represents the outlet, i.e. the absorbing point. At each time step, the particle can choose to move one step either to the left, or to the right on the line and your simulation will update the particle’s x position accordingly.

#### Here are the rules for the random walk:

At each time step:

If the particle is not at the right edge or the left edge, it can take a step of one grid spacing either to the left or to the right with equal probability.
If the particle is at the left edge (x = −50), it cannot leave the system and should always take a step to the right (sometimes called a “reflective” boundary condition).
If the particle touches x = +50, the random walk ends.

### Simulating a random walk in two dimensions.
For this part, you will use a two-dimensional grid where the x axis goes from -50 to +50 and the y axis also goes from -50 to +50. The particle will start at the middle of the left edge ($x$, $y$) = (−50,0), and we’ll put the outlet/absorber in the middle of the right edge ($x$, $y$) = (+50,0). Again, the particle will diffuse around randomly between these points and when the absorbing point at ($x$, $y$) = (+50,0) is reached, the simulation ends. At each time step, the particle can move one step on the grid and your simulation will update the particle’s x and y positions accordingly. Here are the rules for the random walk:

At each time step:

If the particle is not at an edge, it can take a step of one grid spacing in any of four directions:±$x$, ±$y$; these should all be equally probable.
If the particle is at one of the edges, but not at the absorber, it cannot pass out of the box. It should have a 50% probability of taking a step perpendicularly away from the wall, and a 25% chance of stepping in either of the directions along the wall.
If the particle is at a corner, it has a 50% chance of going in either of the two directions along the walls.
If the particle touches the absorbing point at ($x$, $y$) = (+50,0), the random walk ends.
