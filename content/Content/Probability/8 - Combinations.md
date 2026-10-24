
A teacher needs to choose 3 students from Alex, Ben, Chloe and Dan to represent the class. Choosing {Alex, Ben, Chloe} is the same as choosing {Chloe, Alex, Ben}: it's the same 3 people. **Order doesn't matter, only who is chosen.** Counting selections like this is called a **combination**.

**Definition**: A combination is a **selection** of objects in which **order does NOT matter**. The number of combinations of r objects chosen from n different objects is written as:

==**ⁿCᵣ = n! ÷ (r! × (n − r)!)**==

*read as "n choose r."*

$${}^{n}C_{r}=\binom{n}{r}=\frac{n!}{r!\,(n-r)!}$$

*Note: $\binom{n}{r}$ is another way of writing ⁿCᵣ that you will often see in textbooks.*

## Why divide by r!?

Each selection of r objects can be put in order in r! different ways. A [[7 - Permutation]] counts every one of those orders separately, but a combination counts the whole group only once. So:

==**ⁿCᵣ = ⁿPᵣ ÷ r!**==

![[Combinations - Selections vs Arrangements.png]]

$${}^{4}C_{3}=\frac{{}^{4}P_{3}}{3!}=\frac{24}{6}=4$$

## Permutation or combination?

|                    | Permutation                                          | Combination                                                  |
| ------------------ | ---------------------------------------------------- | ------------------------------------------------------------ |
| Does order matter? | **Yes**                                              | **No**                                                       |
| Key words          | arrange, order, line up, 1st/2nd/3rd, code, roles    | choose, select, pick, team, committee, group, hand of cards  |
| Formula            | $\dfrac{n!}{(n-r)!}$                                 | $\dfrac{n!}{r!\,(n-r)!}$                                     |
| Example            | Gold, silver and bronze from 10 runners: ¹⁰P₃ = 720  | 3 runners from 10 to go through to the final: ¹⁰C₃ = 120     |

> [!tip] Exam tip: permutation or combination?
> Ask yourself: "If I swap two of the chosen things, do I get a different result?"
> **Yes**: it is permutation. **No**: it is combination.

## Useful properties

$${}^{n}C_{0}={}^{n}C_{n}=1\qquad {}^{n}C_{1}=n\qquad {}^{n}C_{r}={}^{n}C_{n-r}$$

*The last one makes sense: choosing r objects to take is the same as choosing n − r objects to leave behind.*

> [!tip] Tip: use the symmetry
> ⁿCᵣ = ⁿCₙ₋ᵣ makes big ones easy: ¹⁰⁰C₉₈ = ¹⁰⁰C₂ = (100 × 99) ÷ 2 = 4950.

> [!info] Fun fact: Pascal's triangle
> Every number in Pascal's triangle is a combination: row n, position r is ⁿCᵣ (counting both from 0). Each number is the sum of the two numbers above it.
> ```
>             1
>           1   1
>         1   2   1
>       1   3   3   1
>     1   4   6   4   1
>   1   5  10  10   5   1
> 1   6  15  20  15   6   1
> ```
> e.g. row 4 is 1, 4, 6, 4, 1 = ⁴C₀, ⁴C₁, ⁴C₂, ⁴C₃, ⁴C₄.
> It's named after the French mathematician Blaise Pascal (1600s), but the Chinese mathematician Yang Hui described it in 1261, almost 400 years earlier, so in China it's called **Yang Hui's triangle**.

## On the calculator

|     | TI-84 Plus CE                          | Casio fx-580VNX               |
| --- | -------------------------------------- | ----------------------------- |
| ⁿCᵣ | n, then MATH -> PROB -> 3: nCr, then r | n, then SHIFT / (nCr), then r |

## Selecting from groups

When you choose from different groups (e.g. boys and girls), choose from each group separately, then **multiply** (the multiplication principle from [[7 - Permutation]]):

==**Number of ways = (ways to choose from group 1) × (ways to choose from group 2)**==

For **"at least one"** questions, it is usually quicker to use the complement:

==**Number of ways with at least one = total − number of ways with none**==

> [!info] Fun fact: the handshake problem
> If 30 people at a party each shake hands with everyone else once, there are ³⁰C₂ = 435 handshakes, because every handshake is just a choice of 2 people.

## Combinations and probability

If every selection is equally likely:

==**Pr(event) = number of selections in the event ÷ total number of selections**==

> [!info] Fun fact
> There are ⁵²C₅ = 2 598 960 different 5-card poker hands, but only 4 of them are royal flushes (10, J, Q, K, A of the same suit). So the chance of being dealt one is 4 ÷ 2 598 960 = 1 in 649 740.

---

## Examples:

**Example 1:** In how many ways can 3 students be chosen from a class of 10 to go on a trip?

**Solution**: The 3 students are just a group (no roles), so order doesn't matter:
$${}^{10}C_{3}=\frac{10!}{3!\,7!}=\frac{10\times9\times8}{3\times2\times1}=120$$
*Compare with Example 2 in [[7 - Permutation]]: choosing a president, a vice-president and a secretary gives ¹⁰P₃ = 720 = 120 × 3!, because there, each group of 3 people can fill the 3 roles in 3! ways.*

**Example 2:** A committee of 5 people is chosen from 6 men and 4 women. In how many ways can this be done if:
**a)** there are no restrictions?
**b)** the committee has exactly 2 women?
**c)** the committee has at least 1 woman?

**Solution**:
**a)**
$${}^{10}C_{5}=252$$

**b)** 2 women from 4 **and** 3 men from 6:
$${}^{4}C_{2}\times{}^{6}C_{3}=6\times20=120$$

**c)** Use the complement. "No women" means all 5 members are men: ⁶C₅ = 6 ways.
$$252-6=246$$

**Example 3:** The committee in Example 2 is chosen at random. Find the probability that it has exactly 2 women.

**Solution**:
$$\Pr(\text{exactly 2 women})=\frac{{}^{4}C_{2}\times{}^{6}C_{3}}{{}^{10}C_{5}}=\frac{120}{252}=\frac{10}{21}\approx0.476$$

---

## Exercises:

*Try each question first, then click on "Solution" to check your answer.*

**Question 1:** Evaluate:
**a)** ⁷C₂
**b)** ⁸C₅
**c)** ¹²C₀
**d)** ¹⁰C₇

> [!success]- Solution
> **a)** ${}^{7}C_{2}=\dfrac{7\times6}{2\times1}=21$
>
> **b)** ${}^{8}C_{5}={}^{8}C_{3}=\dfrac{8\times7\times6}{3\times2\times1}=56$
>
> **c)** ${}^{12}C_{0}=1$ (there is only 1 way to choose nothing)
>
> **d)** ${}^{10}C_{7}={}^{10}C_{3}=120$

**Question 2:** A pizza shop offers 8 different toppings.
**a)** How many different pizzas with exactly 3 toppings can be made?
**b)** How many different pizzas with at most 2 toppings can be made (a plain pizza counts)?

> [!success]- Solution
> **a)**
> $${}^{8}C_{3}=56$$
>
> **b)** 0, 1 **or** 2 toppings:
> $${}^{8}C_{0}+{}^{8}C_{1}+{}^{8}C_{2}=1+8+28=37$$

**Question 3:** Permutation or combination? Decide, then calculate the number of ways of:
**a)** choosing 4 books out of 9 to take on holiday.
**b)** arranging 4 books out of 9 on a shelf.
**c)** choosing a captain and a vice-captain from 15 players.
**d)** choosing 2 players out of 15 to collect the equipment.

> [!success]- Solution
> **a)** Combination (just a group of books): ${}^{9}C_{4}=126$
>
> **b)** Permutation (the order on the shelf matters): ${}^{9}P_{4}=3024$
>
> **c)** Permutation (captain ≠ vice-captain): ${}^{15}P_{2}=210$
>
> **d)** Combination (both do the same job): ${}^{15}C_{2}=105$

**Question 4:** A hand of 5 cards is dealt from a standard deck of 52 cards (13 cards in each of the 4 suits).
**a)** How many different hands are possible?
**b)** How many hands contain only hearts?
**c)** Find the probability that a hand contains only hearts.

> [!success]- Solution
> **a)**
> $${}^{52}C_{5}=2\,598\,960$$
>
> **b)** Choose all 5 cards from the 13 hearts:
> $${}^{13}C_{5}=1287$$
>
> **c)**
> $$\Pr(\text{only hearts})=\frac{1287}{2\,598\,960}=\frac{33}{66\,640}\approx0.000495$$

**Question 5:** A team of 4 is chosen from 7 girls and 5 boys.
**a)** How many different teams are possible?
**b)** How many teams have exactly 2 girls?
**c)** How many teams have at least 1 boy?
**d)** The team is chosen at random. Find the probability that it has exactly 2 girls.

> [!success]- Solution
> **a)**
> $${}^{12}C_{4}=495$$
>
> **b)** 2 girls from 7 **and** 2 boys from 5:
> $${}^{7}C_{2}\times{}^{5}C_{2}=21\times10=210$$
>
> **c)** Complement: "no boys" means all 4 are girls, ⁷C₄ = 35 ways.
> $$495-35=460$$
>
> **d)**
> $$\Pr(\text{exactly 2 girls})=\frac{210}{495}=\frac{14}{33}\approx0.424$$

**Question 6:** 8 points are marked on a circle.
**a)** How many straight lines can be drawn by joining 2 of the points?
**b)** How many triangles can be made using 3 of the points as corners?

> [!success]- Solution
> **a)** Each line is a choice of 2 points:
> $${}^{8}C_{2}=28$$
>
> **b)** No 3 points on a circle lie on a straight line, so any 3 points make a triangle:
> $${}^{8}C_{3}=56$$

**Question 7:** A box contains 6 red and 4 white balls. 3 balls are taken out at random (without replacement).
**a)** Find Pr(all 3 are red).
**b)** Find Pr(exactly 2 are red).
**c)** Find Pr(at least 1 is white).

> [!success]- Solution
> Total number of selections: ${}^{10}C_{3}=120$
>
> **a)**
> $$\Pr(\text{all red})=\frac{{}^{6}C_{3}}{{}^{10}C_{3}}=\frac{20}{120}=\frac{1}{6}$$
>
> **b)** 2 red from 6 **and** 1 white from 4:
> $$\Pr(\text{exactly 2 red})=\frac{{}^{6}C_{2}\times{}^{4}C_{1}}{{}^{10}C_{3}}=\frac{15\times4}{120}=\frac{1}{2}$$
>
> **c)**
> $$\Pr(\text{at least 1 white})=1-\Pr(\text{all red})=1-\frac{1}{6}=\frac{5}{6}$$
>
> *Check part a) with a [[5 - Tree Diagram]]: $\dfrac{6}{10}\times\dfrac{5}{9}\times\dfrac{4}{8}=\dfrac{120}{720}=\dfrac{1}{6}$. Same answer!*

**Question 8:** In a lotto game, 6 numbers are drawn from the numbers 1 to 45.
**a)** How many different sets of 6 numbers are possible?
**b)** Find the probability of winning with one ticket (all 6 numbers correct).

> [!success]- Solution
> **a)** The order the numbers are drawn in doesn't matter:
> $${}^{45}C_{6}=8\,145\,060$$
>
> **b)**
> $$\Pr(\text{win})=\frac{1}{8\,145\,060}\approx0.000000123$$
>
> *Fun fact: with 1 ticket a week, you would expect to wait about 8 145 060 weeks, which is roughly **156 000 years**, to win once!*

**Question 9:** Solve ⁿC₂ = 45.

> [!success]- Solution
> $${}^{n}C_{2}=\frac{n(n-1)}{2}=45$$
> $$n^2-n-90=0\Rightarrow(n-10)(n+9)=0\Rightarrow n=10$$
> (n = −9 is rejected, because n must be a positive whole number.)
