[[Crystal Lattice]]

The reciprocal lattice of a Bravais lattice is the set of wave-vectors for which a plane wave will be invariant to any translation by the direct lattice vectors. This reciprocal lattice will have all symmetries of the direct lattice. So if the direct is the set $\mathbf{R}$ and the reciprocal $\mathbf{K}$ we must have:
$$
e^{i\mathbf{K}\cdot\mathbf{R}} = \left\{1\right\}
$$

^c9cd54
>[!remark] The Reciprocal Lattice as Fourier Transform
>Quite generally one can think of the reciprocal lattice as being a Fourier transform of the direct lattice. [🔖](zotero://open-pdf/library/items/FBFPCZB4?page=144&annotation=MU3P3Z34)
>Denote by $\rho(\mathbf{r})$ the density describing the direct lattice (i.e. a sum of delta functions). It's periodic, so we'll choose a primitive unit cell and compute the Fourier *series*:
>$$\mathcal{F}[\rho_{\mathbf{R}}(\mathbf{r})]=\sum_{\mathbf{R}}e^{i\mathbf{k\cdot R}}=\frac{(2\pi)^{D}}{v}\sum_{\mathbf{G}}\delta^{D}(\mathbf{k}-\mathbf{G})$$
>$$\implies \rho_{\mathbf{R}} = \frac{(2\pi)^{D}}{v}\sum_{\mathbf{G}}e^{i\mathbf{k}\cdot \mathbf{G}}$$
>Where $v$ is the volume of the unit cell. In fact, any (integrable) function with the periodicity of the lattice. will have a Fourier transform of the form:
>$$\mathcal{F}[\rho({\bf r})]=(2\pi)^{D}\cdot\left( \underbrace{ \int_{u n i t-c e l l}e^{i{\bf k}\cdot{\bf x}}\rho({\bf x}) }_{ S(\mathbf{k}) } \right)\cdot\sum_{{\bf G}}\delta^{D}({\bf k}-{\bf G}) = (2\pi)^D \cdot (\mathbf{S} \ast \rho_{\mathbf{G}})(\mathbf{k})$$
>$S(\mathbf{k})$ is called *the structure factor*and evidently depends on our choice of unit cell.
>
>

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

>[!thm] Volume of Reciprocal Lattice Primitive Unit Cell
>For a crystal lattice of volume $V$ and $N$ primitive cells, the volume of a primitive cell in the reciprocal lattice is:
>$$\frac{(2\pi)^3}{v} \equiv (2\pi)^3\cdot \frac{N}{V}$$

^d4406d
# BRILLOUIN Zone

The [[Crystal Lattice#^02fae9|Wigner-Seitz primitive cell]] of the reciprocal lattice is known as the first Brillouin zone [🔖](zotero://open-pdf/library/items/I2H7EZCQ?page=111&annotation=KBMV2YC2)

>[!def] Brillouin Zone
>Start with the reciprocal lattice point G = 0. All k points which are closer to 0 than to any other reciprocal lattice point define the first Brillouin zone. Similarly all k points where the point 0 is the second closest reciprocal lattice point to that point constitute the second Brillouin zone, and so forth. Zone boundaries are defined in terms of this definition of Brillouin zones. [🔖](zotero://open-pdf/library/items/FBFPCZB4?page=150&annotation=BYRGIK2E)
>
>*Physical waves in crystals are unchanged if their wavevector is shifted by a reciprocal lattice vector k → k + G. Thus, the Brillouin zone has been defined to include each physically different crystal momentum exactly once*


>[!remark] Drawing the Brillouin Zone
>Draw the perpendicular bisector between the point 0 and each of the reciprocal lattice vectors. These bisectors form the Brillouin zone boundaries. Any point that you can get to from 0 without crossing a perpendicular bisector is in the first Brillouin zone. If you cross only one perpendicular bisector, you are in the second Brillouin zone, and so forth.
>![[Pasted image 20250113163311.png|200]]




# Lattice Planes

LATTICE PLANES [🔖](zotero://open-pdf/library/items/I2H7EZCQ?page=111&annotation=FGHVK5Z8)

>[!def] Bravais Lattice Plane
>Given a particular Bravais lattice, a lattice plane is defined to be any plane con¬ taining at least three noncollinear Bravais lattice points [🔖](zotero://open-pdf/library/items/I2H7EZCQ?page=112&annotation=CJKWQPTY)
>
> "*A lattice plane* (or crystal plane) is a plane containing at least three non-collinear (and therefore an infinite number of ) points of a lattice. *A family* of lattice planes is an infinite set of equally separated parallel lattice planes which taken together *contain all points of the lattice*.” (Simon, 2013, p. 131)[🔖](zotero://open-pdf/library/items/FBFPCZB4?page=145&annotation=4F68GQNU)
> ![[Pasted image 20250113120533.png|300]]


>[!thm] Lattice Plane - Reciprocal Lattice Duality
>The lattice planes are in one-to-one correspondence with the reciprocal lattice vectors. Denoting the normalized vector: $$\mathbf{G} = h_{i}\mathbf{b}_{i}\implies \mathbf{\hat{G}} = \frac{1}{\text{gcd}(h_{i})}\mathbf{G}$$
>Then the *families* of lattice planes are in one-to-one correspondence with the set of normalized reciprocal lattice vectors.
>For each plane family, the displacement (orthogonal) vector $\mathbf{d}$ between consecutive planes is *(up to scale)* a member $\mathbf{G}$ of the reciprocal lattice, and its scale is: $$d = \frac{2\pi}{\lvert \lvert \mathbf{\hat{G}} \rvert  \rvert_{2} }$$
>(Simon, 2013, p. 131) [🔖](zotero://open-pdf/library/items/FBFPCZB4?page=146&annotation=E62HFL9D)
>*In other words, each reciprocal lattice vector $\mathbf{G}$ represents a frequency, or periodicity of the direct lattice. In the direction of $\mathbf{G}$ , we have a 1D lattice with angular frequency $G$, or equivalently with lattice spacing $d=\frac{2\pi}{G}$. This 1D lattice defines a family of infinite planes, each one perpendicular to it and passing through one of its points. However, this is not necessarily a family of lattice planes. Lattice plane families must have 3+ non co-linear lattice points in each plane, and cover all lattice points. If we choose $\mathbf{\hat{G}}$as our frequency vector , we will have both properties (this is not straightforward).
>There is a big gotcha here - how is there even a minimal $\mathbf{G}$?  After all, if $g$ is some frequency, than $\frac{g}{n}$is a frequency for all natural n. *Answer:  the italicized interpretation here is based on the Fourier series interpretation of the reciprocal lattice. In this interpretation, the reciprocal lattice vectors depict the frequencies within a primitive unit cell, which are bounded from below.

>[!warning]
>Not every Miller index is necessarily a lattice plane. In fact, all Miller indices are lattice planes if and only if we use the primitive unit vectors of the reciprocal lattice if and only if we use the primitive unit vectors of the direct lattice.
>Further, a *family* of lattice planes will be represented by the reduced index $\frac{(h,k,l)}{\text{gcd}(h,k,l)}$, and any multiple of which will be a lattice plane in that family.

## Miller Indices
![[Pasted image 20241212165914.png]]
