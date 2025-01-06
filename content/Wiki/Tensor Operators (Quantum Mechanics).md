>[!quote]
>Tensor Operators, [Sakurai and Napolitano, 2021, p. 248](zotero://select/library/items/M5GJ8IYH), [🔖](zotero://open-pdf/library/items/PMLKPKUE?page=251&annotation=ZV483T5W)

# My Take
## Vector Operators, Cartesian Vector Operators
The states of a quantum system are described by a Hilbert space $\mathcal{H}$. The space $\mathcal{O}  =\text{Hom}(\mathcal{H})$ of operators over $\mathcal{H}$ is a vector space over $\mathbb{C}$. Standard vector operators, for example the angular momentum $\mathbf{J}$, are elements of the vector space $\mathcal{O}^3$, which is infinite-dimensional. However, By choosing 3 independent basis vectors $\mathbf{e}_{i} \in \mathcal{O}$, we can define a 3D vector space $\text{Sp}\{(\mathbf{e_{1}},0,0),(0,\mathbf{e_{2}},0),(0,0,\mathbf{e_{3}})\}$. 

From this perspective, a rotation of the quantum system corresponds to a change of basis: 
$$\mathbf{e}_{i}^\prime = {\mathcal D}^{\dagger}_{R}\mathbf{e}_{i}{\mathcal D}_{R} \equiv \mathbf{e}_{i}^R$$

And see [[The QM Rotation Operator]] for elaboration on the connection between rotating the system and transforming the operators.

Suppose $\mathbf{e}_{i}^R = \sum R_{ij}\mathbf{e}_{j}$, then we'll call the basis a Cartesian basis. It follows that for $\mathbf{V}\in \mathcal{O}$:
$$\sum V_{i}\mathbf{e}_{i} = \mathbf{V} =\sum V_{j}^R\mathbf{e}_{j}^R = \sum_{ij}V_{j}^RR_{ji} \mathbf{e}_{i} \implies \vec{V} = R^T \cdot \vec{V}^R \implies \vec{V}^R = R \cdot \vec{V}$$
If we treat the coordinates as operators on the Hilbert space, we find:
$$(V_{i}\mathbf{e}_{i})^R = {\mathcal D}^{\dagger}_{R}V_{i}\mathbf{e}_{i}{\mathcal D}_{R} = {\mathcal D}^{\dagger}_{R}V_{i}{\mathcal D}^{\dagger}_{R}\cdot{\mathcal D}_{R}\mathbf{e}_{i}{\mathcal D}_{R} = V_{i}^R \mathbf{e}_{i}^R$$
Which implies:
$${\mathcal D}^{\dagger}_{R}\vec{V}{\mathcal D}_{R}=R \cdot \vec{V}$$
## Tensor Operators, Spherical Operators

The above ideas can be generalized to [[Tensor Analysis|tensors]]. For example, a cartesian tensor will be defined over a cartesian tensor basis, with coordinate transformations:

$$.T_{i j k\dots}\longrightarrow T_{i^{\prime}j^{\prime}k^{\prime}\dots}^{\prime}=\sum_{i j k\dots}R_{i^{\prime}i}R_{j^{\prime}j}R_{k^{\prime}k}\cdot\cdot\cdot T_{i j k\dots}$$
From this expression it would seem that rotating the physical system intermixes all coordinates, but this is not the case. In fact, the tensor $T$ is reducible - its indices can be partitioned into subsets, such that rotations only intermix within subsets. This is reminiscent of [[The QM Rotation Operator]], [[The QM Rotation Operator#^a5248b]] . So we define a spherical tensor as this algebra:
$$\begin{array}{c}{{\displaystyle{\mathcal D}^{\dagger}T_{q}^{(k)}\mathcal D=\sum_{q^{\prime}=-k}^{k}\mathcal D_{q q^{\prime}}^{(k)*}T_{q^{\prime}}^{(k)}}}\\ {{\displaystyle{\mathcal D}T_{q}^{(k)}\mathcal D^{\dagger}=\sum_{q^{\prime}=-k}^{k}T_{q^{\prime}}^{(k)}\mathcal D_{q^{\prime}q}^{(k)}}}\end{array}$$

# Lectures

>[!def] QM Vector Operator Definiton
>A vector operator $\mathbf{V}$ in QM is an operator tuple such that the components transform:
>$${\mathcal D}^{\dagger}_{R}V_{i}{\mathcal D}_{R}=\sum_{i}R_{i j}V_{j}$$
>Where $\mathcal{D}$ is [[The QM Rotation Operator]] and $R$ is a [[Rotation Matrix]]. Equivalently we can define using commutation relations:
>$$[V_{i},J_{j}]=i\varepsilon_{i j k}\hbar V_{k}.$$

>[!def] (QM Tensor Operator Definition)
>A tensor operator $T$