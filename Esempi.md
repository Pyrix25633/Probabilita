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
