# Massa di probabilità
$$\begin{flalign}P(x)=\begin{cases}
\frac{1}{2},&x=1 \\
\frac{1}{5},&x=2,3 \\
\frac{1}{10},&x=5 \\
0,&\text{elsewhere}
\end{cases} &&\end{flalign}$$
```desmos-graph
left=-0.5; right=5.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
(0,0)|blue
(1,1/2)|blue
(2,1/5)|blue
(3,1/5)|blue
(4,0)|blue
(5,1/10)|blue
```

$$\begin{flalign}F(x)=\begin{cases}
0,&x<1 \\
\frac{1}{2},&1\leq x<2 \\
\frac{7}{10},&2\leq x<3 \\
\frac{9}{10},&3\leq x<5 \\
1,&x\geq5
\end{cases} &&\end{flalign}$$
```desmos-graph
left=-0.5; right=5.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
y=0|x<1|green
(1,1/2)|green
y=1/2|1<=x<2|green
(2,7/10)|green
y=7/10|2<=x<3|green
(3,9/10)|green
y=9/10|3<=x<5|green
(5,1)|green
y=1|x>=5|green
```

# Densità di probabilità
$$\begin{flalign}f(x)=\begin{cases}
\frac{2}{3}e^{-2x/3},&x\geq0 \\
0,&x<0
\end{cases} &&\end{flalign}$$
```desmos-graph
left=-0.5; right=5.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
y=0|x<0|blue
y=(2/3)e^{-(2/3)x}|x>=0|blue
```
$$\begin{flalign}F(x)=\begin{cases}
-\frac{2}{3}e^{-2x/3}+\frac{2}{3},&x\geq0 \\
0,&x<0
\end{cases} &&\end{flalign}$$
```desmos-graph
left=-0.5; right=5.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
y=0|x<0|green
y=-(2/3)e^{-(2/3)x}+2/3|x>=0|green
```

# Funzione di ripartizione congiunta
$x_{1}=2,x_{2}=4,y_{1}=\frac{1}{2},y_{2}=1$
Domini di $P(x,y)$ o $f(x,y)$ sui quali vengono calcolati
$F(x_{2},y_{2})$:
```desmos-graph
left=-0.5; right=5.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
y<=1|x<=4|blue
x=4|y<=1|blue
```
$F(x_{1},y_{2})$:
```desmos-graph
left=-0.5; right=5.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
y<=1|x<=2|orange
x=2|y<=1|orange
```
$F(x_{2},y_{1})$:
```desmos-graph
left=-0.5; right=5.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
y<=1/2|x<=4|purple
x=4|y<=1/2|purple
```
<div class="page-break" style="page-break-before: always;"></div>

$F(x_{1},y_{1})$:
```desmos-graph
left=-0.5; right=5.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
y<=1/2|x<=2|red
x=2|y<=1/2|red
```
$\mathbb{P}((x_{1}<X\leq x_{2})\cap(y_{1}<Y\leq y_{2}))$:
```desmos-graph
left=-0.5; right=5.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
1/2<y<=1|2<x<=4|green
x=4|1/2<y<=1|green
x=2|1/2<y<=1|green|dashed
```

# Varianza
$$\begin{flalign}f(x)=\begin{cases}
-|x|+1,&-1\leq x\leq1 \\
0,&\text{elsewhere}
\end{cases} &&\end{flalign}$$
$\mathbb{E}[X]=0$
$$\begin{flalign}\mathbb{E}[X^{2}]&=\int_{-\infty}^{+\infty}x^{2}f(x)\,dx=\int_{-1}^{0}x^{3}+x^{2}\,dx+\int_{0}^{1}-x^{3}+x^{2}\,dx\\
&=\left[ \frac{x^{4}}{4}+\frac{x^{3}}{3} \right]_{-1}^{0}+\left[ -\frac{x^{4}}{4}+\frac{x^{3}}{3} \right]_{0}^{1}=\frac{1}{6}
&&\end{flalign}$$
$\mathrm{Var}[X]=\frac{1}{6}=0.167$
```desmos-graph
left=-2.5; right=2.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
y=x+1|-1<=x<=0|blue
y=-x+1|0<=x<=1|blue
```
<div class="page-break" style="page-break-before: always;"></div>

$$\begin{flalign}f(y)=\begin{cases}
-\frac{4}{9}|x|+\frac{2}{3},&-\frac{3}{2}\leq x\leq \frac{3}{2} \\
0,&\text{elsewhere}
\end{cases} &&\end{flalign}$$
$\mathbb{E}[Y]=0$
$$\begin{flalign}\mathbb{E}[Y^{2}]&=\int_{-\infty}^{+\infty}y^{2}f(y)\,dy=\int_{-\frac{3}{2}}^{0} \frac{4}{9}y^{3} +\frac{2}{3}y^{2}\,dy+\int_{0}^{\frac{3}{2}} -\frac{4}{9}y^{3}+\frac{2}{3}y^{2}\,dy\\
&=\left[ \frac{y^{4}}{9}+\frac{2}{9}y^{3} \right]_{-\frac{3}{2}}^{0}+\left[ -\frac{y^{4}}{9}+\frac{2}{9}y^{3} \right]_{0}^{\frac{3}{2}}=\frac{3}{8}
&&\end{flalign}$$
$\mathrm{Var}[Y]=\frac{3}{8}=0.375$
```desmos-graph
left=-2.5; right=2.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
y=(4/9)x+(2/3)|-(3/2)<=x<=0|green
y=-(4/9)x+(2/3)|0<=x<=(3/2)|green
```
