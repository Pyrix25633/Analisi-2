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
$f:A \subset\mathbb{R}^{n}\to \mathbb{R}$, $p_{0}$ punto di accumulazione di $A$
Il limite
$$\begin{flalign}\exists\lim_{ p \to p_{0} } f(p)=l\in \mathbb{R} &&\end{flalign}$$
se
$\forall\epsilon>0\;\;\exists\delta>0:|f(p)-l|<\epsilon\;\;\forall(p)\in \mathrm{B}(p,\delta)\cap (A\setminus \{ p_{0} \})$

$f,g:A\subset \mathbb{R}^{n}\to \mathbb{R}$, $p_{0}$ punto di accumulazione di $A$
Se $\exists \lim_{ p \to p_{0} }f(p)=l\in \mathbb{R}$ e $\exists \lim_{ p \to p_{0} }g(p)=m\in \mathbb{R}\implies$
- $\exists \lim_{ p \to p_{0} }(f(p)+g(p))=l+m$
- $\exists \lim_{ p \to p_{0} }f(p)\cdot g(p)=l\cdot m$
- Se $g(p)\neq0\;\;\forall p \in(A\setminus \{ p_{0} \})$ e $m\neq0\implies$$$\begin{flalign}\exists \lim_{ p \to p_{0} } \frac{f(p)}{g(p)}=\frac{l}{m} &&\end{flalign}$$
- $F:\mathbb{R}\to \mathbb{R}$ continua, $h(p):=F(f(p))\implies$ $\exists \lim_{ p \to p_{0} }h(p)=F(l)$
- $h:A\to \mathbb{R}$, $f(p)\leq h(p)\leq g(p)\;\;\forall p \in(A\setminus \{ p_{0} \})$ se $l=m\implies \exists \lim_{ p \to p_{0} }g(p)=l$

# Limite lungo direzioni
Funzione restrizione: $B\subset A$, $f|_{B}:B\to \mathbb{R}$, $f|_{B}(p):=f(p)$ se $p \in B$

$f:A\subset \mathbb{R}^{n}\to \mathbb{R}$, $p_{0}$ punto di accumulazione di $A$, sono equivalenti:
- $\exists \lim_{ p \to p_{0} }f(p)=l$
- $\forall B\subset A$ per cui $p_{0}$ è punto di accumulazione di $B$ $\exists \lim_{ p \to p_{0} }f|_{B}(p)=l$
