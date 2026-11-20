This study area covers data analysis: how to classify data, summarise and
compare distributions of a single variable (**univariate data**), and
describe, model, and predict with the relationship between two variables
(**bivariate data**).

## Notes
1. [[2 - Types of Statistical Data]] - categorical vs. numerical, discrete vs. continuous
2. [[3 - Measures of Centre and Spread]] - mean, median, mode, range, IQR, standard deviation
3. [[4 - Boxplots and Outliers]] - five-number summary, the $1.5\times IQR$ outlier test
4. [[5 - Stem-and-Leaf Plots and Histograms]] - stem plots, grouped-frequency histograms
5. [[6 - Comparing Distributions]] - back-to-back stem plots, parallel boxplots
6. [[7 - Bivariate Data and Scatterplots]] - scatter plots, Pearson's $r$, $r^2$
7. [[8 - Least Squares Regression]] - the LSRL, interpreting slope and intercept
8. [[9 - Prediction - Interpolation and Extrapolation]] - how far you can trust a prediction
9. [[10 - Residual Analysis]] - checking a straight line was the right model
10. [[11 - Linearising Data]] - transforming non-linear data to fit a straight line
11. [[12 - Revision]] - practice questions and harder review questions

## Formula sheet
| Rule | Formula |
|---|---|
| Mean | $\bar{x} = \dfrac{\sum x}{n}$ |
| Population standard deviation | $\sigma_x = \sqrt{\dfrac{\sum(x-\bar{x})^2}{n}}$ |
| Sample standard deviation | $s_x = \sqrt{\dfrac{\sum(x-\bar{x})^2}{n-1}}$ |
| Range | $\text{max} - \text{min}$ |
| Interquartile range | $IQR = Q_3 - Q_1$ |
| Outlier boundaries | $\left[\,Q_1 - 1.5\times IQR,\ \ Q_3 + 1.5\times IQR\,\right]$ |
| Pearson's correlation coefficient | $r = \dfrac{\sum(x-\bar{x})(y-\bar{y})}{(n-1)\,s_x\,s_y}$, $-1\le r\le1$ |
| Coefficient of determination | $r^2$ = proportion of variation in $y$ explained by $x$ |
| Least-squares regression line | $y=ax+b$, where $a = r\,\dfrac{s_y}{s_x}$, $b = \bar{y}-a\bar{x}$ |
| Residual | $\text{Residual} = y_{\text{actual}} - y_{\text{predicted}}$ |

## Which method?
| The question... | Use |
|---|---|
| asks to classify a variable | [[2 - Types of Statistical Data]] |
| gives raw data and asks for mean / median / mode / IQR / SD | [[3 - Measures of Centre and Spread]] |
| gives a five-number summary, or asks to test for outliers | [[4 - Boxplots and Outliers]] |
| gives raw data and asks you to draw or read off a stem plot / histogram | [[5 - Stem-and-Leaf Plots and Histograms]] |
| asks you to compare two or more groups | [[6 - Comparing Distributions]] |
| gives paired $(x,y)$ data and asks for direction / strength / $r$ | [[7 - Bivariate Data and Scatterplots]] |
| asks for "the equation of the line of best fit" | [[8 - Least Squares Regression]] |
| asks you to substitute a given $x$ or $y$ to predict | [[9 - Prediction - Interpolation and Extrapolation]] - then check interpolation vs. extrapolation |
| gives residuals, or asks whether a straight line is a good model | [[10 - Residual Analysis]] |
| a scatter or residual plot shows a curved pattern | [[11 - Linearising Data]] |

## Key words
| Word | What to do |
|---|---|
| "typical value", "on average" | mean, or median if skewed/has outliers |
| "spread", "variation" | IQR or standard deviation |
| "outlier" | $1.5\times IQR$ fence from $Q_1$/$Q_3$ |
| "skewed" | compare mean vs. median (or see "Describing the shape of a distribution" below) |
| "strength of the relationship" | $r$ |
| "% of variation explained" | $r^2 \times 100\%$ |
| "reliable prediction?" | check interpolation (inside the data) vs. extrapolation (outside) |
| "is a straight line the right model?" | plot the residuals - random scatter is good, a curve isn't |

---

## Describing the shape of a distribution

The same skew shows up in three different kinds of display - a density
curve, a boxplot, or a histogram - so it's worth knowing what to look for
in each.

### Via a density curve (or any smooth distribution sketch)

**Skewness** describes how symmetric a distribution is. Look at the
direction of the longer "tail":

| Shape | What it looks like | Mean vs. median |
|---|---|---|
| **Symmetrical** | Evenly spread on both sides of the centre | Mean $\approx$ median $\approx$ mode |
| **Positively skewed** | Longer tail on the **right** (a few unusually large values stretch it out) | Mean $>$ median (the large values pull the mean up) |
| **Negatively skewed** | Longer tail on the **left** (a few unusually small values stretch it out) | Mean $<$ median (the small values pull the mean down) |

![[Skewness - symmetrical positive negative.png]]

A quick way to remember which is which: the name describes **which side
the tail is stretched toward**, not which side has more data piled up.

### Via a boxplot: where the median sits in the box

The median divides the box into two parts: $Q_1$-to-median, and
median-to-$Q_3$. If one of those parts is visibly squashed while the other
is stretched out, that's the same skew showing up in a different shape:

- **Median sits closer to $Q_1$** (squashed on the left, more room on the
  right side of the box, often with a longer right whisker too) $\Rightarrow$
  **positively skewed**.
- **Median sits closer to $Q_3$** (squashed on the right, more room on the
  left side of the box, often with a longer left whisker too) $\Rightarrow$
  **negatively skewed**.

![[Skewness from a boxplot - median position.png]]

This is exactly the same underlying idea as the curve above -> the "stretched"
side of the box points toward the longer tail.

### Via a histogram

The same rule again, just drawn as bars: if the bars **trail off into a
longer, lower run of bars on one side** (rather than dropping off sharply),
the distribution is skewed toward that side.

**Example**: the distance-to-college histogram from [[5 - Stem-and-Leaf Plots and Histograms]]:

![[Histogram - distance to college.png]]

The bars are tallest on the left and trail off into a long, low tail on the
right (only $1$–$2$ students in each of the farthest intervals) => so this
distribution is **positively skewed**, which also matches its mean
($10.875$ km, from [[3 - Measures of Centre and Spread]]) sitting above its
median interval ($10$–$14$ km).

---

> [!warning] 
> - **Slope interpretation, backwards.** Always phrase it as *"for every
>   1 [unit] increase in the **independent** variable, the **dependent**
>   variable changes by [slope] [unit]."* It's very easy to accidentally
>   swap which variable is doing the changing and which is responding ->
>   before writing the sentence, check which one you substituted on the
>   x-axis (independent) and which is on the y-axis (dependent).
> - **Interpolation vs. extrapolation, mixed up.** Interpolation = predicting
>   *inside* the range of the original data (generally reliable).
>   Extrapolation = predicting *outside* that range (generally unreliable,
>   and less reliable the further outside the range you go). Always check
>   the prediction's $x$-value against the min/max of the actual data
>   before judging reliability, don't just guess from the question's wording.
> - **Correlation vs. causation.** A strong $r$ only shows the variables
>   move together. It never by itself proves one *causes* the other.
>   There's often a third (confounding) variable, or the causation could run
>   in the opposite direction.
> - **Judging the *strength* of $r$ from its sign.** Direction (positive/
>   negative) and strength (weak/moderate/strong) are two separate things:
>   e.g. $r=-0.16$ is a **weak** negative correlation, not a strong one, even
>   though it's definitely negative. Judge strength only from how close
>   $|r|$ is to $1$ (close to $0$ = weak, close to $\pm1$ = strong),
>   completely separately from the sign.
> - **Sample vs. population standard deviation.** Check whether you're
>   given/asked for $s_x$ (divide by $n-1$, used for a sample, almost
>   always the one your calculator's "Sx" gives) or $\sigma_x$ (divide by
>   $n$, used only when you have the whole population).
> - **Outlier test, using the wrong fence.** The boundaries use $1.5\times
>   IQR$ added/subtracted from $Q_3$/$Q_1$, not the mean, and not the
>   range.
> - **Reading "$r^2$" as a percentage of something other than variation.**
>   It is specifically the proportion of *variation* in $y$ explained by
>   $x$, not "how often the model is correct" or "how close the points are
>   to each other."
> - **Linearising the wrong axis.** Before transforming, look at which way
>   the scatter curves: check a few standard transformations ($x^2$,
>   $\sqrt{x}$, $1/x$, $\log x$, $\log y$) and pick whichever one actually
>   pushes $r$ closer to $\pm 1$, don't assume a transformation worked
>   without checking the new $r$.
