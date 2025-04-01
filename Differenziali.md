# Funzione continua
Una funzione $f:A\subset \mathbb{R}^{n}\to \mathbb{R}$ si dice continua in $p_{0}$ se vale una delle seguenti:
- $p_{0}$ è un punto isolato di $A$
- $p_{0}$ è punto di accumulazione e $\exists \lim_{ p \to p_{0} }f(p)=f(p_{0})$
Si dice continua su $A$ se è continua $\forall p_{0} \in A$

# Derivate parziali
$f:A\subset \mathbb{R}^{2}\to \mathbb{R}$, $A$ aperto
$\exists\delta>0:[x_{0}-\delta,x_{0}+\delta]\times[y_{0}-\delta,y_{0}+\delta]\subset A$
In particolare
$(x,y_{0})\in A\;\;\forall x \in(x_{0}-\delta,x_{0}+\delta)$ e $(x_{0},y)\in A\;\;\forall y\in(y_{0}-\delta,y_{0}+\delta)$
Si dice che $f$ è derivabile rispetto a $x$ in $p_{0}$ se
$$\begin{flalign}\exists \lim_{ x \to x_{0} } \frac{f(x,y_{0})-f(x_{0},y_{0})}{x-x_{0}}:=\frac{\partial f}{\partial x}(x_{0},y_{0})=\mathrm{D}_{1}f(x_{0},y_{0}) &&\end{flalign}$$
Si dice che $f$ è derivabile rispetto a $y$ in $p_{0}$ se
$$\begin{flalign}\exists \lim_{ y \to y_{0} } \frac{f(x_{0},y)-f(x_{0},y_{0})}{y-y_{0}}:=\frac{\partial f}{\partial y}(x_{0},y_{0})=\mathrm{D}_{2}f(x_{0},y_{0}) &&\end{flalign}$$
Si chiama il gradiente il vettore $\nabla f(p_{0}):=(\mathrm{D}_{1}f(p_{0}),\mathrm{D}_{2}f(p_{0}))$

# Differenziabilità
$f:A\subset\mathbb{R}^{2}\to \mathbb{R}$, $A$ aperto
Se $\exists a,b\in \mathbb{R}:$
$$\begin{flalign}\exists \lim_{ (x,y) \to (x_{0},y_{0}) } \frac{f(x,y)-[a(x-x_{0})+b(y-y_{0})+f(x_{0},y_{0})]}{\sqrt{(x-x_{0})^{2}+(y-y_{0})^{2}}} \implies&&\end{flalign}$$
il piano $\pi:a(x-x_{0})+b(y-y_{0})+f(x_{0},y_{0})$ si dice piano tangente al grafico in $(x_{0},y_{0},f(x_{0},y_{0}))$ e $f$ si dice differenziabile nel punto $(x_{0},y_{0})$

Se $f$ è differenziabile in $p_{0}\implies \exists \nabla f(p_{0})$ e $a=\frac{\partial f}{\partial x}(p_{0}),\;b=\frac{\partial f}{\partial y}(p_{0})$
Dimostrazione:
Se $y=y_{0}\implies$$$\begin{flalign}\exists \lim_{ x \to x_{0} } \frac{f(x,y_{0})-[a(x-x_{0})+f(x_{0},y_{0})]}{|x-x_{0}|}\iff \exists \lim_{ x \to x_{0} } \frac{f(x,y_{0})-f(x_{0},y_{0})}{x-x_{0}}=a\iff \exists \frac{\partial f}{\partial x}(p_{0})=a &&\end{flalign}$$
Analogamente con $x=x_{0}$

# Differenziale
L'applicazione lineare $L:\mathbb{R}^{2}\to \mathbb{R}\;\;\;L(v_{1},v_{2}):=\frac{\partial f}{\partial x}(p_{0})\cdot v_{1}+\frac{\partial f}{\partial y}(p_{0})\cdot v_{2}\;\;\forall (v_{1},v_{2})\in \mathbb{R}^{2}$ si chiama differenziale di $f$ in $p_{0}$ denotato anche come $df(p_{0})=\frac{\partial f}{\partial x}(p_{0})dx+\frac{\partial f}{\partial y}(p_{0})dy$
Se $f$ è differenziabile in $p_{0}$ esiste il piano tangente al grafico in $(x_{0},y_{0},f(p_{0}))$ $\pi:z=\nabla f(p_{0})\cdot(x-x_{0},y-y_{0})+f(x_{0},y_{0})$

### Continuità
$f:A\subset \mathbb{R}^{n}\to \mathbb{R}$, $A$ aperto, $f$ differenziabile in $p_{0}\in A\implies f$ è continua in $p_{0}$
Dimostrazione:
$$\begin{flalign}\exists \lim_{ p \to p_{0} } \frac{f(p)-[df(p_{0})(p-p_{0})+f(p_{0})]}{\mathrm{d}(p,p_{0})}=0 &&\end{flalign}$$
$L(v_{1},v_{2})=df(p_{0})(v_{1},v_{2})$
$$\begin{flalign}f(p)-f(p_{0})=\frac{f(p)-[L(p-p_{0})+f(p_{0})]}{\mathrm{d}(p,p_{0})} \cdot \mathrm{d(p,p_{0})}+L(p-p_{0})&&\end{flalign}$$
$\lim_{ p \to p_{0} }L(p-p_{0})\implies \exists \lim_{ p \to p_{0} }f(p)-f(p_{0})=0$

# Condizioni sulle derivate parziali che assicurano la differenziabilità

### Teorema del differenziale totale
$f:A\subset \mathbb{R}^{2}\to \mathbb{R}$, $A$ aperto, $p_{0}\in A$
Se:
- $\exists \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}:A\to \mathbb{R}$
- $\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}$ continue in $p_{0}$
$\implies f$ è differenziabile in $p_{0}$
Osservazione: è sufficiente richiedere le ipotesi su un intorno di $p_{0}$

$f$ si dice differenziabile in $p_{0}$ se $\exists L:\mathbb{R}^{2}\to \mathbb{R}$ lineare tale che
$$\begin{flalign}\exists \lim_{ p \to p_{0} } \frac{f(p)-f(p_{0})-L(p-p_{0})}{\mathrm{d}(p,p_{0})}=0 \implies&&\end{flalign}$$
- $\exists \nabla f(p_{0})$
- $L(\underline{v})=\nabla f(p_{0})\cdot \underline{v}$
- $f$ è continua in $p_{0}$

$f$ si dice differenziabile su $A$ se è differenziabile in ogni punto di $A$
$f$ si dice di classe $\mathrm{C}^{1}(A)$ se è continua ed $\exists \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}:A\to \mathbb{R}$ continue

Corollario: $f\in \mathrm{C}^{1}\implies f$ è differenziabile in ogni punto $p_{0}\in A$

# Derivate direzionali
$\underline{v}$ si dice direzione se $||\underline{v}||=1$
$f$ è derivabile rispetto a $\underline{v}$ in $p_{0}$ se
$$\begin{flalign}\exists \frac{\partial f}{\partial \underline{v}}(p_{0})=\lim_{ h \to 0 } \frac{f(p_{0}+h\underline{v})-f(p_{0})}{h} &&\end{flalign}$$
Osservazione: $F:(-\delta,\delta)\to \mathbb{R}$, $F(t)=f(p_{0}+t\underline{v})$ per $t\in(-\delta,\delta)\implies$
$$\begin{flalign}\exists \frac{\partial f}{\partial \underline{v}}(p_{0})\iff \exists F'(0)=\lim_{ h \to 0 } \frac{F(h)-F(0)}{h} &&\end{flalign}$$e $\frac{\partial f}{\partial \underline{v}}(p_{0})=F'(0)$

$f$ differenziabile in $p_{0}\implies \exists \frac{\partial f}{\partial \underline{v}}(p_{0})=df(p_{0})(\underline{v})=\nabla f(p_{0})\cdot \underline{v}$
Dimostrazione: per ipotesi $f$ è differenziabile in $p_{0}\implies$
$$\begin{flalign}\exists \lim_{ p \to p_{0} } \frac{f(p)-f(p_{0})-\nabla f(p_{0})\cdot(p-p_{0})}{\mathrm{d}(p,p_{0})}=0 &&\end{flalign}$$
che è equivalente a $f(p)=f(p_{0})+\nabla f(p_{0})\cdot(p-p_{0})+o(\mathrm{d}(p,p_{0}))\;\;\forall p \in A$
si ottiene $F(h):=f(p_{0}+h\underline{v})=f(p_{0})+\nabla f(p_{0})\cdot(h\underline{v})+o(\mathrm{d}(p_{0}+h\underline{v},p_{0}))=F(0)+h(\nabla f(p_{0})\cdot \underline{v})+o(|h|)$
Segue che $\exists F'(0):=\lim_{ h \to 0 }F(h)-F(0)=\nabla f(p_{0})\cdot \underline{v}=df(p_{0})(\underline{v})$

# Teorema del valore intermedio
$f:A\subset \mathbb{R}^{2}\to \mathbb{R}$, $A$ aperto, $f:A\to \mathbb{R}$
Se:
- $\exists p,q\in A:[p,q]:=\{ tq+(1-t)p: t\in[0,1] \}\subset A$
- $f$ è continua su $[p,q]$ e differenziabile su $(p,q)$
$\implies \exists\bar{c}\in(p,q):f(q)-f(p)=\nabla f(\bar{c})(q-p)$
Dimostrazione: supponiamo $p\neq q$
$\underline{v}=\frac{q-p}{||q-p||}$ direzione di $\mathbb{R}^{2}$
$F(t):=f(p+t\underline{v})$, $r\in[0,||p-q||]$ è ben definita per la prima ipotesi e $F(||q-p||)=f(q)$
Per la seconda ipotesi $F$ è continua e $\exists F'(t)=\frac{\partial f}{\partial \underline{v}}(p+t\underline{v})\;\;\forall t\in(0,||q-p||)$
Per il teorema in una variabile: $f(q)-f(p)=F(||q-p||)-F(0)=F'(t)||q-p||=\frac{\partial f}{\partial \underline{v}}(p+t\underline{v})||q-p||=$$(\nabla f(p+t\underline{v})\cdot \underline{v})||q-p||=\left( \nabla f(p+t\underline{v}) \frac{q-p}{||q-p||} \right)||q-p||$
Scegliendo $\bar{c}=p+t\underline{v}$ otteniamo la tesi

# Derivate parziali di una funzione composta
$g:A\subset \mathbb{R}^{n}\to \mathbb{R}^{m},f:B\subset \mathbb{R}^{m}\to \mathbb{R}^{k}$
Se:
- $g(A)\subset B$
- $g=(g_{1},\dots,g_{m}),f=(f_{1},\dots,f_{k})$
- $g_{i}:A\to \mathbb{R}$ differenziabile in $x_{0}\in A$
- $f_{i}:B\to \mathbb{R}$ differenziabile in $y_{0}=g(x_{0})\in B$
- $h:=f\circ g$
$$\begin{flalign}\implies Dh(x_{0})=Df(y_{0})\cdot Dg(x_{0})=\begin{bmatrix}\nabla f_{1}(y_{0}) \\
\dots \\
\nabla f_{k}(y_{0})
\end{bmatrix}\cdot \begin{bmatrix}
\nabla g_{1}(x_{0}) \\
\dots \\
\nabla g_{m}(x_{0})
\end{bmatrix} &&\end{flalign}$$

# Derivate parziali di ordine superiore
$f:A\subset \mathbb{R}^{2}\to \mathbb{R}$, $A$ aperto, se $\exists \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}\implies$
Sono dette derivate parziali seconde pure
$$\begin{flalign} \frac{\partial^{2}f}{\partial x^{2}}:=\frac{\partial}{\partial x}\left( \frac{\partial f}{\partial x} \right),\;\;\frac{\partial^{2}f}{\partial y^{2}}:=\frac{\partial}{\partial y}\left( \frac{\partial f}{\partial y} \right) &&\end{flalign}$$
e derivate parziali seconde miste
$$\begin{flalign} \frac{\partial^{2}f}{\partial x\partial y}:=\frac{\partial}{\partial x}\left( \frac{\partial f}{\partial y} \right),\;\;\frac{\partial^{2}f}{\partial y\partial x}:=\frac{\partial}{\partial y}\left( \frac{\partial f}{\partial x} \right) &&\end{flalign}$$

Se le derivate parziali seconde miste sono continue $\implies$ coincidono

# Polinomi di Taylor
$m\in \mathbb{N}$, $p_{0}=(x_{0},y_{0})\in \mathbb{R}^{2}$
Si chiama polinomio di Taylor di ordine $m$ di $n=2$ variabili centrato in $p_{0}$ una funzione $T:\mathbb{R}^{2}\to \mathbb{R}$
$$\begin{flalign}T(x,y)=\sum_{h=0}^{m} \sum_{i=0}^{n} c_{i,n-i}(x-x_{0})^{i}(y-y_{0})^{n-i}\;\;\forall(x,y)\in \mathbb{R}^{2} &&\end{flalign}$$
tale che $f(p)=T(p)+o(||p-p_{0}||^{2})$

# Matrice Hessiana
$f\in \mathrm{C}^{2}(A)$
Si chiama matrice Hessiana di $f$ in $p \in A$ la matrice
$$\begin{flalign}D^{2}f(p)=H_{f}(p):=\begin{bmatrix}
\frac{\partial^{2}f}{\partial x^{2}}(p) & \frac{\partial^{2}f}{\partial y\partial x}(p) \\
\frac{\partial^{2}f}{\partial x\partial y}(p) & \frac{\partial^{2}f}{\partial y^{2}}(p)
\end{bmatrix}=\begin{bmatrix}
\nabla \left( \frac{\partial f}{\partial x} \right) \\
\nabla\left( \frac{\partial f}{\partial y} \right)
\end{bmatrix} &&\end{flalign}$$

Osservazione: $H_{f}(p)$ è simmetrica

$T_{2}(p)=f(p_{0})+\nabla f(p)(p-p_{0})+\frac{1}{2}H_{f}(p)(p-p_{0})\cdot(p-p_{0})$
Dimostrazione:
$p \in \mathrm{B}(po,r)$, $\underline{v}:=\frac{p-p_{0}}{||p-p_{0}||}=(v_{1},v_{2})$, $F(t):=f(p_{0}+t\underline{v})\;\;t\in(-r,r)$
Poiché $g(t)=p_{0}+t\underline{v}\in \mathrm{C}^{2}((-r,r))$ anche $F(t)=f(g(t))\in \mathrm{C}^{2}((-r,r))$
Applicando la formula di Taylor in una variabile per $t=0$ si ottiene
$F(t)=F(0)+F'(0)\cdot t+\frac{1}{2}F''(0)\cdot t^{2}+o(t^{2})$
$F'(t)=\nabla f(p+t\underline{v})\cdot \underline{v}$
$$\begin{flalign}F''(t)=\frac{\partial^{2}f}{\partial x^{2}}(p_{0}+t\underline{v})\cdot v_{1}^{2}+2 \frac{\partial^{2} f}{\partial y\partial x}(p_{0}+t\underline{v})\cdot v_{1}\cdot v_{2}+\frac{\partial^{2}f}{\partial y^{2}}(p_{0}+t\underline{v})\cdot v_{2}^{2} &&\end{flalign}$$
$F(0)=f(p_{0})$, $F'(0)=\nabla f(p_{0})\cdot \underline{v}$, $F''(0)=H_{f}(p_{0})\underline{v}\cdot \underline{v}$
$F(t)=f(p_{0})+(\nabla f(p_{0})\cdot \underline{v})t+\frac{1}{2}(H_{f}(p_{0})\underline{v}\cdot \underline{v})t^{2}+o(t^{2})$
Sostituendo $t=p-p_{0}$ e $\underline{v}$ si ottiene la tesi

# Massimi e minimi
$f:A\subset \mathbb{R}^{2}\to \mathbb{R}$
$p_{0}\in A$ si dice punto di
- massimo relativo di $f$ in $A$ se $\exists r_{0}>0:f(p)\leq f(p_{0})\;\;\forall p \in A\cap B(p_{0},r_{0})$
- massimo assoluto di $f$ in $A$ se $f(p)\leq f(p_{0})\;\;\forall p \in A$
- minimo relativo di $f$ in $A$ se $\exists r_{0}>0:f(p)\geq f(p_{0})\;\;\forall p \in A\cap B(p_{0},r_{0})$
- minimo assoluto di $f$ in $A$ se $f(p)\geq f(p_{0})\;\;\forall p \in A$
Osservazione: non confondere punto di massimo e massimo di una funzione: $\mathrm{Max}_{A}f:=\mathrm{Max}\{ f(p):p \in A \}$ se esiste è unico

I punti di massimo e minimo relativi sono detti estremi liberi

$A$ aperto, se $\exists p_{0}\in A$ tale che:
- $\exists \nabla f(p_{0})$
- $p_{0}$ è un estremo libero di $f$ in $A$
$\implies \nabla f(p_{0})=\underline{0}$
Dimostrazione: $p_{0}=(x_{0},y_{0})$, $A$ aperto $\implies \exists\delta>0:p_{0}+t\underline{i}=(x_{0}+t,y_{0})\in A$ se $t\in(-\delta,\delta)$
$F:(-\delta,\delta)\to \mathbb{R}$, $F(t)=f(p_{0}+t\underline{i})$
Dalle ipotesi:
- $\exists \frac{\partial f}{\partial x}(p_{0})\iff F$ è derivabile in $t=0$ e $F'(0)=\frac{\partial f}{\partial x}(p_{0})$
- $t=0$ è un estremo libero di $F$
Per il teorema in una variabile $F'(0)=0$, analogamente per $\underline{j}\implies \nabla f(p_{0})=(0,0)=\underline{0}$

Un punto $p_{0}\in A$ si chiama punto stazionario o critico di $f$ se $\exists \nabla f(p_{0})=\underline{0}$

# Matrice positiva
$H\in M_{n}(\mathbb{R})$ si dice:
- positiva se $H\underline{v}\cdot \underline{v}>0\;\;\forall \underline{v}\in \mathbb{R}^{n}\setminus \{ \underline{0} \}$
- semi-definita positiva se $H\underline{v}\cdot \underline{v}\geq0\;\;\forall \underline{v}\in \mathbb{R}^{n}\setminus \{ \underline{0} \}$
- negativa se $H\underline{v}\cdot \underline{v}<0\;\;\forall \underline{v}\in \mathbb{R}^{n}\setminus \{ \underline{0} \}$
- semi-definita negativa se $H\underline{v}\cdot \underline{v}\leq0\;\;\forall \underline{v}\in \mathbb{R}^{n}\setminus \{ \underline{0} \}$

$H=[h_{ij}]\in M_{n}(\mathbb{R})$
$$\begin{flalign}D_{i}:=\det \begin{bmatrix}
h_{11} & \dots & h_{1i}\\
\dots & & \dots \\ \\
h_{i_{1}} & \dots & h_{ii}
\end{bmatrix}\;\;1\leq i\leq n &&\end{flalign}$$
$H$ è:
- positiva $\iff D_{i}>0\;\;\forall i=1,\dots,n$
- negativa $\iff D_{i}>0$ per $i$ pari, $D_{i}<0$ per $i$ dispari
- se $\det(H)\neq0$ e nessuna delle condizioni precedenti $\implies$ non è semi-definita

Corollario: $H\in M_{2}(\mathbb{R})\implies H$ è:
- positiva se $h_{11}>0\land \det(H)>0$
- negativa se $h_{11}<0\land \det(H)>0$
- se $\det(H)<0\implies$ non è semi-definita

### Matrice Hessiana ed estremi liberi
$A\subset \mathbb{R}^{n}$ aperto, $f\in \mathrm{C}^{2}(A)$, $p_{0}$ punto stazionario
Se $H_{f}(p_{0})$ è:
- positiva $\implies p_{0}$ è un punto di minimo relativo
- negativa $\implies p_{0}$ è un punto di massimo relativo
- non semi-definita $\implies p_{0}$ è un punto di sella

# Teorema di Weierstrass
$f:A\subset \mathbb{R}^{n}\to \mathbb{R}$ continua su $A$ limitato e chiuso
$\implies \exists \mathrm{Max}_{A}f=f(p_{1})\land \exists \mathrm{Min}_{A}f=f(p_{2})\;\;p_{i}\in A\;\;i=1,\dots,n$
si verifica una delle seguenti per ogni punto:
- $p_{i}\in \mathring{A} \land \exists \nabla f(p_{i})=\underline{0}$
- $p_{i}\in\mathring{A} \land \nexists \nabla f(p_{i})$
- $p_{i}\in \partial A$

# Parametrizzazione
Si chiama parametrizzazione della frontiera $\partial A$ una funzione $\gamma:B\subset \mathbb{R}^{n}\to A\subset \mathbb{R}^{n+1}$, $\gamma(t_{1},\dots,t_{n})=(\gamma_{1}(t),\dots,\gamma_{n+1}(t))$, con le seguenti proprietà:
- $B$ chiuso e limitato
- $\gamma(B)=\partial A$
- $\gamma_{1},\dots ,\gamma_{n+1}\in \mathrm{C}^{0}(B)\cap \mathrm{C}^{1}(\mathring{B})$
$f:A\to \mathbb{R}$, $f\in \mathrm{C}^{1}(A)$ da massimizzare/minimizzare sulla frontiera
$F:B\to \mathbb{R}$, $F(t_{1},\dots,t_{n}):=f(\gamma(t_{1},\dots,t_{n}))\implies$
- $\mathrm{Max}_{\partial A}f=\mathrm{Max}_{B}F$
- $\mathrm{Min}_{\partial A}f=\mathrm{Min}_{B}F$
