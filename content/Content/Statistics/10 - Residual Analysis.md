Fitting a regression line is sometimes not enough, by itself, to confirm
that data really is linear. **Residual analysis** checks this by looking
at how far each point sits from the fitted line.

## What a residual is

$$\text{Residual} = y_{\text{actual}} - y_{\text{predicted}}$$

— the vertical difference between an actual data point and the value the
regression line predicts for that same $x$. A **positive** residual means
the actual point sits *above* the line (the line underestimated it); a
**negative** residual means it sits *below* (the line overestimated it).

> [!tip]
> Always calculate the regression line *first* — residuals are measured
> against that specific line, so you need its equation before you can find
> any of them.

### Worked Example — calculating residuals

Using the age/distance-thrown regression line $y = 3.29x - 20.3$ from
[[9 - Prediction - Interpolation and Extrapolation]]:

**For the point $(12, 20)$:**
$$y_{\text{predicted}} = 3.29(12) - 20.3 = 19.18$$
$$\text{Residual} = 20 - 19.18 = 0.82$$

**For the point $(10, 15)$:**
$$y_{\text{predicted}} = 3.29(10) - 20.3 = 12.6$$
$$\text{Residual} = 15 - 12.6 = 2.4$$

On a graphics calculator: once the regression is done, enter the actual
$y$-values in one list, generate predicted values in another (by typing the
regression equation referencing the $x$-list), then subtract the two lists
into a third list — that third list is your set of residuals.

## Residual plots

A **residual plot** graphs each $x$-value against its residual (with a
horizontal reference line at residual $=0$). Its *shape* tells you whether
a straight line was really the right model:

| Residual plot shape | What it means |
|---|---|
| Points **randomly scattered** above and below $0$, no pattern | The original data probably **is linear** — a straight line is a good model |
| Points follow a **curved** pattern (e.g. a bowl/U-shape, or a hump) | The original data is probably **non-linear** — a straight line is *not* the best model, even if $r$ looked reasonably high |

![[Residual Plot - random scatter vs curved pattern.png]]

This is a genuinely useful check, because **a high $r$ alone doesn't
guarantee the relationship is linear** — $r$ measures how well a straight
line fits, but a strong curve can still produce a fairly high $r$ if it's
"close enough" to straight over the range you have. The residual plot is
often what exposes the curve that a quick glance at $r$ misses.

### Worked Example — a residual plot exposing non-linearity

A biology study records an animal's body mass ($y$) against its age ($x$).
A scatter plot already looks like a smooth growth curve (small, close-
together values at low ages, increasingly steep at higher ages) rather
than a straight line, even though fitting a straight line gives a
reasonably strong correlation, $r = 0.98$:
$$y = 16.5x - 18.5$$

Checking one point: at $x=5$ (age $5$), the actual body mass was $54$ kg.
$$y_{\text{predicted}} = 16.5(5) - 18.5 = 64 \text{ kg} \qquad \text{Residual} = 54 - 64 = -10 \text{ kg}$$

Plotting *every* point's residual against age reveals a clear curved
(bowl-shaped) pattern — confirming what the scatter plot already hinted
at: the true relationship is **non-linear**, so the straight line
$y=16.5x-18.5$, despite its high $r$, isn't actually the best model here.
The next step is to **linearise** the data — see [[11 - Linearising Data]],
which continues this exact example.

---
See [[Content/Statistics/1 - Overview]] for the full formula sheet and common mistakes for this
study area.
