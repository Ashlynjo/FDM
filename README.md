# FDM
In this repository I will add codes based on finite difference method used to simulate fluid particle based motion
1D Burgers' Equation Solver using Finite Difference Method
This repository contains a Python implementation of the 1D Burgers' equation using the explicit finite difference method. The Burgers' equation is a fundamental PDE in fluid mechanics that combines non-linear convection and diffusion:

∂
u
∂
t
+
u
∂
u
∂
x
=
ν
∂
2
u
∂
x
2
∂t
∂u
​
 +u 
∂x
∂u
​
 =ν 
∂x 
2
 
∂ 
2
 u
​
 
Features
Discretization of time and space using the finite difference method.
Handles the advection and diffusion terms explicitly:
Advection: 
−
u
∂
u
∂
x
−u 
∂x
∂u
​
 
Diffusion: 
ν
∂
2
u
∂
x
2
ν 
∂x 
2
 
∂ 
2
 u
​
 
Simulates the time evolution of 
u
(
x
,
t
)
u(x,t) over a 1D spatial domain.
Implements step-like initial conditions for testing shock formation and diffusion.
Code Workflow
Initialization:

Define the spatial domain (
x
x) and discretize it using step size 
Δ
x
Δx.
Set the time parameters with step size 
Δ
t
Δt for numerical stability.
Initialize the velocity field 
u
(
x
)
u(x) with step-like initial conditions.
Numerical Scheme:

The finite difference method is used to compute 
u
(
x
,
t
)
u(x,t) for the next time step:
u
i
n
+
1
=
u
i
n
−
u
i
n
Δ
t
Δ
x
(
u
i
n
−
u
i
−
1
n
)
+
ν
Δ
t
Δ
x
2
(
u
i
+
1
n
−
2
u
i
n
+
u
i
−
1
n
)
u 
i
n+1
​
 =u 
i
n
​
 −u 
i
n
​
  
Δx
Δt
​
 (u 
i
n
​
 −u 
i−1
n
​
 )+ν 
Δx 
2
 
Δt
​
 (u 
i+1
n
​
 −2u 
i
n
​
 +u 
i−1
n
​
 )
Boundary conditions are enforced to maintain stability at the edges.
Output:

Saves the simulation data for all time steps.
Generates a plot showing the evolution of 
u
(
x
,
t
)
u(x,t) over time.
Getting Started
Prerequisites:

Python 3.x
Libraries: numpy, matplotlib
Run the Simulation:

python burgers_equation_solver.py
This will simulate the time evolution of 
u
(
x
,
t
)
u(x,t) and save a plot.

Modify Parameters:

Adjust the viscosity (
ν
ν), time step (
Δ
t
Δt), and spatial resolution (
Δ
x
Δx) for customized simulations.
Key Notes
Stability Condition: Ensure the Courant–Friedrichs–Lewy (CFL) condition is satisfied:
Δ
t
Δ
x
≤
ν
2
Δx
Δt
​
 ≤ 
2
ν
​
 
The current setup is suitable for diffusion-dominated regimes. To emphasize non-linear effects, adjust the initial conditions or parameters.
Applications
This implementation can be used to study:

Shockwave formation in fluids.
Transition from laminar to turbulent flow.
Diffusion and dissipation of velocity profiles.
Visualization
The output shows how the velocity field 
u
(
x
,
t
)
u(x,t) evolves over time, showcasing the balance between advection and diffusion. Below is an example plot:

(Update with the actual file path)


