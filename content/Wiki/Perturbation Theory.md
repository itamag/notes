# In Quantum Mechanics


## Time-Independent Non-Degenerate QM Perturbation Theory

“תורת הפרעות בלתי תלויה בזמן” ([pdf](zotero://open-pdf/library/items/Q7PEVZSQ?page=5&annotation=DIK3EMG6))
Time-Independent Perturbation Theory: Nondegenerate Case [🔖](zotero://open-pdf/library/items/PMLKPKUE?page=308&annotation=4TN3SH76)

*Problem statement*: assume a solved Hamiltonian $H_{0}$ with eigensolutions $\ket{n^{(0)}},\;E_{n}^{(0)}$, and a Hamiltonian of the form:
$$H = H_{0} + V$$
Such that:
$$\big|\;\langle m^{(0)}|V|n^{(0)}\rangle\big|\ll\big|E_{n}^{(0)}-E_{m}^{(0)}\big|$$
The potential $V$ is the *perturbation*. The physical rationale behind this conditions is: (1) we'd like to perform small adjustments to our diagonalized system and so it makes sense to represent $V$ in that basis (LHS); (2) $V$ is a small addition to our system, and so it makes sense that it must be small w.r.t. the *difference* between energy levels. We wish to solve:
 $$(H_{0}+\lambda V)|n\rangle_{\lambda}=E_{n}^{(\lambda)}|n\rangle_{\lambda}$$
And letting:

$$\Delta_{n} \equiv E_{n} - E_{n}^{(0)} = \lambda \bra{n^{(0)}}V\ket{n} \iff E_{n} = E_{n}^{(0)} + \lambda \bra{n^{(0)}}V\ket{n}$$


We get: $$(E_{n}^{(0)}-H_{0})|n\rangle=(\lambda V-\Delta_{n})|n\rangle.$$We'd like to invert the LHS operator to get an equation of the form $\ket{n} = \mathcal{O}\ket{n}$, but it's singular (due to $\ket{n^{(0)}}$).  So we split the Hilbert space into two orthogonal subspaces, one corresponding to $\ket{n^{(0)}}$, and the other its complement. Applying $\bra{n^{(0)}}$ to both sides of the equation we get $0=0$, and so we can choose any component $c_{n}(\lambda)$ we want in the $\bra{n^{(0)}}$ direction. It's useful to choose $=1$.

Now restricting our attention to the complement subspace, we can safely write:

>[!thm] Exact implicit solution of Hamiltonian non-Degenerate Perturbation
>$$|n\rangle=\underbrace{ |n^{(0)}\rangle }_{ \ket{n^{(0)}}\text{-space solution}  }+\underbrace{ \frac{1}{E_{n}^{(0)}-H_{0}}\Phi_{n}(\lambda V-\Delta_{n})|n\rangle }_{ \text{complement-space solution} }$$
>$$\Delta_{n} \equiv E_{n} - E_{n}^{(0)} = \lambda \bra{n^{(0)}}V\ket{n}$$
>Where $\Phi_{n}\equiv I - \ket{n^{(0)}}\bra{n^{(0)}}$

^021379

Where $\Phi_{n}\equiv I - \ket{n^{(0)}}\bra{n^{(0)}}$ just annihilates the $\bra{n^{(0)}}$ coordinate which we wish to avoid. We found equations for the modified energy eigenkets and eigenvalues as functions of $\lambda$. Assuming analyticity, we can do *power expansion*:
$$\begin{array}{l}{{\langle n\rangle=|n^{(0)}\rangle+\lambda|n^{(1)}\rangle+\lambda^{2}|n^{(2)}\rangle+\cdots}}\\ {{\Delta_{n}=\lambda\Delta_{n}^{(1)}+\lambda^{2}\Delta_{n}^{(2)}+\cdots.}}\end{array}$$
By repeatedly substituting the two equations of [[#^021379]]  into each other we get:
>[!thm] Power-Expansion Approximation of non-Degenerate Perturbation
>$$\begin{align}
\Delta_{n} & \approx\lambda \underbrace{ V_{n n} }_{ \Delta_{n}^{(1)} } \\
 & +\lambda^{2}\underbrace{ \sum_{k\neq n}\frac{|V_{n k}|^{2}}{E_{n}^{(0)}-E_{k}^{(0)}} }_{ \Delta_{n}^{(2)} }
\end{align}$$
>$$\begin{align}
\ket{n} & \approx \ket{n^{(0)}}+ \lambda\underbrace{ \sum_{k\neq n}|k^{(0)}\rangle\frac{V_{k n}}{E_{n}^{(0)}-E_{k}^{(0)}} }_{ \ket{n^{(1)}}  } \\
 & +  \lambda^{2}\underbrace{ \left(\sum_{k\neq n}\sum_{l\neq n}\frac{|k^{(0)}\rangle V_{k l}V_{l n}}{(E_{n}^{(0)}-E_{k}^{(0)})(E_{n}^{(0)}-E_{l}^{(0)})}-\sum_{k\neq n}\frac{|k^{(0)}\rangle V_{n n}V_{k n}}{(E_{n}^{(0)}-E_{k}^{(0)})^{2}}\right) }_{ \ket{n^{(2)}}  }
\end{align}$$
Where $V_{mn}=\bra{m^{(0)}}V\ket{n^{(0)}}$ is the potential representation *in the unperturbed basis*.  The summation expansion (vs. matrix notation) is useful here because the matrices are infinite dimensional.

>[!rmk] 
>1. It's clear from the above expansion of the second-order energy-shift that *different* energy levels tend to repel each other when a perturbation is applied. This is a special case of the no-level crossing theorem, which states that a pair of energy levels connected by perturbation do not cross as the strength of the perturbation is varied.
>2. The perturbed ground energy will always be lower than the unperturbed ground energy.


## Time-Independent Degenerate QM Perturbation Theory

If the unperturbed Hamiltonian has eigenvalue degeneracy, then the above equations don't work, as we have items of the form:$$\frac{\bra{n_{i}^{(0)}}V\ket{n_{j}^{(0)}}}{\lvert E_{n_{i}}^{(0)} - E_{n_{j}}^{(0)} \rvert} = \frac{V_{ij}}{\lvert E_{n_{i}}^{(0)} - E_{n_{j}}^{(0)} \rvert}$$
We can still use perturbation theory, but we'll have to use the right basis for each degenerate eigenspace $D$, which is the eigenbasis of the perturbation, denoted by a new index $\alpha$, aka $\{\ket{n_{\alpha}^{(0)}}\}$. Letting $P$ be the projection onto that subspace, we require:
$$PVP\ket{n_{\alpha}^{(0)}} = \Delta _{\alpha}^{(1)}\ket{n_{\alpha}^{(0)}} $$
The reason for this is: if we choose a basis such that the perturbation $V$ is diagonal, then $V_{nk} = 0$ for $n \neq k$ in the degenerate eigenspace, and we can ignore the zero denominator ([🔖](zotero://open-pdf/library/items/PMLKPKUE?page=320&annotation=W84DGZIF)).

The final results then follow through sheer algebra:
>[!thm] Power-Expansion Approximation of Degenerate Perturbation
>$$\Delta_{\alpha} \approx \lambda\underbrace{ \langle n_{\alpha}^{(0)}|V|n_{\alpha}^{(0)}\rangle }_{ E_{\alpha}^{(1)} } + \lambda^2 \underbrace{ \sum_{m\not\in D}\frac{\left|\left\langle m^{(0)}|V|n_{\alpha}^{(0)}\right\rangle\right|^{2}}{E_{\alpha}^{(0)}-E_{m}^{(0)}}}_{E_{\alpha}^{(2)}  }$$
>$$\left|n_{\alpha}\right\rangle \approx \left|n_{\alpha}^{(0)}\right\rangle + \lambda\underbrace{ \sum_{m\not\in D}{\frac{\langle m^{(0)}|V|n_{\alpha}^{(0)}\rangle}{E_{\alpha}^{(0)}-E_{m}^{(0)}}}\left|m^{(0)}\right\rangle }_{ \left|n_{\alpha}^{(1)}\right\rangle }$$

## Time-Dependent Perturbation Theory in QM
תורת הפרעות תלויה בזמן [🔖](zotero://open-pdf/library/items/C6MHE6UA?page=1&annotation=LJRVBSGP)
Time-dependent perturbation theory ∗ [🔖](zotero://open-pdf/library/items/MX3R9QGL?page=1&annotation=VIZBVLA3)

Working in [[Quantum Dynamical Pictures#The Interaction Picture|the interaction picture]] is useful here because will get, (setting $t_{0}\equiv_{0}$):
$$\ket{\psi_{t}}_{S} \equiv \sum_{n}c_{n}(t)\ket{n_{t}} _{S} \implies \ket{\psi_{t}}_{I} =\sum_{n}c_{n}(t)\ket{n_{0}}_{I}   $$
Plugging these results into the [[Quantum Dynamical Pictures#Recap|dynamical eqution of the interaction picture]], and seeing that we found a representation of the state where only the coefficients (and not the spanning vectors) change in time (algebra spared):
$$i\hbar \sum_{n}\frac{ \partial c_{n}  }{ \partial t }\ket{n_{0}}_{I}  = V_{I}(t)\sum_{n}c_{n}(t)\ket{n_{0}}_{I} $$
Shoving $I=\sum_{m}\ket{m_{0}}\bra{m_{0}}$ in there and multiplying by some $\bra{n_{0}}$ (mind the abuse of notation), we see that we have a linear equation over the $\ket{n_{0}}$ basis:
$$i\hbar\frac{\partial}{\partial t}c_{m}\left(t\right)=\sum_{n}V_{m n}\left(t\right)e^{i\omega_{m n}t}c_{n}\left(t\right)$$
![[Pasted image 20250114173004.png|400]]
Where $V_{m n}\left(t\right)\,\equiv\,\langle m|V\left(t\right)|n\rangle,\;\;\omega_{m n}\,\equiv\,\left(E_{m}-E_{n}\right)/\hbar$. *Note that exponent added - this is because we switched from using $V_{I}$ from the interaction picture to using $V$*. 

We don't like solving PDEs and hence we approximate iteratively.  We *assume that we start at an eigenstate $\ket{i_{0}}$ and hence*  that ${} c_{n}^{(0)}=\delta_{ni} {}$ are constant in time and so:
$${\partial_{t}c_{n}^{(0)}(t)=0}$$
Then we can continue:
$$\begin{align}
i\hbar \frac{ \partial  c_{m}^{(k+1)} }{ \partial t } & =\sum_{n} V_{mn}e^{i\omega_{mn}t}c_{n}^{(k)} \\
\end{align}$$

^b454f6

The first (test important) expansions:

> [!thm] Time-Dependent Perturbation Approximation in QM
> *Assuming we start at an eigenstate of the unperturbed Hamiltonian, i.e.* $\ket{\psi(0)}=\ket{i}$ and denoting ${} \ket{\psi_{t}}_{S} = \sum_{n}c_{n}(t)\ket{n_{t}}_{S} {}$, it follows:
> $$\begin{align}
> c_{n}\left(t\right) & =c_{n}^{(0)}+c_{n}^{(1)}+c_{n}^{(2)}+\ldots \\
> c_{n}^{(0)}  &  = \delta_{ni}\\
> c_{n}^{(1)} & =\displaystyle-\frac{i}{\hbar}\int_{0}^{t}\mathrm{d}t^{\prime}\,V_{n i}\left(t^{\prime}\right)e^{i\omega_{n i}t^{\prime}} \\
> c_{n}^{(2)} & =\left(-\frac{i}{\hbar}\right)^{2}\sum_{m}\int_{0}^{t}\mathrm{d}t^{\prime}\,V_{n m}\left(t^{\prime}\right)e^{i\omega_{n m}t^{\prime}}\int_{0}^{t^{\prime}}\mathrm{d}t^{\prime\prime}V_{m i}\left(t^{\prime\prime}\right)e^{i\omega_{m i}t^{\prime\prime}}
> \end{align}$$
> Don't confuse complex $i$ with the $i$ eigenstate.. This can also be considered as an iterative expansion of the time-evolution operator in the interaction picture, see [[Quantum Dynamical Pictures#^7cb92c]] 

^6125bf

Then the probability to be at state $\ket{j_{0}}$ at time $t$, given we started at $\ket{i_{0}}$ at $t_{0}=0$:
$$\mathbb{P}(i\stackrel{t}{\to}j) = \left\lvert  \sum_{k}c_{j}^{(k)}(t)  \right\rvert^2$$
We can think of $c_{j}^{(k)}$ as probability amplitudes that the system will be at $j$ at time $t$ after performing exactly $k$ hops, given that it started at $i$. This is because the equation for $c_{m}^{(k)}$ is reminiscent of the master equation of a continuous time Markov chain in right-eigenvector convention. Furthering the analogy, we will see that in computing [[#^b454f6]], generally we could separate:
$$\mathbb{P}(i\stackrel{t}{\to}j) = f(V_{mn})\cdot g(\omega_{mn}, t)$$
Meaning that only the energy difference between states dictates the holding time distribution between them.

>[!remark] Approximate Transition Probabilities
>$$\begin{align}
P_{i\rightarrow n}\left(t\right) & =\left|c_{n}\left(t\right)\right|^{2}=\left|c_{n}^{\left(1\right)}\left(t\right)+c_{n}^{\left(2\right)}\left(t\right)+\ldots\right|^{2} \\
 & =\left( \sum_{k}\lvert c_{n}^{(k)} \rvert^2  \right) + \sum_{k_{1} < k_{2}} \text{Re}({c_{n}^{(k_{1})}}^*\cdot c_{n}^{(k_{2})})
\end{align}$$
>Looking at the above theorem, we can think of $V_{nm}$ as *infinitesimal transition amplitudes, i.e. transition rates* from state $\ket{n}\to \ket{m}$. The coefficient $c_{n}^{(k)}(t)$ can be thought of as the (phased) transition probabilities from $\ket{i}\to \ket{n}$ in duration $t$, with $k$ "state-jumps" in between.
>

^60d321

>[!remark]
>$$c_{n}(t)=\langle n|U_{I}(t,t_{0})|i\rangle.$$
>Where $U_{I}$ is the time evolution operator in the [[Quantum Dynamical Pictures#The Interaction Picture|the interaction picture]]. 
>

