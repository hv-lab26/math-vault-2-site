We get a better understanding of a data set if we can locate its **centre**
(a "typical" value) and its **spread** (how varied the data is). How you
calculate each measure depends on how the data is presented: as a plain
list, in a frequency table, or in a frequency table with class intervals.

## Measures of centre

| Measure | Definition | How to find it |
|---|---|---|
| **Mean** ($\bar{x}$) | The average | $\bar{x} = \dfrac{\sum x}{n}$ |
| **Mode** | The value that occurs most often | Read off the most frequent value. A data set can have no mode, one mode, or several modes (bimodal/multimodal) |
| **Median** | The middle value when the data is sorted | Odd $n$: the middle value. Even $n$: the average of the two middle values |

## Measures of spread

| Measure | Formula | Notes |
|---|---|---|
| **Range** | $\text{max} - \text{min}$ | The simplest measure of spread — only uses two values, so it's very sensitive to outliers |
| **Interquartile range (IQR)** | $IQR = Q_3 - Q_1$ | The spread of the *middle 50%* of the data — Q1 is the median of the lower half, Q3 is the median of the upper half (exclude the overall median itself when $n$ is odd) |
| **Sample standard deviation** | $s_x = \sqrt{\dfrac{\sum(x-\bar{x})^2}{n-1}}$ | Used almost always in practice — this is what your calculator's "$s_x$" / "Sx" gives for a data **sample** |
| **Population standard deviation** | $\sigma_x = \sqrt{\dfrac{\sum(x-\bar{x})^2}{n}}$ | Only use this if the data genuinely *is* the entire population, not a sample from it |

Standard deviation tells you the typical distance a data point sits from
the mean — a small SD means the data is tightly clustered, a large SD means
it's spread out.

**Effect of a linear change in the data.** If every value in a data set has
a constant added to it (e.g. "everyone grows 5 cm taller"), the **mean**
shifts by that same constant, but the **standard deviation is unchanged**
(spread doesn't change just because everything shifted up together). If
every value is instead *scaled* by a constant $k$, both the mean and the
standard deviation get multiplied by $k$ (and the SD by $|k|$, since spread
can't be negative).

---

## Worked Example 1 — finding all five measures, and what happens when you add a data point

The number of small aeroplanes flying into a remote airstrip over a 15-day
period is:
$$5,\ 7,\ 0,\ 3,\ 4,\ 6,\ 4,\ 0,\ 5,\ 3,\ 6,\ 9,\ 4,\ 2,\ 8$$

**Sorted:** $0,0,2,3,3,4,4,4,5,5,6,6,7,8,9$

- **Mean:** $\bar{x} = \dfrac{66}{15} = 4.4$
- **Mode:** $4$ (appears 3 times — more than any other value)
- **Median:** $n=15$ is odd, so the median is the 8th value $= 4$
- **Range:** $9 - 0 = 9$
- **IQR:** lower half $\{0,0,2,3,3,4,4\} \Rightarrow Q_1 = 3$ (its median);
  upper half $\{5,5,6,6,7,8,9\} \Rightarrow Q_3 = 6$ (its median).
  $IQR = 6 - 3 = 3$

On the next day, 6 more aeroplanes land, extending the data to 16 days:
$$5,\ 7,\ 0,\ 3,\ 4,\ 6,\ 4,\ 0,\ 5,\ 3,\ 6,\ 9,\ 4,\ 2,\ 8,\ 6$$

**Sorted:** $0,0,2,3,3,4,4,4,5,5,6,6,6,7,8,9$

- **Mean:** $\bar{x} = \dfrac{72}{16} = 4.5$ (shifted slightly up)
- **Mode:** now **bimodal** — $4$ and $6$ both occur 3 times
- **Median:** $n=16$ is even, so median $= \dfrac{4+5}{2} = 4.5$
- **Range:** still $9-0=9$ (new value wasn't a new max/min)
- **IQR:** lower half (first 8) $\Rightarrow Q_1=3$; upper half (last 8)
  $\Rightarrow Q_3=6$. $IQR = 3$ (unchanged)

This shows why IQR is often preferred to range: a single new data point
nudged the mean and median, but the "middle 50%" of the data barely moved.

---

## Worked Example 2 — mean from a frequency table

The table shows the number of questions (out of a short quiz) answered
correctly by 40 students:

| Score ($x$) | 3 | 4 | 5 | 6 | 7 | 8 | 9 | **Total** |
|---|---|---|---|---|---|---|---|---|
| Frequency ($f$) | 1 | 2 | 4 | 14 | 11 | 6 | 2 | **40** |

With a frequency table, every value is weighted by how often it occurs:
$$\bar{x} = \frac{\sum (x \times f)}{\sum f} = \frac{(3)(1)+(4)(2)+(5)(4)+(6)(14)+(7)(11)+(8)(6)+(9)(2)}{40} = \frac{258}{40} = 6.45$$

On a graphics calculator: enter the scores into one list and the
frequencies into a second list, then run 1-Variable Statistics with the
frequency list set as the "FreqList" (leave FreqList blank for a plain,
unweighted list of data).

---

## Worked Example 3 — mean and standard deviation from grouped (interval) data

When data is grouped into class intervals, we don't know the exact values
inside each interval — so we use the **midpoint of each interval** to
stand in for every value in it.

The table shows the distance (to the nearest km) travelled to college by a
class of 40 students:

| Distance (km) | $0$–$4$ | $5$–$9$ | $10$–$14$ | $15$–$19$ | $20$–$24$ | $25$–$29$ | $30$–$34$ |
|---|---|---|---|---|---|---|---|
| Frequency | 8 | 11 | 10 | 7 | 2 | 1 | 1 |
| Midpoint | 2 | 7 | 12 | 17 | 22 | 27 | 32 |

**Mean** (using midpoints exactly as in Worked Example 2):
$$\bar{x} = \frac{(2)(8)+(7)(11)+(12)(10)+(17)(7)+(22)(2)+(27)(1)+(32)(1)}{40} = \frac{435}{40} = 10.875 \text{ km}$$

**Standard deviation** (sample, dividing by $n-1=39$):
$$s_x = \sqrt{\frac{\sum f(x-\bar{x})^2}{n-1}} = \sqrt{\frac{2024.375}{39}} \approx 7.205 \text{ km}$$

**What percentage of students travel 15 km or more?** Add the frequencies
for every interval from $15$–$19$ upward, divide by the total, and convert
to a percentage:
$$\frac{7+2+1+1}{40}\times 100 = 27.5\%$$

**Median interval.** With $n=40$, the median sits between the 20th and
21st values. Running totals of frequency: $0$–$4 \to 8$, $5$–$9 \to 19$,
$10$–$14 \to 29$ — the 20th and 21st values both fall in the $10$–$14$
interval, so the **median interval is $10$–$14$**.

(This distribution turns out to be positively skewed — see [[Content/Statistics/1 - Overview]]
for how to recognise and describe the shape of a distribution.)

---
See [[Content/Statistics/1 - Overview]] for the full formula sheet and common mistakes for this
study area.
