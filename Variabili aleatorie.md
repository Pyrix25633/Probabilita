# Variabile aleatoria
$(S,\mathcal{A},\mathbb{P})$ spazio di probabilità
La funzione $X:S\to \mathbb{R}$ è variabile aleatoria $\iff X$ è misurabile in $(S,\mathcal{A})$
Gli elementi misurabili di $S$ sono quelli in $\mathcal{A}$

# Funzione di ripartizione
Anche chiamata distribuzione cumulativa, fornisce la probabilità dell'evento $(X\in(-\infty,x)\;\;\forall x \in \mathbb{R}$ e si indica con
$$\begin{flalign}F_{X}(x)=F(x)=\mathbb{P}(X\leq x) &&\end{flalign}$$
Proprietà:
- è continua a destra: $F(x)=\lim_{ \epsilon \to 0 }F(x+\epsilon)=F(x^{+})$
- è monotona crescente: se $x_{2}>x_{1}\implies F(x_{2})\geq F(x_{1})$
- $\lim_{ x \to -\infty }F(x)=0$ e $\lim_{ x \to +\infty }F(x)\implies F(x)\in[0,1] \;\;\forall x \in \mathbb{R}$

Per definizione $\mathbb{P}(X\leq x)=F(x)\implies \mathbb{P}(X>x)=1-F(x)$

Se $x_{2}>x_{1}\implies \mathbb{P}(X\leq x_{1})+\mathbb{P}(x_{1}<X\leq x_{2})=\mathbb{P}(X\leq x_{2})\implies$$\mathbb{P}(x_{1}<X\leq x_{2})=F(x_{2})-F(x_{1})$

Inoltre se $x_{1}=x-\epsilon,\;x_{2}=x\;\;\forall\epsilon>0\implies$$\mathbb{P}(X=x)=\lim_{ \epsilon \to 0 }\mathbb{P}(x_{1}<X\leq x_{2})=\lim_{ \epsilon \to 0 }\mathbb{P}(x-\epsilon<X\leq x)=F(x)-F(x^{-})$

$X$ variabile aleatoria, $(X>x_{0})$ evento, $x>x_{0}$
$$\begin{flalign}F(x|X>x_{0})=\mathbb{P}(X\leq x|X>x_{0})=\frac{\mathbb{P}((X\leq x)\cap(X\geq x_{0}))}{\mathbb{P}(X>x_{0})}= &&\end{flalign}$$
$$\begin{flalign}=\frac{\mathbb{P}(x_{0}<X\leq x)}{1-F(x_{0})}=\frac{F(x)-F(x_{0})}{1-F(x_{0})} &&\end{flalign}$$
