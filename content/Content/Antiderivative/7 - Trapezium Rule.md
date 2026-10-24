See also: [[5 - Area Under Graph]]

Integration = finding the area under a curve, e.g. $\int_1^2x^2\,dx=\frac73$.
The trapezium rule **approximates** this area with trapeziums.

Single trapezium: $A=\frac12(b_1+b_2)\,h$

## Formula
$$A\approx\frac{h}{2}\Big[f(x_0)+2f(x_1)+2f(x_2)+\dots+2f(x_{n-1})+f(x_n)\Big],\qquad h=\frac{b-a}{n}$$
$n$ = number of trapeziums. First and last heights once, all middle heights twice.

> [!tip] Over or under?
> Curve **concave up** (bends upward, e.g. $x^2$) -> **overestimate**.
> Curve **concave down** -> **underestimate**.

## Example: $y=x^2+2$ from $x=1$ to $x=3$
**1 trapezium** ($h=2$): $f(1)=3,\ f(3)=11$
$$A=\tfrac12\times2\times(3+11)=14$$

**2 trapeziums** ($h=1$): $f(2)=6$
$$T_1=\tfrac12(3+6)=\tfrac92,\quad T_2=\tfrac12(6+11)=\tfrac{17}2,\quad A=13$$

**4 trapeziums** ($h=\frac12$): $f(1.5)=4.25,\ f(2.5)=8.25$
$$A=\frac{29}{16}+\frac{41}{16}+\frac{57}{16}+\frac{77}{16}=\frac{51}{4}=12.75$$

![[Trapezium Rule - Example.png]]

More trapeziums → closer to the exact value.

## $y=x^3$ from $2$ to $3$, 4 trapeziums
$h=\frac14$
$$A=\frac12\times\frac14\left(8+2(2.25^3)+2(2.5^3)+2(2.75^3)+27\right)=16.328125$$

## Ex 15: $y=\frac1x$ from $0.5$ to $2.5$
**a)** $h=1$
$$A=\frac12\times1\times\left(2+2\times\frac23+\frac25\right)=\frac{28}{15}$$

## Table-data example
$h=20$, heights $0,30,20,40,60,50$
$$A=\frac12\times20\times(0+2\times30+2\times20+2\times40+2\times60+50)=3500\text{ m}^2$$

---
## Review
**Q5** $f(x)=x^2$, $h=1$: $A=\frac12(1+2\times4+9)=9$

**Q6**
- **a)** $A=\frac12\times2\times(3+5)=8$
- **b)** $A=\frac12\times2\times(2+2\times3+5)=13$

**Q10**
- **a)** $A=\frac12\times1\times(10+2\times14+2\times15+13)=\frac{81}{2}$
- **b)** $f(x)=-x^2+6x-5$: $A=\frac12(0+2\times3+2\times4+2\times3+0)=10$
- **c)** $f(x)=\frac12x^3$: $A=\frac12\left(0+1+2\times4+\frac{27}{2}\right)=\frac{45}{4}$
- **d)** $f(x)=10-x^2$ on $[-1,1]$, $h=\frac12$: $A=\frac14(9+2\times9.75+2\times10+2\times9.75+9)=\frac{77}{4}$
- **e)** $f(x)=e^x$ on $[0,3]$: $A=\frac12(1+2e+2e^2+e^3)$

---
