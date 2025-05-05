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

<div class="page-break" style="page-break-before: always;"></div>

# Variabile aleatoria geometrica
Esperimenti indipendenti ripetuti con probabilità di successo costante
Conta il numero di ripetizioni dell'esperimento fino al primo insuccesso
$X\sim \mathrm{Geo}(p)$
$P_{X}(x)=p^{x}\cdot(1-p)\;\;x \in \mathbb{N}$
$$\begin{flalign}\sum_{i=0}^{+\infty}P_{X}(x)=\sum_{i=0}^{+\infty}p^{x}\cdot(1-p)=(1-p)\cdot \sum_{i=0}^{+\infty}p^{x}=1 &&\end{flalign}$$
$$\begin{flalign}\Phi_{X}(t)=\frac{1-p}{1-e^{t}p} &&\end{flalign}$$
$$\begin{flalign}\mathbb{E}[X]=\frac{d\Phi_{X}(t)}{dt}\bigg\rvert_{t=0}=\frac{p}{1-p} &&\end{flalign}$$
è il numero medio di successi prima di un insuccesso

# Variabile aleatoria di Poisson
$Y\sim \mathrm{Bin}(n,p)$, $(n\to + \infty, p\to0)$, $\frac{y}{n}\to0$ ($y\ll n$)
Poniamo $\mu=n\cdot p$
$$\begin{flalign}P_{Y}(y)&=\binom{n}{y}\cdot p^{y}\cdot(1-p)^{n-y}=\frac{n!}{y!(n-y)!}\cdot p^{y}\cdot(1-p)^{n-y}\\
&=\frac{n(n-1)\cdot{\dots}\cdot(n-y)}{y!}\cdot p^{y}\cdot(1-p)^{n-y}\approx \frac{n^{y}}{y!}\cdot p^{y}\cdot(1-p)^{n-y}\\
&\approx \frac{n^{y}}{y!}\cdot p^{y}\cdot(1-p)^{n}=\frac{(np)^{y}}{y!}\cdot\sum_{i=0}^{n}\binom{n}{i}\cdot1^{n-i}\cdot(-p)^{i}\\
&=\frac{(np)^{y}}{y!}\cdot\left[ 1-np+\frac{n(n-1)}{2!}p^{2}-\frac{n(n-1)(n-2)}{3!}p^{3}+... \right]\\
&\approx\frac{(np)^{y}}{y!}\cdot\left[ 1-np+\frac{n^{2}}{2!}p^{2}-\frac{n^{3}}{3!}p^{3}+\dots \right]=\frac{\mu^{y}}{y!}\left[ 1-\mu+\frac{\mu^{2}}{2!}-\frac{\mu^{3}}{3!}+\dots \right]\\
&\approx \frac{\mu^{y}}{y!}\cdot e^{-\mu}
&&\end{flalign}$$
$Z\sim \mathrm{Pois(\mu)}$, $\mu>0$, $z\in \mathbb{N}$
$$\begin{flalign}P_{Z}(z)=\frac{\mu^{z}}{z!}\cdot e^{-\mu} &&\end{flalign}$$
Approssima la probabilità di eventi simili che si possono verificare in un intervallo di tempo/spazio/...

$$\begin{flalign}\Phi_{Z}(t)=\mathbb{E}[e^{tZ}]=\sum_{z=0}^{+\infty}e^{tz}\cdot \frac{\mu^{z}}{z!}\cdot e^{-\mu}=e^{-\mu}\sum_{z=0}^{+\infty} \frac{(e^{t}\mu)^{z}}{z!}=e^{-\mu}e^{e^{t}\mu}=e^{\mu\cdot(e^{t}-1)} &&\end{flalign}$$
Si può notare che la media è uguale a quella del $\mathrm{Bin}$
$$\begin{flalign}\mathbb{E}[Z]=\frac{d\Phi_{Z}(t)}{dt}\bigg\rvert_{t=0}=e^{\mu\cdot(e^{t}-1)}\cdot(\mu e^{t})=\mu=n\cdot p &&\end{flalign}$$
$$\begin{flalign}\mathbb{E}[Z^{2}]=\frac{d^{2}\Phi_{Z}(t)}{dt^{2}}\bigg\rvert_{t=0}=\mu^{2}+\mu &&\end{flalign}$$
$\mathrm{Var}[Z]=\mathbb{E}[Z^{2}]-\mathbb{E}[Z]^{2}=\mu^{2}+\mu-\mu^{2}=\mu$

<div class="page-break" style="page-break-before: always;"></div>

Inoltre è riproducibile
$Z_{1}\sim \mathrm{Pois(\mu_{1})}\perp \!\!\! \perp Z_{2}\sim \mathrm{Pois(\mu_{2})}$, $Z=Z_{1}+Z_{2}$
$\Phi_{Z}(t)=\Phi_{Z_{1}}(t)\cdot \Phi_{Z_{2}}(t)=e^{\mu_{1}\cdot(e^{t}-1)}\cdot e^{\mu_{2}\cdot(e^{t-1})}=e^{(\mu_{1}+\mu_{2})(e^{t}-1)}\implies Z\sim \mathrm{Pois(\mu_{1}+\mu_{2})}$

# Variabile aleatoria ipergeometrica
Estrazione senza reimmissione da un lotto contenente $N$ elementi di cui $D$ difettosi
L'estrazione di un pezzo difettoso vale $1$ e di un pezzo non difettoso $0$
Indica la probabilità di estrarre $k\leq D$ pezzi difettosi da un campione di $n\leq N$ elementi
$K\sim \mathrm{Iper}(N,n,D)$, $k\in[\mathrm{max}\{ 0,n-N+D \},\mathrm{min}\{ n,D \}]$
$$\begin{flalign}P_{K}(k)=\frac{\binom{D}{k}\binom{N-D}{n-k}}{\binom{N}{n}} &&\end{flalign}$$

Ogni estrazione è una Bernoulliana con $p=\frac{D}{N}$
La probabilità di estrarre un pezzo difettoso alla seconda estrazione è
$$\begin{flalign}\mathbb{P}(D\mathrm{II})&=\mathbb{P}(D\mathrm{II|D\mathrm{I}})\cdot \mathbb{P}(D\mathrm{I})+\mathbb{P}(D\mathrm{II|\bar{D\mathrm{I}}})\cdot \mathbb{P}(\bar{D\mathrm{I}})=\frac{D-1}{N-1}\cdot \frac{D}{N}+\frac{D}{N-1}\cdot\left( 1-\frac{N}{D} \right)\\
&=\frac{D^{2}-D+DN-D^{2}}{(N-1)(N)}=\frac{D(N-1)}{N(N-1)}=\frac{D}{N}
&&\end{flalign}$$

$$\begin{flalign}\mathbb{E}[K]=n\cdot \frac{D}{N} &&\end{flalign}$$

# Variabile aleatoria di Pascal
Anche chiamata negativa binomiale
$Y\sim \mathrm{NegBin}(m,p)$
Conta il numero di insuccessi $y$ prima di $m$ successi, quindi per definizione l'ultimo è un successo
$$\begin{flalign}P_{Y}(y)=\binom{y+m-1}{y}\cdot p^{m}\cdot(1-p)^{y} &&\end{flalign}$$
Si può anche scrivere come somma di $y$ geometriche indipendenti $X_{i}\sim \mathrm{Geo(p)}$ con $p$ identica
$$\begin{flalign}\Phi_{Y}(t)=\mathbb{E}[e^{tY}]=\mathbb{E}\left[ e^{t\sum_{i=1}^{y}X_{i}} \right]=\prod_{i=1}^{y}\mathbb{E}[e^{tX_{i}}]=\frac{(1-p)^{y}}{(1-e^{t}p)^{y}} &&\end{flalign}$$
$$\begin{flalign}\mathbb{E}[Y]=\mathbb{E}\left[ \sum_{i=1}^{y}X_{i} \right]=\sum_{i=1}^{y}\mathbb{E}[X_{i}]=\frac{yp}{1-p} &&\end{flalign}$$

---
# Variabile aleatoria uniforme
$X\sim \mathrm{Unif}(a,b)$
$$\begin{flalign}f_{X}(x)=\begin{cases}
\frac{1}{b-a},&x \in[a,b] \\
0,&x \notin[a,b]
\end{cases} &&\end{flalign}$$
$$\begin{flalign}\Phi_{X}(t)=\mathbb{E}[e^{tX}]=\int_{a}^{b}e^{tx}\cdot \frac{1}{b-a}\,dx=\frac{e^{tb}-e^{ta}}{(b-a)\cdot t} &&\end{flalign}$$
<div class="page-break" style="page-break-before: always;"></div>

Si può definire una trasformazione
$\varphi:[a,b]\to[0,1]$, $\varphi(y)=\frac{y-a}{b-a}$
$$\begin{flalign} \frac{X-a}{b-a}=Y\sim \mathrm{Unif}(0,1) &&\end{flalign}$$
$$\begin{flalign}f_{Y}(y)=\begin{cases}
1,&y\in[0,1] \\
0,&y\notin[0,1]
\end{cases} &&\end{flalign}$$
$$\begin{flalign}\Phi_{Y}(t)=\mathbb{E}[e^{tY}]=\frac{e^{t}-1}{t} &&\end{flalign}$$
$$\begin{flalign}\mathbb{E}[Y]=\frac{d\Phi_{Y}(t)}{dt}\bigg\rvert_{t=0}=\frac{d}{dt}\left( \frac{e^{t}-1}{t} \right)\bigg\rvert_{t=0}=\frac{te^{t}-(e^{t}-1)}{t^{2}}\bigg\rvert_{t=0}=\lim_{ t \to 0 } \frac{t\cdot e^{t}}{2t}=\frac{1}{2} &&\end{flalign}$$
$$\begin{flalign}\mathrm{Var}[Y]=\frac{1}{12} &&\end{flalign}$$
Ora si possono riutilizzare i calcoli per $X=Y\cdot(b-a)+a$
$$\begin{flalign}\mathbb{E}[X]=\mathbb{E}[Y\cdot(b-a)+a]=(b-a)\cdot\mathbb{E}[Y]+a=\frac{b-a}{2}+a=\frac{b+a}{2} &&\end{flalign}$$
$$\begin{flalign}\mathrm{Var}[X]=\mathrm{Var}[Y\cdot(b-a)+a]=(b-a)^{2}\cdot \mathrm{Var}[Y]=\frac{(b-a)^{2}}{12} &&\end{flalign}$$

# Variabile aleatoria esponenziale
$\mu=\lambda x$, $Y\sim \mathrm{Pois}(\mu)$
$$\begin{flalign}P_{Y}(y)=\frac{(\lambda x)^{y}}{y!}\cdot e^{-\lambda x} &&\end{flalign}$$
con $y\in \mathbb{N}$
$x$ indica il tempo di funzionamento di un sistema riparabile, $Y$ conta gli eventi guasto
La probabilità di non osservare guasti in $[0,x]$ è $\mathbb{P}(Y=0)=P_{Y}(0)=e^{-\lambda x}$, $x,\lambda>0$
Allo stesso modo non osservare guasti entro un tempo $x$ equivale al corretto funzionamento per tale tempo
$X\sim \mathrm{Exp}(\lambda)$ conta il tempo di funzionamento, $\mathbb{P}(X>x)=e^{-\lambda x}$ e $F_{X}(x)=\mathbb{P}(X\leq x)=1-e^{-\lambda x}$
$f_{X}(x)=\lambda\cdot e^{-\lambda x}$, $x>0$
Viene utilizzata per misurare attese, code, decadimenti e rotture improvvise
$$\begin{flalign}\Phi_{X}(t)=\mathbb{E}[e^{tX}]=\int_{0}^{+\infty}e^{-(\lambda-t)\cdot x}\,dx=\frac{\lambda}{\lambda-t} &&\end{flalign}$$
con $t<\lambda$
$$\begin{flalign}\mathbb{E}[X]=\frac{d\Phi_{X}(t)}{dt}\bigg\rvert_{y=0}=\frac{1}{\lambda} &&\end{flalign}$$
$$\begin{flalign}\mathrm{Var}[X]=\frac{1}{\lambda^{2}} &&\end{flalign}$$
Vige della proprietà di assenza di memoria, dati $x_{2}>x_{1}$, $x_{2}=x_{1}+x$ ($x>0$)
$$\begin{flalign}\mathbb{P}(X>x_{2}|X>x_{1})&=\frac{\mathbb{P}((X>x_{2})\cap(X>x_{1}))}{\mathbb{P}(X>x_{1})}=\frac{\mathbb{P}(X>x_{2})}{\mathbb{P}(X>x_{1})}=\frac{1-F_{X}(x_{2})}{1-F_{X}(x_{1})}\\
&=\frac{e^{-\lambda(x_{1}+x)}}{e^{-\lambda x_{1}}}=\frac{e^{-\lambda x_{1}}\cdot e^{-\lambda x}}{e^{-\lambda x_{1}}}=e^{-\lambda x}=\mathbb{P}(X>x)
&&\end{flalign}$$
