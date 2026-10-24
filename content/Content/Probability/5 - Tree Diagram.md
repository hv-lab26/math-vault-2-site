
Imagine tossing a coin, then tossing it again. The possible results are HH, HT, TH and TT, which are easy to list. But toss it 3 times, or take 2 marbles out of a bag without putting the first one back, and listing everything in your head gets messy fast. This is where a tree diagram comes in.

**Definition**: A tree diagram is a diagram that shows **all the possible outcomes** of a **multi-stage experiment** (an experiment done in two or more steps, e.g. tossing a coin twice). Each stage is drawn as a set of branches, and the probability of each result is written on its branch.

![[Tree Diagram - Structure.png]]

## Parts of a tree diagram:

- **Stage**: one step of the experiment (1st toss, 2nd toss,...).
- **Branch**: a line showing one possible result of a stage, with its probability written on it.
- **Outcome**: one complete path from the start to the end of the tree, e.g. A ∩ B. The list of all the outcomes is the **sample space**.

## Notations:

The branches on the 2nd stage depend on what happened on the 1st stage, so their probabilities are **conditional probabilities**. The probability of B, given that A has already happened, is written as:

==**Pr(B | A)**==

*read as "the probability of B given A."*

## Rules of a tree diagram:

**Rule 1:** The branches coming out of the same point add up to 1, because one of them must happen.

==**Pr(A) + Pr(A') = 1**==

**Rule 2:** **Multiply along the branches** to find the probability of an outcome (A **and** B).

==**Pr(A ∩ B) = Pr(A) × Pr(B | A)**==

*Note: if A and B are independent, then Pr(B | A) = Pr(B), so the rule becomes Pr(A ∩ B) = Pr(A) × Pr(B), the same as in [[3 - Laws of Probability]].*

**Rule 3:** **Add the outcomes** you need (outcome 1 **or** outcome 2). Two different paths can never happen at the same time (they are mutually exclusive), so we simply add them.

==**Pr(B) = Pr(A ∩ B) + Pr(A' ∩ B)**==

**Rule 4:** All the outcomes at the end of the tree add up to 1. *Use this to check your tree!*

> [!tip] Exam tip
> Write each outcome and its probability at the end of its path, like in the images on this page. Most marks are lost by multiplying along the wrong path, and this makes the right one easy to spot.

## With replacement vs. without replacement

**With replacement**: the object is put back before the next pick. The probabilities stay the same at every stage, so the stages are **independent**.

**Without replacement**: the object is NOT put back. There is one less object for the next pick, so the probabilities on the 2nd stage change, and the stages are **dependent**.

![[Tree Diagram - With vs Without Replacement.png]]

> [!tip] Tip
> In a "without replacement" tree, don't simplify the fractions on the branches (keep 2/4 instead of 1/2). Seeing the bottom numbers go 5 → 4 → 3 tells you straight away that the tree is right.

## Reading the tree backwards

Sometimes we know what happened on the 2nd stage and want the probability of what happened on the 1st stage. Divide the probability of the outcome you want by the total probability of what you already know:

==**Pr(A | B) = Pr(A ∩ B) / Pr(B)**==

*read as "the probability of A given B."* See Example 3.

> [!info] Fun fact: the medical test surprise
> The formula for reading a tree backwards is known as **Bayes' theorem**, after Thomas Bayes, an English minister whose idea was only published in 1763, two years after he died.
> It explains a famous surprise. A disease affects 1% of people. A test catches 95% of the people who have it, but it also wrongly flags 5% of healthy people. If you test positive (+), the chance that you actually have the disease (D) is only about **16%**!
> $$\Pr(D\mid +)=\frac{0.01\times0.95}{0.01\times0.95+0.99\times0.05}=\frac{0.0095}{0.059}\approx0.16$$
> Most positive results come from the huge healthy group, not from the tiny sick one.

---

## Examples:

**Example 1:** A fair coin is tossed 3 times.
**a)** Draw a tree diagram and list the sample space.
**b)** Find the probability of getting exactly two heads.
**c)** Find the probability of getting at least one head.

**Solution**:
**a)**
![[Tree Diagram - Three Coin Tosses.png]]
Sample space = {HHH, HHT, HTH, HTT, THH, THT, TTH, TTT}: 8 outcomes, each with probability $\dfrac{1}{2}\times\dfrac{1}{2}\times\dfrac{1}{2}=\dfrac{1}{8}$.

**b)** Exactly two heads: HHT, HTH, THH
$$\Pr(\text{exactly 2 heads})=\frac{1}{8}+\frac{1}{8}+\frac{1}{8}=\frac{3}{8}$$

**c)** "At least one head" is every outcome except TTT, so use the complement:
$$\Pr(\text{at least 1 head})=1-\Pr(TTT)=1-\frac{1}{8}=\frac{7}{8}$$

*Note: "at least one" → 1 − Pr(none). Much faster than adding 7 outcomes!*

> [!info] Fun fact
> A coin-toss tree doubles with every toss: 2 tosses → 4 outcomes, 3 tosses → 8 outcomes, and 10 tosses → 2¹⁰ = 1024 outcomes! For experiments that big, we use a formula instead of drawing the tree: the **binomial distribution**.

**Example 2:** A bag contains 3 red and 2 blue marbles. Two marbles are taken out one after another, **without replacement**.
**a)** Find Pr(both marbles are red).
**b)** Find Pr(one marble of each colour).
**c)** Find Pr(at least one marble is blue).

**Solution**: Use the "without replacement" tree above.
**a)**
$$\Pr(RR)=\frac{3}{5}\times\frac{2}{4}=\frac{6}{20}=\frac{3}{10}$$

**b)** One of each colour means RB **or** BR:
$$\Pr(RB)+\Pr(BR)=\frac{3}{5}\times\frac{2}{4}+\frac{2}{5}\times\frac{3}{4}=\frac{3}{10}+\frac{3}{10}=\frac{3}{5}$$

**c)**
$$\Pr(\text{at least 1 blue})=1-\Pr(RR)=1-\frac{3}{10}=\frac{7}{10}$$

**Example 3:** It rains on 30% of days. If it rains, the probability that a student is late to class is 0.4. If it does not rain, the probability is 0.1.
**a)** Find the probability that the student is late.
**b)** Given that the student is late, find the probability that it rained.

**Solution**: Let R = it rains and L = the student is late.
![[Tree Diagram - Rain and Late.png]]
**a)** The student can be late in 2 ways: R ∩ L **or** R' ∩ L.
$$\Pr(L)=0.3\times0.4+0.7\times0.1=0.12+0.07=0.19$$

**b)**
$$\Pr(R\mid L)=\frac{\Pr(R\cap L)}{\Pr(L)}=\frac{0.12}{0.19}=\frac{12}{19}\approx0.632$$

> [!info] Fun fact: the Monty Hall problem
> On a game show there are 3 doors: 1 hides a car and 2 hide goats. You pick a door. The host, who knows where the car is, opens one of the other doors to show a goat, then asks: "Do you want to switch?"
> Most people think it's 50/50, but a tree diagram shows that **switching wins 2/3 of the time**:
> - You first pick the car (probability 1/3) → switching loses.
> - You first pick a goat (probability 2/3) → the host has to show the other goat, so switching wins.
>
> $$\Pr(\text{win by switching})=\frac{2}{3}$$
> When this puzzle appeared in a magazine column in 1990, thousands of readers, including some mathematicians, wrote in to say the answer was wrong. It wasn't!

---

## Exercises:

*Try each question first, then click on "Solution" to check your answer.*

**Question 1:** A spinner has 3 equal sections numbered 1, 2 and 3. It is spun twice.
**a)** Draw a tree diagram and list the sample space.
**b)** Find Pr(two 3s).
**c)** Find Pr(the sum of the two numbers is 4).
**d)** Find Pr(at least one 3).

> [!success]- Solution
> **a)**
> ![[Tree Diagram - Exercise 1.png]]
> 9 outcomes, each with probability $\dfrac{1}{3}\times\dfrac{1}{3}=\dfrac{1}{9}$.
>
> **b)** Only one outcome, (3, 3):
> $$\Pr(\text{two 3s})=\frac{1}{9}$$
>
> **c)** A sum of 4 comes from (1, 3), (2, 2) and (3, 1):
> $$\Pr(\text{sum}=4)=\frac{3}{9}=\frac{1}{3}$$
>
> **d)** Use the complement: no 3 on either spin.
> $$\Pr(\text{at least one 3})=1-\frac{2}{3}\times\frac{2}{3}=1-\frac{4}{9}=\frac{5}{9}$$

**Question 2:** A bag contains 4 green and 6 yellow balls. A ball is drawn, its colour is recorded, and it is **put back**. Then a second ball is drawn.
**a)** Find Pr(both balls are green).
**b)** Find Pr(the two balls are different colours).
**c)** Find Pr(at least one ball is yellow).

> [!success]- Solution
> The ball is put back, so Pr(G) = 4/10 = 0.4 and Pr(Y) = 0.6 on **both** draws.
>
> **a)**
> $$\Pr(GG)=0.4\times0.4=0.16$$
>
> **b)** Different colours means GY **or** YG:
> $$\Pr(GY)+\Pr(YG)=0.4\times0.6+0.6\times0.4=0.48$$
>
> **c)**
> $$\Pr(\text{at least 1 yellow})=1-\Pr(GG)=1-0.16=0.84$$

**Question 3:** Repeat Question 2, but this time the first ball is **NOT put back**.
**a)** Draw a tree diagram.
**b)** Find Pr(both balls are green).
**c)** Find Pr(the two balls are different colours).
**d)** Find Pr(at least one ball is yellow).

> [!success]- Solution
> **a)**
> ![[Tree Diagram - Exercise 3.png]]
>
> **b)**
> $$\Pr(GG)=\frac{4}{10}\times\frac{3}{9}=\frac{12}{90}=\frac{2}{15}$$
>
> **c)**
> $$\Pr(GY)+\Pr(YG)=\frac{4}{10}\times\frac{6}{9}+\frac{6}{10}\times\frac{4}{9}=\frac{24}{90}+\frac{24}{90}=\frac{8}{15}$$
>
> **d)**
> $$\Pr(\text{at least 1 yellow})=1-\Pr(GG)=1-\frac{2}{15}=\frac{13}{15}$$
>
> *Compare with Question 2: Pr(GG) drops from 0.16 to 2/15 ≈ 0.133, because once a green ball is taken out, there are fewer green balls left.*

**Question 4:** A box contains 10 chocolates: 7 milk (M) and 3 dark (D). Three chocolates are eaten one after another, each chosen at random.
**a)** Draw a tree diagram.
**b)** Find Pr(all three are milk).
**c)** Find Pr(exactly one is dark).
**d)** Find Pr(at least one is dark).

> [!success]- Solution
> **a)**
> ![[Tree Diagram - Exercise 4.png]]
>
> **b)**
> $$\Pr(MMM)=\frac{7}{10}\times\frac{6}{9}\times\frac{5}{8}=\frac{210}{720}=\frac{7}{24}$$
>
> **c)** Exactly one dark: MMD, MDM or DMM. Each path has probability $\dfrac{126}{720}=\dfrac{7}{40}$, so
> $$\Pr(\text{exactly 1 dark})=3\times\frac{7}{40}=\frac{21}{40}$$
>
> **d)**
> $$\Pr(\text{at least 1 dark})=1-\Pr(MMM)=1-\frac{7}{24}=\frac{17}{24}$$

**Question 5:** Sam catches the bus (B) to school on 70% of days and the train (T) on the other days. When Sam catches the bus, the probability of being late (L) is 0.2. When Sam catches the train, the probability of being late is 0.05.
**a)** Draw a tree diagram.
**b)** Find the probability that Sam is late.
**c)** Given that Sam is late, find the probability that Sam caught the bus.

> [!success]- Solution
> **a)**
> ![[Tree Diagram - Exercise 5.png]]
>
> **b)** Late by bus **or** late by train:
> $$\Pr(L)=0.7\times0.2+0.3\times0.05=0.14+0.015=0.155$$
>
> **c)**
> $$\Pr(B\mid L)=\frac{\Pr(B\cap L)}{\Pr(L)}=\frac{0.14}{0.155}=\frac{28}{31}\approx0.903$$

**Question 6:** A biased coin has Pr(H) = p. The coin is tossed twice, and Pr(two heads) = 0.36.
**a)** Find p.
**b)** Find Pr(exactly one head).
**c)** Find Pr(at least one tail).

> [!success]- Solution
> **a)** The branches are p for H and 1 − p for T.
> $$\Pr(HH)=p\times p=p^2=0.36\Rightarrow p=0.6$$
> (p = −0.6 is rejected, because a probability can't be negative.)
>
> **b)**
> $$\Pr(HT)+\Pr(TH)=0.6\times0.4+0.4\times0.6=0.48$$
>
> **c)**
> $$\Pr(\text{at least 1 tail})=1-\Pr(HH)=1-0.36=0.64$$

**Question 7:** Ana and Ben play a best-of-three tennis match: the first player to win 2 sets wins the match. Ana wins any set with probability 0.6, independently of the other sets.
**a)** Draw a tree diagram.
**b)** Find Pr(Ana wins the match).
**c)** Find Pr(the match lasts 3 sets).
**d)** Given that the match lasts 3 sets, find Pr(Ana wins the match).

> [!success]- Solution
> **a)**
> ![[Tree Diagram - Exercise 7.png]]
> *The paths AA and BB stop after 2 sets, because the match is already over.*
>
> **b)** Ana wins with AA, ABA or BAA:
> $$\Pr(\text{Ana wins})=0.36+0.144+0.144=0.648$$
>
> **c)** A 3rd set is needed when the first two sets are split (AB or BA):
> $$\Pr(\text{3 sets})=0.6\times0.4+0.4\times0.6=0.48$$
>
> **d)**
> $$\Pr(\text{Ana wins}\mid\text{3 sets})=\frac{\Pr(ABA)+\Pr(BAA)}{\Pr(\text{3 sets})}=\frac{0.288}{0.48}=0.6$$
> *This makes sense: at 1–1, the 3rd set decides the match, and Ana wins any set with probability 0.6.*
