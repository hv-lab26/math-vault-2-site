Up: [[Content/Statistics/1 - Overview]]

## Practice Questions

A spread of questions across every topic in this study area, at roughly
coursework difficulty, each with a full worked solution.

---

**PQ1 (Types of Data).** For each variable below, state whether it is
categorical or numerical — and if numerical, whether it's discrete or
continuous: (a) a runner's finishing time, (b) shirt size (S/M/L/XL),
(c) number of pets owned, (d) blood type.

> [!success]- Solution
> (a) Numerical, continuous (time can take any value in a range).
> (b) Categorical (sizes are labels/groups, not quantities — you can't
> average "M" and "L").
> (c) Numerical, discrete (whole-number counts only — you can't own 2.5
> pets).
> (d) Categorical.
>
---

**PQ2 (Measures of Centre and Spread).** A book club's 7 members each
report how many pages they read last week:
$$120,\ 95,\ 140,\ 110,\ 95,\ 200,\ 130$$
Find the mean, median, mode, range, IQR, and sample standard deviation.

> [!success]- Solution
> Sorted: $95,95,110,120,130,140,200$.
> - Mean: $\bar{x} = \dfrac{890}{7} \approx 127.14$
> - Median ($n=7$, odd): 4th value $=120$
> - Mode: $95$ (appears twice)
> - Range: $200-95=105$
> - IQR: lower half $\{95,95,110\}\Rightarrow Q_1=95$; upper half
>   $\{130,140,200\}\Rightarrow Q_3=140$. $IQR = 140-95=45$
> - Sample SD: $s_x \approx 36.27$
>
> Note how much the mean ($127.14$) is pulled up by the one high value
> ($200$) compared to the median ($120$) — a hint of positive skew, even in
> a data set this small.
>
---

**PQ3 (Boxplots and Outliers).** A data set has five-number summary
$\text{min}=20$, $Q_1=30$, median $=50$, $Q_3=60$, $\text{max}=80$.
(a) Find the IQR and the outlier boundaries. (b) Is either the minimum or
maximum an outlier? (c) What percentage of the data lies between $30$ and
$60$?

> [!success]- Solution
> (a) $IQR = 60-30=30$. Lower boundary $=30-1.5(30)=-15$. Upper boundary
> $=60+1.5(30)=105$.
> (b) Neither $20$ nor $80$ falls outside $[-15,105]$, so **neither is an
> outlier**.
> (c) $30$ is $Q_1$ and $60$ is $Q_3$, so the interval $[Q_1,Q_3]$ always
> contains the **middle 50%** of the data.
>
---

**PQ4 (Stem-and-Leaf, Histograms, Skewness).** Midday temperatures (°C)
over a 14-day stretch:
$$18,21,19,23,20,17,22,24,19,21,20,18,25,20$$
(a) Draw an ordered stem-and-leaf plot. (b) Describe the shape of the
distribution.

> [!success]- Solution
> Sorted: $17,18,18,19,19,20,20,20,21,21,22,23,24,25$.
> $$
> \begin{array}{c|c}
> \textbf{Stem} & \textbf{Leaf} \\
> \hline
> 1 & 7\ 8\ 8\ 9\ 9 \\
> 2 & 0\ 0\ 0\ 1\ 1\ 2\ 3\ 4\ 5 \\
> \end{array}
> $$
> *Key: $1|7$ means $17$.*
>
> (b) Mean $=20.5$, median $=20$ — very close together, and the leaves taper
> off gently on both sides of the $19$–$21$ cluster with no extreme stretch
> either way $\Rightarrow$ roughly **symmetrical**.
>
---

**PQ5 (Comparing Distributions).** Two classes sit the same 5-question
quiz (out of 20):
$$\text{Class X: } 14, 18, 12, 16, 19 \qquad\qquad \text{Class Y: } 11, 13, 10, 15, 12$$
Compare the centre and spread of the two classes.

> [!success]- Solution
> Class X: mean $=15.8$, median $=16$, $s_x\approx 2.86$.
> Class Y: mean $=12.2$, median $=12$, $s_x\approx 1.92$. Class X scored
> noticeably higher on average (by about $3.6$ marks) and was also slightly
> more spread out (SD $2.86$ vs. $1.92$) than Class Y.
>
---

**PQ6 (Correlation vs. Causation).** A researcher finds that companies
with CEOs who wear wider neckties tend to have higher profits, and
suggests companies should encourage wider ties to increase profits. Why is
this suggestion questionable?

> [!success]- Solution
> This confuses correlation with causation. A plausible
> alternative explanation: more established/profitable companies may simply
> have workplace cultures (and budgets) that happen to favour more formal,
> expensive clothing — profit isn't *caused* by tie width, both could instead
> be linked to company size, industry norms, or management culture (a
> confounding variable), or the association could simply be coincidental.
>
---

**PQ7 (Least Squares Regression).** Data for a mass hung on a spring:

| Mass $x$ (g) | 0 | 50 | 100 | 150 | 200 | 250 |
|---|---|---|---|---|---|---|
| Length $y$ (cm) | 17.7 | 20.4 | 22.0 | 25.0 | 26.0 | 27.8 |

Find the least-squares regression line and interpret its slope and
intercept.

> [!success]- Solution
> Using technology: $r = 0.992$,
> $$y = 0.04x + 18.13$$
> **Slope:** for every $1$ gram increase in mass, the spring's length
> increases by about $0.04$ cm.
> **Intercept:** when there's no mass on the spring ($x=0$), its length is
> about $18.13$ cm — this is the spring's natural (unstretched) length, so
> it makes good physical sense here.
>
---

**PQ8 (Residuals, and a hint of Linearising).** Jin decorates cupcakes
individually; the table shows the total time taken as the batch size
grows:

| Cupcakes $x$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|---|
| Time $y$ (min) | 5 | 6 | 8 | 15 | 24 | 30 | 47 | 77 | 98 | 150 |

(a) Find the LSRL. (b) Find the residual at $x=1$ and at $x=10$.
(c) What do the residuals, overall, suggest about this data?

> [!success]- Solution
> (a) $y = 14.52x - 33.87$ ($r=0.912$)
> (b) At $x=1$: predicted $=14.52(1)-33.87=-19.35$, residual
> $=5-(-19.35)=24.35$ (way too low a prediction — even negative, which
> can't be a real time!). At $x=10$: predicted $=111.35$, residual
> $=150-111.35=38.65$.
> (c) The residuals start large and positive, dip negative in the middle,
> then swing sharply positive again at the end — a clear systematic
> (non-random) pattern, not random scatter. This means a **straight line
> isn't the right model**: the data is growing faster than linearly. (In
> fact, transforming to $\log_{10}(y)$ gives $r=0.996$ — a much better fit;
> see [[11 - Linearising Data]] for the method.)
>
---

## Review Questions

Ten more advanced questions — harder and more multi-part than the practice
questions above, often combining several ideas from across this study
area. Work through them before checking the solution.

---

### RQ1 — Effect of linear transformations

Eight gym members' resting heart rates (bpm):
$$62, 58, 71, 65, 70, 84, 58, 77$$

(a) Find the mean and sample standard deviation.
(b) After a 10-minute warm-up, every member's heart rate rises by exactly
$12$ bpm. State the new mean and SD **without recalculating from the raw
data** — explain your reasoning.
(c) The same readings instead need converting from "beats per minute" to
"beats per 10 seconds" (divide every value by $6$). State the new mean and
SD.

> [!success]- Solution
> (a) $\bar{x} = 68.13$ bpm, $s_x = 9.22$ bpm.
> (b) Adding the same constant ($12$) to every value shifts the **mean** by
> that constant, but leaves the **spread** (SD) completely unchanged — every
> value moved by the same amount, so the distances between values (and from
> the new mean) are identical to before. New mean $=68.13+12=80.13$ bpm, SD
> $=9.22$ bpm (unchanged).
> (c) Scaling every value by a constant ($\times\frac16$) scales **both**
> the mean and the SD by that same factor. New mean $=68.13/6\approx11.35$,
> new SD $=9.22/6\approx1.54$.
>
---

### RQ2 — Outliers and when the mean misleads

A café's daily pastry sales (units) over 11 days:
$$34,36,31,29,40,33,35,32,38,30,65$$

(a) Find the five-number summary and test for outliers.
(b) A 12th day is added: $37$ units. Recompute the five-number summary —
how much did it change?
(c) Explain why the **mean** would be a misleading way to describe a
"typical" day's sales here, and which measure of centre would be better.

> [!success]- Solution
> (a) Sorted: $29,30,31,32,33,34,35,36,38,40,65$. Median (6th value) $=34$.
> $Q_1=31$, $Q_3=38$, $IQR=7$. Boundaries: $31-10.5=20.5$ and
> $38+10.5=48.5$. Since $65>48.5$, **$65$ is an outlier**.
> (b) New sorted list: $29,30,31,32,33,34,35,36,37,38,40,65$. Five-number
> summary barely shifts: $Q_1$ from $31\to31.5$, median $34\to34.5$, $Q_3$
> from $38\to37.5$ — all tiny changes, and $65$ is still flagged as an
> outlier under the new boundaries. **One more typical day barely moved
> anything.**
> (c) The mean is $36.6$ (11 days) — pulled upward by the single unusually
> high day ($65$). The **median** ($34$) better represents what a "typical"
> day actually looks like, since (unlike the mean) it isn't dragged around
> by one extreme value.
>
---

### RQ3 — Reasoning about shape from summary statistics alone

Without seeing any raw data: Exam A has mean $58$ and median $72$. Exam B
has mean $75$ and median $74$. What shape of distribution does each
suggest, and why?

> [!success]- Solution
> **Exam A:** the mean ($58$) is noticeably *lower* than the
> median ($72$) — this happens when some unusually **low** scores drag the
> mean down below the middle of the data, which is the signature of a
> **negatively skewed** distribution (long tail on the low/left side — e.g.
> most students did well, but a handful did very poorly).
> **Exam B:** mean ($75$) and median ($74$) are almost identical, suggesting
> a roughly **symmetrical** distribution (perhaps very slightly positively
> skewed, given the mean is marginally higher, but close enough to call
> symmetric without more information).
>
---

### RQ4 — Back-to-back stem-and-leaf, two groups

Two sports teams' player ages:
$$\text{Team A: } 19,22,23,25,21,24,26,20,23,27$$
$$\text{Team B: } 31,28,33,35,29,34,30,32,36,27$$

(a) Draw a back-to-back stem-and-leaf plot. (b) Compare the centre and
spread of the two teams.

> [!success]- Solution
> Team A sorted: $19,20,21,22,23,23,24,25,26,27$. Team B
> sorted: $27,28,29,30,31,32,33,34,35,36$.
>
> $$
> \begin{array}{c|c|c}
> \textbf{Team A} & \textbf{Stem} & \textbf{Team B} \\
> \hline
> 9 & 1 & \\
> 7\ 6\ 5\ 4\ 3\ 3\ 2\ 1\ 0 & 2 & 7\ 8\ 9 \\
> & 3 & 0\ 1\ 2\ 3\ 4\ 5\ 6 \\
> \end{array}
> $$
>
> *Key: Team A, $2|7$ means $27$. Team B, $3|1$ means $31$.*
>
> (b) Team A: mean $=23$, median $=23$, $SD\approx2.58$. Team B: mean
> $=31.5$, median $=31.5$, $SD\approx3.03$. Team B players are, on average,
> about $8.5$ years older, and also slightly more spread out in age than
> Team A — the two groups don't overlap at all (Team A's oldest player, 27,
> is younger than every single Team B player).
>
---

### RQ5 — Correlation, causation, and a confound

Across 12 months, a town's monthly ice-cream sales and the number of
recorded shark attacks nearby were both logged, giving a correlation of
$r = 0.99$ between them.

(a) Is it reasonable to conclude that buying ice cream causes shark
attacks (or vice versa)? If not, suggest a more plausible explanation.
(b) A news article says: "Since $r=0.99$ is so strong, the relationship
must be causal." Explain what's wrong with this reasoning in general (not
just for this example).

> [!success]- Solution
> (a) No — this is a classic confounding-variable case. Both ice-cream sales
> and the number of people swimming (and therefore at risk of a shark
> encounter) rise together in **warmer months**. Temperature/season is
> driving both variables; neither causes the other directly.
> (b) The size of $r$ only measures how strong a *linear association* is —
> it says nothing about *why* that association exists. No value of $r$, no
> matter how close to $1$, can by itself rule out a confounding variable,
> reverse causation, or coincidence. Establishing causation needs more than
> correlation (e.g. a controlled experiment, or ruling out plausible
> confounders).
>
---

### RQ6 — LSRL, interpretation, and judging two predictions

A delivery company records, across 9 trips, the number of parcels loaded
onto a van ($x$) and the van's fuel consumption ($y$, L/100km):

| Parcels $x$ | 20 | 35 | 50 | 65 | 80 | 95 | 110 | 125 | 140 |
|---|---|---|---|---|---|---|---|---|---|
| Fuel $y$ (L/100km) | 7.8 | 8.5 | 9.1 | 9.9 | 10.6 | 11.0 | 11.9 | 12.4 | 13.0 |

(a) Find the LSRL and interpret the slope and intercept.
(b) Predict fuel consumption for $100$ parcels and for $200$ parcels,
commenting on the reliability of each.

> [!success]- Solution
> (a) $r = 0.999$, $$y = 0.0436x + 6.982$$
> **Slope:** for every extra parcel loaded, fuel consumption rises by about
> $0.0436$ L/100km. **Intercept:** an empty van ($x=0$) is predicted to use
> about $6.98$ L/100km — this is plausible (a van still burns fuel just
> driving around empty).
> (b) At $x=100$ (inside the data's range, $20$–$140$): $y\approx
> 11.34$ L/100km — **interpolation, reliable**. At $x=200$ (well outside the
> range): $y\approx15.70$ L/100km — **extrapolation, not reliable** (a van
> loaded with $200$ parcels may not even behave the same way mechanically,
> let alone follow the same linear fuel trend).
>
---

### RQ7 — LSRL from summary statistics, with a reverse prediction

A study of $x=$ weekly study hours against $y=$ exam score (out of 100)
found $\bar{x}=12$, $\bar{y}=68$, $s_x=4.5$, $s_y=9.2$, $r=0.73$, with
recorded study hours ranging from $5$ to $20$ hours per week.

(a) Find the LSRL. (b) Predict the score for someone studying $15$ hours a
week. (c) A student wants to know how many hours they'd need to study to
score $85$ — find this, and comment on its reliability.

> [!success]- Solution
> (a) $$a = r\frac{s_y}{s_x} = 0.73\times\frac{9.2}{4.5} \approx 1.49 \qquad b = \bar{y}-a\bar{x} = 68-1.49(12)\approx 50.09$$
> $$y = 1.49x + 50.09$$
> (b) $y = 1.49(15)+50.09 \approx 72.5$. Since $15$ is within $[5,20]$, this
> is **interpolation — reliable** (especially with $r=0.73$ showing a
> reasonably strong relationship).
> (c) Solve for $x$: $85 = 1.49x+50.09 \implies x \approx 23.4$ hours. Since
> $23.4$ is outside $[5,20]$, this is **extrapolation — not reliable**: the
> model was never tested on students studying that much, so there's no
> evidence the same trend continues that far.
>
---

### RQ8 — Computing and judging residuals

A plant's height ($y$, cm) was measured at the same time each week:

| Week $x$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|---|---|---|---|---|---|---|---|---|
| Height $y$ | 4 | 9 | 15 | 24 | 34 | 43 | 50 | 55 |

The least-squares regression line is $y = 7.81x - 5.89$ ($r=0.996$).

(a) Calculate the residual at week $3$ and at week $6$.
(b) The full set of residuals, in order, is approximately: $2.08, -0.73,
-2.54, -1.35, 0.85, 2.04, 1.23, -1.58$. Based on this, is a straight line
an adequate model here? Explain.

> [!success]- Solution
> (a) Week 3: predicted $=7.81(3)-5.89=17.54$, residual $=15-17.54=-2.54$.
> Week 6: predicted $\approx 40.96$, residual $=43-40.96=2.04$.
> (b) The residuals are fairly small relative to the heights themselves
> (mostly under $3$ cm, against heights up to $55$ cm) and don't show one
> single consistent curve (they go positive, negative, negative, negative,
> positive, positive, positive, negative — not a clean U-shape or hump).
> Combined with the already very high $r=0.996$, this suggests the **linear
> model is adequate** here — unlike Review Question 9 below, there isn't
> strong evidence a transformation is needed.
>
---

### RQ9 — Linearising a diminishing-returns relationship

A company tracks weekly advertising spend ($x$, in hundreds of dollars)
against new customer sign-ups ($y$):

| Spend $x$ | 2 | 4 | 6 | 8 | 10 | 12 | 14 | 16 |
|---|---|---|---|---|---|---|---|---|
| Sign-ups $y$ | 15 | 28 | 36 | 42 | 46 | 49 | 51 | 52 |

(a) Find the LSRL on the raw data, and comment on its residuals'
pattern: $-7.5, 0.5, 3.6, 4.6, 3.6, 1.7, -1.3, -5.3$.
(b) The scatter plot shows sign-ups rising quickly at first, then
levelling off — suggest and apply an appropriate transformation.
(c) Use the better model to predict sign-ups for $\$1800$ of spend
($x=18$), and comment on reliability.

> [!success]- Solution
> (a) $y = 2.48x+17.54$ ($r=0.940$). The residuals rise, peak in the
> middle, then fall back down and go negative — a hump shape, not random
> scatter — meaning the straight line over- and under-predicts in a
> systematic way: **not actually the best model**, despite a fairly high
> $r$.
> (b) A curve that rises quickly then flattens off (diminishing returns) is
> a good match for a $\log(x)$ transform:
> $$y = 42.24\log_{10}(x) + 2.85 \qquad (r = 0.998,\text{ up from } 0.940)$$
> A large jump in $r$ confirms this transformation fits much better.
> (c) $x=18$ is outside the original spend range ($2$–$16$), so this is
> **extrapolation**: $y = 42.24\log_{10}(18)+2.85 \approx 55.9$ sign-ups —
> but since advertising returns are already levelling off within the data
> we have, and we have no evidence of what happens beyond $\$1600$ spend
> (does it keep flattening, or drop off entirely?), this prediction should
> be treated cautiously despite the model's excellent fit to known data.
>
---

### RQ10 — Hybrid question: a full analysis from scratch

A weather station logs the midday temperature ($x$, °C) and a nearby
ice-cream van's daily revenue ($y$, \$) on 10 summer days:

| Temp $x$ | 22 | 24 | 26 | 28 | 30 | 32 | 34 | 25 | 29 | 31 |
|---|---|---|---|---|---|---|---|---|---|---|
| Revenue $y$ | 180 | 210 | 250 | 300 | 340 | 390 | 430 | 230 | 320 | 370 |

(a) Is temperature categorical or numerical? Which variable here is
independent, and which is dependent?
(b) Find $r$ and the least-squares regression line.
(c) Interpret the slope in context.
(d) Predict revenue at $27\,°C$ and at $40\,°C$, commenting on reliability
for each.
(e) Find the residual for the day with temperature $30\,°C$ (actual
revenue $\$340$), and briefly comment on what it means.

> [!success]- Solution
> (a) Temperature is numerical (continuous). Independent variable:
> temperature (it's driving the pattern); dependent variable: revenue (what
> we're trying to explain/predict).
> (b) $$r = 0.998 \qquad y = 21.68x - 307.23$$
> (c) For every $1\,°C$ rise in temperature, the van's daily revenue
> increases by about $\$21.68$.
> (d) At $27\,°C$ (inside the data's range, $22$–$34$): $y \approx \$278$ —
> **interpolation, reliable** (and $r$ is extremely strong). At $40\,°C$
> (well outside the range): $y\approx\$560$ — **extrapolation, not
> reliable**: there's no guarantee revenue keeps climbing at the same rate
> once it gets that hot (people may stay indoors instead, or the van may run
> out of stock).
> (e) Predicted at $30\,°C$: $y = 21.68(30)-307.23 \approx \$343.2$.
> Residual $= 340 - 343.2 = -\$3.2$ — tiny compared to the scale of daily
> revenue, confirming the linear model fits this particular day very
> closely.
>
---
See [[Content/Statistics/1 - Overview]] for the full formula sheet and common mistakes for this
study area.
