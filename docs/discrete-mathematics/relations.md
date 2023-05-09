# Relation

- <https://en.wikipedia.org/wiki/Relation_(mathematics)>

## Types

Let, $R$ be relation on $X$

- Reflexivity
    - Reflexive
        - $\forall x \in X, xRx$
    - Irreflexive
        - $\forall x \in X, \neg xRx$
- Symmetry
    - Symmetric
        - $xRy \rightarrow yRx$
    - Antisymmetric
        - $xRy \land yRx \rightarrow x = y$
    - Asymmetric
        - $xRy \rightarrow \neg yRx$
- Transitive
    - $xRy \land yRz \rightarrow xRz$
- Connectedness
    - Connected
        - $\forall x, y \in X \text{ if } x \neq y \text{ either } xRy \text{ or } yRx$
    - Strongly Connected
        - $\forall x, y \in X \text{ either } xRy \text{ or } yRx$
- Uniqueness property
    - Injective, left-unique
        - $\forall x, y, z, xRy \land zRy \rightarrow x=z$
    - Functional, right-unique
        - $\forall x, y, z, xRy \land xRz \rightarrow y=z$
- Totality Properties
    - Serial, left-total, total
        - $\forall x \in X, \exists y \in X | xRy$
    - Surjective, right-total, onto
        - $\forall y \in X, \exists x \in X | xRy$

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

#### Partial order

- A relation that is
    - reflexive
    - antisymmetric
    - transitive
- means that there is order between some elements but not all elements
- all elements are not comparable
- for having order between all elements, relation should also be connected

- A set $S$ together with a partial order relation $R$ is called POSET partially ordered set. $(S, \leqslant)$

##### Hasse Diagram

- To represent partial order with a hasse diagram, make a directed graph of relation,
    - remove reflexive edges
    - remove transitive edges

- Minimal Elements
    - set of minimal elements
    - $x$ is minimal element, if $\nexists y \in X | yRx$
    - starting nodes elements
- Maximal Elements
    - set of maximal elements
    - $x$ is maximal element, if $\nexists y \in X | xRy$
    - leaves of the diagram
- Least element
    - it is unique if it exist
    - $x$ is least element if $\forall y \in X, xRy$
- Greatest element
    - it is unique if it exist
    - $x$ is greatest element if $\forall y \in X, yRx$
- Lower Bounds
    - set of all lower bound
    - given $T \subseteq X$, $x$ is lower bound of $T$ if $\forall y \in T, xRy$
- Upper Bounds
    - set of all upper bound
    - given $T \subseteq X$, $x$ is upper bound of $T$ if $\forall y \in T, yRr$
- Least Upper Bound, LUB, Superemum, join, $\land$
    - unique if exists
    - min(set all upper bounds)
    - given $T \subseteq X$, least upper bound is minimum of upper bound of $T$
- Greatest Lower Bound, GLB, infimum, meet, $\lor$
    - unique if exists
    - max(set of the lower bounds)
    - given $T \subseteq X$, greatest lower bound is maximum of lower bound of $T$
- Meet Semilattice
    - Given poset $(X,R)$ is meet semilattice if $\forall x, y \in X, \text{GLB}(x, y)$ exists
- Join Semilattice
    - Given poset $(X,R)$ is join semilattice if $\forall x, y \in X, \text{LUB}(x, y)$ exists
- Lattice
    - A poset is lattice if it both meet semilattice and join semilattice
- Complete lattice
    - Given Poset $(X,R)$ is complete lattice if $\forall S \subseteq X | \text{GLB}(S) \neq \phi \land \text{LUB}(S) \neq \phi$
    - every finite lattice is complete
- Bounded lattice
    - if there is greatest and least element in lattice, it is called bounded
    - complement of an element
        - $1$ is symbol for the greatest element and $0$ is for least element
        - $a$ is complement of $b$ if,
            - $a \lor b = 1, \text{LUB}(a,b) = 1$, $\lor$ means meet
            - $a \land b = 0, \text{GLB}(a,b) = 0$, $\land$ means join
        - a given lattice is complemented lattice if every element has atleast one complement
    - Distributive lattice
        - a lattice is distributive if it follows distributive properties on join and meet
        - $a \lor (b \land c) = (a \lor b) \land (a \lor c)$
        - $a \land (b \lor c) = (a \land b) \lor (a \land c)$
        - every element in distributive lattice has atmost one complement, and this is sufficient condition to test
          if lattice is distributive

#### Strict partial order

- A relation that is
    - irreflexive
    - antisymmetric
    - transitive

#### Total order or linear order

- A relation that is
    - reflexive
    - antisymmetric
    - transitive
    - connected
- all elements are comparable

#### Strict total order

- A relation that is
    - irreflexive
    - antisymmetric
    - transitive
    - connected.

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
