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

# Statistica descrittiva
> [!definizione]
> Si concentra sull'analisi dei dati osservati con l'obiettivo di sintetizzare le informazioni contenute nei dati di un campione
> Si possono rappresentare queste informazioni tramite grafici e tabelle

### Variabili
> [!definizione]
> Si distinguono tra:
> - Numeriche (quantitative):
>   - Discrete
>   - Continue
> - Categoriche (qualitative)

### Indici di posizione e dispersione
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

### Tabelle
> [!definizione]
> ### Di frequenza
> Si suddividono i dati in classi e si calcolano la frequenza relativa e cumulativa

### Grafici
> [!definizione]
> ### Istogramma
> Ogni classe è rappresentata da un rettangolo la cui area è proporzionale alla frequenza
> 
> ### Box and whiskers plot
> Fornisce una rappresentazione visiva della distribuzione dei dati, permette di confrontare la distribuzione dei dati tra diversi gruppi o categorie e di identificare simmetrie o asimmetrie
> - Baffi: linee verticali che si estendono dal box fino al massimo e minimo escludendo gli outliers
> - Box: rappresenta il $50\%$ centrale dei dati compreso tra $Q_{1}$ e $Q_{3}$, una linea all'interno rappresenta la mediana
> - Outliers: punti al di fuori dei baffi che rappresentano i valori che distano più di $1.5\cdot \mathrm{IQR}$ dalla scatola

# Statistica inferenziale
> [!definizione]
> Cerca di fare affermazioni riguardanti l'intera popolazione basandosi sulle informazioni ricavate da un campione, espresse in termini di probabilità
