# Variabile aleatoria
> [!definizione] Definizione
$(S,\mathcal{A},\mathbb{P})$ spazio di probabilità
La funzione $X:S\to \mathbb{R}$ è variabile aleatoria $\iff X$ è misurabile in $(S,\mathcal{A})$

Gli elementi misurabili di $S$ sono quelli in $\mathcal{A}$

# Funzione di ripartizione
> [!definizione] Definizione
> Anche chiamata **distribuzione cumulativa** o **Cumulative Distribution Function**, fornisce la probabilità dell'evento $(X\in(-\infty,x))\;\;\forall x \in \mathbb{R}$
> e si indica con
> $$\begin{flalign}F_{X}(x)=F(x)=\mathbb{P}(X\leq x) &&\end{flalign}$$
> Proprietà:
> - è continua a destra: $F(x)=\lim_{ \epsilon \to 0 }F(x+\epsilon)=F(x^{+})$
> - è monotona crescente: se $x_{2}>x_{1}\implies F(x_{2})\geq F(x_{1})$
> - $\lim_{ x \to -\infty }F(x)=0$ e $\lim_{ x \to +\infty }F(x)\implies F(x)\in[0,1] \;\;\forall x \in \mathbb{R}$

> [!formule]
> $\mathbb{P}(X>x)=1-F(x)$
> > [!dimostrazione]-
> > ${\dots}=1-\mathbb{P}(X\leq x)={\dots}$
> 
> $\mathbb{P}(x_{1}<X\leq x_{2})=F(x_{2})-F(x_{1})$
> > [!dimostrazione]-
> $x_{2}>x_{1}\implies \mathbb{P}(X\leq x_{1})+\mathbb{P}(x_{1}<X\leq x_{2})=\mathbb{P}(X\leq x_{2})$
> 
> $\mathbb{P}(X=x)=F(x)-F(x^{-})$
> > [!dimostrazione]-
> > $x_{1}=x-\epsilon,\;x_{2}=x\;\;\forall\epsilon>0\implies$$\lim_{ \epsilon \to 0 }\mathbb{P}(x_{1}<X\leq x_{2})=\lim_{ \epsilon \to 0 }\mathbb{P}(x-\epsilon<X\leq x)$
> 
> $$\begin{flalign}F(x|X>x_{0})=\frac{F(x)-F(x_{0})}{1-F(x_{0})} &&\end{flalign}$$
> > [!dimostrazione]-
> > $(X>x_{0})$ evento, $x>x_{0}$$$\begin{flalign}{\dots}=\mathbb{P}(X\leq x|X>x_{0})=\frac{\mathbb{P}((X\leq x)\cap(X> x_{0}))}{\mathbb{P}(X>x_{0})}=\frac{\mathbb{P}(x_{0}<X\leq x)}{1-F(x_{0})}={\dots}&&\end{flalign}$$

# Massa di probabilità
$X$ è detta variabile aleatoria discreta se la funzione di ripartizione è a gradini, le discontinuità hanno ampiezza $F(x)-F(x^{-})=\mathbb{P}(X=x)$

> [!definizione]
> $P(x)=\mathbb{P}(X=x)$ è detta funzione massa di probabilità o anche **Probability Mass Function**
> Fornisce la probabilità che la variabile aleatoria assuma un certo valore, pertanto
> $$\begin{flalign}F(x_{1})=\sum_{x=x_{1}}P(x)  &&\end{flalign}$$
> $$\begin{flalign}\mathbb{P}(x_{i}<X\leq x_{j})=\sum_{x_{i}<x\leq x_{j}}P(x)\;\;x_{i}<x_{j}  &&\end{flalign}$$
> Soddisfa le seguenti proprietà:
> $$\begin{flalign}\sum_{-\infty<x<+\infty}P(x)=1\land P(x)\geq0\;\;\forall x \in \mathbb{R}  &&\end{flalign}$$

> [!formule]
> $\mathbb{P}(x<X)=F(x)-P(x)$
> > [!dimostrazione]-
> > ${\dots}=\mathbb{P}(x\leq X)-\mathbb{P}(x=X)={\dots}$

> [!esempio]-
> ![Massa di probabilità](Esempi.md#Massa%20di%20probabilità)

# Densità di probabilità
$X$ è detta variabile aleatoria continua se la funzione di ripartizione è continua

> [!definizione]
> $$\begin{flalign}f(x)=\lim_{ \Delta x \to 0 } \frac{F(x+\Delta x)-F(x)}{\Delta x}=\frac{dF(x)}{dx}  &&\end{flalign}$$
> è detta funzione densità di probabilità
> Fornisce la probabilità che la variabile aleatoria assuma uno specifico valore, quindi
> $$\begin{flalign}F(x_{1})=\int_{-\infty}^{x_{1}}f(t) \,dt &&\end{flalign}$$
> $$\begin{flalign}\mathbb{P}(x_{1}\leq X\leq x_{2})=\int_{x_{1}}^{x_{2}} f(t)\,dt\;\;x_{1}\leq x_{2} &&\end{flalign}$$
> Soddisfa le seguenti proprietà:
$$\begin{flalign}\int_{-\infty}^{+\infty}f(t) \,dt=1\land f(x)\geq0\;\;\forall x \in \mathbb{R} &&\end{flalign}$$

> [!formule]
> $\mathbb{P}(X< x)=\mathbb{P}(X\leq x)$
> > [!dimostrazione]-
> > $$\begin{flalign} {\dots}=\mathbb{P}(X\leq x)-\mathbb{P}(X=x)=\int_{-\infty}^{x}f(t) \,dt-\int_{x}^{x} f(t)\,dt=\int_{-\infty}^{x} f(t)\,dt={\dots}&&\end{flalign}$$

> [!esempio]-
> ![Densità di probabilità](Esempi.md#Densità%20di%20probabilità)
