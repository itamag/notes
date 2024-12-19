# In Quantum Mechanics

Defined by the [[Commutator|commutation]] relations:
$$[J_{i},J_{j}]=\sum_{k}i\hbar\epsilon_{i j k}J_{k},\qquad\left[J^{2},{\bf J}\right]=0$$
## Orbital Angular Momentum
![[Pasted image 20241122145332.png]]

$$P_{\ell}^{m}\left(x\right)={\frac{1}{2^{\ell}\ell!}}\left(1-x^{2}\right)^{m/2}{\frac{\mathrm{d}^{\ell+m}}{\mathrm{d}x^{\ell+m}}}\left(x^{2}-1\right)^{\ell}$$[🔖](zotero://open-pdf/library/items/Y56CQUPC?page=6&annotation=G3AUF5ZP)

## Spin

A spin is an angular momentum operator denoted $S$. A particle has a given, fixed value for $S^2$ (equivalently fixed quantum number/ quantum eigenspace $s$). 

**The spin space and the corresponding spin state are independent of the regular Hilbert space, so spin commutes with all regular operators**

Unlike [[Angular Momentum#Orbital Angular Momentum]], spin numbers can take half-integer values

>[!theorem] Magnetic Dipole Moment of Spin
>$$H=-{\boldsymbol{\mu}}\cdot\mathbf{B}:\qquad\boldsymbol{\mu}_{S}=\gamma\mathbf{S}=g{\frac{q}{2m c}}\mathbf{S}\quad\left({\boldsymbol{\mu}}_{L}={\frac{q}{2m c}}\mathbf{L}\right)$$

[[Pauli Matrices]]
[[Stern Gerlach]]
## Addition of Angular Momentum in Composite Systems

Context: what is the total angular momentum in a system with more than one particle, where the state space is a product of the individual particle spaces?

The total angular momentum in a given axis, is just the sum of the individual particles' momentums $m = m_{1}+m_{2}$. The total angular momentum is subtler, because the angle between the two momenta is non-deterministic.

>[!proposition] Definition for the total angular momentum of composite system
>$$S^2 = \left(S^{(1)}\right)^{2}+\left(S^{(2)}\right)^{2}+2\mathbf{S}^{(1)}\cdot\mathbf{S}^{(2)}$$
>$${\bf S}^{(1)}\cdot{\bf S}^{(2)}\,|\!\uparrow\!\downarrow\,\rangle=\left(S_{x}^{(1)}\,|\!\uparrow\!\rangle\right)\left(S_{x}^{(2)}\,|\!\downarrow\,\rangle\right)+\left(S_{y}^{(1)}\,|\!\uparrow\!\rangle\right)\left(S_{y}^{(2)}\,|\!\downarrow\,\rangle\right)+\left(S_{z}^{(1)}\,|\!\uparrow\!\rangle\right)\left(S_{z}^{(2)}\,|\!\downarrow\,\rangle\right)$$

So the quantum numbers $s$ will be determined as the eigenvalues of $S^2$.

>[!claim] Eigenvalues of the total spin
>$$s=(s_{1}+s_{2})\,,\;(s_{1}+s_{2}-1)\,,\;(s_{1}+s_{2}-2)\,,\dots,\;|s_{1}-s_{2}|$$
>Roughly speaking, the highest total spin occurs when the individual spins are aligned parallel to one another, and the lowest occurs when they are antiparallel [🔖](zotero://open-pdf/library/items/PZZ2UD4T?page=191&annotation=XJRHW6WA)

### Eigenbasis for the total angular momentum

>[!Recap] Recap
>Given two angular momenta J1 and J2 (<u>i.e. the quantum numbers $j_i$ are fixed</u>) we can work in two bases:
>1. The product of the single particle basis |j1m1⟩ ⊗ |j2m2⟩ = |j1j2m1m2⟩. These states are generally not eigenstates of J2 = (J1 + J2)2. 
>2. In the basis |j1j2jm⟩ in which J2 and Jz = J1z + J2z are diagonal. Finding these states amounts to block-diagonalizng the (2j1 + 1)(2j2 + 1) space into blocks of constant j. The coefficients that transform one basis to the other are called Clebsch-Gordan coefficients. Below we find these coefficients.” ([pdf](zotero://open-pdf/library/items/V3A3F9XN?page=9&annotation=3LMBPYNF))
>My explanation on basis 2: we divide the subspace determined by specific values of $j_{1},j_{2}$ into smaller subspaces - shared eigenspaces of the total angular momentum and total z-coordinate angular momentum. Turns out these are enough quantum numbers such that all of our eigenspaces are of dimension 1.

Instead of using the $\ket{j_{1}j_{2}m_1m_{2}}$ eigenbasis of $J_{i}^2, J_{iz}$, we'll decompose the subspace with fixed $j_{1}, j_{2}$ values into eigenspaces of $J^2, J_{z}$. The $j_i$ are fixed because we care about spin.
$$j_{1}\otimes j_{2}=|j_{1}-j_{2}|\oplus\left(|j_{1}-j_{2}|+1\right)\oplus\ldots\oplus j_{1}+j_{2}.$$
The benefit of this new basis, is that in this basis rotations are block-diagonal. In other words, rotations won't change the total angular momentum, but just its projection. 

### Changing Bases, Calbesh-Gordan

By algebra of the angular momentum operator, we can already know how $S_{\pm}$ (lowering indices of the total momenta) should act on the vectors $\ket{jm}$ in the subspace $j_{1},j_{2}$ - the total $j$ will not change, and we will lower $m$. 

So, we can find the $\ket{jm}$ eigenvectors by first setting $m=m_{\text{max}}=m_{1,\text{max}} + m_{2,\text{max}}$, which will give $j=j_{1}+j_{2}$.:
$$\ket{j_{1}+j_{2},j_{1}+j_{2}}  = \ket{++} $$
Then by repeatedly using $S_-$ on both sides of the equation, we will find all $\ket{j_{1}+j_{2},m}$ values until the last one $$\ket{j_{1}+j_{2},-|j_{1}-j_{2}|} = \ket{--}$$





