
Model: 
1. The crystal is a *finite* Bravais lattice (sample)
2. A planar wave of *X-ray* wavelength ($\sim 1 \mathring{A}$) hits the sample. Equivalently, the wave-length is about the same as the interatomic distances in the lattice
3. The scattering is elastic i.e. there is conservation of energy i.e. the incident and scattered waves have the same wavelength i.e. $|\mathbf{k|} = |\mathbf{k'}|$ for the incident and scattered plane waves.

Experimental Results:

>[!quote]
>In 1913 W. H. and W. L. Bragg found that [...] in crystalline materials, for certain sharply defined wavelengths and incident directions, intense peaks of scattered radiation (now known as Bragg peaks) were observed. [🔖](zotero://open-pdf/library/items/2CHG866D?page=92&annotation=5RDQXQU3)

There are two equivalent ways  to view the scattering of X rays by a perfect periodic structure, due to Bragg and to von Laue.  Both viewpoints are still widely used. The von Laue approach, which exploits the reciprocal  lattice, is closer to the spirit of modern solid state physics

## Bragg Formulation

Model:
1. A crystal is made out of parallel planes of ions, spaced a distance $d$ apart.
2. The wave dynamics can be described satisfactorily by geometric rays.
3. A sharp peak occurs when:
	1. The incident rays are specularly reflected by any such ion plane (incident angle = reflected angle)
	2. Rays from consecutive planes should interfere constructively

> [!thm] Bragg Condition
> $$n\lambda=2d\sin\theta$$
> The integer n is known as the order of the corresponding reflection

Mathematically, we are looking for [[Reciprocal Lattice#Lattice Planes|lattice plane]] families of the [[Crystal Lattice]]. For each family, we'll have different possible incidence angles:

![[Pasted image 20241219133347.png|350]] ![[Pasted image 20241219133411.png|300]]



# Von Laue Formulation

>[!quote]
>One regards the crystal as composed of identical microscopic objects (sets of ions or atoms) placed at the sites $\mathbf{R}$ of a Bravais lattice, each of which can reradiate the incident radiation in all directions. Sharp peaks will be observed only in directions and at wavelengths for which the rays scattered from all lattice points interfere constructively
>
(Ashcroft and Mermin, 1976, p. 70) [🔖](zotero://open-pdf/library/items/2CHG866D?page=94&annotation=4EIFBHCW)

>[!lemma]- Von Laue 2-point condition
>For a plane wave $\mathbf{k} = \frac{2\pi}{\lambda}\mathbf{\hat{n}}$ incident on two identical scatterers, constructive interference will occur if and only if:
>$$\mathbf{d}\cdot(\mathbf{\hat{n}}-\mathbf{\hat{n}'}) \in \lambda \mathbb{Z} \iff \mathbf{d}\cdot(\mathbf{k}-\mathbf{k'}) \in 2\pi \mathbb{Z}$$
>Where $\mathbf{d}$ is the displacement between the scatterers

>[!thm] Von Laue Condition
>*Constructive interference of the refractions of a plane wave $\mathbf{k}$ incident on a crystal lattice will occur only for refractions $\mathbf{k'}$ such that $\mathbf{k'}-\mathbf{k}$ is in the reciprocal lattice.*
>
>`\begin{proof}`
>For a plane wave $\mathbf{k}$ incident on a [[Crystal Lattice]] $\mathbf{R}$, interference will occur only for refracted wavevectors (assumed to have the same wave-length as the incident wave) that have:
>$$\mathbf{R}\cdot(\mathbf{k}-\mathbf{k'}) \subset 2\pi \mathbb{Z}$$
>Equivalently:
>$$e^{i(\mathbf{k}^{\prime}-\mathbf{k})\cdot\mathbf{R}}=1$$
>Which is iff $\mathbf{K}=\mathbf{k'}-\mathbf{k}$ is in the [[Reciprocal Lattice]]
>`\end{proof}`


# Miller Indices of Cubic Family Peaks
- [ ] TBD

>[!thm] Miller Indices of Cubic Family Bragg Peaks
![[Pasted image 20241219200919.png]]
 ([pdf](zotero://open-pdf/library/items/MY4APA5Y?page=6&annotation=Y28T8EH4))

^7ae3ea







