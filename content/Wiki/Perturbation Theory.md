# In Quantum Mechanics

## Time-Independent QM Perturbation Theory

“תורת הפרעות בלתי תלויה בזמן” ([pdf](zotero://open-pdf/library/items/Q7PEVZSQ?page=5&annotation=DIK3EMG6))

We'll assume a solved Hamiltonian $H_{0}$ with eigensolutions $\ket{n^{(0)}},\;E_{n}^{(0)}$, and a Hamiltonian of the form:
$$H = H_{0} + V$$
If we assume:
$$\big|\;\langle m^{(0)}|V|n^{(0)}\rangle\big|\ll\big|E_{n}^{(0)}-E_{m}^{(0)}\big|$$
Then:
$$\begin{array}{c}{{E_{n}=E_{n}^{(0)}+E_{n}^{(1)}+E_{n}^{(2)}+\ldots}}\\ {{\left|n\right\rangle=\,\left|n^{(0)}\right\rangle+\,\left|n^{(1)}\right\rangle+\,\left|n^{(2)}\right\rangle+\ldots}}\end{array}$$Where:
$$E_{n}^{(1)}=\,\langle n^{(0)}|V|n^{(0)}\rangle=V_{n n}$$
$$E_{n}^{(2)}=\sum_{m\neq n}\frac{\left|\left\langle m^{(0)}|V|n^{(0)}\right\rangle\right|^{2}}{E_{n}^{(0)}-E_{m}^{(0)}}=\sum_{m\neq n}\frac{|V_{m n}|^{2}}{\Delta_{n m}}$$
$$|n^{(1)}\rangle=\sum_{m\neq n}\frac{\langle m^{(0)}|V|n^{(0)}\rangle}{E_{n}^{(0)}-E_{m}^{(0)}}\,|m^{(0)}\rangle=\sum_{m\neq n}\frac{V_{m n}}{\Delta_{n m}}\,|m^{(0)}\rangle$$
