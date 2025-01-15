# Semi-Lagrangian method

Thanks to operator splitting, solving Vlasov-Equation boils down to solving different advection step (respectively \\( \partial_t f_s = -v \partial_x f_s \\), and \\(\partial_t f_s = -E \partial_v f_s \\)).
Semi-Lagrangian method (SL) takes advantage of the explicit solution of the advection equation.
Indeed, v and E being constants along respectively x and v axis, the solution of those equations take the form given below.
\\[
f_s(x,v,t) = f_s(x-v \Delta t ,v,t - \Delta t) 
\\]
Therefore, given a point \\((x,v,t) \\), the goal is to reconstruct the point at \\((x-v \Delta t ,v,t-\Delta t)\\) at previous time step. Different polynomial reconstructions exist, we chose to use a CWENO-3.2 polynomial reconstruction to prevent Gibbs phenomenom close to discontinuity.


