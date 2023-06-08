# Multi-variable Calculus

## Notation

$$
\nabla \equiv
\left(
\frac{\partial}{\partial x},
\frac{\partial}{\partial y},
\frac{\partial}{\partial z}
\right)
$$

## Gradient

$$
\operatorname{grad} \phi = \nabla \phi
$$

- computed for a scalar valued function and returns a vector valued function.
- it point in the direction fof steepest change

## Directional Derivative

- <https://en.wikipedia.org/wiki/Directional_derivative>

## Divergence

$$
\operatorname{div} \textbf{A} = \nabla \cdot \textbf{A}
$$

## Curl

$$
\operatorname{curl} \textbf{A} = \nabla \times \textbf{A}
$$

## Change of Variables

If,

- $z = f(x,y)$
- $x = \phi(t)$
- $y = \phi(t)$

Then,

$$
\frac{df}{dt} = \frac{\partial f}{\partial x} \cdot \frac{dx}{dt} + \frac{\partial f}{\partial y} \cdot \frac{dy}{ty}
$$

If,

- $z = f(x,y)$
- $x = \phi(u, v)$
- $y = \phi(u, v)$

Then,

$$
\frac{\partial f}{\partial u} = \frac{\partial f}{\partial x} \cdot \frac{\partial x}{\partial u} + \frac{\partial f}{\partial y} \cdot \frac{\partial y}{\partial u}
$$

$$
\frac{\partial f}{\partial v} = \frac{\partial f}{\partial x} \cdot \frac{\partial x}{\partial v} + \frac{\partial f}{\partial y} \cdot \frac{\partial y}{\partial v}
$$
