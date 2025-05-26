# Divergenza
> [!definizione]
> $F:E\subset \mathbb{R}^{n}\to \mathbb{R}^{n}$ campo vettoriale, $F\in \mathrm{C}^{1}(E)$
> $$\begin{flalign}\mathrm{div}(F)(\underline{x}):=\sum_{i=1}^{n} \frac{\partial F_{i}}{\partial x_{i}}(\underline{x}) &&\end{flalign}$$
> si dice divergenza di $F$

# Rotore
> [!definizione]
> $E\subset \mathbb{R}^{3}$ aperto, $F:E\to \mathbb{R}^{3}$ campo vettoriale, $F\in \mathrm{C}^{1}(E)$
> $$\begin{flalign}\mathrm{rot}(F)(x,y,z)&=\det \begin{bmatrix}
\hat{e_{1}} & \hat{e_{2}} & \hat{e_{3}} \\
\partial_{x} & \partial_{y} & \partial_{z} \\
F_{1} & F_{2} & F_{3}
\end{bmatrix} \\
&=\left( \frac{\partial F_{3}}{\partial y}-\frac{\partial F_{2}}{\partial z}, \frac{\partial F_{1}}{\partial z}-\frac{\partial F_{3}}{\partial x}, \frac{\partial F_{2}}{\partial x}-\frac{\partial F_{1}}{\partial y} \right)(x,y,z) &&\end{flalign}$$
> si dice rotore di $F$

> [!teorema]
> $E\subset \mathbb{R}^{3}$ aperto, $F:E\to \mathbb{R}^{3}$ campo vettoriale, $F\in \mathrm{C}^{1}(E)$, $\omega=\langle F,d\underline{x}\rangle$
> $F$ è chiusa su $E\iff \mathrm{rot}(F)(x,y,z)=\underline{0}\;\;\forall(x,y,z)\in E$
> > [!dimostrazione]-
> > Segue direttamente dalla definizione di forma differenziale chiusa e di rotore