## Dependent and independent variables

Bivariate data involves two variables, and to analyse the relationship
between them we first decide which is which:

- The **independent variable** is the one we believe might be driving or
  explaining the relationship (often something we set/control, or that
  occurs first). Plotted on the **horizontal (x)** axis.
- The **dependent variable** is the one being **measured**, whatever is
  responding to/depending on the other variable. Plotted on the
  **vertical (y)** axis.

**Example.** Aida wants to see which brand of fertiliser helps plants grow
fastest, so she adds a different brand to each plant and measures how tall
they grow.
- *Independent variable:* type of fertiliser (what she's changing)
- *Dependent variable:* plant height (what she's measuring)

Not every pair of variables is worth comparing this way: e.g. pairing
"a person's blood group" with "their favourite TV channel" doesn't make
sense as an independent/dependent relationship, because there's no reason
to think one could plausibly affect the other.

## Scatter diagrams (scatter plots)

A scatter plot shows each observation as a point $(x,y)$ -> independent
variable on the horizontal axis, dependent on the vertical. When
describing a scatter plot, comment on all four of:

1. **Direction** — positive (as $x$ increases, $y$ tends to increase) or
   negative (as $x$ increases, $y$ tends to decrease)
2. **Form** — linear (points cluster around a straight line) or non-linear
   (points follow a curve)
3. **Strength** — weak, moderate, or strong (how tightly the points hug
   the line/curve)
4. **Outliers** — any points that sit well away from the general pattern

![[Scatterplot - Age vs Distance Thrown.png]]

*Example read-off: this scatter plot of age vs. distance thrown shows a
positive, linear, strong relationship — as age increases, distance thrown
increases, and the points sit close to a straight line — with the point at
$(10,15)$ standing out as a possible outlier (much younger than the rest).*

## Pearson's correlation coefficient, $r$

$r$ gives a single number summarising the direction and strength of a
**linear** relationship:

$$r = \frac{\sum(x-\bar{x})(y-\bar{y})}{(n-1)\,s_x\,s_y}$$

- $-1 \le r \le 1$.
- **Sign** = direction: $r>0$ positive, $r<0$ negative.
- **Size of $|r|$** = strength, completely independent of the sign:

| $|r|$ | Strength |
|---|---|
| close to $1$ (e.g. $> 0.75$ or so) | strong |
| mid-range (roughly $0.25$–$0.75$) | moderate |
| close to $0$ (e.g. $< 0.25$ or so) | weak |

A value like $r=-0.16$ is a **weak negative** correlation — weak because
$|{-0.16}|$ is close to $0$, negative because of the sign. Don't let the
negative sign make a weak correlation sound "strong."

In practice you'll almost always compute $r$ using technology (graphics
calculator or software) rather than the formula by hand — enter the data
into two lists and run a linear-regression command, which reports $r$
alongside the regression equation (see [[8 - Least Squares Regression]]).

## Coefficient of determination, $r^2$

Simply $r$ squared — but interpreted differently: it's the **proportion of
variation** in the dependent variable that can be explained by the
variation in the independent variable, read as a percentage.

$$\text{``}r^2 \times 100\%\text{ of the variation in [dependent variable] can be explained by the variation in [independent variable].''}$$

## Worked Example — computing and interpreting $r$ and $r^2$

A researcher studies the relationship between hours of screen time per day
($x$) and a productivity score ($y$):

| $x$ (hours) | 1 | 3 | 4 | 7 | 10 | 12 | 14 | 15 |
|---|---|---|---|---|---|---|---|---|
| $y$ (score) | 11 | 9 | 10 | 6 | 8 | 4 | 3 | 1 |

Using technology:
$$y = -0.6343x + 11.7327 \qquad r = -0.9348 \qquad r^2 = 0.8739$$

**Interpreting $r$:** strong (close to $-1$) and negative — longer screen
time is associated with lower productivity.

**Interpreting $r^2$:** $87\%$ of the variation in productivity score can
be explained by variation in screen time (the remaining $13\%$ is down to
other factors not captured by this model).

![[Scatterplot with LSRL line - screen time vs productivity.png]]

(This equation's slope/intercept are interpreted fully in
[[8 - Least Squares Regression]].)

## Correlation is not causation

A strong $r$ only tells you the two variables move together — it never by
itself proves that one *causes* the other. Two classic ways a strong
correlation can mislead:

- **A third (confounding) variable drives both.** At a penguin colony,
  tourist ticket sales and the number of baby penguins born both rose over
  five years alongside a fox-removal program — but that doesn't mean
  selling more tickets *causes* penguins to be born; both are better
  explained by the fox-removal program (fewer predators $\to$ more chicks
  survive) running alongside unrelated tourism growth.
- **Reversed, coincidental, or spurious association.** E.g. noticing that
  companies with CEOs who wear wider ties tend to have higher profits
  doesn't mean wider ties *cause* higher profits — profitable companies may
  simply have a culture that happens to also favour certain fashion norms,
  with no causal link at all.

Before claiming causation, you'd need to rule out confounding variables,
reverse causation, and coincidence — correlation alone can't do that.

---
See [[Content/Statistics/1 - Overview]] for the full formula sheet and common mistakes for this
study area.
