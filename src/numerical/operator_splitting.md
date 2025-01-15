# Operator Splitting

The operator splitting (or "time splitting" in plasma physics) is a numerical method that transform the equation into simpler problem to solve. 
With operator splitting, one will solve first advection along space axis, then advection along velocity axis, and finally collisions. All those steps represents therefore one time step. This operator splitting comes with a cost of a time discretization error in \\(O(\Delta t ^2) \\) (higher order schemes also exist). 

Operator splitting will be useful when adding different types of collisions and to gain more flexibility for the solver.
