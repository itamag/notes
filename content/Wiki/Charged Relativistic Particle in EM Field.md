The total action will be a sum of [[Special Relativity#חלקיק חופשי יחסותי במבט אנליטי]] action and the *interaction action*. Assumptions for its derivation:
1. Action should be a scalar
2. The EM potential is not reference-frame invariant, and so we assume a vector.
3. The action should be proportional to the charge amount, and additive in the potential
4. *The particle is not radiating as it moves, or this radiation is negligible*

Therefore we guess:

> [!theorem] Interaction Action of Charged Relativistic Particle (CGS)
$$S_{\text{int}} = -\frac{q}{c}\int A_{\mu}dx^\mu = \int\left( -q \varphi - +\frac{q}{c}\vec{A}\cdot \vec{v} \right)dt$$
> Where $A = (\varphi, \vec{A})$
> We see that $S_{\text{int}}$ is the classical non-relativistic action
> We can further transform into the covariant formulation:
> $$\delta S = \int\left\{ \frac{mdU_{\mu}}{d\tau} - \frac{q}{c}\left( \frac{ \partial A_{\nu} }{ \partial X^\mu }  - \frac{ \partial A_{\mu} }{ \partial x^\nu }  \right)U^\nu \right\}dx^\mu d\tau$$
> And from Hamilton's principle
> $$\frac{dP_{\mu}}{d\tau} = \frac{mdU_{\mu}}{d\tau} = \frac{q}{c}\left( \frac{ \partial A_{\nu} }{ \partial X^\mu }  - \frac{ \partial A_{\mu} }{ \partial x^\nu }  \right)U^\nu \equiv \frac{q}{c} F_{\mu \nu}U^\nu$$
> Where we defined the [[The Electromagnetic Field Tensor|field tensor $F$]]



![[Pasted image 20241124131935.png]]



Where we used [[Classical EM#^67920e]] and
![[Pasted image 20241124124224.png]]

We compute the action variation using [[Calculus of Variation#מדריך הישרדות]]


## Reworking the interaction action for charge densities
2. Ron discusses charge density, says he'll assume it's differentiable even though in practice it's a sum of delta functions. Says that this is okay if we do coarse graining.
	1. Charge density is not a Lorenz scalar, even though charge itself is! This is due to Lorentz contraction. Ron says $\rho dV = dq$ , i.e. the total charge in a volume element, is a scalar. 
3. By the above discussion of charge density we get: that $dq\cdot dX^\mu = \rho \frac{dX^\mu}{dt} \cdot \frac{d\Omega}{c}$ is a four-vector
	1. The Minkowski space volume element $d\Omega$ is a scalar because as we perform Lorentz transformations, the time dilation and Lorenz contraction will cancel out. [[Special Relativity#Minkowski Spacetime]]
	2. Because we know that the expression is a four vector and the volume elemtn is a scalar, then the charge current $J^\mu = \rho \frac{dX^\mu}{dt}$ is a four-vector. It's worth mentioning that the derivative is the normal time derivative. Indeed, if it was $d\tau$ then we wouldn't have had a four-vector generally (because we'd have a four-vector times a non-scalar).

So:
$$S_{\text{int}} = -\sum_{i}\frac{q_{i}}{c}\int A_{\mu}dx^\mu \sim -\frac{1}{c^2}\int A_{\mu}J^\mu d\Omega \implies \mathcal{L}_{\text{int}} = -\frac{1}{c^2}A_{\mu}J^\mu$$
