# Number Theory

## Modular arithmetic

- $a \equiv (a-p) \mod p$
- $a \equiv (a+np) \mod p$, $n \in \text{Z}$
- $a \equiv b \mod p \implies a - k \equiv b - k \mod p$
- $a_1 \equiv b_1 \mod p$ and $a_2 \equiv b_2 \mod p$, then
    - $a_1 + a_2 \equiv b_1 + b_2 \mod p$
    - $a_1 - a_2 \equiv b_1 - b_2 \mod p$
    - $a_1 \times a_2 \equiv b_1 \times b_2 \mod p$
- $(ab) \mod p = ((a \mod p)(b \mod p))\mod p$
- $(a+b) \mod p = ((a \mod p) + (b \mod p))\mod p$

### Fermat little theorem

Given, a no. $a$ and a prime no. $p$,

$$
a^{p-1} \equiv 1 \mod p
$$

### Euler's Theorem

Given no $a$ and $b$, and $a$ and $b$ are co-primes

$$
a^{\phi(b)} \equiv 1 \mod b
$$

- Euler's totient function,
  $\phi(n) = \#\{x: \gcd(x, n) = 1 \text{ and } x \in \{1,2,...,n\}\}$

### Wilson's theorem

Given a prime no $a$,

$$
(a-1)! \equiv -1 \mod a
$$

## Applications

### Modulus of any given Exponent

- find the value of

$$
a^b \mod c
$$

- find the cycle length, let it be $l$
- then, $a^b \mod c = a^{b \mod l} \mod c$

Example,

- $5^{123} \mod 7$
    - $5^{123} \mod 7$
    - use fermat theorem, $a^{p-1} \equiv 1 \mod p$, for prime $p$, so cycle length is 6
    - $5^{123 \mod 6} \mod 7 = 6$

- Finding Unit Digit in Exponent, i.e. mod 10
    - Find, $x^n \mod 10$, first reduce $x$ to $(x \mod 10)$, so we only have to find rules for $\{2, ..., 9\}$
    - $2^n \equiv f(n \mod 4) \mod 10, n \ne 0 \text{, where, } f(x) = \{(0, 6), (1, 2), (2, 4), (3, 8)\}$
    - $3^n \equiv f(n \mod 4) \mod 10, n \ne 0 \text{, where, } f(x) = \{(0, 1), (1, 3), (2, 9), (3, 7)\}$
    - $4^n \equiv f(n \mod 2) \mod 10, n \ne 0 \text{, where, } f(x) = \{(0, 6), (1, 4)\}$
    - $5^n \equiv 5 \mod 10$
    - $6^n \equiv 6 \mod 10$
    - $7^n \equiv f(n \mod 4) \mod 10, n \ne 0 \text{, where, } f(x) = \{(0, 1), (1, 7), (2, 9), (3, 3)\}$
    - $8^n \equiv 2^{3n} \mod 10$
    - $9^n \equiv f(n \mod 2) \mod 10, n \ne 0 \text{, where, } f(x) = \{(0, 1), (1, 9)\}$

- Finding the last two digits in Exponent, i.e. mod 100
    - Find, $x^n \mod 100$, first reduce $x$ to $(x \mod 100)$, so we only have to find rules for $\{2, ..., 99\}$, which is still huge
    - Use this theorem, $(10x + y)^{n} \equiv 10nxy^{n-1} + y^n \mod 100$
        - Proof:
            - $(10x + y)^{n} \mod 100$
            - Using binomial expansion, $y^n + C_1^n(10x)y^{n-1} + C_2^n(10x)^2y^{n-2} + ... + (10x)^n \mod 100$
            - We know that, $(10x)^a \equiv 0 \mod 100$, for $a >=2$, so our expression reduce to
            - $y^n + C_1^n 10xy \mod 100 = 10nxy + y^n \mod 100$
    - Now we only have to find, $y^n \mod 100$ and $y^{n-1} \mod 100$, and $y \in \{1,2,\cdots,9\}$
    - $2^n \equiv f(n \mod 2) \mod 100, n \ne 0 \text{, where, } f(x) = \{(0, 24), (1, 76)\}$
    - $3^n \equiv 81^{\lfloor n/4 \rfloor} + 3^{n \mod 4} \mod 100$, now use the theorem given above for 81
    - $4^n \equiv 2^{2n} \mod 100$
    - $5^n \equiv 25 \mod 100$
    - $6^n \equiv 2^n 3^n \mod 100$
    - $7^n \equiv f(n \mod 4) \mod 100, n \ne 0 \text{, where, } f(x) = \{(0, 1), (1, 7), (2, 49), (3, 43)\}$
    - $8^n \equiv 2^{3n} \mod 100$
    - $9^n \equiv 81^{\lfloor n/2 \rfloor} + 9^{n \mod 2} \mod 100$, now use the theorem given above for 81
