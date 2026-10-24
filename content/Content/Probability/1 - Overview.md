## Notes
1. [[2 - Language of Probability in Mathematics]] - Pr(A), complements, ∩ and ∪
2. [[3 - Laws of Probability]] - addition rule, mutually exclusive and independent events
3. [[4 - Venn Diagram]] - events as overlapping circles
4. [[5 - Tree Diagram]] - multi-stage experiments, with / without replacement, conditional probability
5. [[6 - Karnaugh Diagram (Probability Table)]] - two-way tables, "and / or / given"
6. [[7 - Permutation]] - arrangements (order matters), $n!$, ${}^{n}P_{r}$
7. [[8 - Combinations]] - selections (order doesn't matter), ${}^{n}C_{r}$
8. [[9 - Revision]] - advanced and tricky mixed practice

## Formula sheet
| Rule                     | Formula                                                                          |
| ------------------------ | -------------------------------------------------------------------------------- |
| Range                    | $0\le\Pr(A)\le1$                                                                 |
| Equally likely outcomes  | $\Pr(A)=\dfrac{\text{number of outcomes in }A}{\text{total number of outcomes}}$ |
| Complement               | $\Pr(A')=1-\Pr(A)$                                                               |
| Addition rule            | $\Pr(A\cup B)=\Pr(A)+\Pr(B)-\Pr(A\cap B)$                                        |
| Mutually exclusive       | $\Pr(A\cap B)=0$, so $\Pr(A\cup B)=\Pr(A)+\Pr(B)$                                |
| Conditional probability  | $\Pr(A\mid B)=\dfrac{\Pr(A\cap B)}{\Pr(B)}$                                      |
| Multiplication rule      | $\Pr(A\cap B)=\Pr(A)\times\Pr(B\mid A)$                                          |
| Independent events       | $\Pr(A\cap B)=\Pr(A)\times\Pr(B)$, i.e. $\Pr(B\mid A)=\Pr(B)$                    |
| Total probability (tree) | $\Pr(B)=\Pr(A)\Pr(B\mid A)+\Pr(A')\Pr(B\mid A')$                                 |
| "At least one"           | $1-\Pr(\text{none})$                                                             |
| Factorial                | $n!=n(n-1)(n-2)\cdots2\times1,\ 0!=1$                                            |
| Permutations             | ${}^{n}P_{r}=\dfrac{n!}{(n-r)!}$                                                 |
| Identical objects        | $\dfrac{n!}{a!\,b!\cdots}$                                                       |
| Combinations             | ${}^{n}C_{r}=\dbinom{n}{r}=\dfrac{n!}{r!\,(n-r)!}$                               |

## Which method?
| The question...                                         | Use                                                                  |
| ------------------------------------------------------- | -------------------------------------------------------------------- |
| has 2 events and asks about "only", "neither" or "both" | [[6 - Karnaugh Diagram (Probability Table)]] or [[4 - Venn Diagram]] |
| has 3 events                                            | [[4 - Venn Diagram]]                                                 |
| happens in stages, or says "without replacement"        | [[5 - Tree Diagram]]                                                 |
| asks you to arrange, order or line up                   | [[7 - Permutation]]                                                  |
| asks you to choose, select or pick a group              | [[8 - Combinations]]                                                 |
| says "at least one"                                     | the complement: 1 - Pr(none)                                         |

## Key words
| Word           | Symbol | What to do                                      |
| -------------- | ------ | ----------------------------------------------- |
| "and", "both"  | ∩      | multiply along the branches, or read one cell   |
| "or", "either" | ∪      | add, then take away the overlap                 |
| "not"          | A'     | 1 - Pr(A)                                       |
| "given", "if"  | \|     | divide by the probability of what you are given |
| "at least one" |        | 1 - Pr(none)                                    |
| "arrange"      | ⁿPᵣ    | order matters                                   |
| "choose"       | ⁿCᵣ    | order doesn't matter                            |
