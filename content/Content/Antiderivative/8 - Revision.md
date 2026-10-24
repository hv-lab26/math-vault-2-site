
## Section A: Indefinite integrals (basic)
1. $\int(6x^5-4x^2+3)\,dx=x^6-\frac43x^3+3x+c$
2. $\int\left(\frac5{x^3}+2\sqrt x\right)dx=-\frac52x^{-2}+\frac43x^{3/2}+c$
3. $\int(4\sin x-3\cos x)\,dx=-4\cos x-3\sin x+c$
4. $\int(3e^x-2e^{2x})\,dx=3e^x-e^{2x}+c$
5. $\int\left(\frac3x+\frac2{x^2}\right)dx=3\ln|x|-2x^{-1}+c$

## Section B: $(ax+b)$ form
6. $\int(3x+2)^4\,dx=\frac{(3x+2)^5}{15}+c$
7. $\int(5x-1)^3\,dx=\frac{(5x-1)^4}{20}+c$
8. $\int\frac1{4x+3}\,dx=\frac14\ln|4x+3|+c$
9. $\int e^{2x-5}\,dx=\frac12e^{2x-5}+c$
10. $\int\sin(3x+1)\,dx=-\frac13\cos(3x+1)+c$


## Section C: Definite integrals
11. $\int_0^2(3x^2+1)\,dx=\big[x^3+x\big]_0^2=10$
12. $\int_1^3(2x^3-4x)\,dx=\left[\frac{x^4}2-2x^2\right]_1^3=\frac{45}2+\frac32=24$
13. $\int_0^\pi\sin x\,dx=\big[-\cos x\big]_0^\pi=2$
14. $\int_0^1e^x\,dx=e-1$
15. $\int_1^3\frac1x\,dx=\ln3$
16. $\int_0^2(2x+1)^3\,dx=\left[\frac{(2x+1)^4}8\right]_0^2=78$

## Mixed
17. $\int\left(2x^3+\frac4x-5\sin x+e^x\right)dx=\frac{x^4}2+4\ln|x|+5\cos x+e^x+c$
18. $\int\left[(2x+1)^3+e^{x-2}\right]dx=\frac{(2x+1)^4}8+e^{x-2}+c$
19. $\int\left(\frac3{2x+5}-\cos4x\right)dx=\frac32\ln|2x+5|-\frac14\sin4x+c$

## Q20: Trapezium rule
$\int_0^4(x^2+2x+1)\,dx$ with 4 intervals ($h=1$)
- **(i)** $A\approx\frac12\times1\times(1+2\times4+2\times9+2\times16+25)=42$
- **(ii)** Exact: $\left[\frac{(x+1)^3}3\right]_0^4=\frac{124}3=41\tfrac13$
- **(iii)** Overestimate, since $42>41\frac13$. The curve is concave up, so each trapezium's top edge sits above the curve.

See [[7 - Trapezium Rule]].

## Q21:
$f'(x)=3x^2-4x+1$, passes through $(2,5)$
$$f(x)=x^3-2x^2+x+c,\quad 8-8+2+c=5\Rightarrow c=3$$
$$\therefore f(x)=x^3-2x^2+x+3$$

---
