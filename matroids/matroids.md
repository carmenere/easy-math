# Linear combinations
If $`{\displaystyle \mathbf {v} _{1},\mathbf {v} _{2},\dots ,\mathbf {v} _{k}}`$ are vectors and $a_1$,...,$a_n$ are scalars, then the **linear combination** of those vectors is $`{\displaystyle a_{1}\mathbf {v} _{1}+a_{2}\mathbf {v} _{2}+a_{3}\mathbf {v} _{3}+\cdots +a_{n}\mathbf {v} _{n}}`$.<br>

<br>

## Linearly dependent vectors
A sequence of vectors $`{\displaystyle \mathbf {v} _{1},\mathbf {v} _{2},\dots ,\mathbf {v} _{k}}`$ is said to be **linearly dependent**, if there exist scalars $`{\displaystyle a_{1},a_{2},\dots ,a_{k}}`$, not all zero, such that $`{\displaystyle a_{1}\mathbf {v} _{1}+a_{2}\mathbf {v} _{2}+\cdots +a_{k}\mathbf {v} _{k}=\mathbf {0} }`$, where $`{\displaystyle \mathbf {0}}`$ denotes the **zero vector**.<br>

This implies that at least one of the scalars is nonzero, say $`{\displaystyle a_{1}\neq 0}`$, and the above equation is able to be written as 
$`{\displaystyle \mathbf {v} _{1}={\frac {-a_{2}}{a_{1}}}\mathbf {v} _{2}+\cdots +{\frac {-a_{k}}{a_{1}}}\mathbf {v} _{k}}`$.<br>

In other words, **any vector** in the sequence of vectors **can be represented** as a **linear combination** of the **remaining vectors** in the sequence.<br>

<br>

## Linearly independent vectors
A sequence of vectors $`{\displaystyle \mathbf {v} _{1},\mathbf {v} _{2},\dots ,\mathbf {v} _{n}}`$ is said to be **linearly independent** if it is **not** *linearly dependent*, that is, if the equation $`{\displaystyle a_{1}\mathbf {v} _{1}+a_{2}\mathbf {v} _{2}+\cdots +a_{n}\mathbf {v} _{n}=\mathbf {0}}`$
can only be satisfied by $`{\displaystyle a_{i}=0}$ for ${\displaystyle i=1,\dots ,n}`$.<br>

In other words, **no vector** in the sequence of vectors **can be represented** as a **linear combination** of the **remaining vectors** in the sequence.<br>

<br>

## Basis
A *set of vectors* which is **linearly independent** forms a **basis** for that **vector space**.<br>

A set $B$ is a **basis** if its elements are **linearly independent** and **every other** vector in vector space is a **linear combination** of elements of $B$.<br>

A **vector space** can have **several** *bases*. However **all** the *bases* have the **same number of elements**, called the **dimension** of the *vector space*.<br>

<br>

# Matroids
A **matroid** /ˈmeɪtrɔɪd/ is a structure that abstracts and **generalizes** the notion of **linear independence** in vector spaces.<br>
There are many equivalent definitions of matroids. One definition of matroids uses **independent sets**.

A matroid $M$ is a pair $(E,I)$ consisting of a finite set $E$ and a collection $I$ of subsets of $E$ satisfying the following properties:
1. The **empty set** $∅$ is **independent**, so $I$ is **always non-empty**:
   - $∅ ∈ I$;
2. **Any subset** of an **independent set** is **independent**, in other words, every subset of every member of $I$ is also in $I$:
   - if $A ∈ I$ and $B ⊂ A$, then $B ∈ I$;
3. If you have **two independent sets** $A$ and $B$ with **different** sizes, you can take an element from the bigger one $B$ and add it to the smaller one $A$ to get a **larger independent set**:
   - if $A ∈ I$, $B ∈ I$ and $|B| = |A| + 1$, then there is an element $b$ in $B \setminus A$
such that $A ∪ {b} ∈ I$;

<br>

$E$ is called the **ground set** of the matroid.<br>
$I$ is the **collection of independent sets** of $E$.<br>
A subset of the ground set $E$ that is **not** independent is called **dependent**.<br>

<br>

If we want to **prove** that *something is a matroid*, then we are out of luck: we have to check these properties.

<br>

## Uniform matroid
Let $`E = \{1, 2, 3, 4\}`$. Let $`I = \{∅, \{1\}, \{2\}, \{3\}, \{4\}, \{12\}, \{13\}, \{14\}, \{23\}, \{24\}, \{34\}\}`$. In other
words, all the zero, one, and two element subsets of $E$ are **independent**. Let us check that $M = (E, I)$ is a matroid.
1. The empty set $∅$ is in $I$, so property 1 is satisfied.
2. The only subset of the empty set $∅$ is itself and it is in $I$.
3. The only subsets of $`\{1\}`$ are $∅$ and $`\{1\}`$. Both of these are in $I$. Check the rest in the same way.
4. The only subsets of $`\{1, 2\}`$ are $∅$, $`\{1\}`$, $`\{2\}`$, and $`\{1, 2\}`$. Check the rest in the same way.
5. Take $A = ∅$ and $`B = \{1\}`$. We see that $1 = |B| > |A| = 0$, and we can add $1$ to $∅$ to get a larger independent set. 
6. Take $A = ∅$ and $`B = \{1, 2\}`$. Then we can add either $1$ or $2$ to $∅$. Check the rest the same way.
7. Take $`A = \{1\}`$ and $`B = \{1, 4\}`$. We can add $4$ to $A$. Take $`A = \{1\}`$ and $`B = \{2, 3\}`$. We can add either $2$ or $3$ to $A$. Check the rest the same way.

After a lot of checking, we find that the $M$ we defined above is actually a matroid. This matroid has another name: the **uniform matroid** $`U_{2,4}`$. The $4$ refers to the **size of** $E$, and the $2$ refers to the fact that **every subset** of $E$ with **at most** $2$ elements is **independent**.<br>

In general, $`U_{k,n}`$ is a **uniform matroid** with $|E| = n$ and **every subset** of $E$ with **at most** $k$ elements is **independent**.<br>

<br>

# Graphic matroid
To define a matroid from a graph $G = (V,E)$, we’ll set the **ground set** $E$ to be the **set of edges**. Then the **independent sets** will be those sets of edges that do **not** contain a **cycle**. The matroids you get this way are called **graphic**.

<br>

## Non-isomorphic matroids
If we look at the set $E = ∅$, we find there is exactly **one** matroid on $E$:
   - $`I = \{∅\}`$

If $`E = \{1\}`$, we find the **two** matroids on $E$:
   - $`I = \{∅\}`$
   - $`I = \{∅, \{1\}\}`$

If $`E = \{1, 2\}`$ there are **five** matroids on E:
   - $`I = \{∅\}`$
   - $`I = \{∅, \{1\}\}`$
   - $`I = \{∅, \{2\}\}`$
   - $`I = \{∅, \{1\}, \{2\}\}`$
   - $`I = \{∅, \{1\}, \{2\}, \{1, 2\}\}`$

We have the same structure in the matroids $`I = \{∅, \{1\}\}`$ and $`I = \{∅, \{2\}\}`$. Even though there are **five** matroids, we have **four non-isomorphic matroids** on this set since $`\{∅, \{1\}\}`$ and $`\{∅,\{2\}\}`$ are **isomorphic**.

<br>

If $`E = \{1, 2, 3\}`$ we have **eight non-isomorphic matroids**. They are:
- $`I = \{∅\}`$
- $`I = \{∅, \{1\}\}`$
- $`I = \{∅, \{1\}, \{2\}\}`$
- $`I = \{∅, \{1\}, \{2\}, \{1, 2\}\}`$
- $`I = \{∅, \{1\}, \{2\}, \{3\}\}`$
- $`I = \{∅, \{1\}, \{2\}, \{3\}, \{1, 2\}, \{2, 3\}\}`$
- $`I = \{∅, \{1\}, \{2\}, \{3\}, \{1, 2\}, \{2, 3\}, \{1, 3\}\}`$
- $`I = \{∅, \{1\}, \{2\}, \{3\}, \{1, 2\}, \{1, 3\}, \{2, 3\}, \{1, 2, 3\}\}`$

<br>

## Basis
A **basis of a matroid** is a **maximal independent set** of the matroid. In other words, the **basis** of a matroid is an independent set that is **not** contained in any other independent set. A  **basis** becomes **dependent** set by adding to it any element of $E$.<br>

**Any** two bases of a matroid $M$ have the **same number** of elements.<br>

The **rank of a matroid** $M$ is the size of **basis of a matroid** $M$.<br>

In a **graphic matroid**, where the independent sets are the forests, the **bases** are called the **spanning forests** of the graph.<br>

A **circuit** in a matroid $M$ is a **minimal dependent subset** of $E$. In other words, a **circuit** is a **dependent set** whose **proper subsets** are **all independent**.<br>
