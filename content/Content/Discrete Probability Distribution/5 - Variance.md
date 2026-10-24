Two classes both have an average test score of 70%. In the first class, every student scored between 65% and 75%. In the second class, the scores ranged from 30% to 100%. The means are the same, but the classes are very different! The mean tells us the centre of a distribution; the variance tells us how **spread out** it is.

**Definition**: **Variance** is an important feature of probability distributions as it provides information about the **spread** of the distribution with respect to the mean.
- If the variance is **large**, the possible values are spread (or deviate) quite a distance from the mean.
- If the variance is **small**, the possible values are close to the mean.

Variance is also called a **measure of spread** or **dispersion**.

![[Variance - Same Mean Different Spread.png]]

## Notations:

==**E(X) = μ**== → the mean
==**Var(X) = σ²**== → the variance *(σ is the Greek letter "sigma")*
==**SD(X) = σ = √Var(X)**== → the standard deviation

## Formulas:

The variance is the expected value of the squared distance from the mean:

$$\operatorname{Var}(X)=E\left[(X-\mu)^2\right]=\sum(x-\mu)^2\,\Pr(X=x)$$

In practice, this shortcut is much quicker:

==**Var(X) = E(X²) − [E(X)]²**==

*Say it as "the mean of the squares minus the square of the mean".*

The **standard deviation** is the square root of the variance:

==**SD(X) = √Var(X)**==

*The variance is measured in squared units (e.g. slices²), which is hard to picture. The standard deviation is back in the same units as X (e.g. slices), so it's easier to interpret.*

**Steps to find the variance:**
1. Find E(X) = Σx·Pr(X = x).
2. Find E(X²) = Σx²·Pr(X = x).
3. Var(X) = E(X²) − [E(X)]².
4. If needed, SD(X) = √Var(X).

## Properties of variance:

==**Var(X) ≥ 0**== *(it's an average of squares, so it can never be negative)*
==**Var(b) = 0**== *(a constant doesn't vary)*
==**Var(aX + b) = a²Var(X)**==
==**SD(aX + b) = |a|·SD(X)**==

**Why?** Adding b moves every value by the same amount, so the spread doesn't change. Multiplying by a stretches every distance from the mean by a, so the squared distances are multiplied by a².

> [!tip] Exam tip
> If you ever get a **negative** variance, you have made a mistake, usually by calculating [E(X)]² − E(X²) instead of E(X²) − [E(X)]², or by squaring the probabilities instead of the values.

> [!tip] Calculator tip (TI-84 Plus CE)
> With the values in L1 and the probabilities in L2, 1-Var Stats L1, L2 gives x̄ = E(X) and **σx = SD(X)**. Use σx, not Sx (Sx is for samples of data).

> [!info] Fun fact: how much of the distribution is near the mean?
> For **any** distribution at all, at least 75% of the probability is within 2 standard deviations of the mean, and at least 8/9 (about 89%) is within 3. This guarantee is called **Chebyshev's inequality**, after the Russian mathematician Pafnuty Chebyshev (1821–1894). For bell-shaped distributions the numbers are much higher: about 95% within 2 standard deviations.

---

## Examples:

**Example 1:** The probability distribution of X is:

| x         | 1    | 2    | 3    | 4    |
| --------- | ---- | ---- | ---- | ---- |
| Pr(X = x) | 0.25 | 0.26 | 0.14 | 0.35 |

Find Var(X) and SD(X).

**Solution**: From [[4 - Expectation]] (Example 9), E(X) = 2.59 and E(X²) = 8.15.
$$\operatorname{Var}(X)=E(X^2)-[E(X)]^2=8.15-2.59^2=8.15-6.7081=1.4419$$
$$\operatorname{SD}(X)=\sqrt{1.4419}\approx1.2008$$

**Example 2:** The number of slices of pizza eaten by a randomly selected student is recorded. Let X represent the number of slices of pizza eaten by a student.

| x         | 1    | 2    | 3    | 4    | 5    |
| --------- | ---- | ---- | ---- | ---- | ---- |
| Pr(X = x) | 0.15 | 0.12 | 0.24 | 0.37 | 0.12 |

**a)** Find the expected value E(X).
**b)** Find the variance Var(X).
**c)** Interpret the expected value and the variance in this context.

**Solution**:
**a)**
$$E(X)=1(0.15)+2(0.12)+3(0.24)+4(0.37)+5(0.12)=0.15+0.24+0.72+1.48+0.6=3.19$$

**b)**
$$E(X^2)=1(0.15)+4(0.12)+9(0.24)+16(0.37)+25(0.12)=0.15+0.48+2.16+5.92+3=11.71$$
$$\operatorname{Var}(X)=11.71-3.19^2=11.71-10.1761=1.5339$$

**c)** On average, a student eats **3.19 slices** of pizza. The variance is 1.5339, so the standard deviation is
$$\sigma=\sqrt{1.5339}\approx1.24\text{ slices}$$
A typical student eats about 1.24 slices more or fewer than the mean, i.e. roughly between 2 and 4.4 slices.

![[Variance - Pizza.png]]

**Example 3:** For the library distribution in [[4 - Expectation]] (Example 1), E(X) = 2.4. Find Var(X) using **both** formulas.

| x         | 1   | 2   | 3   | 4   | 5   |
| --------- | --- | --- | --- | --- | --- |
| Pr(X = x) | 0.4 | 0.1 | 0.3 | 0.1 | 0.1 |

**Solution**:
**Using the definition** (squared distances from the mean 2.4):
$$\operatorname{Var}(X)=(1-2.4)^2(0.4)+(2-2.4)^2(0.1)+(3-2.4)^2(0.3)+(4-2.4)^2(0.1)+(5-2.4)^2(0.1)$$
$$=0.784+0.016+0.108+0.256+0.676=1.84$$

**Using the shortcut**:
$$E(X^2)=1(0.4)+4(0.1)+9(0.3)+16(0.1)+25(0.1)=7.6$$
$$\operatorname{Var}(X)=7.6-2.4^2=7.6-5.76=1.84$$

Both give **Var(X) = 1.84** ✓, but the shortcut has fewer messy decimals.

**Example 4:** Using Var(X) = 1.4419 from Example 1, find:
**a)** Var(3X)  **b)** Var(2X − 4)  **c)** SD(2X − 4)

**Solution**:
**a)**
$$\operatorname{Var}(3X)=3^2\times1.4419=12.9771$$

**b)** The −4 doesn't change the spread:
$$\operatorname{Var}(2X-4)=2^2\times1.4419=5.7676$$

**c)**
$$\operatorname{SD}(2X-4)=\sqrt{5.7676}\approx2.4016$$
*or* 2 × SD(X) = 2 × 1.2008 = 2.4016 ✓


---

## Exercises:

*Try each question first, then click on "Solution" to check your answer.*

**Question 1:** Let X be the result of rolling a fair die. Find Var(X) and SD(X).

> [!success]- Solution
> $$E(X)=\frac{1+2+3+4+5+6}{6}=3.5$$
> $$E(X^2)=\frac{1+4+9+16+25+36}{6}=\frac{91}{6}$$
> $$\operatorname{Var}(X)=\frac{91}{6}-3.5^2=\frac{91}{6}-\frac{49}{4}=\frac{35}{12}\approx2.9167$$
> $$\operatorname{SD}(X)=\sqrt{\frac{35}{12}}\approx1.7078$$

**Question 2:** The probability distribution of X is:

| x         | 1   | 2   | 3   |
| --------- | --- | --- | --- |
| Pr(X = x) | p   | q   | 0.3 |

Given that E(X) = 2.1:
**a)** Find p and q.
**b)** Find Var(X) and SD(X).

> [!success]- Solution
> **a)**
> $$p+q+0.3=1\implies p+q=0.7\quad(1)$$
> $$1p+2q+3(0.3)=2.1\implies p+2q=1.2\quad(2)$$
> (2) − (1): q = 0.5, so p = 0.2.
>
> **b)**
> $$E(X^2)=1(0.2)+4(0.5)+9(0.3)=4.9$$
> $$\operatorname{Var}(X)=4.9-2.1^2=4.9-4.41=0.49$$
> $$\operatorname{SD}(X)=\sqrt{0.49}=0.7$$

**Question 3:** Var(X) = 4. Find:
**a)** Var(5 − 3X)
**b)** SD(5 − 3X)

> [!success]- Solution
> **a)** Here a = −3 and b = 5:
> $$\operatorname{Var}(5-3X)=(-3)^2\times4=36$$
> **b)**
> $$\operatorname{SD}(5-3X)=\sqrt{36}=6$$
>
> *Common mistakes: −12 (forgot to square a), 41 (added the 5), or −6 (a standard deviation is never negative).*

**Question 4:** E(X) = 5 and Var(X) = 2. Find E(X²).

> [!success]- Solution
> Rearrange Var(X) = E(X²) − [E(X)]²:
> $$E(X^2)=\operatorname{Var}(X)+[E(X)]^2=2+5^2=27$$

**Question 5:** Without calculating, decide which distribution has the larger variance. Then check by calculating.

| x         | 1    | 2   | 3   | 4   | 5    |
| --------- | ---- | --- | --- | --- | ---- |
| Pr(X = x) | 0.05 | 0.2 | 0.5 | 0.2 | 0.05 |

| y         | 1   | 2   | 3   | 4   | 5   |
| --------- | --- | --- | --- | --- | --- |
| Pr(Y = y) | 0.3 | 0.1 | 0.2 | 0.1 | 0.3 |

> [!success]- Solution
> Both are symmetric about 3, so E(X) = E(Y) = 3. Y puts most of its probability at the ends (1 and 5), far from the mean, so **Y has the larger variance**.
> $$E(X^2)=1(0.05)+4(0.2)+9(0.5)+16(0.2)+25(0.05)=9.8\implies\operatorname{Var}(X)=9.8-9=0.8$$
> $$E(Y^2)=1(0.3)+4(0.1)+9(0.2)+16(0.1)+25(0.3)=11.6\implies\operatorname{Var}(Y)=11.6-9=2.6$$
> ✓ Var(Y) > Var(X). This is the picture at the top of this page.

**Question 6:** A student works out Var(X) and gets −0.36. Without seeing the working, explain what probably went wrong.

> [!success]- Solution
> A variance can never be negative, because it's an average of **squared** distances. The student probably calculated [E(X)]² − E(X²) (the wrong way round), or squared the probabilities instead of the values when finding E(X²).
