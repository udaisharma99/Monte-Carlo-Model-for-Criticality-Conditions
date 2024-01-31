# Monte Carlo Model for Criticality Conditions in Neutron Transport Scenarios

This project involves using a Monte Carlo code to estimate the critical size of various objects with respect to the growth of thermal neutron density. The project is divided into 2 phases. In the first phase, The essential goal is to theoretically think of a strategy that strikes a balance between statistical fluctuations and transient effects to achieve optimal accuracy. Once an optimal strategy is devised, the project transitions to the second phase, which involves implementing a cylindrical geometry with a height equal to the radius (H = R) and utilizing the Monte Carlo code to estimate the critical length of this cylindrical geometry.

Methodology:

Phase 1:

Two approaches were explored to optimize the accuracy of the calculations:
1. Manually adjusting queue length: This involved starting with a shorter queue to minimize transient effects and gradually increasing it until stable behavior was observed.
2. Adaptive queue length: This involved dynamically modifying the queue length based on the behavior of the neutron population. A feedback loop was used to modify the queue length after a certain number of trajectories.

The effectiveness of the approach depended on the available computational budget, desired accuracy, and problem complexity.

Phase 2:
1. The code was modified to accommodate a cylindrical geometry by creating a ‘cylinder’ object class inherited from the ‘shape’ class.
2. An iterative technique was employed to determine the critical length for the cylinder.
3. The critical length was initially estimated and the trajectory tracking process was initiated.
4. The count of neutron particles in the queue was observed to determine whether the critical length estimate was too high or too low.
5. The critical length estimate was adjusted based on the observed trend.
6. The process was repeated until the critical length was accurately determined to a satisfactory level.
7. The critical length for the cylindrical geometry was found to be 7.745868 cm.
8. The critical length for a cylindrical geometry is greater than that of a slab geometry due to the curved trajectories taken by neutrons in a cylinder.
9. Observing the growth rate of neutrons against the number of trajectories reveals an initial surge followed by a steady decline. This transient behavior is caused by the replacement of the initial set of neutrons by a new set, effectively flushing out the initial group. Once the new set of neutrons takes over, the growth rate stabilizes around zero, indicating an equilibrium state and confirmation of criticality.

<center> <img width="704" alt="image" src="https://github.com/udaisharma99/Monte-Carlo-Model-for-Criticality-Conditions/assets/138836370/b2f6ff81-4eff-48a5-a52f-a3dab42a7e61"> </center>

