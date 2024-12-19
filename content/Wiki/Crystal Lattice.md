# Definitions

>[!def]- Baravais Lattice
>Two equivalent definitions:
>1. A Bravais lattice is an infinite array of discrete points with an arrangement and orientation that appears exactly the same, from whichever of the points the array is viewed. 
>2. A (three-dimensional) Bravais lattice consists of all points with position vectors R of the form $${\bf R}=n_{1}{\bf a}_{1}+n_{2}{\bf a}_{2}+n_{3}{\bf a}_{3}$$ where $\mathbf{a}_{i}$  are any three vectors not all in the same plane, and $n_{i} \in \mathbb{Z}$ ([pdf](zotero://open-pdf/library/items/2CHG866D?page=84&annotation=TB5LQG6Z))

>[!def]- Primitive Vectors
>The vectors $\mathbf{a}_{i}$ in the definition of the Baravais Lattice are called primitive vectors, and they are not unique

>[!def]- Coordination Number
>The points in a Bravais lattice that are closest to a given point are called its nearest neighbors. Because of the periodic nature of a Bravais lattice, each point has the same number of nearest neighbors. This number is thus a property of the lattice, and is referred to as the coordination number of the lattice. A simple cubic lattice has coordination number 6; a body-centered cubic lattice, 8; and a face-centered cubic lattice, 12.

>[!def]- Primitive Unit Cell
>A volume of space that, when translated through all the vectors in a Bravais lattice, just fills all of space without either overlapping itself or leaving voids is called a primitive cell or primitive unit cell of the lattice.8 There is no unique way of choosing a primitive cell for a given Bravais lattice

While choosing the primitive cell as the parallelogram from the primitive vectors is easy and natural, this choice often does not reveal the full symmetry of the lattice. Instead we can choose:

>[!def]- Conventional Unit Cell
> A unit cell is a region that just fills space without any over¬ lapping when translated through some subset of the vectors of a Bravais lattice. The conventional unit cell is generally chosen to be bigger than the primitive cell and to have the required symmetry.

>[!def]- Wigner Seitz Primitive Cell
>One can always choose a primitive cell with the full symmetry of the Bravais lattice. By far the most common such choice is the Wigner-Seitz cell. The Wigner-Seitz cell about a lattice point is the region of space that is closer to that point than to any other lattice point.10 Because of the translational symmetry of the Bravais lattice, the Wigner-Seitz cell about any one lattice point must be taken into the Wigner-Seitz cell about any other, when translated through the lattice vector that joins the two points. Since any point in space has a unique lattice point, as its nearest neighbor11 it will belong to the Wigner-Seitz cell of precisely one lattice point. 
>[[#^8bb59c]] 
>[[#^d39aaa]]
^02fae9

>[!def] Crystal Structure; Physical Lattice; Lattice with a Basis
>A physical crystal can be described by giving its underlying Bravais lattice, together with a description of the arrangement of atoms, molecules, ions, etc., within a particular primitive cell. When emphasizing the difference between the abstract pattern of points composing the Bravais lattice and an actual physical crystal14 embodying the lattice, the technical term “crystal structure” is used. A crystal structure consists of identical copies of the same physical unit, called the basis, located at all the points of a Bravais lattice (or, equivalently, translated through all the vectors of a Bravais lattice). Sometimes the term lattice with a basis is used instead. 
# Examples and Theorems

>[!example]- Cubic Crystals
>1. Simple cubic: $${\bf a}_{1}=a\hat{x},\;{\bf a}_{2}=a\hat{y},\;{\bf a}_{3}=a\hat{z}$$
>2. Body-centered cubic (BCC): $$\left\{\begin{array}{l l}{{\mathbf{a}_{1}=a{\hat{x}}}}\\ {{\mathbf{a}_{2}=a{\hat{y}}}}\\ {{\mathbf{a}_{3}={\frac{a}{2}}({\hat{x}}+{\hat{y}}+{\hat{z}})}}\end{array}\right.$$ $$\left\{\begin{array}{l l}{\mathbf{a}_{1}={\frac{a}{2}}({\hat{y}}+{\hat{z}}-{\hat{x}})}\\ {\mathbf{a}_{2}={\frac{a}{2}}({\hat{z}}+{\hat{x}}-{\hat{y}})}\\ {\mathbf{a}_{3}={\frac{a}{2}}({\hat{x}}+{\hat{y}}-{\hat{z}})}\end{array}\right.$$
>3. (Face-centered cubic) FCC: $$\left\{\begin{array}{l l}{\mathbf{a}_{1}={\frac{a}{2}}({\hat{x}}+{\hat{y}})}\\ {\mathbf{a}_{2}={\frac{a}{2}}({\hat{y}}+{\hat{z}})}\\ {\mathbf{a}_{3}={\frac{a}{2}}({\hat{x}}+{\hat{z}})}\end{array}\right.$$
![[Pasted image 20241205112241.png]]


>[!thm] Uniqueness of primitive unit cell volume
>The volume of the primitive unit cell is unique, even though the cell choice itself isn't unique
>![[Pasted image 20241205113155.png]]

>[!clm] Symmetry of the Wigner Seitz Primitive Cell
>Because the definition of the Wigner Seitz cell is geometric, it must obey all symmetries of it lattice.

^8bb59c

# Procedures

> [!clm] Counting the Points in a Unit Cell
> - Introduction: The problem with counting points in a unit cell, is that some lattice points will fall on the cell surface and will be shared between neighboring cells.
> - Method: instead of figuring out a unique set of surface points for each cell, count all points and for each point divide by the number cells that share it.

^e793da

>[!clm] Recipe for Building the [[#^02fae9]] 
> - Draw line segments from one lattice point to all other lattice points.
> - From the midpoint of each segment, draw a perpendicular line (in 3D: an infinite plane perpendicular to the segment).
> - The smallest closed shape formed by these perpendicular lines (or planes in 3D) is the Wigner–Seitz unit cell.
> ([pdf](zotero://open-pdf/library/items/7GQA2R6H?page=5&annotation=68VRYCBB))

^d39aaa




