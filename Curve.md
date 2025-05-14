# Curva in $\mathbb{R}^{n}$
> [!definizione]
> Si chiama curva una mappa $\gamma:I\to \mathbb{R}^{n}$ continua, $\gamma(t):=(\gamma_{1}(t),\dots,\gamma_{n}(t))$, $I$ intervallo di $\mathbb{R}$, $\gamma_{i}(t):I\to \mathbb{R}$ ($i=1,..,n$)
> Se $I=[a,b]$, $\gamma(a)$ e $\gamma(b)$ si chiamano estremi della curva
> L'insieme $\Gamma=\gamma(I)\subset \mathbb{R}^{n}$ si chiama **sostegno** o **supporto** della curva
> $\underline{x}=(x_{1},\dots,x_{n})=\gamma(t)$ si chiama **equazione parametrica** o anche legge oraria della curva
> 
> ### Curva chiusa
> Se $I=[a,b]$ e gli estremi coincidono, $\gamma(a)=\gamma(b)$, $\gamma$ si dice chiusa
> 
> ### Curva semplice
> $\gamma$ si dice semplice se è iniettiva, oppure se è chiusa e $\gamma:[a,b)\to \mathbb{R}^{n}$ è iniettiva
> 
> ### Curve cartesiane
> $f\in \mathrm{C}^{0}([a,b])$, $\gamma,\gamma^{*}:[a,b]\to \mathbb{R}^{n}$, $\gamma(t)=(t,f(t)),\gamma^{*}(t)=(f(t),t)$ sono dette curve piane cartesiane

> [!osservazione]-
> Se almeno una componente $\gamma_{i}$ p iniettiva $\implies \gamma$ è iniettiva

# Orientazione di una curva semplice
> [!definizione]
> Una curva semplice $\gamma:I\to \mathbb{R}^{n}$ induce un'orientazione, anche detta verso, al suo sostegno
> Si dice che $\underline{x_{1}}=\gamma(t_{1})$ precede $\underline{x_{2}}=\gamma(t_{2})$ se $t_{1}<t_{2}$
<div class="page-break" style="page-break-before: always;"></div>

# Vettore velocità e retta tangente
> [!definizione]
> $\gamma:I\to \mathbb{R}^{n}$ curva, se $\gamma_{i}:I\to \mathbb{R}$ sono derivabili in $t_{0}\in I$
> $\gamma'(t_{0}):=(\gamma_{1}'(t_{0}),\dots,\gamma_{n}'(t_{0}))$ è detto vettore velocità di $\gamma$ in $t_{0}$
> Se $t\to t_{0}$ $\gamma(t)=\gamma(t_{0})+\gamma'(t_{0})(t-t_{0})+o(t-t_{0})$

> [!osservazione]-
> $\gamma'(t_{0})=J_{\gamma}(t_{0})^{T}$

> [!definizione]
> Se $\gamma'(t_{0})\neq\underline{0}$ si chiama retta tangente a $\gamma$ in $\underline{x_{0}}=\gamma(t_{0})$ la retta $\underline{x}=\gamma(t_{0})+\gamma'(t_{0})(t-t_{0})$
> 
> $\gamma:I\to \mathbb{R}^{n}$ si dice di classe $\mathrm{C}^{m}$ se $\gamma_{i}\in \mathrm{C}^{m}(I)\;\;\forall i\in \{ 1,\dots,n \}$
> $\gamma$ si dice regolare se $\gamma \in \mathrm{C}^{1}(I)$ e $\gamma'(t)\neq \underline{0}\;\;\forall t \in I$
> Si chiama versore o direzione tangente a $\gamma$ il campo vettore
> $$\begin{flalign}T_{\gamma}(t):=\frac{\gamma'(t)}{||\gamma'(t)||} &&\end{flalign}$$
> $\gamma:[a,b]\to \mathbb{R}^{n}$ si dice $\mathrm{C}^{1}$ a tratti se $\exists \{ a=t_{0}<{\dots}<t_{k}=b \}$ suddivisione di $[a,b]$ tale che $\gamma_{j}=\gamma|_{[t_{j-1},t_{j}]}:[t_{j-1},t_{j}]\to \mathbb{R}^{n}$ è di classe $\mathrm{C}^{1}$ e $\gamma=\bigcup_{j=1}^{k}\gamma_{j}$

# Cambiamento di parametro
> [!definizione]
> $\gamma:I\to \mathbb{R}^{n},\tilde{\gamma}:\tilde{I}\to \mathbb{R}^{n}$ di classe $\mathrm{C}^{1}$ si dicono equivalenti se $\exists \varphi:\tilde{I}\to I$ biiettiva tale che $\varphi \in \mathrm{C}^{1}(\tilde{I})$, $\varphi'(\tau)\neq0$ e $\tilde{\gamma}(\tau)=\gamma(\varphi(\tau))\;\;\forall \tau \in \tilde{I}$
> $\tau \in \tilde{I}\to t=\varphi(\tau)\in I$ si dice cambiamento di parametrizzazione
> Inoltre $\Gamma=\gamma([a,b])=\tilde{\gamma}([\alpha,\beta])$

> [!osservazione]-
> Se $\varphi(\tau)>0\;\;\forall \tau \in \tilde{I}$ allora $\gamma$ e $\tilde{\gamma}$ hanno lo stesso verso, altrimenti se $\varphi(\tau)<0\;\;\forall \tau \in \tilde{I}$ hanno verso opposto
<div class="page-break" style="page-break-before: always;"></div>

# Lunghezza di una curva
> [!definizione]
> $\gamma:[a,b]\to \mathbb{R}^{n}$ curva, $\mathcal{D}=\{ a=t_{0}<{\dots}<t_{k}=b \}$ suddivisione di $[a,b]$ induce una suddivisione del sostegno di $\gamma$ in $k+1$ punti definiti da $\gamma(t_{0}),\dots,\gamma(t_{k})$ e quindi $k$ segmenti $[\gamma(t_{i-1}),\gamma(t_{i})]:=\{ s\cdot \gamma(t_{i})+(1-s)\cdot \gamma(t_{i-1}):0\leq s\leq1 \}$
> La lunghezza della spezzata definita da $\bigcup_{i=1}^{k}[\gamma(t_{i-1}),\gamma(t_{i})]$ è data da $L(\gamma,\mathcal{D}):=\sum_{i=1}^{k}||\gamma(t_{i})-\gamma(t_{i-1})||\in[0,+\infty)$
> $L(\gamma):=\mathrm{sup}_{\mathcal{D}}\{ L(\gamma,\mathcal{D}) \}\in[0,+\infty]$
> Se $L(\gamma)<+\infty\implies \gamma$ si dice rettificabile e $L(\gamma)$ è detta lunghezza di $\gamma$

> [!teorema]
> $\gamma:[a,b]\to \mathbb{R}^{n}$ curva, $\gamma \in \mathrm{C}^{1}([a,b])$
> $\implies \gamma$ è rettificabile e
> $$\begin{flalign}L(\gamma)=\int_{a}^{b}||\gamma'(t)||\,dt=\int_{a}^{b}\sqrt{\gamma_{1}'^{2}(t)+{\dots}+\gamma_{n}'^{2}(t)}\,dt &&\end{flalign}$$

> [!osservazione]-
> $\gamma:[a.b]\to \mathbb{R}^{2}$ curva piana cartesiana, $\gamma,f \in \mathrm{C}^{1}([a,b])$, $\gamma(t):=(t,f(t))$
> $\implies \gamma$ è rettificabile e $L(\gamma)=\int_{a}^{b}\sqrt{1+f'^{2}(t)}\,dt$

# Indipendenza della lunghezza dalla parametrizzazione
> [!teorema]
> $\gamma:[a,b]\to \mathbb{R}^{n},\tilde{\gamma}:[\alpha,\beta]\to \mathbb{R}^{n}$ curve di classe $\mathrm{C}^{1}$ equivalenti
> $\implies L(\tilde{\gamma})=L(\gamma)$
> > [!dimostrazione]-
> > $\varphi:[\alpha,\beta]\to[a,b]$ cambiamento di parametrizzazione, $\varphi(\tau)>0\;\;\forall \tau \in[\alpha,\beta]$
> > $$\begin{flalign}{\dots}&=\int_{\alpha}^{\beta}||\tilde{\gamma}'(\tau)||\,d\tau=\int_{\alpha}^{\beta}||\gamma'(\varphi(\tau))\cdot \varphi'(\tau)||\,d\tau=\int_{\alpha}^{\beta}||\gamma'(\varphi(\tau))||\cdot\varphi'(\tau)\,d\tau\\
> > &=\int_{\varphi(\alpha)}^{\varphi(\beta)}||\gamma'(t)||\,dt=\int_{a}^{b}||\gamma'(t)||\,dt={\dots} &&\end{flalign}$$
<div class="page-break" style="page-break-before: always;"></div>

> [!osservazione]-
> Una curva $\mathrm{C}^{1}$ a tratti $\gamma=\sum_{i=1}^{k}\gamma_{i}$, $\gamma_{i}:[t_{i-1},t_{i}]\to \mathbb{R}^{n}$ è rettificabile e
> $$\begin{flalign}L(\gamma)=\sum_{i=1}^{k}\int_{t_{i-1}}^{t_{i}}||\gamma_{i}'(t)||\,dt &&\end{flalign}$$

# Integrali curvilinei di prima specie
> [!definizione]
> $\gamma:[a,b]\to \mathbb{R}^{n}$ curva di classe $\mathrm{C}^{1}$, $f:\Gamma\to \mathbb{R}$ continua
> $$\begin{flalign}\int_{\gamma}f\,ds:=\int_{a}^{b}f(\gamma(t))\cdot ||\gamma'(t)||\,dt &&\end{flalign}$$
> si chiama integrale curvilineo di prima specie di $f$ lungo $\gamma$
> Se $\gamma$ è chiusa e semplice si indica anche con $\oint_{\gamma}f\,ds$

> [!teorema]
> $\gamma:[a,b]\to \mathbb{R}^{n},\tilde{\gamma}:[\alpha,\beta]\to \mathbb{R}^{n}$ curve di classe $\mathrm{C}^{1}$ equivalenti, $f:\Gamma\to \mathbb{R}$ continua
> $$\begin{flalign}\implies \int_{\tilde{\gamma}}f\,ds=\int_{\gamma}f\,ds &&\end{flalign}$$
> > [!dimostrazione]-
> > $\varphi:[\alpha,\beta]\to[a,b]$ cambio di parametrizzazione, $\varphi(\tau)\neq0\;\;\forall \tau \in[\alpha,\beta]$
> > $$\begin{flalign}{\dots}&=\int_{\alpha}^{\beta}f(\tilde{\gamma}(\tau))\cdot ||\tilde{\gamma}'(\tau)||\,d\tau=\int_{\alpha}^{\beta}f(\gamma(\varphi(\tau)))\cdot ||\tilde{\gamma}'(\tau)||\,d\tau\\
> > &=\int_{\alpha}^{\beta}f(\gamma(\varphi(\tau)))\cdot ||\gamma'(\varphi(\tau))\cdot \varphi'(\tau)||\,d\tau\\
> > &=\int_{\alpha}^{\beta}f(\gamma(\varphi(\tau)))\cdot ||\gamma'(\varphi(\tau))||\cdot |\varphi'(\tau)|\,d\tau\\
> > &=\int_{a}^{b}f(\gamma(t))\cdot ||\gamma'(t)||\,dt={\dots} &&\end{flalign}$$ 
<div class="page-break" style="page-break-before: always;"></div>

# Integrali curvilinei di seconda specie
### Campo vettoriale
> [!definizione]
> Si chiama campo vettoriale su un insieme $E\subset \mathbb{R}^{n}$ una mappa $F:E\to \mathbb{R}^{n}$, $F(\underline{x})=(F_{1}(\underline{x}),\dots,F_{n}(\underline{x}))$

### Forma differenziale
> [!definizione]
> $F:E\to \mathbb{R}^{n}$ campo vettoriale
> Si chiama forma differenziale su $E$ l'espressione formale
> $\omega=F_{1}dx_{1}+{\dots+F_{n}dx_{n}}=\sum_{i=1}^{n}F_{i}dx_{i}=\langle F,d\underline{x}\rangle$
> Una forma differenziale $\omega$ su $E$ si dice di classe $\mathrm{C}^{0}$ (o $\mathrm{C}^{1}$) se $F_{i}\in \mathrm{C}^{0}(E)\;\;\forall i\in \{ 1,\dots,n \}$ (o $F_{i}\in \mathrm{C}^{1}(E)$)

> [!definizione]
> $\gamma:[a,b]\to E\subset \mathbb{R}^{n}$, $\gamma \in \mathrm{C}^{1}([a,b])$, $\omega=\langle F,d\underline{x}\rangle$, $\omega \in \mathrm{C}^{0}(E)$
> Si definisce integrale curvilineo di seconda specie di $\omega$ lungo $\gamma$
> $$\begin{flalign}\int_{\gamma}\omega:=\int_{a}^{b}\langle F(\gamma(t)),\gamma'(t)\rangle\,dt=\int_{a}^{b}\sum_{i=1}^{n}F_{i}(\gamma(t))\cdot\gamma_{i}'(t)\,dt &&\end{flalign}$$
> Se $\gamma$ è chiusa si indica anche con $\oint_{\gamma}\omega$
