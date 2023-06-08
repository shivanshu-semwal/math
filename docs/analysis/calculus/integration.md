# Integration

## Definition

## Indefinite Intergral

$$
\int x^n dx = \frac{x^{n+1}}{n+1} + C
$$

$$
\int dx = + C
$$

$$
\int \frac{1}{x} dx = \ln|x|+ C
$$

$$
\int e^x dx = e^x + C
$$

$$
\int \sin(x) dx = - \cos(x) + C
$$

$$
\int \cos(x) dx = \sin(x) + C
$$

$$
\int \tan(x) dx = \ln|\sec(x)|+ C
$$

$$
\int \cot(x) dx = -\ln|\csc(x)| + C
$$

$$
\int \sec(x) dx = \ln|\sec(x) + \tan(x)|+ C
$$

$$
\int \csc(x) dx = \ln|\csc(x) - \cot(x)| + C
$$

$$
\int f(ax+b) dx = \frac{1}{a}f(ax+b) + C
$$

$$
\int \frac{f'(x)}{f(x)} dx = \ln|f(x)| + C
$$

## Integration by Parts

$$
\int u dv = uv - \int v du
$$

$$
\int uv'dx = uv - \int vu'dx
$$

## Integration of Inverse Function

$$
\int f(x)dx = F(x) + C
$$

$$
\int f^{-1}(x)dx = xf^{-1}(x) - F(f^{-1}(x)) + C
$$

## Integration by substitution

$$
\int f(x) dx = \int f(u(y)) u'(y) dy
$$

## Definite Integral

$$
\int_a^b f(x) dx = - \int_b^a f(x) dx
$$

$$
\int_0^a f(x) dx = \int_0^a f(a-x) dx
$$

$$
\int_a^b f(x) dx = \int_a^b f(a+b-x) dx
$$

$$
\int_{-a}^{a} f(x) dx = { \begin{cases}
  2 \int_0^a f(x) dx,&{\text{if }} f(x) = f(-x) \\
  0,&{\text{if }} f(x) \ne f(-x)
  \end{cases}
}
$$

$$
\int_a^b f(x) dx + \int_{f^{-1}(a)}^{f^{-1}(b)} f^{-1}(x) =
  bf^{-1}(b) - af^{-1}(a)
$$
