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

swap theorem, parity corollary, det col theorem, attributes of det (transpose, swap, zero, scalar, scalar zero, col add, add k of another) (4 blocks with 0: ka+b always able transfer to triangle proved by math induct, cross)

all other 0 det lemma, minor det theorem, mismatch minor 0 det corollary (Vandermonte det)

Cramer's rule: D!=0 unique Di/D, D!=0 unique theorem, D!=0 <=> homo non-zero theorem

### matrix

matrix definition

matrix ops: A+B, kA, AB(exchangable, formulas, scalar mat), AT(sym mat, (AB)T=BTAT), detA(|AB|=|A||B|, AA*=|A|E, adjoint mat), conjugate(conjugate mat)

inverse: def(AB=BA=E, unique A^-1), **|A|!=0 <=> A invertible A&ast/|A| theorem** , AB=E => B=A^-1 corollary, attributes(A^-1, kA, AB, AT), A^-k, diagnolizable f(A)g(A)=g(A)f(A), f(A)=Pf(K)P^-1=Pdiagnol(f(ki))P^-1

matrix partition: A+B,kA,AB,AT,invA, ATA=0 <=> A=0, Cramer's rule(augmented mat)

### rank(elementary transformation and solution of linear system)

**REF(elem trans) -> mat mul**

elementary transformation and elementary matrix: def of equivalence(3 trans, ref rref standard), def of elem mat(map to trans, invertible, invertible <=> A=P1P2..Pn), A ~ B <=> B=PAQ theorem, A ~ E <=> A invertible corollary

**REF(elem trans) -> mat attr(rank,minor)**

rank: how to make non-zero rows of ref as an attribute of mat? minor with order k, non-zero minor with highest order, full rank <=> invertible, rank of ref is No. of non-zero rows, A~B => R(A)=R(B) theorem(simplify, 1 2 row, elem mat, R(A)>=R(B)), **B=PAQ => R(A)=R(B) corollary**. 

rank attr: R(A)<=min(m,n), R(A)=R(AT), A~B => R(A)=R(B) theorem, B=PAQ => R(A)=R(B) corollary, max(R(A),R(B))<=R(A,B)<=R(A)+R(B) use col trans, R(A+B)<=R(A)+R(B) (R(A+B,B)~R(A,B)), R(AB)<min(R(A),R(B)), mnp AB=0 => R(A)+R(B)<=n(nullspace), mnp AB=C R(A)=n => R(B)=R(C) (A=(E,0)T)

**solution of linear system(get R(AB) attr)**

n is column number of A

0 solution <=> R(A)!=R(A,b), 1 solution <=> R(A)[=R(A,b)]=n, many solutions <=> R(A)=R(A,b)<n theorem (prove using (E,B,d), and just prove sufficiency)

homo sys non-zero solution <=> R(A)<n theorem

have solution <=> R(A)=R(A,b) thoerem

have mat solution <=> R(A)=R(A,B) theorem

R(AB)<=min(R(A),R(B)) attr (R(A)=R(A,AB) from above, and R(AB)<=R(A,AB)=R(A))

### vector set and its linear dependency

**linear combination and linear representable**

b linear representable by A <=> R(A)=R(A,b), B linear representable by A <=> R(A)=R(A,B),  B linear representable by A => R(A)>=R(B) theorems

vector set are equivalent if mutal linear representable. (invertible matrix transformation)

**linear independent**

linear independent <=> exist linear combination, linear independent <=> R(A)=n theorem, (1)n linear dependent => n+1 also linear dependent, (2) amount > n => linear dependent (3) n linear independet and n+1 linear dependent => a_n+1 has unique linear combination from others theorems (all deducted from prev theorem). 

**rank of vector set**

def largest independent set, mat rank<=> row/col vector set rank theorem, def2 largest independent set(equivalent) corollary (R(A)<=R(B) and independent R(A) theorem), finite vector set linear combination theorem to infinite vector set

**solution vector set(nullspace)**

add/mul for homo, sub/addhomo for non-homo. homo solution vector set(largest independent set) Rs=n-R(A) (prove by (B, En-r)T), mnq AB=0 => R(A)+R(B)<=n, Ax=0 Bx=0 same solution => R(A)=R(B), R(ATA)=R(A)

**vector space**

linear attr, homo solution space, generated vector space, basis, coordinates, basis transfer XA^-1B, coordinate transform B^-1AX

### similar matrix and quadratic form

inner product(schwarz inequality), length, cos; orthognol vector set(pairwise), independent theorem, orthonormal basis, orthonormalize(Schimidt), orthogonol matrix(ATA=E), orthogonal mat<=>orthonormal col vector theorem, attributes(AT,AB,|A|=1/-1), orthognol transformation(||x|| same)

eigen value, eigen vector, eigen equation, eigen polynomial, tr, |A|, k^2, 1/k, ki diff => all pi linear independent theorem, k1 k2 diff => p1+p2 not eigen vector

similar matrix: A=PBP^-1 => same eigen polynomial => same eigen values theorem, A=PVP^-1 => eigen values of A are V diagnols corollary, diagnolizable <=> n linear independent eigen vectors theorem, n diff eigen values => diagbolizable corollary

symmetric matrix: real eigen values thus real eigen vectors theorem, diff k => orthognol theorem, always diagnolizable to orthonomal mat theorem(not proved), k has same m roots => R(A-kE)=n-m => m independent eigen vectors corollary

quadratic form: function need to be presented in standard form, canonical form, 1. quadratic form one to one map to symmetric matrix, rank of quadratic form, 2. congruent CTAC (C invertible) (also symmetric and same rank), quadratic form always can convert to standard form theorem, quadratic from alway can convert to canonical form corollary

complete the square method: quadratic form to non-unique standard form is not unique

positive definite quadratic form: positive definite def, not only same rank but also same number of pos term for different quadratic form(inertia theorem not proved) (positive inertia index), positive definite <=> n positive inerita index theorem,  positive definite <=> n positive eigen value corollary, Hurwitz theorem(main minor)(not proved)

### linear space and linear transformation

linear space Vn: def(closed + linear operations rules), properties (0,neg <=> product 0 or neg)

dimension, basis, and coordinates: def(linear independent + represent all), isomorphism(1 to 1 to Rn, hold linear correspondence on add and scala)

basis/coordinates transformation: B=AP(P=A^-1B), B xb=A xa(xb=P^-1 xa) theorem

linear transformation: def(mapping, 2 condition), properties(0 neg, linear combination, linear dependent, image space(T(Vn)), kernel(St))

linear transformation and matrix: lineat trans <=> mat(on some basis), lineat trans one to one mat(on some basis), def( T(a1,...an), T[(a1,...an)x]=(a1...an)Ax), linear trans and basis(B=P^-1AP, P is A basis =>B basis), rank of linear trans is rank of T(Vn) is rank of A
