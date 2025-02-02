>[!thm] Poisson Equation
>$$\nabla^2\psi = f$$
>If $f \equiv 0$ then the equation will be called Laplace's equation

The solutions to this equation are unique, if we are given boundary conditions - information about the potential on the boundary.

>[!thm] Uniqueness of Solution to Poisson Equation
>Given boundary conditions, the solution to the Poisson equation is unique. There are two types:
>1. Dirichlet: $psi$ is given on $\partial V$
>2. Neumann: $\nabla \psi \cdot \mathbf{\hat{n}} = \frac{ \partial \psi }{ \partial n }$ is given on $\partial V$ where $\hat{n}$ is a vector field giving the outward pointing orthogonal vector to each point of the boundary surface.
>Remark: one can't specify both Dirichlet and Neumann conditions for a function, and then "advance" the solution in space, as in the case of ODEs where $y(t=0)$ and $\dot{y}(t=0)$ is given.


>[!thm] The Mean-Value Theorem:
>In a simply connected region, the value of a harmonic function $\psi(\mathbf{r})$ is the mean over a sphere of arbitrary radius:
>$$\psi(\mathbf{r}) = \frac{1}{|S|}\int_{S}\psi(\mathbf{r'})d^3\mathbf{r'}$$
>$$u(x)={\frac{1}{n\omega_{n}r^{n-1}}}\int_{\partial B(x,r)}u\,d\sigma={\frac{1}{\omega_{n}r^{n}}}\int_{B(x,r)}u\,d V$$
>In particular, $\psi$ will not have an extremum.

^8564a7

# Formal Solution to Poisson Eq. Using Green's Function

A direct approach to solving the equation would be to use a [[Green's Function]]:

>[!thm] Green's Function of Poisson Equation
>$$G(\mathbf{r'}, \mathbf{r}) = \frac{1}{ \lvert \mathbf{r'}-\mathbf{r} \rvert } + F(\mathbf{r'}, \mathbf{r}) \;\;\;\; [\nabla^2F = 0]$$

^d8bb11

By using [[Tensor Analysis#^8e7ef6]], we find:
$$\varphi\left({\boldsymbol{r}}\right)=\int_{V}{\frac{\rho\left({\boldsymbol{r}^{\prime}}\right)}{R}}d^{3}{\boldsymbol{r}}^{\prime}\quad+{\frac{1}{4\pi}}\int_{S}\left[{\frac{1}{R}}{\frac{\partial\varphi}{\partial{\boldsymbol{n}}^{\prime}}}-\varphi{\frac{\partial}{\partial{\boldsymbol{n}}^{\prime}}}\left({\frac{1}{R}}\right)\right]d a^{\prime}$$
This tells us something important! To directly solve the boundary condition problem, we must simultaneously know both the Neumann and Dirichlet boundary conditions. However, this can't be done (no proof supplied).

So, we must find a more general Green's function. By repeating the above derivation with $G$ instead of a literal expression we get:
$$\varphi\left({\boldsymbol{r}}\right)=\int_{V}{\rho\left({\boldsymbol{r}}^{\prime}\right)G\left({\boldsymbol{r}},{\boldsymbol{r}}^{\prime}\right)d^{3}r^{\prime}}+{\frac{1}{4\pi}}\int_{S}\left[\underbrace{G\left({\boldsymbol{r}},{\boldsymbol{r}}^{\prime}\right){\frac{\partial\varphi}{\partial{\boldsymbol{n}}^{\prime}}}}_{\text{Neumann-Compatible}}-\underbrace{\varphi{\frac{\partial G\left({\boldsymbol{r}},{\boldsymbol{r}}^{\prime}\right)}{\partial{\boldsymbol{n}}^{\prime}}}}_{\text{Dirichlet-Compatible}}\right]d a^{\prime}$$
And so to only have one of the underbraced terms, we'd require:
$$\mathbf{r'} \in S \implies G_{D}\left(r,r^{\prime}\right)=0$$
$$\mathbf{r'}\in S \implies \frac{\partial G_{N}\left(r,r^{\prime}\right)}{\partial n^{\prime}}=-\,\frac{4\pi}{\lvert S \rvert }$$
**The upshot is that these Green's functions only depend on the geometry of the problem, i.e. what is the volume of space where we want to solve Poisson's equation.**

# Formal Solution to Poisson Eq. in Spherical Harmonics
Again we'd like to solve using a [[Green's Function]], i.e. a function $G$ having: $$\nabla_{\mathbf{r}}^2G(\mathbf{r},\mathbf{r'}) = -4\pi\delta(\mathbf{r-r'})$$

But this time, *instead of solving directly - we'll (1) define a function space of solutions (2) find a nice basis for this function space (3) express our solution as a vector in that function space*. In that sense, whereas we started with a PDE, Green's method turned it into an integration problem, and this approach aims to replace the integration problem with a coupled equations problems for the coefficients

We know:
>[!thm] Delta Function Expansion in Spherical Harmonics
>$$\delta(\mathbf{r-r'}) = \sum_{l=0}^{\infty}\sum_{m=-l}^{l}\frac{\delta(r-r')}{r^{2}}Y^*_{l m}(\theta^{\prime},\phi')Y_{l m}(\theta,\phi)$$
>Indeed for any test function $f(\mathbf{r})$: 
>$$\begin{align}
\int \delta(\mathbf{r-r'})f(\mathbf{r'})d^3\mathbf{r'} & =\int\sum_{l=0}^{\infty} \sum_{m=-l}^{l}\frac{\delta(r-r')}{r^{2}}Y^*_{l m}(\theta^{\prime},\phi')Y_{l m}(\theta,\phi)f(r',\theta',\phi')d^3\mathbf{r'} \\
 & = \sum_{l=0}^\infty \sum_{m=-l}^l Y_{lm}(\theta,\phi)\int Y^*_{l m}(\theta^{\prime},\phi')f(r,\theta',\phi')d\Omega' \\
 & =f(r,\theta,\phi) = f(\mathbf{r})
\end{align}$$

And hence *we can expand $G$* over the solid harmonics basis. Then, solving Poisson's equation for Green's function amount to finding the coefficients. We will have two solutions for the radial coefficients - one for $r<r'$ and another for $r>r'$. Indeed, $\nabla^2G$ is a delta function and hence $G$ is not smooth and can't have a single expansion.

Alas, finding the coefficients isn't easy. Ron did it for several special cases of boundary conditions seen here: פונקצית גרין בנוכחות כדור מוליך ברדיוס [🔖](zotero://open-pdf/library/items/KF4V7K2P?page=3&annotation=XMIWPMD5)

# Physics

1. Due to [[#^8564a7]] , an electrostatic potential cannot have an extremum in a region without charges, and this implies that you cannot fix a charged particle in a region of space with vacuum.
2. 