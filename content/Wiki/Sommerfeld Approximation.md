>[!theorem] Sommerfeld Expansion for Fermi-Dirac Statistics
>$$\int_{-\infty}^{\infty}{\frac{H(\varepsilon)}{e^{\beta(\varepsilon-\mu)}+1}}\,\mathrm{d}\varepsilon=\int_{-\infty}^{\mu}H(\varepsilon)\,\mathrm{d}\varepsilon+{\frac{\pi^{2}}{6}}\left({\frac{1}{\beta}}\right)^{2}\!H^{\prime}(\mu)+O\!\left({\frac{1}{\beta\mu}}\right)^{4}$$
([pdf](zotero://open-pdf/library/items/THE4E543?page=1&annotation=7LEPP2GJ))

(Electrons have [[Angular Momentum#Spin|half-spin]] and so their multiplicity for a given wavevector is 2)

For metals at room temperature, the energy-level occupation function is very close to the Fermi-Dirac distribution seen for T=0. Thus, in the Sommerfeld approximation, to evaluate an integral of quantities that are dependent on the energy level and are additive in electron numbers (for example energy - if you have two electrons at the same energy level, you will have double the energy), we can use the regular integral at T=0 and then add a minor contribution from the smooth cutoff that replaced the step drop:

![[Pasted image 20241128141227.png]]
We can go further, and use the $T=0$ integral only up to $\mu_{F} = \epsilon_{F}$:
$$\int_{0}^{\mu}H({\mathcal{E}})\,d{\mathcal{E}}=\int_{0}^{{\mathcal{E}}_{F}}H({\mathcal{E}})\,d{\mathcal{E}}+\left(\mu-{\mathcal{E}}_{F}\right)H\left({\mathcal{E}}_{F}\right)$$
And finally we get:
$$\mu=\mathcal{E}_{F}-\frac{\pi^{2}}{6}\,(k_{B}T)^{2}\,\frac{g^{\prime}\left(\mathcal{E}_{F}\right)}{g\left(\mathcal{E}_{F}\right)}$$
The density g may change between different models for electrons, for example if we assume or do not assume the [[Model of Conduction#Drude-Sommerfeld|free electron approximation]]
