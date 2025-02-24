# Funzioni di più variabili e funzioni vettoriali
$f:A\subset \mathbb{R}^{n}\to \mathbb{R}^{k}$ è una funzione
- di più variabili se $k=1 \land n\geq2$
- vettoriale di più variabili se $k\geq2 \land n\geq2$

# Insieme
$A\subset \mathbb{R}^{n}$

### Intorno
Si chiama intorno sferico di $p_{0}\in \mathbb{R}^{n}$ di raggio $r>0$ l'insieme $\mathrm{B}(p_{0},r):=\{ p \in \mathbb{R}^{n}:\mathrm{d}(p,p_{0})<r \}$

### Punto di frontiera
$p_{0}\in \mathbb{R}^{n}$ si dice punto di frontiera di $A$ se $\mathrm{B}(p_{0},r)\cap A\neq \emptyset \land \mathrm{B}(p_{0},r)\cap(\mathbb{R}^{n}\setminus A)\neq \emptyset\;\;\forall r>0$
L'insieme di tutti i punti di frontiera di $A$ è detto frontiera di $A$ e si denota con $\partial A$

### Insieme chiuso
$A$ è detto chiuso se ogni punto di frontiera di $A$ appartiene ad $A$

### Insieme aperto
$A$ è detto aperto se non contiene alcun punto della sua frontiera

### Parte interna
L'insieme di tutti i punti di $A$ che non sono di frontiera si chiama parte interna di $A$ e si denota con $\mathring{A}$

### Insieme limitato
$A$ è detto limitato se $\exists r>0:A\subset \mathrm{B}(\underline{0},r)$

### Punto di accumulazione
$p_{0}\in \mathbb{R}^{n}$ si dice punto di accumulazione per $A$ se $\mathrm{B}(p_{0},r)\cap(A\setminus \{ p_{0} \})\neq \emptyset\;\;\forall r>0$

### Punto isolato
$p_{0}\in A$ si dice punto isolato di $A$ se non è un punto di accumulazione

# Limite
$f:\mathbb{R}^{2}\to \mathbb{R}$
Il limite
$$\begin{flalign}\lim_{ (x,y) \to (x_{0},y_{0}) } f(x,y)=l\in \mathbb{R} &&\end{flalign}$$
è definito come
$\forall\epsilon>0\;\;\exists\delta>0:|f(x,y)-l|<\epsilon\;\;\forall(x,y)\in \mathrm{B}((x_{0},y_{0}),\delta)$