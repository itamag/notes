# Premise
<u>Transformations</u> are represented by unitary operators. Why unitary? Because the inner product $\bra{\chi}\ket{\psi }$ represents a physical quantity (when $\chi$ is an eigenvector for some operator, from which the general case follows). 

We have two equivalent ways of transforming the dynamics: (1) transforming the wavefunction $\ket{\psi} \to U\ket{\psi}$, or (2) the operators $O \to U^{\dagger}OU$.  This is equivalent because $$\langle\chi|O^{\prime}|\psi\rangle~=~\langle\chi^{\prime}|O|\psi^{\prime}\rangle$$
<u>Symmetetries</u> are transformations under which the solutions for [[Schordinger's Equation]] remain the same. A sufficient condition is commutation with the Hamiltonian: $$\left[H,U\right]=0$$
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
[[Euler Rotations]]