# efficient-PIDE-2D

Authors: Gujji Reddy, Alan Seitenfuss, Debora Medeiros, Luca Meacci, Milton Assunção, and Michael Vynnycky

A short MATLAB implementation is provided for the numerical solution of the parabolic integro-differential equations on unstructured grids in two spatial dimensions. The piecewise linear finite element spaces on triangles are used for the space discretization, whereas the time discretization is based on the backward-Euler and the Crank-Nicolson methods. The quadrature rules, to discretize the Volterra integral term, are chosen so as to be consistent with the time-stepping schemes. Further, an efficient version of the code is presented using vectorization technique in the assembling process and a comparative study is presented. Numerical example prove the flexibility of the code.

There are six zip-files which contain the necessary MATLAB files therein:
– BE LRR unvectorized.zip (backward Euler, left rectangular rule, unvectorized)
– BE LRR vectorized.zip (backward Euler, left rectangular rule, vectorized)
– BE RRR unvectorized.zip (backward Euler, right rectangular rule, unvectorized)
– BE RRR vectorized.zip (backward Euler, right rectangular rule, vectorized)
– CN unvectorized.zip (Crank-Nicolson, unvectorized)
– CN vectorized.zip (Crank-Nicolson, vectorized)

To run the demo program, uncompress the desired zip file, and run the solve.m file; this:
– specifies the geometry;
– computes the solution;
– plots the solution.

In particular, the computation of the solution is carried out by PIDE.m, which sets the initial conditions via U0.m, and assembles the stiffness matrix and the
mass matrix via StiffAssemb.m , MassAssemb.m , respectively; thereafter, locsol.m updates the boundary conditions via Ud.m, assembles the load vector via LoadVec.m 
and obtains the solution at the current time step. Note that, in all cases, LoadVec.m makes calls to f.m and intgral.m for the functions f and B , respectively. Furthermore, note that whilst most of the subroutines are the same in both the vectorized and unvectorized versions of the code, those for StiffAssemb.m and MassAssemb.m are necessarily slightly different.

Each of the authors have an equal contribution to this work.
