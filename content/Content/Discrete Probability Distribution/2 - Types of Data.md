Count the chairs in a classroom and you will always get a whole number like 28 or 29, never 28.4. Measure the height of a student, though, and the answer could be 172 cm, 172.3 cm or 172.35 cm, depending on how carefully you measure. These two kinds of data behave very differently, and they need different tools later on in this topic.

**Definition**: **Data** is the information we collect from an experiment or an observation. It comes in two main types:

- **Discrete data** is **counted**. It can only take separate values (usually whole numbers), with gaps in between. *e.g. the number of chairs in a room.*
- **Continuous data** is **measured**. It can take **any value in an interval**. *e.g. weight, height, time.*

![[Types of Data - Overview.png]]

==**Count it → discrete. Measure it → continuous.**==

## Random variables:

**Definition**: A **random variable** (r.v.) is what we measure or record about each outcome of an experiment. Its value depends on chance, so we don't know it until the experiment is done.

*e.g. Choose a student at random and record the number of students in their class wearing black t-shirts.*

- A random variable is written with a **capital letter**: X, Y, Z.
- The values it can take are written with a **small letter**: x, y, z.

==**Pr(X = x)**==

*read as "the probability that the random variable X takes the value x."* For example, Pr(X = 2) is the probability that X equals 2.

Random variables have the same two types as data:

- A **discrete random variable** takes separate values, so we can list them: {0, 1, 2, 3, …}. → [[3 - Discrete Probability Distributions]]
- A **continuous random variable** takes any value in an interval, e.g. 150 ≤ X ≤ 190. There are too many values to list. → [[8 - Continuous Distributions]]

![[Types of Data - Number Line.png]]

> [!tip] Tip
> Rounding doesn't change the type. A height written as "172 cm" is still **continuous**, because 172 is only the measurement rounded to the nearest cm. The real height could be 172.348… cm.

> [!tip] Tip
> Discrete doesn't always mean whole numbers. Shoe sizes (7, 7½, 8, 8½, …) are discrete because there are gaps between the possible values. Ask yourself: *"Can the value be anything in between?"* If not, it's discrete.


---

## Examples:

**Example 1:** Which of the following could be represented by discrete random variables?
**(a)** The number of goals scored at a football match
**(b)** The height of students in a maths class
**(c)** The number of HDs in Maths Unit 1
**(d)** The number of girls in a family with five children
**(e)** The time taken to run 10 km, in minutes

**Solution**:
**(a)** Goals are counted: 0, 1, 2, … → **discrete**
**(b)** Height is measured → **continuous**
**(c)** HDs are counted: 0, 1, 2, … → **discrete**
**(d)** Girls are counted: 0, 1, 2, 3, 4 or 5 → **discrete**
**(e)** Time is measured → **continuous**

So **(a), (c) and (d)** could be represented by discrete random variables.

*Note: in (d), there can't be 2.5 girls, so the values have gaps between them. A discrete variable can have just a few possible values: here only 6 (0 to 5).*

**Example 2:** A fair die is rolled 4 times. Let X be the number of sixes rolled.
**(a)** Is X discrete or continuous?
**(b)** List the possible values of X.

**Solution**:
**(a)** Sixes are counted, so X is a **discrete** random variable.
**(b)** X can be 0, 1, 2, 3 or 4, so x ∈ {0, 1, 2, 3, 4}.


---

## Exercises:

*Try each question first, then click on "Solution" to check your answer.*

**Question 1:** Classify each random variable as discrete or continuous.
**a)** The number of text messages a student sends in a day
**b)** The mass of a newborn baby
**c)** A person's shoe size
**d)** The temperature at noon
**e)** The number of heads when 10 coins are tossed
**f)** The time between two buses
**g)** A student's score on a 20-question multiple-choice test

> [!success]- Solution
> **a)** Discrete (counted)
> **b)** Continuous (measured)
> **c)** Discrete: sizes jump from one value to the next (7, 7½, 8, …)
> **d)** Continuous (measured)
> **e)** Discrete: 0, 1, 2, …, 10
> **f)** Continuous (measured)
> **g)** Discrete: 0, 1, 2, …, 20

**Question 2:** A student says: *"My height is 172 cm, which is a whole number, so height is discrete."* Explain what is wrong with this statement.

> [!success]- Solution
> Height is **measured**, so it's continuous. "172 cm" is only the height rounded to the nearest centimetre. The real height could be any value from 171.5 cm to 172.5 cm, such as 172.348… cm.

**Question 3:** Let X be the age of a randomly chosen student, and let Y be their age in completed years (the age they would write on a form). Classify X and Y.

> [!success]- Solution
> - X is **continuous**: age is time, and time is measured. A student could be 18.62… years old.
> - Y is **discrete**: completed years are counted (17, 18, 19, …), with gaps in between.
>
> *Same person, same idea, but how the data is recorded decides the type!*

**Question 4:** List the possible values of each random variable.
**a)** X = the sum of the numbers when two dice are rolled
**b)** Y = the number of times a coin is tossed until the first head appears
**c)** Z = the number of red balls when 3 balls are drawn without replacement from a bag of 2 red and 5 blue balls

> [!success]- Solution
> **a)** x ∈ {2, 3, 4, …, 12}
> **b)** y ∈ {1, 2, 3, 4, …}. Y is discrete but has **infinitely many** possible values, since the coin could land on tails again and again.
> **c)** z ∈ {0, 1, 2}. Z can't be 3 because there are only 2 red balls in the bag.
