Once you have a least-squares regression line (see [[8 - Least Squares Regression]]), you can substitute values into it to **predict**. But how
much you should trust that prediction depends on *where* the value you're
substituting sits, relative to the original data.

## Definitions

- **Interpolation** — estimating a value **inside** the range of the
  original data. Generally **reliable**, especially when $r$ shows a
  strong linear association.
- **Extrapolation** — estimating a value **outside** the range of the
  original data (smaller than the smallest recorded value, or larger than
  the largest). Generally **not reliable** — and becomes less and less
  reliable the further outside the data's range you go, since there's no
  evidence the same linear pattern continues out there.

The closer the data is to being perfectly linear, the more accurate
predictions will be — but that only applies *within* the range you
actually have data for.

**To check which one you're doing:** look at whichever value you were
*given* (the one you're substituting in), and compare it against the range
of that same variable in the original data. If it falls inside that
range $\to$ interpolation. If it falls outside $\to$ extrapolation. This
works whether you're predicting $y$ from a given $x$, or (by rearranging
the equation) predicting $x$ from a given $y$.

---

## Worked Example 1 — predicting both ways from the same line

Twelve athletes' ages and discus-throw distances give the regression line:
$$\text{Distance thrown (m)} = 3.29 \times \text{Age (years)} - 20.3$$
The original data covers ages from $10$ to $20$, and distances from $15$ m
to $50$ m.

**1. Predict the distance thrown by an 11-year-old.**
$$y = 3.29(11) - 20.3 = 15.9 \text{ m}$$
$11$ is within the data's age range $[10,20]$ $\Rightarrow$ **interpolation
— reliable.**

**2. Predict the distance thrown by a 45-year-old.**
$$y = 3.29(45) - 20.3 = 127.8 \text{ m}$$
$45$ is far outside $[10,20]$ $\Rightarrow$ **extrapolation — not
reliable** (and $127.8$ m is an unrealistic discus distance, which is a
good sign something's wrong with extrapolating this far!).

**3. Someone throws $60$ m — estimate their age.** Rearrange and solve for
$x$:
$$60 = 3.29x - 20.3 \implies x = \frac{80.3}{3.29} \approx 24 \text{ years}$$
Here we were *given* a distance ($60$ m), so we check it against the
distance range $[15,50]$: $60$ m is outside that range $\Rightarrow$
**extrapolation — not reliable.**

---

## Worked Example 2 — interpolation and extrapolation together

The table below shows how far a group of students live from their college,
and how long their daily commute takes:

| Distance $x$ (km) | 7.2 | 4.5 | 13 | 1.3 | 9.9 | 12.2 | 19.6 | 6.1 | 23.1 |
|---|---|---|---|---|---|---|---|---|---|
| Time $y$ (min) | 17 | 13 | 29 | 2 | 25 | 27 | 41 | 15 | 53 |

Using technology: $r=0.99$, and the least-squares regression line is
$$y = 2.16x + 1.42$$

The data's distance range is $[1.3,\ 23.1]$ km.

**Kim lives $15$ km away.**
$$y = 2.16(15)+1.42 \approx 33.8 \text{ min}$$
$15$ is inside $[1.3, 23.1]$ $\Rightarrow$ **interpolation — reliable**
(especially given how strong $r=0.99$ is).

**Sulaaf lives $32$ km away.**
$$y = 2.16(32)+1.42 \approx 70.5 \text{ min}$$
$32$ is outside $[1.3,23.1]$ $\Rightarrow$ **extrapolation — not
reliable**, even though $r$ is very strong — a strong $r$ only describes
how well the line fits the data you *have*, it says nothing about whether
the same relationship continues beyond it.

---
See [[Content/Statistics/1 - Overview]] for the full formula sheet and common mistakes for this
study area.
