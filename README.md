# efficient-PIDE-2D

Authors: Gujji Reddy, Alan Seitenfuss, Debora Medeiros, Luca Meacci, Milton Assunção, and Michael Vynnycky

A short MATLAB implementation is provided for the numerical solution of the parabolic integro-differential equations on unstructured grids in two spatial dimensions. The piecewise linear finite element spaces on triangles are used for the space discretization, whereas the time discretization is based on the backward-Euler and the Crank-Nicolson methods. The quadrature rules, to discretize the Volterra integral term, are chosen so as to be consistent with the time-stepping schemes. Further, an efficient version of the code is presented using vectorization technique in the assembling process and a comparative study is presented. Numerical example prove the flexibility of the code.

Each of the authors have an equal contribution to this work.
