# Area Under Graph
Up: [[Content/Antiderivative/1 - Overview]] · Prereq: [[3 - Definite Integrals]]

## Cases
**Above the $x$-axis**
$$A=\int_a^b f(x)\,dx$$

**Below the $x$-axis** (integral is negative)
$$A=-\int_a^b f(x)\,dx=\left|\int_a^b f(x)\,dx\right|$$

**One part below, one above** — split at the root $c$:
$$A_1=\int_c^b f(x)\,dx,\qquad A_2=-\int_a^c f(x)\,dx,\qquad A=A_1+A_2$$

> [!tip]
> Always find the $x$-intercepts first. Integrating straight across a root lets the positive and negative parts cancel.

## Examples
**Q1** $y=\dfrac1x$ from $1$ to $4$
$$A=\int_1^4\frac1x\,dx=\big[\ln|x|\big]_1^4=\ln4\text{ units}^2$$

![[Area Under Graph - Q1.png]]

**Q2** $y=x^2-4x$ from $1$ to $3$ (below axis)
$$A=\left|\int_1^3(x^2-4x)\,dx\right|=\frac{22}{3}=7\tfrac13\text{ units}^2$$

![[Area Under Graph - Q2.png]]

**Q3** $y=x^3-4x$ from $-2$ to $2$ (roots at $-2,0,2$)
$$A_1=\int_{-2}^{0}(x^3-4x)\,dx=4,\qquad A_2=\left|\int_0^2(x^3-4x)\,dx\right|=4$$
$$A=4+4=8\text{ units}^2$$

![[Area Under Graph - Q3.png]]

---
