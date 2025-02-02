This is under [[Maxwell Equations#Maxwell's Static Equations]]

[[Maxwell Equations|Maxwe'll Equation]] generally allow us to solve for the EM field, if we know the charge and current densities in a region of space, including the boundary of that region (which has a non-negligible effect on the EM field). 

If we know the densities and boundary conditions, we can solve using [[Maxwell Equations#Superposition Problems for Static Maxwell|Superposition]] or [[Maxwell Equations#Boundary Condition Problems|boundary condition formal approach]]. But what if we don't know the densities in the material? 

Another outlook: so far in [[EM]] we'd looked at conductors - there is no field inside the bulk matter. Now there will be.

>[!note] Intuition Recap by Me
>We want to understand the fields that will be generated in bulk matter when an external field is applied. 
>1. First hurdle: what's an external field? Even if we can generate some static field, once the charge in the material moves around due to it, the charge generating the applied field will move as well, so there isn't really a predetermined external field. *An external field will be defined as a field due to a charge distribution so far from the bulk matter, such that the bulk matter can't move it.* 
>2. Second hurdle: it's easy to see that a single bound charge / dipole will align/polarize with the total field it's subjected to. But once we talk about the total polarization aligning with the total field there's a problem. On the one hand, the polarization is depicted as a linear response to the total field, but on the other the polarization is part of the total field, so the polarization responds to itself?
>3. Third hurdle: in a similar manner, the magnetization $M$ is a linear response *but to *
>



# Detour Into Particle Physics
In dielectric materials, we will partition the charge density of the material to two contributions $\rho = \rho_{b}+ \rho_{f}$. The density $\rho_{b}$ is due to charges that are bound to atoms and cannot move much. The will be unaffected by external applied fields. However $\rho_{f}$ can be affected, such that the total field will be the applied field plus an induced, response field.

We can use the molecular description below to take $\rho_{b}$ out of the PDE.

The material is modeled as a collection of molecules. Let's look at one such molecule, which is a (known) discrete charge distribution. As we apply an external field, we can approximate the induced electrostatic field using [[Multipole Expansion]] dipole fields. So we can approximate the entire field in the material using a sum over these dipole fields:
$$\mathbf{P} = \sum_{\text{molecules}}\mathbf{p} \implies \nabla \cdot \mathbf{E}_\text{tot} = 4\pi[\rho_{f} - \nabla \cdot \mathbf{P}] = 4\pi \rho$$
$$\implies \nabla \cdot \underbrace{[\mathbf{E}_{\text{tot}}+4\pi \mathbf{P}]}_{\mathbf{D}} = \nabla \cdot \mathbf{D} = 4\pi \rho_{f}$$
$$\rho_{b} = -\nabla \cdot \mathbf{P}$$
# Return to Classical Continuous Description
The molecular detour allowed us to simplify the problem using an approximation, but not losing the niceties of the original PDE. 

In linear isotropic materials, we will drop the molecular computation of the total polarization $\mathbf{P}$ for a very simplifying assumption: **the polarization is a linear response to the total electric field in the material**. *Notice that that is a bit circular, because the polarization itself contributes to the total field*:

$$\mathbf{P} = \chi_{e}\mathbf{E}\implies D = (1+4\pi \chi)\mathbf{E}\equiv\epsilon \mathbf{E}$$
This further simplifies the problems, because now the original equation $\nabla \times \mathbf{E} = 0$ is equivalent to $\nabla \times \mathbf{D} = 0$. 

In a very similar manner we can work out the magnetic approximation:
$$\mathbf{M} = \chi_{M}\mathbf{H}$$
$$\mathbf{B} = \mathbf{H} + 4\pi \mathbf{M} = (1+4\pi \chi_{m})\mathbf{H}\equiv \mu \mathbf{H}$$
$$\mathbf{J}_{b} = c\cdot\nabla \times \mathbf{M}$$
>[!def] Paramagnets and Diamagnets
>Are both isotropic linear materials, differing by the sign of the susceptibility $\chi_{M}$. In paramagnets it is positive (the magnetization aligns with the free field), and diamagnets negative (the magnetization resists the free field).

And in total we get 

>[!thm] Maxwell's Static Equations in Dielectric Material
>$$\begin{gather}
>\nabla \cdot \mathbf{D} = 4\pi \rho_{f},\;\;\;\nabla \times \mathbf{E} = 0\\
>\nabla \cdot \mathbf{B} = 0,\;\;\;\;\;\;\; \nabla \times \mathbf{H} = \frac{4\pi}{c}\mathbf{J}_{f}
\end{gather}
>$$


# Boundary Conditions
>[!thm] Boundary Conditions for Dielectric Materials
>$$
>\begin{gather}
\mathbf{\hat{n}}\cdot(\mathbf{D_{2}-D_{1}}) = 4\pi\sigma_{f} \\
\mathbf{\hat{n}}\times(\mathbf{E_{2}-E_{1}}) = 0 \\
\mathbf{\hat{n}}\cdot(\mathbf{B_{2}-B_{1}}) = 0 \\
\mathbf{\hat{n}}\times(\mathbf{H_{2}-H_{1}}) = \frac{4\pi}{c}\mathbf{K}_{f}
\end{gather}
>$$
>Where $\mathbf{\hat{n}}$ is perpendicular to the boundary, and points from region $1\to 2$. Note that the LHS can be interpreted as the difference between the regions of the D components perpendicular to the boundary and the E components parallel to the boundary, respectively. By the same logic we get:
>$$\begin{gather}
>\mathbf{\hat{n}}\cdot(\mathbf{P_{2}-P_{1}}) = -\sigma_{b}\\
>\mathbf{\hat{n}}\times(\mathbf{M_{2}-M_{1}}) = \frac{1}{c}\mathbf{K}_{b}
\end{gather}$$

>[!warning] On the Notion of Applied Field
>The notion of applied field is misleading here. Rigorously, there is no applied field - just total field in a region of space. We can envision an applied field as a field generated by a charge distribution very far from the dielectric material. So mathematically, the applied field will usually just be a boundary condition - the total field very far from the free charge distribution.
# Return to the Poisson Equation and Statics

>[!warning]
>In statics we'll assume $\mathbf{J}=0 \implies \mathbf{J}_{f} = 0 \implies \mathbf{J}_{b} = 0$

We have received two decoupled [[Poisson Equation]]:
$$\begin{gather}
\nabla^2\psi_{D} = 4\pi \rho_{f};\;\;\;\mathbf{D} = -\nabla \psi_{D} \\
\nabla \times \mathbf{H} \implies \mathbf{H} = -\nabla \psi_{M} \implies \nabla^2\psi_{M} = -4\pi \cdot\underbrace{(-\nabla \cdot \mathbf{M})}_{\rho_{M}} = -4\pi \rho_{M}
\end{gather}$$
So now all of our discussion on solving this equation applies.

