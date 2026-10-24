
A Venn diagram is great for *seeing* how two events overlap. But when you need to *calculate* with them, a table is often quicker to read. This table is called a Karnaugh diagram (also known as "a Karnaugh map" or "a probability table.")

**Definition**: A Karnaugh diagram (probability table) is a two-way table that shows the probability of every combination of two events A and B and their complements A' and B'.

![[Karnaugh Diagram - Venn to Table.png]]


Each of the 4 inner cells matches one region of the [[4 - Venn Diagram]], and the totals sit on the edges:

|           | **B**      | **B'**      | **Total** |
| --------- | ---------- | ----------- | --------- |
| **A**     | Pr(A ∩ B)  | Pr(A ∩ B')  | Pr(A)     |
| **A'**    | Pr(A' ∩ B) | Pr(A' ∩ B') | Pr(A')    |
| **Total** | Pr(B)      | Pr(B')      | 1         |

## Rules of a Karnaugh diagram:

**Rule 1:** Each row adds up to its total, and each column adds up to its total. For example:

==**Pr(A ∩ B) + Pr(A ∩ B') = Pr(A)**==
==**Pr(A ∩ B) + Pr(A' ∩ B) = Pr(B)**==

**Rule 2:** The grand total (bottom-right corner) is always 1.

==**Pr(A) + Pr(A') = 1**== and ==**Pr(B) + Pr(B') = 1**==

*Note: if you know 2 of the 3 numbers in any row or column, you can always find the 3rd one. That's how you fill in the whole table from just a few values.*

> [!tip] Tip: treat it like Sudoku
> Look for a row or column that already has 2 numbers, fill in the 3rd, and repeat until the table is full. Start with the totals (e.g. Pr(A') = 1 − Pr(A)), because they are the easiest.

## Reading the table:

- **"and" (∩)**: read **one cell**. E.g. Pr(A ∩ B') is the cell in row A, column B'.
- **"or" (∪)**: add every cell that is in A or B (or both), or take the "neither" cell away from 1:

==**Pr(A ∪ B) = Pr(A ∩ B) + Pr(A ∩ B') + Pr(A' ∩ B) = 1 − Pr(A' ∩ B')**==

- **"given" (|)**: stay inside the row or column you are given, and divide by its total:

==**Pr(A | B) = Pr(A ∩ B) ÷ Pr(B)**==

*read as "the probability of A given B."*

- **Independent?** A and B are independent if ==**Pr(A ∩ B) = Pr(A) × Pr(B)**== (see [[3 - Laws of Probability]]).
- **Mutually exclusive?** A and B are mutually exclusive if ==**Pr(A ∩ B) = 0**==, i.e. the A ∩ B cell is 0.

> [!tip] Tip: "given" questions
> Cover the rest of the table with your hand and look only at the row or column you were given. That row or column becomes your new "whole", so its total goes on the bottom of the fraction.


> [!tip] Venn or Karnaugh?
> Use a Karnaugh diagram for **2 events**, especially when you are given probabilities like Pr(A' ∩ B'). Use a [[4 - Venn Diagram]] for **3 or more events**, where a simple table doesn't work.

## Counts instead of probabilities

A Karnaugh diagram can also hold **numbers** of people or items (this is often called a two-way table). The grand total is then the total number instead of 1, and to turn a count into a probability, divide by the grand total:

==**Pr(event) = number in the cell(s) ÷ grand total**==

---

## Examples:

**Example 1:** For two events A and B, Pr(A) = 0.6, Pr(B) = 0.5 and Pr(A ∩ B) = 0.2.
**a)** Complete the Karnaugh diagram.
**b)** Find Pr(A ∪ B).
**c)** Find Pr(A' ∩ B').
**d)** Find Pr(A | B).
**e)** Are A and B independent?

**Solution**:
**a)** Put in the given values (in bold), then use "rows and columns add up":

|           | **B**           | **B'**          | **Total**     |
| --------- | --------------- | --------------- | ------------- |
| **A**     | **0.2**         | 0.6 − 0.2 = 0.4 | **0.6**       |
| **A'**    | 0.5 − 0.2 = 0.3 | 0.4 − 0.3 = 0.1 | 1 − 0.6 = 0.4 |
| **Total** | **0.5**         | 1 − 0.5 = 0.5   | 1             |

*Check: column B' => 0.4 + 0.1 = 0.5*

**b)** $\Pr(A\cup B)=0.2+0.4+0.3=0.9$ (or $1-0.1=0.9$)

**c)** $\Pr(A'\cap B')=0.1$

**d)**
$$\Pr(A\mid B)=\frac{\Pr(A\cap B)}{\Pr(B)}=\frac{0.2}{0.5}=0.4$$

**e)** $\Pr(A)\times\Pr(B)=0.6\times0.5=0.3\mathrel{\char"2260}0.2=\Pr(A\cap B)$, so A and B are **not independent**.

**Example 2:** 100 students were surveyed: 45 study Economics (E), 60 study Maths (M) and 25 study both.
**a)** Show this information in a two-way table.
**b)** A student is chosen at random. Find the probability that the student studies neither subject.
**c)** Given that the student studies Maths, find the probability that they also study Economics.
**d)** Are E and M independent?

**Solution**:
**a)**

|           | **M**  | **M'** | **Total** |
| --------- | ------ | ------ | --------- |
| **E**     | **25** | 20     | **45**    |
| **E'**    | 35     | 20     | 55        |
| **Total** | **60** | 40     | **100**   |

**b)**
$$\Pr(E'\cap M')=\frac{20}{100}=0.2$$

**c)** Stay inside the M column (60 students):
$$\Pr(E\mid M)=\frac{25}{60}=\frac{5}{12}\approx0.417$$

**d)** $\Pr(E)\times\Pr(M)=0.45\times0.6=0.27\mathrel{\char"2260}0.25=\Pr(E\cap M)$, so E and M are **not independent**.

---

## Exercises:

*Try each question first, then click on "Solution" to check your answer.*

**Question 1:** Pr(A) = 0.7, Pr(B) = 0.4 and Pr(A ∩ B) = 0.3.
**a)** Complete the Karnaugh diagram.
**b)** Find Pr(A ∪ B).
**c)** Find Pr(A ∩ B').
**d)** Find Pr(A' ∪ B').
**e)** Find Pr(B | A).

> [!success]- Solution
> **a)**
>
> |           | **B**   | **B'** | **Total** |
> | --------- | ------- | ------ | --------- |
> | **A**     | **0.3** | 0.4    | **0.7**   |
> | **A'**    | 0.1     | 0.2    | 0.3       |
> | **Total** | **0.4** | 0.6    | 1         |
>
> **b)** $\Pr(A\cup B)=1-\Pr(A'\cap B')=1-0.2=0.8$
>
> **c)** $\Pr(A\cap B')=0.4$
>
> **d)** A' ∪ B' is every cell except A ∩ B:
> $$\Pr(A'\cup B')=1-\Pr(A\cap B)=1-0.3=0.7$$
>
> **e)** Stay inside row A:
> $$\Pr(B\mid A)=\frac{\Pr(A\cap B)}{\Pr(A)}=\frac{0.3}{0.7}=\frac{3}{7}\approx0.429$$

**Question 2:** Pr(A') = 0.45, Pr(B) = 0.3 and Pr(A' ∩ B') = 0.35.
**a)** Complete the Karnaugh diagram.
**b)** Find Pr(A ∪ B).
**c)** Find Pr(A | B).
**d)** Are A and B independent?

> [!success]- Solution
> **a)** Pr(A) = 1 − 0.45 = 0.55 and Pr(B') = 1 − 0.3 = 0.7. Then fill in row A' first, because it already has 2 numbers.
>
> |           | **B**           | **B'**             | **Total** |
> | --------- | --------------- | ------------------ | --------- |
> | **A**     | 0.3 − 0.1 = 0.2 | 0.55 − 0.2 = 0.35  | 0.55      |
> | **A'**    | 0.45 − 0.35 = 0.1 | **0.35**         | **0.45**  |
> | **Total** | **0.3**         | 0.7                | 1         |
>
> *Check: column B' → 0.35 + 0.35 = 0.7 ✓*
>
> **b)** $\Pr(A\cup B)=1-\Pr(A'\cap B')=1-0.35=0.65$
>
> **c)**
> $$\Pr(A\mid B)=\frac{\Pr(A\cap B)}{\Pr(B)}=\frac{0.2}{0.3}=\frac{2}{3}\approx0.667$$
>
> **d)** $\Pr(A)\times\Pr(B)=0.55\times0.3=0.165\mathrel{\char"2260}0.2=\Pr(A\cap B)$, so A and B are **not independent**.

**Question 3:** A and B are **independent** events with Pr(A) = 0.4 and Pr(B) = 0.5.
**a)** Complete the Karnaugh diagram.
**b)** Find Pr(A ∪ B).
**c)** Show that A' and B' are also independent.

> [!success]- Solution
> **a)** Independent, so $\Pr(A\cap B)=\Pr(A)\times\Pr(B)=0.4\times0.5=0.2$
>
> |           | **B**   | **B'** | **Total** |
> | --------- | ------- | ------ | --------- |
> | **A**     | 0.2     | 0.2    | **0.4**   |
> | **A'**    | 0.3     | 0.3    | 0.6       |
> | **Total** | **0.5** | 0.5    | 1         |
>
> **b)** $\Pr(A\cup B)=1-\Pr(A'\cap B')=1-0.3=0.7$
>
> **c)** $\Pr(A')\times\Pr(B')=0.6\times0.5=0.3=\Pr(A'\cap B')$ ✓, so A' and B' are independent too.

**Question 4:** A and B are **mutually exclusive** events with Pr(A) = 0.35 and Pr(B) = 0.4.
**a)** Complete the Karnaugh diagram.
**b)** Find Pr(A ∪ B).
**c)** Find Pr(A | B).
**d)** Are A and B independent?

> [!success]- Solution
> **a)** Mutually exclusive, so Pr(A ∩ B) = 0.
>
> |           | **B**   | **B'** | **Total** |
> | --------- | ------- | ------ | --------- |
> | **A**     | **0**   | 0.35   | **0.35**  |
> | **A'**    | 0.4     | 0.25   | 0.65      |
> | **Total** | **0.4** | 0.6    | 1         |
>
> **b)** $\Pr(A\cup B)=\Pr(A)+\Pr(B)=0.35+0.4=0.75$
>
> **c)** $\Pr(A\mid B)=\dfrac{0}{0.4}=0$. If B happened, A cannot have happened.
>
> **d)** $\Pr(A)\times\Pr(B)=0.35\times0.4=0.14\mathrel{\char"2260}0=\Pr(A\cap B)$, so A and B are **not independent**.
> *Note: mutually exclusive is NOT the same as independent. Mutually exclusive events (with non-zero probabilities) are never independent, because one happening tells you the other did not.*

**Question 5:** A café had 200 customers on Monday: 120 ordered coffee (C), 70 ordered cake (K) and 40 ordered both.
**a)** Show this information in a two-way table.
**b)** A customer is chosen at random. Find Pr(the customer ordered cake but no coffee).
**c)** Find Pr(the customer ordered neither).
**d)** Find Pr(C | K).
**e)** Find Pr(K | C).

> [!success]- Solution
> **a)**
>
> |           | **K**  | **K'** | **Total** |
> | --------- | ------ | ------ | --------- |
> | **C**     | **40** | 80     | **120**   |
> | **C'**    | 30     | 50     | 80        |
> | **Total** | **70** | 130    | **200**   |
>
> **b)** $\Pr(C'\cap K)=\dfrac{30}{200}=\dfrac{3}{20}=0.15$
>
> **c)** $\Pr(C'\cap K')=\dfrac{50}{200}=\dfrac{1}{4}$
>
> **d)** Stay inside the K column (70 customers):
> $$\Pr(C\mid K)=\frac{40}{70}=\frac{4}{7}\approx0.571$$
>
> **e)** Stay inside the C row (120 customers):
> $$\Pr(K\mid C)=\frac{40}{120}=\frac{1}{3}$$
> *Note: Pr(C | K) ≠ Pr(K | C). Which event is "given" matters!*

**Question 6:** Pr(A) = 0.5, Pr(B) = 0.4 and Pr(A ∪ B) = 0.7.
**a)** Find Pr(A ∩ B).
**b)** Complete the Karnaugh diagram.
**c)** Are A and B independent?

> [!success]- Solution
> **a)** Use the addition rule from [[3 - Laws of Probability]]:
> $$\Pr(A\cap B)=\Pr(A)+\Pr(B)-\Pr(A\cup B)=0.5+0.4-0.7=0.2$$
>
> **b)**
>
> |           | **B**   | **B'** | **Total** |
> | --------- | ------- | ------ | --------- |
> | **A**     | 0.2     | 0.3    | **0.5**   |
> | **A'**    | 0.2     | 0.3    | 0.5       |
> | **Total** | **0.4** | 0.6    | 1         |
>
> **c)** $\Pr(A)\times\Pr(B)=0.5\times0.4=0.2=\Pr(A\cap B)$, so A and B **are independent**.

**Question 7:** Pr(A) = 0.6, Pr(B | A) = 0.5 and Pr(B | A') = 0.25.
**a)** Complete the Karnaugh diagram.
**b)** Find Pr(B).
**c)** Find Pr(A | B).

> [!success]- Solution
> **a)** Multiply, just like along the branches of a [[5 - Tree Diagram]]:
> $\Pr(A\cap B)=0.6\times0.5=0.3$ and $\Pr(A'\cap B)=0.4\times0.25=0.1$
>
> |           | **B** | **B'** | **Total** |
> | --------- | ----- | ------ | --------- |
> | **A**     | 0.3   | 0.3    | **0.6**   |
> | **A'**    | 0.1   | 0.3    | 0.4       |
> | **Total** | 0.4   | 0.6    | 1         |
>
> **b)** $\Pr(B)=0.3+0.1=0.4$
>
> **c)**
> $$\Pr(A\mid B)=\frac{\Pr(A\cap B)}{\Pr(B)}=\frac{0.3}{0.4}=0.75$$
