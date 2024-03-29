# k-tuples
A **tuple** is an **ordered collection** of elements taken from a set and may have **duplicate** elements.<br>
A **tuple** of size `k` (**tuple** of `k` elements) is called an `k-tuple`.<br>
**Notation**: **parentheses** `( )` or **angle brackets** `⟨ ⟩`.<br>
**Example**: `(2,7,4,1,7)` denotes a **5-tuple**.<br>
**Orderedness**: `(1,2,3)` is **different** from `(3,2,1)`, i.e. `(1, 2, 3) ≠ (3, 2, 1)` .<br>

<br>

The general rule for the identity of two **k-tuples** is `(a1, a2, …, an) = (b1, b2, …, bn)` if and only if `a1 = b1`, `a2 = b2`, ..., `an = bn`.

The number of **k-tuples** that can be selected from set `{1, 2, . . . , n}` **without** repeating elements and is `P(n,k)`.

<br>

# Permutations
A **permutation** is an **arrangement** of items in a **particular order**, i.e. **order matters**.

<br>

## Permutations without repetitions
Consider a set `A = {1,2,3, ..., n}`.<br>
A **k-permutation of n** *without repetitions* (aka **partial permutations**, **k-arrangements of n**) is **all ordered tuples** of length `k, k <= n` that consist of **distinct** elements from `A, |A| = n`.<br>
The **number** of all such **k-permutations** is denoted as `P(n,k)`.<br>

When `k = n`, **k-permutation of n** is simply called **permutation of n**.<br>
The **number** of all such **permutations** is denoted as `P(n)`.<br>

<br>

## Formulas
- `P(n,k) = n!/(n-k)!`;
- `P(n) = n!`;

<br>

## Proofs
Main idea: when we form **k-permutation of n** *without repetitions* we select element from set **without** returning it back.<br>
So, after each such selection we get **new set** with **decremented** *cardinality*.<br>

<br>

### Trivial case
Consider finite set `A = {1,2,3}, |A| = 3`. Find number of all **3-tuples** `(a,b,c)` **without repetitions** from `A`.<br>
Steps:<br>
1. We have `|A|` **choices** to select element from `A`. Take element `1` from `A` **without returning** it back, then we get new set `B = A \ {1} = {2,3}` with cardinality `|A| - 1 = 2`.
2. We have `|B|` **choices** to select element from `B`. Take element `2` from `B` **without returning** it back, then we get new set `C = B \ {2} = {1}` with cardinality `|B| - 1 = 1`.
3. We have `|C|` **choices** to select element from `C`. Take element `1` from `C` **without returning** it back, then we get new **empty** set `D = C \ {1} = {}` with cardinality `|C| - 1 = 0`.

The **total number** by **MP** of all **3-tuples** `(a,b,c)` **without repetitions** from `A` is equal to the cardinality of cartesian product of sets `A`, `B`, `C`:
- `A x B x C = |A| * |B| * |C| = 3 * 2 * 1 = 6`.<br>

<br>

After all steps we get 3 sets: `A = {1,2,3}`, `B = {1,2}`, `C = {1}`.<br>
We see that choice in next step is **independent** from all choices in previous steps. It implies **MP**.<br>
Consider 3 another sets: `X = {x1,x2,x3}`, `Y = {y1,y2}`, `Z = {z1}`.<br>

Using **MP** we see than we have 6 **3-tuples** `(x,y,z)` **without repetitions** from `X x Y x Z`:
- `(x1,y1,z1)`
- `(x1,y2,z1)`
- `(x2,y1,z1)`
- `(x2,y2,z1)`
- `(x3,y1,z1)`
- `(x3,y2,z1)`

<br>

If we require that xi ≠ yi, yi ≠ zi, xi ≠ xi then it is the same as we choose **3-tuples** **without repetitions** from `A`.<br>

<br>

### More general case
Consider finite set `A = {1,2, ..., n}, |A| = n`. Find number of all **3-tuples** `(a,b,c)` **without repetitions** from `A`.<br>
Steps:<br>
0. Consider `A1 = A`, so `|A1| = n`.
1. We have `|A1|` **choices** to select element from `A1`. Take element from `A1` **without returning** it back, then we get new set `A2 = A1 \ {a}` with cardinality `|A1| - 1 = n-1`.
2. We have `|A2|` **choices** to select element from `A2`. Take element from `A2` **without returning** it back, then we get new set `A3 = A2 \ {a}` with cardinality `|A2| - 1 = n-2`.
3. And so on.

<br>

Then
- `P(n,k) = A1 x A2 x ... x An = |A1| * |A2| * ... * |An| = n * (n-1) * ... * (n - k + 1)`

We can **complement** `P(n,k) = n * (n-1) * ... * (n - k + 1)` to `n!` by **multiplying** it by `(n-k)!`, where `(n-k)! = (n-k) * (n-(k+1)) * (n-(k+2)) * 3 * 2 * 1`.<br>
So,
- `P(n,k) * (n-k)! = n!` **=>** `P(n,k) = n!/(n-k)!`.

<br>

## Examples
Consider `A = {a}`. Then, there is only **one** **1-permutaton** of `A`:
- `(a)`;

Consider `A = {a,b}`. Then, there are only **two** **2-permutatons** of `A`:
- `(a,b)`;
- `(b,a)`;

Consider `A = {a,b,c}`. Find **all** **3-permutatons** of `A`.
Divide problem into 2 disjoint cases. There are only **two** **2-permutatons** of `{a,b}`. 
Count all new permutations for each permutation of `{a,b}`:
1. Adding `c` to ordered pair `(a,b)` gives us **three** new 3-tuples:
   - `(c,a,b)`
   - `(a,c,b)`
   - `(a,b,c)`
2. Adding `c` to ordered pair `(b,a)` gives us **three** new 3-tuples:
   - `(c,b,a)`
   - `(b,c,a)`
   - `(b,a,c)`

According **AP** we have `3 + 3 = 6` total **3-tuples** of `{a,b} + {c} = {a,b,c} = A`.

<br>

## Permutations with repetitions
A **k-permutation of n** *with repetitions* is **all ordered pairs** of length `k, k <= n` that consist of elements from `A, |A| = n`.<br>
The **number** of such **k-permutations** is denoted as `P̄(n,k)`.<br>

<br>

## Formulas
- `P̄(n,k) = n^k`;

<br>

## Proofs
When we form **k-permutation of n** *with repetitions* we **return** back selected element to original set.<br>
So, on every step we use the original set and its cardinality isn't changed.

Example, consider set `A = {1,2,3,4,5}, |A| = 3`. Find number of all **3-tuples** `(a,b,c)` **with repetitions** from `A`. <br>
Let's divide problem into **3** disjoint cases:<br>
1. Take element from `A` then **return it back** to `A`. Here we have `|A|` **choices** to select element from `A`.
2. Take element from `A` then **return it back** to `A`. Here we have `|A|` **choices** to select element from `A`.
3. Take element from `A` then **return it back** to `A`. Here we have `|C|` **choices** to select element from `A`.

Acording **MP** the **total number** of all **5-tuples** `(a,b,c,d,e)` is equal to the *cardinality* of cartesian product of sets `A`, `A`, `A`, `A` and `A`:
- `A x A x A x A x A = |A| * |A| * |A| * |A| * |A| = 5^5`.<br>

<br>

Consider **more general example**: `A = {1,2, ..., n}, |A| = n`. Find all **k-tuples** from `A`.<br>
Then,
- `P̄(n,k) = A x A x ... x A = |A| * |A| * ... * |A| = n^k`.
