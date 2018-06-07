## cs229 suppliment

**matrix multiplication**

| diag+symm | inverse | rank |
|:----------|:--------|:-----|
| tr,norm | det | rank |
| diag,transpose,1/2(A+AT) 1/2(A-AT) | A^-1, adj(A), eigenspace(tr,det,rank) | colspace R, nullspace N, Proj(y;A) |
| diagnol mat(eigen values), symmetric mat(quadratic form, PSD, PD/ND -> full rank, use UTAU to judge PD/ND), diagnolizable(symmetric) | non-singular/invertible mat, orthognal mat(norm) | full rank mat(invertible) | 

UTU=I(m>n, orthonormal), Proj(y;A)=A(ATA)^-1ATy (m>n, full rank), gram mat ATA is PSD( it is PD when m>n and full rank)

min xTAx, s.t. xTx=1

**matrix calculus**: Gradient, Hessian, quadratic and linear gradient, LMS, det grad, constrained quadratic form

## tongji

### number of inverse, parity of inverse number, definition of det(det of diagnol, right diagnol, triangle)

swap theorem, parity corollary, det col theorem, attributes of det (transpose, swap, zero, scalar, scalar zero, col add, add k of another) (4 blocks with 0, cross)

all other 0 det lemma, minor det theorem, mismatch minor 0 det corollary (Vandermonte det)

Cramer's rule: D!=0 unique Di/D, D!=0 unique theorem, D!=0 <=> homo non-zero theorem

### matrix

matrix definition

matrix ops: A+B, kA, AB(exchangable, formulas, scalar mat), AT(sym mat, (AB)T=BTAT), detA(|AB|=|A||B|, AA*=|A|E, adjoint mat), conjugate(conjugate mat)

inverse: def(AB=BA=E, unique A^-1), |A|!=0 <=> A invertible A*/|A| theorem, AB=E => B=A^-1 corollary, attributes(A^-1, kA, AB, AT), A^-k, diagnolizable f(A)g(A)=g(A)f(A), f(A)=Pf(K)P^-1=Pdiagnol(f(ki))P^-1

matrix partition: A+B,kA,AB,AT,invA, ATA=0 <=> A=0, Cramer's rule(augmented mat)

