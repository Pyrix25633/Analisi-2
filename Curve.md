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
> Se almeno una componente $\gamma_{i}$ è iniettiva $\implies \gamma$ è iniettiva

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
> $\gamma$ si dice **regolare** se $\gamma \in \mathrm{C}^{1}(I)$ e $\gamma'(t)\neq \underline{0}\;\;\forall t \in I$
> Si chiama versore o direzione tangente a $\gamma$ il campo vettore
> $$\begin{flalign}T_{\gamma}(t):=\frac{\gamma'(t)}{||\gamma'(t)||} &&\end{flalign}$$
> $\gamma:[a,b]\to \mathbb{R}^{n}$ si dice $\mathrm{C}^{1}$ a tratti se $\exists \{ a=t_{0}<{\dots}<t_{k}=b \}$ suddivisione di $[a,b]$ tale che $\gamma_{j}=\gamma|_{[t_{j-1},t_{j}]}:[t_{j-1},t_{j}]\to \mathbb{R}^{n}$ è di classe $\mathrm{C}^{1}$ e $\gamma=\bigcup_{j=1}^{k}\gamma_{j}$

# Cambiamento di parametro
> [!definizione]
> $\gamma:I\to \mathbb{R}^{n},\tilde{\gamma}:\tilde{I}\to \mathbb{R}^{n}$ di classe $\mathrm{C}^{1}$ si dicono equivalenti se $\exists \varphi:\tilde{I}\to I$ biiettiva tale che $\varphi \in \mathrm{C}^{1}(\tilde{I})$, $\varphi'(\tau)\neq0$ e $\tilde{\gamma}(\tau)=\gamma(\varphi(\tau))\;\;\forall \tau \in \tilde{I}$
> $\tau \in \tilde{I}\to t=\varphi(\tau)\in I$ si dice cambiamento di parametrizzazione
> Inoltre $\Gamma=\gamma(I)=\tilde{\gamma}(\tilde{I})$

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
> $\omega:=F_{1}dx_{1}+{\dots}+F_{n}dx_{n}=\sum_{i=1}^{n}F_{i}dx_{i}=\langle F,d\underline{x}\rangle$
> Una forma differenziale $\omega$ su $E$ si dice di classe $\mathrm{C}^{0}$ (o $\mathrm{C}^{1}$) se $F_{i}\in \mathrm{C}^{0}(E)\;\;\forall i\in \{ 1,\dots,n \}$ (o $F_{i}\in \mathrm{C}^{1}(E)$)

> [!definizione]
> $\gamma:[a,b]\to E\subset \mathbb{R}^{n}$, $\gamma \in \mathrm{C}^{1}([a,b])$, $\omega=\langle F,d\underline{x}\rangle$, $\omega \in \mathrm{C}^{0}(E)$
> Si definisce integrale curvilineo di seconda specie di $\omega$ lungo $\gamma$
> $$\begin{flalign}\int_{\gamma}\omega:=\int_{a}^{b}\langle F(\gamma(t)),\gamma'(t)\rangle\,dt=\int_{a}^{b}\sum_{i=1}^{n}F_{i}(\gamma(t))\cdot\gamma_{i}'(t)\,dt &&\end{flalign}$$
> Se $\gamma$ è chiusa si indica anche con $\oint_{\gamma}\omega$

> [!teorema]
> $E\subset \mathbb{R}^{n}$, $\gamma:[a,b]\to E,\tilde{\gamma}:[\alpha,\beta]\to E$ curve di classe $\mathrm{C}^{1}$ equivalenti, $\tilde{\gamma}=\gamma \circ\varphi$
> - $\varphi(\tau)>0\;\;\forall \tau \in[\alpha,\beta]\implies \int_{\gamma}\omega=\int_{\tilde{\gamma}}\omega$
> - $\varphi(\tau)<0\;\;\forall \tau \in[\alpha,\beta]\implies \int_{\gamma}\omega=-\int_{\tilde{\gamma}}\omega$
> 
> > [!dimostrazione]-
> > $\varphi:[\alpha,\beta]\to[a,b]$ cambiamento di parametrizzazione, $\tilde{\gamma}'=\gamma'(\varphi(\tau))\cdot \varphi'(\tau)$
> > $$\begin{flalign}{\dots}&=\int_{\alpha}^{\beta}\langle F(\tilde{\gamma}(\tau)),\tilde{\gamma}'(\tau)\rangle\,d\tau=\int_{\alpha}^{\beta}\langle F(\gamma(\varphi(\tau))),\gamma'(\varphi(\tau))\cdot \varphi(\tau)\rangle\,d\tau\\
> > &=\int_{\alpha}^{\beta}\langle F(\gamma(\varphi(\tau))),\gamma'(\varphi(\tau))\rangle \cdot \varphi'(\tau)\,d\tau=\int_{\varphi(\alpha)}^{\varphi(\beta)}\langle F(\gamma(t)),\gamma'(t)\rangle\,dt={\dots} &&\end{flalign}$$
<div class="page-break" style="page-break-before: always;"></div>

> [!teorema]
> $\gamma:[a,b]\to E\subset \mathbb{R}^{n}$ curva regolare, $F:E\to \mathbb{R}^{n}$ campo vettoriale su $E$ di classe $\mathrm{C}^{0}$, $\omega=\langle F,d\underline{x}\rangle$ forma differenziale
> $$\begin{flalign}\implies \int_{\gamma}\omega=\int_{\gamma}\langle F,T_{\gamma}\rangle\,ds &&\end{flalign}$$
> > [!dimostrazione]-
> > $$\begin{flalign}{\dots}=\int_{a}^{b}\langle F(\gamma(t)),\gamma'(t)\rangle\,dt=\int_{a}^{b}\langle F(\gamma(t)),T_{\gamma}(t)\rangle\cdot ||\gamma'(t)||\,dt={\dots} &&\end{flalign}$$

> [!osservazione]-
> $\gamma:[a,b]\to E\subset \mathbb{R}^{n}$ regolare e semplice, $\omega=\langle F, d\underline{x}\rangle$ forma differenziale si classe $\mathrm{C}^{0}(E)$
> $\implies \int_{\gamma}\omega=\int_{\gamma}\langle F,T_{\gamma}\rangle\,ds$

# Forme differenziali esatte
> [!definizione]
> $E\subset \mathbb{R}^{n}$ aperto, $U\in \mathrm{C}^{1}(E)$, $F:E\to \mathbb{R}^{n}$, $\omega=\langle F,d\underline{x}\rangle$
> $dU=\langle \nabla U,d\underline{x}\rangle=\frac{\partial U}{\partial x_{1}}dx_{1}+{\dots}+\frac{\partial U}{\partial x_{n}}dx_{n}$ viene chiamata forma differenziale di $U$
> $\omega$ si dice esatta se $\exists U:\nabla U(\underline{x})=F(\underline{x})\;\;\forall \underline{x}\in E$, equivalentemente $dU=\omega$ e $U$ è detta **funzione potenziale** di $\omega$ (o anche di $F$) in $E$

> [!teorema]
> $E\subset \mathbb{R}^{n}$ aperto, $\omega$ forma differenziale continua ed esatta su $E$, $\gamma:[a,b]\to E$ $\mathrm{C}^{1}$ a tratti, $U$ qualunque potenziale di $\omega$
> $\implies \int_{\gamma}\omega=U(\gamma(b))-U(\gamma(a))$
> > [!dimostrazione]-
> > Per ipotesi $\exists U$ potenziale di $\omega$ su $E$ tale che $\nabla U(\underline{x})=F(\underline{x})$
> > $\frac{d}{dt}(U(\gamma(t)))=\langle \nabla U(\gamma(t)),\gamma'(t)\rangle=\langle F(\gamma(t)),\gamma'(t)\rangle\;\;\forall t\in[a,b]$
> > $$\begin{flalign}{\dots}=\int_{a}^{b}\langle F(\gamma(t)),\gamma'(t)\rangle\,dt=\int_{a}^{b} \frac{d}{dt}(U(\gamma(t)))\,dt=[U(\gamma(t))]_{a}^{b}={\dots} &&\end{flalign}$$
<div class="page-break" style="page-break-before: always;"></div>

> [!osservazione]-
> $\gamma$ curva chiusa $\implies \oint_{\gamma}\omega=0$

# Forme differenziali chiuse
> [!definizione]
> $E\subset \mathbb{R}^{n}$ aperto, $\omega=\langle F,d\underline{x}\rangle$, $F:E\to \mathbb{R}^{n}$, $F(\underline{x})=(F_{1}(\underline{x}),\dots,F_{n}(\underline{x}))$, $F_{i}\in \mathrm{C}^{1}(E)$ ($i=1,\dots,n$)
> $\omega$ si dice chiusa in $E$ se
> $$\begin{flalign} \frac{\partial F_{i}}{\partial x_{j}}(\underline{x})=\frac{\partial F_{j}}{\partial x_{i}}(\underline{x})\;\;\forall \underline{x}\in E,\;i,j\in \{ 1,\dots,n \} &&\end{flalign}$$

> [!teorema]
> $\omega \in \mathrm{C}^{1}(E)$
> $\omega$ esatta su $E\implies \omega$ chiusa su $E$
> > [!dimostrazione]-
> > Per ipotesi $\exists U$ potenziale e $\frac{\partial U}{\partial x_{i}}=F_{i}(\underline{x})$ ($i=1,\dots,n$)
> > Essendo $U\in \mathrm{C}^{2}(E)$
> > $$\begin{flalign}{\dots}=\frac{\partial^{2}U}{\partial x_{j}\partial x_{i}}(\underline{x})=\frac{\partial^{2}U}{\partial x_{i}\partial x_{j}}(\underline{x})={\dots} &&\end{flalign}$$

> [!osservazione]-
> $\omega$ non chiusa in $E\implies$ $\omega$ non esatta in $E$

> [!teorema]
> $E\subset \mathbb{R}^{n}$ aperto e convesso, ovvero
> $[\underline{p},\underline{q}]:=\{ t\underline{p}+(1-t)\underline{q}:0\leq t\leq_{1} \}\subset E\;\;\forall\underline{p},\underline{q}\in E$
> $\omega \in \mathrm{C}^{1}(E)$
> $\omega$ esatta in $E\iff \omega$ chiusa in $E$
<div class="page-break" style="page-break-before: always;"></div>

# Costruzione di un potenziale
> [!formule] Formula
> $E\subset \mathbb{R}^{n}$ convesso, $F:E\to \mathbb{R}^{n}$ campo vettoriale, $\omega=\langle F,d\underline{x}\rangle$ forma differenziale chiusa, allora è esatta ed esiste una funzione potenziale $U:E\to \mathbb{R}$ di $\omega$, $U\in \mathrm{C}^{2}(E):\nabla U(\underline{x})=F(\underline{x})$
> Procedura, con ordine delle variabili interscambiabile:
> $U(\underline{x})=\int F_{1}(\underline{x})\,dx_{1}=U_{1}(\underline{x})+C_{1}(x_{2},\dots,x_{n})$
> $$\begin{flalign} \frac{\partial U}{\partial x_{2}}(\underline{x})=\frac{\partial U_{1}}{\partial x_{2}}(\underline{x})+\frac{\partial C_{1}}{\partial x_{2}}(x_{2},\dots,x_{n})=F_{2}(\underline{x}) &&\end{flalign}$$
> $$\begin{flalign}\frac{\partial C_{1}}{\partial x_{2}}(x_{2},\dots,x_{n})=F_{2}(\underline{x})-\frac{\partial U_{1}}{\partial x_{2}}(\underline{x}) &&\end{flalign}$$
> che è costante rispetto ad $x_{1}$
> > [!dimostrazione]-
> > $$\begin{flalign} \frac{ \partial F_{2} }{ \partial x_{1} } (\underline{x})-\frac{ \partial^{2}U_{1} }{ \partial x_{1}\partial x_{2} }(\underline{x}) =\frac{ \partial F_{2} }{ \partial x_{1} } (\underline{x})-\frac{ \partial^{2}U_{1} }{ \partial x_{2}\partial x_{1} }(\underline{x})=\frac{ \partial F_{2} }{ \partial x_{1} } (\underline{x})-\frac{ \partial F_{1} }{ \partial x_{2} } (\underline{x})=0  &&\end{flalign}$$
> 
> $$\begin{flalign}C_{1}(x_{2},\dots,x_{n})=\int \frac{ \partial C_{1} }{ \partial x_{2} }(x_{2},\dots x_{n})\,dx_{2} =U_{2}(x_{2},\dots,x_{n})+C_{2}(x_{3},\dots,x_{n}) &&\end{flalign}$$
> Iterando: $U(\underline{x})=U_{1}(\underline{x})+U_{2}(x_{2},\dots ,x_{n})+{\dots}+U_{n}(x_{n})+c$
