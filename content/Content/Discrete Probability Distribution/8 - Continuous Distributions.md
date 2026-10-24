What is the probability that a randomly chosen student is **exactly** 170 cm tall? Not 170.01 cm, not 169.999 cm, but exactly 170.000… cm? Surprisingly, the answer is **0**. A continuous random variable has infinitely many possible values, so we can't give each value its own probability like in a table. Instead, we use a curve, and probabilities become **areas** under that curve.

**Definition**: A **continuous random variable** can take any value in an interval (see [[2 - Types of Data]]). Its distribution is described by a **probability density function (pdf)**, f(x). The probability that X lies between a and b is the **area under the graph of f** between a and b:

==**Pr(a < X < b) = ∫ f(x) dx from a to b**==

In LaTeX:
$$\Pr(a<X<b)=\int_{a}^{b}f(x)\,dx$$

![[Continuous - Area Under Curve.png]]

*Finding these areas is integration, so revise [[3 - Definite Integrals]] and [[5 - Area Under Graph]] first.*

## Properties of a pdf:

For f(x) to be a probability density function, it must satisfy **both** conditions:

**Condition 1:** The graph is never below the x-axis.

==**f(x) ≥ 0 for all x**==

**Condition 2:** The total area under the graph is 1.

==**∫ f(x) dx over all x = 1**==
$$\int_{-\infty}^{\infty}f(x)\,dx=1\quad\text{or, if } f(x)=0 \text{ outside } [a,b]:\quad\int_{a}^{b}f(x)\,dx=1$$

*These are the continuous versions of "Pr(X = x) ≥ 0" and "ΣPr(X = x) = 1" from [[3 - Discrete Probability Distributions]] (but f(x) itself can be bigger than 1, see below).*

## The probability of a single value is 0:

==**Pr(X = a) = 0**==

The area of a single vertical line is 0. This means the end points don't matter:

$$\Pr(a<X<b)=\Pr(a\le X\le b)=\Pr(a<X\le b)=\Pr(a\le X<b)$$

*This is a big difference from discrete distributions, where Pr(X < 3) and Pr(X ≤ 3) can be different!*

*Note: f(x) is **not** a probability, so it can be bigger than 1. For example, f(x) = 2x on [0, 1] reaches f(1) = 2. Only areas are probabilities.*

## Piecewise (hybrid) functions:

A pdf is usually written as a piecewise function, e.g.
$$f(x)=\begin{cases}4-2x, & 1\le x\le 2\\ 0, & \text{elsewhere}\end{cases}$$
"Elsewhere" means everywhere else: here x < 1 or x > 2. 

## Median, percentiles and quantiles:

The **median** m splits the area in half:
$$\Pr(X\le m)=\int_{-\infty}^{m}f(x)\,dx=0.5$$

More generally, the value a with Pr(X ≤ a) = p is called the **p quantile** or the **100p-th percentile**.

*e.g. if Pr(X ≤ a) = 0.6, then a is the 0.6 quantile, or the 60th percentile.*

**Steps:**
1. Set up ∫ f(x) dx from the start of the domain to a, equal to the probability.
2. Integrate and solve for a.
3. **Reject** any solution outside the domain of f.

## Mean and variance of a continuous random variable:

The formulas are the same as for discrete variables, with Σ replaced by ∫ and Pr(X = x) replaced by f(x):

==**E(X) = ∫ x·f(x) dx**==
==**Var(X) = E(X²) − [E(X)]², where E(X²) = ∫ x²·f(x) dx**==

$$E(X)=\int_{-\infty}^{\infty}x\,f(x)\,dx,\qquad E(X^2)=\int_{-\infty}^{\infty}x^2f(x)\,dx$$

> [!tip] Calculator tip
> **TI-84 Plus CE**: MATH → 9: fnInt( → fill in the ∫ template with the lower limit, upper limit and f(X). *(In Classic mode, type fnInt(f(X), X, a, b), e.g. fnInt(0.5e^(−X/2), X, 0, 3) = 0.7769.)*
> **Casio fx-580VNX**: press the ∫ key, enter the function, then the lower and upper limits.

> [!tip] Exam tip
> For conditional probability, find the **intersection** first. *e.g.* "X > 9 **and** X > 8.5" is just "X > 9", because any number bigger than 9 is also bigger than 8.5.

---

## Examples:

**Example 1:** Determine whether each function may be a probability density function, and sketch its graph.

**a)**
$$f(x)=\begin{cases}4x, & 1\le x\le 2\\ 0, & \text{elsewhere}\end{cases}$$

**b)**
$$f(x)=\begin{cases}10x-4, & 0\le x\le 1\\ 0, & \text{elsewhere}\end{cases}$$

**c)**
$$f(x)=\begin{cases}0.5, & -1\le x\le 1\\ 0, & \text{elsewhere}\end{cases}$$

**Solution**:
**a)** Written in full: f(x) = 0 for x < 1, 4x for 1 ≤ x ≤ 2, and 0 for x > 2.
![[Continuous - Ex 1a.png]]
Condition 1: f(x) ≥ 0 ✓
Condition 2:
$$\int_{1}^{2}4x\,dx=\left[2x^2\right]_{1}^{2}=8-2=6\mathrel{\char"2260}1$$
→ **NOT a pdf**

**b)** Written in full: f(x) = 0 for x < 0, 10x − 4 for 0 ≤ x ≤ 1, and 0 for x > 1.
![[Continuous - Ex 1b.png]]
Condition 1: f(0) = −4 < 0. In fact, f(x) < 0 for all 0 ≤ x < 0.4 ✗
→ **NOT a pdf**

*Note: the area does come to $\int_0^1(10x-4)\,dx=[5x^2-4x]_0^1=1$, but that's not enough. Both conditions must be true!*

**c)** Written in full: f(x) = 0 for x < −1, 0.5 for −1 ≤ x ≤ 1, and 0 for x > 1.
![[Continuous - Ex 1c.png]]
Condition 1: f(x) ≥ 0 ✓
Condition 2:
$$\int_{-1}^{1}0.5\,dx=\left[0.5x\right]_{-1}^{1}=0.5-(-0.5)=1$$
→ **This is a pdf** ✓

**Example 2:** The function f(x) = a(12 − 3x) for 2 ≤ x ≤ 4, and 0 elsewhere, is a probability density function. Find the value of a.

**Solution**: The total area must be 1:
$$\int_{2}^{4}a(12-3x)\,dx=1$$
$$a\left[12x-\frac{3x^2}{2}\right]_{2}^{4}=1$$
$$a\left[(48-24)-(24-6)\right]=1\implies6a=1\implies a=\frac{1}{6}$$
$$f(x)=\begin{cases}\dfrac{1}{6}(12-3x), & 2\le x\le 4\\ 0, & \text{elsewhere}\end{cases}$$

![[Continuous - Ex 2.png]]

*Check: the graph is a triangle with base 2 and height f(2) = 1, so the area is ½ × 2 × 1 = 1 ✓*

**Example 3:** The continuous random variable X has the pdf
$$f(x)=\begin{cases}\dfrac{1}{2}x-4, & 8\le x\le 10\\ 0, & \text{elsewhere}\end{cases}$$
Find **a)** Pr(X > 9), **b)** Pr(8.5 < X < 9), **c)** Pr(X > 9 | X > 8.5).

**Solution**:
**a)**
$$\Pr(X>9)=\int_{9}^{10}\left(\frac{1}{2}x-4\right)dx=\left[\frac{x^2}{4}-4x\right]_{9}^{10}=(25-40)-(20.25-36)=0.75$$

**b)**
$$\Pr(8.5<X<9)=\int_{8.5}^{9}\left(\frac{1}{2}x-4\right)dx=(20.25-36)-(18.0625-34)=0.1875$$

**c)** "X > 9 and X > 8.5" is just X > 9, so
$$\Pr(X>9\mid X>8.5)=\frac{\Pr(X>9)}{\Pr(X>8.5)}=\frac{\int_{9}^{10}\left(\frac{1}{2}x-4\right)dx}{\int_{8.5}^{10}\left(\frac{1}{2}x-4\right)dx}=\frac{0.75}{0.9375}=0.8$$

![[Continuous - Ex 3.png]]

**Example 4:** The continuous random variable X has the pdf
$$f(x)=\begin{cases}\dfrac{1}{2}e^{-\frac{1}{2}x}, & x>0\\ 0, & x\le 0\end{cases}$$
**a)** Draw the graph of f.
**b)** Find:
i) Pr(X < 3)
ii) Pr(X > 2.5)
iii) Pr(X > 2.5 | X < 3)

**Solution**:
**a)** The graph starts at (0, ½) (open dot, since x > 0) and decreases towards 0 as x gets larger.
![[Continuous - Ex 4.png]]

**b)** An antiderivative of $\frac{1}{2}e^{-\frac{1}{2}x}$ is $-e^{-\frac{1}{2}x}$.
i)
$$\Pr(X<3)=\int_{0}^{3}\frac{1}{2}e^{-\frac{1}{2}x}\,dx=\left[-e^{-\frac{1}{2}x}\right]_{0}^{3}=1-e^{-1.5}\approx0.7769$$

ii) Use the complement:
$$\Pr(X>2.5)=1-\Pr(X<2.5)=1-\int_{0}^{2.5}\frac{1}{2}e^{-\frac{1}{2}x}\,dx=1-\left(1-e^{-1.25}\right)=e^{-1.25}\approx0.2865$$

iii) "X > 2.5 and X < 3" means 2.5 < X < 3:
$$\Pr(X>2.5\mid X<3)=\frac{\Pr(2.5<X<3)}{\Pr(X<3)}=\frac{\int_{2.5}^{3}\frac{1}{2}e^{-\frac{1}{2}x}\,dx}{0.7769}=\frac{e^{-1.25}-e^{-1.5}}{1-e^{-1.5}}\approx\frac{0.0634}{0.7769}\approx0.0816$$

**Example 5:** The continuous random variable X has the pdf
$$f(x)=\begin{cases}4-2x, & 1\le x\le 2\\ 0, & \text{elsewhere}\end{cases}$$
Find the value of a such that Pr(X ≤ a) = 0.75.

**Solution**: a must be between 1 and 2.
$$\int_{1}^{a}(4-2x)\,dx=0.75$$
$$\left[4x-x^2\right]_{1}^{a}=0.75\implies(4a-a^2)-(4-1)=0.75\implies a^2-4a+3.75=0$$
$$a=\frac{4\pm\sqrt{16-15}}{2}=\frac{4\pm1}{2}\implies a=1.5\ \text{ or }\ a=2.5$$
a = 2.5 is outside 1 ≤ a ≤ 2, so **a = 1.5**.

![[Continuous - Ex 5.png]]

**Example 6:** The continuous random variable X has the pdf
$$f(x)=\begin{cases}2x, & 0\le x\le 1\\ 0, & \text{elsewhere}\end{cases}$$
Find the 0.36 quantile (the 36th percentile).

**Solution**: Find a such that Pr(X ≤ a) = 0.36:
$$\int_{0}^{a}2x\,dx=0.36\implies\left[x^2\right]_{0}^{a}=0.36\implies a^2=0.36\implies a=\pm0.6$$
a must be between 0 and 1, so **a = 0.6**.

![[Continuous - Ex 6.png]]

**Example 7:** The time X (in minutes) between calls to a help desk has the pdf
$$f(x)=\begin{cases}0.6e^{-0.6x}, & x\ge 0\\ 0, & x<0\end{cases}$$
**a)** Find the probability that the next call comes within 30 seconds.
**b)** Find Pr(2 ≤ X ≤ 3).
**c)** Find the probability that there is no call for more than 7 minutes.

**Solution**: An antiderivative of $0.6e^{-0.6x}$ is $-e^{-0.6x}$.
**a)** 30 seconds = 0.5 minutes:
$$\Pr(X\le0.5)=\int_{0}^{0.5}0.6e^{-0.6x}\,dx=\left[-e^{-0.6x}\right]_{0}^{0.5}=1-e^{-0.3}\approx0.2592$$

**b)**
$$\Pr(2\le X\le3)=\int_{2}^{3}0.6e^{-0.6x}\,dx=e^{-1.2}-e^{-1.8}\approx0.1359$$

**c)**
$$\Pr(X>7)=1-\Pr(X\le7)=1-\int_{0}^{7}0.6e^{-0.6x}\,dx=e^{-4.2}\approx0.0150$$

![[Continuous - Ex 7.png]]

> [!info] Fun fact: half-life
> Pdfs like the ones in Examples 4 and 7, f(x) = λe^(−λx), are called **exponential distributions**. They describe waiting times, like the time until the next phone call, or the time until a radioactive atom decays. The median waiting time is ln 2 / λ, which in physics is called the **half-life**: the time it takes for half of the atoms to decay.

---

## Exercises:

*Try each question first, then click on "Solution" to check your answer.*

**Question 1:** The continuous random variable X has pdf f(x) = kx² for 0 ≤ x ≤ 3, and 0 elsewhere.
**a)** Find k.
**b)** Find Pr(X > 2).
**c)** Find the median of X.

> [!success]- Solution
> **a)**
> $$\int_{0}^{3}kx^2\,dx=1\implies k\left[\frac{x^3}{3}\right]_{0}^{3}=1\implies9k=1\implies k=\frac{1}{9}$$
> **b)**
> $$\Pr(X>2)=\int_{2}^{3}\frac{x^2}{9}\,dx=\left[\frac{x^3}{27}\right]_{2}^{3}=1-\frac{8}{27}=\frac{19}{27}$$
> **c)**
> $$\int_{0}^{m}\frac{x^2}{9}\,dx=0.5\implies\frac{m^3}{27}=0.5\implies m=\sqrt[3]{13.5}\approx2.381$$

**Question 2:** The continuous random variable X has pdf
$$f(x)=\begin{cases}kx, & 0\le x\le 2\\ k(4-x), & 2<x\le 4\\ 0, & \text{elsewhere}\end{cases}$$
**a)** Find k.
**b)** Find Pr(X < 1).
**c)** Find Pr(1 < X < 3).

> [!success]- Solution
> **a)** The graph is a triangle with base 4 and height f(2) = 2k:
> ![[Continuous - Triangle.png]]
> $$\frac{1}{2}\times4\times2k=1\implies4k=1\implies k=\frac{1}{4}$$
> *(or integrate both pieces: $\int_0^2 kx\,dx+\int_2^4 k(4-x)\,dx=2k+2k=4k$)*
>
> **b)**
> $$\Pr(X<1)=\int_{0}^{1}\frac{x}{4}\,dx=\left[\frac{x^2}{8}\right]_{0}^{1}=\frac{1}{8}$$
> **c)** The graph is symmetric about x = 2, so Pr(X > 3) = Pr(X < 1) = 1/8:
> $$\Pr(1<X<3)=1-\frac{1}{8}-\frac{1}{8}=\frac{3}{4}$$

**Question 3:** For the pdf f(x) = 2x, 0 ≤ x ≤ 1 (Example 6):
**a)** Find E(X).
**b)** Find Var(X).
**c)** Find Pr(X < E(X)). Is it equal to 0.5?

> [!success]- Solution
> **a)**
> $$E(X)=\int_{0}^{1}x\cdot2x\,dx=\left[\frac{2x^3}{3}\right]_{0}^{1}=\frac{2}{3}$$
> **b)**
> $$E(X^2)=\int_{0}^{1}x^2\cdot2x\,dx=\left[\frac{x^4}{2}\right]_{0}^{1}=\frac{1}{2}$$
> $$\operatorname{Var}(X)=\frac{1}{2}-\left(\frac{2}{3}\right)^2=\frac{1}{2}-\frac{4}{9}=\frac{1}{18}$$
> **c)**
> $$\Pr\left(X<\frac{2}{3}\right)=\left(\frac{2}{3}\right)^2=\frac{4}{9}\approx0.444$$
> No! The mean is not the median here. The distribution is skewed (most of the area is near x = 1), so the mean and the median are different. The median is $\sqrt{0.5}\approx0.707$.

**Question 4:** For the pdf in Example 4, f(x) = ½e^(−x/2), x > 0:
**a)** Find Pr(X > 5 | X > 3).
**b)** Compare your answer with Pr(X > 2). What do you notice?

> [!success]- Solution
> For this pdf, Pr(X > t) = e^(−t/2).
> **a)**
> $$\Pr(X>5\mid X>3)=\frac{\Pr(X>5)}{\Pr(X>3)}=\frac{e^{-2.5}}{e^{-1.5}}=e^{-1}\approx0.3679$$
> **b)**
> $$\Pr(X>2)=e^{-1}\approx0.3679$$
> They are the same! If X is a waiting time in minutes, then having already waited 3 minutes, the chance of waiting at least another 2 minutes is the same as if you had just started. The exponential distribution "has no memory", which is called the **memoryless property**.

**Question 5:** The function f(x) = 2/x² for 1 ≤ x ≤ b, and 0 elsewhere, is a pdf. Find b.

> [!success]- Solution
> $$\int_{1}^{b}\frac{2}{x^2}\,dx=1\implies\left[-\frac{2}{x}\right]_{1}^{b}=1\implies-\frac{2}{b}+2=1\implies b=2$$

**Question 6:** Explain why f(x) = 3 for 0 ≤ x ≤ 1/3 (and 0 elsewhere) is a valid pdf, even though f(x) > 1.

> [!success]- Solution
> f(x) ≥ 0 everywhere ✓, and the area is a rectangle: 3 × 1/3 = 1 ✓. Both conditions are true, so it's a pdf.
> f(x) is a **density**, not a probability, so it is allowed to be bigger than 1. Only areas under f have to be between 0 and 1.

**Question 7:** For the help desk in Example 7, find the median waiting time between calls.

> [!success]- Solution
> $$\int_{0}^{m}0.6e^{-0.6x}\,dx=0.5\implies1-e^{-0.6m}=0.5\implies e^{-0.6m}=0.5$$
> $$m=\frac{\ln2}{0.6}\approx1.155\text{ minutes}\ (\approx69\text{ seconds})$$

**Question 8:** For the pdf in Example 5, f(x) = 4 − 2x on [1, 2], find the 90th percentile.

> [!success]- Solution
> $$\int_{1}^{a}(4-2x)\,dx=0.9\implies4a-a^2-3=0.9\implies a^2-4a+3.9=0$$
> $$a=\frac{4\pm\sqrt{16-15.6}}{2}=2\pm\sqrt{0.1}$$
> a = 2 + √0.1 ≈ 2.316 is outside [1, 2], so **a = 2 − √0.1 ≈ 1.684**.
