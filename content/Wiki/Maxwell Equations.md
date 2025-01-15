>[!def] Maxwell's Equations
>$$\begin{array}{r l}{\nabla\cdot\mathbf{E}}&{={4\pi \rho}}\\ {\nabla\cdot\mathbf{B}}&{=0}\\ {\nabla\times\mathbf{E}}&{=-{\cfrac{\partial\mathbf{B}}{\partial t}}}\\ {\nabla\times\mathbf{B}}&{=\mathbf{\frac{4\pi}{c}J}+\frac{1}{c}{\cfrac{\partial\mathbf{E}}{\partial t}}}\end{array}$$
>The equations aren't independent - 8 equations for 6 field components. Noticing that  [[Tensor Analysis#^a2c75f]], we can see how the first two equations are derived from the (2/8) are derived from the latter 2 (6/8)

# Maxwell's Static Equations

When the fields are time-independent, we get:

>[!def] Maxwell's static equations and the [[Poisson Equation]]:
>$$\left\{\begin{array}{l l}{{\boldsymbol{\nabla\cdot E}=4\pi\rho}}\\ {{\boldsymbol{\nabla\times E}=0}}\end{array}\right.\qquad,\qquad\left\{\begin{array}{l l}{{\boldsymbol{\nabla\times B}=\frac{4\pi}{c}\boldsymbol{J}}}\\ {{\boldsymbol{\nabla\cdot B}=0}}\end{array}\right.$$
>These equations can be reduced to 4 scalar equations for the field potentials. This reduces the number of PDEs we need to solve - and instead we'll have to calculate derivatives:
>$$\begin{array}{l c r}{{\nabla^{2}\varphi=-4\pi\rho}}\\ {{\nabla^{2}A=-{\frac{4\pi}{c}}J}}\end{array}$$
>This is in the  [[Covariant Formulation of EM#^75e5b1|Colon gauge]] only. Generally we'd have to substract $\nabla(\nabla \cdot \mathbf{A})$ from the LHS.

^420f1c

There are several important consequences in this special case:

>[!remark] Properties of the Static Maxwell's Equations:
>1. The two fields are independent
>2. The field potential equations are inhomogeneous, so the solution isn't unique - we can add any homogeneous solution to the special one. For a unique solution - we must specify boundary conditions

Generally, we'll learn to solve the equations in three scenarios:
1. [[#Superposition Problems for Static Maxwell|Superposition problems]] - the charge and currents are given, so we just need to some individual contributions using Green's functions ^aa18a1
2. [[#Dirichlet Boundary Problems for Static Maxwell|Dirichlet boundary problems]] - the potential (any coordinate) is given on the boundary of a volume. For the electric field, a conductor is the major example of such problems.
3. [[#Neumann Boundary Problems for Static Maxwell|Neumann boundary problems]] - the potential derivative in the direction orthogonal to the volume surface. For electrostatic potentials this is the dot product of the electric field and the inwards facing surface normal.
## Superposition Problems for Static Maxwell
### Green's Function Approach

>[!quote]
>![[#^aa18a1]]

Only if we can safely claim the the solution vanishes at infinity! Then we can solve an integral problem instead, a-la [[Green's Function]]:

>[!thm] Integral Solution of Maxwell's Equations
>If we assume that the fields vanish at infinity (fast enough), we get for E:
>$$\varphi(\mathbf{r})=\int{\frac{\mathrm{d}q}{|\mathbf{r}-\mathbf{r}^{\prime}|}}=\int{\frac{\rho(\mathbf{r}^{\prime})\mathrm{d}^{3}r^{\prime}}{|\mathbf{r}-\mathbf{r}^{\prime}|}}$$
>$$\mathbf{E}(\mathbf{r})=-\nabla\varphi=\int{\frac{\rho(\mathbf{r}^{\prime}){\hat{\mathbf{e}}}_{\mathbf{r}-\mathbf{r}^{\prime}}\mathrm{d}^{3}r^{\prime}}{|\mathbf{r}-\mathbf{r}^{\prime}|^{2}}}=\int{\frac{\rho(\mathbf{r}^{\prime})(\mathbf{r}-\mathbf{r}^{\prime})\mathrm{d}^{3}r^{\prime}}{|\mathbf{r}-\mathbf{r}^{\prime}|^{3}}}$$
>If we further assume [[Covariant Formulation of EM#^75e5b1|Colon gauge]], by [[#^420f1c|the static potential equations]] we get the same results for B:
>$$\mathbf{A}(\mathbf{r})={\frac{1}{c}}\int{\frac{\mathbf{J}(\mathbf{r}^{\prime})d^{3}r^{\prime}}{|\mathbf{r}-\mathbf{r}^{\prime}|}}$$
>$$\mathbf{B}(\mathbf{r})=\nabla \times \mathbf{A} = {\frac{1}{c}}\int{\frac{\mathbf{J}(\mathbf{r}^{\prime})\times{\hat{\mathbf{e}}}_{\mathbf{r}-\mathbf{r}^{\prime}}\mathbf{d}^{3}r^{\prime}}{|\mathbf{r}-\mathbf{r}^{\prime}|^{2}}}$$
>([pdf](zotero://open-pdf/library/items/S8BHCP57?page=8&annotation=MZN4WAES)) 

Note that the same idea can be used to compute the total force at a point in space.

>[!exr] Calculating the energy of the EM field in superposition problems
>[[Hamilton's Principle for the EM Field#^93d106]] 
>
>Using integration by parts we can directly incorporate the charge density into the integral  ([pdf](zotero://open-pdf/library/items/S8BHCP57?page=12&annotation=DB9XPZCA)):
>$$
>\int_{V} \mathbf{X}^2dV = \int_{V}(-\mathbf{\nabla}\phi)\cdot \mathbf{X} dV = -\int_{\partial V}\phi \mathbf{X} \cdot d\mathbf{a}+ \int_{V} \phi(\nabla \cdot \mathbf{X})dV
>$$

### Using Symmetry
In some cases, the charge/current density field will be symmetrical under some transformation, that may change either/both the manifold or its tangent bundle. In these cases, the empirical versions of Maxwell's equations will be of most use:

>[!thm] Gauss Integral Law
>$$\nabla \cdot \mathbf{E} = 4\pi \rho \implies \textstyle\iint\mathbf{E}\cdot\,d\mathbf{a}=4\pi Q_{\mathrm{enc}}$$
^7d927f

>[!thm] Ampere Integral Law
>$$\nabla \times \mathbf{B} = \frac{4\pi}{c}\mathbf{J} \implies \oint\mathbf{B}\cdot\mathrm{d}{\boldsymbol{\ell}}={\frac{4\pi}{c}}I_{\mathrm{enc}}$$
^421105

### Multipole Expansion
[[Multipole Expansion]] can also be used to approximate a solution when the charge density is given to us.



## Boundary Condition Problems

>[!warning] 
>In [[Maxwell Equations#Superposition Problems for Static Maxwell]], we solved the equations for entire space, assuming the fields are vanishing at infinity. In other words, we solved the equations for a specific region of space and specific boundary conditions. But what if we have a different region or boundary conditions? Then we need the following


If we don't control the charge density, then we can't use superposition methods. In this case, for example in conducting metals, we will know the charge density or something equivalent, on the surface of the material

[[Poisson Equation#Formal Solution to Poisson Eq. Using Green's Function]]

### Dirichlet Boundary Problems for Static Maxwell
#### Solution to Static Maxwell's Equations for a Spherical Dirichlet Boundary

We notice from [[Poisson Equation#Formal Solution to Poisson Eq. Using Green's Function]] that in the case where we want to solve the the static Maxwell equations outside/inside a sphere with Dirichlet boundary conditions, then [[Green's Function]] is exactly the electrostatic potential of a [[Charge Particle with Grounded Conducting Sphere]], with $q=1$.  Thus we get:

>[!thm] Solution to Static Maxwell's Equations for a Spherical Dirichlet Boundary
$$G_{D}\left(r,r^{\prime}\right)=\frac{1}{\left[r^{2}+r^{\prime2}-2r r^{\prime}\cos\gamma\right]^{1/2}}-\frac{1}{\left[\left(\frac{r^{\prime}r}{a}\right)^{2}+a^{2}-2r r^{\prime}\cos\gamma\right]^{1/2}}$$
$$\varphi\left({\boldsymbol{r}}\right)=\int_{V}\rho\left({\boldsymbol{r}}^{\prime}\right)G_{D}\left({\boldsymbol{r}},{\boldsymbol{r}}^{\prime}\right)d^{3}r^{\prime}+{\frac{1}{2\pi}}\int_{S}\varphi\left(a,\theta^{\prime},\phi^{\prime}\right){\frac{a\left({\boldsymbol{r}}^{2}-a^{2}\right)}{\left({\boldsymbol{r}}^{2}+a^{2}-2a r\cos\gamma\right)^{3/2}}}d\Omega^{\prime}$$
Where $\rho$ is the charge density inside the region (not related to the boundary).

### Neumann Boundary Problems for Static Maxwell