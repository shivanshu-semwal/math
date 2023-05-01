# Special Functions

## Gamma Function

$$
\Gamma (z)=\int_{0}^{\infty} t^{z-1}e^{-t} dt
$$

- $\Gamma(n + 1) = n \Gamma(n)$
- $\Gamma(n) = (n-1)!$, for every positive integer
- $\Gamma(1/2) = \sqrt{\pi}$

## Beta function (Euler integral of first kind)

$$
\mathrm {B} (z_{1},z_{2}) =
\int_{0}^{1}t^{z_{1}-1}(1-t)^{z_{2}-1}dt
$$

- symmetric $\mathrm {B} (z_{1},z_{2}) = \mathrm {B} (z_{2},z_{1})$
- relationship to gamma
  $$
  \mathrm {B} (z_{1},z_{2}) =
  \frac{\Gamma(z_1)\Gamma(z_2)}{\Gamma(z_1+z_2)}
  $$
- $$
  \mathrm {B} (z_{1},z_{2}) =
  \int_{0}^{\infty} \frac{t^{z_1 - 1}}
  {(1+x)^{z_1 + z_2}} dt
  $$
- $$
  \mathrm {B} (z_{1},z_{2}) = 2
  \int_{0}^{\pi/2} \sin^{2z_1 - 1}(t) \cos^{2z_2 - 1}(t) dt
  $$
