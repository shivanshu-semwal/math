# Order Theory

- <https://en.wikipedia.org/wiki/Order_theory>
- <https://en.wikipedia.org/wiki/Partially_ordered_set>
- <https://en.wikipedia.org/wiki/Lattice_(order)>

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
