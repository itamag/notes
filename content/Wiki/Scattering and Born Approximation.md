Scattering is first described physically semi-classically. We shoot some objects at some other object or a potential, and the see where our original objects end up. In elastic scattering, we assume that due to the scattering the internal states of our objects do not change. For example, if we shoot hydrogen atoms, their energy levels won't change.

# Set-Up 1: 1D Scattering for Analogy
In a scattering scenario, all we can say is what we expect the incoming and outgoing states to be very far from the potential (1D - as $x\to \pm\infty$):

$$\bra{x} \ket{\text{in}} = \begin{cases}
\bra{x} \ket{\mathbf{k}} = I_{R}(X) & x\to-\infty \\
\bra{x} \ket{-\mathbf{k}} = I_{L}(X)&  x\to \infty
\end{cases} $$
Where $I_{R}$ ($I_{L}$) abbreviates incoming with right (left) direction, and the same for $\ket{\text{out}}$. *We'll keep assuming $\lvert \mathbf{k}_{\text{in}} \rvert=\lvert \mathbf{k}_{\text{out}} \rvert$., i.e. elastic scattering i.e. conservation of energy*.  So we can say that the right-moving and left-moving solutions would be:
$$\begin{pmatrix}
\psi_{R} \\
\psi_{L}
\end{pmatrix} = \begin{pmatrix}
I_{R} \\
I_{L}
\end{pmatrix} + \underbrace{ \begin{pmatrix}
t & r \\
r' & t'
\end{pmatrix} }_{ S } \begin{pmatrix}
O_{R} \\
O_{L}
\end{pmatrix}$$
So, $S$ is the representation of the operator $\hat{S} = \ket{\text{out}}\bra{\text{in}}$. *By some crapshoot we say that $\hat{S}$ is unitary*, and we get conservation of probability
$$SS^{\dagger} = I \implies $$
$$\left|r\right|^{2}+\left|t\right|^{2}=1,\quad t^{*}r^{\prime}+t^{\prime}r^{*}=0,\quad\left|t\right|=\left|t^{\prime}\right|,\quad\left|r\right|=\left|r^{\prime}\right|$$
***Revisiting the 1D scattering scenario from Quantum 1, we can interpret the problem in a particle-like manner***. An incoming wave is me sending a particle towards the potential. With some probability the particle will pass it and be transmitted, and with some probability it will be reflected. *By the symmetry of Schrodinger's equation for time-reversal, it follows that $t=t'$*. 


# Set-Up 2: Definite-Momentum Ingoing Particle

Say we're sending a particle/function *with definite momentum* $\mathbf{k}$ towards the potential. Formally, we'll say that there's an *incident wave* $\ket{\mathbf{k}}$. It propagates in time:
$$\bra{\mathbf{r}} \ket{\mathbf{k}_{t}} = \bra{\mathbf{r}}e^{- \frac{i}{\hbar}Ht}\ket{\mathbf{k}} \stackrel{\text{far from potential}}{\approx} e^{i(\mathbf{k\cdot r} - Et/\hbar)}$$
A good guess as to what the transmitted wave should be defined is a *spherically-progpagating wave* (when we're far from the potential):
$$\bra{\mathbf{r}} \ket{\mathbf{\phi_{trans}}} \stackrel{?}{\equiv} f(\theta,\phi)\cdot\frac{e^{i(kr - Et/\hbar)}}{r}$$
The $r$ denominator is because our wavefunction should fall out at infinity. And hence the total ansatz solution:

$$\bra{\mathbf{r}} \ket{\psi} \stackrel{\text{far from potential}}{\approx} e^{-iEt/\hbar}\cdot\left[ e^{i(\mathbf{k_{i}}\cdot \mathbf{r} )} + \frac{f(\theta, \phi)}{r} e^{ik_{f}\cdot r}\right]  $$
^amcsld

*By our assumption of no change to internal states, we must have $k_{i} = k_{f}$ in magnitude*. Further, $E$ here is (somewhat) well defined because if $V \approx 0$ then our momentum eigenstates are also energy eigenstates with $E = \frac{\hbar^2k^2}{2m}$.

## Introduction to Differential Cross Section
We arrived at the conclusion that the outgoing/scattered wave will be a spherical wave modulated by $f(\theta,\phi)$, the scattering amplitude . *In fact, this is the differential cross section:*
$$d\sigma = \lvert f(\theta,\phi) \rvert^2 d\Omega $$
*For intuition, let's say the that incoming wave has uniform probability density. Then for a large stream of particles, each area $d\sigma$ will have some average number of particles, but $d\Omega$ will not be uniform for different angles, because the potential interacted with our particles and has different probabilities of scattering them in different directions. The total cross section is interpreted as the probability of the incoming particles to interact with the potential. If you have a small cross section, you'll shoot many particles at a potential but only a few will scatter.*

## Born Series of the Outgoing Wave
Now moving on to the region where $V \not\approx 0$. Our [[Schordinger's Equation]] (over the position eigenbasis):
$$\left[-\frac{\hbar^{2}}{2m}\nabla^{2}+V({\bf r})\right]\psi({\bf r})=E\psi({\bf r})\,,$$
Which we can simplify using ${} E = \frac{\hbar^2k^2}{2m},\;\;V(\mathbf{r}) \equiv \frac{\hbar^2}{2m}U(\mathbf{r}) {}$:
$$\left(\nabla^{2}+k^{2}\right)\psi(\mathbf{r})=U(\mathbf{r})\psi(\mathbf{r})$$
Now this is easy, we treat the RHS as a function (forgetting for the moment that both sides of the equation have $\psi$ in them) and use a [[Green's Function]]:
$$\psi({\mathbf{r}})=\underbrace{ \psi_{0}(\mathbf{r}) }_{ [\nabla^2+k^2]\psi_{0}=0 }+\int\mathrm{d}^{3}\mathbf{r}^{\prime}G(\mathbf{r}-\mathbf{r}^{\prime})U(\mathbf{r}^{\prime})\psi(\mathbf{r}^{\prime})$$
Where tbh $$\frac{\hbar^{2}}{2m}\,\left\langle\mathbf{r}\left|\hat{G}_{\pm}\right|\mathbf{r}^{\prime}\right\rangle \equiv G_{\pm}\left(\mathbf{r},\mathbf{r}^{\prime}\right)=-{\frac{1}{4\pi}}{\frac{e^{\pm i k|\mathbf{r}-\mathbf{r}^{\prime}|}}{\left|\mathbf{r}-\mathbf{r}^{\prime}\right|}}\;\xrightarrow[r\gg r^{\prime}]{}-{\frac{1}{4\pi}}{\frac{e^{\pm i k r}}{r}}e^{\mp i k{\hat{\mathbf{r}}}\cdot\mathbf{r}^{\prime}}$$
and we are going to refer to G+ as the outgoing wave Green function and to G− as the ingoing wave Green function. We can now drop the position basis representation for the general:
$$\ket{\psi} = \ket{\psi_{0}} + \frac{\hbar^2}{2m}\hat{G}_{\pm}\ket{U\psi}  $$

# Partial Waves and Phase Shifts

## Partial Waves
We'll continue with the [[Schordinger's Equation|TISE]], but now with spherically-symmetric potential $V(\mathbf{r}) = V(r)$. Already if we consider the [[#Set-Up 2 Definite-Momentum Ingoing Particle]] scenario, we can conclude $f(\theta,\phi) = f( \theta)$.

Seeing [[Schordinger's Equation#In Spherical Coordinates]], a nice eigenbasis for our problem is $\ket{\alpha}\otimes \ket{lm}$, where the potential affects only the solutions $\ket{\alpha}$. 

Far from the potential, again we have an incoming definite momentum wave from the left, which we'd like to expand over our new basis. *By the lack of dependence on $\phi$, we must have that only $Y_{l_{0}}$'s contribute:*
$$\begin{align}
e^{i k z} & =e^{i k r\cos\theta}=\sum_{\ell=0}^{\infty}a_{\ell}\underbrace{ P_{\ell}(\cos\theta) }_{ Y_{l0} (\Omega)}j_{\ell}(k r) \\
 & =\sqrt{4\pi}\sum_{\ell=0}^{\infty}\sqrt{2\ell+1}\,i^{\ell}\,Y_{\ell,0}(\theta)j_{\ell}(k r)
\end{align}$$
Where $j_{l}$ are the spherical [[Bessel Functions]]. *Each function in the sum is called a partial wave. As $r\to \infty$, the Bessel functions are approximately sines and cosines of $r$, **i.e. spherical waves***. So, as in the [[#Set-Up 2 Definite-Momentum Ingoing Particle]], we have inbound and outbound spherical waves, with modulations $\ket{lm}$ that determine the scattering amplitudes:

$$e^{i k z}=\frac{\sqrt{4\pi}}{k}\sum_{\ell=0}^{\infty}\sqrt{2\ell+1}\,i^{\ell}\,Y_{\ell,0}(\theta)\frac{1}{2i}\Big[\underbrace{\frac{e^{i\left(k r-\frac{\ell\pi}{2}\right)}}{r}}_{\mathrm{outgoing}}-\underbrace{\frac{e^{-i\left(k r-\frac{\ell\pi}{2}\right)}}{r}}_{\mathrm{incoming}}\Big]\,,\quad r\gg a$$
 ([pdf](zotero://open-pdf/library/items/MBM3E435?page=6&annotation=LF3KMHSD))

## Phase Shifts
Let's think of 1D scattering again, with a finite range potential. Where the potential is zero, the solution basis is $e^{\pm ikx}$, for all $k\in \mathbb{R}_{>0}$ which are (in the context of our problem) incoming and outgoing waves. The incoming wave contribution is determined, and our job is to ask what will the outgoing wave be? First we fixed $k$ by having a definite momentum for the incoming wave and adding conservation of energy. So our total solution is $\psi = Ae^{-ikx} + e^{ikx}$. But supposedly by conservation of [[QM Probability Current|probability current]], it must be that $\lvert A \rvert=1$ and hence all that can happen is the accumulation of a phase shift of the outgoing wave. 

Now, we'll carry over this understanding to our 3D case. Recall above: ![[#^amcsld]]
This is still the problem we're trying to solve: send a plane wave, what will be the scattered wave, which we expect is a modulated radial wave? In 1D above, we saw that far from the potential, each *simple* ingoing wave generates a simple *outgoing* wave, up to phase shift. In our 3D spherically symmetric case, the ingoing and outgoing/scattering waves are the spherical waves. *So, we should expand this equation into the spherical coordinates basis*:
$$
\begin{align}
\text{SOLVED:}\;\;\;\; & f(\theta)=\sum_{l=0}^{\infty}\frac{2l+1}{k}f_{l}P_{l}(\cos\theta)  \\
 & \implies  \\
  & \psi\left({\bf r}\right)\sim\frac{i}{2k}\sum_{\ell=0}^{\infty}i^{\ell}\left(2\ell+1\right)\left[\underbrace{ \frac{e^{-i\left(k r-\frac{\pi}{2}\ell\right)}}{r} }_{ \substack{\text{inbound}\\\text{definite momentum}} }-\underbrace{ (1+2ikf_{l}(k)) }_{ \equiv S_{\ell}\left(k\right) }\underbrace{ \frac{e^{i\left(k r-\frac{\pi}{2}\ell\right)}}{r} }_{ \substack{\text{outbound}\\\text{definite momentum}} }\right]P_{\ell}\left(\cos\theta\right) \\
 & \implies \\ \\
 & S_{l} \equiv 1 + 2if_{l} \equiv e^{2i\delta_{l}} \\ \\

 & \implies \\
 \\
 & f_{l} = e^{i\delta_l}\sin(\delta_{l})
\end{align}$$
$$$$

We've reduced our problem to understanding the phase shift of inbound and outbound waves. Formally, the spherical symmetry of the potential allowed for separation of variables into $r,\Omega$ where the scattering problem is contained to the radial part, which is a 1D scattering problem up to the fact the $r>0$ whereas $x \in (-\infty,\infty)$ which affects boundary conditions.

 Reminiscent of the [[#Set-Up 1 1D Scattering for Analogy|1D case]] we can define an operator $\hat{S}$ that takes as input an inbound state and returns the corresponding outbound state, including amplitude. *In retrospect, all we did was find that $\hat{S}$ is diagonalized over the spherically-separated basis of our Hilbert space. Indeed, taking into account the boundary conditions of no singularity at the origin, the basis is $\ket{klm}$ where $k$ is the radial momentum, and:*
$$\hat{S}\ket{klm} = e^{2i\delta_{l}}\ket{-k,lm}  $$

***The phase shifts are determined by the boundary conditions (at the boundary of the support of the potential) - the wavefunction must be continuous in $\mathbf{r}$ and its derivative must "jump" a certain amount over the boundary.***

>[!thm] Total Cross Section in Partial Waves Formalism
>$$\sigma = \frac{4\pi}{k^{2}}\sum_{l}(2l+1)\sin^{2}\delta_{l}.$$
>We can compute the (total/differential) cross section for each $l$, which represents our cross section for particles with given angular momentum. The *total* cross section will be the sum over all such $l$-cross sections - they don't intermix. However, the differential cross section at a specific angle $\Omega$ isn't the sum of all $l$-differential cross section at that angle. 





----
[^1]: Actually, the 1D S-matrix we saw 