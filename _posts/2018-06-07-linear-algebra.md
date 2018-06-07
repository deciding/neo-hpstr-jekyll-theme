### cs229 suppliment

**matrix multiplication**

| diag+symm | inverse | rank |
|:----------|:--------|:-----|
| tr,norm | det | rank |
| diag,transpose,1/2(A+AT) 1/2(A-AT) | A^-1, adj(A), eigenspace(tr,det,rank) | colspace R, nullspace N, Proj(y;A) |
| diagnol mat(eigen values), symmetric mat(quadratic form, PSD, PD/ND -> full rank, use UTAU to judge PD/ND), diagnolizable(symmetric) | non-singular/invertible mat, orthognal mat(norm) | full rank mat(invertible) | 

UTU=I(m>n, orthonormal), Proj(y;A)=A(ATA)^-1ATy (m>n, full rank), gram mat ATA is PSD( it is PD when m>n and full rank)

min xTAx, s.t. xTx=1

**matrix calculus**: Gradient, Hessian, quadratic and linear gradient, LMS, det grad, constrained quadratic form

### tongji
