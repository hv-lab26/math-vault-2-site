When you have two (or more) data sets measuring the same kind of thing,
you can compare them side by side. Two standard tools for this: **back-
to-back stem plots** and **parallel boxplots**. Either way, always compare
both:
- **Centre** — mean and/or median (which group tends to have bigger/smaller
  values?)
- **Spread** — IQR and/or standard deviation (which group is more varied?)

## Back-to-back stem plots

A stem plot can be drawn for two groups sharing the same stems, with one
group's leaves running outward to the left of the stem and the other
group's leaves running outward to the right. This lets you compare the
shapes of both distributions at a glance.

**Worked Example.** Students were given 50 minutes to work on a group task
in class. The teacher recorded how many minutes students in two different
class blocks actually spent on the task:

$$\text{Block 1: } 12, 37, 36, 36, 25, 49, 37, 49, 49, 36$$
$$\text{Block 4: } 24, 13, 24, 12, 24, 25, 13, 13, 36, 25$$

$$
\begin{array}{c|c|c}
\textbf{Block 1} & \textbf{Stem} & \textbf{Block 4} \\
\hline
2 & 1 & 2\ 3\ 3\ 3 \\
5 & 2 & 4\ 4\ 4\ 5\ 5 \\
7\ 7\ 6\ 6\ 6 & 3 & 6 \\
9\ 9\ 9 & 4 & \\
\end{array}
$$

*Key: for Block 1 (read outward from the stem), $3|7$ means $37$. For
Block 4, $1|3$ means $13$.*

**Comparing:** Block 1's mean is $36.6$ minutes (median $36.5$) vs. Block
4's mean of $20.9$ minutes (median $24$) — Block 1 students spent
noticeably **more** time on task, and their times cluster in the 30s–40s,
while Block 4's cluster lower, in the teens-to-twenties.

---

## Parallel boxplots

When comparing a numerical variable across **more than two** categories
(or when boxplots are simply easier to line up than stem plots), draw one
boxplot per group on the **same scale**, stacked above/below each other.
Using the same scale and units for every group is essential — otherwise
the boxplots can't be compared directly.

**Worked Example.** As part of an R U OK Day activity, some students took
part in a meditation exercise. Their pulse rate was recorded before and
after:

$$\text{Before: } 90, 88, 86, 88, 106, 94, 102, 108, 98, 102$$
$$\text{After: } 83, 78, 82, 82, 86, 84, 92, 88, 90, 89$$

| | Min | $Q_1$ | Median | $Q_3$ | Max | IQR |
|---|---|---|---|---|---|---|
| **Before** | 86 | 88 | 96 | 102 | 108 | 14 |
| **After** | 78 | 82 | 85 | 89 | 92 | 7 |

(Neither group has any outliers by the $1.5\times IQR$ test.)

![[Parallel Boxplots - pulse rate before and after meditation.png]]

**Comparing:** every single statistic is lower after meditation — the
median pulse rate dropped from $96$ to $85$ bpm, and the spread roughly
halved (IQR $14 \to 7$). So the meditation exercise is associated with both
a **lower** typical pulse rate and **less variation** between students'
pulse rates.

---
See [[Content/Statistics/1 - Overview]] for the full formula sheet and common mistakes for this
study area.
