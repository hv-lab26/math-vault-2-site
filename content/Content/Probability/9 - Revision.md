Up: [[Content/Probability/1 - Overview]]

*Advanced and tricky questions that mix everything in the Probability notes. Try each question properly before you open the solution. Most of them hide a trap, and the solution explains it.*

> [!tip] How to attack a tricky question
> 1. **Name your events** with letters first (e.g. L = late).
> 2. **Pick the tool:** Venn or Karnaugh diagram for overlaps, a tree diagram for stages, permutations or combinations for counting.
> 3. **Look for the complement:** "at least one" -> 1 - Pr(none).
> 4. **Check your answer:** every probability is between 0 and 1, and the branches, rows and columns add up correctly.

## Section A: Laws of probability & Venn diagrams

**Question 1:** In a class of 40 students, 22 study Maths (M), 18 study Physics (P) and 15 study Chemistry (C). 9 study both Maths and Physics, 7 study both Maths and Chemistry, 6 study both Physics and Chemistry, and 4 study all three.
**a)** Draw a Venn diagram.
**b)** How many students study none of the three subjects?
**c)** A student is chosen at random. Find Pr(the student studies exactly one subject).
**d)** Given that a student studies exactly two subjects, find Pr(one of them is Physics).

> [!success]- Solution
> **a)** Fill the centre first (4), then the "two subjects only" regions, then the "one subject only" regions:
> - M ∩ P only: 9 − 4 = 5, M ∩ C only: 7 − 4 = 3, P ∩ C only: 6 − 4 = 2
> - M only: 22 − 5 − 3 − 4 = 10, P only: 18 − 5 − 2 − 4 = 7, C only: 15 − 3 − 2 − 4 = 6
>
> ![[Probability Revision - Three-Set Venn.png]]
>
> **b)** Students in at least one circle: 10 + 7 + 6 + 5 + 3 + 2 + 4 = 37, so 40 − 37 = **3** students study none.
>
> **c)**
> $$\Pr(\text{exactly one})=\frac{10+7+6}{40}=\frac{23}{40}$$
>
> **d)** Exactly two subjects: 5 + 3 + 2 = 10 students. Of these, 5 + 2 = 7 study Physics.
> $$\Pr(\text{Physics}\mid\text{exactly two})=\frac{7}{10}$$
>
> *Trap: writing 9 in the M ∩ P region. 4 of those 9 students also study Chemistry, so they belong in the centre.*

**Question 2:** Pr(A) = 0.6 and Pr(B) = 0.5.
**a)** Find the largest and the smallest possible values of Pr(A ∩ B).
**b)** Find Pr(A ∪ B) if A and B are independent.

> [!success]- Solution
> **a)** **Largest:** A ∩ B is inside both A and B, so it can't be bigger than the smaller of the two:
> $$\Pr(A\cap B)\le\Pr(B)=0.5$$
> (This happens when B is completely inside A.)
>
> **Smallest:** Pr(A ∪ B) can't be more than 1, so by the addition rule:
> $$\Pr(A\cap B)=\Pr(A)+\Pr(B)-\Pr(A\cup B)\ge0.6+0.5-1=0.1$$
> So $0.1\le\Pr(A\cap B)\le0.5$.
>
> **b)**
> $$\Pr(A\cup B)=0.6+0.5-0.6\times0.5=0.8$$
>
> *Trap: saying the smallest value is 0. A and B can't be mutually exclusive here, because 0.6 + 0.5 = 1.1 > 1.*

**Question 3:** Pr(A) = 0.3 and Pr(B) = 0.4. Find Pr(A ∪ B) if:
**a)** A and B are mutually exclusive.
**b)** A and B are independent.
**c)** A is a subset of B (whenever A happens, B happens too).

> [!success]- Solution
> **a)** $\Pr(A\cup B)=0.3+0.4=0.7$
>
> **b)** $\Pr(A\cup B)=0.3+0.4-0.3\times0.4=0.58$
>
> **c)** A is inside B, so A ∪ B is just B: $\Pr(A\cup B)=\Pr(B)=0.4$
>
> *Same two numbers, three different answers: always check how the events are related before you use a formula.*

**Question 4:**
**a)** A fair coin has landed on heads 5 times in a row. Find Pr(the next toss is heads).
**b)** Two fair dice are rolled. Find Pr(at least one 6).
**c)** A family has two children, and you are told that at least one of them is a boy. Find Pr(both are boys).

> [!success]- Solution
> **a)** $\dfrac{1}{2}$. The coin has no memory: every toss is independent.
>
> **b)** Not $\dfrac{1}{6}+\dfrac{1}{6}=\dfrac{1}{3}$, because that counts (6, 6) twice!
> $$\Pr(\text{at least one 6})=1-\left(\frac{5}{6}\right)^2=\frac{11}{36}$$
>
> **c)** Not $\dfrac{1}{2}$! The equally likely families are BB, BG, GB and GG. "At least one boy" removes GG, leaving BB, BG and GB:
> $$\Pr(\text{both boys}\mid\text{at least one boy})=\frac{1}{3}$$
> *This one is known as the Boy or Girl paradox, and people still argue about it!*

> [!info] Fun fact: the gambler's fallacy
> Believing that "tails is due" after a run of heads is called the **gambler's fallacy**. At the Monte Carlo Casino in 1913, a roulette ball landed on black 26 times in a row, and gamblers lost millions betting on red, sure that red "had to" come up next :D.

## Section B: Tree diagrams & conditional probability

**Question 5:** 1 in 200 people have a rare condition (D). A test is positive (+) for 98% of people who have the condition, and for 3% of people who don't.
**a)** Find Pr(+).
**b)** A person tests positive. Find Pr(D | +).
**c)** The person takes the test again and is positive a second time. Assuming the two results are independent once you know whether the person has the condition, find the new probability that they have it.

> [!success]- Solution
> **a)**
> $$\Pr(+)=0.005\times0.98+0.995\times0.03=0.0049+0.02985=0.03475$$
>
> **b)**
> $$\Pr(D\mid +)=\frac{0.0049}{0.03475}\approx0.141$$
> Only about 14%, even though the test is "98% accurate"!
>
> **c)** Extend the tree with a second test. Two positive results:
> $$\Pr(D\cap{+}{+})=0.005\times0.98^2=0.004802\qquad\Pr(D'\cap{+}{+})=0.995\times0.03^2=0.0008955$$
> $$\Pr(D\mid{+}{+})=\frac{0.004802}{0.004802+0.0008955}\approx0.843$$
> A second positive test raises the chance from about 14% to about 84%.
>
> *Trap: answering 0.98 in part b). That is Pr(+ | D), the reverse of what was asked.*

**Question 6:** Ana and Ben play a best-of-five tennis match: the first player to win 3 sets wins the match. Ana wins any set with probability 0.6, independently of the other sets.
**a)** Find Pr(Ana wins in exactly 3 sets).
**b)** Find Pr(Ana wins in exactly 4 sets).
**c)** Find Pr(Ana wins the match).

> [!success]- Solution
> The full tree is huge, so think about the paths instead. **Ana must win the last set played**, so only her other wins can be anywhere.
>
> **a)** AAA:
> $$0.6^3=0.216$$
>
> **b)** Ana wins 2 of the first 3 sets (${}^{3}C_{2}=3$ ways: AAB, ABA, BAA), then wins set 4:
> $${}^{3}C_{2}\times0.6^3\times0.4=3\times0.216\times0.4=0.2592$$
>
> **c)** Add winning in exactly 5 sets: 2 wins in the first 4 sets (${}^{4}C_{2}=6$ ways), then she wins set 5:
> $${}^{4}C_{2}\times0.6^3\times0.4^2=6\times0.216\times0.16=0.20736$$
> $$\Pr(\text{Ana wins})=0.216+0.2592+0.20736=0.68256\approx0.683$$
>
> *Trap: using ⁴C₃ in part b). If Ana won all of the first 3 sets, the match would already be over, so the 4th set must be her 3rd win.*
> *Compare with [[5 - Tree Diagram]] Question 7: in a best-of-three, Ana wins with probability 0.648. Longer matches favour the stronger player!*

**Question 7:** A bag contains n balls: 3 are red and the rest are green. Two balls are taken out without replacement, and Pr(both are red) = 1/15.
**a)** Find n.
**b)** Find Pr(the two balls are different colours).

> [!success]- Solution
> **a)**
> $$\frac{3}{n}\times\frac{2}{n-1}=\frac{1}{15}\Rightarrow n(n-1)=90\Rightarrow n^2-n-90=0\Rightarrow(n-10)(n+9)=0$$
> So n = 10 (n = −9 is impossible).
>
> **b)** 3 red and 7 green:
> $$\Pr(RG)+\Pr(GR)=\frac{3}{10}\times\frac{7}{9}+\frac{7}{10}\times\frac{3}{9}=\frac{21}{90}+\frac{21}{90}=\frac{7}{15}$$
>
> *Trap: writing $\dfrac{3}{n}\times\dfrac{2}{n}$. Without replacement, there is one ball fewer on the 2nd draw.*

**Question 8:** Box A contains 2 white and 3 black balls. Box B contains 4 white and 1 black ball. A fair die is rolled: if it shows 1 or 2, a ball is taken from Box A, otherwise from Box B.
**a)** Find Pr(the ball is white).
**b)** Given that the ball is white, find Pr(it came from Box A).
**c)** Are the events "Box A is used" and "the ball is white" independent?

> [!success]- Solution
> ![[Probability Revision - Two Boxes.png]]
>
> **a)**
> $$\Pr(W)=\frac{1}{3}\times\frac{2}{5}+\frac{2}{3}\times\frac{4}{5}=\frac{2}{15}+\frac{8}{15}=\frac{2}{3}$$
>
> **b)**
> $$\Pr(A\mid W)=\frac{\Pr(A\cap W)}{\Pr(W)}=\frac{2/15}{2/3}=\frac{1}{5}$$
>
> **c)** $\Pr(A)\times\Pr(W)=\dfrac{1}{3}\times\dfrac{2}{3}=\dfrac{2}{9}\mathrel{\char"2260}\dfrac{2}{15}=\Pr(A\cap W)$, so they are **not independent**.
> *This makes sense: a white ball makes Box B (the "whiter" box) more likely.*

## Section C: Karnaugh diagrams & independence

**Question 9:** A and B are independent events with Pr(A) = Pr(B) and Pr(A' ∩ B') = 0.36.
**a)** Find Pr(A).
**b)** Complete the Karnaugh diagram.
**c)** Find Pr(exactly one of A and B happens).

> [!success]- Solution
> **a)** Let Pr(A) = Pr(B) = p. A' and B' are also independent (see Question 11), so:
> $$(1-p)^2=0.36\Rightarrow1-p=0.6\Rightarrow p=0.4$$
> (1 − p = −0.6 would give p = 1.6, which is impossible.)
>
> **b)**
>
> |           | **B** | **B'** | **Total** |
> | --------- | ----- | ------ | --------- |
> | **A**     | 0.16  | 0.24   | 0.4       |
> | **A'**    | 0.24  | 0.36   | 0.6       |
> | **Total** | 0.4   | 0.6    | 1         |
>
> **c)**
> $$\Pr(A\cap B')+\Pr(A'\cap B)=0.24+0.24=0.48$$

**Question 10:** In a group of 60 people, 25 like tea (T) and 30 like coffee (C). The number of people who like neither is twice the number who like both.
**a)** How many people like both?
**b)** Complete a two-way table.
**c)** Find Pr(C | T).

> [!success]- Solution
> **a)** Let x people like both. Then 25 + 30 − x = 55 − x people like at least one, so 60 − (55 − x) = 5 + x like neither.
> $$5+x=2x\Rightarrow x=5$$
>
> **b)**
>
> |           | **C** | **C'** | **Total** |
> | --------- | ----- | ------ | --------- |
> | **T**     | 5     | 20     | 25        |
> | **T'**    | 25    | 10     | 35        |
> | **Total** | 30    | 30     | 60        |
>
> **c)** Stay inside row T (25 people):
> $$\Pr(C\mid T)=\frac{5}{25}=\frac{1}{5}$$

**Question 11 (proof):** Show that if A and B are independent, then A and B' are also independent.

> [!success]- Solution
> Row A of the Karnaugh diagram gives $\Pr(A\cap B')=\Pr(A)-\Pr(A\cap B)$. Since A and B are independent:
> $$\Pr(A\cap B')=\Pr(A)-\Pr(A)\Pr(B)=\Pr(A)\big(1-\Pr(B)\big)=\Pr(A)\Pr(B')\quad\blacksquare$$
> This is exactly the rule for A and B' to be independent.
> *The same trick shows that A' and B, and A' and B', are independent too.*

## Section D: Permutations & combinations

**Question 12:** The letters of the word PROBABILITY are arranged in a row.
**a)** How many different arrangements are there?
**b)** In how many arrangements are the two B's next to each other?
**c)** In how many arrangements are the two I's NOT next to each other?
**d)** An arrangement is chosen at random. Find Pr(the two B's are next to each other).

> [!success]- Solution
> PROBABILITY has 11 letters, with two B's and two I's.
>
> **a)**
> $$\frac{11!}{2!\times2!}=9\,979\,200$$
>
> **b)** Glue BB into one block. The two B's are identical, so the block has only 1 order. That leaves 10 units, including two I's:
> $$\frac{10!}{2!}=1\,814\,400$$
>
> **c)** In the same way, the I's are together in $\dfrac{10!}{2!}=1\,814\,400$ arrangements, so
> $$9\,979\,200-1\,814\,400=8\,164\,800$$
>
> **d)**
> $$\frac{1\,814\,400}{9\,979\,200}=\frac{2}{11}$$
>
> *Trap: multiplying by 2! for the BB block. Swapping two identical B's doesn't make a new arrangement.*

**Question 13:** A committee of 4 is chosen from 5 married couples (10 people).
**a)** How many committees are possible?
**b)** How many committees contain no married couple?
**c)** A committee is chosen at random. Find Pr(it contains at least one married couple).

> [!success]- Solution
> **a)**
> $${}^{10}C_{4}=210$$
>
> **b)** Choose which 4 of the 5 couples are on the committee, then 1 person from each of those couples (2 ways each):
> $${}^{5}C_{4}\times2^4=5\times16=80$$
>
> **c)**
> $$1-\frac{80}{210}=\frac{130}{210}=\frac{13}{21}$$
>
> *Trap: answering 10 × 8 × 6 × 4 = 1920 in part b). That counts each committee in 4! different orders. Dividing by 4! gives 80 again.*

**Question 14:** How many 4-digit numbers have 4 different digits and are divisible by 5?

> [!success]- Solution
> A number divisible by 5 ends in 0 or 5. Split into cases, because 0 can't be the first digit:
> - **Ends in 0:** the 1st digit has 9 choices (1–9), then 8 and 7 choices: $9\times8\times7=504$
> - **Ends in 5:** the 1st digit has 8 choices (not 0, not 5), then 8 and 7 choices: $8\times8\times7=448$
>
> $$504+448=952$$
>
> *Trap: doing one calculation for both endings. The digit 0 behaves differently, so it needs its own case.*

**Question 15:** A box contains 5 red, 4 blue and 3 green pens. Three pens are chosen at random. Find the probability that:
**a)** the three pens are all different colours.
**b)** the three pens are all the same colour.
**c)** exactly two colours are chosen.

> [!success]- Solution
> Total number of selections: ${}^{12}C_{3}=220$
>
> **a)** 1 pen of each colour:
> $$\frac{5\times4\times3}{220}=\frac{60}{220}=\frac{3}{11}$$
>
> **b)**
> $$\frac{{}^{5}C_{3}+{}^{4}C_{3}+{}^{3}C_{3}}{220}=\frac{10+4+1}{220}=\frac{3}{44}$$
>
> **c)** Everything else:
> $$1-\frac{3}{11}-\frac{3}{44}=\frac{29}{44}$$

**Question 16:** 6 people, including Ann and Bob, line up in a row.
**a)** In how many arrangements is Ann somewhere to the left of Bob (not necessarily next to him)?
**b)** In how many arrangements is there exactly one person between Ann and Bob?

> [!success]- Solution
> **a)** Swapping Ann and Bob turns every "Ann on the left" arrangement into an "Ann on the right" one, so exactly half of all arrangements work:
> $$\frac{6!}{2}=360$$
>
> **b)** The seats for Ann and Bob can be (1, 3), (2, 4), (3, 5) or (4, 6): 4 pairs, × 2 for who takes the left seat, × 4! for the other 4 people:
> $$4\times2\times4!=192$$
>
> *Tip: symmetry arguments like part a) can save a lot of work.*

## Section E: Mixed challenge

**Question 17:** 4 people each choose a whole number from 1 to 10, at random and independently. Find the probability that at least two of them choose the same number.

> [!success]- Solution
> Complement: all 4 numbers are different.
> $$\Pr(\text{all different})=\frac{{}^{10}P_{4}}{10^4}=\frac{5040}{10\,000}=0.504$$
> $$\Pr(\text{at least two the same})=1-0.504=0.496$$
> *This is a mini version of the birthday problem in [[7 - Permutation]].*

**Question 18:** Two cards are drawn without replacement from a standard deck of 52 cards, which contains 4 aces. Find Pr(at least one ace) in two different ways:
**a)** using a tree diagram.
**b)** using combinations.

> [!success]- Solution
> **a)** Complement: no ace on either draw.
> $$1-\frac{48}{52}\times\frac{47}{51}=1-\frac{188}{221}=\frac{33}{221}$$
>
> **b)**
> $$1-\frac{{}^{48}C_{2}}{{}^{52}C_{2}}=1-\frac{1128}{1326}=\frac{33}{221}$$
>
> Same answer from two methods, so use whichever one is quicker for the question.

**Question 19:** Ann and Bob take turns to draw a ball, without replacement, from a bag containing 2 red and 3 blue balls. Ann goes first. The first person to draw a red ball wins. Find Pr(Ann wins).

> [!success]- Solution
> ![[Probability Revision - Red Ball Game.png]]
> Ann draws 1st and 3rd. The game can never reach a 5th draw, because there are only 3 blue balls.
> $$\Pr(\text{Ann wins})=\Pr(R)+\Pr(BBR)=\frac{2}{5}+\frac{1}{5}=\frac{3}{5}$$
>
> *Trap: assuming it's a 50/50 game. Going first is a real advantage here.*

**Question 20 (de Méré's problem):** A gambler offers two bets:
- **Bet 1:** roll one die 4 times, and win if at least one 6 appears.
- **Bet 2:** roll two dice 24 times, and win if at least one double six appears.

Find the probability of winning each bet. Which bet is better than 50/50?

> [!success]- Solution
> **Bet 1:**
> $$1-\left(\frac{5}{6}\right)^4\approx0.518$$
>
> **Bet 2:** Pr(double six) = 1/36 on each roll of two dice:
> $$1-\left(\frac{35}{36}\right)^{24}\approx0.491$$
>
> Only Bet 1 is better than 50/50, even though both bets "feel" the same: 4 × 1/6 = 24 × 1/36 = 2/3.
>
> *Trap: adding the probabilities (4 × 1/6). That only works for mutually exclusive events, and rolls are not. Use 1 − Pr(none).*

> [!info] Fun fact: the birth of probability
> This puzzle came from a French gambler, the Chevalier de Méré, who kept losing money on Bet 2. It was one of the problems that led Blaise Pascal and Pierre de Fermat to write letters to each other in 1654, and those letters are often called the birth of probability theory!
