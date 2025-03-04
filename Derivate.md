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