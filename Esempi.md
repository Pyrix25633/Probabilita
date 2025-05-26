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

# Variabile aleatoria binomiale
$Y\sim \mathrm{Bin}\left( 20, \frac{1}{3} \right)$ conta il numero di teste su $20$ lanci
La media di teste è $\mathbb{E}[Y]\approx6.667$
La probabilità che esca testa esattamente $3$ volte è $P_{Y}(3)\approx0.0429$
La probabilità che esca testa tra $4$ e $6$ volte è $\sum_{y=4}^{6}P_{Y}(y)\approx0.4189$

# Variabile aleatoria geometrica
$X\sim \mathrm{Geo(0.85)}$ conta il numero di lanci prima che un razzo esploda
La media di lanci prima che il razzo esploda è $\mathbb{E}[X]\approx5.667$
La probabilità che il razzo esploda al secondo lancio è $P_{X}(2)\approx0.1084$
La probabilità che esploda prima del quarto lancio è $\sum_{x=1}^{3}P_{X}(x)\approx0.3280$

# Variabile aleatoria di Poisson
$Z\sim \mathrm{Pois}(5)$ conta il numero di pizze prodotte in un'ora
La media di pizze per ora è esattamente $\mathbb{E}[X]=5$
La probabilità che siano state prodotte $6$ pizze è $P_{Z}(6)\approx0.1462$
La probabilità che siano state prodotte tra $3$ e $8$ pizze è $\sum_{z=3}^{8}P_{Z}(z)\approx0.8073$

# Variabile aleatoria ipergeometrica
$K\sim \mathrm{Iper}(120,7,35)$ conta i pezzi difettosi estratti su un campione di $7$ da un totale di $120$ di cui $35$ difettosi
La media di pezzi difettosi estratti è $\mathbb{E}[K]\approx2.042$
La probabilità di estrarre $5$ pezzi difettosi è $P_{K}(5)\approx0.0195$
La probabilità di estrarre tra $4$ e $7$ pezzi difettosi è $\sum_{k=4}^{7}P_{K}(k)\approx0.1089$

# Variabile aleatoria di Pascal
$Y\sim \mathrm{NegBin}(15,0.75)$ conta il numero di partite perse prima di riuscire a vincerne 15
La media di partite perse è $\mathbb{E}[Y]=5$
La probabilità di perdere $3$ partite è $P_{Y}(3)\approx0.1420$
La probabilità di perdere tra $4$ e $7$ partite è $\sum_{y=4}^{7}P_{Y}(y)\approx0.5328$

# Variabile aleatoria uniforme
$X\sim \mathrm{Unif}(0,30)$ approssima la distribuzione di probabilità che l'autobus arrivi alla fermata tra le 10:00 e le 10:30
La media di minuti di attesa è $\mathbb{E}[X]=15$
La probabilità di aspettare più di $10$ minuti è $\int_{10}^{30}f_{X}(x)\,dx=0.75$

# Variabile aleatoria esponenziale
$X\sim \mathrm{Exp}\left( \frac{1}{50} \right)$ conta il tempo di funzionamento di una batteria di un'auto
La media del tempo di vita prima della rottura è $\mathbb{E}[X]=50$ mila chilometri
La probabilità che duri meno di $45$ mila chilometri è $\mathbb{P}(X\leq45)\approx0.5934$
La probabilità che si rompa dopo più di $40$ mila chilometri è $\mathbb{P}(X>40)\approx0.4493$

# Variabile aleatoria gamma
$X\sim \mathrm{Gamma}\left(8, \frac{1}{50} \right)$ conta la strada percorsa da un'auto durante una gara avendo a disposizione $8$ pieni di carburante che si consumano ogni $50$ chilometri
La probabilità che l'auto riesca a percorrere $250$ chilometri è $\mathbb{P}(X>250)\approx0.8666$

# Variabile aleatoria gaussiana
$X\sim \mathrm{N}(0.45,0.05^{2})$ conta i litri erogati da un distributore automatico con media $0.45$ e deviazione $0.05$
$U\sim \mathrm{N}(0,1)$ normale standard dalla quale si ottengono i valori tabulati
La probabilità che siano erogati più di $0.5$ litri è $\mathbb{P}(X>0.5)=1-\mathbb{P}(U\leq1)\approx0.1587$

# Tabella di frequenza, istogramma e box plot
Dati ordinati:
$67.8,68.2,69.3,70.5,72.1,73.4,75.5,75.0,76.4,77.9,79.0,$$80.6,81.5,82.3,83.7,85.6,86.4,88.7,90.1,91.2,105.8$

$Q_{0}=x_{\mathrm{min}}=67.8$
$Q_{1}=72.1\cdot0.25+73.4\cdot0.75=73.075$
$Q_{2}=79.0$
$Q_{3}=85.6\cdot0.75+86.4\cdot0.25=85.8$
$Q_{4}=x_{\mathrm{max}}=105.8$
$\bar{x}=\frac{1}{21}\sum_{i=1}^{21}x_{i}=80$
$\mathrm{Range}=38$
$\mathrm{IQR}=12.725$
Outliers: $x\not\in[Q_{1}-1.5\cdot \mathrm{IQR},Q_{3}+1.5\cdot \mathrm{IQR}]=[53.9875,104.8875]$
<div class="page-break" style="page-break-before: always;"></div>

Suddivisione in classi di larghezza $3$

| Classe      | Frequenza assoluta | Frequenza relativa | Frequenza cumulativa |
| ----------- | ------------------ | ------------------ | -------------------- |
| $[67,70)$   | $3$                | $\frac{3}{21}$     | $\frac{3}{21}$       |
| $[70,73)$   | $2$                | $\frac{2}{21}$     | $\frac{5}{21}$       |
| $[73,76)$   | $3$                | $\frac{3}{21}$     | $\frac{8}{21}$       |
| $[76,79)$   | $2$                | $\frac{2}{21}$     | $\frac{10}{21}$      |
| $[79,82)$   | $3$                | $\frac{3}{21}$     | $\frac{13}{21}$      |
| $[82,85)$   | $2$                | $\frac{2}{21}$     | $\frac{15}{21}$      |
| $[85,88)$   | $2$                | $\frac{2}{21}$     | $\frac{17}{21}$      |
| $[88,91)$   | $2$                | $\frac{2}{21}$     | $\frac{19}{21}$      |
| $[91,94)$   | $1$                | $\frac{1}{21}$     | $\frac{20}{21}$      |
| $[94,97)$   | $0$                | $0$                | $\frac{20}{21}$      |
| $[97,100)$  | $0$                | $0$                | $\frac{20}{21}$      |
| $[100,103)$ | $0$                | $0$                | $\frac{20}{21}$      |
| $[103,106)$ | $1$                | $\frac{1}{21}$     | $1$                  |
Istogramma:
![istogramma](istogramma.png)

Box plot:
![box_plot](box_plot.png)