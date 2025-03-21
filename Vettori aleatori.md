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
