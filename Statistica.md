> [!definizione]
> Studia le popolazioni di individui, ovvero gruppi che condividono una caratteristica specifica
> Si occupa di analizzare ed interpretare i dati
> 
> ### Campione
> Nell'impossibilità di osservare l'intera popolazione spesso si osserva un campione, ovvero un sottoinsieme ottenuto tramite un processo di selezione
> Deve essere rappresentativo, quindi ogni elemento deve avere la stessa probabilità di essere considerato nel campione
> 
> ### Parametro
> Misura numerica calcolata sull'intera popolazione, solitamente fissa ma sconosciuta
> 
> ### Stimatore
> O statistica, è una misura calcolata su un campione nota ma variabile da campione a campione

---

# Statistica descrittiva
> [!definizione]
> Si concentra sull'analisi dei dati osservati con l'obiettivo di sintetizzare le informazioni contenute nei dati di un campione
> Si possono rappresentare queste informazioni tramite grafici e tabelle

## Variabili
> [!definizione]
> Si distinguono tra:
> - Numeriche (quantitative):
>   - Discrete
>   - Continue
> - Categoriche (qualitative)

## Indici di posizione e dispersione
> [!definizione]
> ### Media aritmetica
> Anche chiamata media campionaria
> $$\begin{flalign}\bar{x}=\frac{1}{n}\sum_{i=1}^{n}x_{i} &&\end{flalign}$$
> Per i dati raggruppati in classi si moltiplica il valore centrale per la frequenza assoluta e si divide per il numero totale di osservazioni
> 
> ### Mediana
> Valore che divide il campione (dati ordinati) in due parti
> - dispari: valore centrale
> - pari: media aritmetica dei due valori centrali
> 
> ### Quartile e percentile
> Valori che dividono il campione in quarti e percentuali
> Si applica la stessa regola della mediana
> 
> ### Range
> Distanza tra il minimo ed il massimo
> $\mathrm{Range}=x_{\mathrm{max}}-x_{\mathrm{min}}$
> 
> ### IQR
> Range interquartile
> $\mathrm{IQR}=Q_{3}-Q_{1}$
> 
> ### Deviazione Standard
> $$\begin{flalign}\sigma=\sqrt{\frac{1}{n}\sum_{i=1}^{n}(x_{i}-\bar{x})^{2}} &&\end{flalign}$$
> 

## Tabelle
> [!definizione]
> ### Di frequenza
> Si suddividono i dati in classi e si calcolano la frequenza relativa e cumulativa

## Grafici
> [!definizione]
> ### Istogramma
> Ogni classe è rappresentata da un rettangolo la cui area è proporzionale alla frequenza
> 
> ### Box and whiskers plot
> Fornisce una rappresentazione visiva della distribuzione dei dati, permette di confrontare la distribuzione dei dati tra diversi gruppi o categorie e di identificare simmetrie o asimmetrie
> - Baffi: linee verticali che si estendono dal box fino al massimo e minimo escludendo gli outliers
> - Box: rappresenta il $50\%$ centrale dei dati compreso tra $Q_{1}$ e $Q_{3}$, una linea all'interno rappresenta la mediana
> - Outliers: punti al di fuori dei baffi che rappresentano i valori che distano più di $1.5\cdot \mathrm{IQR}$ dalla scatola

---

# Statistica inferenziale
> [!definizione]
> Cerca di fare affermazioni riguardanti l'intera popolazione basandosi sulle informazioni ricavate da un campione, espresse in termini di probabilità

## Stimatore
> [!definizione]
> Si identifica il campione con una famiglia di variabili aleatorie$X_{1},\dots,X_{n}$ stocasticamente indipendenti con stessa distribuzione le cui CDF/PDF/PMF dipendono da un parametro $\theta$ spesso ignoto, l'obiettivo è determinarlo
> Una regola che dice come calcolare la stima di $\theta$ o $\psi(\theta)$ dal campione $x_{1},\dots,x_{n}$ è detta stimatore
> 
> $T$ funzione delle variabili aleatorie $X_{1},\dots,X_{n}$ è variabile aleatoria, si indica con $T=t(X_{1},\dots X_{n})$ ed è detta statistica o stimatore di $\theta$ o $\psi(\theta)$ se osservato il campione e si utilizza $t(x_{1},\dots,x_{n})$ al posto del parametro

> [!esempio]- Esempi
> $T_{1}:x_{1}$
> $T_{2}:x_{1}+{\dots}+x_{n}$
> $T_{3}: \frac{1}{n}(x_{1},{\dots},x_{n})$
> $T_{4}:\sqrt[n]{x_{1}\cdot{\dots}\cdot x_{n}}$

## Correttezza
> [!definizione]
> Uno stimatore si dice corretto o **non distorto** per $\theta$ o $\psi(\theta)$ se $\mathbb{E}[T]=\theta\;\;\forall\theta$

> [!esempio]- Esempi
> $\mathbb{E}[T_{1}]=\theta$, corretto
> $\mathbb{E}[T_{2}]=\mathbb{E}[X_{1}+{\dots}+X_{n}]=\sum_{i=1}^{n}X_{i}=n\theta$, non corretto
> $\mathbb{E}[T_{3}]=\frac{1}{n}n\theta=\theta$, corretto
> $\mathbb{E}[T_{4}]\leq\theta$, non corretto

## Consistenza
> [!definizione]
> Uno stimatore si dice consistente se $\lim_{ n \to +\infty }\mathrm{Var}[T]=0$ ovvero più grande è il campione più si riduce l'incertezza

> [!esempio]- Esempi
> $\lim_{ n \to +\infty }\mathrm{Var}[T_{1}]=\mathrm{Var}[X_{1}]$, non consistente
> $\lim_{ n \to +\infty }\mathrm{Var}[T_{3}]=\lim_{ n \to +\infty }\mathrm{Var}\left[ \frac{1}{n}(X_{1}+{\dots}+X_{n}) \right]=\lim_{ n \to +\infty } \frac{\sigma^{2}}{n}=0$, consistente

## Stimatori per la media
> [!formule]
> Per $\theta$:
> $$\begin{flalign} \frac{1}{n}\sum_{i=1}^{n}x_{i} &&\end{flalign}$$
> Per $\theta^{-1}$:
> $$\begin{flalign} \frac{n-1}{\sum_{i=1}^{n}x_{i}} &&\end{flalign}$$

## Stimatori per la varianza
> [!formule]
> Se $\mu$ è noto:
> $$\begin{flalign} \frac{1}{n}\sum_{i=1}^{n}(x_{i}-\mu)^{2} &&\end{flalign}$$
> > [!dimostrazione]-
> > $$\begin{flalign}\mathbb{E}[T]&=\mathbb{E}\left[ \frac{1}{n}\sum_{i=1}^{n}(X_{i}-\mu)^{2} \right]=\frac{1}{n}\mathbb{E}\left[ \sum_{i=1}^{n}(X_{i}^{2}-2X_{i}\mu+\mu^{2}) \right]\\
> > &=\frac{1}{n}\mathbb{E}\left[ \sum_{i=1}^{n}X_{i}^{2}-2\mu \sum_{i=1}^{n}X_{i}+n\mu^{2} \right]=\frac{1}{n}\left[ \sum_{i=1}^{n}\mathbb{E}[X_{i}^{2}]-2\mu \sum_{i=1}^{n}\mathbb{E}[X_{i}]+n\mu^{2} \right]\\
> > &=\frac{1}{n}\left[ \sum_{i=1}^{n}\mathbb{E}[X_{i}^{2}]-2n\mu^{2}+n\mu^{2} \right]=\frac{1}{n}\left[ \sum_{i=1}^{n}(\mathbb{E}[X_{i}^{2}]-\mathbb{E}[X_{i}]^{2}) \right]=\frac{1}{n}n\sigma^{2}=\sigma^{2} &&\end{flalign}$$
> 
> Se $\mu$ non è noto:
> $$\begin{flalign} \frac{1}{n-1}\sum_{i=1}^{n}(x_{i}-\bar{x})^{2}=\frac{1}{n-1}\left[\sum_{i=1}^{n}x_{i}^{2}-n\bar{x}^{2}\right] &&\end{flalign}$$
> anche chiamata varianza campionaria

## Intervallo di confidenza
> [!definizione]
> Un intervallo di confidenza o **Confidence Interval** di livello $\alpha$ per un parametro $\theta$ o $\psi(\theta)$ è un intervallo $I_{X}:\mathbb{P}(\theta \in I_{X})=\alpha$, dipende dalle osservazioni $X_{1},\dots,X_{n}$ quindi è un'intervallo aleatorio
