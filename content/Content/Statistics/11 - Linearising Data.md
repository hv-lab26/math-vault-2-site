Sometimes a scatter plot (or a curved residual plot — see [[10 - Residual Analysis]]) shows that the true relationship between $x$ and $y$ isn't
actually linear, even if a straight line gives a reasonably high $r$. To
get a better model — and more trustworthy predictions — we can
**transform** one of the variables to "straighten out" the curve. This is
called **linearising** the data.

## Choosing a transformation

Look at the shape of the curve in the scatter plot, and try the matching
transformation on $x$ and/or $y$:

| Scatter plot looks like... | Try transforming to... | New model form |
|---|---|---|
| A parabola-like curve, accelerating | $x^2$ | $y = a x^2 + b$ |
| A curve that rises quickly then levels off | $\sqrt{x}$ | $y = a\sqrt{x} + b$ |
| A curve that drops quickly then levels off/flattens | $\dfrac{1}{x}$ (or $\dfrac1y$) | $y = \dfrac{a}{x}+b$ |
| Exponential-looking growth/decay | $\log(y)$ | $\log y = kx + d \;\Rightarrow\; y = A\times 10^{kx}$ (with $A = 10^d$) |
| Growth that slows as $x$ increases | $\log(x)$ | $y = a\log(x) + b$ |

**Process on a graphics calculator:** keep the original data in one list
(e.g. $L_1, L_2$), create a new list applying the transformation (e.g.
$L_3 = L_1^2$, or $L_3 = \log(L_1)$), then run linear regression using the
transformed list in place of the original. Compare the new $r$ to the
original $r$ — **only keep the transformation if $|r|$ moved closer to
$1$.** If it didn't help, try a different transformation from the table.

---

## Worked Example 1 — squaring $x$ (continuing from [[10 - Residual Analysis]])

An animal's body mass ($y$, kg) was modelled against its age ($x$, years).
The straight-line fit looked fairly strong ($r=0.979$) but its residual
plot showed a clear curved (bowl-shaped) pattern — a sign the real
relationship isn't linear:
$$y = 16.5x - 18.5 \qquad (r = 0.979,\ r^2 \approx 0.958)$$

Squaring the age values and re-running the regression:
$$y = 1.64x^2 + 11.98 \qquad (r = 0.999,\ r^2 \approx 0.998)$$

$r$ moved from $0.979$ to $0.999$ — much closer to $1$ — so the squared
model is the better fit.

**Using the new model to predict:** at $x=6.5$ years,
$$y = 1.64(6.5)^2 + 11.98 \approx 81.27 \text{ kg}$$
($6.5$ falls inside the original data's age range, so this is
interpolation — see [[9 - Prediction - Interpolation and Extrapolation]].)

---

## Worked Example 2 — reciprocal transformation, and choosing between two models

The price of iron ore ($P$, cents/tonne) was recorded for 9 years
($T$ = years after 2000, $T=0$ to $8$):

| $T$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|---|---|---|---|---|---|---|---|---|---|
| $P$ | 25 | 30 | 27 | 33 | 38 | 62 | 75 | 80 | 144 |

**Original (linear) model:**
$$P = 12.52T + 7.04 \qquad r = 0.88,\ r^2 = 0.78$$
A residual plot for this model shows a clear curved pattern — the
relationship is non-linear, even though $r=0.88$ looks fairly strong.

**Transforming:** since price rises slowly at first then shoots up
steeply, try a reciprocal transform, $\frac1P$, against $T$:
$$\frac{1}{P} = -0.004T + 0.041 \qquad r = -0.973,\ r^2 \approx 0.95$$
(The negative sign makes sense: as $T$ increases, $P$ grows, so $1/P$
*shrinks*.) This residual plot shows no obvious pattern — a much better
fit.

![[Linearisation - iron ore price before and after transform.png]]

*Left: the original data curves away from its fitted line (notice the
$T=8$ point sitting well above it). Right: after the $1/P$ transform, the
points sit much closer to the fitted line.*

**Deciding which equation to use for prediction:** compare $r^2$ for each
model — $0.78$ (original) vs. $0.95$ (transformed). Since the transformed
model explains far more of the variation, **use the transformed equation**
(solve it for $P$ by taking the reciprocal of the predicted $\frac1P$
value) to make predictions, not the original linear one.

---
See [[Content/Statistics/1 - Overview]] for the full formula sheet and common mistakes for this
study area.
