## Stem-and-leaf plots

A stem-and-leaf plot (or "stem plot") displays numerical data by splitting
each value into two parts:
- the **stem** — the leading digit(s)
- the **leaf** — always the **last** digit

A **key** must always be given, since it tells the reader what place value
the stem/leaf represent — e.g. $1|6$ means $16$, or (for different data)
$1|6$ could mean $1.6$.

**Example.** Test scores: $62, 58, 71, 65, 70, 84, 58, 77, 91, 65, 73, 80$

Splitting into stem (tens digit) and leaf (units digit):

**Unordered** (leaves written in the order the data was collected):
```
Key: 6|2 means 62
 5 | 8 8
 6 | 2 5 5
 7 | 1 0 7 3
 8 | 4 0
 9 | 1
```

**Ordered** (each row's leaves sorted smallest to largest — makes it much
easier to read off the median, quartiles, etc.):
```
Key: 6|2 means 62
 5 | 8 8
 6 | 2 5 5
 7 | 0 1 3 7
 8 | 0 4
 9 | 1
```

A stem plot is quick to draw by hand and keeps every original data value
visible (unlike a histogram, which groups values into intervals) while
still showing the overall shape of the distribution.

---

## Histograms

A histogram displays grouped (interval) data as adjoining bars — the bar
height shows the frequency (or % frequency) for that interval, and because
the intervals are continuous, the bars touch (no gaps), unlike a bar chart
for categorical data.

**Example — using the grouped distance-to-college data from [[3 - Measures of Centre and Spread]]:**

| Distance (km) | $0$–$4$ | $5$–$9$ | $10$–$14$ | $15$–$19$ | $20$–$24$ | $25$–$29$ | $30$–$34$ |
|---|---|---|---|---|---|---|---|
| Frequency | 8 | 11 | 10 | 7 | 2 | 1 | 1 |

![[Histogram - distance to college.png]]

On a graphics calculator: enter the midpoints (or raw values) into one
list and the frequencies into a second list, turn on Stat Plot, choose the
histogram plot type, set the frequency list, check an appropriate window
(especially the bar width, "Xscl", matching your class width), then graph.

---

## Describing shape

See [[Content/Statistics/1 - Overview]] for the three ways to recognise and describe the shape of
a distribution (density curve / boxplot / histogram).

**Applying it:** for the distance-to-college data above, the mean
($10.875$ km) is noticeably larger than the median (inside the $10$–$14$
interval, close to $12$), and the frequencies trail off to the right (a
few students travel a long way) — so this distribution is **positively
skewed**.

---
See [[Content/Statistics/1 - Overview]] for the full formula sheet and common mistakes for this
study area.
