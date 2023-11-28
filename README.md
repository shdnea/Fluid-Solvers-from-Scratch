# Fluid-Solvers-from-Scratch
Personal study on building fluid solvers from scratch inside Houdini from Jeff Lait Masterclass.

Reference video : https://vimeo.com/42988999

# FOG Volume VS SDFs
- FOG Volumes are like traditional texture map, stores 1 if object is there, 0 if not (notes : only store integer value)
- SDF "Signed Distance Field", store negative for present, positive for absent.
- Zero crossing no longer restricted to voxel boundaries inside SDFs
- SDF also can maintain sharp edges
- SDF is much faster to compute compared to FOG Volumes, this include the minimal distance and direction

# Eulerian VS Lagrangian
- Eulerian  --> store values on grid
- Lagragian --> store values on particles
- Traditional particle system using Lagrangian mechanics

To put it simply, we have a physical system evolving, and the question is where do you want to store the attribute in that simulation, the Eulerian representation store the attribute on fixes grids location and Lagrangian, store the information on the particle itself.

# What the f is Divergence
Divergence is a measure of inbalance in velocity fields.

- Divergence at the center can be measured by comparing ingoing and outgoing velocities of boundary of cells.
- Incompressible fluids should have zero divergence
- Zero divergence fields have "swirl", "shear", and "translate" factors. They do not have a "scale" factor.

Reference for further research on Divergent :
- https://en.wikipedia.org/wiki/Divergence
- https://www.khanacademy.org/math/multivariable-calculus/multivariable-derivatives/divergence-and-curl-articles/a/divergence
