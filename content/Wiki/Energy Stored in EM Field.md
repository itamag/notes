# Electrostatic Energy of EM Field
From [[Hamilton's Principle for the EM Field#^93d106]]  we define the E-field contribution as the electrostatic energy:

$$U=\frac{1}{8\pi}\int E^{2}d V$$

If the charge distribution is finite:
$$U=\frac12\int\rho\varphi d V=\frac12\int\frac{\rho\left(r\right)\rho\left(r^{\prime}\right)}{\left|r-r^{\prime}\right|}d^{3}r d^{3}r^{\prime}$$

>[!warning]
>One must be careful with the domain of integration when using the [[Method of Image Charges]] to compute the electrostatic energy.

# Energy of General EM Field
The derivation will be shown for a [[Electrodynamics in Dielectric Material|linear material]] but $\mathbf{D,H}$ can be replace with $\mathbf{E,B}$. The density of energy stored in the EM field:
>[!thm] Energy *Stored* in EM Field
$$u = \frac{1}{8\pi}\cdot(\mathbf{E\cdot D + B\cdot H} ),\;\;\;U = \int u\cdot d^3\mathbf{r'}$$

^fe4eac

# Energy of Charge Distribution in EM Field
Confusion: the energy of a charge distribution <u>under an external field</u> is said to be:

$$U=\int\rho\left({\boldsymbol{r}}\right)\phi\left({\boldsymbol{r}}\right)d^{3}r$$
Which yields in [[Multipole Expansion]]:

$$U=Q\phi\left(0\right)-{\boldsymbol{p}}\cdot{\boldsymbol{E}}\left(0\right)-{\frac{1}{6}}\sum_{i,j}Q_{i j}{\frac{\partial E_{j}}{\partial r_{i}}}\left(0\right)+\ldots$$
So the energy is approximately a sum involving the monopole, dipole and quadrupole. Intuitively, the dipole interacts with the E-field, and the quadrupole interacts with the E-field gradient. Further, the energy is minimal when the dipole is aligned with the electric field at the origin. If we're dealing with [[Maxwell Equations#Maxwell's Static Equations|static magnetic field]]:

$$\mathbf{F} = -\vec{\nabla}U = \cdots = (\mathbf{p}\cdot \vec{\nabla})\cdot \mathbf{E}\rvert_{\mathbf{0}}$$
Physical takeaway: in statics, we can have a torque on the dipole (because it will rotate to match the E-field direction), but its COM will not move unless we have a changing E-field.

“אנרגיה של התפלגות מטען סופית בשדה חיצוני” ([pdf](zotero://open-pdf/library/items/S8BHCP57?page=19&annotation=XYAKRRYJ))