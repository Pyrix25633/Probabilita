# Variabile aleatoria di Bernoulli
> [!definizione]
> Astrazione del lancio di una moneta
> $X\sim \mathrm{B}(p)$ assume valori $\{0,1\}$
> $$\begin{flalign}P_{X}(x)=\begin{cases}
p,\;&x=1 \\
1-p=q, &x=0
\end{cases} &&\end{flalign}$$
> con $p \in(0,1)$

> [!formule]
> $\Phi_{X}(t)=q+e^{t}p$
> > [!dimostrazione]-
> > ${\dots}=\mathbb{E}[e^{tX}]=\sum_{i=0}^{1}e^{t\cdot i}\cdot P_{X}(x_{i})=\sum_{i=0}^{1}e^{t\cdot i}\cdot P_{X}(i)=e^{0t}(1-p)+e^{1t}p={\dots}$
> 
> $$\begin{flalign}\mathbb{E}[X]=p &&\end{flalign}$$
> > [!dimostrazione]-
> > ${\dots}=\frac{d\Phi_{X}(t)}{dt}\bigg\rvert_{t=0}=e^{t}p\big\rvert_{t=0}={\dots}$
> > oppure
> > $\dots=\sum_{i=0}^1x_{i}\cdot P_{X}(x_{i})=\sum_{i=0}^1i\cdot P_{X}(i)=0\cdot q+1\cdot p=\dots$
> 
> $$\begin{flalign}\mathbb{E}[X^{2}]=p &&\end{flalign}$$
> > [!dimostrazione]-
> > ${\dots}=\frac{d^{2}\Phi_{X}(t)}{dt^{2}}\bigg\rvert_{t=0}=\frac{d}{dt}e^{t}p\big\rvert_{t=0}=e^{t}p\big\rvert_{t=0}={\dots}$
> > oppure
> > $\dots=\sum_{i=0}^1x^2_{i}\cdot P_{X}(x_{i})=\sum_{i=0}^1i^2\cdot P_{X}(i)=0^2\cdot q+1^2\cdot p=\dots$
> 
> $\mathrm{Var}(X)=p(1-p)=p\cdot q$
> > [!dimostrazione]-
> > ${\dots}=\mathbb{E}[X^{2}]-(\mathbb{E}[X])^{2}=p-p^{2}={\dots}$
<div class="page-break" style="page-break-before: always;"></div>

# Variabile aleatoria binomiale
> [!definizione]
> Esperimenti ripetuti e indipendenti con due possibili esiti con probabilità $p$ e $1-p$
> Abbinando $1$ al successo e $0$ all'insuccesso, ripetendo $n$ volte l'esperimento, la variabile che conta il numero di successi è detta binomiale ed è la somma di $n$ variabili aleatorie Bernoulliane stocasticamente indipendenti
> $X_{1},\dots,X_{n}\sim \mathrm{B}(p)$, $X_{i}\perp \!\!\! \perp X_{j}\;\;i\neq j$
> $Y=\sum_{i=1}^{n}X_{i}\sim \mathrm{Bin}(n,p)$
> $$\begin{flalign}P_{Y}(y)=\binom{n}{y}(p)^{y}(1-p)^{n-y}\;\;y\in \{ 0,\dots,n \} &&\end{flalign}$$

> [!formule]
> $\Phi_{Y}(t)=(e^{t}p+q)^{n}$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}=\mathbb{E}[e^{tY}]=\mathbb{E}\left[ e^{t\sum_{i=1}^{n}X_{i}} \right]=\mathbb{E}\left[ \prod_{i=1}^{n}e^{tX_{i}} \right]=\prod_{i=1}^{n}\mathbb{E}[e^{tX_{i}}]={\dots} &&\end{flalign}$$
> 
> $\mathbb{E}[Y]=n\cdot p$
> > [!dimostrazione]-
> > ${\dots}=\mathbb{E}\left[ \sum_{i=1}^{n}X_{i} \right]=\sum_{i=1}^{n}\mathbb{E}[X_{i}]={\dots}$
> 
> $\mathrm{Var}(Y)=n\cdot p\cdot(1-p)=n\cdot p\cdot q$

> [!approfondimento]-
> $Y_{1}\sim \mathrm{Bin}(n_{1},p)$, $Y_{2}\sim \mathrm{Bin}(n_{2},p)$, $Y_{1}\perp \!\!\! \perp Y_{2}$, $Z=Y_{1}+Y_{2}$
> $Z\sim \mathrm{Bin}(n_{1}+n_{2},p)$
> $\Phi_{Z}(t)=\mathbb{E}[e^{tZ}]=\mathbb{E}[e^{tY_{1}+tY_{2}}]=\mathbb{E}[e^{tY_{1}}e^{tY_{2}}]=\mathbb{E}[e^{tY_{1}}]\cdot \mathbb{E}[e^{tY_{2}}]$$=(e^{t}p+q)^{n_{1}}(e^{t}p+q)=(e^{t}p+q)^{n_{1}+n_{2}}$

<div class="page-break" style="page-break-before: always;"></div>

# Variabile aleatoria geometrica
> [!definizione]
> Esperimenti indipendenti ripetuti con probabilità di successo $p$ costante
> Conta il numero di ripetizioni dell'esperimento fino al primo insuccesso
> $X\sim \mathrm{Geo}(p)$
> $P_{X}(x)=p^{x}\cdot(1-p)\;\;x \in \mathbb{N}$
$$\begin{flalign}\sum_{i=0}^{+\infty}P_{X}(x)=\sum_{i=0}^{+\infty}p^{x}\cdot(1-p)=(1-p)\cdot \sum_{i=0}^{+\infty}p^{x}=1 &&\end{flalign}$$

> [!formule]
> $$\begin{flalign}\Phi_{X}(t)=\frac{1-p}{1-e^{t}p} &&\end{flalign}$$
> $$\begin{flalign}\mathbb{E}[X]=\frac{d\Phi_{X}(t)}{dt}\bigg\rvert_{t=0}=\frac{p}{1-p} &&\end{flalign}$$
> è il numero medio di successi prima di un insuccesso

# Variabile aleatoria di Poisson
> [!definizione]
> $Y\sim \mathrm{Bin}(n,p)$, $(n\to + \infty, p\to0)$, $\frac{y}{n}\to0$ ($y\ll n$)
> Poniamo $\mu=n\cdot p$
> $$\begin{flalign}P_{Y}(y)\approx \frac{\mu^{y}}{y!}\cdot e^{-\mu}
&&\end{flalign}$$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}&=\binom{n}{y}\cdot p^{y}\cdot(1-p)^{n-y}=\frac{n!}{y!(n-y)!}\cdot p^{y}\cdot(1-p)^{n-y}\\
&=\frac{n(n-1)\cdot{\dots}\cdot(n-y)}{y!}\cdot p^{y}\cdot(1-p)^{n-y}\approx \frac{n^{y}}{y!}\cdot p^{y}\cdot(1-p)^{n-y}\\
&\approx \frac{n^{y}}{y!}\cdot p^{y}\cdot(1-p)^{n}=\frac{(np)^{y}}{y!}\cdot\sum_{i=0}^{n}\binom{n}{i}\cdot1^{n-i}\cdot(-p)^{i}\\
&=\frac{(np)^{y}}{y!}\cdot\left[ 1-np+\frac{n(n-1)}{2!}p^{2}-\frac{n(n-1)(n-2)}{3!}p^{3}+... \right]\\
&\approx\frac{(np)^{y}}{y!}\cdot\left[ 1-np+\frac{n^{2}}{2!}p^{2}-\frac{n^{3}}{3!}p^{3}+\dots \right]\\
&=\frac{\mu^{y}}{y!}\left[ 1-\mu+\frac{\mu^{2}}{2!}-\frac{\mu^{3}}{3!}+\dots \right]={\dots} &&\end{flalign}$$
> <div class="page-break" style="page-break-before: always;"></div>
> 
> $Z\sim \mathrm{Pois(\mu)}$, $\mu>0$, $z\in \mathbb{N}$
> $$\begin{flalign}P_{Z}(z)=\frac{\mu^{z}}{z!}\cdot e^{-\mu} &&\end{flalign}$$
> Approssima la probabilità di eventi simili che si possono verificare in un intervallo di tempo/spazio/...

> [!formule]
> $\Phi_{Z}(t)=e^{\mu\cdot(e^{t}-1)}$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}=\mathbb{E}[e^{tZ}]=\sum_{z=0}^{+\infty}e^{tz}\cdot \frac{\mu^{z}}{z!}\cdot e^{-\mu}=e^{-\mu}\sum_{z=0}^{+\infty} \frac{(e^{t}\mu)^{z}}{z!}=e^{-\mu}e^{e^{t}\mu}={\dots} &&\end{flalign}$$
> Si può notare che la media è uguale a quella del $\mathrm{Bin}$
> $\mathbb{E}[Z]=\mu=n\cdot p$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}=\frac{d\Phi_{Z}(t)}{dt}\bigg\rvert_{t=0}=e^{\mu\cdot(e^{t}-1)}\cdot(\mu e^{t})={\dots} &&\end{flalign}$$
> 
> $$\begin{flalign}\mathbb{E}[Z^{2}]=\frac{d^{2}\Phi_{Z}(t)}{dt^{2}}\bigg\rvert_{t=0}=\mu^{2}+\mu &&\end{flalign}$$
> $\mathrm{Var}[Z]=\mu$
> > [!dimostrazione]-
> > ${\dots}=\mathbb{E}[Z^{2}]-\mathbb{E}[Z]^{2}=\mu^{2}+\mu-\mu^{2}={\dots}$

> [!approfondimento]-
> Inoltre è riproducibile
> $Z_{1}\sim \mathrm{Pois(\mu_{1})}\perp \!\!\! \perp Z_{2}\sim \mathrm{Pois(\mu_{2})}$, $Z=Z_{1}+Z_{2}$
> $\Phi_{Z}(t)=\Phi_{Z_{1}}(t)\cdot \Phi_{Z_{2}}(t)=e^{\mu_{1}\cdot(e^{t}-1)}\cdot e^{\mu_{2}\cdot(e^{t-1})}=e^{(\mu_{1}+\mu_{2})(e^{t}-1)}\implies Z\sim \mathrm{Pois(\mu_{1}+\mu_{2})}$
<div class="page-break" style="page-break-before: always;"></div>

# Variabile aleatoria ipergeometrica
> [!definizione]
> Estrazione senza reimmissione da un lotto contenente $N$ elementi di cui $D$ difettosi
> L'estrazione di un pezzo difettoso vale $1$ e di un pezzo non difettoso $0$
> Indica la probabilità di estrarre $k\leq D$ pezzi difettosi da un campione di $n\leq N$ elementi
> $K\sim \mathrm{Iper}(N,n,D)$, $k\in[\mathrm{max}\{ 0,n-N+D \},\mathrm{min}\{ n,D \}]$
> $$\begin{flalign}P_{K}(k)=\frac{\binom{D}{k}\binom{N-D}{n-k}}{\binom{N}{n}} &&\end{flalign}$$
> 
> Ogni estrazione è una Bernoulliana con $p=\frac{D}{N}$

> [!approfondimento]-
> La probabilità di estrarre un pezzo difettoso alla seconda estrazione è
> $$\begin{flalign}\mathbb{P}(D\mathrm{II})&=\mathbb{P}(D\mathrm{II|D\mathrm{I}})\cdot \mathbb{P}(D\mathrm{I})+\mathbb{P}(D\mathrm{II|\bar{D\mathrm{I}}})\cdot \mathbb{P}(\bar{D\mathrm{I}})=\frac{D-1}{N-1}\cdot \frac{D}{N}+\frac{D}{N-1}\cdot\left( 1-\frac{N}{D} \right)\\
&=\frac{D^{2}-D+DN-D^{2}}{(N-1)(N)}=\frac{D(N-1)}{N(N-1)}=\frac{D}{N}
&&\end{flalign}$$

> [!formule]
> $$\begin{flalign}\mathbb{E}[K]=n\cdot \frac{D}{N} &&\end{flalign}$$

# Variabile aleatoria di Pascal
> [!definizione]
> Anche chiamata negativa binomiale
> $Y\sim \mathrm{NegBin}(m,p)$
> Conta il numero di insuccessi $y$ prima di $m$ successi, quindi per definizione l'ultimo è un successo
> $$\begin{flalign}P_{Y}(y)=\binom{y+m-1}{y}\cdot p^{m}\cdot(1-p)^{y} &&\end{flalign}$$
> Si può anche scrivere come somma di $y$ geometriche indipendenti $X_{i}\sim \mathrm{Geo(p)}$ con $p$ identica
<div class="page-break" style="page-break-before: always;"></div>

> [!formule]
> $$\begin{flalign}\Phi_{Y}(t)=\frac{(1-p)^{y}}{(1-e^{t}p)^{y}} &&\end{flalign}$$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}=\mathbb{E}[e^{tY}]=\mathbb{E}\left[ e^{t\sum_{i=1}^{y}X_{i}} \right]=\prod_{i=1}^{y}\mathbb{E}[e^{tX_{i}}]={\dots} &&\end{flalign}$$
> 
> $$\begin{flalign}\mathbb{E}[Y]=\frac{yp}{1-p} &&\end{flalign}$$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}=\mathbb{E}\left[ \sum_{i=1}^{y}X_{i} \right]=\sum_{i=1}^{y}\mathbb{E}[X_{i}]={\dots} &&\end{flalign}$$

---
# Variabile aleatoria uniforme
> [!definizione]
> $X\sim \mathrm{Unif}(a,b)$
> $$\begin{flalign}f_{X}(x)=\begin{cases}
\frac{1}{b-a},&x \in[a,b] \\
0,&x \notin[a,b]
\end{cases} &&\end{flalign}$$

> [!formule]
> $$\begin{flalign}\Phi_{X}(t)=\frac{e^{tb}-e^{ta}}{(b-a)\cdot t} &&\end{flalign}$$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}=\mathbb{E}[e^{tX}]=\int_{a}^{b}e^{tx}\cdot \frac{1}{b-a}\,dx={\dots} &&\end{flalign}$$
<div class="page-break" style="page-break-before: always;"></div>

> [!approfondimento]-
> Si può definire una trasformazione
> $\varphi:[a,b]\to[0,1]$, $\varphi(y)=\frac{y-a}{b-a}$
> $$\begin{flalign} \frac{X-a}{b-a}=Y\sim \mathrm{Unif}(0,1) &&\end{flalign}$$
> $$\begin{flalign}f_{Y}(y)=\begin{cases}
1,&y\in[0,1] \\
0,&y\notin[0,1]
\end{cases} &&\end{flalign}$$
> $$\begin{flalign}\Phi_{Y}(t)=\mathbb{E}[e^{tY}]=\frac{e^{t}-1}{t} &&\end{flalign}$$
> $$\begin{flalign}\mathbb{E}[Y]=\frac{d\Phi_{Y}(t)}{dt}\bigg\rvert_{t=0}=\frac{d}{dt}\left( \frac{e^{t}-1}{t} \right)\bigg\rvert_{t=0}=\frac{te^{t}-(e^{t}-1)}{t^{2}}\bigg\rvert_{t=0}=\lim_{ t \to 0 } \frac{t\cdot e^{t}}{2t}=\frac{1}{2} &&\end{flalign}$$
> $$\begin{flalign}\mathrm{Var}[Y]=\frac{1}{12} &&\end{flalign}$$
> Ora si possono riutilizzare i calcoli per $X=Y\cdot(b-a)+a$

> [!formule]
> $$\begin{flalign}\mathbb{E}[X]=\frac{b+a}{2} &&\end{flalign}$$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}=\mathbb{E}[Y\cdot(b-a)+a]=(b-a)\cdot\mathbb{E}[Y]+a=\frac{b-a}{2}+a={\dots} &&\end{flalign}$$
> 
> $$\begin{flalign}\mathrm{Var}[X]=\frac{(b-a)^{2}}{12} &&\end{flalign}$$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}=\mathrm{Var}[Y\cdot(b-a)+a]=(b-a)^{2}\cdot \mathrm{Var}[Y]={\dots} &&\end{flalign}$$
<div class="page-break" style="page-break-before: always;"></div>

# Variabile aleatoria esponenziale
> [!definizione]
> $\mu=\lambda x$, $Y\sim \mathrm{Pois}(\mu)$
> $$\begin{flalign}P_{Y}(y)=\frac{(\lambda x)^{y}}{y!}\cdot e^{-\lambda x} &&\end{flalign}$$
> con $y\in \mathbb{N}$
> $x$ indica il tempo di funzionamento di un sistema riparabile, $Y$ conta gli eventi guasto
> La probabilità di non osservare guasti in $[0,x]$ è $\mathbb{P}(Y=0)=P_{Y}(0)=e^{-\lambda x}$, $x,\lambda>0$
> Allo stesso modo non osservare guasti entro un tempo $x$ equivale al corretto funzionamento per tale tempo
> $X\sim \mathrm{Exp}(\lambda)$ conta il tempo di funzionamento
> $\mathbb{P}(X>x)=e^{-\lambda x}$ e $F_{X}(x)=\mathbb{P}(X\leq x)=1-e^{-\lambda x}$
> $f_{X}(x)=\lambda\cdot e^{-\lambda x}$, $x>0$
> Viene utilizzata per misurare attese, code, decadimenti e rotture improvvise

> [!formule]
> $$\begin{flalign}\Phi_{X}(t)=\frac{\lambda}{\lambda-t} &&\end{flalign}$$
> con $t<\lambda$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}=\mathbb{E}[e^{tX}]=\int_{0}^{+\infty}e^{-(\lambda-t)\cdot x}\,dx={\dots} &&\end{flalign}$$
> 
> $$\begin{flalign}\mathbb{E}[X]=\frac{d\Phi_{X}(t)}{dt}\bigg\rvert_{y=0}=\frac{1}{\lambda} &&\end{flalign}$$
> $$\begin{flalign}\mathrm{Var}[X]=\frac{1}{\lambda^{2}} &&\end{flalign}$$

> [!approfondimento]-
> Vige della proprietà di assenza di memoria, dati $x_{2}>x_{1}$, $x_{2}=x_{1}+x$ ($x>0$)
> $$\begin{flalign}\mathbb{P}(X>x_{2}|X>x_{1})&=\frac{\mathbb{P}((X>x_{2})\cap(X>x_{1}))}{\mathbb{P}(X>x_{1})}=\frac{\mathbb{P}(X>x_{2})}{\mathbb{P}(X>x_{1})}=\frac{1-F_{X}(x_{2})}{1-F_{X}(x_{1})}\\
&=\frac{e^{-\lambda(x_{1}+x)}}{e^{-\lambda x_{1}}}=\frac{e^{-\lambda x_{1}}\cdot e^{-\lambda x}}{e^{-\lambda x_{1}}}=e^{-\lambda x}=\mathbb{P}(X>x)
&&\end{flalign}$$
<div class="page-break" style="page-break-before: always;"></div>

# Variabile aleatoria gamma
> [!definizione]
> $X_{i}\sim \mathrm{Exp}(\lambda)$, $i=1,\dots,n$
> $X_{n}=\sum_{i=1}^{n}X_{i}\sim \mathrm{Gamma}(n,\lambda)$ può essere pensato come periodo complessivo di funzionamento avendo a disposizione $n$ elementi, utilizzati uno dopo l'altro appena si verifica il guasto del precedente
> $Y$ conta il numero di elementi rotti (quindi di guasti), la probabilità che il periodo di funzionamento sia $>x$ è
> $$\begin{flalign}\mathbb{P}(X>x)=1-F(x)=\sum_{y=0}^{n-1} \frac{(\lambda x)^{y}}{y!}e^{-\lambda x}=\mathbb{P}(Y<n) &&\end{flalign}$$
> ovvero la probabilità che si verifichino $n-1$ guasti

> [!formule]
> $$\begin{flalign}F_{X_{n}}(x)=\sum_{y=n}^{+\infty} \frac{(\lambda x)^{y}}{y!}\cdot e^{-\lambda x} &&\end{flalign}$$
> $$\begin{flalign}f_{X_{n}}(x)=\lambda e^{-\lambda x}\cdot \frac{(\lambda x)^{n-1}}{(n-1)!} &&\end{flalign}$$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}&=\frac{dF_{X_{n}}(x)}{dx}=\sum_{y=n}^{+\infty} \frac{\lambda(\lambda x)^{y-1}}{(y-1)!}\cdot e^{-\lambda x} - \sum_{y=n}^{+\infty} \frac{\lambda(\lambda x)^{y}}{(y)!}\cdot e^{-\lambda x}\\
> > &=\lambda e^{-\lambda x}\left[ \sum_{z=n-1}^{+\infty} \frac{(\lambda x)^{z}}{z!}-\sum_{y=n}^{+\infty} \frac{(\lambda x)^{y}}{y!} \right]={\dots} &&\end{flalign}$$
> 
> $$\begin{flalign}\Phi_{X_{n}}(t)=\left( \frac{\lambda}{\lambda-t} \right)^{n} &&\end{flalign}$$
> con $t<\lambda$

> [!definizione]
> Si definisce una funzione gamma anche per $n$ non interi tale che
> $$\begin{flalign}f_{X_{n}}(x)=\lambda e^{-\lambda x}\cdot \frac{(\lambda x)^{n-1}}{\Gamma(n)} &&\end{flalign}$$
> Se $n\in N$, da prima, $\Gamma(n)=(n-1)!$
> Se invece $\alpha \in \mathbb{R}$
> $$\begin{flalign}\Gamma(\alpha)=\int_{0}^{+\infty}x^{\alpha-1}\cdot e^{-x}\,dx &&\end{flalign}$$
> <div class="page-break" style="page-break-before: always;"></div>
> 
> > [!esempio]-
> > Alcuni valori noti: $\Gamma(\alpha+1)=\alpha \cdot\Gamma(\alpha)$, $\Gamma(1)=1$, $\Gamma\left( \frac{1}{2} \right)=\sqrt{\pi}$

# Variabile aleatoria gaussiana
> [!definizione]
> Anche chiamata **normale**, modello di interpretazione di errori o scostamenti
> Lo scostamento $X-\mu$, con $\mu$ valore vero, accompagna le misure sperimentali di un certo valore $X$ effettuate nelle stesse condizioni
> $$\begin{flalign}U=\frac{X-\mu}{\sigma} &&\end{flalign}$$
> sono gli errori di misura come multipli della loro ampiezza tipica, $\sigma=\sqrt{\mathrm{Var}[X]}$
> $U\sim \mathrm{N}(0,1)$ è variabile normale standard con media $0$ e deviazione $1$, senza errori sistematici
> $$\begin{flalign}f_{U}(u)=\frac{1}{\sqrt{2\pi}}e^{-u^{2}/2} &&\end{flalign}$$
> > [!dimostrazione]-
> >  Se le misure non sono affette da errori sistematici:
> > - $\mathbb{E}[U]=0$
> > - $f_{U}(u)=f_{U}(-u)$ e $\lim_{ u \to +\infty }f_{U}(u)=\lim_{ u \to -\infty }f_{U}(u)=0$
> > - $f_{U}(0)>f_{U}(u)\;\;\forall u\in \mathbb{R}\setminus \{ 0 \}$
> > 
> > Ovvero:
> > $$\begin{flalign} \frac{df_{U}(u)}{du}=-f_{U}(u)\cdot u &&\end{flalign}$$
> > e $f_{U}(u)>0\;\;\forall u\in \mathbb{R}$
> > Una soluzione all'equazione differenziale è $e^{-u^{2}/2}$
> > $f_{U}(u)=k\cdot e^{-u^{2}/2}$, per essere densità
> > $$\begin{flalign}1&=\int_{-\infty}^{+\infty}k\cdot e^{-u^{2}/2}\,du=2k\int_{0}^{+\infty}e^{-u^{2}/2}\,du\\
> > &\;\;\;t=\frac{u^{2}}{2}\;\;\;u=\sqrt{2t}\;\;\;du=\frac{1}{\sqrt{2}}t^{(1/2)-1}\\
> > &=\frac{2}{\sqrt{2}}k\int_{0}^{+\infty}t^{(1/2)-1}\cdot e^{-t}\,dt=\frac{2}{\sqrt{2}}k\cdot\Gamma\left( \frac{1}{2} \right)=\frac{2\sqrt{\pi}}{\sqrt{2}}k\implies k=\frac{1}{\sqrt{2\pi}}&&\end{flalign}$$
> <div class="page-break" style="page-break-before: always;"></div>
> 
> $X=\mu+\sigma U\sim \mathrm{N}(\mu,\sigma^{2})$ è variabile aleatoria normale (non standard)
> $$\begin{flalign}f_{X}(x)=\frac{1}{\sqrt{2\pi}}e^{-(1/2)((X-\mu)/\sigma)}\left| \frac{du}{dx}\right|=\frac{1}{\sigma \sqrt{2\pi}}e^{-(1/2)((x-\mu)/\sigma)^{2}} &&\end{flalign}$$
> con $\sigma>0$

> [!formule]
> $\Phi_{U}(t)=e^{t^{2}/2}$
> 
> $\Phi_{X}(t)=e^{t\mu+t^{2}\sigma^{2}/2}$
> 
> $\mathbb{E}[X]=\mu$
> > [!dimostrazione]-
> > ${\dots}=\mathbb{E}[\mu+\sigma U]=\mu+\sigma\mathbb{E}[U]={\dots}$
> 
> $\mathrm{Var}[X]=\sigma^{2}$

> [!approfondimento]-
> $X_{1},X_{2}\sim \mathrm{N}(0,1)$, $X_{1}\perp \!\!\! \perp X_{2}$, $Y=X_{1}+X_{2}$
> $$\begin{flalign}\Phi_{Y}(t)=\Phi_{X_{1}}(t)\cdot \Phi_{X_{2}}(t)=e^{t^{2}/2}\cdot e^{t^{2}/2}=e^{2t^{2}2} &&\end{flalign}$$
> Quindi $Y\sim \mathrm{N}(0,2)$
> 
> $X_{i}\sim \mathrm{N}(\mu_{i},\sigma_{i}^{2})$, $X_{i}\perp \!\!\! \perp X_{j}\;\;i\neq j$, $a_{i}\in \mathbb{R}$ ($i,j=1,\dots,n$)
> $Y=\sum_{i=1}^{n}a_{i}X_{i}$
> $\mathbb{E}[Y]=\sum_{i=1}^{n}a_{i}\mu_{i}=\bar{\mu}$
> $\mathrm{Var}[X]=\sum_{i=1}^{n}(a_{i}\sigma_{i})^{2}=\bar{\sigma}^{2}$
> $$\begin{flalign}\Phi_{Y}(t)=\prod_{i=1}^{n}\Phi_{X_{i}}(t)=e^{t\bar{\mu}+t^{2}\bar{\sigma}^{2}/2} &&\end{flalign}$$
> Quindi $Y\sim \mathrm{N}(\bar{\mu},\bar{\sigma}^{2})$
> 
> $X_{i}\sim \mathrm{N}(\mu_{i},\sigma_{i}^{2})$, $X_{i}\perp \!\!\! \perp X_{j}\;\;i\neq j$, $a_{i},b_{i}\in \mathbb{R}$ ($i,j=1,\dots,n$)
> $Y=\sum_{i=1}^{n}a_{i}X_{i}$, $Z=\sum_{i=1}^{n}b_{i}X_{i}$
> $\mathrm{Cov}(Y,Z)=\mathbb{E}[(Y-\mathbb{E}[Y])(Z-\mathbb{E}[Z])]=\sum_{i=1}^{n}a_{i}b_{i}\sigma_{i}^{2}$
> Se $\sigma_{i}=\sigma\;\;\forall i\in \{ 1,\dots,n \}$
> $\mathrm{Cov}(Y,Z)=0\iff \sum_{i=1}^{n}a_{i}b_{i}=0$, $Y$ e $Z$ sono dette ortogonali
<div class="page-break" style="page-break-before: always;"></div>

# Variabile aleatoria normale bivariata
> [!definizione]
> $X\sim \mathrm{N}(\mu_{1},\sigma_{1}^{2})$, $Y\sim \mathrm{N}(\mu_{2},\sigma_{2}^{2})$, $X\perp \!\!\! \perp Y$, per semplicità $\mu_{1}=\mu_{2}=0$
> Allora si può definire
> $$\begin{flalign}f(x,y)=\frac{1}{2\pi\sigma_{1}\sigma_{2}}e^{-(1/2)(x^{2}/\sigma_{1}^{2}+y^{2}/\sigma_{2^{2}})} &&\end{flalign}$$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}=f_{X}(x)\cdot f_{Y}(y)=\frac{1}{\sqrt{2\pi\sigma_{1}^{2}}}e^{-(1/2)(x^{2}/\sigma_{1}^{2})}\cdot\frac{1}{\sqrt{2\pi\sigma_{2}^{2}}}e^{-(1/2)(y^{2}/\sigma_{2}^{2})}={\dots} &&\end{flalign}$$
> 
> $(X,Y)$ si dice normale bivariata
> 
> $X_{i}\sim \mathrm{N}(0,1)$, $X_{i}\perp \!\!\! \perp X_{j}\;\;i\neq j$ ($i,j=1,\dots,n$)
> Allora
> $$\begin{flalign}f(x_{1},\dots,x_{n})=\frac{1}{(\sqrt{2\pi})^{n}}e^{-(1/2)(x_{1}^{2}+\dots+x_{n}^{2})} &&\end{flalign}$$
> Il vettore $(X_{1},\dots,X_{n})$ si dice gaussiana multivariata standard
<div class="page-break" style="page-break-before: always;"></div>

# Teorema centrale del limite
> [!teorema]
> $X_{i}$ variabile aleatoria, $X_{i}\perp \!\!\! \perp X_{j}\;\;i\neq j$, tutte seguenti la stessa distribuzione con media $\mu$ e varianza $\sigma^{2}$ ($i,j=1,\dots,n$)
> $Y=\sum_{i=1}^{n}X_{i}$ converge in distribuzione a $\mathrm{N}(n\mu,n\sigma^{2})$
> > [!dimostrazione]-
> > Si dice che una successione $\{X_{n}\}_{n\in \mathbb{N}}$ di variabili aleatorie converge in distribuzione a $X$ se $\lim_{ n \to +\infty }F_{X_{n}}(x)=F_{X}(x)\;\;\forall x$ in cui $F_{X}(x)$ è continua
> > $$\begin{flalign}Y_{i}=\frac{X_{i}-\mu}{\sigma} &&\end{flalign}$$
> > $$\begin{flalign}Z=\frac{\left( \sum_{i=1}^{n}X_{i} \right) -n\mu}{\sqrt{n}\sigma}=\sum_{i=1}^{n} \frac{X_{i}-\mu}{\sqrt{n}\sigma}=\frac{1}{\sqrt{n}}\sum_{i=1}^{n}Y_{i}\sim \mathrm{N}(0,1)  &&\end{flalign}$$
> > $$\begin{flalign}\Phi_{Z}(t)&=\mathbb{E}[e^{tZ}]=\mathbb{E}\left[ e^{t\left( \frac{1}{\sqrt{n}}\sum_{i=1}^{n}Y_{i} \right)} \right]=\mathbb{E}\left[ \prod_{i=1}^{n}e^{\frac{t}{\sqrt{n}}Y_{i}} \right]=\prod_{i=1}^{n}\mathbb{E}\left[e^{\frac{t}{\sqrt{n}}Y_{i}}\right]\\
> > &=\prod_{i=1}^{n}\mathbb{E}\left[ 1+\frac{t}{\sqrt{n}}Y_{i}+\left( \frac{t}{\sqrt{n}} \right)^{2}\cdot \frac{Y_{i}^{2}}{2!}+\dots \right]\\
> > &=\prod_{i=1}^{n}\left[ \mathbb{E}[1]+\frac{t}{\sqrt{n}}\mathbb{E}[Y_{i}]+\left( \frac{t}{\sqrt{n}} \right)^{2}\cdot \frac{\mathbb{E}[Y_{i}^{2}]}{2!}+\dots \right]\\
> > &\;\;\;\mathbb{E}[1]=1\;\;\;\mathbb{E}[Y_{i}]=\frac{\mathbb{E}[X_{i}]-\mu}{\sigma}=\frac{\mu-\mu}{\sigma}=0\;\;\;\mathbb{E}[Y_{i}^{2}]=1\\
> > &=\prod_{i=1}^{n}\left[ 1+0+\frac{1}{n}\left( \frac{t^{2}}{2!}+\frac{t^{3}}{\sqrt{n}}\cdot \frac{\mathbb{E}[Y_{i}^{3}]}{3!}+\dots \right) \right]&&\end{flalign}$$
> > $\mathbb{E}[Y_{i}]=\mathbb{E}[Y_{j}]\;\;\forall i,j=1,\dots,n$ poiché hanno la stessa distribuzione
> > $$\begin{flalign}{\dots}=\left[ 1+\frac{1}{n}\left( \frac{t^{2}}{2!}+\frac{t^{3}}{\sqrt{n}}\cdot \frac{\mathbb{E}[Y_{i}^{3}]}{3!}+\dots \right) \right]^{n} &&\end{flalign}$$
> > $$\begin{flalign}\lim_{ n \to +\infty } \frac{n}{f(n)}=\pm \infty\implies \lim_{ n \to +\infty }\left[ 1+\frac{f(n)}{n} \right]^{n}=e^{\lim_{ n \to +\infty }f(n) }  &&\end{flalign}$$
> > $$\begin{flalign}n\to +\infty\implies{\dots}=e^{\lim_{ n \to +\infty } \left( \frac{t^{2}}{2!}+\frac{t^{3}}{\sqrt{n}}\cdot \frac{\mathbb{E}[Y_{i}^{3}]}{3!}+\dots \right) }=e^{t^{2}/2} &&\end{flalign}$$
> > Ovvero è la funzione di generazione dei momenti della gaussiana standard
> > $Y=Z\sqrt{n}\sigma+n\mu\implies{\dots}$
<div class="page-break" style="page-break-before: always;"></div>

# Approssimazione normale della distribuzione binomiale
> [!teorema] Teorema di De Moivre-Laplace
> Una variabile aleatoria $\mathrm{Bin}(n,p)$ per $n$ grandi ha approssimativamente la stessa distribuzione di una $\mathrm{N}(np,np(1-p))$
> 
> $X_{i}\sim \mathrm{Bin}(n,p)$, $X_{i}\perp \!\!\! \perp X_{j}\;\;i\neq j$
> $S_{n}=\sum_{i=1}^{n}X_{i}$ è il numero di successi
> Se $n\to +\infty$
> $$\begin{flalign} \frac{S_{n}-np}{\sqrt{np(1-p)}}\sim \mathrm{N}(0,1) &&\end{flalign}$$
> $U\sim \mathrm{N}(0,1)$
> Se $a<b$ e $np(1-p)>10$
> $$\begin{flalign}\lim_{ n \to \infty }\mathbb{P}\left( a\leq \frac{S_{n}-np}{\sqrt{np(1-p)}}\leq b \right)=F_{U}(b)-F_{U}(a)  &&\end{flalign}$$
> è una buona approssimazione

> [!approfondimento]- Correzione di continuità
> Nell'approssimazione di una variabile aleatoria discreta con una continua per $t$ si considera l'intervallo $t-\frac{1}{2}\leq y\leq t+\frac{1}{2}$
