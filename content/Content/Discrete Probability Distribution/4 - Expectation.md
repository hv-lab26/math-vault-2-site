Roll a fair die thousands of times and work out the average of all the results. The average gets closer and closer to **3.5**, even though you can never actually roll a 3.5! This long-run average is called the expected value.

**Definition**: The **expected value** (or **expectation**) of a random variable X is the long-run average value of X if the experiment is repeated many, many times. It is also called the **mean** of X.

**Notation**: ==**E(X) = μ**==

*μ is the Greek letter "mu".*

## Formula:

Multiply each value of x by its probability, then add them all up:

==**E(X) = Σx·Pr(X = x)**==

In LaTeX:
$$E(X)=\mu=\sum_{i=1}^{n}x_i\,p_i=x_1p_1+x_2p_2+\dots+x_np_n$$

*e.g. a fair die:*
$$E(X)=1\times\frac{1}{6}+2\times\frac{1}{6}+3\times\frac{1}{6}+4\times\frac{1}{6}+5\times\frac{1}{6}+6\times\frac{1}{6}=\frac{21}{6}=3.5$$

*Note: the expected value does not have to be a value that X can take (you can't roll a 3.5, or borrow 2.4 books).*

The expected value is the **balance point** of the distribution: if each stick of the graph were a weight on a ruler, the ruler would balance exactly at E(X).

![[Expectation - Balance Point.png]]

> [!tip] Calculator tip (TI-84 Plus CE)
> Put the values of x in L1 and the probabilities in L2 (STAT → 1: Edit), then go to STAT → CALC → 1: 1-Var Stats, set List: L1 and FreqList: L2. The value of x̄ is E(X).

## Median:

**Definition**: The **median** of a random variable is the middle value of the distribution, i.e. the value such that 50% of the distribution is greater than it and 50% is less than it.

*For a discrete X, an exact 50/50 split is usually impossible (the probabilities come in chunks), so use the running-total rule below.*

**To find the median**, add the probabilities from the smallest value of X upwards until the running total **reaches or exceeds 0.5**:
- If the running total **exceeds** 0.5, the value of X reached is the median.
- If the running total **equals 0.5 exactly**, the median is **halfway** between this value and the next value.

![[Expectation - Median.png]]

## Mode:

**Definition**: The **mode** is the value of X with the **highest probability** (the most likely value).

## Expected value of a function of X:

To find the expected value of something like X² or 3X + 1, apply the function to each value of x, and keep the same probabilities:

==**E(g(X)) = Σg(x)·Pr(X = x)**==

*e.g.*
$$E(X^2)=\sum x^2\,\Pr(X=x)$$

*Warning: E(X²) is NOT the same as [E(X)]². Square the values first, then multiply by the probabilities.*

## Properties of expectation:

For constants a, b and k:

==**E(k) = k**==
==**E(aX) = aE(X)**==
==**E(aX + b) = aE(X) + b**==

**Why?** Because the probabilities add up to 1:
$$E(X+3)=\sum(x_i+3)p_i=\sum x_ip_i+3\sum p_i=E(X)+3\times1=E(X)+3$$

These rules also work for longer expressions, as long as you expand first:
$$E(X^2+2X+3)=E(X^2)+2E(X)+3$$

> [!tip] Exam tip
> E(aX + b) = aE(X) + b only works for **linear** functions. For anything else, like X², 1/X or √X, you must use the table: E(X²) ≠ [E(X)]² and E(1/X) ≠ 1/E(X).

> [!info] Fun fact: the St Petersburg paradox
> A casino offers a game: a coin is tossed until the first head appears. If it takes 1 toss you win \$2, 2 tosses \$4, 3 tosses \$8, and so on, doubling each time. The expected winnings are
> $$2\times\frac{1}{2}+4\times\frac{1}{4}+8\times\frac{1}{8}+\dots=1+1+1+\dots=\infty$$
> So the "fair" price to play would be infinite, yet hardly anyone would pay even \$20 to play! The mathematician Daniel Bernoulli wrote about this puzzle in 1738, and it is still used to explain why people don't make decisions using expected value alone.

---

## Examples:

**Example 1:** At the College library, the number of books a randomly selected semester 2 student borrows in a week is recorded. Let the random variable X represent the number of books borrowed. The probability distribution of X is:

| x         | 1   | 2    | 3    | 4    | 5    |
| --------- | --- | ---- | ---- | ---- | ---- |
| Pr(X = x) | 2/5 | 1/10 | 3/10 | 1/10 | 1/10 |

Find the expected number of books borrowed by a student in a week.

**Solution**:
$$E(X)=1\times\frac{2}{5}+2\times\frac{1}{10}+3\times\frac{3}{10}+4\times\frac{1}{10}+5\times\frac{1}{10}=\frac{4+2+9+4+5}{10}=\frac{24}{10}=\frac{12}{5}$$
On average, a student borrows **2.4 books** per week.

**Example 2:** A group of athletes attends optional training sessions each week. Let the random variable X represent the total number of hours a randomly selected athlete spends training in a week. The possible values are in multiples of 3 hours.

| x         | 0    | 3    | 6    | 9    | 12   |
| --------- | ---- | ---- | ---- | ---- | ---- |
| Pr(X = x) | 0.21 | 0.08 | 0.19 | 0.17 | 0.35 |

Find the expected number of hours an athlete trains per week.

**Solution**:
$$E(X)=0\times0.21+3\times0.08+6\times0.19+9\times0.17+12\times0.35=7.11$$
On average, an athlete trains **7.11 hours** per week.

**Example 3:** A local delivery company tracks how many parcels a driver delivers during a short shift. Let X represent the number of parcels delivered. Due to incomplete records, one of the probabilities (a) is missing.

| x         | 2   | 4   | 6   | 8   | 10  |
| --------- | --- | --- | --- | --- | --- |
| Pr(X = x) | 0.2 | 0.4 | a   | 0.1 | 0.1 |

**a)** Find the missing probability a.
**b)** Find the expected number of parcels delivered in a shift.

**Solution**:
**a)**
$$0.2+0.4+a+0.1+0.1=1\implies a=0.2$$

**b)**
$$E(X)=2\times0.2+4\times0.4+6\times0.2+8\times0.1+10\times0.1=0.4+1.6+1.2+0.8+1=5$$
On average, a driver delivers **5 parcels** per shift.

**Example 4:** A transport company is studying the number of delivery delays per driver each week. Let X represent the number of delayed deliveries a driver has in a week.

| x         | 1   | 2   | 3   | 4   | 5   | 6   | 7   |
| --------- | --- | --- | --- | --- | --- | --- | --- |
| Pr(X = x) | 0.1 | 0.1 | a   | 0.3 | 0.2 | b   | 0.2 |

It is also known that the expected number of delays per week is E(X) = 4.29. Find the values of a and b.

**Solution**: Two unknowns → we need two equations.
**Equation 1** (the probabilities add up to 1):
$$0.1+0.1+a+0.3+0.2+b+0.2=1\implies a+b=0.1\quad(1)$$

**Equation 2** (the expected value):
$$1(0.1)+2(0.1)+3a+4(0.3)+5(0.2)+6b+7(0.2)=4.29$$
$$3.9+3a+6b=4.29\implies3a+6b=0.39\quad(2)$$

From (1), a = 0.1 − b. Substitute into (2):
$$3(0.1-b)+6b=0.39\implies0.3+3b=0.39\implies b=0.03$$
$$a=0.1-0.03=0.07$$

So **a = 0.07** and **b = 0.03**.

**Example 5:** A newsagent records the number of magazines bought by customers who buy at least one magazine: 23% of these customers buy 1 magazine, 38% buy 2, 21% buy 3, 13% buy 4 and 5% buy 5.
**a)** Define a suitable random variable.
**b)** Make a probability table.
**c)** Find the expected value and explain what it means in this context.

**Solution**:
**a)** Let X = the number of magazines purchased by a randomly chosen customer (who buys at least one magazine).

**b)**

| x         | 1    | 2    | 3    | 4    | 5    |
| --------- | ---- | ---- | ---- | ---- | ---- |
| Pr(X = x) | 0.23 | 0.38 | 0.21 | 0.13 | 0.05 |

**c)**
$$E(X)=1\times0.23+2\times0.38+3\times0.21+4\times0.13+5\times0.05=2.39$$
On average, a customer who buys magazines buys **2.39 magazines**.

**Example 6:** Find the median and the mode of X.

| x         | 0     | 1     | 2     | 3     |
| --------- | ----- | ----- | ----- | ----- |
| Pr(X = x) | 0.064 | 0.288 | 0.432 | 0.216 |

**Solution**: Running total from the smallest value:
- x = 0: 0.064
- x = 1: 0.064 + 0.288 = 0.352 (still below 0.5)
- x = 2: 0.352 + 0.432 = 0.784 > 0.5 ✓

The running total passes 0.5 at x = 2, so **median = 2**.
The highest probability is 0.432, so **mode = 2**.

**Example 7:** Find the median, the mean and the mode of X.

| x         | 1   | 3   | 6   | 8   | 11  |
| --------- | --- | --- | --- | --- | --- |
| Pr(X = x) | 0.1 | 0.2 | 0.2 | 0.2 | 0.3 |

**Solution**:
**Median**: running totals: 0.1, 0.3, **0.5** (at x = 6, exactly 0.5!). The median is halfway between 6 and the next value, 8:
$$\text{median}=\frac{6+8}{2}=7$$

**Mean**:
$$E(X)=1\times0.1+3\times0.2+6\times0.2+8\times0.2+11\times0.3=0.1+0.6+1.2+1.6+3.3=6.8$$

**Mode**: x = 11 has the highest probability (0.3), so **mode = 11**.

*Note: the mean, median and mode can all be different!*

**Example 8:** For the athletes in Example 2, find the mode, the median and the mean.

**Solution**:
**Mode** = 12 (highest probability, 0.35).
**Median**: running totals: 0.21, 0.29, 0.48, **0.65** → passes 0.5 at x = 9, so **median = 9**.
**Mean** = 7.11 (from Example 2).

**Example 9:** A random variable has the following probability distribution:

| x         | 1    | 2    | 3    | 4    |
| --------- | ---- | ---- | ---- | ---- |
| Pr(X = x) | 0.25 | 0.26 | 0.14 | 0.35 |

Find **a)** E(X), **b)** E(3X), **c)** E(2X − 4), **d)** E(X²), **e)** E(X² + 2X + 3), **f)** [E(X)]².

**Solution**:
**a)**
$$E(X)=1\times0.25+2\times0.26+3\times0.14+4\times0.35=2.59$$

**b)**
$$E(3X)=3E(X)=3\times2.59=7.77$$

**c)**
$$E(2X-4)=2E(X)-4=2\times2.59-4=1.18$$

**d)** Square the values, keep the probabilities:
$$E(X^2)=1^2\times0.25+2^2\times0.26+3^2\times0.14+4^2\times0.35=0.25+1.04+1.26+5.6=8.15$$

**e)**
$$E(X^2+2X+3)=E(X^2)+2E(X)+3=8.15+2\times2.59+3=16.33$$

**f)**
$$[E(X)]^2=2.59^2=6.7081$$

*Compare d) and f): E(X²) = 8.15 but [E(X)]² = 6.7081. They are not the same! The difference between them is the [[5 - Variance|variance]].*

> [!info] Fun fact: the law of large numbers
> During World War II, the mathematician John Kerrich was held in an internment camp in Denmark and passed the time by tossing a coin **10 000 times**. He got 5067 heads, a proportion of 0.5067, very close to the expected 0.5. The more times you repeat an experiment, the closer the average gets to the expected value.

---

## Exercises:

*Try each question first, then click on "Solution" to check your answer.*

**Question 1:** The probability distribution of X is:

| x         | 0   | 1   | 2   | 3   |
| --------- | --- | --- | --- | --- |
| Pr(X = x) | 0.2 | p   | q   | 0.1 |

Given that E(X) = 1.4, find p and q.

> [!success]- Solution
> **Sum = 1:**
> $$0.2+p+q+0.1=1\implies p+q=0.7\quad(1)$$
> **E(X) = 1.4:**
> $$0(0.2)+1p+2q+3(0.1)=1.4\implies p+2q=1.1\quad(2)$$
> (2) − (1):
> $$q=0.4,\quad p=0.7-0.4=0.3$$

**Question 2:** Find the median, mode and mean of X.

| x         | 0   | 1   | 2   | 3    | 4    |
| --------- | --- | --- | --- | ---- | ---- |
| Pr(X = x) | 0.2 | 0.3 | 0.1 | 0.25 | 0.15 |

> [!success]- Solution
> **Median**: running totals: 0.2, **0.5** at x = 1 (exactly 0.5!), so the median is halfway between 1 and 2:
> $$\text{median}=\frac{1+2}{2}=1.5$$
> **Mode** = 1 (highest probability, 0.3).
> **Mean**:
> $$E(X)=0+0.3+0.2+0.75+0.6=1.85$$

**Question 3:** E(X) = 3 and E(X²) = 11. Find:
**a)** E(2X − 5)
**b)** E((X − 1)²)

> [!success]- Solution
> **a)**
> $$E(2X-5)=2E(X)-5=2\times3-5=1$$
>
> **b)** Expand first, then use the rules:
> $$E((X-1)^2)=E(X^2-2X+1)=E(X^2)-2E(X)+1=11-6+1=6$$
>
> *Common mistake: E((X − 1)²) ≠ (E(X) − 1)² = 4.*

**Question 4:** The probability distribution of X is:

| x         | 1   | 2    | 4    |
| --------- | --- | ---- | ---- |
| Pr(X = x) | 0.5 | 0.25 | 0.25 |

**a)** Find E(X).
**b)** Find E(1/X).
**c)** Is E(1/X) equal to 1/E(X)?

> [!success]- Solution
> **a)**
> $$E(X)=1\times0.5+2\times0.25+4\times0.25=2$$
>
> **b)** Apply 1/x to each value, keep the probabilities:
> $$E\left(\frac{1}{X}\right)=\frac{1}{1}\times0.5+\frac{1}{2}\times0.25+\frac{1}{4}\times0.25=0.5+0.125+0.0625=0.6875$$
>
> **c)** No: 1/E(X) = 1/2 = 0.5, but E(1/X) = 0.6875. The shortcut E(aX + b) = aE(X) + b only works for linear functions.

**Question 5:** Two fair dice are rolled, and X is the **larger** of the two numbers, with $\Pr(X=x)=\dfrac{2x-1}{36}$ for x = 1, 2, …, 6 (see [[3 - Discrete Probability Distributions]], Question 5). Find E(X).

> [!success]- Solution
> $$E(X)=\frac{1(1)+2(3)+3(5)+4(7)+5(9)+6(11)}{36}=\frac{1+6+15+28+45+66}{36}=\frac{161}{36}\approx4.47$$
>
> *Makes sense: the larger of two dice is usually bigger than the average of one die (3.5).*
