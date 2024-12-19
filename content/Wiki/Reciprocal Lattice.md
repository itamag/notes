[[Crystal Lattice]]

The reciprocal lattice of a Bravais lattice is the set of wave-vectors for which a plane wave will be invariant to any translation by the direct lattice vectors. This reciprocal lattice will have all symmetries of the direct lattice. So if the direct is the set $\mathbf{R}$ and the reciprocal $\mathbf{K}$ we must have:
$$
e^{i\mathbf{K}\cdot\mathbf{R}} = \left\{1\right\}
$$

^c9cd54

>[!thm] THE RECIPROCAL LATTICE IS A BRAVAIS LATTICE [🔖](zotero://open-pdf/library/items/I2H7EZCQ?page=108&annotation=XCLHEWCW)
>The reciprocal is a Bravais lattice with the same basis vectors (up to scale)
>$${\bf b}_{i}=2\pi{\frac{{\bf a}_{j}\times{\bf a}_{k}}{\mathbf{a}_{1}\cdot(\mathbf{a}_{2} \times \mathbf{a}_{3})}}$$
>$${\bf b}_{i}\cdot{\bf a}_{j}\,=\,2\pi\delta_{i j}$$
>
>Thus for [[#^c9cd54]] to hold we need the coordinates of $\mathbf{K}$ over the new basis to be integers.

>[!remark] What if the lattice is 2D
>If the lattice is 2D, we'll still use the above procedure, "completing" to 3D with $\hat{\mathbf{n}}$ the vector perpendicular to the lattice

>[!remark] That $\mathbf{\hat{a}}_{i} \neq \mathbf{\hat{b}}_{i}$
>This is only true when the original basis is orthogonal

>[!example] Reciprocal Lattices
>![[Pasted image 20241212164709.png]]
>([pdf](zotero://open-pdf/library/items/MV5P7VMG?page=2&annotation=TMNICFUT))

# BRILLOUIN Zone

The [[Crystal Lattice#^02fae9|Wigner-Seitz primitive cell]] of the reciprocal lattice is known as the first Brillouin zone [🔖](zotero://open-pdf/library/items/I2H7EZCQ?page=111&annotation=KBMV2YC2)

# Lattice Planes

LATTICE PLANES [🔖](zotero://open-pdf/library/items/I2H7EZCQ?page=111&annotation=FGHVK5Z8)

>[!def] Bravais Lattice Plane
>Given a particular Bravais lattice, a lattice plane is defined to be any plane con¬ taining at least three noncollinear Bravais lattice points [🔖](zotero://open-pdf/library/items/I2H7EZCQ?page=112&annotation=CJKWQPTY)

>[!thm] Lattice Plane - Reciprocal Lattice Duality
>For any family of lattice planes separated by a distance d, there are reciprocal lattice vectors perpendicular to the planes, the shortest of which have a length of $\frac{2\pi}{d}$. Conversely, for any reciprocal lattice vector K, there is a family of lattice planes normal to K and separated by a distance d, where:
> $$\frac{2\pi}{d} = \min_{\mathbf{\hat{K}} = \mathbf{\hat{K}'} \in \mathcal{B}} \lvert \lvert \mathbf{K}' \rvert  \rvert $$ is the length of the shortest reciprocal lattice vector parallel to K. [🔖](zotero://open-pdf/library/items/I2H7EZCQ?page=112&annotation=82PZ4N5Z)


## Miller Indices
![[Pasted image 20241212165914.png]]
