# Probability
**Probability** is the branch of mathematics concerning **events** and numerical descriptions of **how likely they are to occur**.<br>
The **probability of an event** is a number in range `[0, 1]`: the larger means the more likely an event is to occur.<br>

<br>

# Probability space
**probability space** is a **mathematical triplet** `<Ω, 𝓕, P>` that provides a **formal model** of a **random process** or **experiment**.
A **probability space** consists of **three elements**:
1. A **sample space**, `Ω`, which is the **set of all possible outcomes**. An **outcome** is the **result** of a **single** experiment.
2. An **event space**, `𝓕`, which is a **set of events**. An **event** is a **set** of *zero or more* **outcomes**. So, an **event** is a **subset** of the **sample space**. More formally, `𝓕` is `σ-algebra` (aka `σ-field`) and contains `2^Ω` subsets of `Ω`.
3. A **probability function**, `P`, which assigns each event in the event space a **probability**, which is a number between `0` and `1`. More formally, `P` a function on `𝓕`: `P: 𝓕 -> [0,1]`.

<br>

A **probability space** is a **measure space** such that the **measure of the whole space** is **equal to one**: `P(Ω) = 1`.

The elements of `σ-algebra` are called **measurable sets**.

<br>

### Example
The **sample space** to be `{1,2,3,4,5,6}`.
For the **event space**, we could simply use the **set of all subsets** of the sample space, which would then contain simple events such as `{5}` as well as complex events such as `{2,4,6}`.
For the **probability function**, we would map each event to its probability (the number of outcomes in that event divided by `6`). For example, `{5}` would be mapped to `1/6`, and `{2,4,6}` would be mapped to `3/6 = 1/2`.

When an **experiment** is **conducted**, we imagine that nature selects a single **outcome**, `ω`, from the sample space `Ω`.<br>
All the events in the event space `𝓕` that contain the selected outcome `ω` are said to **have occurred**.<br>
This selection happens in such a way that **if the experiment were repeated many times**, the **number of occurrences of each event** would most likely tend **towards** the **probability** assigned to that event by the probability function.

<br>

The Soviet mathematician Andrey Kolmogorov introduced the notion of probability space, together with other axioms of probability, in the 1930s.<br>


<br>

# Complete probability space
A probability space `<Ω, 𝓕, P>` is said to be a **complete probability space** if for all `B ∈ 𝓕` with `P(B) = 0` and all `A ⊂ B` the `𝓕` also contains `A`: `A ∈ 𝓕`. 

<br>

# Examples
![Examples](/img/pspace_examples.jpeg)

<br>

