# Combinations
A **combination** is an **arrangement** of items in which **order doesn't matter**.<br>

<br>

## Combinations without repetitions
A **k-combination** *without repetitions* of `A` is a **subset** of `A` with *cardinality* `k`.<br>
The **number** of all such **k-combinations** is denoted as `C(n,k)`.<br>

When `k = n`, **k-combination of n** is simply called **combination of n**.<br>
The **number** of all such **combinations** is denoted as `C(n)`.<br>

Since the *order doesn't matter* in combinations, it is obvious that `C(n,k) < P(n,k)`, i.e. the all *combinations* are **subset** of all *permutations*.<br>

The number of **k-combinations** for **all** `k` is the number of **all subsets** of a set `A` of `n` elements, it is **power set**.<br>
`Power set = C(n,0) + C(n,1) + C(n,2) + ... + C(n,n-1) + C(n,n)`.

<br>

## Formulas
- `C(n,k) = P(n,k)/k!`;

<br>

## Proofs
Each **k-combination** of a set `A` of `n` members has `k!` **permutations** so `P(n,k) = C(n,k) * k!` **=>** `C(n,k) = P(n,k)/k!`.

<br>

## Combinations with repetitions
A **k-combination** *without repetitions* (aka **k-multisubsets**) of `A` is a **multiset** with *cardinality* `k` that consists of elements from `A`.<br>
The **number** of all such **k-multisubsets** is denoted as `C̄(n,k)`.

<br>

## Formulas
- `C̄(n,k) = C(n+k-1,k)`;
