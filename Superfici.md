# Curva di Jordan
> [!definizione]
> Una curva di Jordan è una curva piana semplice e chiusa

> [!teorema]
> $\gamma:[a,b]\to \mathbb{R}^{2}$ curva di Jordan $\implies$
> - $\Gamma=\gamma([a,b])$ divide il piano in due insiemi aperti di cui uno è limitato $D_{\mathrm{int}}$ chiamato interno e uno illimitato $D_{\mathrm{ext}}$ chiamato esterno, entrambi aperti
> - $\partial D_{\mathrm{int}}=\partial D_{\mathrm{ext}}=\Gamma$

> [!definizione]
> Si chiama chiusura di $D$ l'insieme $\bar{D}=D\cup \partial D$

# Superficie
> [!definizione]
> Un sottoinsieme $S\subset \mathbb{R}^{3}$ si dice superficie se $\exists\sigma:\bar{D}\subset \mathbb{R}^{2}\to \mathbb{R}^{3}$ mappa detta parametrizzazione di $S$, $\sigma(u,v)=(\sigma_{1}(u,v),\sigma_{2}(u,v),\sigma_{3}(u,v))=(x(u,v),y(u,v),z(u,v))$ verificante:
> - $D$ è un aperto di $\mathbb{R}^{2}$, interno di una curva di Jordan
> - $\sigma$ è continua e iniettiva
> - $\sigma(\bar{D})=S$
> 
> $S$ si dice superficie cartesiana se $\exists\sigma:\bar{D}\subset \mathbb{R}^{2}\to \mathbb{R}^{3}$ parametrizzazione di uno dei seguenti tipi, con $f:\bar{D}\to \mathbb{R}$, $f\in \mathrm{C}^{1}(\bar{D})$:
> - $\sigma(u,v)=(u,v,f(u,v))$
> - $\sigma(u,v)=(u,f(u,v),v)$
> - $\sigma(u,v)=(f(u,v),u,v)$
<div class="page-break" style="page-break-before: always;"></div>

# Punti interni e bordo intrinseci
> [!definizione]
> $S\subset \mathbb{R}^{3}$ superficie elementare: $\partial S=S$ e $\mathring{S}=\emptyset$
> Un punto $\underline{p_{0}}\in S$ si dice interno a $S$ se esistono $\mathrm{B}(\underline{p_{0}},r_{0})$ e $\sigma_{*}:\bar{D}_{*}\subset \mathbb{R}^{2}\to \mathbb{R}^{3}$ parametrizzazione di $\overline{\mathrm{B}(\underline{p_{0}},r_{0})\cap S}$ tale che $\underline{p_{0}}\in\sigma_{*}(D_{*})$
> L'insieme dei punti interni di $S$ si denota con $S'$
> Si chiama bordo di $S$ l'insieme dei punti che non sono interni $\mathrm{bor(S)}=S\setminus S'$

# Regolarità della parametrizzazione e piano tangente
> [!definizione]
> $S\subset \mathbb{R}^{3}$ superficie parametrizzata da $\sigma:\bar{D}\to \mathbb{R}^{3}$ di classe $\mathrm{C}^{1}$, $\underline{p_{0}}=\sigma(u_{0},v_{0})\;\;(u_{0},v_{0})\in D$
> Se $\gamma:[a,b]\to D$ di classe $\mathrm{C}^{1}$, $\gamma'(t_{0})\neq \underline{0}$, $\tilde{\gamma}=\sigma\circ \gamma$ è la corrispondente curva sulla superficie ed è di classe $\mathrm{C^{1}}$
> Se $\tilde{\gamma}'(t_{0})\neq \underline{0}$ e la retta tangente a $\tilde{\gamma}$ passante per $\tilde{\gamma}(t_{0})$ appartiene a $\pi$ allora $\exists \pi$ piano tangente a $S$ in $\underline{p_{0}}$
> Si vuole imporre $\tilde{\gamma}'(t_{0})=u'(t_{0})\cdot\sigma_{u}(u_{0},v_{0})+v'(t_{0})\cdot\sigma_{v}(u_{0},v_{0})\neq \underline{0}$
> $\pi:\{ \underline{p_{0}}+\lambda\sigma_{u}(u_{0},v_{0})+\mu\sigma_{v}(u_{0},v_{0}):\lambda,\mu \in \mathbb{R} \}$ è il piano di equazione cartesiana $a(x-x_{0})+b(y-y_{0})+c(z-z_{0})=0$ con $(a,b,c):=\sigma_{u}(u_{0},v_{0})\times\sigma_{v}(u_{0},v_{0})\neq \underline{0}$ e $\underline{p_{0}}=(x_{0},y_{0},z_{0})$
> 
> $\underline{p_{0}}\in S'$ si dice regolare se esistono $\mathrm{B}(\underline{p_{0}},r_{0})$ e $\sigma:\bar{D}\to \mathbb{R}^{3}$ parametrizzazione di $\overline{\mathrm{B}(\underline{p_{0}},r_{0})\cap S}$ tale che
> - $\sigma$ è di classe $\mathrm{C}^{1}$
> - $\sigma_{u}(u_{0},v_{0})\times\sigma_{v}(u_{0},v_{0})\neq \underline{0}$
> 
> $\pi$ si chiama piano tangente a $S$ in $\underline{p_{0}}$
> I due versori normali a $\pi$ sono $$\begin{flalign} \pm\frac{\sigma_{u}(u_{0},v_{0})\times\sigma_{v}(u_{0},v_{0})}{||\sigma_{u}(u_{0},v_{0})\times\sigma_{v}(u_{0},v_{0})||} &&\end{flalign}$$
> $S$ si dice regolare se tutti i punti interni sono regolari
<div class="page-break" style="page-break-before: always;"></div>

# Area di una superficie
> [!definizione]
> $S\subset \mathbb{R}^{3}$ superficie regolare, $\sigma:\bar{D}\subset \mathbb{R}^{2}\to \mathbb{R}^{3}$ sua parametrizzazione di classe $\mathrm{C}^{1}$
> $Q=[u_{0},u_{0}+du]\times[vo,v_{0}+dv]$ è l'elemento infinitesimo di area
> Se $(u,v)\to(u_{0},v_{0})$, $\sigma(u,v)=\sigma(u_{0},v_{0})+J_{\sigma}(u_{0},v_{0})\cdot(u-u_{0},v-v_{0})^{T}+o(||(u-u_{0},v-v_{0})||)$
> $\tilde{Q}:=\{ \sigma(u_{0},v_{0})+\lambda\sigma_{u}(u_{0},v_{0})+\mu\sigma_{v}(u_{0},v_{0}):0\leq\lambda\leq du\land0\leq \mu\leq dv \}=\sigma(Q)$
> $\mathrm{area}(\tilde{Q})=||\sigma_{u}(u_{0},vo)\times\sigma_{v}(u_{0},v_{0})||\,du\,dv=dS$
> Si chiama area di $S$ se $||\sigma_{u}(u_{0},vo)\times\sigma_{v}(u_{0},v_{0})||$ è limitata $\forall(u,v)\in D$ e quindi è ben definita
> $$\begin{flalign}\mathrm{area}(S):=\iint_{S}dS=\iint_{D}||\sigma_{u}(u_{0},vo)\times\sigma_{v}(u_{0},v_{0})||\,du\,dv &&\end{flalign}$$

> [!osservazione]-
> $D\subset \mathbb{R}^{2}$ interno di una curva di Jordan, $f\in \mathrm{C}\mathrm{0}(\bar{D})$, $f\in \mathrm{C}^{1}(D)$, $\sigma:D\to \mathbb{R}^{3}$ superficie cartesiana parametrizzazione di $S\subset \mathbb{R}^{3}$
> $$\begin{flalign}\mathrm{area}(S)=\iint_{D}\sqrt{1+||\nabla f(u,v)||^{2}}\,du\,dv &&\end{flalign}$$

# Integrale di superficie
> [!definizione]
> $S\subset \mathbb{R}^{3}$ superficie regolare parametrizzata da $\sigma:\bar{D}\to \mathbb{R}^{3}$ tale che $D$ è misurabile e $||\sigma_{u}(u_{0},vo)\times\sigma_{v}(u_{0},v_{0})||$ è limitata, $f:S'\to \mathbb{R}$ continua e limitata
> $$\begin{flalign}\iint_{S}f\,dS=\iint_{D}f\cdot||\sigma_{u}(u_{0},vo)\times\sigma_{v}(u_{0},v_{0})||\,du\,dv &&\end{flalign}$$
> si chiama integrale di superficie di $f$ su $S$
