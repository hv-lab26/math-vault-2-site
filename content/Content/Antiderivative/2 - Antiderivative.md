
## Rules
$$\int x^n\,dx=\frac{x^{n+1}}{n+1}+c,\quad n\mathrel{\char"2260}-1$$
$$\int (ax+b)^n\,dx=\frac{(ax+b)^{n+1}}{a(n+1)}+c$$

When $n=-1$:
$$\int\frac{1}{x}\,dx=\int x^{-1}\,dx=\ln|x|+c$$
$$\int\frac{1}{ax+b}\,dx=\frac{1}{a}\ln|ax+b|+c$$

Constant $g$:
$$\int g\,dx=gx+c$$

## Worked examples
**a)** $\displaystyle\int x^5\,dx=\frac{x^6}{6}+c$

**b)** $\displaystyle\int 3x^5\,dx=3\cdot\frac{x^6}{6}+c=\frac{x^6}{2}+c$

**c)** $\displaystyle\int (3x)^5\,dx=\frac{(3x)^6}{3\times6}+c=\frac{(3x)^6}{18}+c$

**d)** $\displaystyle\int\sqrt{x}\,dx=\int x^{1/2}\,dx=\frac{x^{3/2}}{3/2}+c=\frac{2x^{3/2}}{3}+c$

**e)** $\displaystyle\int\frac{1}{\sqrt{3x-5}}\,dx=\int(3x-5)^{-1/2}\,dx=\frac{2(3x-5)^{1/2}}{3}+c$

**f)** $\displaystyle\int\frac{1}{x^5}\,dx=\int x^{-5}\,dx=\frac{x^{-4}}{-4}+c=-\frac{1}{4x^4}+c$

**g)** $\displaystyle\int(x+3)(x-2)\,dx=\int(x^2+x-6)\,dx=\frac{x^3}{3}+\frac{x^2}{2}-6x+c$

## Finding $f(x)$ from $f'(x)$
**Q1** $f'(x)=2x$, curve passes through $(-1,4)$
$$f(x)=x^2+c,\quad 4=(-1)^2+c\Rightarrow c=3$$
$$\therefore f(x)=x^2+3$$

![[Antiderivative - Family of Curves.png]]

**Q2** $f'(x)=x^3+4x^2$, $f(0)=0$
$$f(x)=\frac{x^4}{4}+\frac{4x^3}{3}+c,\quad c=0$$

**Q3**
$$\int\frac{x^2+5x}{x^4}\,dx=\int(x^{-2}+5x^{-3})\,dx=\frac{x^{-1}}{-1}+\frac{5x^{-2}}{-2}+c=-\frac{1}{x}-\frac{5}{2x^2}+c$$

**Q4**
$$\int\frac{2}{3x-5}\,dx=\frac{2}{3}\ln|3x-5|+c$$

**Ex** $f'(x)=\dfrac{3}{x}$, $y=10$ when $x=1$
$$f(x)=3\ln|x|+c,\quad 3\ln1+c=10\Rightarrow c=10$$
$$\therefore y=3\ln|x|+10$$

---
## Review
### Q1
- **a)** $\int x\,dx=\dfrac{x^2}{2}+c$
- **f)** $\int -2x^4\,dx=-\dfrac{2x^5}{5}+c$
- **k)** $\int\dfrac{x^{-4}}{3}\,dx=\dfrac13\cdot\dfrac{x^{-3}}{-3}+c=-\dfrac{1}{9x^3}+c$
- **p)** $\int\dfrac{5}{x^3}\,dx=5\cdot\dfrac{x^{-2}}{-2}+c=-\dfrac{5}{2x^2}+c$

### Q2
- **a)** $\int(2x+5)\,dx=\dfrac{(2x+5)^2}{4}+c$
- **c)** $\int(10x^4+6x^3+2)\,dx=2x^5+\dfrac{3x^4}{2}+2x+c$
- **e)** $\int(x^3-x^2+12)\,dx=\dfrac{x^4}{4}-\dfrac{x^3}{3}+12x+c$
- **g)** $\int5(x^2+2x-1)\,dx=\dfrac{5x^3}{3}+5x^2-5x+c$
- **i)** $\int x(x-1)(x-4)\,dx=\int(x^3-5x^2+4x)\,dx=\dfrac{x^4}{4}-\dfrac{5x^3}{3}+2x^2+c$

### Q5
- **a)** $\int(x+3)^2\,dx=\dfrac{(x+3)^3}{3}+c$
- **e)** $\int(6x+5)^4\,dx=\dfrac{(6x+5)^5}{30}+c$
- **i)** $\int4(8-3x)^4\,dx=-\dfrac{4(8-3x)^5}{15}+c$
- **m)** $\int6(4x-7)^{-4}\,dx=\dfrac{6(4x-7)^{-3}}{4\cdot(-3)}+c=-\dfrac{(4x-7)^{-3}}{2}+c$

### Q7
- **a)** $\int\dfrac{3}{x}\,dx=3\ln|x|+c$
- **d)** $\int\dfrac{7}{3x}\,dx=\dfrac73\ln|x|+c$
- **g)** $\int\dfrac{3}{x+3}\,dx=3\ln|x+3|+c$
- **j)** $\int\dfrac{4}{3x+2}\,dx=\dfrac43\ln|3x+2|+c$
- **m)** $\int\dfrac{-5}{3+2x}\,dx=-\dfrac52\ln|2x+3|+c$
- **p)** $\int\dfrac{3}{6-11x}\,dx=-\dfrac{3}{11}\ln|6-11x|+c$


### Q9
$$\int\frac{2x+7}{x}\,dx=\int\left(2+\frac7x\right)dx=2x+7\ln|x|+c$$

### Q10
- **a)** $\int\left(x^4+2x+\dfrac1x\right)dx=\dfrac{x^5}{5}+x^2+\ln|x|+c$
- **d)** $\int\dfrac{3}{2x+1}\,dx=\dfrac32\ln|2x+1|+c$
- **g)** $\int3(4x+1)^{-3}\,dx=-\dfrac{3(4x+1)^{-2}}{8}+c$
- **j)** $\int\left(\sqrt x+\dfrac{2}{3-x}\right)dx=\dfrac{2x^{3/2}}{3}-2\ln|3-x|+c$
- **m)** $\displaystyle\int\frac{x^2+2x-1}{\sqrt x}\,dx=\int\left(x^{3/2}+2x^{1/2}-x^{-1/2}\right)dx=\frac{2x^{5/2}}{5}+\frac{4x^{3/2}}{3}-2x^{1/2}+c$


### Q11
**a)** $f'(x)=4x+1$, through $(0,2)$ → $f(x)=2x^2+x+2$

**b)** $f'(x)=5-2x$, through $(1,-1)$ → $5-1+c=-1\Rightarrow c=-5$ → $f(x)=5x-x^2-5$

**g)** $f'(x)=(x+4)^3$, through $(-2,5)$
$$f(x)=\frac{(x+4)^4}{4}+c,\quad \frac{2^4}{4}+c=5\Rightarrow c=1$$
$$\therefore f(x)=\frac{(x+4)^4}{4}+1$$

**j)** $f'(x)=\dfrac{8}{7-2x}$, $f(3)=7$
$$f(x)=-4\ln|7-2x|+c,\quad -4\ln1+c=7\Rightarrow c=7$$
$$\therefore f(x)=-4\ln|7-2x|+7$$
---
