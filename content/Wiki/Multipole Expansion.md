# Quick Summary
“תרגול 6” ([pdf](zotero://open-pdf/library/items/6LMJTUM7?page=1&annotation=N6KZHTBK))
# Premise
Main idea: far from a charge distribution, the electric field will approximately seem like that of a point charge $$\psi \approx \frac{Q}{r}$$
Let's be exact. In the above example, for each point $\mathbf{r'}$ of the charge distribution, we approximated $\frac{1}{|\mathbf{r'} - \mathbf{r}|} \approx \frac{1}{|\mathbf{r}|}$, i.e. the distribution is approximately a point charge at the axis origin. 

We can go further: for each point $\mathbf{r'}$ of the charge distribution, approximate its distance from a far point $\mathbf{r}$ using a Taylor series:

>[!thm] Multipole Expansion
>$$
\begin{aligned}
\frac{1}{|\mathbf{r'}-\mathbf{r|}}  = \frac{1}{r}\sum_{n=0}^\infty P_{n}(\mathbf{r}\cdot \mathbf{r'})\left( \frac{r'}{r} \right)^n
\end{aligned}$$

^641d24

>[!Proof]-
> `\begin{proof}`
> $$\begin{aligned}
> \frac{1}{|\mathbf{r'}-\mathbf{r|}}  & = \frac{1}{\sqrt{ {r^2 + (r')^2 - 2\mathbf{r}\cdot \mathbf{r'}} }} = \frac{1}{r} \cdot \frac{1}{\sqrt{ 1+\left( \frac{r'}{r} \right)^2 - 2\left( \frac{r'}{r} \right)\;\mathbf{\hat{r}}\cdot \mathbf{\hat{r}} }} \\
>  & ={\frac{1}{r}}\left\{1+{\frac{r^{\prime}}{r}}\left({\hat{\boldsymbol{r}}}\cdot{\hat{\boldsymbol{r}}}^{\prime}\right)+\left({\frac{r^{\prime}}{r}}\right)^{2}\left[{\frac{3}{2}}\left({\hat{\boldsymbol{r}}}\cdot{\hat{\boldsymbol{r}}}^{\prime}\right)-{\frac{1}{2}}\right]+\left({\frac{r^{\prime}}{r}}\right)^{3}\left[{\frac{5}{2}}\left({\hat{\boldsymbol{r}}}\cdot{\hat{\boldsymbol{r}}}^{\prime}\right)^{3}-{\frac{3}{2}}\left({\hat{\boldsymbol{r}}}\cdot{\hat{\boldsymbol{r}}}^{\prime}\right)\right]+\ldots\right\} \\
>  & \frac={1}{r}\sum_{n=0}^\infty P_{n}(\mathbf{r}\cdot \mathbf{r'})\left( \frac{r'}{r} \right)^n
> \end{aligned}$$
> 
> `\end{proof}`

This approximation can be applied when calculating either magnetic or electric fields in [[Maxwell Equations#Superposition Problems for Static Maxwell]].

>[!thm] Multiple Expansion of Electric Field
>$$\begin{aligned} \\
\varphi\left({\boldsymbol{r}}\right) & =\sum_{n=0}^{\infty}{\frac{1}{r^{n+1}}}\int\left({\boldsymbol{r}}^{\prime}\right)^{n}P_{n}\left({\hat{\boldsymbol{r}}}\cdot{\hat{\boldsymbol{r}}}^{\prime}\right)\rho\left({\boldsymbol{r}}^{\prime}\right)d^{3}r^{\prime} \\
 & ={\frac{1}{r}}{\int}\rho\left({\boldsymbol{r}}^{\prime}\right)d^{3}r^{\prime}+{\frac{1}{r^{2}}}\int r^{\prime}\left({\hat{\boldsymbol{r}}}\cdot{\hat{\boldsymbol{r}}}^{\prime}\right)\rho\left({\boldsymbol{r}}^{\prime}\right)d^{3}r^{\prime}+{\frac{1}{r^{3}}}\int\left({\boldsymbol{r}}^{\prime}\right)^{2}\left[{\frac{3}{2}}\left({\hat{\boldsymbol{r}}}\cdot{\hat{\boldsymbol{r}}}^{\prime}\right)^{2}-{\frac{1}{2}}\right]\rho\left({\boldsymbol{r}}^{\prime}\right)d^{3}r^{\prime}+\ldots
\end{aligned}$$
^facfa1

>[!remark] The role of the multipole moment in multipole expansion
>In the above formula [[#^facfa1]] , the integral mixes $\mathbf{r'}$, which is integrated, and $\mathbf{r}$ which is not. We open the dot products element-wise, and take the $r_i$ components out of the integral. For the n-th item in the multipole expansion, we'll be left with a n-form $r_{i_{1}\dots}r_{i_{n}}Q^{{i_{1}\dots}{i_{n}}}$. where $Q$ is a tensor that does not depend on $\mathbf{r}$. Q will be the multipole n-th moment


>[!example]- Electric Dipole
>![[Pasted image 20241216171602.png]]
>$$\varphi\left(r\right)={\frac{q d\cos\theta}{r^{2}}}$$
^2e1e55

# Spherical Multipoles

The Taylor series in [[#^641d24]]  is not everywhere convergent. We can have two series for two zones: $r'<r$ and $r' > r$. Physically, we may be very far from a charge, or inside a very large charge. In each series, we'll build the power series s.t the bigger one will be in the denominator (so that the $\frac{r_{1}}{r_{2}}<1$):

>[!def] Spherical Multipoles
>$$\frac{1}{\vert r-r^{\prime}\vert}=\frac{1}{r_{>}}\sum_{l=0}^{\infty}\left(\frac{r_{<}}{r_{>}}\right)^{l}P_{l}\left(\hat{r}\cdot\hat{r}^{\prime}\right)$$
>Where:
>$$\cdot\left\{{r_{>}}=\operatorname*{max}\left(r,r^{\prime}\right)\right.$$

By [[Spherical Harmonics#^0e35b5]] :

>[!thm] Equivalent definition of spherical multipole
>$$\frac{1}{\vert r-r^{\prime}\vert}=\frac{1}{r_{>}}\sum_{l=0}^{\infty}\frac{4\pi}{2l+1}\left(\frac{r_{<}}{r_{>}}\right)^{l}\sum_{m=-l}^{l}Y_{l m}^{*}\left(\Omega_{<}\right)Y_{l m}\left(\Omega_{>}\right)$$


# Dipole Quirks
$$\varphi_{d i p}\left(r\right)=\frac{1}{r^{2}}\hat{r}\cdot\underbrace{\int \mathbf{r^{\prime}}\rho\left(r^{\prime}\right)d^{3}r^{\prime}}_{p} = \frac{\mathbf{p}\cdot \mathbf{r}}{r^3}$$
Where the new $p$ is aptly named the Dipole moment.

>[!exr] List of Dipole moments:
>Point charges:
>$$\mathbf{p} = \sum_{i}q_{i}\mathbf{r}_{i}$$

## The Electric Dipole

Seeing [[#^facfa1]]: 

$$E_{d i p}\left(r\right)=-\nabla\left({\frac{p\cdot r}{r^{3}}}\right)=-{\frac{1}{r^{3}}}\underbrace{\nabla\left(p\cdot r\right)}_{p}-\left(p\cdot r\right){\nabla\left({\frac{1}{r^{3}}}\right)}={\frac{1}{r^{3}}}\left[3\left(p\cdot r\right){\hat{r}}-p\right]$$

>[!exr] List of Electric Dipole fields:
>For $\mathbf{p} = p\hat{\mathbf{z}}$:
>$$E\left(r,\theta,\phi\right)={\frac{p}{r^{3}}}\left(2\cos\theta{\hat{r}}+\sin\theta{\hat{\theta}}\right)$$

# Quadrupole Quirks

$$\varphi_{q u a d}\left(r\right)=\frac{1}{2r^{5}}\sum_{i,j}r_{i}r_{j}\underbrace{\int\left[3r_{i}^{\prime}r_{j}^{\prime}-\left(r^{\prime}\right)^{2}\delta_{i j}\right]\rho\left(r^{\prime}\right)d^{3}r^{\prime}}_{Q_{i j}} = \frac{1}{2r^5}\bra{\mathbf{r}}Q\ket{\mathbf{r}}  $$
$Q_{ij}$ is the quadrupole moment - a symmetric 2-degree [[Tensor Analysis|tensor]].

## The Electric Quadrupole
>[!example] Coupled Electric Dipoles
![[Pasted image 20241216175201.png]]
>Solving in cartesian coordinates:
$$Q=\left(\begin{array}{c c c}{{-2}}&{{0}}&{{0}}\\ {{0}}&{{-2}}&{{0}}\\ {{0}}&{{0}}&{{-2}}\end{array}\right)q d^{2}$$
And in spherical:
$$\varphi_{\text{quad}}(\mathbf{r})=q d^{2}{\frac{2\cos^{2}\theta-\sin^{2}\theta}{r^{3}}}$$
([pdf](zotero://open-pdf/library/items/S8BHCP57?page=18&annotation=EJ9P6QEU))


# Magnetic Multipoles

From [[#^641d24]]:

>[!thm] Magnetic Dipole
>The magnetic dipole moment is:
>$$m=\frac{1}{2c}\int\left(r^{\prime}\times\mathbf{J}\left(r\right)\right)d^{3}r^{\prime}$$
>And the dipole vector potential:
>$$A_{d i p}\left(r\right)=\frac{m\times r}{r^{3}}=\frac{m\times\hat{r}}{r^{2}}$$
>B-field:
>$$B_{d i p}\left(r\right)=\nabla\times A_{d i p}\left(r\right)=\frac{3\left(m\cdot\hat{r}\right)\hat{r}-m}{r^{3}}$$
>“מומנט הדיפול המגנטי” ([pdf](zotero://open-pdf/library/items/S8BHCP57?page=20&annotation=FIA4PVQL))
