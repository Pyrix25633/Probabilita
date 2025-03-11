# Probabilità condizionata
Si definisce probabilità condizionata il nuovo giudizio di probabilità che muta visto l'accadere di un'altro evento
$A,B$ eventi, si indica $\mathbb{P}(B|A)$ oppure $\mathbb{P}_{A}(B)$ come $\mathbb{P}(B|A)\cdot \mathbb{P}(A)=\mathbb{P}(A\cap B)$
Se $\mathbb{P}(A)\neq0\implies$
$$\begin{flalign}\mathbb{P}(B|A)=\frac{\mathbb{P}(A\cap B)}{\mathbb{P}(A)} &&\end{flalign}$$

# Indipendenza stocastica
$A,B$ eventi si dicono stocasticamente indipendenti $A\perp \!\!\! \perp B\iff \mathbb{P}(A\cap B)=\mathbb{P}(A)\cdot \mathbb{P}(B)$ ovvero $\mathbb{P}(A|B)=\mathbb{P}(A)\land \mathbb{P}(B|A)=\mathbb{P}(B)$

$A,B$ eventi dipendenti
Se $\mathbb{P}(A\cap B)>\mathbb{P}(A)\cdot \mathbb{P}(B)\implies$ si dicono positivamente correlati
Se $\mathbb{P}(A\cap B)<\mathbb{P}(A)\cdot \mathbb{P}(B)\implies$ si dicono negativamente correlati

# Probabilità totali condizionate
$A,B$ eventi
$\mathbb{P}(A)=\mathbb{P}(A\cap B)+\mathbb{P}(A\cap \bar{B})=\mathbb{P}(B)\cdot \mathbb{P}(A|B)+\mathbb{P}(\bar{B})\cdot \mathbb{P}(A|\bar{B})$

# Calcolo combinatorio
$S$ finito
Il calcolo si distingue in tre casi in base a ordine e ripetizioni

### Disposizioni
Si dice disposizione di $n$ oggetti di classe $k\leq n$ ogni ordinamento di $k$ oggetti scelti tra $n$
Senza ripetizioni:
$$\begin{flalign}\mathrm{D}_{n,k}=\mathrm{D}^{n}_{k}=n\cdot(n-1)\cdot{\dots}\cdot(n-k+1)=\frac{n!}{(n-k)!} &&\end{flalign}$$

Con ripetizioni:
$$\begin{flalign}D'_{n,k}=D_{n,k}^{r}=n^{k} &&\end{flalign}$$

### Permutazioni
Si dice permutazione di $n$ oggetti ogni ordinamento composto da tutti gli $n$ oggetti
Senza ripetizioni:
$$\begin{flalign}\mathrm{P}_{n}=\mathrm{D}^{n}_{n}=n! &&\end{flalign}$$

Con ripetizioni:
$n$ oggetti di cui $d$ distinti, $n=k_{1}+{\dots}+k_{d}$ dove ogni elemento $j$ è presente $k_{j}$ volte
$$\begin{flalign}\mathrm{P}_{n}^{k_{1},\dots,k_{d}}=\frac{n!}{k_{1}!\cdot{\dots}\cdot k_{d}!} &&\end{flalign}$$

### Combinazioni
Si dice combinazione semplice di $n$ oggetti di classe $k\leq n$ ogni sottoinsieme costituito da $k$ elementi tra gli $n$
Senza ripetizioni:
$$\begin{flalign}\mathrm{C}_{k}^{n}=\mathrm{C}_{n,k}=\binom{n}{k}=\frac{n!}{(n-k)!\cdot k!} &&\end{flalign}$$

Con ripetizioni:
$$\begin{flalign}\mathrm{C}'_{n,k}=\mathrm{C}_{n,k}^{r}=\binom{n+k-1}{k}=\frac{(n+k-1)!}{(n-1)!\cdot k!} &&\end{flalign}$$

# Teorema di Bayes
$A,C$ eventi
$$\begin{flalign}\mathbb{P}(C|A)=\frac{\mathbb{P}(C)\cdot \mathbb{P}(A|C)}{\mathbb{P}(A)}=\frac{\mathbb{P}(C)\cdot \mathbb{P}(A|C)}{\mathbb{P}(C)\cdot \mathbb{P}(A|C)+\mathbb{P}(\bar{C})\cdot \mathbb{P}(A|\bar{C})} &&\end{flalign}$$
$E_{1},\dots,E_{n},A$ eventi $:E_{i}\cap E_{j}=\emptyset\;\;\forall i\neq j$ e $\bigcup\limits_{i=1}^{n}E_{i}=S$
$$\begin{flalign}\mathbb{P}(E_{j}|A)=\frac{\mathbb{P}(E_{j})\cdot \mathbb{P}(A|E_{j})}{\sum_{i=1}^{n} \mathbb{P}(E_{i})\cdot \mathbb{P}(A|E_{i})} &&\end{flalign}$$
