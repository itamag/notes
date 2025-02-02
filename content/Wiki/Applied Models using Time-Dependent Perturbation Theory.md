Chapter 2: Constant Perturbation

### Hypotheses
Physically, this chapter addresses a system where a constant perturbation, $V$, is applied to a time-independent Hamiltonian, $H_0$, starting at $t = 0$. Mathematically, the perturbation is expressed as:

$$
V(t) = \begin{cases} 
0, & t < 0 \\
V, & t \geq 0
\end{cases}
$$

The starting point assumes the system is initially in an eigenstate $|i\rangle$ of $H_0$, with energy $E_i$. The goal is to compute the probability of transitioning to another eigenstate $|n\rangle$ of $H_0$ due to the perturbation.

### Key Results

>[!thm] First-Order Transition Probability with Constant Perturbation
>
To first order in perturbation theory, the probability of transitioning from $|i\rangle$ to $|n\rangle$ is:
> $$
> P(i \to n) \approx 4 \frac{|V_{ni}|^2}{(E_n - E_i)^2} \sin^2\left(\frac{(E_n - E_i)t}{2\hbar}\right).
> $$
> Here, $V_{ni}$ is the matrix element of the perturbation operator, and $\omega = \frac{E_n - E_i}{\hbar}$ represents the energy difference between the states in frequency units. *This result shows that transitions are most probable when energy conservation is nearly satisfied, i.e. between states with nearly-identical energy (wrt the original Hamiltonian $H_{0}$*.

**Time Dependence and Energy Conservation**
For short times, $P(i \to n) \propto t^2$. This may be surprising, because it follows that the system will not achieve a steady-state. but as $t \to \infty$, the probability becomes proportional to $t$, as gradually transitions with large energy differences become improbable. *The linear scaling allows us to continue the analogy to a CTMC described in [[Perturbation Theory#^60d321]], by defining an effective transition rate (probability per unit time) in the long-time limit *:

>[!thm] Fermi's Rule
>In the long-time limit, the transition rate (time-independent probability per unit time, in first-order approximation) $i \to [n]$, where $[n]$ is a set of eigenstates (possibly continuous)  with energy $\approx E_{n}$ is given by Fermi's Golden Rule:
> $$
> \begin{align}
w_{i \to n}  & \equiv \lim_{ t \to \infty } \frac{\mathbb{P}(i \stackrel{t}{\to} n)}{t} \\
 & = \frac{2\pi}{\hbar} \lvert V_{ni} \rvert^2 \delta(E_{n}-E_i) \\ \\
w_{i\to[n]} & = \frac{2\pi}{\hbar}\int d E_{n}\rho(E_{n})|V_{n i}|^{2}\delta(E_{n}-E_{i})\\
 & =  \frac{2\pi}{\hbar} \bar{|V_{ni}|^2} \rho(E_n),
\end{align}
> $$
>Where $\rho(E_n)$ is the density of states at energy $E_n$. *Crap warning: this is ill-defined, particularly because that $V_{ni}$ is not even single-valued. In the last line the bar means taking average over all n's with approximately the same energy as i, which is also ill defined.*

^5703c9


## Chapter 3: Sinusoidal Perturbation

### Hypotheses
In this chapter, the perturbation is time-dependent, oscillating sinusoidally:

$$
V(t) = V e^{i\omega t} + V^\dagger e^{-i\omega t}.
$$

This scenario models systems where external forces or fields (such as electromagnetic waves) interact with quantum systems. The initial state is $|i\rangle$, and the goal is to determine how the oscillatory nature of $V(t)$ affects the transition probabilities.

### Key Results
By taking a good look at [[Perturbation Theory#^60d321]] and [[Perturbation Theory#^6125bf]], we can see that the exponents $e^{\pm i\omega t}$ merely add a "phase shift" to $\omega_{nm}$.  Let's concentrate on $Ve^{\pm i\omega t}$ for now. Setting $\omega'_{nm} = \omega_{nm} \pm \omega$, we effectively reduced the problem to that of a piecewise time-constant potential from [[#Chapter 2 Constant Perturbation|above]]. Reiterating the results, as $t\to \infty$, in first order the only probable transitions are to states $\ket{n}$ with energies $E_{n} \approx E_{i}  \mp\hbar\omega$. *In first order, adding the $\pm$ exponent to the potential made only those transitions to states with an energy of approximately $\hbar\omega$ below (above) $E_{i}$ probable $t\to \infty$.*

Now, *we'll continue assuming the similarity to a CTMC, by thinking of each potential $Ve^{\pm i\omega t}$ as generating an emission/+ (absorption/-) random process represented by a CTMC at steady-state. Then $V(t)$ can be thought of as the simultaneous instantiation of both processes, i.e.:*
$$w_{i\to n} = w_{i\to n}^{(+)} + w_{i\to n}^{(-)}$$
Where the individual rates are determined by Fermi's golden rule as above:

>[!thm] Fermi's Rule for Oscillating Perturbation
> $$w_{i\rightarrow n}^{(+)}=w_{i\rightarrow n}^{(\text{emission})}=\frac{2\pi}{\hbar}\overline{{{|V_{n i}|^{2}}}}\rho(E_{n})\Bigg|_{E_{n}\approx E_{i}- \hbar\omega}$$
> $$w_{i\rightarrow n}^{(-)}=w_{i\rightarrow n}^{(\text{absorption})}=\frac{2\pi}{\hbar}\overline{{{|V_{n i}^{\dagger}|^{2}}}}\rho(E_{n})\Bigg|_{E_{n}\approx E_{i}+ \hbar\omega}$$
> Finally we see, substituting $\lvert V_{ni} \rvert^2 = |V_{in}^{\dagger}|^2$:
> $$\rho(E_{n})w_{n\to i}^{(\text{emission})} = \rho(E_{i})w_{i\to n}^{(\text{absorption})}$$
> *In the long-time limit, we reach a steady-state where on average the number of transitions $i\to n$ (with energy **increase** $\hbar \omega$) is equal to the number of transitions ${} n\to i$ (with energy **decrease** $\hbar\omega$).*

^c11494

>[!warning] Validity of this CTMC analogy
>We have done a *lot* of sketchy stuff. Raffi claims they are valid when:
>1. $\frac{t}{\hbar} \gg \frac{1}{\lvert E_{n}-E_{i} \rvert}\approx \frac{1}{\hbar\omega}$
>2. $\frac{t}{\hbar} \ll \frac{1}{\lvert V_{ni} \rvert}$

---

## Chapter 4: Interaction of an Atom with an Electromagnetic Field
>[!quote]
>![[Pasted image 20250115133752.png]]

The chapter examines the interaction of an atom with an electromagnetic field. The Hamiltonian is given by:

$$
H = \frac{p^2}{2m} + e\phi - \frac{e}{m c} \mathbf{A} \cdot \mathbf{p},
$$

where $\mathbf{A}$ is a *weak* vector potential, and $\phi$ is a *weak* scalar potential. Thus we can treat the $\mathbf{A}$ contribution as a perturbation, and we *assume*:
$$\mathbf{A}(\mathbf{r},t)=2A_{0}\hat{\epsilon}\cos\left(\mathbf{k}\cdot\mathbf{x}-\omega t\right)$$
The primary focus is on two scenarios: (1)Absorption of photons (photoelectric effect);  (2) Spontaneous emission of photons.

Applying the results from [[#^c11494]], we get:
$$w_{i\to n}^{(\text{absorption})}=\frac{2\pi}{\hbar}\frac{e^{2}}{m_{e}^{2}c^{2}}|A_{0}|^{2}\left|\langle n|e^{i{\bf k}\cdot{\bf x}}\hat{\epsilon}\cdot{\bf p}|i\rangle\right|^{2}\delta\left(E_{n}-E_{i}-\hbar\omega\right)$$
> [!note]- Absorption Cross-Section
> We can *define an effective cross-section for the absorption $i\to n$: the average amount of energy absorbed by the point charge per unit time, divided by the average energy flux provided by the EM field:*
> $$\sigma_{\text{abs}} \equiv \frac{\hbar\omega \cdot w_{i\to n}}{\text{EM flux}} = 4\pi^2\alpha \cdot \frac{\hbar}{m_{e}^2\omega}\left\lvert \underbrace{ \bra{n} e^{i\mathbf{k\cdot x}}\cdot\mathbf{\hat{\epsilon}\cdot p}\ket{i} }_{ \propto V_{ni} }  \right\rvert^2 \delta(E_{n}-E_{i-\hbar\omega})$$
> This can be thought of the effective scattering area of the "spherical" point charge

*If we limit our inspection to atomic-scale distances $x$, we can say that usually the EM field wavelength will be much larger:* $$\mathbf{k\cdot x}\sim \frac{x}{\lambda}\ll 1\implies e^{i\mathbf{k\cdot x}} = 1+i\mathbf{k\cdot x} + \dots \approx 1$$
***This it the dipole approximation of the EM field***. Using ***the very useful property that I forgot***: $[x_{j},H_{0}] =\frac{i\hbar}{m}p_{j}$ it follows:
$$\langle n|p_{j}|i\rangle=i m_{e}\omega_{n i}\langle n|x_{j}|i\rangle.$$$$\sigma_{a b s}=4\pi^{2}\alpha\omega_{n i}|\langle n|x_{j}|i\rangle|^{2}\delta\left(\omega-\omega_{n i}\right).$$
#### Photoelectric Effect
To understand the photoelectric effect, we'll drop the dipole approximation. Instead, we'll replace 
The absorption cross-section quantifies the likelihood of photon absorption and is derived as:

$$
\sigma_{\text{abs}} = \frac{4\pi^2 \hbar \alpha}{m_e^2 \omega} |\langle n | e^{i\mathbf{k} \cdot \mathbf{x}} \mathbf{\epsilon} \cdot \mathbf{p} | i \rangle|^2 \delta(E_n - E_i - \hbar \omega),
$$

where $\alpha$ is the fine-structure constant, and $\mathbf{\epsilon}$ is the polarization vector.

#### Spontaneous Emission
The spontaneous emission rate is proportional to the cube of the emitted photon frequency:

$$
\frac{1}{\tau_{i \to n}} = \frac{2\alpha \omega^3}{c^2} |\langle n | \mathbf{\epsilon} \cdot \mathbf{x} | i \rangle|^2.
$$
