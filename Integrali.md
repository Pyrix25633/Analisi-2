# Integrale doppio su un rettangolo
> [!definizione]
> $f:A\subset \mathbb{R}^{2}\to \mathbb{R}$, $A=[a,b]\times[c,d]$, $f$ limitata (e non negativa)
> Il trapezoide sotteso al grafico di $f$ in $A$ è l'insieme dei punti
> $T_{f}(A):=\{ (x,y,z)\in \mathbb{R}^{3}:0\leq z\leq f(x,y)\land(x,y)\in A \}$

### Suddivisione
> [!definizione]
> Si chiama suddivisione di $[a,b]$ un insieme finito $\{ x_{0},x_{1},\dots,x_{m} \}:a=x_{0}<x_{1}<{\dots}<x_{m}=b$ 
> Si chiama suddivisione di $A$ l'insieme $\mathcal{D}:=\mathcal{D}_{1}\times\mathcal{D}_{2}=\{ x_{0},\dots,x_{m} \}\times \{ y_{0},\dots,y_{n} \}=\{ (x_{i},y_{j}):i=0,\dots,m\land j=0,\dots,n \}$
> $A$ resta suddiviso in $n\times m$ rettangoli $A_{ij}:=[x_{i-1},x_{i}]\times[y_{j-1},y_{j}]$ di area $\mathrm{area}(A_{ij})=(x_{i}-x_{i-1})\cdot(y_{j}-y_{j-1})$

### Somma superiore e inferiore
> [!definizione]
> $$\begin{flalign}&M_{ij}:=\mathrm{sup}_{A_{ij}}\{ f \}\\
> &m_{ij}:=\mathrm{inf}_{A_{ij}}\{ f \}&&\end{flalign}$$
> Si chiamano somma superiore e inferiore
> $$\begin{flalign}&S(f,\mathcal{D}):=\sum_{i=1}^{m} \sum_{j=1}^{n} M_{ij}\cdot \mathrm{area}(A_{ij})\\
&s(f,\mathcal{D}):=\sum_{i=1}^{m} \sum_{j=1}^{n} m_{ij}\cdot \mathrm{area}(A_{ij})&&\end{flalign}$$
> Proprietà:
> - Se $f\geq0$, $M_{ij}\cdot \mathrm{area}(A_{ij})$ e $m_{ij}\cdot \mathrm{area}(A_{ij})$ rappresentano il volume di un parallelepipedo che approssima il grafico per eccesso e per difetto
> - $\mathrm{area}(A_{ij})\cdot \mathrm{inf}_{A_{ij}}\{ f \}\leq s(f,\mathcal{D})\leq S(f,\mathcal{D})\leq \mathrm{area}(A_{ij})\cdot \mathrm{sup}_{A_{ij}}\{ f \}$
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
> $$\begin{flalign}\mathrm{inf}_{A}\{ f \}\leq \frac{1}{\mathrm{area}(A)}\iint_{A}f=z_{0}\leq \mathrm{sup}_{A}\{ f \} &&\end{flalign}$$
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

> [!teorema]
> $g:[a,b]\to \mathbb{R}$ integrabile
> $\implies G_{g}:=\{ (x,g(x)):x \in[a,b] \}\subset \mathbb{R}^{2}$ è misurabile e $|G_{g}|_{2}=0$

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

> [!approfondimento]- Rotazione del sistema di riferimento
> In alcuni casi potrebbe essere utile ruotare il sistema di riferimento per rendere semplice un dominio, come nel caso di un rettangolo ruotato che andrebbe altrimenti diviso in $3$ o in $2$ se quadrato
> Quindi scegliamo due nuovi assi $u$ e $v$ in modo che
> $y=mx+u$ e $y=-\frac{x}{m}+v$
> Ovvero $u=y-mx$ e $u=y+\frac{x}{m}$
> Con alcuni calcoli si ottiene
> $$\begin{flalign}\psi(u,v)=\left( \frac{m^{2}v+u}{1+m^{2}},m \frac{v-u}{1+m^{2}} \right) &&\end{flalign}$$
> Il fattore di trasformazione è il valore assoluto del determinante
> $$\begin{flalign}\det(J_{\psi}(u,v))=\frac{m}{1+m^{2}} &&\end{flalign}$$

# Integrale triplo su un parallelepipedo
### Suddivisione
> [!definizione]
> $A=[a_{1},b_{1}]\times[a_{2},b_{2}]\times[a_{3},b_{3}]\subset \mathbb{R}^{3}$
> $\mathcal{D}_{1}:=\{ a_{1}=x_{0}\leq{\dots}\leq x_{i}\leq{\dots}\leq x_{m}=b_{1} \}$ suddivisione di $[a_{1},b_{1}]$
> $\mathcal{D}_{2}:=\{ a_{2}=y_{0}\leq{\dots}\leq y_{j}\leq{\dots}\leq y_{n}=b_{2} \}$ suddivisione di $[a_{2},b_{2}]$
> $\mathcal{D}_{3}:=\{ a_{3}=z_{0}\leq{\dots}\leq z_{k}\leq{\dots}\leq z_{p}=b_{3} \}$ suddivisione di $[a_{3},b_{3}]$
> $\mathcal{D}=\mathcal{D}_{1}\times\mathcal{D}_{2}\times\mathcal{D}_{3}$ si chiama suddivisione di $A$
> $A$ risulta diviso in $m\times n\times p$ parallelepipedi $A_{ijk}=[x_{i-1},x_{i}]\times[y_{j-1},y_{j}]\times[z_{k-1},z_{k}]$ di volume $\mathrm{vol}(A_{ijk})=|A_{ijk}|_{3}=(x_{i}-x_{i-1})\cdot(y_{j}-y_{j-1})\cdot(z_{k}-z_{k-1})$
> ($i=1,\dots,m$, $j=1,\dots,n$, $k=1,\dots,p$)

### Somma superiore e inferiore
> [!definizione]
> $$\begin{flalign}&M_{ijk}:=\mathrm{sup}_{A_{ijk}}\{ f \}\\
> &m_{ijk}:=\mathrm{inf}_{A_{ijk}}\{ f \}&&\end{flalign}$$
> Si chiamano somma superiore e inferiore
> $$\begin{flalign}&S(f,\mathcal{D}):=\sum_{i=1}^{m} \sum_{j=1}^{n}\sum_{k=1}^{p} M_{ijk}\cdot \mathrm{vol}(A_{ijk})\\
&s(f,\mathcal{D}):=\sum_{i=1}^{m} \sum_{j=1}^{n}\sum_{k=1}^{p} m_{ijk}\cdot \mathrm{vol}(A_{ijk})&&\end{flalign}$$

# Funzione integrabile secondo Riemann
> [!definizione]
> Se $\mathrm{sup}\{ s(f,\mathcal{D}) \}=\mathrm{inf}\{ S(f,\mathcal{D}) \}=L\in \mathbb{R}\implies f\in\mathcal{R}(A)$ e si denota
> $$\begin{flalign}L=\iiint_{A}f &&\end{flalign}$$

> [!teorema] Teoremi
> ### Esistenza dell'integrale
> $f\in \mathrm{C}^{0}(A)\implies f\in\mathcal{R}(A)$
> 
> ### Linearità
> $\iiint_{A}(\alpha f+\beta g)=\alpha \iiint_{A}f+\beta \iiint_{A}g$
> 
> ### Monotonia
$g\leq f\implies \iiint_{A}g\leq \iiint_{A}f$
> 
> ### Valore assoluto
> $|\iiint_{A}f|\leq \iiint_{A} |f|$

> [!teorema] Teorema della media integrale
> $f:A\subset \mathbb{R}^{3}\to \mathbb{R}$, $f\in\mathcal{R}(A)$
> $$\begin{flalign}\mathrm{inf}_{A}\{ f \}\leq \frac{1}{\mathrm{vol}(A)}\iint_{A}f=w_{0}\leq \mathrm{sup}_{A}\{ f \} &&\end{flalign}$$
> Inoltre se $f\in \mathrm{C}^{0}(A)\implies \exists \underline{p_{0}}:f(\underline{p_{0}})=w_{0}$

# Formule di riduzione sui rettangoli
> [!formule]
> $A=[a_{1},b_{1}]\times[a_{2},b_{2}]\times[a_{3},b_{3}]$, $f\in \mathrm{C}^{0}(A)$
> 
> > [!note]-
>> **Cosa sto facendo quando calcolo un integrale triplo?**
>> Riportiamoci in due variabili, l'idea è di calcolare una somma di aree per ottenere un volume
>  > In questo caso io quando calcolo l'integrale sto integrando sempre per fili perché sia se integro per $x$ o per $y$ io sto calcolando nel primo integrale un'area rispetto ad un filo per $x$ o $y$ e poi attraverso il secondo calcolo le aree rispetto ad un filo per l'altra variabile ed in questo modo ottengo il volume sotteso grafico della funzione
> > ---
> > In tre variabili invece l'idea è che calcolo una somma di volumi rispetto ad altezze diverse, perciò in questo caso io posso scegliere se integrare prima per il filo e poi per la superficie e viceversa, ovvero integro 3 volte per fili. 
> 
> ### Riduzione per fili
> $\forall z\in[a_{3},b_{3}]\;\;(x,y)\in[a_{1},b_{1}]\times[a_{2},b_{2}]\to \int_{a_{3}}^{b_{3}}f(x,y,z)\,dz$ è integrabile su $[a_{1},b_{1}]\times[a_{2},b_{2}]$ e
> $$\begin{flalign}\iiint_{A}f=\iint_{[a_{1},b_{1}]\times[a_{2},b_{2}]}\left( \int_{a_{3}}^{b_{3}}f(x,y,z)\,dz \right)\,dx\,dy &&\end{flalign}$$
> Analogamente per $x$ e $y$
> 
> > [!note]-
> > Effettuando prima l'integrazione per il filo noi stiamo calcolando un'area rispetto ad un filo di una delle variabili ($x,y,z$) e poi quest'area la andiamo a calcolare rispetto ad una superficie (le altre 2 variabili rimanenti), ovvero sommiamo l'area per ogni punto della superficie, se pensiamo alla superficie come un'insieme di fili noi stiamo calcolando un numero di volumi pari alla lunghezza del terzo filo
> > La somma di questi volumi è il risultato dell'integrale
>
> ### Riduzione per strati
> $\forall(x,y)\in[a_{1},b_{1}]\times[a_{2},b_{2}]\;\;z\in[a_{3},b_{3}]\to \iint_{[a_{1},b_{1}]\times[a_{2},b_{2}]}f(x,y,z)\,dx\,dz$ è integrabile su $[a_{3},b_{3}]$ e
> $$\begin{flalign}\iiint_{A}f=\int_{a_{3}}^{b_{3}}\left(\iint_{[a_{1},b_{1}]\times[a_{2},b_{2}]}f(x,y,z)\,dx\,dy\right)\,dz &&\end{flalign}$$
> Analogamente per $x$ e $y$
> 
>>[!note]-
> > Effettuando prima l'integrazione per la superficie noi stiamo calcolando direttamente un volume, ovvero abbiamo calcolato un integrale doppio, un integrale calcolato per fili 2 volte
> > Poi come ultimo integrale abbiamo un'altra integrazione per fili del volume ottenuto rispetto a 2 variabili ed infine come in precedenza andiamo a sommare il volume per ogni punto del filo ovvero rispetto all'ultima variabile
> > Come prima il risultato è una somma di volumi per ogni punto del filo che corrisponde al risultato dell'integrale triplo
>

# Integrale triplo su un insieme generale
> [!definizione]
> Se $A\subset \mathbb{R}^{3}$ è limitato ma non parallelepipedo è possibile definire una nuova funzione
> $A\subset Q=[a_{1},b_{1}]\times[a_{2},b_{2}]\times[a_{3},b_{3}]$, $\tilde{f}:Q\to \mathbb{R}$
> $$\begin{flalign}\tilde{f}(x,y,z)=\begin{cases}
f(x,y,z),&(x,y,z)\in A \\
0,&(x,y,z)\in Q\setminus A
\end{cases} &&\end{flalign}$$
> Di conseguenza $\tilde{f}\in\mathcal{R}(Q)\implies f\in\mathcal{R}(A)$ e
> $$\begin{flalign}\iiint_{A}f=\iiint_{Q}\tilde{f} &&\end{flalign}$$

# Insieme misurabile
> [!definizione]
> $A\subset \mathbb{R}^{3}$ limitato, $f:A\to \mathbb{R}$, $f(x,y,z):=1$ se $(x,y,z)\in A$
> $A$ si dice misurabile secondo Peano-Jordan se $f\in\mathcal{R}(A)$ e $\mathrm{vol}(A)=|A|_{3}=\iiint_{A}f$

> [!teorema]
> $A\subset \mathbb{R}^{3}$ limitato
> $A$ è misurabile $\iff \partial A$ è misurabile e $|\partial A|_{3}=0$

> [!teorema]
> $E\subset \mathbb{R}^{2}$ limitato e misurabile, $g\in\mathcal{R}(E)$
> $\implies G_{g}:=\{ (x,y,g(x,y)):(x,y) \in E \}\subset \mathbb{R}^{3}$ è misurabile e $|G_{g}|_{3}=0$

# Integrale triplo su un insieme misurabile
> [!teorema]
> $f:A\to \mathbb{R}$, $f\in \mathrm{C}^{0}(A)$ limitata, $A\subset \mathbb{R}^{3}$ limitato e misurabile
> $\implies f\in\mathcal{R}(A)$

> [!teorema]
> $A\subset \mathbb{R}^{3}$ limitato e misurabile, $A=B\cup C$ misurabili, $|C|_{}=0$, $f\in\mathcal{R}(A)$
> $$\begin{flalign}\implies \iiint_{A}f=\iiint_{B}f &&\end{flalign}$$

# Integrale triplo su un dominio semplice e formula di riduzione
> [!definizione]
> $A\subset \mathbb{R}^{3}$ si dice semplice o normale rispetto all'asse $z$ se
> - $\exists g_{1},g_{2}\in \mathrm{C}^{0}(E):g_{1}\leq g_{2}$ su $E\in \mathbb{R}^{2}$
> - $A=\{ (x,y,z)\in \mathbb{R}^{3}:(x,y)\in E\land g_{1}(x,y)\leq z\leq g_{2}(x,y) \}$
> 
> Analogamente rispetto agli assi $x$ e $y$
> Un dominio semplice è limitato e misurabile

> [!formule]
> $A\subset \mathbb{R}^{3}$ semplice rispetto a $z$, $f\in \mathrm{C}^{0}(A)\implies f\in\mathcal{R}(A)$ e
> $$\begin{flalign}\iiint_{A}f=\iint_{E}\left(\int_{g_{1}(x,y)}^{g_{2}(x,y)}f(x,y,z)\,dz\right)\,dy\,dx &&\end{flalign}$$
> Analogamente per $x$ e $y$

> [!teorema]
> $A\subset \mathbb{R}^{3}$ limitato e misurabile, $A=A\cap(\mathbb{R}\times \mathbb{R}\times[a,b])$
> $A_{z}:=\{ (x,y)\in \mathbb{R}^{2}:(x,y,z)\in A \}$ misurabile, $f\in \mathrm{C}^{0}(A)\implies f\in\mathcal{R}(A)$ e
> $$\begin{flalign}\iiint_{A}f=\int_{a}^{b}\left(\iint_{A_{z}}f(x,y,z)\,dx\,dy\right)\,dz &&\end{flalign}$$

> [!approfondimento]- Applicazione della riduzione per strati al volume di un solido per rotazione
> $A=\{ (x,y,z)\in \mathbb{R}^{3}:z\in[a,b]\land x^{2}+y^{2}\leq g(z)^{2} \}$, $g\in \mathrm{C}^{0}([a,b])$, $g(z)\geq0\;\;\forall z\in[a,b]$
> $A$ può essere visto come la rotazione di $F=\{ (y,z)\in \mathbb{R}^{2}:z\in[a,b]\land0\leq y\leq g(z) \}$ (o analogamente per $x$)
> $A_{z}=\{ (x,y)\in \mathbb{R}^{2}:x^{2}+y^{2}\leq g(z)^{2} \}$ è uno strato, più nello specifico un cerchio di area $\mathrm{area}(A_{z})=|A_{z}|_{2}=\pi\cdot g(z)^{2}$ e
> $$\begin{flalign}|A|_{3}&=\iiint_{A}1=\int_{a}^{b}\left(\iint_{A_{z}}1\,dx\,dy\right)\,dz=\int_{a}^{b}\mathrm{area}(A_{z})\,dz=\pi \int_{a}^{b}g(z)^{2}\,dz &&\end{flalign}$$
