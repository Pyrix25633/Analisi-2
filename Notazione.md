# Funzioni di più variabili e funzioni vettoriali
$f:A\subset \mathbb{R}^{n}\to \mathbb{R}^{k}$ è una funzione
- di più variabili se $k=1 \land n\geq2$
- vettoriale di più variabili se $k\geq2 \land n\geq2$

# Insieme
$A\subset \mathbb{R}^{n}$

### Intorno
Si chiama intorno sferico di $\underline{p_{0}}\in \mathbb{R}^{n}$ di raggio $r>0$ l'insieme $\mathrm{B}(\underline{p_{0}},r):=\{ \underline{p} \in \mathbb{R}^{n}:\mathrm{d}(\underline{p},\underline{p_{0}})<r \}$

### Punto di frontiera
$\underline{p_{0}}\in \mathbb{R}^{n}$ si dice punto di frontiera di $A$ se $\mathrm{B}(\underline{p_{0}},r)\cap A\neq \emptyset \land \mathrm{B}(\underline{p_{0}},r)\cap(\mathbb{R}^{n}\setminus A)\neq \emptyset\;\;\forall r>0$
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
$\underline{p_{0}}\in \mathbb{R}^{n}$ si dice punto di accumulazione per $A$ se $\mathrm{B}(\underline{p_{0}},r)\cap(A\setminus \{ \underline{p_{0}} \})\neq \emptyset\;\;\forall r>0$

### Punto isolato
$\underline{p_{0}}\in A$ si dice punto isolato di $A$ se non è un punto di accumulazione
<div class="page-break" style="page-break-before: always;"></div>

# Limite
$f:A \subset\mathbb{R}^{n}\to \mathbb{R}$, $\underline{p_{0}}$ punto di accumulazione di $A$
Il limite
$$\begin{flalign}\exists\lim_{ \underline{p} \to \underline{p_{0}} } f(\underline{p})=l\in \mathbb{R} &&\end{flalign}$$
se
$\forall\epsilon>0\;\;\exists\delta>0:|f(\underline{p})-l|<\epsilon\;\;\forall(\underline{p})\in \mathrm{B}(\underline{p},\delta)\cap (A\setminus \{ \underline{p_{0}} \})$

$f,g:A\subset \mathbb{R}^{n}\to \mathbb{R}$, $\underline{p_{0}}$ punto di accumulazione di $A$
Se $\exists \lim_{ \underline{p} \to \underline{p_{0}} }f(\underline{p})=l\in \mathbb{R}$ e $\exists \lim_{ \underline{p} \to \underline{p_{0}} }g(\underline{p})=m\in \mathbb{R}\implies$
- $\exists \lim_{ \underline{p} \to \underline{p_{0}} }(f(\underline{p})+g(\underline{p}))=l+m$
- $\exists \lim_{ \underline{p} \to \underline{p_{0}} }f(\underline{p})\cdot g(\underline{p})=l\cdot m$
- Se $g(\underline{p})\neq0\;\;\forall \underline{p} \in(A\setminus \{ \underline{p_{0}} \})$ e $m\neq0\implies$$$\begin{flalign}\exists \lim_{ \underline{p} \to \underline{p_{0}} } \frac{f(\underline{p})}{g(\underline{p})}=\frac{l}{m} &&\end{flalign}$$
- $F:\mathbb{R}\to \mathbb{R}$ continua, $h(\underline{p}):=F(f(\underline{p}))\implies$ $\exists \lim_{ \underline{p} \to \underline{p_{0}} }h(\underline{p})=F(l)$
- $h:A\to \mathbb{R}$, $f(\underline{p})\leq h(p)\leq g(\underline{p})\;\;\underline{\forall}p \in(A\setminus \{ \underline{p_{0}} \})$ se $l=m\implies \exists \lim_{ p \to \underline{p_{0}} }g(\underline{p})=l$

# Limite lungo direzioni
Funzione restrizione: $B\subset A$, $f|_{B}:B\to \mathbb{R}$, $f|_{B}(\underline{p}):=f(\underline{p})$ se $\underline{p} \in B$

$f:A\subset \mathbb{R}^{n}\to \mathbb{R}$, $\underline{p_{0}}$ punto di accumulazione di $A$, sono equivalenti:
- $\exists \lim_{ \underline{p} \to \underline{p_{0}} }f(\underline{p})=l$
- $\forall B\subset A$ per cui $\underline{p_{0}}$ è punto di accumulazione di $B$ $\exists \lim_{ \underline{p} \to \underline{p_{0}} }f|_{B}(\underline{p})=l$
