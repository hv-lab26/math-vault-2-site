Roll a fair die. The result X can be 1, 2, 3, 4, 5 or 6, and each value has a probability of 1/6. If we write down **every** value X can take together with its probability, we get a complete picture of how X behaves. This picture is called a probability distribution.

**Definition**: A **probability distribution** consists of all the values a random variable can take, along with the associated probability of each of these values.

*e.g. Rolling a fair die: x ∈ {1, 2, 3, 4, 5, 6}*

| x         | 1   | 2   | 3   | 4   | 5   | 6   |
| --------- | --- | --- | --- | --- | --- | --- |
| Pr(X = x) | 1/6 | 1/6 | 1/6 | 1/6 | 1/6 | 1/6 |

![[Discrete Distributions - Fair Die.png]]

A discrete probability distribution can be given as:
- a **table** (like above),
- a **graph** (like above), or
- a **rule (formula)**, e.g. Pr(X = x) = (5x + 3)/42 for x = 0, 1, 2, 3.

## Conditions:

For a table (or a rule) to be a discrete probability distribution, it must satisfy **both** conditions:

**Condition 1:** Every probability is between 0 and 1.

==**0 ≤ Pr(X = x) ≤ 1 for every value of x**==

**Condition 2:** The probabilities add up to 1. *(If they don't, it isn't a probability distribution, so if you built the table yourself, check your working!)*

==**ΣPr(X = x) = 1**==

*Σ (sigma) means "sum" or "add them all up".* In LaTeX:
$$\sum_{i=1}^{n}p_i=p_1+p_2+\dots+p_n=1$$

*Note: the values of x can be negative (e.g. a profit of −\$2), but the probabilities can never be negative.*

> [!tip] Exam tip
> Whenever a table has an unknown (like k), the first step is almost always **"add everything and set it equal to 1"**. Then check that the value you found doesn't make any probability negative or bigger than 1.

## Finding probabilities from a table:

Add the probabilities of the values of x you need. Be careful with the inequality signs:

| Words                          | Symbol        | Values of x to add (if x = 0, 1, …, 5) |
| ------------------------------ | ------------- | -------------------------------------- |
| more than 2                    | Pr(X > 2)     | 3, 4, 5                                |
| at least 2 / 2 or more         | Pr(X ≥ 2)     | 2, 3, 4, 5                             |
| less than 2 / fewer than 2     | Pr(X < 2)     | 0, 1                                   |
| at most 2 / no more than 2     | Pr(X ≤ 2)     | 0, 1, 2                                |
| between 1 and 4 (not included) | Pr(1 < X < 4) | 2, 3                                   |

**The complement**: if you need many values, it's often faster to take away the ones you don't need.

==**Pr(X > 2) = 1 − Pr(X ≤ 2)**==

**Conditional probability**: the same rule as in [[3 - Laws of Probability]]. Divide by the probability of what you are given:

==**Pr(A | B) = Pr(A ∩ B) ÷ Pr(B)**==

*e.g.* $\Pr(X=0\mid X\le2)=\dfrac{\Pr(X=0)}{\Pr(X\le2)}$, because if X = 0 then X ≤ 2 is automatically true.

> [!tip] Tip
> Before adding, write down the list of x-values you need, e.g. Pr(1 < X ≤ 3) → x = 2, 3. Most mistakes come from including (or leaving out) the end value.

## From an experiment to a distribution:

Sometimes the distribution isn't given, and we have to build it from the experiment:

1. List all the outcomes, usually with a [[5 - Tree Diagram|tree diagram]].
2. Find the value of X for each outcome.
3. Group the outcomes with the same value of X and **add** their probabilities.
4. Check that the probabilities add up to 1.

See Examples 6 and 7.

> [!info] Fun fact: Benford's law
> Take a huge list of real-life numbers, like the populations of every town in the world, and look at the first digit of each number. You might expect each digit 1–9 to appear 1/9 of the time, but the digit **1** appears about **30%** of the time, and 9 only about 5%! The probability distribution of the first digit is
> $$\Pr(D=d)=\log_{10}\left(1+\frac{1}{d}\right),\quad d=1,2,\dots,9$$
> Tax offices and auditors use this to detect fake numbers, because people who make up data tend to spread the first digits too evenly.

---

## Examples:

**Example 1:** Which of the following tables represent a discrete probability distribution?

**a)**

| x         | 0   | 1   | 2   | 3   |
| --------- | --- | --- | --- | --- |
| Pr(X = x) | 0.2 | 0.5 | 0.2 | 0.1 |

**b)**

| x         | 0   | 2   | 4   | 6   |
| --------- | --- | --- | --- | --- |
| Pr(X = x) | 0.5 | 0.3 | 0.1 | 0.1 |

**c)**

| x         | −1  | 0   | 1   | 2   |
| --------- | --- | --- | --- | --- |
| Pr(X = x) | 0.2 | 0.1 | 0.3 | 0.3 |

**d)**

| x         | −2   | 0   | 5   | 7   |
| --------- | ---- | --- | --- | --- |
| Pr(X = x) | −0.2 | 0.3 | 0.5 | 0.4 |

**Solution**:
**a)** All probabilities are between 0 and 1, and 0.2 + 0.5 + 0.2 + 0.1 = 1 -> **yes**
**b)** All probabilities are between 0 and 1, and 0.5 + 0.3 + 0.1 + 0.1 = 1 -> **yes**
**c)** 0.2 + 0.1 + 0.3 + 0.3 = 0.9 ≠ 1 -> **no**
**d)** The probabilities add up to 1, but Pr(X = −2) = −0.2 is negative -> **no**

So only **a) and b)** are probability distributions.

*Note: in c), x = −1 is fine. Negative values of x are allowed, negative probabilities are not.*

**Example 2:** Find k in these probability distributions.

**a)**

| x         | 0   | 1   | 2   |
| --------- | --- | --- | --- |
| Pr(X = x) | 0.3 | k   | 0.5 |

**b)**

| x         | 0   | 1   | 2   | 3   |
| --------- | --- | --- | --- | --- |
| Pr(X = x) | k   | 2k  | 3k  | k   |

**c)**

| x         | 1   | 2   | 3   |
| --------- | --- | --- | --- |
| Pr(X = x) | 3k  | 4k  | 5k  |

**Solution**:
**a)**
$$k=1-0.3-0.5=0.2$$

**b)**
$$k+2k+3k+k=1\implies7k=1\implies k=\frac{1}{7}$$

**c)**
$$3k+4k+5k=1\implies12k=1\implies k=\frac{1}{12}$$

**Example 3:** A quiz has 5 questions. Let X be the number of questions that a randomly chosen student answers correctly. The probability distribution of X is:

| x         | 0    | 1    | 2   | 3    | 4    | 5    |
| --------- | ---- | ---- | --- | ---- | ---- | ---- |
| Pr(X = x) | 0.07 | 0.14 | k   | 0.46 | 0.08 | 0.02 |

**a)** State what the random variable X represents.
**b)** Find k.
**c)** Find:
i) Pr(X = 2)  ii) Pr(X > 2)  iii) Pr(X ≥ 2)  iv) Pr(X < 2)  v) Pr(X ≤ 2)
vi) Pr(2 < X < 4)  vii) Pr(1 < X ≤ 3)  viii) Pr(0 ≤ X < 3)
ix) Pr(X = 0 | X ≤ 2)  x) Pr(X = 3 | X > 1)

**Solution**:
**a)** X represents the number of correct answers of a randomly chosen student.

**b)**
$$0.07+0.14+k+0.46+0.08+0.02=1\implies k=0.23$$

**c)**
i) $\Pr(X=2)=0.23$
ii) $\Pr(X>2)=0.46+0.08+0.02=0.56$
iii) $\Pr(X\ge2)=0.23+0.56=0.79$
iv) $\Pr(X<2)=0.07+0.14=0.21$
v) $\Pr(X\le2)=0.21+0.23=0.44$
vi) $\Pr(2<X<4)=\Pr(X=3)=0.46$
vii) $\Pr(1<X\le3)=0.23+0.46=0.69$
viii) $\Pr(0\le X<3)=0.07+0.14+0.23=0.44$

ix) X = 0 is already inside X ≤ 2:
$$\Pr(X=0\mid X\le2)=\frac{\Pr(X=0)}{\Pr(X\le2)}=\frac{0.07}{0.07+0.14+0.23}=\frac{0.07}{0.44}=\frac{7}{44}$$

x) X = 3 is already inside X > 1:
$$\Pr(X=3\mid X>1)=\frac{\Pr(X=3)}{\Pr(X>1)}=\frac{0.46}{0.23+0.46+0.08+0.02}=\frac{0.46}{0.79}=\frac{46}{79}$$

*Check: Pr(X ≥ 2) = 1 − Pr(X < 2) = 1 − 0.21 = 0.79 ✓. Using the complement is a quick way to check your answers.*

**Example 4:** The probability distribution of X is given by the rule
$$\Pr(X=x)=\frac{5x+3}{42},\quad x=0,1,2,3$$
Write the probability distribution as a table.

**Solution**: Substitute each value of x into the rule:

| x         | 0                  | 1                  | 2     | 3                  |
| --------- | ------------------ | ------------------ | ----- | ------------------ |
| Pr(X = x) | 3/42 = 1/14        | 8/42 = 4/21        | 13/42 | 18/42 = 3/7        |

*Check:* $\dfrac{3+8+13+18}{42}=\dfrac{42}{42}=1$ ✓

**Example 5:** The probability distribution of X is given by the rule
$$\Pr(X=x)=\frac{4x-3}{66},\quad x=1,2,3,4,5,6$$
Find **a)** Pr(X > 2), **b)** Pr(X ≤ 5), **c)** Pr(2 < X < 5).

**Solution**: The probabilities are 1/66, 5/66, 9/66, 13/66, 17/66, 21/66.
**a)** Use the complement:
$$\Pr(X>2)=1-\Pr(X\le2)=1-\frac{1+5}{66}=1-\frac{6}{66}=\frac{10}{11}$$

**b)**
$$\Pr(X\le5)=1-\Pr(X=6)=1-\frac{21}{66}=\frac{45}{66}=\frac{15}{22}$$

**c)**
$$\Pr(2<X<5)=\Pr(X=3)+\Pr(X=4)=\frac{9+13}{66}=\frac{22}{66}=\frac{1}{3}$$

**Example 6:** A fair coin is tossed 3 times. Let X be the number of tails. Find the probability distribution of X.

**Solution**: Draw a tree diagram, then count the tails in each outcome:
![[Discrete Distributions - Three Coins Tree.png]]
Each outcome has probability 1/8. Group the outcomes by the value of X:

| x         | 0   | 1   | 2   | 3   |
| --------- | --- | --- | --- | --- |
| Pr(X = x) | 1/8 | 3/8 | 3/8 | 1/8 |

*Check: 1/8 + 3/8 + 3/8 + 1/8 = 1 ✓*

**Example 7:** A bag contains 6 blue and 4 yellow balls. A ball is drawn at random, its colour is noted, and it is put back. This is done 3 times. Let X be the number of blue balls drawn. Find the probability distribution of X.

**Solution**: Pr(B) = 6/10 = 0.6 and Pr(Y) = 0.4 on every draw, because the ball is put back.
![[Discrete Distributions - Bag Tree.png]]

| x         | 0     | 1     | 2     | 3     |
| --------- | ----- | ----- | ----- | ----- |
| Pr(X = x) | 0.064 | 0.288 | 0.432 | 0.216 |

*Check: 0.064 + 0.288 + 0.432 + 0.216 = 1 ✓*

*Note: drawing the whole tree takes time. In [[7 - Binomial Distribution]], we will find these probabilities with one formula.*

> [!info] Fun fact
> Casino dice are made so precisely that each face really does have probability 1/6. The dots aren't just painted on: they are drilled into the die and then filled with paint of the same weight as the plastic that was removed, so that no face is heavier than another.

---

## Exercises:

*Try each question first, then click on "Solution" to check your answer.*

**Question 1:** Show that Pr(X = x) = x/10, x = 1, 2, 3, 4, is a probability distribution.

> [!success]- Solution
> The probabilities are 0.1, 0.2, 0.3 and 0.4.
> - They are all between 0 and 1 ✓
> - $0.1+0.2+0.3+0.4=1$ ✓
>
> So it is a probability distribution.

**Question 2:** The random variable X has the rule Pr(X = x) = kx², x = 1, 2, 3.
**a)** Find k.
**b)** Find Pr(X ≥ 2).

> [!success]- Solution
> **a)**
> $$k(1)^2+k(2)^2+k(3)^2=1\implies14k=1\implies k=\frac{1}{14}$$
>
> **b)**
> $$\Pr(X\ge2)=1-\Pr(X=1)=1-\frac{1}{14}=\frac{13}{14}$$

**Question 3:** The probability distribution of X is:

| x         | 0   | 1   | 2   | 3    |
| --------- | --- | --- | --- | ---- |
| Pr(X = x) | 0.1 | k   | k²  | 0.15 |

**a)** Find k.
**b)** Find Pr(X = 1 | X ≥ 1).

> [!success]- Solution
> **a)**
> $$0.1+k+k^2+0.15=1\implies k^2+k-0.75=0\implies(k+1.5)(k-0.5)=0$$
> So k = 0.5 or k = −1.5. A probability can't be negative, so **k = 0.5** (and then k² = 0.25).
>
> **b)**
> $$\Pr(X=1\mid X\ge1)=\frac{\Pr(X=1)}{\Pr(X\ge1)}=\frac{0.5}{1-0.1}=\frac{0.5}{0.9}=\frac{5}{9}$$

**Question 4:** A box contains 3 red and 2 green counters. Two counters are drawn **without replacement**. Let X be the number of red counters drawn. Find the probability distribution of X.

> [!success]- Solution
> $$\Pr(X=0)=\Pr(GG)=\frac{2}{5}\times\frac{1}{4}=\frac{1}{10}$$
> $$\Pr(X=2)=\Pr(RR)=\frac{3}{5}\times\frac{2}{4}=\frac{3}{10}$$
> $$\Pr(X=1)=1-\frac{1}{10}-\frac{3}{10}=\frac{6}{10}=\frac{3}{5}$$
>
> | x         | 0    | 1   | 2    |
> | --------- | ---- | --- | ---- |
> | Pr(X = x) | 1/10 | 3/5 | 3/10 |
>
> *Tip: finding the easiest values first and using "add up to 1" for the last one saves time.*

**Question 5:** Two fair dice are rolled. Let X be the **larger** of the two numbers (if both are the same, X is that number).
**a)** Show that $\Pr(X=x)=\dfrac{2x-1}{36}$ for x = 1, 2, …, 6.
**b)** Find Pr(X ≥ 5).

> [!success]- Solution
> **a)** X = x happens when one die shows x and the other shows x or less. Out of the 36 equally likely outcomes:
> - the first die shows x and the second shows 1, 2, …, x: **x** outcomes,
> - the second die shows x and the first shows 1, 2, …, x: another **x** outcomes,
> - but (x, x) has been counted twice, so take 1 away.
>
> That's 2x − 1 outcomes, so
> $$\Pr(X=x)=\frac{2x-1}{36}$$
> *Check: 1 + 3 + 5 + 7 + 9 + 11 = 36 ✓*
>
> **b)**
> $$\Pr(X\ge5)=\frac{9}{36}+\frac{11}{36}=\frac{20}{36}=\frac{5}{9}$$

**Question 6:** A fair coin is tossed until the first head appears. Let X be the number of tosses.
**a)** Find Pr(X = 1), Pr(X = 2) and Pr(X = 3), and write a rule for Pr(X = x).
**b)** Find Pr(X ≤ 3).
**c)** Find Pr(X > 3).

> [!success]- Solution
> **a)** X = x means x − 1 tails followed by a head:
> $$\Pr(X=1)=\frac{1}{2},\quad\Pr(X=2)=\frac{1}{2}\times\frac{1}{2}=\frac{1}{4},\quad\Pr(X=3)=\frac{1}{8}$$
> $$\Pr(X=x)=\left(\frac{1}{2}\right)^{x},\quad x=1,2,3,\dots$$
>
> **b)**
> $$\Pr(X\le3)=\frac{1}{2}+\frac{1}{4}+\frac{1}{8}=\frac{7}{8}$$
>
> **c)** X > 3 means the first three tosses are all tails:
> $$\Pr(X>3)=1-\frac{7}{8}=\frac{1}{8}=\left(\frac{1}{2}\right)^3$$
>
> *Note: X has infinitely many values, but the probabilities still add up to 1: 1/2 + 1/4 + 1/8 + … = 1.*
