# Basics
A **set**, *informally*, is a **collection of objects**.<br>
The objects in a *set* are called its **elements**. If `a` is a **member** (or **element**) of `A`, the notation `a ∈ A` is used.<br>

There are 2 approaches to describe sets:
- by **listing all elements** surrounded with curly brackets `{ }`;
- using **set-builder notation** (aka **set comprehension**) `{x: P(x)}`, which means set of all `x` belonging to some set `X` such that predicate `P(x)` is `true`;
  
<br>

**Empty set** (aka **null set**) is the set with **no** elements. It is expressed as `{}` or `∅`.<br>
**Singleton** ia s set which has **only one** element, e.g. `{x}`.<br>

If `A` has exactly `n` distinct elements we write `|A| = n` and call `n` the **size** or **cardinality** of `A`.<br>

For example, `|{1,2}| = 2`.<br>

<br>

Let `A` and `B` be sets:<br>
- `x∈A` means `x` is an *element of* `A`;
- `x∉A` means `x` is **not** an *element of* `A`;

<br>

# Subset
- `A ⊆ B` means `A` is a **subset** of `B` or `A` is **contained in** `B`, in other words **every** element of `A` is **also** an element of `B`;
  - **formal defenition**: `A ⊆ B, if ∀ a∈A ⇒ b∈B`;
  - also `B` is called a **superset** of set `A` and denoted `B ⊇ A`;
- If `A ⊆ B and A ⊆ B` => `A = B`;
- `A ⊈ B` means `A` is **not** a **subset** of `B`.
- `A ⊊ B` means `A` is a **proper subset** of `B`, in other words `A` is a **subset** of `B` **but** `A ≠ B`;
  - **formal defenition**: `A ⊊ B, if A ⊆ B and A ≠ B`;
  - `B` is called a **proper superset** of set `A` and denoted `B ⊋ A`;

<br>

Some authors use the symbols `⊂` and `⊃` to indicate **subset** and **superset** respectively; that is, with the same meaning as and instead of the symbols `⊆` and `⊇`.<br>
Some authors use the symbols `⊂` and `⊃` to indicate **proper subset** and **proper superset** respectively; that is, with the same meaning as and instead of the symbols `⊊` and `⊋`.<br>

Example, consider set `A = {1,3,5}`, then 
- set `B = {1,5}` is a **proper subset** of `A`: `B ⊊ A`, also `B` is a **subset** of `A`: `B ⊆ A`;
- set `C = {1,3,5}` is a **subset** of `A`: `C ⊆ A`, but it is **not** a **proper subset** of `A` since `C = A`;
- set `D = {1,4}` is not even a subset of `A`, since 4 is **not** an **element** of `A`.

<br>

## Properties
- Each set **contains itself**, i.e. `A ⊆ A`.
- **Null set** `∅` is a **subset** of any set.
- If set `B` is a **subset** of set `A`, then `B ∩ A = B`.
- If set `B` is a **subset** of set `A`, then `B ∪ A = A`.

<br>

## Trivial subsets
**Trivial subsets** of set `A` are **empty set** `{}` and **set itself** `A`.<br>

<br>

# Disjoint sets
Two sets are said to be **disjoint sets** if they **have no element in common**.<br>
Equivalently, **two disjoint sets are sets whose intersection is the empty set**. Two sets `A` and `B` are called **disjoint** if `A ∩ B = ∅`.<br>
For example, `{1, 2, 3}` and `{4, 5, 6}` are **disjoint sets**, while `{1, 2, 3}` and `{3, 4, 5}` are **not disjoint**.<br>
