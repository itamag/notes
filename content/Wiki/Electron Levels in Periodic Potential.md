>[!quote]
>In this chapter we shall discuss those properties of the electronic levels that depend only on the periodicity of the potential, without regard to its particular form.  [🔖](zotero://open-pdf/library/items/2CHG866D?page=114&annotation=U7HPLQN7)
>
>“We emphasize at the outset that perfect periodicity is an idealization. Real solids are never absolutely pure, and in the neighborhood of the impurity atoms the solid is not the same as elsewhere in the crystal. Furthermore, there is always a slight temperature-dependent probability of finding missing or misplaced ions (Chapter 30) that destroy the perfect translational symmetry of even an absolutely pure crystal. Finally, the ions are not in fact stationary, but continually undergo thermal vibrations about their equilibrium positions” (Ashcroft and Mermin, 1976, p. 90)


Idea: To understand electrons in matter, we'll depict the atoms as a [[Crystal Lattice]] which creates a periodic potential, then solve [[Schordinger's Equation]]
# Toy Model
To get going, we'll use the physical assumptions:
1. 1: The atoms form a [[Crystal Lattice]]
3. Each atom has just one orbital.
4. The atoms (i.e. lattice points) are far enough from one another such that the orbital of different atoms don't overlap and it's clear where the electron is on the lattice.
5. The potential of each atom can only move an electron from a site to its neighbors.


Which gives the mathematical equivalents:
1. Bravais Lattice AND periodic wavefunction (in 1D: $\psi(x+a) = \psi(x)$)
2. For each atom/site, there is just one eigenstate (of the Hamiltonian). $$H_{m}\ket{m} = \varepsilon_{\alpha} \ket{m} $$
	And $\varepsilon_{\alpha}$ is the energy **of the atom**.
3. For atoms/sites $n,m$ of the lattice, the eigenfunctions are orthogonal $$\bra{m}\ket{n} = \delta_{mn} {}$$
2. If $H = K + \sum_{j \in \text{lattice}}V_{j}$ then $$\bra{n}V_{j}\ket{m} = V_{0}\delta_{nm} -t \delta_{n,m\pm 1}$$
From here we develop:
1. Compute $\bra{n}H\ket{m}$ and $\implies$ Hamiltonian eigenstates are linear combinations of the $\ket{n}$ states $\psi = \sum_{n}A_{n}\ket{n}$
2. Periodic boundary condition $\implies$ $A_{n} = \frac{1}{\sqrt{ N }}e^{ikna}$, **where $N$ is the number of electrons in the region of space where we solve the problem**
3. Lattice periodicity  $\implies A_{k} = A_{k+N} \implies e^{ikna} = 1$

Finally  ([pdf](zotero://open-pdf/library/items/KXSQC4NR?page=70&annotation=TSLQD56W)):
>[!thm] Dispersion relation of a 1D atomic chain
>$$H\psi = \epsilon\psi \implies H_{nm}\psi_{m} = \epsilon\psi_{m} \implies\epsilon - \epsilon_{0} = -2t\cos(ka)$$
>Where we used the assumption of a single, shared orbital/energy level in the first implication, and $\epsilon_{0}\equiv\epsilon_{a} + V_{0}$. 
>This is a dispersion relation for our model! But it's dependent on the so called lattice momentum rather than the particle momentum

^0c789d

>[!thm] Electron velocity in 1D atomic chain
>From [[#^0c789d]] : 
>$$v_{\mathbf{k}} = \frac{1}{\hbar}\frac{ \partial \epsilon_{\mathbf{k}} }{ \partial \mathbf{k} } $$


# Higher Dimensions

>[!thm] Bloch's Theorem
> For a potential $V$ invariant to translation by a [[Crystal Lattice]] $\mathbf{R}$, the solutions to [[Schordinger's Equation]] will be of the form:
> $$\Psi_{n,\mathbf{k}}(\mathbf{r})=e^{i\mathbf{k}\cdot\mathbf{r}}u_{n,\mathbf{k}}(\mathbf{r})$$
> Where
> $$u_{n,\mathbf{k}}(\mathbf{r+R})=u_{n,\mathbf{k}}(\mathbf{r})$$
> The momentum $\mathbf{k}$ is not the momentum of the wavefunction $\Psi_{n,\mathbf{k}}$ (this function is not a momentum eigenstate). However, it may be called a lattice momentum, because if $\mathbf{k'} \equiv \mathbf{k}+\mathbf{G}$ where $\mathbf{G}$ is the [[Reciprocal Lattice]], then $\Psi_{\mathbf{k'}} = \Psi_{\mathbf{k}}$.
>  A function $\psi$ can always be found such that:
>  $$\Psi_{n,\mathbf{k}}(\mathbf{r})=\sum_{\mathbf{R}}e^{i\mathbf{k\cdot R}}\,\psi(\mathbf{r-R})$$

^b2e546


And conclusions:
1. The solution is invartiant to translation 
2. [!!!] Generally $k \in \frac{2\pi}{Na}\mathbb{Z}$, and we'll have a wavefunction solution for each $k$. But due to periodicity of the lattice originating the problem, we can see that (in the 1D case) if the lattice has period $a$ then the [[Reciprocal Lattice]] has period $\frac{2\pi}{a}$, and so the momentum translation $k \mapsto k + \frac{2\pi}{a}$ is the minimal translation such that the lattice is intact, which will yield from invariance $\psi_{k} = \psi_{k+\frac{2\pi}{a}}$. All in all, $k \in \left[ -\frac{\pi}{a}, \frac{\pi}{a} \right]$ **I don't understand why not $k = -\frac{2\pi}{a} \frac{N-1}{N}, \dots, \frac{2\pi}{a} \frac{N-1}{N}$**

# Kronig Penney


# Bi-Atomic 1D Lattice / Chain
“1 מודל פשטני לשרשרת דו-אטומית” ([pdf](zotero://open-pdf/library/items/MLBTW6YH?page=2&annotation=RL9H8WNA))


