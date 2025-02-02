# Macroscopic Equations in Non-Statics
We'll extend the static macroscopic equations above to the case where $\mathbf{D,H}$ (and hence $P,M$ or $\rho_{b},\mathbf{J}_{b}$) can change in time. *Minimally, we'd require conservation of total charge and conservation of bound charge to be consequences of the equation.* This turns out to be enough, as we get:
$$\begin{bmatrix}
\;\;\;\;\;\;\nabla \cdot \mathbf{D} = 4\pi \rho_{f} & \nabla \times \mathbf{E} + \frac{1}{c}\frac{ \partial \mathbf{B} }{ \partial t }  = 0 \\
\nabla \cdot \mathbf{B} = 0 & \;\;\;\;\;\;\;\nabla \times \mathbf{H} = \frac{4\pi}{c}\mathbf{J}_{f} + \frac{1}{c}\frac{ \partial \mathbf{D} }{ \partial t } 
\end{bmatrix}
$$
And:
$$\begin{bmatrix}
\rho_{\text{tot}} = \rho_{b} + \underbrace{ (-\nabla \cdot \mathbf{P}) }_{ \rho_{f} } \\
\mathbf{J}_{\text{tot}} = \mathbf{J}_{f} + \underbrace{ c \nabla \times \mathbf{M} }_{ \mathbf{J}_{M} } + \frac{ \partial \mathbf{P} }{ \partial t } 
\end{bmatrix}$$
In the total current in the dynamic case, we add a current that may arise from polarization change.

