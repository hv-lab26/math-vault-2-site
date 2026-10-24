
How many ways can 3 friends, A, B and C, line up for a photo?
ABC, ACB, BAC, BCA, CAB, CBA => **6 ways**.
With 10 friends, there are 3 628 800 ways! We can't list them all, so we need a way to **count without listing**. That's what permutations are for.

## The multiplication principle

**Definition**: If one task can be done in m ways, and a second task can then be done in n ways, then the two tasks together can be done in m × n ways.

==**Total number of ways = m × n**==

*Example: 3 shirts and 4 pairs of pants => 3 × 4 = 12 different outfits.*

*Note: this is exactly what a [[5 - Tree Diagram]] does: 3 branches, then 4 branches from each one → 3 × 4 = 12 outcomes. If the tasks are alternatives instead (you do one OR the other, not both), add the numbers: m + n.*

## Factorial notation

**Definition**: n! is the product of all the whole numbers from n down to 1.

==**n! = n × (n − 1) × (n − 2) × … × 2 × 1**==

*read as "n factorial."*

*Notes: ==**0! = 1**== *(by definition)*

> [!tip] Why is 0! = 1?
> There is exactly **one** way to arrange nothing: do nothing! It also keeps the pattern working: n! = n × (n − 1)!, so 1! = 1 × 0!, which only works if 0! = 1.

Examples:
$$5!=5\times4\times3\times2\times1=120$$
$$\frac{8!}{6!}=\frac{8\times7\times6!}{6!}=8\times7=56$$

**Key fact:** the number of ways to arrange **n different objects in a row** is **n!**
*e.g. 3 friends => 3! = 6 ways (as above), 10 friends => 10! = 3 628 800 ways.*

> [!info] Fun facts: factorials get HUGE
> - 10! seconds is **exactly 6 weeks**: 6 × 7 × 24 × 60 × 60 = 3 628 800 = 10!
> - A deck of 52 cards can be arranged in 52! = 8 × 10⁶⁷ ways. That's so many that every time you shuffle a deck properly, you are almost certainly holding an order that has never existed before.
> - A Rubik's Cube has 43 252 003 274 489 856 000 (about 43 quintillion) possible arrangements, yet every one of them can be solved in 20 moves or fewer.

## Permutations

**Definition**: A permutation is an **arrangement** of objects in which **order matters**. The number of permutations of r objects chosen from n different objects is written as:

==**ⁿPᵣ = n! / (n − r)!**==

*read as "n P r": the number of ways to arrange r objects out of n.*

$${}^{n}P_{r}=\frac{n!}{(n-r)!}=\underbrace{n\times(n-1)\times(n-2)\times\dots\times(n-r+1)}_{r\text{ numbers}}$$

The **box method** shows where the formula comes from. Draw one box for each position, and write in it how many choices are left for that position:

![[Permutation - Box Method.png]]

> [!info] Fun fact
> A "combination lock" should really be called a **permutation lock**: a lock set to 1-2-3 won't open with 3-2-1, so the order matters!

## On the calculator

|     | TI-84 Plus CE                          | Casio fx-580VNX               |
| --- | -------------------------------------- | ----------------------------- |
| n!  | n, then MATH -> PROB -> 4: !           | n, then SHIFT x⁻¹ (x!)        |
| ⁿPᵣ | n, then MATH -> PROB -> 2: nPr, then r | n, then SHIFT × (nPr), then r |

> [!tip] Calculator limit
> 69! = 1.7 × 10⁹⁸ is the biggest factorial these calculators can show. 70! ≈ 1.2 × 10¹⁰⁰ is bigger than a googol (10¹⁰⁰), so you get an error. For something like 100! / 98!, cancel first: 100 × 99 = 9900.

## Arrangements with restrictions

1. **Restricted positions go first.** Fill the positions that have a condition (e.g. "must start with a vowel", "must be even") before the others.
2. **Objects that must be together:** glue them into one block. Arrange the block with the other objects, then multiply by the number of ways to arrange the objects inside the block.
3. **Objects that must NOT be together:** total arrangements − arrangements where they are together.

![[Permutation - Block Method.png]]

## Arrangements with identical objects

If some of the objects are identical, swapping them does not make a new arrangement, so we divide by the factorial of each group of identical objects:

==**Number of arrangements = n! / (a! × b! × …)**==

where a, b, … are the numbers of each kind of identical object.

*e.g. the letters of APPLE (two P's):* $\dfrac{5!}{2!}=\dfrac{120}{2}=60$

## Permutations and probability

If all arrangements are equally likely:

==**Pr(event) = number of arrangements in the event ÷ total number of arrangements**==

> [!info] Fun fact: the birthday problem
> In a group of just **23 people**, there is a better than 50% chance that two of them share a birthday! The trick is to find the chance that everyone's birthday is different, using permutations (ignoring 29 February):
> $$\Pr(\text{all different})=\frac{{}^{365}P_{23}}{365^{23}}\approx0.493\quad\Rightarrow\quad\Pr(\text{shared birthday})\approx1-0.493=0.507$$

---

## Examples:

**Example 1:** In how many ways can 5 students line up in a row?

**Solution**: 5 different students in 5 positions:
$$5!=5\times4\times3\times2\times1=120$$

**Example 2:** A club has 10 members. In how many ways can a president, a vice-president and a secretary be chosen (one person cannot hold two roles)?

**Solution**: Order matters, because being president is different from being secretary:
$${}^{10}P_{3}=10\times9\times8=720$$

**Example 3:** The letters of the word NUMBER are arranged in a row. How many arrangements are possible if:
**a)** there are no restrictions?
**b)** the arrangement starts with N?
**c)** the arrangement starts and ends with a vowel?
**d)** N and U are next to each other?
**e)** N and U are NOT next to each other?

**Solution**: NUMBER has 6 different letters, and 2 of them are vowels (U and E).
**a)** $6!=720$

**b)** N is fixed in the 1st position, and the other 5 letters can go anywhere: $5!=120$

**c)** 1st position: 2 vowels to choose from. Last position: the 1 vowel left. Middle 4 positions: $4!$
$$2\times4!\times1=48$$

**d)** Glue N and U into one block (see the image above): 5 units → $5!$, and NU or UN inside the block -> $2!$
$$5!\times2!=240$$

**e)** $720-240=480$

**Example 4:** The letters of NUMBER are arranged at random. Find the probability that N and U are next to each other.

**Solution**: Using Example 3:
$$\Pr(\text{N and U together})=\frac{240}{720}=\frac{1}{3}$$

---

## Exercises:

*Try each question first, then click on "Solution" to check your answer.*

**Question 1:** Evaluate:
**a)** 7!
**b)** 8! / 6!
**c)** ⁷P₃
**d)** Simplify (n + 1)! / (n − 1)!

> [!success]- Solution
> **a)** $7!=7\times6\times5\times4\times3\times2\times1=5040$
>
> **b)** $\dfrac{8!}{6!}=8\times7=56$
>
> **c)** ${}^{7}P_{3}=7\times6\times5=210$
>
> **d)**
> $$\frac{(n+1)!}{(n-1)!}=\frac{(n+1)\times n\times(n-1)!}{(n-1)!}=n(n+1)=n^2+n$$

**Question 2:** How many 3-digit numbers can be made from the digits 1, 2, 3, 4 and 5 if:
**a)** digits cannot be repeated?
**b)** digits can be repeated?
**c)** digits cannot be repeated and the number is even?
**d)** digits cannot be repeated and the number is greater than 300?

> [!success]- Solution
> **a)** $5\times4\times3=60$
>
> **b)** $5\times5\times5=125$
>
> **c)** Restricted position first: the last digit must be 2 or 4 (2 choices). Then the 1st digit has 4 choices left and the middle digit has 3.
> $$4\times3\times2=24$$
>
> **d)** The 1st digit must be 3, 4 or 5 (3 choices). Then the other two digits have 4 and 3 choices.
> $$3\times4\times3=36$$

**Question 3:** 8 runners are in a race. In how many ways can the gold, silver and bronze medals be awarded?

> [!success]- Solution
> Order matters (gold ≠ silver), so
> $${}^{8}P_{3}=8\times7\times6=336$$

**Question 4:** 4 boys and 3 girls stand in a row. How many arrangements are possible if:
**a)** there are no restrictions?
**b)** boys and girls alternate?
**c)** the 3 girls stand together?
**d)** there is a boy at each end?

> [!success]- Solution
> **a)** $7!=5040$
>
> **b)** With 4 boys and 3 girls, the only alternating pattern is B G B G B G B. Arrange the boys in their 4 spots and the girls in their 3 spots:
> $$4!\times3!=24\times6=144$$
>
> **c)** Glue the 3 girls into one block: 4 boys + 1 block = 5 units, and the girls can be ordered in $3!$ ways inside the block.
> $$5!\times3!=120\times6=720$$
>
> **d)** Left end: 4 boys to choose from. Right end: 3 boys left. Then the other 5 people fill the middle.
> $$4\times3\times5!=1440$$

**Question 5:**
**a)** How many different arrangements of the letters of COFFEE are there?
**b)** How many of these arrangements start with C?
**c)** An arrangement is chosen at random. Find the probability that it starts with C.

> [!success]- Solution
> **a)** 6 letters, with two F's and two E's:
> $$\frac{6!}{2!\times2!}=\frac{720}{4}=180$$
>
> **b)** Fix C first, then arrange O, F, F, E, E:
> $$\frac{5!}{2!\times2!}=\frac{120}{4}=30$$
>
> **c)**
> $$\Pr(\text{starts with C})=\frac{30}{180}=\frac{1}{6}$$
> *Check: 1 of the 6 letters is a C, so 1/6 makes sense.*

**Question 6:** 5 people, including Ann and Bob, sit in a row of 5 seats in random order. Find the probability that:
**a)** Ann and Bob sit next to each other.
**b)** Ann sits in the middle seat.
**c)** Ann and Bob do NOT sit next to each other.

> [!success]- Solution
> Total number of arrangements: $5!=120$
>
> **a)** Glue Ann and Bob into one block: $4!\times2!=48$
> $$\Pr(\text{next to each other})=\frac{48}{120}=\frac{2}{5}$$
>
> **b)** Ann is fixed in the middle, and the other 4 people fill the other seats: $4!=24$
> $$\Pr(\text{Ann in the middle})=\frac{24}{120}=\frac{1}{5}$$
>
> **c)**
> $$\Pr(\text{not next to each other})=1-\frac{2}{5}=\frac{3}{5}$$

**Question 7:** A 4-digit PIN uses the digits 0 to 9, with no digit repeated.
**a)** How many PINs are possible?
**b)** A PIN is chosen at random. Find the probability that all 4 of its digits are even.

> [!success]- Solution
> **a)**
> $${}^{10}P_{4}=10\times9\times8\times7=5040$$
>
> **b)** There are 5 even digits (0, 2, 4, 6, 8):
> $$\Pr(\text{all even})=\frac{{}^{5}P_{4}}{{}^{10}P_{4}}=\frac{120}{5040}=\frac{1}{42}$$

**Question 8:** Solve ⁿP₂ = 56.

> [!success]- Solution
> $${}^{n}P_{2}=n(n-1)=56$$
> $$n^2-n-56=0\Rightarrow(n-8)(n+7)=0\Rightarrow n=8$$
> (n = −7 is rejected, because n must be a positive whole number.)
