# Enumeration

## Pigeonhole Principle

- if you have more pigeon than pigeonholes then atleast one pigeonhole will have more pigeon

## Mathematical Induction

- way of proving things
- first prove it for initial values
- then assume it is true for ith value and using that prove it is also true for i+1 value

## Using different counting methods to prove things

- if you count things in one way and then in other way
- those results are equal

## Linear Order

- no. of linear orders for given set with $n$ elements

$$
n!
$$

- no. of linear order for given set with $n$ elements, if you have to choose $r$ elements

$$
n(n-1)(n-2)\cdots(n-r+1) = \frac{n!}{(n-r)!}
$$

## Binomial Theorem

$$
(x+y)^n = \sum_{i-0}^{n}\binom{n}{i}x^iy^{n-i}
$$

## Order and choice

- no. of ways to choose $r$ elements for given set of $n$ elements

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

- no. of ways to choose given set with $n$ elements,
  also $n_1$ elements are of same type, $n_2$ elements are of same type, and so on.

$$
\binom{n}{n_1, n_2, n_3, \cdots, n_k} = \frac{n!}{n_1! n_2! n_3! \cdots n_k!}
$$

## Sets and Multisets

- The number of ways of choosing $r$ objects from $n$ types of objects (with replacement or repetition allowed) is

$$
\left(\binom{n}{r}\right) = \binom{n+r-1}{r}
$$

## Sequences and Compositions

- Weak composition of $k$ into $n$ parts, is a sequence $(r_1, r_2, \cdots, r_n)$ such that $r_1 + r_2 + \cdots + r_n = k$, $0 \leq r_i \leq k$
- no. of weak composition of $k$ into $n$ parts is equal to

$$
\left(\binom{k}{n}\right)
$$

- Strong composition of $k$ into $n$ parts, is a sequence $(r_1, r_2, \cdots, r_n)$ such that $r_1 + r_2 + \cdots + r_n = k$, $1 \leq r_i \leq k$
- no. of strong composition of $k$ into $n$ parts is equal to

$$
\left(\binom{k-n}{n}\right) = \binom{k-1}{n-1}
$$

## Sequence and Partitions

- A partition is a weekly decreasing sequence of positive integers.
- E.g. partition of $n$ into $k$ parts is: $r_1 \geq r_2 \geq \cdots \geq r_k$, such that $r_1 + r_2 + \cdots + r_k = n$
- No. of partitions of $n$ is equal to $p(n)$

$$
p(n) \sim \frac{1}{4 \sqrt{3}}e^{\pi\sqrt{\frac{2n}{3}}}
$$

- Conjugate of a partition $r$ is $r_i = \#\{j | r_j \geq i\}$
- no. of self conjugate partitions of $n$ = no. of partitions of $n$ into distinct odd parts

- A set partition of a set $S$ is partitioning of $S$ into blocks $B_1, \cdots, B_k$ such that
    - $B_1 \cup \cdots \cup B_k = S$
    - $B_i \cap B_j = \phi, i \neq j$
    - $B_i \neq \phi, \forall i \in \{1, \cdots, k\}$
- No. of set partitions of a set $S$ into $k$ blocks is equal to $S(n, k)$ (stirling no of second kind)

- $S(n, 1) = 1$
- $S(n, 2) = 2^{n-1} -1$
- $S(n, n-1) = \binom{n}{2}$
