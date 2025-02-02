# Local and Global Conservation of Charge
## From Maxwell Equations
![[Maxwell Equations#^9ec328]] 

## From Gauge Symmetry
See [[Hamilton's Principle for the EM Field#Charge Conservation]] and [[Covariant Formulation of EM#^e46cdb]] .

By the gauge invariance, we can use Hamilton's principle, knowing that both Hamiltonians (before and after a gauge transform) will be simultaneously extermized:

$$S=\int{\mathcal{L}}{\overset{d\Omega}{d^{3}r d t}}=-{\frac{1}{16\pi}}\int F_{\mu\nu}F^{\mu\nu}{\frac{d\Omega}{c}}-{\frac{1}{c}}\int A_{\mu}J^{\mu}{\frac{d\Omega}{c}}$$

$$\implies $$
![[Pasted image 20250201140209.png]]
Where $\delta \chi$ is a general gauge transformation and hence it must be that:
$$\partial_{\mu}J^\mu=0$$
ו[🔖](zotero://open-pdf/library/items/NS9XN6WX?page=49&annotation=D5LTUIRV)


# Local and Global Energy Conservation
## From [[Maxwell Equations]]
>[!warning]
>For some reason the above derivation assumes that particles do not leave the system

[[Energy Stored in EM Field#Energy of General EM Field]]
![[Energy Stored in EM Field#^fe4eac]] 

From [[Maxwell Equations#Maxwell's Dynamic Equations|Maxwell's equations]]:
$$\partial_{t}u + \mathbf{J\cdot E} = -\nabla \cdot\underbrace{ \left[ \frac{c}{4\pi}(\mathbf{E \times H}) \right] }_{ \mathbf{S} } \equiv -\nabla \cdot \mathbf{S}$$
This is a conservation equation stating: *the total energy stored in an electromagnetic system is the potential energy stored in the fields and the kinetic energy of the **free** charges producing the fields. When these quantities change in time, it is accounted by $S$*:
$$\frac{ \partial  }{ \partial t } (u+\mathcal{E}_{k}) + \nabla \cdot \mathbf{S} = 0,\;\;\;\;\;\;\;\left( \frac{d}{dt} \mathcal{E}_{k} = \mathbf{J\cdot E} \right)$$
The quantity $\mathbf{S}$ is the Poynting vector, aka the energy flux density aka the energy density current aka the energy current density (see [[Current and Flux]]).
By integration we get the total conservation:
$$\frac{d}{dt} [U + E_{k}] = -\int_{\partial\Theta} \underbrace{ \mathbf{S\cdot}d\mathbf{a} }_{ \text{Energy flux} }\stackrel{\Theta \to \mathbb{R}^3}{\to}0$$

# Conservation of Momentum
>[!warning]
>The treatment for conservation of charge will be only for the $\mathbf{E,B}$ fields and not $\mathbf{D,H}$ because there are delicate points about whether to account momenta to the bound or free charges

The momenta of charged particles will change due to Lorentz force when under the influence of an EM field. But where does this momentum go? It turns out that the EM field itself has momentum.

The Lorentz force density for a continuous charge distribution:
$${\dot{p}}_{m}=\rho E+{\frac{1}{c}}J\times B=f\left(r,t\right)$$
By substituting Maxwell's equations into this expression we get:
$$\begin{align}
\overbrace{\left(\rho E+\frac{1}{c}J\times B\right)}^{J(r,\tau)=\dot{p}_{m}}+ & \frac{1}{4\pi c}\frac{\partial}{\partial t}\left(E\times B\right)  = \\
 & =\frac{1}{4\pi}\left[E\left(\nabla\cdot E\right)+B\left(\nabla\cdot B\right)-E\times\left(\nabla\times E\right)-B\times\left(\nabla\times B\right)\right]
\end{align}$$

*On the LHS we have the time variation of two quantities with the units of momentum density. Therefore, it would make sense to define as the momentum of the EM field: $\frac{1}{4\pi c}\mathbf{E\times B}=\frac{1}{c^2}\mathbf{S}$*. And indeed we see that for each scalar equation (we have 3 above), the RHS is a gradient:
$$E\left(\nabla\cdot E\right)-E\times\left(\nabla\times E\right)=\sum_{i}{\frac{\partial}{\partial x_{i}}}\left(E_{i}E_{j}-{\frac{1}{2}}E\cdot E\delta_{i j}\right)$$$$\implies T_{i j}\equiv \frac{1}{4\pi}\left[E_{i}E_{j}+B_{i}B_{j}-\frac12\left(E^{2}+B^{2}\right)\delta_{i j}\right]$$
$$\implies \frac{ \partial  }{ \partial t } (\mathbf{p_{\text{matter}} + p_{\text{field}}}) = \nabla \cdot \mathbf{T}$$
*Then $T_{xy}$ is the current of the x-momentum flowing in direction y*. ^a8f16f

# Noether's Theorem for Fields
Following [[Noether's Theorem]], we get the
>[!thm] Canonical Momentum-Energy tensor of the EM field
>$$T^{\alpha\beta}=-{\frac{1}{4\pi}}\left(g^{\alpha\mu}F_{\mu\lambda}\partial^{\beta}A^{\lambda}-{\frac{1}{4}}g^{\alpha\beta}F_{\mu \nu}F^{\mu\nu}\right)$$
>$$\partial_{\alpha}T^{\alpha\beta} = 0$$

We may expect the space-part of this tensor to be [[#^a8f16f|Maxwell's stress tensor]], however we see this is not the case because it's symmetric and our tensor above isn't. Further, it would seem gauge-variant because of the present of the derivatives of $A$. 

But - things are okay. As it turns out the tensor decomposes into a symmetric part $\theta^{\alpha\beta}$ and anti-symmetric part $\tau^{\alpha\beta}$, in such a way that $\partial_{\alpha}\tau^{\alpha\beta}=0$ on purely algebraic grounds, and $\partial_{\alpha}\theta^{\alpha\beta}=0$ will be solely responsible for the interesting physics.

Indeed substituting $\partial^{\beta}A^{\lambda}=-F^{\lambda\beta}+\partial^{\lambda}A^{\beta}\,$ we can decompose:
$$\cdot T^{\alpha\beta}=\underbrace{ {\frac{1}{4\pi}}\left(g^{\alpha\mu}F_{\mu\lambda}F^{\lambda\beta}+{\frac{1}{4}}g^{\alpha\beta}F_{\mu\lambda}F^{\mu\lambda}\right) }_{ \theta^{\alpha\beta} }-\underbrace{ {\frac{1}{4\pi}}g^{\alpha\mu}F_{\mu\lambda}\partial^{\lambda}A^{\beta} }_{ \tau^{\alpha\beta} },$$
***In vacuum** we can simplify* ([[Tensor Analysis#^1fff98]] ):
$$\begin{align}
\tau^{\alpha\beta}  & = \frac{1}{4\pi}\partial_{\lambda}\left(F^{\lambda\alpha}A^{\beta}\right) \implies \partial_{\alpha}\tau^{\alpha\beta}=\frac{1}{4\pi}\underbrace{\partial_{\alpha}\partial_{\lambda}}_{\text{symmetric}}\left(\underbrace{F^{\lambda\alpha}}_{\text{anti-asymmetric}}A^{\beta}\right)=0 \\

\end{align}$$
Hence:
>[!thm] Symmetric Momentum Energy Tensor
>In vacuum, the conservation equations for the[[Maxwell Equations]] or equivalently for the [[Hamilton's Principle for the EM Field]]can be derived from the symmetric momentum energy tensor:
>$$\theta^{\alpha\beta}= {\frac{1}{4\pi}}\left(g^{\alpha\mu}F_{\mu\lambda}F^{\lambda\beta}+{\frac{1}{4}}g^{\alpha\beta}F_{\mu\lambda}F^{\mu\lambda}\right)=\begin{bmatrix}
u & \frac{1}{c}\mathbf{S} \\
\frac{1}{c}\mathbf{S} & T_{\text{Maxwell}}
\end{bmatrix}$$
>$$\partial_{\alpha}\theta^{\alpha\beta} =0$$
> 








