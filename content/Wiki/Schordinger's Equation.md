
>[!theorem] **Time-dependent Schrödinger equation** (general)
>$$i\hbar\frac{d}{d t}|\Psi(t)\rangle=\hat{H}|\Psi(t)\rangle$$

# Exact Solutions

כמה פתרונות מדויקים למשוואת שרדינגר [🔖](zotero://open-pdf/library/items/Y56CQUPC?page=7&annotation=6GVNIPT2)
## Particle in a Box

# In Spherical Coordinates
![[Pasted image 20250127155239.png]]
([pdf](zotero://open-pdf/library/items/MBM3E435?page=5&annotation=VLGN4X4C))

When the potential is spherically-symmetric, we get by separation of variables a "free particle" equation for the angular variables and a radial equation with $V(r)$ for the radial dependence. The natural eigenbasis of a free Hamiltonian on the sphere are the spherical harmonics. Thus the solutions are of the form $u(r)Y_{lm}(\Omega)$, or in Hilbert space $\ket{\alpha lm}\equiv \ket{\alpha}\otimes \ket{lm}$, Where $\ket{\alpha}$ are the radial solutions / eigenbasis of the radial Hamiltonian. In other words, The potential allowed for separation of variables in a way that induced an isomoprhic structure on our Hilbert space as a product space $\mathcal{H}_{1} \otimes \mathcal{H}_{2}$, where the eigenbasis for $\mathcal{H}_{2}$ is simply the spherical harmonics (a general basis for functions on the sphere), and $\mathcal{H}_{1}$ is yet to be diagonalized, but generally can be spanned by the Bessel and Neumann functions (which take into account the boundary conditions of $r$ at $\infty$ and $0$). 

The free particle in spherical coordinates [[Schordinger's Equation#In Spherical Coordinates]]:
$$V=0\,,\quad E={\frac{\hbar^{2}k^{2}}{2m}}\,,\quad\psi(\mathbf{r})={\frac{u_{E\ell}(r)}{r}}Y_{\ell m}({\boldsymbol{\Omega}})$$
*Notice that the free particle solutions in spherical coordinates still have definite momentum, but only in magnitude*. 

## Take 2
If $V(\mathbf{r}) = V(r)$, then we can decompose the Hamiltonian into two parts $H = H_{r} + H_{\Omega}$ which commute. Thus, the Hilbert space our system $\mathcal{H}$ assumes the structure of a product space $\mathcal{H}_{r} \otimes \mathcal{H}_{\Omega}$ spanned by the basis $\ket{r}\otimes \ket{\theta,\phi}$. Further, $H_{\Omega}\propto L^2$. Thus, the eigenstates of $H$ will be $\ket{\alpha}\otimes \ket{lm}$ where $\ket{lm}$ are the Y_lm states, and $\ket{\alpha}$ are the eigenstates of $H_{r}$.

$$\nabla^2 = \frac{1}{r^2}\frac{ \partial ^2 }{ \partial r^2 } r - \frac{1}{\hbar^2r^2}L^2$$