Toss a coin 10 times and count the heads. A [[5 - Tree Diagram|tree diagram]] for this would have 2¹⁰ = 1024 branches at the end! Luckily, experiments like this, where the same thing is repeated again and again, follow a pattern, and one formula gives every probability. This is the binomial distribution.

**Definition**: A **binomial experiment** is an experiment where:
1. There is a **fixed number of trials**, n.
2. Each trial has only **two outcomes**: "success" or "failure".
3. The **probability of success, p, is the same** for every trial.
4. The trials are **independent** (the result of one trial doesn't affect the others).

If X is the **number of successes** in the n trials, then X has a **binomial distribution**:

==**X ~ B(n, p)**==

*read as "X is distributed binomially with n trials and probability of success p".*
- n = the number of trials
- p = the probability of success
- X can take the values 0, 1, 2, …, n

*Note: "success" is just the outcome we are counting. It doesn't have to be a good thing (e.g. X = the number of faulty batteries).*

## Formula:

==**Pr(X = x) = ⁿCₓ · pˣ · (1 − p)ⁿ⁻ˣ, x = 0, 1, …, n**==

In LaTeX:
$$\Pr(X=x)=\binom{n}{x}p^{x}(1-p)^{n-x}$$

**Why?** Think of a tree diagram. Every path with exactly x successes and n − x failures has probability pˣ(1 − p)ⁿ⁻ˣ, and the number of such paths is the number of ways to **choose** which x of the n trials are the successes: ⁿCₓ (see [[8 - Combinations]]).

*e.g. 3 coin tosses, X = number of tails: Pr(X = 2) = ³C₂ × 0.5² × 0.5¹ = 3/8, the same answer as the tree in [[3 - Discrete Probability Distributions]].*

## Mean and variance:

==**E(X) = μ = np**==
==**Var(X) = σ² = np(1 − p)**==
==**SD(X) = σ = √(np(1 − p))**==

*Sometimes q = 1 − p (the probability of failure) is used, so Var(X) = npq.*

*Makes sense: if you toss a coin 100 times, you expect 100 × 0.5 = 50 heads.*

## Shape of the distribution:

![[Binomial - Shapes.png]]

- p < 0.5 → **positively skewed** (tail on the right)
- p = 0.5 → **symmetric**
- p > 0.5 → **negatively skewed** (tail on the left)

The peak is always close to the mean np.

## Using the calculator:

| Probability       | TI-84 Plus CE (2nd → VARS = DISTR)           | Casio fx-580VNX                                         |
| ----------------- | -------------------------------------------- | ------------------------------------------------------- |
| Pr(X = x)         | A: binompdf(n, p, x)                         | MENU → Distribution → Binomial PD → Variable → x, N, p |
| Pr(X ≤ x)         | B: binomcdf(n, p, x)                         | MENU → Distribution → Binomial CD → Variable → x, N, p |

- **pdf** = probability of **exactly** one value.
- **cdf** = **cumulative**: adds up all the probabilities from 0 to x, i.e. Pr(X ≤ x).

## From words to the calculator:

The calculator's cdf only gives Pr(X ≤ x), so every other inequality must be rewritten first:

| Words                          | Symbol          | Rewrite as               | Calculator (TI-84)                 |
| ------------------------------ | --------------- | ------------------------ | ---------------------------------- |
| exactly 3                      | Pr(X = 3)       |                          | binompdf(n, p, 3)                  |
| at most 3 / no more than 3     | Pr(X ≤ 3)       |                          | binomcdf(n, p, 3)                  |
| less than 3 / fewer than 3     | Pr(X < 3)       | Pr(X ≤ 2)                | binomcdf(n, p, 2)                  |
| at least 3 / no fewer than 3   | Pr(X ≥ 3)       | 1 − Pr(X ≤ 2)            | 1 − binomcdf(n, p, 2)              |
| more than 3                    | Pr(X > 3)       | 1 − Pr(X ≤ 3)            | 1 − binomcdf(n, p, 3)              |
| from 2 to 5 (inclusive)        | Pr(2 ≤ X ≤ 5)   | Pr(X ≤ 5) − Pr(X ≤ 1)    | binomcdf(n, p, 5) − binomcdf(n, p, 1) |
| at least one                   | Pr(X ≥ 1)       | 1 − Pr(X = 0)            | 1 − (1 − p)ⁿ                       |

> [!tip] Exam tip
> X is discrete, so **"<" and "≤" are different**: Pr(X < 3) = Pr(X ≤ 2). Draw a quick number line 0, 1, 2, 3, … and circle the values you need before you touch the calculator.

> [!tip] Tip
> In two-step questions (see Examples 4, 5 and 7, and Question 6), the answer to the first part becomes the p of a new binomial distribution. Keep the **unrounded** answer in your calculator (2nd → (−) = ANS on the TI-84) instead of retyping a rounded value, or your final answer can be off in the 4th decimal place.

## Finding n:

Sometimes p and the probability are given, and we need the **number of trials n**.

**"At least one" questions** can be solved with logarithms:
$$\Pr(X\ge1)=1-(1-p)^n>k\implies(1-p)^n<1-k\implies n>\frac{\ln(1-k)}{\ln(1-p)}$$

*The inequality sign flips because ln(1 − p) is negative. Always round **up** to the next whole number.*

![[Binomial - Finding n.png]]

**Other questions** ("at least 2", "exactly 3", …) are solved by **trial and error**: try values of n on the calculator until the condition is true. On the TI-84, you can type the probability as a function of X in Y= and look at the TABLE.

> [!tip] Tip
> For "at least" questions, the probability keeps increasing as n increases, so the first n that works is the answer. But for "**exactly**" questions, the probability goes **up and then down again**, so there can be a whole range of values of n that work (see Example 10).


---

## Examples:

**Example 1:** A fair die is rolled twelve times and X is the number of sixes that could result.
**a)** Find the mean and standard deviation of X.
**b)** What is the probability of getting exactly 3 sixes?

**Solution**: n = 12 trials, success = rolling a six, p = Pr(6) = 1/6.
$$X\sim B\left(12,\frac{1}{6}\right)$$

**a)**
$$E(X)=np=12\times\frac{1}{6}=2$$
$$\operatorname{Var}(X)=np(1-p)=12\times\frac{1}{6}\times\frac{5}{6}=\frac{5}{3}$$
$$\operatorname{SD}(X)=\sqrt{\frac{5}{3}}\approx1.291$$

**b)**
$$\Pr(X=3)=\binom{12}{3}\left(\frac{1}{6}\right)^3\left(\frac{5}{6}\right)^{12-3}\approx0.1974$$
*Calculator: binompdf(12, 1/6, 3) = 0.1974*

![[Binomial - Twelve Dice.png]]

**Example 2:** 72% of union members are in favour of a certain change to their conditions of employment. A random sample of five members is chosen. Let X be the number of union members in the sample who are in favour of the change.
**a)** State the values of n and p, and the possible values of X.
**b)** Calculate the expected number of members who are in favour of the change.
**c)** Calculate the variance of X.
**d)** Calculate the standard deviation of X.
**e)** Calculate the probability that exactly 2 members are in favour of the change.
**f)** Calculate the probability that more than 3 members are in favour of the change.
**g)** Calculate the probability that fewer than 5 members are in favour of the change.

**Solution**:
**a)** n = 5, p = 0.72, so X ~ B(5, 0.72), and x ∈ {0, 1, 2, 3, 4, 5}.

**b)**
$$E(X)=np=5\times0.72=3.6$$

**c)**
$$\operatorname{Var}(X)=np(1-p)=5\times0.72\times0.28=1.008$$

**d)**
$$\operatorname{SD}(X)=\sqrt{1.008}\approx1.004$$

**e)**
$$\Pr(X=2)=\binom{5}{2}(0.72)^2(0.28)^3\approx0.1138$$
*binompdf(5, 0.72, 2)*

**f)**
$$\Pr(X>3)=\Pr(X=4)+\Pr(X=5)=1-\Pr(X\le3)\approx0.5697$$
*1 − binomcdf(5, 0.72, 3)*

**g)**
$$\Pr(X<5)=\Pr(X\le4)=1-\Pr(X=5)=1-0.72^5\approx0.8065$$
*binomcdf(5, 0.72, 4)*

**Example 3:** 5% of a batch of batteries are defective. A random sample of 80 batteries is taken with replacement.
**i.** Find the mean and standard deviation of the number of defective batteries in the sample.
**ii.** What is the probability of the sample having no defective battery?
**iii.** What is the probability of the sample having more than 3 defective batteries?

**Solution**: X = number of defective batteries, X ~ B(80, 0.05).
**i.**
$$E(X)=80\times0.05=4,\qquad\operatorname{SD}(X)=\sqrt{80\times0.05\times0.95}=\sqrt{3.8}\approx1.949$$

**ii.**
$$\Pr(X=0)=0.95^{80}\approx0.0165$$
*binompdf(80, 0.05, 0)*

**iii.**
$$\Pr(X>3)=1-\Pr(X\le3)\approx0.5716$$
*1 − binomcdf(80, 0.05, 3)*

**Example 4:** A basketball player makes 70% of her free throws. In each game, she takes 10 free throws.
**a)** Find the probability that she makes at least 8 free throws in a game.
**b)** Find the probability that, over her next 10 games, she makes at least 8 free throws in exactly 9 of the games.

**Solution**:
**a)** X = number of free throws made in a game, X ~ B(10, 0.7).
$$\Pr(X\ge8)=1-\Pr(X\le7)=1-\text{binomcdf}(10,0.7,7)\approx0.3828$$

**b)** Now each **game** is a trial, and "success" = making at least 8 free throws, with probability 0.3828 from a). Let Y = number of such games out of 10:
$$Y\sim B(10,0.3828)$$
$$\Pr(Y=9)=\text{binompdf}(10,0.3828\ldots,9)\approx0.0011$$

**Example 5:** 65% of the seeds of a certain plant germinate. Seeds are sold in packets of 12. *(Give answers to 4 decimal places.)*
**a)** Find the probability that at least 9 seeds in a packet germinate.
**b)** A gardener buys 10 packets. Find the probability that exactly 8 of the packets have at least 9 seeds germinating.

**Solution**:
**a)** X ~ B(12, 0.65):
$$\Pr(X\ge9)=1-\Pr(X\le8)=1-\text{binomcdf}(12,0.65,8)\approx0.3467$$

**b)** Each packet is a trial with p = 0.3467. Y = number of packets out of 10 with at least 9 seeds germinating:
$$Y\sim B(10,0.3467)$$
$$\Pr(Y=8)=\text{binompdf}(10,0.3467\ldots,8)\approx0.0040$$

**Example 6:** 75% of the students at a school own a smartphone. 15 students are chosen at random. Find the probability that at least 10 of them own a smartphone.

**Solution**: X ~ B(15, 0.75):
$$\Pr(X\ge10)=1-\Pr(X\le9)=1-\text{binomcdf}(15,0.75,9)\approx0.8516$$

**Example 7:** 5% of light bulbs are faulty. The bulbs are packed in boxes of 6.
**a)** Find the probability that a box contains at most 1 faulty bulb.
**b)** A shop orders 24 boxes. Find the probability that at least 22 of the boxes contain at most 1 faulty bulb.

**Solution**:
**a)** X = number of faulty bulbs in a box, X ~ B(6, 0.05):
$$\Pr(X\le1)=\text{binomcdf}(6,0.05,1)\approx0.9672$$

**b)** Each box is a trial with p ≈ 0.9672 (keep the unrounded value). Y = number of boxes out of 24 with at most 1 faulty bulb:
$$Y\sim B(24,0.9672)$$
$$\Pr(Y\ge22)=1-\Pr(Y\le21)=1-\text{binomcdf}(24,0.9672\ldots,21)\approx0.9574$$

### Finding n:

**Example 8:** Only 1/3 of the selfies a student takes are good enough to post. What is the minimum number of selfies she must take so that the probability of getting at least 2 acceptable selfies is more than 0.9?

**Solution**: X = number of acceptable selfies, X ~ B(n, 1/3).
$$\Pr(X\ge2)>0.9\implies1-\Pr(X\le1)>0.9\implies1-\text{binomcdf}\left(n,\tfrac{1}{3},1\right)>0.9$$

Trial and error:

| n  | Pr(X ≥ 2) |
| -- | --------- |
| 10 | 0.8960    |
| 11 | 0.9249 ✓  |

The minimum number of selfies is **11**.

**Example 9:** 30% of customers at a café order a hot chocolate. How many customers must be observed so that the probability that at least one of them orders a hot chocolate is greater than 0.95?

**Solution**: X ~ B(n, 0.3).
$$\Pr(X\ge1)>0.95\implies1-0.7^n>0.95\implies0.7^n<0.05$$
$$n>\frac{\ln0.05}{\ln0.7}\approx8.40$$
Round up: **n = 9**.
*Check: n = 8 gives 1 − 0.7⁸ ≈ 0.9424 (too small); n = 9 gives 1 − 0.7⁹ ≈ 0.9596 ✓*

**Example 10:** X ~ B(n, 0.2). Find the minimum value of n such that Pr(X = 3) > 0.1.

**Solution**: "Exactly 3", so use binompdf(n, 0.2, 3) and try values of n:

| n | Pr(X = 3) |
| - | --------- |
| 5 | 0.0512    |
| 6 | 0.0819    |
| 7 | 0.1147 ✓  |

The minimum is **n = 7**.

*Note: with "exactly", the probability doesn't keep increasing. It rises to a peak and then falls again, and it drops below 0.1 again after n = 27. So Pr(X = 3) > 0.1 only for 7 ≤ n ≤ 27.*

![[Binomial - Finding n Tricky.png]]

**Example 11:** An archer hits the target with probability 0.4 on each shot (so she misses with probability 0.6), independently of other shots.
**a)** She takes 6 shots.
i) Find the probability that she misses all 6 shots.
ii) Find the probability that she hits the target at least once.
**b)** Find the minimum number of shots she needs so that the probability of hitting the target at least once is greater than 0.8.

**Solution**:
**a)** i) X = number of misses, X ~ B(6, 0.6):
$$\Pr(X=6)=\text{binompdf}(6,0.6,6)=0.6^6\approx0.0467$$

ii) Y = number of hits, Y ~ B(6, 0.4):
$$\Pr(Y\ge1)=1-\Pr(Y=0)=1-0.6^6\approx0.9533$$

**b)** Y ~ B(n, 0.4):
$$\Pr(Y\ge1)>0.8\implies1-0.6^n>0.8\implies0.6^n<0.2\implies n>\frac{\ln0.2}{\ln0.6}\approx3.15$$
Round up: **n = 4**.
*Check: n = 3 gives 1 − 0.6³ = 0.784; n = 4 gives 1 − 0.6⁴ = 0.8704*

> [!info] Fun fact: Pascal's triangle
> The numbers ⁿCₓ in the binomial formula are the numbers in **Pascal's triangle**: row n gives ⁿC₀, ⁿC₁, …, ⁿCₙ. The triangle is named after Blaise Pascal (1600s), but it was known much earlier: the Chinese mathematician Yang Hui wrote about it in 1261, and in China it is still called "Yang Hui's triangle".

---

## Exercises:

*Try each question first, then click on "Solution" to check your answer.*

**Question 1:** Decide whether each random variable is binomial. If it is, state n and p.
**a)** The number of heads in 20 tosses of a fair coin
**b)** The number of aces when 5 cards are dealt from a deck (without replacement)
**c)** The number of rolls of a die needed to get the first six
**d)** The number of red balls when 4 balls are drawn **with replacement** from a bag of 3 red and 7 blue balls
**e)** The number of left-handed students in a random group of 30, if 10% of people are left-handed

> [!success]- Solution
> **a)** Binomial: X ~ B(20, 0.5)
> **b)** **Not** binomial: the cards aren't put back, so the probability of an ace changes from card to card (the trials aren't independent).
> **c)** **Not** binomial: the number of trials isn't fixed (we keep rolling until a six appears).
> **d)** Binomial: X ~ B(4, 0.3)
> **e)** Binomial (assuming the students are chosen independently): X ~ B(30, 0.1)

**Question 2:** X ~ B(8, 0.25). Find:
**a)** Pr(X = 2)  **b)** Pr(X ≤ 2)  **c)** Pr(X ≥ 3)  **d)** E(X) and SD(X)

> [!success]- Solution
> **a)**
> $$\Pr(X=2)=\binom{8}{2}(0.25)^2(0.75)^6\approx0.3115$$
> **b)**
> $$\Pr(X\le2)=\text{binomcdf}(8,0.25,2)\approx0.6785$$
> **c)**
> $$\Pr(X\ge3)=1-\Pr(X\le2)\approx0.3215$$
> **d)**
> $$E(X)=8\times0.25=2,\qquad\operatorname{SD}(X)=\sqrt{8\times0.25\times0.75}=\sqrt{1.5}\approx1.2247$$

**Question 3:** X has a binomial distribution with mean 6 and variance 4.2. Find n and p.

> [!success]- Solution
> $$np=6\quad(1),\qquad np(1-p)=4.2\quad(2)$$
> Divide (2) by (1):
> $$1-p=\frac{4.2}{6}=0.7\implies p=0.3$$
> $$n=\frac{6}{0.3}=20$$
> So X ~ B(20, 0.3).

**Question 4:** X ~ B(10, 0.4). Find Pr(X ≥ 5 | X ≥ 3).

> [!success]- Solution
> If X ≥ 5, then X ≥ 3 is automatically true, so the intersection is just X ≥ 5:
> $$\Pr(X\ge5\mid X\ge3)=\frac{\Pr(X\ge5)}{\Pr(X\ge3)}=\frac{1-\text{binomcdf}(10,0.4,4)}{1-\text{binomcdf}(10,0.4,2)}\approx\frac{0.3669}{0.8327}\approx0.4406$$

**Question 5:** X ~ B(4, p) and Pr(X = 0) = 0.0256.
**a)** Find p.
**b)** Find Pr(X ≥ 3).

> [!success]- Solution
> **a)**
> $$\Pr(X=0)=(1-p)^4=0.0256\implies1-p=\sqrt[4]{0.0256}=0.4\implies p=0.6$$
> **b)**
> $$\Pr(X\ge3)=\binom{4}{3}(0.6)^3(0.4)+(0.6)^4=0.3456+0.1296=0.4752$$

**Question 6:** 2% of the phones made in a factory are faulty. Phones are packed in boxes of 20, and a box is rejected if it contains more than 1 faulty phone.
**a)** Find the probability that a box is rejected.
**b)** Find the probability that, out of 10 boxes, at most 1 is rejected.

> [!success]- Solution
> **a)** X = number of faulty phones in a box, X ~ B(20, 0.02):
> $$\Pr(X>1)=1-\Pr(X\le1)=1-\text{binomcdf}(20,0.02,1)\approx0.0599$$
> **b)** Y = number of rejected boxes, Y ~ B(10, 0.0599…):
> $$\Pr(Y\le1)=\text{binomcdf}(10,0.0599\ldots,1)\approx0.8827$$

**Question 7:** How many times must a fair die be rolled so that the probability of getting **at least two** sixes is more than 0.5?

> [!success]- Solution
> X ~ B(n, 1/6). We need Pr(X ≥ 2) = 1 − binomcdf(n, 1/6, 1) > 0.5.
>
> | n  | Pr(X ≥ 2) |
> | -- | --------- |
> | 9  | 0.4573    |
> | 10 | 0.5155 ✓  |
>
> The die must be rolled at least **10** times.
>
> *Logarithms don't work here: Pr(X ≥ 2) = 1 − (5/6)ⁿ − n(1/6)(5/6)ⁿ⁻¹ has n both in a power and as a multiplier, so n can't be isolated. Trial and error is the way to go.*
