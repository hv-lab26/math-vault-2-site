Once a scatter plot shows a roughly linear relationship, we can fit a
straight line to the data — a **line of best fit** — and use its equation
to interpret and predict (see [[9 - Prediction - Interpolation and Extrapolation]]).

## Fitting a line "by eye"

A quick, rough method: draw a straight line through the scatter so that
there's roughly an equal number of points above and below it. This is
useful for a fast estimate, but it's subjective — two people could draw
slightly different lines. For anything that needs to be accurate (or
needs a precise equation), use **least-squares regression** instead.

## The least-squares regression line

The least-squares method finds the one line that minimises the sum of the
squared vertical distances from every point to the line (these vertical
distances are exactly the **residuals** — see [[10 - Residual Analysis]]). It's
used whenever the data shows a linear relationship with no major outliers.

General form (matching Vy's course formula sheet):
$$y = ax + b$$

$$a = r\,\frac{s_y}{s_x} \qquad\qquad b = \bar{y} - a\bar{x}$$

where $a$ is the **slope/gradient** and $b$ is the **$y$-intercept**. You
only need this "by hand, from summary statistics" version when you're
given $\bar x, \bar y, s_x, s_y, r$ directly rather than the raw data — if
you have the raw $(x,y)$ pairs, it's faster (and expected) to find the
equation straight from technology (enter both lists, run linear
regression).

> [!tip] Watch the letters
> Different resources label the same two numbers differently — $y=ax+b$,
> $y=mx+c$, $y=a+bx$ all show up. **Don't memorise a letter — memorise a
> role:** whichever number multiplies $x$ is the slope, whichever stands
> alone is the $y$-intercept, no matter what it's called.

## Interpreting the slope and intercept

Once you have the equation, both numbers in it carry meaning:

- **Slope:** *"For every 1 [unit of the independent variable] increase, the
  [dependent variable] [increases/decreases — match the sign] by [slope]
  [unit of dependent variable]."* Always independent → dependent, never
  the other way around.
- **$y$-intercept:** the predicted value of the dependent variable when
  the independent variable is $0$. Sometimes this is meaningful; sometimes
  it isn't (see the coffee-shop example below) — it's still worth checking
  whether $x=0$ is a sensible, real-world situation for the context.

---

## Worked Example 1 — building the LSRL from summary statistics

A study into the relationship between the height of parents and the
height of their adult children found: mean parent height $\bar{x}=180$ cm,
mean child height $\bar{y}=169$ cm, $s_x = 5.3$, $s_y = 4.8$, $r=0.85$.

**(a) Which is the dependent variable?** The height of the *children* — the
study is using parent height to explain/predict child height.

**(b) Slope:**
$$a = r\frac{s_y}{s_x} = 0.85 \times \frac{4.8}{5.3} \approx 0.77$$

**(c) Intercept:**
$$b = \bar{y} - a\bar{x} = 169 - 0.77(180) \approx 30.43$$

So the regression line is $y = 0.77x + 30.43$ (child's height $=0.77\times$
parent's height $+30.43$).

**(d) Predicting:** for a parent who is $195$ cm tall,
$$y = 0.77(195) + 30.43 \approx 181 \text{ cm}$$

---

## Worked Example 2 — predicting in both directions, and checking whether the intercept makes sense

A coffee shop recorded its number of customers ($x$) against cups of
coffee sold ($y$) over several days: $\bar{x}=10$, $\bar{y}=24$, $s_x=2.5$,
$s_y=6$, $r=0.62$.

**Slope and intercept:**
$$a = r\frac{s_y}{s_x} = 0.62\times\frac{6}{2.5} = 1.488 \qquad b = \bar{y}-a\bar{x} = 24 - 1.488(10) = 9.12$$
$$y = 1.488x + 9.12$$

**Interpreting the slope:** for every additional customer, the number of
cups sold increases by about $1.488$.

**Predicting $y$ from $x$:** with $17$ customers,
$$y = 1.488(17) + 9.12 \approx 34.4 \text{ cups}$$

**Predicting $x$ from $y$** (rearrange and solve): how many customers are
needed to sell $50$ cups?
$$50 = 1.488x + 9.12 \implies x = \frac{50-9.12}{1.488} \approx 27.5 \implies 28 \text{ customers}$$

**Does the intercept make sense?** At $x=0$ (no customers), the model
predicts $y=9.12$ cups sold — but with zero customers, the real number of
cups sold must be $0$, not $9.12$. This is a reminder that a regression
line is a model fitted to the range of the data you actually have — it
doesn't have to make literal sense far outside that range (see
[[9 - Prediction - Interpolation and Extrapolation]] for exactly this issue).

---
See [[Content/Statistics/1 - Overview]] for the full formula sheet and common mistakes for this
study area.
