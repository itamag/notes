“קירוב WKB ותורת ההפרעות )בלתי תלויה בזמן(” ([pdf](zotero://open-pdf/library/items/Q7PEVZSQ?page=1&annotation=8PUYCYFD))
The WKB (Semiclassical) Approximation [🔖](zotero://open-pdf/library/items/PMLKPKUE?page=124&annotation=7GLBWN53)


Useful mostly in 1D so we'll focus on that case. It provides an approximate solution to [[Schordinger's Equation]] when the potential is slowly varying w.r.t the "wavelength":
$$\lambda\left(x\right)=\frac{\hbar}{p\left(x\right)}\ll\frac{2\left[E-V\left(x\right)\right]}{\left|\mathrm{d}V/\mathrm{d}x\right|}$$
$$.p\left(x\right)\equiv\sqrt{2m\left[E-V\left(x\right)\right]}$$
Then we get an approximate eigenfunction:
>[!thm] WKB Eigenfunction in 1D
>$$\psi_{\pm}\left(x\right)\approx{\frac{1}{\sqrt{p\left(x\right)}}}\exp\left[\pm{\frac{i}{\hbar}}\int^{x}p\left(x\right)\mathrm{d}x\right] = \frac{1}{\sqrt{ k(x) }}\exp\left( \pm i\int^xk(x')dx'\right)$$

The idea behind this form: when there is a constant potential, then we get plane waves of the form $e^{ikx}$. When the potential is slowly-varying, we'll still get $e^{ik(x)x}$ but with a varying $k(x)$. 

The approximation is valid when both $p(x) \neq 0 \iff E \neq V(x)$ and $\psi(x_{0}) \neq 0$ (the approximated eigenfunction doesn't allow 0 values). The second term only happens at an infinite potential wall. These constraints lead to quantization in the allowed approximation eigenfunctions:

>[!thm] WKB Energy Quantization
>$$\int_{x_{1}}^{x_{2}}p(x)dx= \pi \hbar\begin{cases}
n - \frac{1}{2} &  \text{no walls}  \\
n- \frac{1}{4} & \text{1 wall} \\
n & \text{2 walls}
\end{cases}$$
$x_{1},x_{2}$ in the quantization formula are the boundaries of the potential wall, i.e. the points where $E=V(x)$ and in between $E<V(x)$.

In [[Quantum Tunneling]] problems, i.e. where the energy/Hamiltonian eigenvalue $E$ is smaller than the potential $V(x)$, we can use the theory to approximate the transmission coefficient:
$$T \approx \exp\left( -\frac{2}{\hbar}\int_{x_{1}}^{x_{2}}\lvert p(x) \rvert dx  \right)$$
**$T$ is the probability that a particle will pass the potential barrier**. 

>[!warning]
>In many problems using this theory, the potential is a Coloumb potential. Note however, that $V(x)$ here is a potential and has units of energy, whereas the electrostatic potential has units of energy per unit charge. So $V(x)$ would be $\frac{q}{r}\cdot q'$ .


>[!warning]
>The problems for this theory are shit. Sometimes shit classical explanations are handed out without any justification to magically produce whatever magic expression they want (see for example ([pdf](zotero://open-pdf/library/items/Q7PEVZSQ?page=4&annotation=KYEIBTA2))).


