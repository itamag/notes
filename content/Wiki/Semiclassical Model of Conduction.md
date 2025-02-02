>[!warning]
>For this topic, the recitation is more important than theoretical understanding. Also it has some expressions that we need to use in the test “מבוא למצב מוצק תשפ“ה – תרגול 11” ([pdf](zotero://open-pdf/library/items/T5V27AQW?page=1&annotation=MYSCEDDV))
# Preliminaries
Based on a quantum model we have a band structure ${} E_{n}(\mathbf{k})$. If we model a semi-classical electron as a wave packet with rather definite momentum and position (for example integrating over a small range of $\mathbf{k,R}$ values in the [[Tight Binding Model]]) - then its velocity can be modeled as the group velocity:
$$\mathbf{v} = \frac{1}{\hbar}\frac{ \partial E_{n}(\mathbf{k}) }{ \partial \mathbf{k} } $$
The particle current *density* due to such particles with crystal momentum $\mathbf{k}$ is the velocity times the amount of particles with that state:
$$\delta\mathbf{j} = \mathbf{v}\cdot \frac{d^3{\mathbf{k}}}{(2\pi)^3} \cdot \underbrace{ D }_{ \text{Degeneracy of } E,\mathbf{k} } = \frac{1}{(2\pi)^3\hbar}\frac{ \partial E_{n} }{ \partial \mathbf{k} } \cdot D\cdot d^3\mathbf{k}$$
Because each particle takes up a volume of $\frac{V}{(2\pi)^3}$ in $\mathbf{k}$-space where $V$ is the volume of our crystal. If the energy band is filled and at the limit of an infinite crystal, the total current of a given [[The Band Structure|energy band]] is $\int_{BZ1}\delta\mathbf{j} = 0$. ***The integral vanishes because we integrate over the k-gradient of a function with the lattice periodicity, which is promised to vanish***. The reason for that is that we can turn the volume integral of the derivative to the boundary surface integral of the function. BZ1 is symmetric, but when traversing the boundary we will add contributions with the same values $E_{n}(\pm \mathbf{k})$ but the opposite orientation of integration and thus the contributions will cancel out.

As a result, if the band is not completely filled, the current $\delta \mathbf{j}$ will only be determined by the unoccupied states:
$$\mathbf{j} = \int_{\text{occupied states}}\delta \mathbf{j} = \left[ \int_{\text{BZ1}} - \int_{\text{unoccupied}} \right]\delta \mathbf{j} = -\int_{\text{unoccupied}}\delta \mathbf{j}$$
So we can think of the current in the metal as a current due to charges with *opposite* sign, the populate exactly those states that cannot be populated by the electrons ([[The Band Structure|in the Fermi state]]). This may be useful when most of the band is filled and thus there are many less "holes" than actual electrons. 

# Application of EM Field
>[!quote]
>![[The Band Structure#^d68c15]]


The (mean) current can also be explained semi-classically by the wave packet / particle analogy, and ***assuming a weak electric field*** (for example to avoid electrons being able to jump between separate bands):

$$\hbar\dot{\mathbf{k}}=-e\left[\mathbf{E}(\mathbf{r},t)+{\frac{1}{c}}\mathbf{v}_{n}(\mathbf{k})\times\mathbf{H}(\mathbf{r},t)\right]$$ ^0afb44

Then we can construct a Newton-like equation:
$$\begin{align}
\underbrace{ \mathbf{\dot{v}} }_{ \mathbf{a} } = \frac{1}{\hbar} \frac{d}{dt} \frac{ \partial \epsilon_{n}(\mathbf{k}) }{ \partial \mathbf{k} } = \frac{1}{\hbar^2}\frac{ \partial^2 \epsilon_{n} }{ \partial k_{i}\partial k_{j} } \dot{k_{j}} = \underbrace{ \frac{1}{\hbar} \mathbb{D} ^2\epsilon_{n} }_{ \frac{1}{m} }\cdot \underbrace{ (-e)\left[\mathbf{E}(\mathbf{r},t)+{\frac{1}{c}}\mathbf{v}_{n}(\mathbf{k})\times\mathbf{H}(\mathbf{r},t)\right] }_{ \mathbf{F} }
\end{align}$$

^d57cb3

^543cbb
Where $\mathbb{D}^2\epsilon_{n}$ is the Hessian, and we have a *tensor effective mass*, which is symmetric, and scalar if the band is isotropic ($\epsilon_{n} = \epsilon_{n}(k)$). ***In a way, we reproduced the [[Sommerfeld Approximation]] with an effective mass tensor. ***

# Impurities and Relaxation Time Approximation
According to the semiclassical equation [[#^d57cb3]]  , if only a constant electric field is applied then the electrons will accelerate indefinitely (supposedly by Roni). This means that there is no electric resistance, which we've also seen in [[Tight Binding Model]]. 

Empirically this can't be - what could be the cause? Empirical metals aren't perfectly periodic: they may have impurities or thermal effects. However, we don't precisely know the nature of these imperfections. Hence thermodynamics / statistical physics enter the picture, and the new theory will seem familiar ([[Model of Conduction#Drude-Sommerfeld]]). 

Let's assume that the imperfections can be described by random collisions in the material, changing the momentum of Bloch electrons. *Say that the probability of an electron to collide in time $dt$ is ${dt}/{\tau_{n}(\mathbf{r,k})}$ , and these collisions drive the system towards an equilibrium state, with electron density that is constant in time: *
$$g_{n}(\mathbf{r},\,\mathbf{k},\,t)=g_{n}^{0}(\mathbf{r},\,\mathbf{k})=\frac{1}{e^{(\varepsilon_{n}(\mathbf{k})\,-\,\mu(\mathbf{r})\,)/k_{B}T(\mathbf{r})}\,+\,1},$$

*We'll assume the temperatures are low enough such that chemical potential is roughly the Fermi energy surface $\mu \approx \mathcal{E}_{F}$, **i.e. only the energy level close to the Fermi level have significant density***

Assumptions: (1) $k_{B}T \ll \mathcal{E}_{F} \iff \mu \approx \mathcal{E}_{F}$ (2) in equilibrium the occupation $f$ of energy states is the Fermi-Dirac distribution (3) out of equilibrium, the occupation $f$ is close to $f_{\text{FD}}$ is a function of the entire phase space $\mathbf{r,k}$, not just the momentum states. (4) After each scattering, we return to equilibrium, i.e.  scatterings happen much sparser than the relaxation time of the system.

We get a PDE for $f$:

$${\frac{\partial f}{\partial t}}+\mathbf{v}\cdot\nabla_{\mathbf{r}}f-{\frac{e}{\hbar}}\mathbf{E}\cdot\nabla_{\mathbf{k}}f=-{\frac{f-f_{0}}{\tau(\mathbf{k})}}$$


Which depends on the applied $\mathbf{E}$. If it's weak:$$f(\mathbf{k})\approx f_{0}(\mathbf{k})+{\frac{e\tau}{\hbar}}\mathbf{E}\cdot\nabla_{\mathbf{k}}f_{0}\approx f_{0}\left( \mathbf{k}+\frac{e\tau}{\hbar}\mathbf{E} \right)$$
This is a more formal statement of our intuition in [[The Band Structure#^d68c15]]! ***Applying a weak external electric field shifted the electrons in each level to a slightly different crystal momentum.***

Hence:
$${\bf J}_{n}=-e\!\int_{\mathrm{{BZ1}}}\!{\frac{\mathrm{d}^{3}k}{4\pi^{3}}}\,f^{(n)}({\bf k})\,{\bf v}_{n}({\bf k})=e\!\int_{\mathrm{
{BZ1}}}\!{\frac{\mathrm{d}^{3}k}{4\pi^{3}}}\left[1-f^{(n)}({\bf k})\right]{\bf v}_{n}({\bf k})$$