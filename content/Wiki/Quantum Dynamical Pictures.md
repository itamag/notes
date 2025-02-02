# Recap
Letting $H=H_{0} + V$ in Schrodinger's picture:

| Aspect                               | Schrödinger Picture                                          | Heisenberg Picture                                                      | Interaction Picture                                                                                                                                                                                 |
| ------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **State kets**                       | $\ket{\psi(t)} = e^{-\frac{i}{\hbar}Ht} \ket{\psi(0)}$       |                                                                         | $\ket{\psi_{I}(t)}  \equiv e^{\frac{i}{\hbar}H_{0}t}\ket{\psi_{S}(t)}$<br>$\ket{\psi_{I}(t)} = e^{\frac{i}{\hbar}H_{0}t}U(t)\ket{\psi_{S}(0)}$<br>$\ket{\psi_{I}(t)}=U_{I}(t)\ket{\psi_{I}(0)}$<br> |
| **Observables**                      |                                                              | $\hat{A}_H(t) = e^{\frac{i}{\hbar}Ht} \hat{A}_S e^{-\frac{i}{\hbar}Ht}$ | $\hat{A}_I(t) = e^{\frac{i}{\hbar}H_0t} \hat{A}_S e^{-\frac{i}{\hbar}H_0t}$                                                                                                                         |
| **Time evolution generator**         | $H$                                                          | $H$                                                                     | $V$                                                                                                                                                                                                 |
| **Time evolution operator**          | $U(t) = e^{-\frac{i}{\hbar}Ht}$                              | $U(t) = e^{-\frac{i}{\hbar}Ht}$                                         | $U_I(t) = e^{\frac{i}{\hbar}H_0t} U(t) e^{-\frac{i}{\hbar}H_0t_{0}}$                                                                                                                                |
| **Dynamical equation (kets)**        | $i\hbar \frac{ \partial  }{ \partial t } U(t) = H\cdot U(t)$ |                                                                         | $i\hbar \frac{ \partial  }{ \partial t } U(t) = V_{I}(t)\cdot U(t)$                                                                                                                                 |
| **Dynamical equation (observables)** |                                                              | $i\hbar \frac{d}{dt} \hat{A}_H(t) = [\hat{A}_H(t), H]$                  | $i\hbar \frac{\partial}{\partial t} \hat{A}_I(t) = [\hat{A}_I(t), H_0]$                                                                                                                             |

In the interaction picture, we have one time evolution operator for the kets and another for the observables.
# Schrodinger
The mathematical formalism presented at the beginning of a QM course describes states, observables, transformations, symmetries and the connections between them.

Naturally, we're interested in understanding how a system and our observations of it will evolve in time. We define the time-evolution operator $\mathcal{U}(t_{1},t_{2})$ from $t_{1}\to t_{2}$  as an operator which must have the properties of: 
1. Composition:
$$\mathcal{U}(t,t+\Delta t_{1} + \Delta t_{2}) = \mathcal{U}(t+\Delta t_{1},t+\Delta t_{1}+\Delta t_{2})\mathcal{U}\left( t,t+ \Delta t_{1}\right)$$
2. Identity:
$$\mathcal{U}(t,t) = I$$
3. Unitarity / probability conservation:
$$\mathcal{U}^{\dagger}\mathcal{U} = I \iff \forall_{\ket{\alpha} }. \bra{\alpha}\mathcal{U}\ket{\alpha} = \bra{\alpha} \ket{\alpha}     $$
It follows that there exists a Hermitian operator ${} \Omega = \Omega ^{\dagger} {}$ such that:
$$\frac{d}{dt} \mathcal{U}(t;t_{0}) = -i\Omega \cdot\mathcal{U}(t;t_{0})$$

In an analogy to classical mechanics, this operator will be called the Hamiltonian because it is the generator of time-evolution (up to factor which is necessary for the Hamiltonian to have units of energy - $H = \hbar\Omega$).

[[Schordinger's Equation]] can then be derived, based on these algebraic properties alone:
$$i\hbar \frac{ \partial  }{ \partial t } \mathcal{U}(t;t_{0}) = H\mathcal{U}(t;t_{0}) \iff i\hbar \frac{ \partial  }{ \partial t } \ket{\alpha_{t}} = H\ket{\alpha_{t}}  $$
We can think of unitary transformations such as $\mathcal{U}$ in two ways. The first, the Schrodinger/active picture, says that the state/kets are changing $\ket{\alpha} \to U\ket{\alpha}$. The second, due to Heisenberg/passive - says that the observables are changing while the states/kets stay the same $A \to U^{\dagger}AU$. The Heisenberg passive transformation is analogous to the change of reference frame we think of in classical mechanics.

It's important to observe however, that in the Heisenberg/passive picture the *eigenkets* of an observable *do* change, because the observable changes. Again in analogy to the frame of reference change, the eigenkets will undergo the inverse time evolution:
$$A(0)\ket{\alpha} = \alpha \ket{\alpha} \implies A_{t}\cdot (\mathcal{U}^{\dagger}_{t} \ket{\alpha})  = \alpha \cdot (\mathcal{U}^{\dagger}_{t}\ket{\alpha} ) $$

# The Interaction Picture
With a Hamiltonian $H = H_{0} + V(t)$, the interaction picture is a mash-up of sorts between Heisenberg's and Schrodinger's pictures. Operators change in time as if they were under the Hamiltonian $H_{0}$ in Heisenberg's picture, and kets change in time as if they were under the Hamiltonian $V(t)$ in Schrodinger's picture.

![[Pasted image 20250112165359.png]]

Thus we get from [[Schordinger's Equation]]:
>[!thm] Interaction Picture Schrodinger-Like Equation:
$$i\hbar{\frac{\partial}{\partial t}}|\alpha,t_{0};t\rangle_{I} =e^{i H_{0}t/\hbar}V e^{-i H_{0}t/\hbar}e^{i H_{0}t/\hbar}|\alpha,t_{0};t\rangle_{S} = $V_{I}|\alpha,t_{0};t\rangle_{I}$$

And we get also the equivalent of Heisenberg's equation:

> [!thm] Interaction Picture Heisenberg-Like Equation
> $$\frac{d A_{I}}{d t}=\frac{1}{i\hbar}[A_{I,}H_{0}],$$


>[!thm] The Interaction Picture Time-Evolution Operator
> The time-evolution operator in the interaction picture is defined as:
> $$U_{I}(t,t_{0})\equiv e^{i H_{0}t/\hbar}U(t,t_{0})e^{-i H_{0}t_{0}/\hbar}$$
> From which it follows:
> $$i\hbar\frac{d}{d t}U_{I}(t,t_{0})=V_{I}(t)U_{I}(t,t_{0})$$

^7cb92c

