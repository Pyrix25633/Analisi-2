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
