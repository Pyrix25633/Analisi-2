# Integrale doppio su un rettangolo
> [!definizione]
> $f:A\subset \mathbb{R}^{2}\to \mathbb{R}$, $A=[a,b]\times[c,d]$, $f$ limitata (e non negativa)
> Il trapezoide sotteso al grafico di $f$ in $A$ è l'insieme dei punti
> $T_{f}(A):=\{ (x,y,z)\in \mathbb{R}^{3}:0\leq z\leq f(x,y)\land(x,y)\in A \}$

### Suddivisione
> [!definizione]
> Si chiama suddivisione di $[a,b]$ un insieme finito $\{ x_{0},x_{1},\dots,x_{n} \}:a=x_{0}<x_{1}<{\dots}<x_{n}=b$ 
> Si chiama suddivisione di $A$ l'insieme $\mathcal{D}:=\mathcal{D}_{1}\times\mathcal{D}_{2}=\{ x_{0},\dots,x_{n} \}\times \{ y_{0},\dots,y_{m} \}=\{ (x_{i},y_{j}):i=0,\dots,n\land j=0,\dots,m \}$
> $A$ resta suddiviso in $n\times m$ rettangoli $A_{ij}:=[x_{i-1},x_{i}]\times[y_{j-1},y_{j}]$ di area $\mathrm{area}(A_{ij})=(x_{i}-x_{i-1})\cdot(y_{j}-y_{j-1})$

### Somma superiore e inferiore
> [!definizione]
> $$\begin{flalign}&M_{ij}:=\mathrm{sup}_{A_{ij}}\{ f \}\\
> &m_{ij}:=\mathrm{inf}_{A}\{ f \}&&\end{flalign}$$
> Si chiamano somma superiore e inferiore
> $$\begin{flalign}&S(f,\mathcal{D}):=\sum_{i=1}^{n} \sum_{j=1}^{m} M_{ij}\cdot area(A_{ij})\\
&s(f,\mathcal{D}):=\sum_{i=1}^{n} \sum_{j=1}^{m} m_{ij}\cdot \mathrm{area}(A_{ij})&&\end{flalign}$$
> Proprietà:
> - Se $f\geq0$, $M_{ij}\cdot \mathrm{area}(A_{ij})$ e $m_{ij}\cdot \mathrm{area}(A_{ij})$ rappresentano il volume di un parallelepipedo che approssima il grafico per eccesso e per difetto
> - $\mathrm{area}(A_{ij})\cdot \mathrm{inf}_{A}\{ f \}\leq s(f,\mathcal{D})\leq S(f,\mathcal{D})\leq \mathrm{area}(A_{ij})\cdot \mathrm{sup}_{A}\{ f \}$
> - $\mathcal{D}',\mathcal{D}''$ suddivisioni qualunque, $s(f,\mathcal{D}')\leq S(f,\mathcal{D}'')$
<div class="page-break" style="page-break-before: always;"></div>

# Funzione integrabile secondo Riemann
> [!definizione]
> Se $\mathrm{sup}\{ s(f,\mathcal{D}) \}=\mathrm{inf}\{ S(f,\mathcal{D}) \}=L\in \mathbb{R}\implies f\in\mathcal{R}(A)$ e si denota
> $$\begin{flalign}L=\iint_{A}f=\mathrm{vol}(T_{f}(A)) &&\end{flalign}$$

> [!teorema] Teoremi
> ### Esistenza dell'integrale
> $f\in \mathrm{C}^{0}(A)\implies f\in\mathcal{R}(A)$
> 
> ### Linearità
> $\iint_{A}(\alpha f+\beta g)=\alpha \iint_{A}f+\beta \iint_{A}g$
> 
> ### Monotonia
$g\leq f\implies \iint_{A}g\leq \iint_{A}f$
> 
> ### Valore assoluto
> $|\iint_{A}f|\leq \iint_{A} |f|$

> [!teorema] Teorema della media integrale
> $f:A\subset \mathbb{R}^{2}\to \mathbb{R}$, $f\in\mathcal{R}(A)$
> $$\begin{flalign}\mathrm{inf}_{A}\{ f \}\leq \frac{1}{\mathrm{area(A)}}\iint_{A}f=z_{0}\leq \mathrm{sup}_{A}\{ f \} &&\end{flalign}$$
> Inoltre se $f\in \mathrm{C}^{0}(A)\implies \exists \underline{p_{0}}:f(\underline{p_{0}})=z_{0}$
<div class="page-break" style="page-break-before: always;"></div>

# Formula di riduzione sui rettangoli
> [!formule] Formula
> Se $\forall y\in[c,d]\;\;x \in[a,b]\to f(x,y)$ è integrabile $\implies \forall x \in[a,b]\;\;y\in[c,d]\to f(x,y)$ è integrabile e
> $$\begin{flalign}\iint_{A}f=\int_{c}^{d} \int_{a}^{b}f(x,y)\,dx\,dy &&\end{flalign}$$
> Viceversa in modo analogo
> 
> In particolare se $f\in \mathrm{C}^{0}(A)$ valgono entrambe e
> $$\begin{flalign}\int_{c}^{d} \int_{a}^{b}f(x,y)\,dx\,dy=\int_{a}^{b} \int_{c}^{d}f(x,y)\,dy\,dx &&\end{flalign}$$

# Integrale doppio su un insieme generale
> [!definizione]
> Se $A\subset \mathbb{R}^{2}$ è limitato ma non rettangolare è possibile definire una nuova funzione
> $A\subset Q=[a,b]\times[c,d]$, $\tilde{f}:Q\to \mathbb{R}$
> $$\begin{flalign}\tilde{f}(x,y)=\begin{cases}
f(x,y),&(x,y)\in A \\
0,&(x,y)\in Q\setminus A
\end{cases} &&\end{flalign}$$
> Di conseguenza $\tilde{f}\in\mathcal{R}(Q)\implies f\in\mathcal{R}(A)$ e
> $$\begin{flalign}\iint_{A}f=\iint_{Q}\tilde{f}=\mathrm{vol}(T_{\tilde{f}}(Q)) &&\end{flalign}$$

> [!osservazione]-
> $\tilde{f}$ non è continua su $\partial A$
> $T_{\tilde{f}}(Q)=P\cup T_{f}(A)$ dove $P$ è una parte limitata del piano $z=0$ e $\mathrm{vol(P)=0}$
> Se non fosse definita $\mathrm{area}(A)$ non sarebbe possibile calcolare l'integrale doppio

# Insieme misurabile
> [!definizione]
> $A\subset \mathbb{R}^{2}$ limitato, $f:A\to \mathbb{R}$, $f(x,y):=1$ se $(x,y)\in A$
> $A$ si dice misurabile secondo Peano-Jordan se $f\in\mathcal{R}(A)$ e $\mathrm{area}(A)=|A|_{2}=\iint_{A}f$

> [!osservazione]-
> $Q=[a,b]\times[c,d]$ è misurabile e $|Q|_{2}=(b-a)\cdot(d-c)$
<div class="page-break" style="page-break-before: always;"></div>

> [!teorema]
> $A\subset \mathbb{R}^{2}$ limitato
> $A$ è misurabile $\iff \partial A$ è misurabile e $|\partial A|_{2}=0$

> [!definizione]
> $g:[a,b]\to \mathbb{R}$ integrabile $\implies G_{g}:=\{ (x,g(x)):x \in[a,b] \}$ è misurabile e $|G_{g}|_{2}=0$

> [!osservazione]-
> $A\subset \mathbb{R}^{2}$ limitato, $g_{i}:[a_{i},b_{i}]\to \mathbb{R}$ continua (e quindi integrabile) ($i=1,\dots,k$)
> $\partial A=\bigcup_{i=1}^{k}G_{g_{i}}=G_{g_{1}}\cup{\dots}\cup G_{g_{k}}\implies A$ è misurabile

# Integrale doppio su un insieme misurabile
> [!teorema]
> $f:A\to \mathbb{R}$, $f\in \mathrm{C}^{0}(A)$ limitata, $A\subset \mathbb{R}^{2}$ limitato e misurabile
> $\implies f\in\mathcal{R}(A)$

> [!osservazione]-
> Se $A$ è chiuso e limitato, allora se $f$ è continua è sicuramente anche limitata e quindi $f\in\mathcal{R}(A)$

> [!teorema]
> $A\subset \mathbb{R}^{2}$ limitato e misurabile, $A=B\cup C$ misurabili, $|C|_{2}=0$, $f\in\mathcal{R}(A)$
> $$\begin{flalign}\implies \iint_{A}f=\iint_{B}f &&\end{flalign}$$

> [!osservazione]-
> $A\subset \mathbb{R}^{2}$ limitato e misurabile, $f\in\mathcal{R}(A)$
$$\begin{flalign}\implies \iint_{A}f=\iint_{\mathring{A}}f &&\end{flalign}$$
<div class="page-break" style="page-break-before: always;"></div>

# Integrale doppio su un dominio semplice e formula di riduzione
> [!definizione]
> $A\subset \mathbb{R}^{2}$ si dice semplice o normale rispetto all'asse $y$ se
> - $\exists g_{1},g_{2}\in \mathrm{C}^{0}([a,b]):g_{1}\leq g_{2}$ su $[a,b]$
> - $A=\{ (x,y)\in \mathbb{R}^{2}:x \in[a,b]\land g_{1}(x)\leq y\leq g_{2}(x) \}$
> 
> Analogamente rispetto all'asse $x$
> Un dominio semplice è limitato e misurabile

> [!formule]
> $A\subset \mathbb{R}^{2}$ semplice rispetto a $y$, $f\in \mathrm{C}^{0}(A)\implies f\in\mathcal{R}(A)$ e
> $$\begin{flalign}|A|_{2}=\iint_{A}1=\int_{a}^{b}(g_{2}(x)-g_{1}(x))\,dx &&\end{flalign}$$
> $$\begin{flalign}\iint_{A}f=\int_{a}^{b}\int_{g_{1}(x)}^{g_{2}(x)}f(x,y)\,dy\,dx &&\end{flalign}$$
> Analogamente per $x$

# Additività dell'integrale doppio
> [!teorema]
> $A_{1},\dots,A_{m}\subset \mathbb{R}^{2}$ insiemi semplici tali che $A_{i}\cap A_{j}\subset \partial A_{i}\cap \partial A_{j}\;\;\forall i,j=1,\dots,m\land i\neq j$,
> $B=A_{1}\cup{\dots}\cup A_{m}$,  $f:B\to \mathbb{R}$ tale che $f\in\mathcal{R}(A_{i})\;\;\forall i=1,\dots,m$
> $\implies f\in\mathcal{R}(B)$ e $$\begin{flalign}\iint_{B}f=\sum_{i=1}^{m}\iint_{A_{i}}f &&\end{flalign}$$
<div class="page-break" style="page-break-before: always;"></div>

# Sostituzione di variabili
> [!definizione]
> $D,D^{*}\subset \mathbb{R}^{2}$ aperti, limitati e misurabili, $\psi:D^{*}\to D$, $\psi(u,v)=(\psi_{1}(u,v),\psi_{2}(u,v))$
> La mappa $\psi$ si dice cambiamento o sostituzione di variabili se:
> - è biiettiva
> - $\psi_{i}\in \mathrm{C}^{1}(D^{*})$ e $\psi_{i}, \frac{\partial \psi_{i}}{\partial u}, \frac{\partial \psi_{i}}{\partial v}:D^{*}\to \mathbb{R}$ sono limitate ($i=1,2$)
> - $\det(J_{\psi}(u,v))\neq0\;\;\forall(u,v)\in D^{*}$
> 
> Per definizione $dD^{*}=du\,dv$, $dD=dx\,dy$ e per la sostituzione $dD=|\det(J_{\psi}(u,v))|dD^{*}$

> [!teorema]
> $D,D^{*}\subset \mathbb{R}^{2}$ aperti, limitati e misurabili, $\psi:D^{*}\to D$ cambiamento di variabili
> $$\begin{flalign}\iint_{D}f(x,y)\,dx\,dy=\iint_{D^{*}}f(\psi(u,v))\cdot |\det(J_{\psi}(u,v))|\,du\,dv &&\end{flalign}$$
