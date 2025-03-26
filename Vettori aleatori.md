# Variabili aleatorie congiunte
$(S,\mathcal{A},\mathbb{P})$ spazio di probabilità, $X,Y$ variabili aleatorie
La coppia $(X,Y)$ è detta vettore aleatorio

# Funzione di ripartizione congiunta
$F(x,y)=\mathbb{P}((X\leq x)\cap(Y\leq y))$
Proprietà:
- è continua da destra: $F(x,y)=\lim_{ \epsilon \to 0 }F(x+\epsilon,y)=\lim_{ \epsilon \to 0 }F(x,y+\epsilon)$
- $$\begin{flalign}\lim_{ x \to -\infty } F(x,y)=0\\\lim_{ y \to -\infty }F(x,y)=0\\\lim_{ (x,y) \to (+\infty,+\infty) }F(x,y)=1 &&\end{flalign}$$

Inoltre:
$\mathbb{P}((x_{1}<X\leq x_{2})\land(y_{1}<Y\leq y_{2}))=F(x_{2},y_{2})-F(x_{1},y_{2})-F(x_{2},y_{1})+F(x_{1},y_{1})$

# Funzioni marginali
### Funzioni di ripartizione marginali
$F_{X}(x)=F(x,+\infty)$
$F_{Y}(y)=F(+\infty,y)$

### Funzioni di densità marginali
$$\begin{flalign}f_{X}(x)=\int_{-\infty}^{+\infty} f(x,y)\,dy\\f_{Y}(y)=\int_{-\infty}^{+\infty} f(x,y)\,dx &&\end{flalign}$$

### Funzioni di massa marginali
$$\begin{flalign}P_{X}(x)=\sum_{y_{i}}P(x,y_{i})\\P_{Y}(y)=\sum_{x_{i}}P(x_{i},y)   &&\end{flalign}$$

# Indipendenza
$X,Y$ variabili aleatorie, $D_{X},D_{Y}$ sottoinsiemi degli insiemi di definizione di $X,Y\implies X\perp \!\!\! \perp Y$ se $\mathbb{P}((X\in D_{X})\cap(Y\in D_{Y}))=\mathbb{P}(X\in D_{X})\cdot \mathbb{P}(Y\in D_{Y})\;\;\forall D_{X},D_{Y}$

In particolare se $D_{X}=(X\leq x),D_{Y}=(Y\leq y)$ e $F$ è funzione di ripartizione congiunta $\implies X\perp \!\!\! \perp Y$ se $F(x,y)=F_{X}(x)\cdot F_{Y}(y)$
Analogamente $f(x,y)=f_{X}(x)\cdot f_{Y}(y)$ e $P(x,y)=P_{X}(x)\cdot P_{Y}(y)$

# Media
$$\begin{flalign}\mathbb{E}[X]:=\begin{cases}
\sum_{i}x_{i}P(x_{i})  \\
\int_{-\infty}^{+\infty} xf(x)\,dx
\end{cases} &&\end{flalign}$$
se esiste finita è detta speranza matematica di $X$
$\varphi:\mathbb{R}\to \mathbb{R}\implies$
$$\begin{flalign}\mathbb{E}[\varphi(X)]:=\begin{cases}
\sum_{i}\varphi(x_{i})P(x_{i}) \\
\int_{-\infty}^{+\infty} \varphi(x)f(x)\,dx
\end{cases} &&\end{flalign}$$

Si può anche applicare alla potenza di una variabile aleatoria $X^{n}$ e $\mathbb{E}[X^{n}]$ è detto momento $n$-esimo centrato di $X$

E' lineare: $\mathbb{E}[a+bX]=a+b\mathbb{E}[X]\;\;\forall a,b\in \mathbb{R}$

$(X,Y)$ vettore aleatorio
$$\begin{flalign}\mathbb{E}[(X,Y)]=\begin{cases}
\sum_{i}\sum_{j}x_{i}y_{i}P(x_{i},y_{i}) \\
\int_{-\infty}^{+\infty} \int_{-\infty}^{+\infty} xyf(x,y)\,dx\,dy  
\end{cases} &&\end{flalign}$$
se esistono finiti

### Casi notevoli
$X,Y$ variabili aleatorie, $Z=X+Y\implies \mathbb{E}[Z]=\mathbb{E}[X]+\mathbb{E}[Y]$
Se $X\perp \!\!\! \perp Y$ continue $f(x,y)=f_{X}(x)\cdot f_{Y}(y)\implies$
$$\begin{flalign}\mathbb{E}[(X,Y)]=\left( \int_{-\infty}^{+\infty} xf_{X}(x)\,dx \right)\left( \int_{-\infty}^{+\infty}yf_{Y}(y) \,dy \right) &&\end{flalign}$$

# Varianza
$$\begin{flalign}\mathrm{Var}[X]=\mathbb{E}[(X-\mathbb{E}[X])^{2}]=\begin{cases}
\sum_{i}(x_{i}-\mathbb{E}[X])^{2}P(x_{i}) \\
\int_{-\infty}^{+\infty} (x-\mathbb{E}[X])^{2}f(x)\,dx
\end{cases} &&\end{flalign}$$
Non è lineare e $\mathrm{Var}[a+bX]=b^{2}\mathbb{E}[X]$

$\mathrm{Var}[X+Y]=\mathrm{Var}[X]+\mathrm{Var}[Y]-2\mathbb{E}[(X-\mathbb{E}[X])(Y-\mathbb{E}[Y])]$ misura la tendenza delle due variabili as assumere valori maggiori o minori della media "insieme"

Se $X\perp \!\!\! \perp Y\implies \mathrm{Cov}(X,Y)=\mathbb{E}[(X-\mathbb{E}[X])(Y-\mathbb{E}[Y])]=0\implies$$\mathrm{Var}[X+Y]=\mathrm{Var}[X]+\mathrm{Var}[Y]$
Dimostrazione (nel caso continuo):
$$\begin{flalign}\mathrm{Cov}(X,Y)=\left( \int_{-\infty}^{+\infty} (x-\mathbb{E}[X])f_{X}(x)\,dx \right)\left( \int_{-\infty}^{+\infty} (y-\mathbb{E}[Y])f_{Y}(y)\,dy \right) &&\end{flalign}$$
$$\begin{flalign}\int_{-\infty}^{+\infty} xf_{X}(x)\,dx-\int_{-\infty}^{+\infty} \mathbb{E}[X]f_{X}(x)\,dx=\mathbb{E}[X]-1\mathbb{E}[X]\cdot1=0 &&\end{flalign}$$
Analogamente per $y$
