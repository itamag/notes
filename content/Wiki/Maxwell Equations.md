>[!def] Maxwell's Equations
>$$\begin{array}{r l}{\nabla\cdot\mathbf{E}}&{={4\pi \rho}}\\ {\nabla\cdot\mathbf{B}}&{=0}\\ {\nabla\times\mathbf{E}}&{=-\frac{1}{c}{\cfrac{\partial\mathbf{B}}{\partial t}}}\\ {\nabla\times\mathbf{B}}&{=\mathbf{\frac{4\pi}{c}J}+\frac{1}{c}{\cfrac{\partial\mathbf{E}}{\partial t}}}\end{array}$$
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



# Maxwell's Dynamic Equations
>[!note]
>Maxwell's general equations are first-order homogenous vector differential equations. The coupling of the vector components of the EM fields is rather annoying, so usually we go about by expressing the fields as potential-derivatives, then solving second-order uncoupled equations:
>$$\nabla \cdot \mathbf{B} = 0 \implies \mathbf{B} = \nabla \times \mathbf{A}$$
>$$\implies 0 = \nabla \times \mathbf{E} + \frac{1}{c} \frac{ \partial \mathbf{B} }{ \partial t } = \nabla \times \left( \mathbf{E}+ \frac{1}{c}\frac{ \partial \mathbf{A} }{ \partial t } \right) \implies \mathbf{E} + \frac{1}{c}\frac{ \partial \mathbf{A} }{ \partial t } = -\nabla \psi $$

## Turning Maxwell's Equations into Potential Wave Equations

To solve the equations, we again see that the off-diagonal equations still allow us to replace the first-order problem with a second order, as we define: $$\mathbf{E} = -\nabla \phi_{E} - \frac{1}{c}\frac{ \partial \mathbf{A} }{ \partial t } ;\;\;\;\mathbf{B} = \nabla \times \mathbf{A}$$
Which yields *the dynamical potential equations*:

>[!thm] Maxwell Equations - Potential Form
> $$\begin{gather}
> \nabla^2\varphi + \frac{1}{c}\frac{ \partial  }{ \partial t } (\nabla \cdot \mathbf{A}) = -4\pi \rho\\
> \nabla^2\mathbf{A} - \frac{1}{c}\frac{ \partial^2 \mathbf{A} }{ \partial t^2 } - \nabla\left(\nabla \cdot \mathbf{A} + \frac{1}{c}\frac{ \partial \varphi }{ \partial t } \right) = -\frac{4\pi}{c} \mathbf{J}
> \end{gather}$$
> The potentials are not unique, so we can choose them to make these equations more pleasant. In *Lorentz gauge*:
> $$\nabla \cdot \mathbf{A} + \frac{1}{c}\frac{ \partial \varphi }{ \partial t } =0 \implies \begin{bmatrix}
> \nabla^2\varphi - \frac{1}{c^2}\frac{ \partial ^2\varphi }{ \partial t^2 } = -4\pi \rho \\
> \nabla^2\mathbf{A} - \frac{1}{c^2}\frac{ \partial ^2\mathbf{A} }{ \partial t^2 } = -\frac{4\pi}{c}\mathbf{J}
> \end{bmatrix} \iff \partial_{\nu}F^{\nu \mu} = \frac{4\pi}{c}J^\mu$$
> In *Colon gauge*:
> $$\nabla \cdot \mathbf{A}=0 \implies \begin{bmatrix}
> \nabla^2\varphi = -4\pi \rho \\
> \nabla^2 \mathbf{A} - \frac{1}{c}\frac{ \partial ^2\mathbf{A} }{ \partial t^2 }  = -\frac{4\pi}{c}\left( \underbrace{ \mathbf{J}-\frac{1}{4\pi}\nabla \frac{ \partial \varphi }{ \partial t } }_{ \mathbf{J}_{\text{transverse}} }  \right)
> \end{bmatrix}$$
> [[Covariant Formulation of EM#^e46cdb]] 
> [[Covariant Formulation of EM#^75e5b1]] 


## Solving the Wave Equations using Green's Functions

*In both gauges, we see that the potentials are determined by independent inhomogeneous wave equations*. Now's a good time to find a [[Green's Function]] for such equations. We get *two possible Green's functions*:
![[Green's Function#^011885]] 

Basically, we get the same Green's functions as [[Poisson Equation#^d8bb11]], but now at each point in space, the potential will be a superposition of the charge distributions at different moments in time. *Obviously if we expect causality, i.e. the potential at a point is affected by the past charge distribution and not the future one, we will use $G^{+}$*.

## Retarded Time
So generally we have a causality relation: an observer at $\mathbf{r},t$ will be affected by an event at $\mathbf{r'},t'$ traveling at the speed of light if: $$\lVert \mathbf{r-r'} \rVert = c(t-t') $$
Given a choice of $\mathbf{r'}$, a solution $t'$ to the above equation will be called the retarded time $t_{R}$. Intuitively, a test charge at point $\mathbf{r}, t$ will feel the effect of the charge at $\mathbf{r'}$ at time $t_{R}(\mathbf{r'})$. *When we have a function $f(\mathbf{r'},t')$ and we want to compute it at the retarded time $t'=t_{R}$, it is commonplace to denote*:
$$[f]_{\mathbf{r},t}(\mathbf{r'}) = f(\mathbf{r'}, t_{R}) \equiv f\left( \mathbf{r'},t -\frac{\lVert\mathbf{r'-r}\rVert}{c}  \right)$$
*Essentially, the brackets parameterize a function $f(\mathbf{r'},t')$ of the sender frame in the mixed frame $\mathbf{r'},\mathbf{r},t$ derived from $\mathbf{r'},t'(\mathbf{r'};\mathbf{r},t)$*. So we have two parameters $\mathbf{r},t$ which denote the observer location, and $[f]$ is a function only of space $\mathbf{r'}$.

Alternatively, we can fix a time $t'$ in the equation and then ask: what are the solutions $\mathbf{r'}$? These are the points in space where an event at $t'$ contributes to an observer at $\mathbf{r},t$

# Conservation Laws
>[!thm] Charge Conservation is a Consequence of Maxwell's Equation:
>Indeed, local charge conservation can be derived from the differential equations:
>$$\begin{align}
0  & = \nabla \cdot(\nabla \times \mathbf{B}) = \nabla \cdot\left( \frac{4\pi}{c}\mathbf{J}+\frac{1}{c} \frac{ \partial \mathbf{E} }{ \partial t } \right) \\
 & \implies \nabla \cdot \mathbf{J} + \partial_{t}\rho = 0
\end{align}$$ 
> And then the global conservation by integration:
> $$\dot{Q} = \frac{d}{dt}\int d^3\mathbf{r'}\rho(\mathbf{r'},t) = -\int d^3\mathbf{r'}\nabla \cdot \mathbf{J} = 0$$

^9ec328
