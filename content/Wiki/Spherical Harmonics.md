
>[!thm] Summation theorem for spherical harmonics
>$$P_{l}\left(\hat{\boldsymbol{r}}\cdot\hat{\boldsymbol{r}}^{\prime}\right)={\frac{4\pi}{2l+1}}\sum_{m=-l}^{+l}Y_{l m}^{*}\left(\underbrace{\theta^{\prime},\phi^{\prime}}_{\Omega^{\prime}}\right)Y_{l m}\left(\underbrace{\theta,\phi}_{\Omega}\right)$$
>Where the $P_l$ are the [[Legendre Polynomials]]

^a38af4

## Spherical Harmonics

### Premise and Context  
Spherical harmonics $Y_\ell^m(\theta, \phi)$ are a complete, orthonormal set of functions defined on the surface of a sphere $S^2$. They frequently arise in problems exhibiting spherical symmetry in **electromagnetism** and **quantum mechanics**.

Mathematically, they are solutions to the angular part of Laplace's equation in spherical coordinates.

---

> [!thm] **Definition: Spherical Harmonics**  
> Spherical harmonics are eigenfunctions of the angular part of the Laplace operator,  
> $$
> \nabla^2 Y_\ell^m(\theta, \phi) = -\frac{\ell(\ell+1)}{r^2} Y_\ell^m(\theta, \phi),
> $$  
> where $\ell = 0, 1, 2, \dots$ and $m = -\ell, \dots, \ell$.

- **Coordinates**: $\theta$ (polar angle), $\phi$ (azimuthal angle).  
- **Quantum numbers**:  
  - $\ell$ (degree): Total angular momentum quantum number.  
  - $m$ (order): Magnetic quantum number.

---

### Key Properties  

> [!thm] **Orthogonality**  
> Spherical harmonics satisfy the orthogonality condition:  
> $$
> \int_0^{2\pi} \int_0^\pi Y_\ell^{m}(\theta, \phi) \, Y_{\ell'}^{m'*}(\theta, \phi) \sin \theta \, d\theta \, d\phi = \delta_{\ell \ell'} \delta_{m m'}.
> $$  

- **Normalization**:  
  $$
  \int_{S^2} |Y_\ell^m|^2 \, d\Omega = 1,
  $$  
  where $d\Omega = \sin\theta \, d\theta \, d\phi$ is the solid angle element.

> [!thm] **Completeness**  
> Any well-behaved function $f(\theta, \phi)$ on $S^2$ can be expanded as:  
> $$
> f(\theta, \phi) = \sum_{\ell=0}^\infty \sum_{m=-\ell}^\ell a_\ell^m Y_\ell^m(\theta, \phi),
> $$  
> where $a_\ell^m$ are expansion coefficients.

---

### Applications in Analytical Electromagnetism  

1. **Laplace’s Equation in Spherical Coordinates**  
   In electrostatics, the scalar potential $\Phi(r, \theta, \phi)$ for systems with spherical symmetry can be expanded as:  
   $$
   \Phi(r, \theta, \phi) = \sum_{\ell=0}^\infty \sum_{m=-\ell}^\ell \left[ A_\ell^m r^\ell + B_\ell^m r^{-(\ell+1)} \right] Y_\ell^m(\theta, \phi).
   $$  

2. **Multipole Expansion**  
   Spherical harmonics provide the natural basis for the multipole expansion of electromagnetic potentials, useful for approximating fields at large distances.

3. **Radiation Problems**  
   Solutions to wave equations (e.g., in antenna theory) often use spherical harmonics to separate variables.

---

### Applications in Quantum Mechanics  

1. **Angular Momentum Eigenstates**  
   Spherical harmonics $Y_\ell^m$ are the eigenfunctions of the squared angular momentum operator $\hat{L}^2$ and its $z$-component $\hat{L}_z$:  
   $$
   \hat{L}^2 Y_\ell^m = \hbar^2 \ell(\ell+1) Y_\ell^m, \quad \hat{L}_z Y_\ell^m = \hbar m Y_\ell^m.
   $$  
   Quantum numbers $\ell$ and $m$ correspond to total angular momentum and its projection onto the $z$-axis.

2. **Hydrogen Atom Solutions**  
   The angular part of the hydrogen atom wavefunctions is described by spherical harmonics. Solutions to the Schrödinger equation in spherical coordinates factorize as:  
   $$
   \psi_{n\ell m}(r, \theta, \phi) = R_{n\ell}(r) Y_\ell^m(\theta, \phi),
   $$  
   where $R_{n\ell}(r)$ is the radial solution.

---

### Summary Table  

| Property                | Expression/Condition                             | Notes                                   |
|-------------------------|-------------------------------------------------|----------------------------------------|
| Orthogonality           | $\int_{S^2} Y_\ell^m Y_{\ell'}^{m'*} d\Omega$    | $\delta_{\ell \ell'} \delta_{m m'}$     |
| Completeness            | $f(\theta, \phi) = \sum a_\ell^m Y_\ell^m$       | Basis for $L^2(S^2)$ functions          |
| Laplace’s Equation      | $\nabla^2 Y_\ell^m = -\frac{\ell(\ell+1)}{r^2} Y_\ell^m$ | Separation of variables in EM          |
| Angular Momentum Eigenstates | $\hat{L}^2, \hat{L}_z$ eigenfunctions        | Key in quantum mechanics               |

---

### Links to Related Notes  
- **Separation of Variables**: [[Separation of Variables in PDEs]]  
- **Multipole Expansion**: [[Multipole Expansion in EM]]  
- **Quantum Angular Momentum**: [[Quantum Angular Momentum Operators]]  
- **Hydrogen Atom Solution**: [[Hydrogen Atom in Quantum Mechanics]]  



# Tricks

>[!thm] Total integral of spherical harmonic
>$$
>\int Y_{lm}d\Omega = \int Y_{lm}\cdot_{1} d\Omega = \int Y_{lm}Y_{00} \sqrt{ 4\pi }d\Omega = \sqrt{ 4\pi } \delta_{l_{0}}\delta_{m_{0}}
>$$

^f07ea6

