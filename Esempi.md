# Massa di probabilità
$$\begin{flalign}P(x)=\begin{cases}
\frac{1}{2},&x=1 \\
\frac{1}{5},&x=2,3 \\
\frac{3}{10},&x=5 \\
0,&\text{elsewhere}
\end{cases} &&\end{flalign}$$
```desmos-graph
left=-0.5; right=5.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
(1,1/2)|blue
(2,1/5)|blue
(3,1/5)|blue
(5,3/10)|blue
```

$$\begin{flalign}F(x)=\begin{cases}
0,&x<1 \\
\frac{1}{2},&1\leq x<2 \\
\frac{6}{10},&2\leq x<3 \\
\frac{7}{10},&3\leq x<5 \\
1,&x\geq5
\end{cases} &&\end{flalign}$$
```desmos-graph
left=-0.5; right=5.5; top=1.5; bottom=-0.5;
width=600; height=300;
---
y=0|x<1|green
(1,1/2)|green
y=1/2|1<=x<2|green
(2,6/10)|green
y=6/10|2<=x<3|green
(3,7/10)|green
y=7/10|3<=x<5|green
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
