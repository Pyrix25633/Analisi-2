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
