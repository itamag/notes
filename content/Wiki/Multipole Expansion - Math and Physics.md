
## Mathematical Formulation

This section focuses on the mathematical framework underlying multipole expansions without reference to physical interpretations. The core task is to rigorously define and analyze multipole expansions.

### Definitions and Theorems

### Multipole Expansion

>[!thm] Multipole Expansion  
>$$ \frac{1}{|\mathbf{r'} - \mathbf{r}|} = \frac{1}{r} \sum_{n=0}^\infty P_n(\mathbf{r} \cdot \mathbf{r'}) \left(\frac{r'}{r}\right)^n $$  
>^641d24

#### Explanation:
A multipole expansion is a mathematical series representing a function that depends on angles—usually the two angles used in the spherical coordinate system (the polar and azimuthal angles) for three-dimensional Euclidean space, $\mathbb{R}^3$. Multipole expansions are useful because, similar to Taylor series, oftentimes only the first few terms are needed to provide a good approximation of the original function. The function being expanded may be real- or complex-valued and is defined either on $\mathbb{R}^3$, or less often on $\mathbb{R}^n$ for some other $n$.

### Taylor Series Approach

>[!Proof]  
>$$ \frac{1}{|\mathbf{r'} - \mathbf{r}|} = \frac{1}{r} \sum_{n=0}^\infty P_n(\mathbf{r} \cdot \mathbf{r'}) \left(\frac{r'}{r}\right)^n $$  
>^641d24

---

## Physical Interpretation of Multipole Expansion

This section provides a physics-based explanation of multipole expansion, its implications, and applications in electromagnetic theory.

### Problem Formulation

In electromagnetism, especially in problems involving electric and magnetic fields, we often face the challenge of evaluating interactions between sources and points far from them. Multipole expansion formalizes how to approximate these interactions in such cases.

### Solving the Problem

The multipole expansion allows us to decompose the field into a series of simpler terms, each corresponding to a different multipole order.

- For example, the dipole term approximates the field from a collection of point charges as if they were concentrated at the dipole moment.
  
### Solution and Physical Implications

- **Electric Dipole**  
  $$ \varphi(r) = \frac{p \cdot \mathbf{r}}{r^3} $$  
  Where $p$ is the dipole moment. This approximation simplifies calculations of electric fields at points far from the dipole.

- **Magnetic Dipole**  
  $$ B(r) = \frac{3(\mathbf{m} \cdot \hat{r})\hat{r} - \mathbf{m}}{r^3} $$  
  Where $m$ is the magnetic dipole moment, providing insights into the magnetic field structure.

---

## Quadrupole Expansion

### Definitions and Theorems

>[!thm] Spherical Multipoles  
>$$ \frac{1}{|r - r'|} = \frac{1}{r_{>}} \sum_{l=0}^{\infty} \left(\frac{r_{<}}{r_{>}}\right)^l P_l(\hat{r} \cdot \hat{r}') $$  
>^0e35b5

#### Explanation:
A multipole expansion in this context represents interactions between points in space. In spherical multipole expansions, the terms of the series depend on the separation between points ($r$ and $r'$) and angular relationships between them, captured through Legendre polynomials and spherical harmonics.

### Taylor Series Approach

>[!def] Spherical Multipoles  
>$$ \frac{1}{|r - r'|} = \frac{1}{r_{>}} \sum_{l=0}^{\infty} \frac{4\pi}{2l+1} \left(\frac{r_{<}}{r_{>}}\right)^l Y_{lm}(\Omega) $$  
>^0e35b5

---

## Physics of Quadrupole Expansion

### Problem Formulation

When higher-order field interactions are considered, such as quadrupole moments, the mathematical framework expands the solutions to encompass more complex distribution of charge or current densities.

### Solving the Problem

The quadrupole expansion incorporates second-degree tensors, allowing for the analysis of symmetrical charge distributions beyond dipole contributions.

### Solution and Physical Implications

- **Electric Quadrupole**  
  $$ \varphi(r) = \frac{1}{2r^5} \sum_{i,j} r_i r_j Q_{ij} $$  
  Where $Q_{ij}$ is the quadrupole moment tensor, providing a deeper understanding of field behavior in regions far from the source.

---

## Magnetic Multipoles

### Definitions and Theorems

>[!thm] Magnetic Dipole  
>$$ m = \frac{1}{2c} \int (r' \times \mathbf{J}(r)) d^3r' $$  
>^641d24

### Dipole Vector Potential

>[!thm] Magnetic Dipole Vector Potential  
>$$ A(r) = \frac{\mathbf{m} \times \hat{r}}{r^2} $$  
>^641d24

---

## Physics of Magnetic Multipoles

### Problem Formulation

Magnetic multipole moments are crucial for understanding complex magnetic field distributions, especially in systems with non-uniform current densities or distributed magnetic sources.

### Solving the Problem

The solution leverages the cross-product integrals and tensor analysis to model the behavior of magnetic fields arising from distributed sources.

### Solution and Physical Implications

- **Magnetic Dipole**  
  $$ B(r) = \frac{3(\mathbf{m} \cdot \hat{r})\hat{r} - \mathbf{m}}{r^3} $$  
  This provides insights into how magnetic fields are oriented and how they decay with distance from the source.

---

This version integrates explanations along with the mathematical formulations for each section.
