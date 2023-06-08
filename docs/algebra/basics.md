# Basics

## Equations

- Linear Equation
    - $y = ax + b$
    - Solution:
  $$
  x = \frac{-b}{a}
  $$
- Quadratic Equation
    - $y = ax^2 + bx + c$
    - Solution:
 $$
 x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
 $$
- Cubic Equation
    - $y = ax^3 + bx^2 + cx + d$
    - Solution, let
    - $\Delta _{0}=b^{2}-3ac$
    - $\Delta _{1}=2b^{3}-9abc+27a^{2}d$

$$
C={\sqrt[{3}]{\frac {\Delta_{1}\pm {\sqrt {\Delta _{1}^{2}-4\Delta_{0}^{3}}}}{2}}}
$$

$$
\xi = \frac{-1 + \sqrt{-3}}{2}
$$

$$
x_{k}=-{\frac {1}{3a}}\left(b+\xi ^{k}C+{\frac {\Delta _{0}}{\xi ^{k}C}}\right),\qquad k\in \{0,1,2\}
$$

## Factorization

- $a^2 - b^2 = (a-b)(a+b)$
- $a^3 - b^3 = (a-b)(a^2 + ab -b^2)$
- $a^3 + b^3 = (a+b)(a^2 - ab -b^2)$

## Logarithms

### Definition

- $\log_b c = a \implies b^a = c, b \not= 0$

### Properties

- $\log_a m^n = n \log_a m$
- $\log_a (mn) = \log_a m  + \log_a n$
- $\log_a \frac{m}{n} = \log_a m - \log_a n$
- $\log_a 1 = 0$
- $\log_a a = 1$
- $\log_{a^b} m = \frac{1}{b}\log_a m$
- $\log_{a^b} m^n = \frac{n}{b}\log_a m$
- $\log_a b = \frac{\log_c b}{\log_c a}$
- $\log_a b = \frac{1}{\log_b a}$
- $a^{\log_a x} = x$

### Notation

- $\log a$ refers to the base being 10
- $\ln a$ refers to base being $e$

## Complex Numbers

$$i = \sqrt{-1}$$

### Exponential Notation

$$
e^{i\theta} = \cos \theta + i \sin \theta
$$

### De Moivre's theorem

$$
(r(\cos \theta + i \sin \theta))^n = r^n (\cos n\theta + i \sin n\theta)
$$

### $n^{\text{th}}$ root of complex numbers

If, $z = re^{i\theta} = r(\cos \theta + i \sin \theta)$ then

$$
z^{1/n} = \sqrt[n]{r} e^{i(\theta + 2\pi k)/n}, k = 0, \pm1, \pm 2, \dots
$$

## Vector

### Scalar product

$$
\textbf{a} \cdot \textbf{b} =
\|\mathbf {a} \|\ \|\mathbf {b} \|\cos \theta =
a_1b_1 + a_2b_2 + a_3b_3
$$

### Vector product, cross product

$$
\textbf{a} \times \textbf{b} =
(\|\mathbf {a} \|\ \|\mathbf {b} \|\sin \theta) \hat{\textbf{n}}=
\begin{vmatrix}
\textbf{i} & \textbf{j} & \textbf{j} \\
a_1        & a_2        & a_3        \\
b_1        & b_2        & b_3
\end{vmatrix}
$$

### Triple product

$$[\textbf{a}, \textbf{b}, \textbf{c}] =
(\textbf{a} \times \textbf{b}) \cdot \textbf{c} =
\textbf{a} \cdot (\textbf{b} \times \textbf{c}) =
\begin{vmatrix}
a_1 & a_2 & a_3 \\
b_1 & b_2 & b_3 \\
c_1 & c_2 & c_3 \\
\end{vmatrix}
$$

### two time cross product

$$
\textbf{a} \times (\textbf{b} \times \textbf{c}) =
(\textbf{a} \cdot \textbf{c})  \textbf{b} -
(\textbf{a} \cdot \textbf{b}) \textbf{c}
$$