
## Average value
$$f_{avg}=\frac{1}{b-a}\int_a^b f(x)\,dx$$

**a)** $f(x)=\dfrac{1}{1-x}$ on $[-3,-2]$
$$f_{avg}=\frac{1}{-2+3}\int_{-3}^{-2}\frac{1}{1-x}\,dx=-\ln3+\ln4=\ln\frac43$$

**Ex 1** Drug in bloodstream: $A=2e^{-0.1t}$ mg
- **a)** Initial dose ($t=0$): $A=2e^0=2$ mg
- **b)** Average over first 2 hours:
$$f_{avg}=\frac{1}{2-0}\int_0^2 2e^{-0.1t}\,dt=\frac12\times3.625\approx1.81\text{ mg}$$

![[Average Value - Drug Concentration.png]]

## Kinematics
$$a=\frac{dv}{dt}\Rightarrow v=\int a\,dt,\qquad v=\frac{ds}{dt}\Rightarrow s=\int v\,dt$$

**Ex 2** $a=6t+8$, $v=0$ and $s=3$ when $t=0$
$$v=3t^2+8t+c,\ c=0\Rightarrow v=3t^2+8t$$
$$s=t^3+4t^2+c,\ c=3\Rightarrow s=t^3+4t^2+3$$

**Ex 3** $v(t)=4e^{2t}+2$, $s=8$ when $t=0$
$$s=\int(4e^{2t}+2)\,dt=2e^{2t}+2t+c,\quad 2+c=8\Rightarrow c=6$$
$$\therefore s=2e^{2t}+2t+6$$

## Rates of change
**Ex 4** Diving board deflection: $\dfrac{dy}{dx}=-0.03(x+1)^2+0.03$
- **a)** At the fixed end $x=0$: $y=0$
- **b)**
$$y=\int\left(-0.03(x+1)^2+0.03\right)dx=-0.01(x+1)^3+0.03x+c$$
$$x=0,\ y=0\Rightarrow-0.01+c=0\Rightarrow c=0.01$$
$$\therefore y=-0.01(x+1)^3+0.03x+0.01$$

**Ex 5** Spectators: $\dfrac{dr}{dt}=1375t^2-t^3$, $0\le t\le1.5$, $r(0)=0$
$$r=\frac{1375t^3}{3}-\frac{t^4}{4}+c,\quad c=0$$
$$r(1.5)=\frac{1375}{3}(1.5)^3-\frac{(1.5)^4}{4}\approx1546\text{ spectators}$$

**Ex 6** $r'(t)=-133\left(1-\dfrac{t}{60}\right)$, $r(0)=4000$
$$r(t)=-133t+\frac{133t^2}{120}+4000$$
$$r(20)=-2660+\frac{133\times400}{120}+4000\approx1783$$

---
