We need to expand Noether's theorem from the context of Analytical Mech where it was defined for systems with a discrete set of variables.

Say that a continuous symmetry of the EM system is a continuous transformation of the field $\psi(X^\alpha) \stackrel{s}{\to}\phi(X^\alpha ;s)$, such that the solutions remain the same under Hamilton's principle. Then we must have:
1. The Lagrangian density doesn't change in first order, up to adding a four-divergence of a field $\Lambda^\alpha$

$$\frac{\partial\mathcal{L}}{\partial s}=\underbrace{\frac{\partial\mathcal{L}}{\partial\phi}}_{\partial_{\alpha}\frac{\partial\mathcal{L}}{\partial(\partial_{\alpha}\phi)}}\frac{\partial\phi}{\partial s}+\frac{\partial\mathcal{L}}{\partial\left(\partial_{\alpha}\phi\right)}\underbrace{\frac{\partial\left(\partial_{\alpha}\phi\right)}{\partial s}}_{\partial_{\alpha}\left(\frac{\partial\phi}{\partial s}\right)}=\partial_{\alpha}\left.\left[\frac{\partial\mathcal{L}}{\partial\left(\partial_{\alpha}\phi\right)}\frac{\partial\phi}{\partial s}\right]\right|_{s=0}\stackrel{!}{=}\partial_{\alpha}\Lambda^{\alpha}$$
***At s=0 we expect in advance the action to be the identity, up to addition of gauge transformation.***

This can be written as a continuity equation:
$$\partial_{\alpha}I^{\alpha}=\partial_{\alpha}\left[\frac{\partial{\mathcal{L}}}{\partial\left(\partial_{\alpha}\phi\right)}\left.\frac{\partial\phi}{\partial s}\right|_{s=0}-\Lambda^{\alpha}\right]=0$$

For example, if the Lagrangian doesn't depend on the coordinates $\mathcal{L} = \mathcal{L}(\psi,\partial_{\alpha}\psi)$, we get the canonical energy-momentum tensor
$$T^{\alpha}{}_{\beta}={\frac{\partial{\mathcal{L}}}{\partial\left(\partial_{\alpha}\varphi\right)}}\partial_{\beta}\varphi-\delta^{\alpha}{}_{\beta}{\mathcal{L}};\;\;\;\;\partial_{\alpha}T^\alpha_{\;\;\beta} = 0$$
Or:
$$T^{\alpha\beta}={\frac{\partial{\mathcal{L}}}{\partial\left(\partial_{\alpha}\varphi\right)}}\partial^{\beta}\varphi-g^{\alpha\beta}{\mathcal{L}}$$
