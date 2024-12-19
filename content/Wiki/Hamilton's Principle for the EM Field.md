# Working Out the Action
>[!thm] The Action of the EM field
>$$
>\begin{aligned}
 S  & = S_{\text{matter}} + S_{\text{int}} + S_{\text{field}} \\
\end{aligned}
>$$
>$$
>S_{\text{matter}} = -\sum_{i}m_{i}c\int ds_{i}
>$$
>$$
>S_{\text{int}} = -\sum_{i}\frac{q_{i}}{c}\int A_{\mu}dx^\mu \sim -\frac{1}{c}\int A_{\mu}J^\mu d\Omega \implies \mathcal{L}_{\text{int}} = -\frac{1}{c}A_{\mu}J^\mu
>$$

Assumptions for finding $S_\text{field}$:
1. Scalar: This action should also be a Lorentz scalar
2. Superposition: if we have solutions ${} F^{\mu \nu}_{i} {}$ for $J^\mu_{i}$, then the solution for $\sum J_{i}$ is $\sum F_{i}$
	1. This means that our differential equations, which are derived from the variation $\delta S_{f}$, should be linear. So we'd expect $S_{f}$ to be quadratic in $J_{i}$.

Conclusion: in [[Special Relativity#Minkowski Spacetime|Minkowski spacetime]], the only scalar that holds these assumptions is the norm of the $\sum F_{i}$ (the [[The Electromagnetic Field Tensor]]).

>[!claim] [[The Electromagnetic Field Tensor]] Action (CGS)
>$$
>S_{f} \equiv - \frac{1}{16\pi c}\int F_{\mu \nu}F^{\mu \nu}d\Omega = \frac{1}{8\pi}\int(E^2-B^2)dVdt \implies \mathcal{L}_{f} = \frac{1}{8\pi}(E^2-B^2)
>$$


>[!remark] Separability of the total Lagrangian
>We see that the interaction Lagrangian is dependent on the field vector $A_{\mu}$, and the field Lagrangian is dependent on its derivatives $\partial_{\nu}A^\mu$


# Deriving [[Maxwell Equations]] through the Action

The Lagrangian is a function of the tangent space. In our formulation, to solution is a vector $A^\mu(t, \vec{r})$. And indeed we see that the Lagrangian is separable:
$$
\mathcal{L} = \mathcal{L}_{\text{matter}} + \mathcal{L}_{\text{int}}(A_{\mu}) + \mathcal{L}_{f}(\partial_{\nu}A_{\mu})
$$
We get:
$$
\frac{ \partial \mathcal{L} }{ \partial A_{\mu} } = \partial_{\nu}\frac{ \partial \mathcal{L} }{ \partial (\partial_{\nu}A_{\mu}) } \iff \frac{ \partial \mathcal{L}_{\text{int}} }{ \partial A_{\mu} } = \partial_{\nu}\frac{ \partial \mathcal{L}_{f} }{ \partial (\partial_{\nu}A_{\mu}) } \iff -\frac{1}{c}J^\mu  = -\frac{1}{4\pi}\partial_{\nu} F^{\nu \mu} 
$$
`\begin{proof}`
![[Pasted image 20241204134338.png]]
`\end{proof}`

Finally if we write explicitly in order of indices:
$$
\vec{\nabla} \cdot \vec{E} = 4\pi \rho; \;\; \vec{\nabla}\times \vec{B} = \frac{1}{c}\frac{ \partial \vec{E} }{ \partial t } + \frac{4\pi}{c}\vec{J}
$$
And by integrating we reconstruct the empirical forms of Maxwell's equations

## Charge Conservation:

$$
\partial_{\mu}\partial_{\nu}F^{\mu \nu} = -\frac{1}{c}\partial_{\mu}J^\mu
$$

The LHS is a product of antisymmetric and symmetric tensors and so it's zero due to 
[[Tensor Analysis#^1fff98]] 

# Summary

> [!thm] Lagrangian density of relativistic EM field
>$$\begin{aligned}
 {\mathcal{L}}&={\mathcal{L}}_{m a t t e r}-{\frac{1}{c}}A_{\mu}J^{\mu}-{\frac{1}{16\pi}}F^{\mu\nu}F_{\mu\nu} \\
 & = {\mathcal{L}}_{m a t t e r}  - \left( \rho - \frac{1}{c}\mathbf{J}\cdot \mathbf{A} \right)- \frac{1}{8\pi}(E^2 - B^2)
\end{aligned}$$
>[[The Electromagnetic Field Tensor]]

^d5e94f

>[!thm] Canonical momentum of the EM field
>$$\pi^{\mu} \equiv\frac{\partial\mathcal{L}}{\partial\left(\frac{\partial A_{\mu}}{\partial t}\right)}=\frac{1}{4\pi c}\left(0,\mathbf{E}\right)$$ 


> [!thm] Hamiltonian density of the relativistic EM field
> $$\begin{aligned}
> {\mathcal{H}} & =\frac{\partial{\mathcal{L}}}{\partial\left(\partial_{0}A_{\mu}\right)}\partial_{0}A_{\mu}-{\mathcal{L}} \\
>  & ={\frac{1}{8\pi}}\left(E^{2}+B^{2}\right)\;\;\;\;\;-{\frac{1}{c}}{\boldsymbol{J}}\cdot{\boldsymbol{A}}\;\;\;\;+\;\;\;{\frac{1}{4\pi}}{\boldsymbol{\nabla}}\cdot\left[\varphi{\boldsymbol{E}}\right]
> \end{aligned}$$
> The last term will cancel out when integrating the density due to [[Tensor Analysis#^fd1ddd]] 

^93d106


