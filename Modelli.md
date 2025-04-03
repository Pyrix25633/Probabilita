# Variabile aleatoria di Bernoulli
Astrazione del lancio di una moneta
$X\sim \mathrm{B}(p)$ assume valori $\{0,1\}$
$$\begin{flalign}P_{X}(x)=\begin{cases}
p,\;&x=1 \\
1-p=q, &x=0
\end{cases}\;\;\;p \in(0,1) &&\end{flalign}$$
$\Phi_{X}(t)=\mathbb{E}[e^{tX}]=\sum_{t=0}^{1}e^{t\cdot i}\cdot P_{X}(i)=e^{0t}(1-p)+e^{1t}p=q+e^{t}p$
$$\begin{flalign}\mathbb{E}[X]=\frac{d\Phi_{X}(t)}{dt}\bigg\rvert_{t=0}=e^{t}p\big\rvert_{t=0}=p &&\end{flalign}$$
$$\begin{flalign}\mathbb{E}[X^{2}]=\frac{d^{2}\Phi_{X}(t)}{dt^{2}}\bigg\rvert_{t=0}=e^{t}p\big\rvert_{t=0}=p &&\end{flalign}$$
$\mathrm{Var}(X)=\mathbb{E}[X^{2}]-(\mathbb{E}[X])^{2}=p-p^{2}=p(1-p)=p\cdot q$

# Variabile aleatoria binomiale
Esperimenti ripetuti e indipendenti con due possibili esiti con probabilità $p$ e $1-p$
Abbinando $1$ al successo e $0$ all'insuccesso, ripetendo $n$ volte l'esperimento, la variabile che conta il numero di successi è detta binomiale ed è la somma di $n$ variabili aleatorie Bernoulliane stocasticamente indipendenti
$X_{1},\dots,X_{n}\sim \mathrm{B}(p)$, $X_{i}\perp \!\!\! \perp X_{j}\;\;x\neq j$
$Y=\sum_{i=1}^{n}X_{i}\sim \mathrm{Bin}(n,p)$
$$\begin{flalign}P_{Y}(y)=\binom{n}{y}(p)^{y}(1-p)^{n-y}\;\;y\in \{ 0,\dots,n \} &&\end{flalign}$$
$$\begin{flalign}\Phi_{Y}(t)=\mathbb{E}[e^{tY}]=\mathbb{E}\left[ e^{t\sum_{i=1}^{n}X_{i}} \right]=\mathbb{E}\left[ \prod_{i=1}^{n}e^{tX_{i}} \right]=\prod_{i=1}^{n}\mathbb{E}[e^{tX_{i}}]=(e^{t}p+q)^{n} &&\end{flalign}$$
$\mathbb{E}[Y]=\mathbb{E}\left[ \sum_{i=1}^{n}X_{i} \right]=\sum_{i=1}^{n}\mathbb{E}[X_{i}]=n\cdot p$
$\mathrm{Var}(Y)=n\cdot p\cdot(1-p)=n\cdot p\cdot q$

$Y_{1}\sim \mathrm{Bin}(n_{1},p)$, $Y_{2}\sim \mathrm{Bin}(n_{2},p)$, $Y_{1}\perp \!\!\! \perp Y_{2}$, $Z=Y_{1}+Y_{2}$
$Z\sim \mathrm{Bin}(n_{1}+n_{2},p)$
$\Phi_{Z}(t)=\mathbb{E}[e^{tZ}]=\mathbb{E}[e^{tY_{1}+tY_{2}}]=\mathbb{E}[e^{tY_{1}}e^{tY_{2}}]=\mathbb{E}[e^{tY_{1}}]\cdot \mathbb{E}[e^{tY_{2}}]$$=(e^{t}p+q)^{n_{1}}(e^{t}p+q)=(e^{t}p+q)^{n_{1}+n_{2}}$

# Variabile aleatoria geometrica
Esperimenti indipendenti ripetuti con probabilità di successo costante
Conta il numero di ripetizioni dell'esperimento fino al primo insuccesso
$X\sim \mathrm{Geo}(p)$
$P_{X}(x)=p^{x}\cdot(1-p)\;\;x \in \mathbb{N}$
$$\begin{flalign}\sum_{i=0}^{+\infty}P_{X}(x)=\sum_{i=0}^{+\infty}p^{x}\cdot(1-p)=(1-p)\cdot \sum_{i=0}^{+\infty}p^{x}=1 &&\end{flalign}$$
$$\begin{flalign}\Phi_{X}(t)=\frac{1-p}{1-e^{t}p} &&\end{flalign}$$
$$\begin{flalign}\mathbb{E}[X]=\frac{d\Phi_{X}(t)}{dt}\bigg\rvert_{t=0}=\frac{p}{1-p} &&\end{flalign}$$
è il numero medio di successi prima di un insuccesso
