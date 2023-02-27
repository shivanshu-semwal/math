# Linear Algebra

## Inverse of a matrix

$$
A^{-1} = {\frac {1}{\det(A)}}(\operatorname {adj} (A))
$$

## Elementary Row Transformations

- $R_i \leftrightarrow R_j$ interchange any tow rows
- $R_i \rightarrow kR_i, k \ne 0$
- $R_i \rightarrow R_i + k R_j, k \ne 0$

## Rank of a matrix $\rho(A)$

### Definition

Rank of a matrix is $r$ iff

- it has at least one non zero minor of order $r$
- every minor of order higher than $r$ is 0

## Echelon form - upper triangular matrix

- number of non-zero rows in this form of matrix is equal to rank of matrix

## Normal Form

Any of these forms

$$
\left[ \textbf{I}_n \right]
$$

$$
\left[\begin{array}{c | c}
\mathbf{I}_n & 0 \\
\end{array}\right] \\
$$

$$
\left[\begin{array}{c}
\mathbf{I}_n \\
\hline
0
\end{array}\right]
$$

$$
\left[\begin{array}{c | c}
\mathbf{I}_n & 0 \\
\hline
0            & 0
\end{array}\right]
$$

here rank of these matrix is $n$

## Solution of Linear Equations

$$
AX = B
$$

- $B = 0$
    - homogeneous linear system of equations
    - if $\rho(A) = \text{no of unknowns} \implies$ unique trivial solution, all equal to 0
    - if $\rho(A) \ne \text{no of unknowns} \implies$ infinite no of non-trivial solutions
- $B \ne 0$
    - non homogeneous linear system of equations
    - augumented matrix $[A | B]$
        - if $\rho([A|B]) = \rho(A)$
            - consistent
            - $\rho(A) = \text{no of unknowns}$ - unique solution
            - $\rho(A) \ne \text{no of unknowns}$ - infinite many
                solutions
        - if $\rho([A|B]) \ne \rho(A)$
            - inconsistents
            - no solutions

## Linearly Dependent and Linearly Independent Vectors

Vectors $X_1, X_2, \dots, X_n$ are said to be linearly dependent, iff
$\exists$ $\lambda_1, \lambda_2 \dots, \lambda_n$ $\lambda_i \ne 0$ and
$\sum_{i=0}^{n} \lambda_i X_i = 0$

Vectors $X_1, X_2, \dots, X_n$ are said to be linearly independent, iff
$\sum_{i=0}^{n} \lambda_i X_i = 0$ only when all $\lambda_i = 0$

Vectors, $X_1, X_2, \dots, X_n$, are linearly independent if
$\rho(
\begin{bmatrix}
X_1 & X_2 & \dots & X_n \\
\end{bmatrix}
) = n$, else they are linearly dependent.

## Characteristics Equations

Given a square matrix $\textbf{A}$,
$|\textbf{A} - \lambda \textbf{I} | = 0$ is its characteristics
equation.

### Cayle Hamilton Theorem

Every square matrix satisfies its own characteristics equation

## Eigen Values

- Solution to this equation gives eigen values.

## Eigen Vectors

- corresponding to each eigen value
- the non zero solution to the equation
- $(\textbf{A} - \lambda \textbf{I}) \textbf{X} = 0$
- give eigen vector

## Diagonalization of a Matrix

- Steps to diagonalize a matrix
    - find characteristics equation
    - find eigen values $\lambda_1, \lambda_2 \dots, \lambda_n$
    - find eigen vector $X_1, X_2, \dots, X_n$
    - construct moadal matrix $P = [X_1 X_2 \dots X_n]$
    - find $P^{-1}$
    - finally
        $D = P^{-1}AP = \operatorname{diag}(\lambda_1, \lambda_2 \dots, \lambda_n)$
- property of diagonal matrix
    - $A^n = PD^nP^{-1}$
