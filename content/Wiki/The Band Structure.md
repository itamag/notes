# Insulator or Conductor
In a [[Crystal Lattice]], due to the Born-Karman boundary conditions, *the number of allowed crystal-momentum values (in [[Crystal Lattice|BZ1]]) is exactly the number of primitive unit cells in the crystal*. Further, we can assume that the temperature is low enough such that it's in the [[Sommerfeld Approximation|Fermi state]] - the electrons will populate quantum states in increasing order based on energy. 

![[Pasted image 20250130141207.png]]
 [🔖](zotero://open-pdf/library/items/FBFPCZB4?page=188&annotation=7ISPKCSW)

So we'll start assigning electrons to each allowed $\mathbf{k}$-value in $E_{1}$ band, then $E_{2}$.. At some point, we'll run out of electrons! If each cell has $n$ [[valence electrons]], then there are $n\cdot N$ in total where there are $N$ unit cells, and we have $N\cdot B\cdot D$ available quantum states, where $B$ is the number of bands, and $D$ is the degeneracy of a single $\mathbf{k},E$ state (for example if the spin is taken into account and there is no magnetic interaction, the spin doesn't affect the energy and so each $\mathbf{k},E$ state is actually two distinct state with $\pm$ spin).

*The maximal energy we achieved in the above procedure is approximately the Fermi energy*. 

If a band is not filled, then some electrons could change their crystal momentum if an electric field is applied, *which creates a **mean** current - usually the states $\pm \mathbf{k}$ have the same energy and will have the same number of electrons, and thus the mean current is zero. If there is an electric field, it breaks that symmetry and the current will not be zero (see figure)*. [[Semiclassical Model of Conduction#Application of EM Field]] ^d68c15


# ETC

> [!thm]
> In any and all [[Crystal Lattice]], $\mathcal{E}_{n}(\mathbf{k}) = \mathcal{E}_{n}(-\mathbf{k})$