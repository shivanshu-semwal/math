# Partial Differentiation

Let $z = f(x, y)$ be a function of two independent variables $x$ and $y$,
then the derivative of $z$ with respect to $x$ keeping $y$ constant
is called the partial derivate of $z$ with respect to $x$

## Notation

$$
\frac{\partial f}{\partial x} =
f_x, \quad
\frac{\partial f}{\partial x} =
f_y, \quad
\frac{\partial^2 f}{\partial x^2} =
f_{xx}, \quad
\frac{\partial }{\partial x}
\left( \frac{\partial f}{\partial y} \right) =
f_{xy}, \quad
\frac{\partial }{\partial y}
\left( \frac{\partial f}{\partial x} \right) =
f_{yx}, \quad
\frac{\partial^2 f}{\partial y^2} =
f_{yy}
$$

## Limit of function with two variables

- limit of function with two variables
    - a function $f(x, y)$ is said to tend to limit $L$ as
    - $x \rightarrow a$ and $y \rightarrow b$
    - iff the limit $L$ is independent of the path followed by
    - the point $x, y$ as $x \rightarrow a$ and $y \rightarrow b$

$$
\lim_{(x, y) \rightarrow (a,b)} f(x, y) = L
$$

## Continuity

A function $f(x, y)$ is said to be continuous at $(a, b)$ iff

$$
\lim_{(x, y) \rightarrow (a,b)} f(x, y) = f(a, b)
$$

## Homogeneous functions

- $f(x, y)$ is homogeneous if it can be represented as

$$
f(x, y) = x^n f\left(\frac{x}{y}\right)
$$

$n$ is the called degree of the equation

### Euler's theorem - for homogeneous equations

$$
x \frac{\partial f}{\partial x} + y \frac{\partial f}{\partial y} = n f(x, y)
$$

$$
x^2 \frac{\partial f}{\partial x^2} +
2xy \frac{\partial f}{\partial x \partial y} +
y^2 \frac{\partial f}{\partial y^2}
= n(n-1) f(x, y)
$$

## Expansion of function with multiple variables

### Taylor Series

If $f(x, y)$ and all its partial derivatives upto the
$n^{th}$ order are finite and continuous for all points
$(x, y)$ where $a \le x \le a + h$, $b \le x \le b + h$ then

$$
f(a+h, b+k) = f(a, b) +
\left(
h \frac{\partial}{\partial x} +
k \frac{\partial}{\partial y}
\right)f +
\frac{1}{2!} \left(
h \frac{\partial}{\partial x} +
k \frac{\partial}{\partial y}
\right)^2f +
\dots
$$

On putting $a =0, b=0, h=x, k = y$

$$
f(x, y) = f(0, 0) +
\left(
x \frac{\partial}{\partial x} +
y \frac{\partial}{\partial y}
\right)f +
\frac{1}{2!} \left(
x \frac{\partial}{\partial x} +
y \frac{\partial}{\partial y}
\right)^2f +
\dots
$$

## Maxima and minima

- function $f(x,y)$ have local maximum at point $(a, b)$
    - iff $f(a, b) > f(a+h, b+h)$ for some small values of $h$
    - similar for minimum
- find extreme value of a function
    - find $f_x, f_y$
    - solve $f_x = 0, f_y = 0$ simultaneously
    - find $f_{xx}, f_{xy}, f_{yy}$
    - find $D = f_{xx}f_{yy} - f_{xy}^2$ at each stationary point
        - if $D>0$
            - $f_{xx} < 0$ local minimum
            - $f_{xx} > 0$ local maximum
        - else if $D<0$ no extreme values
        - else $D=0$ test fails

## Lagranage's Method of undetermined multipliers

- Used to find stationary point of function with multiple variables

Given function $f(x, y, z)$, variable $x, y, z$ are connected by the relation

$$
\phi(x, y, z) = 0
$$

Consider the lagrange function,

$$
F(x, y, z) = f(x, y, z) + \lambda \phi(x, y, z)
$$

then for stationary point,

$dF = 0$
$$
(f_{x} + \lambda \phi_{x}) dx +
(f_{y} + \lambda \phi_{y}) dy +
(f_{z} + \lambda \phi_{z}) dz = 0
$$
$$
\nabla F = 0
$$
$$
f_{x} + \lambda \phi_{x} = 0,
f_{y} + \lambda \phi_{y} = 0,
f_{z} + \lambda \phi_{z} = 0
$$

## Jacobians

Functions $u(x, y)$ and $v(x, y)$ have Jacobian(functional determinant), which is

$$
J(u, v) =
\frac{\partial(u, v)}{\partial(x, y)}
=
\begin{vmatrix}
    u_x & u_y \\
    v_x & v_y
\end{vmatrix}
$$

Similarly for $n$ functions $u_1, u_2, \dots, u_n$, and $n$ independent
variables $x_1, x_2, \dots, x_n$

$$
\frac{\partial(u_1, u_2, \dots, u_n)}{\partial(x_1, x_2, \dots, x_n)} =
\begin{vmatrix}
    (u_1)_{x_{1}} & (u_1)_{x_{2}} & \dots  & (u_1)_{x_{n}} \\
    (u_2)_{x_{1}} & (u_2)_{x_{2}} & \dots  & (u_2)_{x_{n}} \\
    \vdots        & \vdots        & \ddots & \vdots        \\
    (u_n)_{x_{1}} & (u_n)_{x_{2}} & \dots  & (u_n)_{x_{n}} \\
\end{vmatrix}
$$

### Properties of Jacobians

- if $u$ and $v$ are functions of $r$ and $s$ and $r$ and $s$ are
  functions of $x$ and $y$
  $$
  \frac{\partial(u, v)}{\partial(x, y)} =
  \frac{\partial(u, v)}{\partial(r, s)}
  \frac{\partial(r, s)}{\partial(x, y)}
  $$
- If $u_1, u_2, \dots, u_n$, and $x_1, x_2, \dots, x_n$ are related as
  follows
      - $u_1 = f_1(x_1)$
      - $u_2 = f_2(x_1, x_2)$
      - $\dots$
      - $u_n = f_n(x_1, x_2, \dots, x_n)$
  then
  $$
  \frac{\partial(u_1, u_2, \dots, u_n)}{\partial(x_1, x_2, \dots, x_n)} =
  \frac{u_1}{x_1} \frac{u_2}{x_2} \dots \frac{u_n}{x_n}
  $$
- For implicit functions - $u_1, u_2, u_3$ are implicit functions of $x_1, x_2, x_3$
    - $F_1(u_1, u_2, u_3, x_1, x_2, x_3) = 0$
    - $F_2(u_1, u_2, u_3, x_1, x_2, x_3) = 0$
    - $F_3(u_1, u_2, u_3, x_1, x_2, x_3) = 0$
  $$
  \frac{\partial(u_1, u_2, u_3)}{\partial (x_1, x_2, x_3)} =
  (-1)^3
  \frac
  {\frac{\partial (F_1, F_2, F_3)}{\partial (x_1, x_2, x_3)}}
  {\frac{\partial (F_1, F_2, F_3)}{\partial (u_1, u_2, u_3)}}
  $$