# Calcolo delle probabilità
Studia esperimenti casuali il cui esito non è prevedibile con certezza
Esperimenti casuali: affermazioni logiche o eventi
Non prevedibile con certezza: aleatorio o stocastico
Giudizio: probabilità, numero tra $0$ (impossibile) e $1$ (certo)

# Teorie
### Classica
Laplace, 1812
La probabilità è il rapporto tra i casi favorevoli e i casi totali

### Frequentista
Von Mises
Legge empirica del caso: in una serie di prove ripetute (nelle stesse condizioni) ciascun evento possibile avviene con una certa frequenza
La probabilità è il limite a cui tende la frequenza all'aumentare delle prove

### Soggettiva
De Finetti e Savage
La probabilità di un evento è la misura del grado di fiducia che un individuo coerente attribuisce secondo le sue informazioni e opinioni al verificarsi dell'evento
Oppure è il prezzo per cui l'individuo è disposto a scommettere per ottenere una vincita unitaria se si avvera

### Assiomatica
Kolmogorov, 1933
Non si occupa del giudizio, fornisce postulati e teoremi per costruirlo

# Spazio di probabilità
### Operazioni
$A,B$ eventi
Somma logica: $A\cup B$ si verifica se almeno un evento si verifica
Prodotto logico: $A\cap B$ si verifica se entrambi gli eventi si verificano
Complementare: $\bar{A}$ o $A^{C}$ si verifica quando $A$ non si verifica
Unione numerabile di eventi tra loro incompatibili: $E_{i}:E_{i}\cap E_{j}=\emptyset\;\;\forall i\neq j$ è partizione di $S$ se $S=\bigcup\limits_{i}E_{i}$
### Definizione
E' una terna $(S,\mathcal{A},\mathbb{P})$

### $S$
Spazio campione/campionario, contiene tutti i possibili eventi

### $\mathcal{A}$
Famiglia di sottoinsiemi di $S$ a cui si può assegnare una probabilità
Proprietà:
- $S\in \mathcal{A}$
- Se $A\in \mathcal{A}\implies \bar{A}\in \mathcal{A}$
- Se $\{ A_{i} \}\subset \mathcal{A}\implies \bigcup\limits_{i=1}^{\infty}A_{i}\in \mathcal{A}\land \bigcap\limits_{i=1}^{\infty}A_{i}\in \mathcal{A}$

### $\mathbb{P}$
Misura di probabilità su $(S,\mathcal{A})$
$\mathbb{P}:\mathcal{A}\to[0,1]$
Proprietà:
- $\forall A\in \mathcal{A}\;\;\mathbb{P}(A)\geq0\land \mathbb{P}(S)=1$
- Se $\{ A_{i} \}\subset \mathcal{A}:A_{i}\cap A_{j}=\emptyset\;\;\forall i\neq j\implies \mathbb{P}\left( \bigcup\limits_{i}A_{i} \right)=\sum\limits_{i}\mathbb{P}(A_{i})$

### Costruzione di $S$
$A,B,C$ eventi
E' possibile costruire $S$ nel seguente modo
$(A\cup \bar{A})\cap(B\cup \bar{B})\cap(C\cup \bar{C})=ABC\cup AB\bar{C}\cup A\bar{B}C\cup A\bar{B}\bar{C}\cup \bar{A}BC\cup \bar{A}B\bar{C}\cup \bar{A}\bar{B}C\cup \bar{A}\bar{B}\bar{C}$
