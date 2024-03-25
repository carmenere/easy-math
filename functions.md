# Function
A function *binds* an **input** to an **output**.<br>
A function *binds* **each element** of a *set* with **exactly one element** of *another set* (possibly the same set).<br>

A **function** **from** a set `X` **to** a set `Y` assigns to **each** element of `X` **exactly one** element of `Y`. In other words **function** `f` **maps** `x∈X` **to** `y∈Y`.<br>

Notations:
1. `f: X → Y`, `f` is the **function**, `X` its **domain**, `Y` its **codomain**.
2. `y = f(x)`, `y∈Y`, `x∈X`.
3. `x ↦ y` **instead** of `y=f(x)`, this allows the definition of a function **without naming** it.

<br>

## Domain. Image. Codomain
1. The **Domain** (`Dom f`) is the **set of values** that go **into** a function.
2. The **Image** (`Im f`) is the **set of values** that **actually** do **come out** of a function.
3. The **Codomain** is the **set of values** that could **possibly** **come out** of a function.

<br>

**Synonyms**:
|Input|Relationship|Output|
|:----|:-----------|:-----|
|Pre-image|*Maps to*|Image|
|Argument|*Maps to*|Value of function|
|Independent variable|*Maps to*|Dependent variable|

<br>

The *Image* is a **subset** of the *Codomain*:
1. `Im f = { y | ∀x∈X, ∃y∈Y : f(x) = y }`.
2. `Im f ⊆ Y`.
3. `Y \ Im f` **don't** have **pre-images**.

Why both? Well, sometimes we don't know the exact **Image**, but we know the set it **lies in**. So we define the **Codomain** and continue on.<br>

<br>

### Example
Consider function `f = x^2` and `dom f = {1,2,3}`. Here **Image** = `{1,4,9}` and **Codomain** can be = `{1,2,3,4,5,6,7,8,9}`.<br>

<br>

# Surjection
Formal defenition: `f: X → Y` is **surjective** if `∀y∈Y, ∃x∈X : y = f(x)`. In other words, the function is **surjective** if **every element** of the **codomain** has **at least one** **pre-image**, but `y` can have **more then one pre-image**.<br>

A **surjective function** is also called a **surjection**.

<br>

# Injection
Formal defenition: `f: X → Y` is **injective** if `∀x,x'∈X, f(x) = f(x') => x = x'`. In other words, the function is **injective** if **every element** of the **codomain** has **exactly one pre-image** or **doesn't** have **pre-image**.<br>

An **injective function** is also called an **injection**.

<br>

# Bijection
Formal defenition: `f: X → Y` is **surjective** if `∀y∈Y, ∃!x∈X : y = f(x)` and `∀x∈X, ∃!y∈Y : y = f(x)`, here `∃!x` means **there exists exactly one** `x`. In other words, the function is **bijective** if each element of the **codomain** is mapped to by **exactly one** element of the **domain**.<br>
The function is **bijective** if it is both **injective** and **surjective**.<br>

A **bijective function** is also called a **bijection**.