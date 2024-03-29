# Combinations
A **combination** is an **arrangement** of items in which **order doesn't matter**.<br>

<br>

## Combinations without repetitions
A **k-combination of n** *without repetitions* is a **subset** of set `A` with *cardinality* `k`.<br>
The **number** of all such **k-combination of n** is denoted as `C(n,k)`.<br>

When `k = n`, **k-combination of n** is simply called **combination of n**.<br>
The **number** of all such **combinations** is denoted as `C(n)`.<br>

Since the *order doesn't matter* in combinations, it is obvious that `C(n,k) < P(n,k)`, i.e. the all *combinations* are **subset** of all *permutations*.<br>

The number of **k-combination of n** for **all** `k∈[0;n]` is the number of **all subsets** of a set `A` of `n` elements, i.e. it is **powerset**:
- `powerset = C(n,0) + C(n,1) + C(n,2) + ... + C(n,i) + ... + C(n,n-1) + C(n,n)`.

<br>

## Formulas
- `C(n,k) = P(n,k)/k!`;

<br>

## Proofs
Each **k-combination of n** *without repetitions* has `k!` **permutations**.<br>
So,
- `P(n,k) = C(n,k) * k!` **=>** `C(n,k) = P(n,k)/k!`.

<br>

## Combinations with repetitions
A **k-combination of n** *with repetitions* is a **multiset** with *cardinality* `k` that consists of elements from `A`.<br>
The **number** of all such **k-combination of n** is denoted as `C̄(n,k)`.

<br>

## Formulas
- `C̄(n,k) = C(n+k-1,k)`;
