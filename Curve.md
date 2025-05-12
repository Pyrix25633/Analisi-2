# Curva in $\mathbb{R}^{n}$
> [!definizione]
> Si chiama curva una mappa $\gamma:I\to \mathbb{R}^{n}$ continua, $\gamma(t):=(\gamma_{1}(t),\dots,\gamma_{n}(t))$, $I$ intervallo di $\mathbb{R}$, $\gamma_{i}(t):I\to \mathbb{R}$ ($i=1,..,n$)
> Se $I=[a,b]$, $\gamma(a)$ e $\gamma(b)$ si chiamano estremi della curva
> L'insieme $\gamma(I)\subset \mathbb{R}^{n}$ si chiama sostegno o supporto della curva
> $\underline{x}=(x_{1},\dots,x_{n})=\gamma(t)$ si chiama equazione parametrica o anche legge oraria della curva
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
> $\gamma:I\to \mathbb{R}^{n},\tilde{\gamma}:\tilde{I}\to \mathbb{R}^{n}$ di classe $\mathrm{C}^{1}$ si dicono equivalenti se $\exists \varphi:\tilde{I}\to I$ biiettiva tale che $\varphi \in \mathrm{C}^{1}(\tilde{I})$, $\varphi'(\tau)\neq0$ e $\tilde{\gamma}=\gamma(\varphi(\tau))\;\;\forall \tau \in \tilde{I}$
> $\tau \in \tilde{I}\to t=\varphi(\tau)\in I$ si dice cambiamento di parametrizzazione

> [!osservazione]-
> Se $\varphi(\tau)>0\;\;\forall \tau \in \tilde{I}$ allora $\gamma$ e $\tilde{\gamma}$ hanno lo stesso verso, altrimenti se $\varphi(\tau)<0\;\;\forall \tau \in \tilde{I}$ hanno verso opposto
