# Funzioni di più variabili scalari e vettoriali
> [!definizione]
> $f:A\subset \mathbb{R}^{n}\to \mathbb{R}^{k}$, $n\geq2$ è una funzione di più variabili
> - scalare se $k=1$
> - vettoriale se $k\geq2$
> 
> ### Grafico
> $k=1$
> $G_{f}:=\{ (\underline{p},f(\underline{p})):\underline{p}\in A \}\subset \mathbb{R}^{n+1}$
> 
> ### Curve di livello
> $n=2$, $k=1$, $t\in \mathbb{R}$
> $C_{t}:=\{ (x,y)\in A:f(x,y)=t \}$

# Insiemistica
$A\subset \mathbb{R}^{n}$

### Distanza euclidea
> [!definizione]
> $\underline{p_{1}},\underline{p_{2}}\in \mathbb{R}^{3}$
> $\mathrm{d}(\underline{p_{1}},\underline{p_{2}})=\sqrt{(x_{1}-x_{2})^{2}+(y_{1}-y_{2})^{2}+(z_{1}-z_{2})^{2}}$
> è detta distanza euclidea tra $\underline{p_{1}}$ e $\underline{p_{2}}$

### Intorno
> [!definizione]
> Si chiama intorno sferico di $\underline{p_{0}}\in \mathbb{R}^{n}$ di raggio $r>0$ l'insieme $\mathrm{B}(\underline{p_{0}},r):=\{ \underline{p} \in \mathbb{R}^{n}:\mathrm{d}(\underline{p},\underline{p_{0}})<r \}$
<div class="page-break" style="page-break-before: always;"></div>

### Frontiera e parte interna
> [!definizione]
> $\underline{p_{0}}\in \mathbb{R}^{n}$ si dice punto di frontiera di $A$ se $\mathrm{B}(\underline{p_{0}},r)\cap A\neq \emptyset \land \mathrm{B}(\underline{p_{0}},r)\cap(\mathbb{R}^{n}\setminus A)\neq \emptyset\;\;\forall r>0$
> L'insieme di tutti i punti di frontiera di $A$ è detto frontiera di $A$ e si denota con $\partial A$
> L'insieme di tutti i punti di $A$ che non sono di frontiera si chiama parte interna di $A$ e si denota con $\mathring{A}:=A\setminus\partial A$

### Insieme chiuso e aperto
> [!definizione]
> $A$ è detto chiuso se ogni punto di frontiera di $A$ appartiene ad $A$
> $\partial A\subset A$
> $A$ è detto aperto se non contiene alcun punto della sua frontiera
> $A\cap \partial A=\emptyset$

### Insieme limitato
> [!definizione]
> $A$ è detto limitato se $\exists r>0:A\subset \mathrm{B}(\underline{0},r)$

### Punto di accumulazione
> [!definizione]
> $\underline{p_{0}}\in \mathbb{R}^{n}$ si dice punto di accumulazione per $A$ se $\mathrm{B}(\underline{p_{0}},r)\cap(A\setminus \{ \underline{p_{0}} \})\neq \emptyset\;\;\forall r>0$

### Punto isolato
> [!definizione]
> $\underline{p_{0}}\in A$ si dice punto isolato di $A$ se non è un punto di accumulazione
<div class="page-break" style="page-break-before: always;"></div>

# Limite
> [!definizione]
> $f:A \subset\mathbb{R}^{n}\to \mathbb{R}$, $\underline{p_{0}}$ punto di accumulazione di $A$
> $$\begin{flalign}\exists\lim_{ \underline{p} \to \underline{p_{0}} } f(\underline{p})=l\in \mathbb{R} &&\end{flalign}$$
> se
> $\exists\delta>0:|f(\underline{p})-l|<\varepsilon\;\;\forall\varepsilon>0,\underline{p}\in \mathrm{B}(\underline{p_{0}},\delta)\cap (A\setminus \{ \underline{p_{0}} \})$

> [!formule]
> $f,g:A\subset \mathbb{R}^{n}\to \mathbb{R}$, $\underline{p_{0}}$ punto di accumulazione di $A$
> $\exists \lim_{ \underline{p} \to \underline{p_{0}} }f(\underline{p})=l\in \mathbb{R}$, $\exists \lim_{ \underline{p} \to \underline{p_{0}} }g(\underline{p})=m\in \mathbb{R}$
> Somma
> $\exists \lim_{ \underline{p} \to \underline{p_{0}} }(f(\underline{p})+g(\underline{p}))=l+m$
> Prodotto
> $\exists \lim_{ \underline{p} \to \underline{p_{0}} }f(\underline{p})\cdot g(\underline{p})=l\cdot m$
> Quoziente, $g(\underline{p})\neq0\;\;\forall \underline{p} \in(A\setminus \{ \underline{p_{0}} \})$ e $m\neq0$
> $$\begin{flalign}\exists \lim_{ \underline{p} \to \underline{p_{0}} } \frac{f(\underline{p})}{g(\underline{p})}=\frac{l}{m} &&\end{flalign}$$
> Composizione, $F:\mathbb{R}\to \mathbb{R}$ continua, $h(\underline{p}):=F(f(\underline{p}))$
> $\exists \lim_{ \underline{p} \to \underline{p_{0}} }h(\underline{p})=F(l)$

> [!teorema] Teorema del confronto
> $f,g,h:A\subset \mathbb{R}^{n}\to \mathbb{R}$, se
> - $f(\underline{p})\leq g(\underline{p})\leq h(\underline{p})\;\;\forall \underline{p}\in A$
> - $$\begin{flalign}\exists \lim_{ \underline{p} \to \underline{p_{0}} } f(\underline{p})=\lim_{ \underline{p} \to \underline{p_{0}} } h(\underline{p}) = l\in \mathbb{R}\cup \{ \pm \infty \} &&\end{flalign}$$
> 
> $$\begin{flalign}\implies \exists \lim_{ \underline{p} \to \underline{p_{0}} } g(\underline{p})=l &&\end{flalign}$$
> > [!dimostrazione]-
> > $\exists\delta_{1}>0:|f(\underline{p})-l|<\varepsilon\;\;\forall\varepsilon>0,\underline{p}\in \mathrm{B}(\underline{p_{0}},\delta_{1})$
> > $\exists\delta_{2}>0:|h(\underline{p})-l|<\varepsilon\;\;\forall\varepsilon>0,\underline{p}\in \mathrm{B}(\underline{p_{0}},\delta_{2})$
> > $\delta=\mathrm{min}(\delta_{1},\delta_{2})$
> > $\implies l-\varepsilon<f(\underline{p})\leq g(\underline{p})\leq h(\underline{p})<l+\varepsilon$
<div class="page-break" style="page-break-before: always;"></div>

# Limite lungo direzioni
> [!definizione]
> $B\subset A$, $f|_{B}:B\to \mathbb{R}$, $f|_{B}(\underline{p}):=f(\underline{p})$ se $\underline{p} \in B$ si dice funzione restrizione su $B$

> [!teorema]
$f:A\subset \mathbb{R}^{n}\to \mathbb{R}$, $\underline{p_{0}}$ punto di accumulazione di $A$, sono equivalenti:
> - $\exists \lim_{ \underline{p} \to \underline{p_{0}} }f(\underline{p})=l$
> - $\forall B\subset A$ per cui $\underline{p_{0}}$ è punto di accumulazione di $B$ $\exists \lim_{ \underline{p} \to \underline{p_{0}} }f|_{B}(\underline{p})=l$
