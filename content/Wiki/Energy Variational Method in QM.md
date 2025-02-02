Variational Methods [🔖](zotero://open-pdf/library/items/PMLKPKUE?page=336&annotation=ZIJBIUBA)

>[!quote]
>The variational method we now discuss is very useful for estimating the ground-state energy when [exact solutions to the Hamiltonian] are not available. [🔖](zotero://open-pdf/library/items/PMLKPKUE?page=336&annotation=WJUURY2N)

The ground-state energy is the lowest eigenvalue of the Hamiltonian. As such, for any vector $\ket{\tilde{0}}$: $$\frac{\bra{\tilde{0}}H\ket{\tilde{0}}}{\bra{\tilde{0}} \ket{\tilde{0}} } = \frac{\left( \sum_{n}\alpha_{n}^2E_{n}  \right)}{\bra{\tilde{0}}\ket{\tilde{0}}  } \geq E_{0}  $$
Usually we'll utilize this in the following way: choose a *continuous family of test kets* parameterized by $\vec{\lambda}$, then minimize the above LHS quantity on $\lambda$ using derivatives. 

>[!warning]
>The above theory that $\frac{\bra{\tilde{0}}H\ket{\tilde{0}}}{\bra{\tilde{0}} \ket{\tilde{0}} }\geq E_{0}$ seems to be true for the entire Hilbert space. However in practice, we'll have some boundary conditions for the solutions to [[Schordinger's Equation]] and hence not all Hilbert space vectors will be solutions. In other words, the above inequality holds only for those vectors which are spanned by the Hamiltonian eigenvectors. We'll have to verify that our test-kets have this property, and it'd be sufficient to check the boundary conditions.



