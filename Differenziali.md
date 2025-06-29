# Funzione continua
> [!definizione]
> Una funzione $f:A\subset \mathbb{R}^{n}\to \mathbb{R}$ si dice continua in $\underline{p_{0}}$ se vale una delle seguenti:
> - $\underline{p_{0}}$ è un punto isolato di $A$
> - $\underline{p_{0}}$ è punto di accumulazione e $\exists \lim_{ \underline{p} \to \underline{p_{0}} }f(\underline{p})=f(\underline{p_{0}})$
> 
> Si dice continua su $A$ se è continua $\forall \underline{p_{0}} \in A$

# Derivate parziali
> [!definizione]
> $f:A\subset \mathbb{R}^{2}\to \mathbb{R}$, $A$ aperto, $\underline{p_{0}}=(x_{0},y_{0})\in \mathbb{R}^{2}$
> $\exists\delta>0:[x_{0}-\delta,x_{0}+\delta]\times[y_{0}-\delta,y_{0}+\delta]\subset A$
> In particolare
> $(x,y_{0})\in A\;\;\forall x \in(x_{0}-\delta,x_{0}+\delta)$ e $(x_{0},y)\in A\;\;\forall y\in(y_{0}-\delta,y_{0}+\delta)$
> Si dice che $f$ è derivabile rispetto a $x$ in $\underline{p_{0}}$ se
> $$\begin{flalign}\exists \lim_{ x \to x_{0} } \frac{f(x,y_{0})-f(x_{0},y_{0})}{x-x_{0}}=:\frac{\partial f}{\partial x}(x_{0},y_{0})=D_{1}f(x_{0},y_{0}) &&\end{flalign}$$
> Si dice che $f$ è derivabile rispetto a $y$ in $\underline{p_{0}}$ se
> $$\begin{flalign}\exists \lim_{ y \to y_{0} } \frac{f(x_{0},y)-f(x_{0},y_{0})}{y-y_{0}}=:\frac{\partial f}{\partial y}(x_{0},y_{0})=D_{2}f(x_{0},y_{0}) &&\end{flalign}$$
> Si chiama il gradiente il vettore $\nabla f(\underline{p_{0}}):=(D_{1}f(\underline{p_{0}}),D_{2}f(\underline{p_{0}}))$
> ### In $n$ variabili
> $f:A\subset \mathbb{R}^{n}\to \mathbb{R}$, $A$ aperto, $\underline{p_{0}}\in \mathbb{R}^{n}$, $\hat{e_{i}}$ versore di $x_{i}$
> $$\begin{flalign}\exists \lim_{ h \to 0 } \frac{f(\underline{p_{0}}+h\cdot \hat{e_{i}})-f(\underline{p_{0}})}{h}=:\frac{\partial f}{\partial x_{i}}(\underline{p_{0}})=D_{i}(\underline{p_{0}}) &&\end{flalign}$$
<div class="page-break" style="page-break-before: always;"></div>

# Differenziabilità
> [!definizione]
> $f:A\subset\mathbb{R}^{2}\to \mathbb{R}$, $A$ aperto
> Se $\exists a,b\in \mathbb{R}:$
> $$\begin{flalign}\exists \lim_{ (x,y) \to (x_{0},y_{0}) } \frac{f(x,y)-[a(x-x_{0})+b(y-y_{0})+f(x_{0},y_{0})]}{\sqrt{(x-x_{0})^{2}+(y-y_{0})^{2}}}=0 \implies&&\end{flalign}$$
> il piano $\pi:z=a(x-x_{0})+b(y-y_{0})+f(x_{0},y_{0})$ si dice piano tangente al grafico in $(x_{0},y_{0},f(x_{0},y_{0}))$ e $f$ si dice differenziabile nel punto $(x_{0},y_{0})$

> [!teorema]
> Se $f$ è differenziabile in $\underline{p_{0}}\implies \exists \nabla f(\underline{p_{0}})$ e $a=\frac{\partial f}{\partial x}(\underline{p_{0}}),\;b=\frac{\partial f}{\partial y}(\underline{p_{0}})$
> > [!dimostrazione]-
> > Se $y=y_{0}\implies$$$\begin{flalign}\exists \lim_{ x \to x_{0} } \frac{f(x,y_{0})-[a(x-x_{0})+f(x_{0},y_{0})]}{|x-x_{0}|}\iff \exists \frac{\partial f}{\partial x}(\underline{p_{0}})=a &&\end{flalign}$$
> > Analogamente con $x=x_{0}$

# Differenziale
> [!definizione]
> L'applicazione lineare $L:\mathbb{R}^{2}\to \mathbb{R}$, $L(\underline{p_{0}})(v_{1},v_{2}):=\frac{\partial f}{\partial x}(\underline{p_{0}})\cdot v_{1}+\frac{\partial f}{\partial y}(\underline{p_{0}})\cdot v_{2}\;\;\forall (v_{1},v_{2})\in \mathbb{R}^{2}$ si chiama differenziale di $f$ in $\underline{p_{0}}$ denotato anche come $df(\underline{p_{0}})=\frac{\partial f}{\partial x}(\underline{p_{0}})dx+\frac{\partial f}{\partial y}(\underline{p_{0}})dy$
> Se $f$ è differenziabile in $\underline{p_{0}}$ esiste il piano tangente al grafico in $(x_{0},y_{0},f(\underline{p_{0}}))$ $\pi:z=\nabla f(\underline{p_{0}})\cdot(\underline{p}-\underline{p_{0}})+f(\underline{p_{0}})$
> ### In $n$ variabili
> $L:\mathbb{R}^{n}\to \mathbb{R}$, $L(\underline{p_{0}})(\hat{v}):=\sum_{i=1}^{n} \frac{\partial f}{\partial x_{i}}(\underline{p_{0}})\;\;\forall \hat{v}\in \mathbb{R}^{n}$
<div class="page-break" style="page-break-before: always;"></div>

### Continuità
> [!teorema]
> $f:A\subset \mathbb{R}^{n}\to \mathbb{R}$, $A$ aperto, $f$ differenziabile in $\underline{p_{0}}\in A\implies f$ è continua in $\underline{p_{0}}$
> > [!dimostrazione]-
> > $$\begin{flalign}\exists \lim_{ \underline{p} \to \underline{p_{0}} } \frac{f(\underline{p})-[\nabla f(\underline{p_{0}})(\underline{p}-\underline{p_{0}})+f(\underline{p_{0}})]}{\mathrm{d}(\underline{p},\underline{p_{0}})}=0 &&\end{flalign}$$
> > $L(\underline{p_{0}})(\hat{v})=\nabla f(\underline{p_{0}})\cdot(\hat{v})$
$$\begin{flalign}f(\underline{p})-f(\underline{p_{0}})=\frac{f(\underline{p})-[L(\underline{p_{0}})(\underline{p}-\underline{p_{0}})+f(\underline{p_{0}})]}{\mathrm{d}(\underline{p},\underline{p_{0}})} \cdot \mathrm{d}(\underline{p},\underline{p_{0}})+L(\underline{p_{0}})(\underline{p}-\underline{p_{0}})&&\end{flalign}$$
> > $$\begin{flalign}\lim_{ \underline{p} \to \underline{p_{0}} }L(\underline{p_{0}})(\underline{p}-\underline{p_{0}})=0\implies \exists \lim_{ \underline{p} \to \underline{p_{0}} }f(\underline{p})-f(\underline{p_{0}})=0 &&\end{flalign}$$

# Condizioni sulle derivate parziali che assicurano la differenziabilità

> [!teorema] Teorema del differenziale totale
> $f:A\subset \mathbb{R}^{2}\to \mathbb{R}$, $A$ aperto, $\underline{p_{0}}\in A$
> Se:
> - $\exists \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}:A\to \mathbb{R}$
> - $\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}$ continue in $\underline{p_{0}}$
> 
> $\implies f$ è differenziabile in $\underline{p_{0}}$

> [!osservazione]-
> E' sufficiente richiedere le ipotesi su un intorno di $\underline{p_{0}}$
<div class="page-break" style="page-break-before: always;"></div>

> [!definizione]
> $f$ si dice differenziabile in $\underline{p_{0}}$ se $\exists L:\mathbb{R}^{2}\to \mathbb{R}$ lineare tale che
> $$\begin{flalign}\exists \lim_{ \underline{p} \to \underline{p_{0}} } \frac{f(\underline{p})-f(\underline{p_{0}})-L(\underline{p_{0}})(\underline{p} -\underline{p_{0}})}{\mathrm{d}(\underline{p},\underline{p_{0}})}=0 \implies&&\end{flalign}$$
> - $\exists \nabla f(\underline{p_{0}})$
> - $L(\underline{p_{0}})(\hat{v})=\nabla f(\underline{p_{0}})\cdot \hat{v}$
> - $f$ è continua in $\underline{p_{0}}$
> 
> $f$ si dice differenziabile su $A$ se è differenziabile in ogni punto di $A$
> $f$ si dice di classe $\mathrm{C}^{1}(A)$ se è continua ed $\exists \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}:A\to \mathbb{R}$ continue

> [!osservazione]-
> $f\in \mathrm{C}^{1}(A)\implies f$ è differenziabile in ogni punto $\underline{p_{0}}\in A$

# Derivate direzionali
> [!definizione]
> $\hat{v}$ si dice direzione se $||\hat{v}||=1$
> $f$ è derivabile rispetto a $\hat{v}$ in $\underline{p_{0}}$ se
> $$\begin{flalign}\exists\lim_{ h \to 0 } \frac{f(\underline{p_{0}}+h\hat{v})-f(\underline{p_{0}})}{h}=:\frac{\partial f}{\partial \hat{v}}(\underline{p_{0}}) &&\end{flalign}$$

> [!osservazione]-
> $F:(-\delta,\delta)\to \mathbb{R}$, $F(t)=f(\underline{p_{0}}+t\hat{v})$ per $t\in(-\delta,\delta)\implies$
> $$\begin{flalign}\exists \frac{\partial f}{\partial \hat{v}}(\underline{p_{0}})\iff \exists F'(0)=\lim_{ h \to 0 } \frac{F(h)-F(0)}{h} &&\end{flalign}$$e $\frac{\partial f}{\partial \hat{v}}(\underline{p_{0}})=F'(0)$
<div class="page-break" style="page-break-before: always;"></div>

> [!teorema]
> $f$ differenziabile in $\underline{p_{0}}\implies \exists \frac{\partial f}{\partial \hat{v}}(\underline{p_{0}})=L(\underline{p_{0}})(\hat{v})=\nabla f(\underline{p_{0}})\cdot \hat{v}$
> > [!dimostrazione]-
> > Per ipotesi $f$ è differenziabile in $\underline{p_{0}}\implies$
> > $$\begin{flalign}\exists \lim_{ \underline{p} \to \underline{p_{0}} } \frac{f(\underline{p})-f(\underline{p_{0}})-\nabla f(\underline{p_{0}})\cdot(\underline{p} -\underline{p_{0}})}{\mathrm{d}(p,\underline{p_{0}})}=0 &&\end{flalign}$$
> > che è equivalente a $f(\underline{p})=f(\underline{p_{0}})+\nabla f(\underline{p_{0}})\cdot(\underline{p} -\underline{p_{0}})+o(\mathrm{d}(\underline{p},\underline{p_{0}}))\;\;\forall \underline{p} \in A$
> > si ottiene $F(h):=f(\underline{p_{0}}+h\hat{v})=f(\underline{p_{0}})+\nabla f(\underline{p_{0}})\cdot(h\hat{v})+o(\mathrm{d}(\underline{p_{0}}+h\hat{v},\underline{p_{0}}))$$=F(0)+h(\nabla f(\underline{p_{0}})\cdot \hat{v})+o(|h|)$
> > $$\begin{flalign}\implies\exists F'(0):=\lim_{ h \to 0 }\frac{F(h)-F(0)}{h}=\nabla f(\underline{p_{0}})\cdot \hat{v}=L(\underline{p_{0}})(\hat{v}) &&\end{flalign}$$

# Teorema del valore intermedio
> [!teorema]
> $f:A\subset \mathbb{R}^{2}\to \mathbb{R}$, $A$ aperto, $f:A\to \mathbb{R}$
> Se:
> - $\exists \underline{p},\underline{q}\in A:[\underline{p},\underline{q}]:=\{ t\underline{q}+(1-t)\underline{p}: t\in[0,1] \}\subset A$
> - $f$ è continua su $[\underline{p},\underline{q}]$ e differenziabile su $(\underline{p},\underline{q})$
> 
> $\implies \exists\underline{c}\in(\underline{p},\underline{q}):f(\underline{q})-f(\underline{p})=\nabla f(\underline{c})\cdot(\underline{q}-\underline{p})$
> > [!dimostrazione]-
> > Supponiamo $\underline{p}\neq\underline{q}$
> > $\hat{v}=\frac{\underline{q}-\underline{p}}{||\underline{q}-\underline{p}||}$ direzione di $\mathbb{R}^{2}$
>  > $F(t):=f(\underline{p}+t\hat{v})$, $r\in[0,||\underline{p}-\underline{q}||]$ è ben definita per la prima ipotesi e $F(||\underline{q}-\underline{p}||)=f(\underline{q})$
> > Per la seconda ipotesi $F$ è continua e $\exists F'(t)=\frac{\partial f}{\partial \hat{v}}(\underline{p}+t\hat{v})\;\;\forall t\in(0,||\underline{q}-\underline{p}||)$
> > Per il teorema in una variabile: $f(\underline{q})-f(\underline{p})=F(||\underline{q}-\underline{p}||)-F(0)=F'(t)||\underline{q}-\underline{p}||=\frac{\partial f}{\partial \hat{v}}(\underline{p}+t\hat{v})||\underline{q}-\underline{p}||=$$(\nabla f(\underline{p}+t\hat{v})\cdot \hat{v})||\underline{q}-\underline{p}||=\left( \nabla f(\underline{p}+t\hat{v}) \frac{\underline{q}-\underline{p}}{||\underline{q}-\underline{p}||} \right)||\underline{q}-\underline{p}||$
> > Scegliendo $\underline{c}=\underline{p}+t\hat{v}$ otteniamo la tesi
<div class="page-break" style="page-break-before: always;"></div>

# Matrice Jacobiana
> [!definizione]
> $f:A\subset\mathbb{R}^{n}\to \mathbb{R}^{m}$, $f\in \mathrm{C}^{1}(A)$
> Si chiama matrice Jacobiana di $f$ in $\underline{p} \in A$ la matrice
> $$\begin{flalign}J_{f}(\underline{p})=Df(\underline{p}):=\begin{bmatrix}
\nabla f_{1}(\underline{p}) \\
\dots \\
\nabla f_{m}(\underline{p})
\end{bmatrix} &&\end{flalign}$$

# Derivate parziali di una funzione composta
> [!teorema]
> $g:A\subset \mathbb{R}^{n}\to \mathbb{R}^{m}$, $f:B\subset \mathbb{R}^{m}\to \mathbb{R}^{k}$
> Se:
> - $g(A)\subset B$
> - $g=(g_{1},\dots,g_{m}),f=(f_{1},\dots,f_{k})$
> - $g_{i}:A\to \mathbb{R}$ differenziabile in $\underline{x_{0}}\in A\;\;\forall i\in \{ 1,\dots,m \}$
> - $f_{j}:B\to \mathbb{R}$ differenziabile in $\underline{y_{0}}=g(\underline{x_{0}})\in B\;\;\forall j\in \{ 1,\dots,k \}$
> - $h:=f\circ g$
> 
> $$\begin{flalign}\implies J_{h}(\underline{x_{0}})=J_{f}(\underline{y_{0}})\cdot J_{g}(\underline{x_{0}}) &&\end{flalign}$$
> 
> > [!dimostrazione]-
> > $g:A\subset \mathbb{R}\to \mathbb{R}^{2}$, $f:B\subset \mathbb{R}^{2}\to \mathbb{R}$, $\underline{p_{0}}=g(t_{0})$
> > $f(\underline{p})=f(\underline{p_{0}})+\langle\nabla f(\underline{p_{0}}),(\underline{p}-\underline{p_{0}})\rangle+o(||\underline{p}-\underline{p_{0}}||)$
> > $f(g(t))=f(g(t_{0}))+\langle\nabla f(g(t_{0})),(g(t)-g(t_{0}))\rangle+o(||g(t)-g(t_{0})||)$
> > $$\begin{flalign}\frac{f(g(t))-f(g(t_{0}))}{t-t_{0}}=\frac{\langle\nabla f(g(t_{0})),(g(t)-g(t_{0}))\rangle}{t-t_{0}}+\frac{o(||g(t)-g(t_{0})||)}{t-t_{0}} &&\end{flalign}$$
> > $$\begin{flalign}\lim_{ t \to t_{0} }  \frac{f(g(t))-f(g(t_{0}))}{t-t_{0}}=\lim_{ t \to t_{0} } \left\langle \nabla f(g(t_{0})),\frac{g(t)-g(t_{0})}{t-t_{0}} \right\rangle&&\end{flalign}$$
> > $\implies h'(t_{0})=\nabla f(\underline{p_{0}})\cdot g'(t_{0})$
<div class="page-break" style="page-break-before: always;"></div>

# Derivate parziali di ordine superiore
> [!definizione]
> $f:A\subset \mathbb{R}^{2}\to \mathbb{R}$, $A$ aperto, se $\exists \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}\implies$
> Sono dette derivate parziali seconde pure
> $$\begin{flalign} \frac{\partial^{2}f}{\partial x^{2}}:=\frac{\partial}{\partial x}\left( \frac{\partial f}{\partial x} \right),\;\;\frac{\partial^{2}f}{\partial y^{2}}:=\frac{\partial}{\partial y}\left( \frac{\partial f}{\partial y} \right) &&\end{flalign}$$
> e derivate parziali seconde miste
> $$\begin{flalign} \frac{\partial^{2}f}{\partial x\partial y}:=\frac{\partial}{\partial x}\left( \frac{\partial f}{\partial y} \right),\;\;\frac{\partial^{2}f}{\partial y\partial x}:=\frac{\partial}{\partial y}\left( \frac{\partial f}{\partial x} \right) &&\end{flalign}$$

> [!teorema] Teorema di Schwarz
> Se le derivate parziali seconde miste sono continue $\implies$ coincidono

# Polinomi di Taylor
> [!definizione]
> $m\in \mathbb{N}$, $\underline{p_{0}}=(x_{0},y_{0})\in \mathbb{R}^{2}$
> Si chiama polinomio di Taylor di ordine $m$ di $n=2$ variabili centrato in $\underline{p_{0}}$ una funzione $T:\mathbb{R}^{2}\to \mathbb{R}$
> $$\begin{flalign}T_{m}(x,y)=\sum_{h=0}^{m} \sum_{i=0}^{n} c_{i,n-i}(x-x_{0})^{i}(y-y_{0})^{n-i}\;\;\forall(x,y)\in \mathbb{R}^{2} &&\end{flalign}$$
> tale che $f(\underline{p})=T(\underline{p})+o(||\underline{p} -\underline{p_{0}}||^{m})$

# Matrice Hessiana
> [!definizione]
> $f:A\subset \mathbb{R}^{n}\to \mathbb{R}$, $f\in \mathrm{C}^{2}(A)$
> Si chiama matrice Hessiana di $f$ in $\underline{p} \in A$ la matrice
> $$\begin{flalign}H_{f}(\underline{p})=D^{2}f(\underline{p}):=\begin{bmatrix}
\frac{\partial^{2}f}{\partial x_{1}^{2}}(\underline{p}) & \dots & \frac{\partial^{2}f}{\partial x_{n}\partial x_{1}}(\underline{p}) \\ \\
\dots & & \dots \\
\frac{\partial^{2}f}{\partial x_{n}\partial x_{1}}(\underline{p}) & \dots& \frac{\partial^{2}f}{\partial x_{n}^{2}}(\underline{p})
\end{bmatrix}=\begin{bmatrix}
\nabla \left( \frac{\partial f}{\partial x_{1}} \right)(\underline{p}) \\
\dots \\
\nabla\left( \frac{\partial f}{\partial x_{n}} \right)(\underline{p})
\end{bmatrix} &&\end{flalign}$$
<div class="page-break" style="page-break-before: always;"></div>

> [!osservazione]-
> $H_{f}(\underline{p})$ è simmetrica

> [!teorema]
> $T_{2}(\underline{p})=f(\underline{p_{0}})+\langle\nabla f(\underline{p}),(\underline{p} -\underline{p_{0}})\rangle+\frac{1}{2}\langle H_{f}(\underline{p})\cdot(\underline{p} -\underline{p_{0}})^{T},(\underline{p} -\underline{p_{0}})\rangle$
> > [!dimostrazione]-
> > $\underline{p} \in \mathrm{B}(\underline{p_{0}},r)$, $\hat{v}:=\frac{\underline{p} -\underline{p_{0}}}{||\underline{p} -\underline{p_{0}}||}=(v_{1},v_{2})$, $F(t):=f(\underline{p_{0}}+t\hat{v})\;\;t\in(-r,r)$
> > Poiché $g(t)=\underline{p_{0}}+t\hat{v}\in \mathrm{C}^{2}((-r,r))$ anche $F(t)=f(g(t))\in \mathrm{C}^{2}((-r,r))$
> > Applicando la formula di Taylor in una variabile per $t=0$ si ottiene
> > $F(t)=F(0)+F'(0)\cdot t+\frac{1}{2}F''(0)\cdot t^{2}+o(t^{2})$
> > $F'(t)=\nabla f(\underline{p}+t\hat{v})\cdot \hat{v}$
> > $$\begin{flalign}F''(t)=\frac{\partial^{2}f}{\partial x^{2}}(\underline{p_{0}}+t\hat{v})\cdot v_{1}^{2}+2 \frac{\partial^{2} f}{\partial y\partial x}(\underline{p_{0}}+t\hat{v})\cdot v_{1}\cdot v_{2}+\frac{\partial^{2}f}{\partial y^{2}}(\underline{p_{0}}+t\hat{v})\cdot v_{2}^{2} &&\end{flalign}$$
> > $F(0)=f(\underline{p_{0}})$, $F'(0)=\langle\nabla f(\underline{p_{0}}), \hat{v}\rangle$, $F''(0)=\langle H_{f}(\underline{p_{0}})\cdot\hat{v}^{T}, \hat{v}\rangle$
> > $F(t)=f(\underline{p_{0}})+\langle\nabla f(\underline{p_{0}}), \hat{v}\rangle t+\frac{1}{2}\langle H_{f}(\underline{p_{0}})\cdot\hat{v}^{T}, \hat{v}\rangle t^{2}+o(t^{2})$
> > Sostituendo $t=\underline{p} -\underline{p_{0}}$ e $\hat{v}$ si ottiene la tesi

# Massimi e minimi
> [!definizione]
> $f:A\subset \mathbb{R}^{n}\to \mathbb{R}$
> $\underline{p_{0}}\in A$ si dice punto di
> - massimo relativo di $f$ in $A$ se $\exists r_{0}>0:f(\underline{p})\leq f(\underline{p_{0}})\;\;\forall \underline{p} \in A\cap B(\underline{p_{0}},r_{0})$
> - massimo assoluto di $f$ in $A$ se $f(\underline{p})\leq f(\underline{p_{0}})\;\;\forall \underline{p} \in A$
> - minimo relativo di $f$ in $A$ se $\exists r_{0}>0:f(\underline{p})\geq f(\underline{p_{0}})\;\;\forall \underline{p} \in A\cap B(\underline{p_{0}},r_{0})$
> - minimo assoluto di $f$ in $A$ se $f(\underline{p})\geq f(\underline{p_{0}})\;\;\forall \underline{p} \in A$
> 
> I punti di massimo e minimo relativi sono detti estremi liberi

> [!osservazione]-
> Non confondere punto di massimo e massimo di una funzione: $\mathrm{Max}_{A}f:=\mathrm{Max}\{ f(\underline{p}):p \in A \}$ se esiste è unico
<div class="page-break" style="page-break-before: always;"></div>

> [!teorema] Teorema di Fermat
> $A\subset \mathbb{R}^{n}$ aperto, se $\exists \underline{p_{0}}\in A$ tale che:
> - $\exists \nabla f(\underline{p_{0}})$
> - $\underline{p_{0}}$ è un estremo libero di $f$ in $A$
>   
> $\implies \nabla f(\underline{p_{0}})=\underline{0}$
> > [!dimostrazione]-
> > $A$ aperto $\implies \exists\delta>0:\underline{p_{0}}+t\hat{e_{i}}\in A$ se $t\in(-\delta,\delta)$
> > $F_{i}:(-\delta,\delta)\to \mathbb{R}$, $F_{i}(t)=f(\underline{p_{0}}+t\hat{e_{i}})$
> > Dalle ipotesi, $\forall i\in \{ 1,\dots,n \}$:
> > - $\exists \frac{\partial f}{\partial x_{i}}(\underline{p_{0}})\iff F$ è derivabile in $t=0$ e $F_{i}'(0)=\frac{\partial f}{\partial x_{i}}(\underline{p_{0}})$
> > - $t=0$ è un estremo libero di $F_{i}$
> > 
> > Per il teorema in una variabile $F_{i}'(0)=0$ $\implies \nabla f(\underline{p_{0}})=(0,\dots,0)=\underline{0}$

> [!definizione]
> Un punto $\underline{p_{0}}\in A$ si chiama punto stazionario o critico di $f$ se $\exists \nabla f(\underline{p_{0}})=\underline{0}$

# Matrice positiva
> [!definizione]
> $H=[h_{ij}]\in M_{n}(\mathbb{R})$ si dice:
> - positiva se $\langle H\cdot\hat{v}, \hat{v}\rangle>0\;\;\forall \hat{v}\in \mathbb{R}^{n}\setminus \{ \underline{0} \}$
> - semi-definita positiva se $\langle H\cdot\hat{v}, \hat{v}\rangle\geq0\;\;\forall \hat{v}\in \mathbb{R}^{n}\setminus \{ \underline{0} \}$
> - negativa se $\langle H\cdot\hat{v}, \hat{v}\rangle<0\;\;\forall \hat{v}\in \mathbb{R}^{n}\setminus \{ \underline{0} \}$
> - semi-definita negativa se $\langle H\cdot\hat{v}, \hat{v}\rangle\leq0\;\;\forall \hat{v}\in \mathbb{R}^{n}\setminus \{ \underline{0} \}$
> 
> $$\begin{flalign}D_{i}:=\det \begin{bmatrix}
h_{11} & \dots & h_{1i}\\
\dots & & \dots \\
h_{i_{1}} & \dots & h_{ii}
\end{bmatrix}\;\;1\leq i\leq n &&\end{flalign}$$
> $H$ è:
> - positiva $\iff D_{i}>0\;\;\forall i\in\{ 1,\dots,n \}$
> - negativa $\iff D_{i}>0$ per $i$ pari, $D_{i}<0$ per $i$ dispari
> - se $\det(H)\neq0$ e nessuna delle condizioni precedenti $\implies$ non è semi-definita
<div class="page-break" style="page-break-before: always;"></div>

> [!osservazione]-
> $H\in M_{2}(\mathbb{R})\implies H$ è:
> - positiva se $h_{11}>0\land \det(H)>0$
> - negativa se $h_{11}<0\land \det(H)>0$
> - se $\det(H)<0\implies$ non è semi-definita

### Matrice Hessiana ed estremi liberi
> [!teorema]
> $A\subset \mathbb{R}^{n}$ aperto, $f\in \mathrm{C}^{2}(A)$, $\underline{p_{0}}$ punto stazionario
> Se $H_{f}(\underline{p_{0}})$ è:
> - positiva $\implies \underline{p_{0}}$ è un punto di minimo relativo
> - negativa $\implies \underline{p_{0}}$ è un punto di massimo relativo
> - non semi-definita $\implies \underline{p_{0}}$ è un punto di sella

# Teorema di Weierstrass
> [!teorema]
> $f:A\subset \mathbb{R}^{n}\to \mathbb{R}$ continua su $A$ limitato e chiuso
> $\implies \exists \mathrm{Max}_{A}f=f(\underline{p_{1}})\land \exists \mathrm{Min}_{A}f=f(\underline{p_{2}})$
> Per $\underline{p_{i}}\in A\;\;i=1,2$ si verifica una delle seguenti:
> - $\underline{p_{i}}\in \mathring{A} \land \exists \nabla f(\underline{p_{i}})=\underline{0}$
> - $\underline{p_{i}}\in\mathring{A} \land \nexists \nabla f(\underline{p_{i}})$
> - $\underline{p_{i}}\in \partial A$

# Parametrizzazione
> [!definizione]
> Si chiama parametrizzazione della frontiera $\partial A$ una funzione $\gamma:B\subset \mathbb{R}^{n}\to A\subset \mathbb{R}^{n+1}$, $\gamma(t_{1},\dots,t_{n})=(\gamma_{1}(t_{1},\dots,t_{n}),\dots,\gamma_{n+1}(t_{1},\dots,t_{n}))$, con le seguenti proprietà:
> - $B$ chiuso e limitato
> - $\gamma(B)=\partial A$
> - $\gamma_{1},\dots ,\gamma_{n+1}\in \mathrm{C}^{0}(B)\cap \mathrm{C}^{1}(\mathring{B})$
<div class="page-break" style="page-break-before: always;"></div>

> [!teorema]
> $f:A\to \mathbb{R}$, $f\in \mathrm{C}^{1}(A)$ da massimizzare/minimizzare sulla frontiera
> $F:B\to \mathbb{R}$, $F(t_{1},\dots,t_{n}):=f(\gamma(t_{1},\dots,t_{n}))\implies$
> - $\mathrm{Max}_{\partial A}f=\mathrm{Max}_{B}F$
> - $\mathrm{Min}_{\partial A}f=\mathrm{Min}_{B}F$

# Metodo dei moltiplicatori di Lagrange
> [!definizione]
> Se $A:=\{ (x,y)\in \mathbb{R}^{2}:g(x,y)\leq0 \}\implies \partial A=\{ (x,y)\in \mathbb{R}^{2}:g(x,y)=0 \}$
> Un insieme del piano $V:=\partial A$ è detto vincolo ed è una curva

> [!teorema] Metodo dei moltiplicatori di Lagrange
> $f,g\in \mathrm{C}^{1}(\mathbb{R}^{2})$, $V$ vincolo
> Se:
> - $\exists \mathrm{Min}_{V}f=f(\underline{p_{0}})\;\;\underline{p_{0}}\in V$ (o $\mathrm{Max}$)
> - $\exists \nabla g(\underline{p_{0}})\neq(0,0)$
> 
> $\implies \exists \lambda_{0}$ detto moltiplicatore tale che $(x_{0},y_{0},\lambda_{0})$ è un punto stazionario di $L(x,y,\lambda):=f(x,y)+\lambda \cdot g(x,y)$ detta funzione lagrangiana
> Ovvero
> $$\begin{flalign}\nabla L(x,y,\lambda )=(0,0,0)\iff\begin{cases}
\frac{\partial L}{\partial\lambda}(x,y,\lambda)=0 \\
\frac{\partial L}{\partial x}(x,y,\lambda)=0 \\
\frac{\partial L}{\partial y}(x,y,\lambda)=0
\end{cases}\iff\begin{cases}
g(x,y)=0 \\
\nabla f(x,y)=\lambda\nabla g(x,y)
\end{cases} &&\end{flalign}$$
> 
> Un punto $\underline{p_{0}}\in V$ verificante tali condizioni per un opportuno $\lambda_{0}$ si dice punto stazionario di $f$ rispetto a $V$, pertanto vanno ovviamente studiati anche i punti stazionari di $f$ nella parte interna $\mathring{A}$
<div class="page-break" style="page-break-before: always;"></div>

> [!teorema]
> Se $g(\underline{p_{0}})=0$ e $\exists \frac{\partial g}{\partial y}(\underline{p_{0}})\neq0$ (o analogamente con $x$) $\implies V$ è localmente grafico di una funzione $y=\varphi(x)$, cioè $\exists\delta>0$ e $\varphi:(x_{0}-\delta,x_{0}+\delta)\to \mathbb{R}$, $\exists r_{0}>0$ tali che
> - $V\cap \mathrm{B}(\underline{p_{0}},r_{0})=\{ (x,\varphi(x)):x \in(x_{0}-\delta,x_{0}+\delta) \}$
> - $\varphi$ è derivabile e $$\begin{flalign}\varphi'(x)=- \frac{\frac{\partial g}{\partial x}(x,\varphi(x))}{\frac{\partial g}{\partial y}(x,\varphi(x))}\;\;\forall x \in(x_{0}-\delta,x_{0}+\delta) &&\end{flalign}$$

> [!dimostrazione]- Dimostrazione del teorema dei moltiplicatori di Lagrange
> Se $\frac{\partial g}{\partial y}(\underline{p_{0}})\neq0$ (analogamente con $x$), $h:=f(x,\varphi(x))\;\;x \in(x_{0}-\delta,x_{0}+\delta)$
> Essendo $\underline{p_{0}}\in V$ punto di minimo di $f$ su $V\implies x_{0}$ è un punto di minimo di $h$ su $(x_{0}-\delta,x_{0}+\delta)$ e $h\in \mathrm{C}^{1}((x_{0}-\delta,x_{0}+\delta))$
> Per quanto visto prima
> $$\begin{flalign}0=h'(x_{0})=\frac{\partial f}{\partial x}(x_{0},\varphi(x_{0}))+\frac{\partial f}{\partial y}(x_{0},\varphi(x_{0}))\varphi'(x_{0})=\frac{\partial f}{\partial x}(\underline{p_{0}})-\frac{\partial f}{\partial y}(\underline{p_{0}}) \frac{\frac{\partial g}{\partial x}(\underline{p_{0}})}{\frac{\partial g}{\partial y}(\underline{p_{0}})} &&\end{flalign}$$
> $$\begin{flalign}\iff \det \begin{bmatrix}
\frac{\partial f}{\partial x}(\underline{p_{0}}) & \frac{\partial f}{\partial y}(\underline{p_{0}}) \\
\frac{\partial g}{\partial x}(\underline{p_{0}}) & \frac{\partial g}{\partial y}(\underline{p_{0}})
\end{bmatrix}=\det \begin{bmatrix}
\nabla f(\underline{p_{0}}) \\
\nabla g(\underline{p_{0}})
\end{bmatrix}=0 &&\end{flalign}$$
> $\iff \exists \lambda_{0}\in \mathbb{R}:\nabla f(\underline{p_{0}})=-\lambda_{0}\cdot \nabla g(\underline{p_{0}})$


> [!teorema]
> $f,g\in \mathrm{C}^{1}(\mathbb{R}^{3})$, $V:=\{ (x,y,z)\in\mathbb{R}^{3}: g(x,y,z)=0\}$
> Se:
> - $\exists \mathrm{Min}_{V}f=f(\underline{p_{0}})$ (o $\mathrm{Max}$)
> - $\nabla g(\underline{p_{0}})\neq(0,0,0)$
> 
> $\implies \exists \lambda_{0}\in \mathbb{R}:\nabla f(\underline{p_{0}})=-\lambda_{0}\cdot \nabla g(\underline{p_{0}})$
