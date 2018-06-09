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

### determinant 

number of inverse, parity of inverse number, definition of det(det of diagnol, right diagnol, triangle)

swap theorem, parity corollary, det col theorem, attributes of det (transpose, swap, zero, scalar, scalar zero, col add, add k of another) (4 blocks with 0, cross)

all other 0 det lemma, minor det theorem, mismatch minor 0 det corollary (Vandermonte det)

Cramer's rule: D!=0 unique Di/D, D!=0 unique theorem, D!=0 <=> homo non-zero theorem

### matrix

matrix definition

matrix ops: A+B, kA, AB(exchangable, formulas, scalar mat), AT(sym mat, (AB)T=BTAT), detA(|AB|=|A||B|, AA*=|A|E, adjoint mat), conjugate(conjugate mat)

inverse: def(AB=BA=E, unique A^-1), |A|!=0 <=> A invertible A*/|A| theorem, AB=E => B=A^-1 corollary, attributes(A^-1, kA, AB, AT), A^-k, diagnolizable f(A)g(A)=g(A)f(A), f(A)=Pf(K)P^-1=Pdiagnol(f(ki))P^-1

matrix partition: A+B,kA,AB,AT,invA, ATA=0 <=> A=0, Cramer's rule(augmented mat)

### rank(elementary transformation and solution of linear system)

**ref(elem trans) -> mat mul**

elementary transformation and elementary matrix: def of equivalence(3 trans, ref rref standard), def of elem mat(map to trans, invertible, invertible <=> A=P1P2..Pn), A ~ B <=> B=PAQ theorem, A ~ E <=> A invertible corollary

**ref(elem trans) -> mat attr**

rank: how to make non-zero rows of ref as an attribute of mat? minor with order k, non-zero minor with highest order, full rank <=> invertible, rank of ref is No. of non-zero rows, A~B => R(A)=R(B) theorem, B=PAQ => R(A)=R(B) corollary. 

rank attr: R(A)<=min(m,n), R(A)=R(AT), A~B => R(A)=R(B) theorem, B=PAQ => R(A)=R(B) corollary, max(R(A),R(B))<=R(A,B)<=R(A)+R(B) use col trans, R(A+B)<=R(A)+R(B) (R(A+B,B)~R(A,B)), R(AB)<min(R(A),R(B)), mnp AB=0 => R(A)+R(B)<=n, mnp AB=C, R(A)=n => R(B)=R(C) (A=(E,0)T)

**solution of linear system(get R(AB) attr)**

0 solution <=> R(A)!=R(A,b), 1 solution <=> R(A)[=R(A,b)]=n, many solutions <=> R(A)=R(A,b)<n theorem (prove using (E,B,d), and just prove sufficiency)

homo sys non-zero solution <=> R(A)<n theorem

have solution <=> R(A)=R(A,b) thoerem

have mat solution <=> R(A)=R(A,B) theorem

R(AB)<=min(R(A),R(B)) attr (R(A)=R(A,AB) from above, and R(AB)<=R(A,AB)=R(A))
