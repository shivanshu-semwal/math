# Vector

## Scalar product

$$
\textbf{a} \cdot \textbf{b} =
\|\mathbf {a} \|\ \|\mathbf {b} \|\cos \theta =
a_1b_1 + a_2b_2 + a_3b_3
$$

## Vector product, cross product

$$
\textbf{a} \times \textbf{b} =
(\|\mathbf {a} \|\ \|\mathbf {b} \|\sin \theta) \hat{\textbf{n}}=
\begin{vmatrix}
\textbf{i} & \textbf{j} & \textbf{j} \\
a_1        & a_2        & a_3        \\
b_1        & b_2        & b_3
\end{vmatrix}
$$

## Triple product

$$[\textbf{a}, \textbf{b}, \textbf{c}] =
(\textbf{a} \times \textbf{b}) \cdot \textbf{c} =
\textbf{a} \cdot (\textbf{b} \times \textbf{c}) =
\begin{vmatrix}
a_1 & a_2 & a_3 \\
b_1 & b_2 & b_3 \\
c_1 & c_2 & c_3 \\
\end{vmatrix}
$$

## two time cross product

$$
\textbf{a} \times (\textbf{b} \times \textbf{c}) =
(\textbf{a} \cdot \textbf{c})  \textbf{b} -
(\textbf{a} \cdot \textbf{b}) \textbf{c}
$$

## Vector calculus

### Notation

$$
\nabla \equiv
\left(
\frac{\partial}{\partial x},
\frac{\partial}{\partial y},
\frac{\partial}{\partial z}
\right)
$$

- Gradient, $\operatorname{grad} \phi = \nabla \phi$
- Divergence, $\operatorname{div} \textbf{A} = \nabla \cdot \textbf{A}$
- Curl, $\operatorname{curl} \textbf{A} = \nabla \times \textbf{A}$
