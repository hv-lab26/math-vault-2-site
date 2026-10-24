At a school fair, a stall charges \$2 to toss two coins. Two heads wins \$5, one head wins \$1, and no heads wins nothing. Is it worth playing? You might win \$5, but you might also win nothing. To decide, we look at what happens **on average** over many games, which is exactly what the [[4 - Expectation|expected value]] measures.

**Definition**: A game is **fair** if the **expected profit** of the player is **zero**. In the long run, neither the player nor the organiser is expected to win or lose money.

==**A game is fair ⟺ E(profit) = 0**==

## Profit vs winnings:

- **Winnings (W)**: the money the player receives.
- **Cost (c)**: the money the player pays to play.
- **Profit (X)**: what the player actually gains, X = W − c. *(A negative profit is a loss.)*

Because E(aX + b) = aE(X) + b:

==**E(profit) = E(winnings) − cost**==

| E(profit) | The game...                                                  |
| --------- | ------------------------------------------------------------ |
| = 0       | is fair                                                      |
| > 0       | favours the player                                           |
| < 0       | favours the organiser (the "house")                         |

The player's expected loss, usually given as a percentage of the bet, is called the **house edge**.

## The fair price:

The **fair price** is the cost that makes the game fair. Set E(profit) = 0:

==**Fair price = E(winnings)**==

## Steps:

1. Choose the random variable: **profit** (or winnings) for each outcome.
2. Find the probability of each outcome and make a probability table.
3. Find the expected value.
4. Fair ⟺ E(profit) = 0. If there is an unknown, set E(profit) = 0 and solve.

![[Fair Games - Expected Profit.png]]

*The graph shows the two-coin game from the start of this page: E(profit) = 1.75 − price. Below \$1.75 the player is expected to gain; above \$1.75 the organiser is.*

> [!tip] Exam tip
> Read carefully whether the **stake is returned**. "You win \$5" usually means you receive \$5, so your profit is \$5 − cost. "You win \$5 and get your \$2 back" means your profit is \$5. Write the profit for every outcome in the table before doing anything else.

> [!tip] Tip
> A fair game can still be risky. Two games can both have E(profit) = 0 but very different [[5 - Variance|variances]]: the one with the bigger variance has bigger wins and bigger losses (see Question 5).

> [!info] Fun fact: the house always wins
> A European roulette wheel has 37 pockets (0 to 36). A \$1 bet on a single number pays \$35 profit if it wins. The expected profit is
> $$E(X)=35\times\frac{1}{37}+(-1)\times\frac{36}{37}=-\frac{1}{37}\approx-0.027$$
> So the casino keeps about 2.7 cents of every dollar bet, on average. American wheels have an extra "00" pocket (38 pockets), which raises the house edge to about 5.3%. Almost every casino game is designed to have a negative expected profit for the player.

---

## Examples:

**Example 1:** Two fair coins are tossed. A player wins \$5 if both coins show heads, \$1 if exactly one coin shows a head, and nothing otherwise. It costs \$2 to play.
**a)** Find the expected winnings.
**b)** Find the expected profit. Is the game fair?
**c)** What should the game cost for it to be fair?

**Solution**:
Pr(2 heads) = 1/4, Pr(1 head) = 2/4 = 1/2, Pr(0 heads) = 1/4.

**a)**

| Winnings w   | \$5  | \$1  | \$0  |
| ------------ | --- | --- | --- |
| Pr(W = w)    | 1/4 | 1/2 | 1/4 |

$$E(W)=5\times\frac{1}{4}+1\times\frac{1}{2}+0\times\frac{1}{4}=1.25+0.5=\$1.75$$

**b)** Profit = winnings − \$2:

| Profit x  | \$3  | −\$1 | −\$2 |
| --------- | --- | --- | --- |
| Pr(X = x) | 1/4 | 1/2 | 1/4 |

$$E(X)=3\times\frac{1}{4}+(-1)\times\frac{1}{2}+(-2)\times\frac{1}{4}=0.75-0.5-0.5=-\$0.25$$
*or simply* E(profit) = E(W) − cost = 1.75 − 2 = −\$0.25.

E(profit) ≠ 0, so the game is **not fair**. On average, the player loses 25 cents per game (the stall gains 25 cents).

**c)** Fair price = E(winnings) = **\$1.75**.

**Example 2:** A player pays \$3 to roll a fair die. If a 6 is rolled, the player receives \$k (the \$3 is not returned). Otherwise, the player receives nothing. Find k so that the game is fair.

**Solution**:

| Profit x  | k − 3 | −3  |
| --------- | ----- | --- |
| Pr(X = x) | 1/6   | 5/6 |

$$E(X)=(k-3)\times\frac{1}{6}+(-3)\times\frac{5}{6}=0$$
$$\frac{k-3-15}{6}=0\implies k=18$$

So the prize should be **\$18**.
*Check with the shortcut: E(winnings) = 18 × 1/6 = \$3 = cost ✓*

**Example 3:** A raffle sells 500 tickets at \$5 each. There is one first prize of \$1000, two second prizes of \$200, and five third prizes of \$50. Find the expected profit for a person who buys one ticket.

**Solution**:

| Winnings w | \$1000 | \$200  | \$50   | \$0      |
| ---------- | ----- | ----- | ----- | ------- |
| Pr(W = w)  | 1/500 | 2/500 | 5/500 | 492/500 |

$$E(W)=\frac{1000\times1+200\times2+50\times5}{500}=\frac{1650}{500}=\$3.30$$
$$E(\text{profit})=3.30-5=-\$1.70$$

On average, each ticket loses \$1.70. *Check: the organiser collects 500 × \$5 = \$2500 and pays out \$1650 in prizes, keeping \$850 = 500 × \$1.70 ✓*

**Example 4:** In a game, a player pays \$1 and spins a spinner that lands on red with probability 0.2, blue with probability 0.3 and white with probability 0.5. Red pays \$3, blue pays \$1, and white pays nothing (the \$1 is not returned). Is the game fair? If not, who does it favour?

**Solution**:
$$E(W)=3(0.2)+1(0.3)+0(0.5)=0.9$$
$$E(\text{profit})=0.9-1=-\$0.10$$
Not fair: it favours the **organiser**, who expects to gain 10 cents per game.

---

## Exercises:

*Try each question first, then click on "Solution" to check your answer.*

**Question 1:** It costs \$1 to play a game. Two fair dice are rolled. If the sum is 7, the player receives \$5 (the \$1 is not returned); otherwise, the player receives nothing.
**a)** Find the expected profit.
**b)** How much should the player receive for a sum of 7 to make the game fair?

> [!success]- Solution
> There are 6 ways to make a sum of 7 out of 36: (1,6), (2,5), (3,4), (4,3), (5,2), (6,1), so Pr(sum = 7) = 1/6.
>
> **a)**
> $$E(\text{profit})=(5-1)\times\frac{1}{6}+(-1)\times\frac{5}{6}=\frac{4-5}{6}=-\frac{1}{6}\approx-\$0.17$$
>
> **b)** Let the prize be \$k. Fair price = E(winnings):
> $$k\times\frac{1}{6}=1\implies k=\$6$$

**Question 2:** A game costs \$2. A card is drawn from a standard deck of 52 cards. If it's an ace, the player wins \$10 **and gets the \$2 back**. If it's a picture card (J, Q or K), the player gets the \$2 back. Otherwise, the player loses the \$2. Find the expected profit.

> [!success]- Solution
> The stake is returned for aces and picture cards, so the profits are:
>
> | Card      | Ace   | Picture card | Other |
> | --------- | ----- | ------------ | ----- |
> | Profit x  | \$10   | \$0           | −\$2   |
> | Pr(X = x) | 4/52  | 12/52        | 36/52 |
>
> $$E(X)=10\times\frac{4}{52}+0\times\frac{12}{52}+(-2)\times\frac{36}{52}=\frac{40-72}{52}=-\frac{32}{52}=-\frac{8}{13}\approx-\$0.62$$

**Question 3:** A spinner lands on red with probability 0.1, blue with probability 0.3 and white with probability 0.6. It costs \$2 to spin. Red pays \$x, blue pays \$3, and white pays nothing (the \$2 is not returned). Find x so that the game is fair.

> [!success]- Solution
> Fair ⟺ E(winnings) = cost:
> $$0.1x+3(0.3)+0(0.6)=2\implies0.1x+0.9=2\implies x=11$$
> Red should pay **\$11**.

**Question 4:** A player plays the game in Example 1 (cost \$2) 200 times. How much money should the player expect to win or lose overall?

> [!success]- Solution
> E(profit) per game = −\$0.25, so over 200 games:
> $$200\times(-0.25)=-\$50$$
> The player should expect to **lose about \$50**.

**Question 5:** Game A: you win \$1 or lose \$1, each with probability 1/2. Game B: you win \$9 with probability 1/10, or lose \$1 with probability 9/10.
**a)** Show that both games are fair.
**b)** Which game is riskier? Use the variance to explain.

> [!success]- Solution
> **a)**
> $$E(A)=1\times\frac{1}{2}+(-1)\times\frac{1}{2}=0,\qquad E(B)=9\times\frac{1}{10}+(-1)\times\frac{9}{10}=0$$
> Both have E(profit) = 0, so both are fair.
>
> **b)** Since both means are 0, Var = E(X²) − 0²:
> $$\operatorname{Var}(A)=1^2\times\frac{1}{2}+(-1)^2\times\frac{1}{2}=1$$
> $$\operatorname{Var}(B)=9^2\times\frac{1}{10}+(-1)^2\times\frac{9}{10}=8.1+0.9=9$$
> Game B has a much larger variance (SD = \$3 instead of \$1), so it is riskier: you usually lose, but occasionally win big.

**Question 6:** A coin is tossed up to 3 times, stopping as soon as a head appears. The player receives \$2 if the first head is on toss 1, \$4 if it's on toss 2, \$8 if it's on toss 3, and nothing if all 3 tosses are tails. What is the fair price to play?

> [!success]- Solution
> $$E(W)=2\times\frac{1}{2}+4\times\frac{1}{4}+8\times\frac{1}{8}+0\times\frac{1}{8}=1+1+1=\$3$$
> Fair price = **\$3**.
>
> *Each extra toss adds another \$1 to the fair price. If the game had no limit on the number of tosses, the fair price would be infinite: this is the St Petersburg paradox from [[4 - Expectation]].*
