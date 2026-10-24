## Notes
1. [[2 - Types of Data]] - discrete vs continuous data, random variables
2. [[3 - Discrete Probability Distributions]] - probability tables, finding k, Pr(a < X ≤ b)
3. [[4 - Expectation]] - mean E(X), median, mode, E(aX + b)
4. [[5 - Variance]] - Var(X), standard deviation, Var(aX + b)
5. [[6 - Fair Games]] - expected profit, fair price, house edge
6. [[7 - Binomial Distribution]] - X ~ B(n, p), binompdf / binomcdf, finding n
7. [[8 - Continuous Distributions]] - pdf, area under the curve, median and quantiles

## Formula sheet
| Rule                         | Formula                                                                              |
| ---------------------------- | ------------------------------------------------------------------------------------ |
| Discrete distribution        | $0\le\Pr(X=x)\le1$ and $\sum\Pr(X=x)=1$                                              |
| Expected value (mean)        | $E(X)=\mu=\sum x\,\Pr(X=x)$                                                          |
| Expected value of g(X)       | $E(g(X))=\sum g(x)\,\Pr(X=x)$                                                        |
| Linear rules                 | $E(aX+b)=aE(X)+b$, $E(k)=k$                                                          |
| Variance                     | $\operatorname{Var}(X)=E(X^2)-[E(X)]^2=E\left[(X-\mu)^2\right]$                     |
| Standard deviation           | $\operatorname{SD}(X)=\sigma=\sqrt{\operatorname{Var}(X)}$                           |
| Variance of aX + b           | $\operatorname{Var}(aX+b)=a^2\operatorname{Var}(X)$                                  |
| Fair game                    | $E(\text{profit})=E(\text{winnings})-\text{cost}=0$                                  |
| Binomial probability         | $X\sim B(n,p)$: $\Pr(X=x)=\dbinom{n}{x}p^x(1-p)^{n-x}$                               |
| Binomial mean and variance   | $E(X)=np$, $\operatorname{Var}(X)=np(1-p)$                                           |
| "At least one" (binomial)    | $\Pr(X\ge1)=1-(1-p)^n$                                                               |
| Continuous probability       | $\Pr(a<X<b)=\displaystyle\int_a^b f(x)\,dx$                                          |
| Probability density function | $f(x)\ge0$ and $\displaystyle\int_{-\infty}^{\infty}f(x)\,dx=1$                       |
| Single value (continuous)    | $\Pr(X=a)=0$                                                                         |
| Median / p quantile          | $\displaystyle\int_{-\infty}^{m}f(x)\,dx=0.5$, $\displaystyle\int_{-\infty}^{a}f(x)\,dx=p$ |
| Continuous mean              | $E(X)=\displaystyle\int_{-\infty}^{\infty}x\,f(x)\,dx$                               |

## Discrete vs continuous
|                    | Discrete random variable              | Continuous random variable                  |
| ------------------ | ------------------------------------- | ------------------------------------------- |
| Values             | separate values (counted)             | any value in an interval (measured)         |
| Described by       | a table or a rule for Pr(X = x)       | a pdf f(x)                                  |
| Probabilities      | add the probabilities                 | area under the curve (integrate)            |
| Total              | ΣPr(X = x) = 1                        | ∫ f(x) dx = 1                               |
| Pr(X = a)          | can be bigger than 0                  | always 0                                    |
| Pr(X < a) vs Pr(X ≤ a) | can be different (by Pr(X = a))   | always the same                             |
| Mean               | Σx·Pr(X = x)                          | ∫ x·f(x) dx                                 |

## Which method?
| The question...                                                    | Use                                                                 |
| ------------------------------------------------------------------ | ------------------------------------------------------------------- |
| asks whether something is a probability distribution               | check 0 ≤ Pr ≤ 1 and Σ = 1 (discrete), or f ≥ 0 and area = 1 (continuous) |
| has an unknown k in a table or rule                                | add all the probabilities and set the sum equal to 1               |
| has two unknowns and gives E(X)                                    | two equations: Σ = 1 and E(X) = the given value                    |
| asks for the mean, expected value or "on average"                  | [[4 - Expectation]]                                                 |
| asks how spread out or variable the values are                     | [[5 - Variance]]                                                    |
| asks whether a game is fair, or what it should cost                | [[6 - Fair Games]]: E(profit) = 0                                   |
| has n independent trials, success/failure, the same p every time   | [[7 - Binomial Distribution]]                                       |
| gives a function f(x) for a measured quantity                      | [[8 - Continuous Distributions]]: integrate                        |
| says "at least one"                                                | the complement: 1 − Pr(X = 0)                                       |

## Key words
| Words                                  | Symbol      | What to do (discrete)              |
| -------------------------------------- | ----------- | ---------------------------------- |
| "expected", "mean", "on average"       | E(X), μ     | Σx·Pr(X = x)                       |
| "spread", "variability"                | Var(X), σ   | E(X²) − [E(X)]²                    |
| "fair"                                 |             | E(profit) = 0                      |
| "exactly 3"                            | Pr(X = 3)   | binompdf (if binomial)             |
| "at most 3", "no more than 3"          | Pr(X ≤ 3)   | binomcdf (if binomial)             |
| "less than 3", "fewer than 3"          | Pr(X < 3)   | Pr(X ≤ 2)                          |
| "at least 3", "no fewer than 3"        | Pr(X ≥ 3)   | 1 − Pr(X ≤ 2)                      |
| "more than 3"                          | Pr(X > 3)   | 1 − Pr(X ≤ 3)                      |
| "given", "if"                          | \|          | divide by the probability of what you are given |

## Calculator keys
| Task                   | TI-84 Plus CE                                                                | Casio fx-580VNX                                 |
| ---------------------- | ---------------------------------------------------------------------------- | ----------------------------------------------- |
| Pr(X = x), binomial    | 2nd -> VARS (DISTR) -> A: binompdf(n, p, x)                                  | MENU -> Distribution -> Binomial PD -> Variable |
| Pr(X ≤ x), binomial    | 2nd -> VARS (DISTR) -> B: binomcdf(n, p, x)                                  | MENU -> Distribution → Binomial CD -> Variable  |
| ⁿCᵣ                    | MATH -> PROB -> 3: nCr                                                       | SHIFT ÷ (nCr)                                   |
| ∫ f(x) dx from a to b  | MATH -> 9: fnInt( (fill in the ∫ template)                                   | ∫ key                                           |
| Mean and SD of a table | x in L1, Pr in L2 -> STAT -> CALC -> 1-Var Stats (FreqList: L2) -> x̄ and σx | Statistics mode with Frequency on -> x̄ and σx  |
