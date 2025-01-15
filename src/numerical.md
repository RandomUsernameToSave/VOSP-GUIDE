# Numerical methods


The Vlasov equation is an equation used in plasma physics. It is given by the following equation, where "s" denote the species "s". And \\(\hat C_{s,s'}\\) denote the collision operator between species "\\(s\\)" and "\\(s'\\)".
\\[
\begin{cases}
    \partial_t f_s + \vec v \partial_x f_s + \frac{q_s}{m_s} \: \vec E \: \partial_v f_s = \sum_{s'} \hat C_{s,s'} \\\\
    \lambda^2 \Delta \phi = -\sum_s q_s n_s  
\end{cases}
\\]

The space of the solution lies in the phase space \\( (\vec x , \vec v)\\) which means that the space of the solution is at least 2 dimensional, and at best 6 dimensional (3 space, 3 velocity). For the moment, the code only works in 1D-1V.

A solver of the Vlasov-Equation is therefore computationally expensive. Moreover, more often than not there exist a huge difference of kinetics between at least two species. The CFL stability condition is therefore a big problem of the Vlasov-Equation. Hence, the methods described below will not suffer this stability condition. However, the time discretization error is still in \\(O(\Delta t ^2)\\). The user will therefore have to find a compromise between time step and calculation.
