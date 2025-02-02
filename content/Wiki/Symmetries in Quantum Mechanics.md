# Premise
<u>Transformations</u> are represented by unitary operators. Why unitary? Because the inner product ${} \bra{\chi}T\ket{\psi } {}$ represents a physical quantity (when $\chi$ is an eigenvector for some operator, from which the general case follows). 

We have two equivalent ways of transforming the dynamics: (1) transforming the wavefunction $\ket{\psi} \to U\ket{\psi}$, or (2) the operators $O \to U^{\dagger}OU$.  This is equivalent because $$\langle\chi|O^{\prime}|\psi\rangle~=~\langle\chi^{\prime}|O|\psi^{\prime}\rangle$$
<u>Symmetries</u> are transformations under which the solutions for [[Schordinger's Equation]] remain the same. A sufficient condition is commutation with the Hamiltonian: $$\left[H,U\right]=0$$
<u>Continuous Symmetry</u>: if we have a continuous family of transformations $U(\theta)$, then by [[Lie Group Theory]] there exists a unitary infinitesimal generator $G$ s.t.: 
$$\begin{gathered}
U(\theta) = e^{-i\theta G/\hbar} \\
U\left(\epsilon\right)\simeq U(0)-\frac{i\epsilon}{\hbar}G = \mathbf{1}-\frac{i\epsilon}{\hbar}G
\end{gathered}$$
In this sense, the generator is the derivative of the family.

Further, from Heisenberg's equation ^[Notice we use Heisenberg because we care about the operator and not the wavefunction], for a family $U(\theta)$ that does not explicitly depend on time: 
$${\frac{\mathrm{d}U}{\mathrm{d}t}}={\frac{1}{i\hbar}}\left[U,H\right]=0\implies{\frac{\mathrm{d}G}{\mathrm{d}t}}=0$$
> [!method] Finding the Generator of a Transformation
> Generally we can see:
> $$U_{\epsilon}^{\dagger}xU_{\epsilon} \simeq \left( 1+\frac{i\epsilon}{\hbar}G \right)x\left( 1-\frac{i\epsilon}{\hbar}G \right)\simeq x - \frac{i}{\hbar }[x,G]\epsilon$$
> So by knowing how the transformation should act on specific operators, we get "differential equations" for the generator.

>[!method]- Computing a transformed operator
>Using ![[Commutator#^97ffdd]] 


# Examples of Continuous Symmetries
$${\mathcal{T}}\left(\mathbf{a}\right)=e^{-i\mathbf{p}\cdot\mathbf{a}/\hbar}:\left|\mathbf{r}+\mathbf{a}\right\rangle={\mathcal{T}}\left(\mathbf{a}\right)\left|\mathbf{r}\right\rangle,\quad{\mathcal{U}}\left(t,0\right)=e^{-i H t/\hbar}:\left|\psi\left(t\right)\right\rangle={\mathcal{U}}\left(t,0\right)\left|\psi\left(0\right)\right\rangle$$
For example for the position translation $\cal{T}$, indeed the generator is $\mathbf{p}$, and we see:
$$\mathcal{T}_{\epsilon}^{\dagger}x\mathcal{T}_{\epsilon} \simeq \left( 1+\frac{i\epsilon}{\hbar}G \right)x\left( 1-\frac{i\epsilon}{\hbar}G \right)\simeq x - \frac{i}{\hbar }[x,G] + O(\epsilon^2)$$
[[The QM Rotation Operator]]

# Algebraic View
We have a Hilbert space $\mathcal{H}$ representing all possible states of our system. If change the system (or change our frame of reference), what was once the state $\ket{\psi}$ may now seem to be the state $\ket{\psi'}$ (what was once the operator $L_{z}$ may now seem like the state $L_{x}$). 

On physical grounds, we expect transformations of the system or our reference frame to be invertible, and that $\lVert \psi \rVert = \lVert \psi' \rVert$. Thus, *transformations must be unitary*. On algebraic grounds, we may say that the system is described precisely by the algebraic structure $\mathcal{H}$, and so automorphisms of $\mathcal{H}$ (unitary operators) are nothing but maps between different ways of describing the same physical system, i.e. transformations.

Naively, one may deduce that all unitary operators are symmetries, because they keep the structure of $\mathcal{H}$. However, we don't have one Hilbert space, but rather one for each moment in time. *Symmetries are those transformations that commute with the time-evolution of the system: we expect to get the same observations if we first rotate our system, let it play out, then de-rotate it, and if we just let it play out (assuming it is spherically symmetric)*.  We defined various [[Quantum Dynamical Pictures|time-evolution operators]]. These are transformations of the $\mathcal{H}$, taking $\ket{\psi_{t_{0}}}\to \ket{\psi_{t}}$. Specifically, each time-evolution operator is a continuous family of operators, which form a group. As such it has a generator ([[Lie Group Theory]]). *From the algebraic approach, the Hamiltonian is defined to be the generator of time-evolution. Hence, symmetries are those transformations that commute with the Hamiltonian*.

*Particularly, if we have an operator $\mathcal{O}$ commuting with the Hamiltonian, they can be jointly diagonalized, and eigenstates of $\mathcal{O}$ (i.e. states with definite $\mathcal{O}$ values) will be conserved in time. This is why symmetry leads to conservation laws.*

Let's return to our continuous symmetries. By definition, the composition of such symmetries is a symmetry, and they must have an identity and inverse and so they form a continuous group. This group can be considered as representations of an abstract group, say the rotations $SO(3)$. So we can find various family of transformations of our Hilbert space that represent rotations. 