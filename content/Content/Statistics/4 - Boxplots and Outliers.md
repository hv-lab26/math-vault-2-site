## The five-number summary

A boxplot (box-and-whisker plot) is built from five numbers:

$$\text{Minimum},\quad Q_1,\quad \text{Median } (Q_2),\quad Q_3,\quad \text{Maximum}$$

- $Q_1$ (lower quartile) is the median of the **lower half** of the data.
- $Q_3$ (upper quartile) is the median of the **upper half** of the data.
- When $n$ is odd, exclude the overall median itself before splitting into
  halves. When $n$ is even, split exactly in half (no value to exclude).

## Drawing a boxplot

A boxplot is drawn above a number line:
- A **box** stretches from $Q_1$ to $Q_3$ (this box covers the middle 50%
  of the data — its width is the IQR), with a line inside it at the median.
- A **whisker** extends from each side of the box out to the minimum and
  maximum — *unless* that extreme value is an outlier (see below), in which
  case the whisker stops at the last value that **isn't** an outlier, and
  the outlier itself is marked separately with an asterisk (there can be
  more than one outlier at either end).

![[Boxplot - five-number summary.png]]

A boxplot can also reveal the distribution's **skew**, from where the
median sits inside the box — see [[Content/Statistics/1 - Overview]].

## Outliers

An **outlier** is a data value separated from the main body of data — much
larger or much smaller than most of the rest. The standard test uses the
IQR to build a "fence" around the data:

$$\text{Lower boundary} = Q_1 - 1.5\times IQR \qquad\qquad \text{Upper boundary} = Q_3 + 1.5\times IQR$$

Any value **below** the lower boundary or **above** the upper boundary is
an outlier:
$$\text{not an outlier} \iff Q_1 - 1.5\times IQR \ \le\ x\ \le\ Q_3 + 1.5\times IQR$$

If a value is an outlier, the whisker doesn't reach it — the whisker
stops at the most extreme value that is *not* an outlier, and the outlier
is drawn as a separate point (asterisk).

## Interpreting a boxplot

Once you have the five-number summary (read straight off the boxplot, or
calculated from raw data), each value has a standard interpretation:

- **Median:** "50% of the [values] are less than or equal to [median], and
  50% are greater than or equal to [median]."
- **Lower quartile ($Q_1$):** "About 25% of the [values] are less than or
  equal to $Q_1$."
- **Upper quartile ($Q_3$):** "About 25% of the [values] are greater than
  or equal to $Q_3$" (equivalently, "about 75% are less than or equal to
  $Q_3$").
- **IQR:** "The middle 50% of the [values] lie between $Q_1$ and $Q_3$."
- **Range:** "The total spread of the [values] is [range], between [min]
  and [max]."

---

## Worked Example — five-number summary, mode, and outlier test, comparing two groups

A survey recorded the ages of 11 workers at a McDonald's outlet and 11
workers at a hawker centre:

$$\text{McDonald's: } 16, 17, 17, 18, 18, 18, 19, 20, 22, 25, 42$$
$$\text{Hawker centre: } 19, 20, 23, 25, 35, 40, 45, 47, 50, 51, 52$$

(Both lists are already sorted, and $n=11$ for each.)

**Mode.** McDonald's: $18$ occurs three times $\Rightarrow$ mode $=18$.
Hawker centre: every value is different $\Rightarrow$ **no mode**.

**Five-number summary (McDonald's).** $n=11$, so the median is the 6th
value: $\text{med} = 18$. Lower half (first 5, excluding the median):
$\{16,17,17,18,18\} \Rightarrow Q_1 = 17$ (its median). Upper half (last 5):
$\{19,20,22,25,42\} \Rightarrow Q_3 = 22$.
$$\text{Min}=16,\ Q_1=17,\ \text{Med}=18,\ Q_3=22,\ \text{Max}=42$$

**Five-number summary (Hawker centre).** Median (6th value) $=40$. Lower
half $\{19,20,23,25,35\}\Rightarrow Q_1=23$. Upper half
$\{45,47,50,51,52\}\Rightarrow Q_3=50$.
$$\text{Min}=19,\ Q_1=23,\ \text{Med}=40,\ Q_3=50,\ \text{Max}=52$$

**Outlier test (McDonald's).** $IQR = 22-17=5$.
$$\text{Lower boundary} = 17-1.5(5) = 9.5 \qquad \text{Upper boundary} = 22+1.5(5)=29.5$$
$42 > 29.5$, so **42 is an outlier** (nobody else is close — the next
highest is 25).

**Outlier test (Hawker centre).** $IQR = 50-23=27$.
$$\text{Lower boundary} = 23-1.5(27) = -17.5 \qquad \text{Upper boundary} = 50+1.5(27)=90.5$$
Every value is between $-17.5$ and $90.5$, so **there are no outliers**.

**Comparing the two groups:** the hawker centre workers are, on average,
considerably older (mean $37$ vs. $21$) and more spread out (IQR $27$ vs.
$5$) than the McDonald's workers — and unlike McDonald's, the hawker
centre's oldest worker (52) is *not* unusually extreme compared to the
rest of that group.

---
See [[Content/Statistics/1 - Overview]] for the full formula sheet and common mistakes for this
study area.
