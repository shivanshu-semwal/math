# Relation

- <https://en.wikipedia.org/wiki/Relation_(mathematics)>

## Types

Let, $R$ be relation on $X$

- Reflexivity
    - Reflexive $\forall x \in X, xRx$
    - Irreflexive $\forall x \in X, \neg xRx$
- Symmetry
    - Symmetric $xRy \rightarrow yRx$
    - Antisymmetric $xRy \land yRx \rightarrow x = y$
    - Asymmetric $xRy \rightarrow \neg yRx$
- Transitive
    - $xRy \land yRz \rightarrow xRz$
- Connectedness
    - Connected $\forall x, y \in X \text{ if } x \neq y \text{ either } xRy \text{ or } yRx$
    - Strongly Connected $\forall x, y \in X \text{ either } xRy \text{ or } yRx$
- Uniqueness property
    - Injective, left-unique $\forall x, y, z, xRy \land zRy \rightarrow x=z$
    - Functional, right-unique $\forall x, y, z, xRy \land xRz \rightarrow y=z$
- Totality Properties
    - Serial, left-total, total $\forall x \in X, \exists y \in X | xRy$
    - Surjective, right-total, onto $\forall y \in X, \exists x \in X | xRy$

## Combination of Properties

### Equivalence Relation

- A relation that is reflexive, symmetric, and transitive.
- It is also a relation that is symmetric, transitive, and serial, since these properties imply reflexivity.

#### Examples

- Modulo operation, $\{(x,y)|x \equiv y \mod m, x, y \in X\}$

#### Equivalence Classes

Given a equivalence relation $R$ on $X$, equivalence class of $x$ is given as $[x] = \{y | xRy\}$

- Equivalent classes divide the set $X$ into partition (disjoint sets)
- Union of all equivalent classes is equal to the set itself

### Orderings

- Partial Order
- Total Order

### Uniqueness

- One-to-one: Injective and functional.
- One-to-many: Injective and not functional.
- Many-to-one: Functional and not injective.
- Many-to-many: Not injective nor functional.

### Uniqueness and totality properties

- A function
    - A binary relation that is functional and total.
- An injection
    - A function that is injective.
- A surjection
    - A function that is surjective.
- A bijection
    - A function that is injective and surjective.
    - Inverse of only these functions is possible.

## Closures

Let, $R = X \times X$

- Reflexive Closure $R_e^+ = R \cup \{(a, a) | a \in X\}$
- Symmetric Closure $R_s^+ = R \cup \{(a, b) | (b, a) \in R\}$
- Transitive Closure $R_t^+ = R \cup \{(a, c) | (a, b) \in R \land (b, c) \in R\}$

## Warshall's algorithm for Transitive Closure

Given. $R = X \times X$, represent $R$ in matrix form, $M_{n \times n}$

- for $k$ in $(1, n)$
    - $A = \{x | M_{x,k} = 1\}$, represent $k$ th col
    - $B = \{x | M_{k,x} = 1\}$, represent $k$ th row
    - find, $R' = R \cup (A \times B)$ and represent $R'$ in matrix form $M'$
    - set, $M = M'$

- convert $M$ to relation, which will be the transitive closure of $R$

- <https://math.stackexchange.com/questions/369134/how-to-use-warshalls-algorithm>
- <https://en.wikipedia.org/wiki/Floyd%E2%80%93Warshall_algorithm>
