>[!def] Bloch Electrons
>Independent electrons, each of which obeys a one electron[[Schordinger's Equation| Schrodinger equation]] with a periodic potential:
>$$H\psi=\left(-{\frac{\hbar^{2}}{2m}}\nabla^{2}\,+\,U({\bf r})\right)\psi=\varepsilon\psi,$$
>Are known as Bloch electrons 
>(Ashcroft and Mermin, 1976, p. 133)  [🔖](zotero://open-pdf/library/items/I2H7EZCQ?page=155&annotation=US3KW46R)

>[!thm] Bloch's Theorem and the Crystal Momentum
>The eigenstates $psi$ of the one-electron Hamiltonian  $H=-{\frac{\hbar^{2}}{2m}}\nabla^{2}\,+\,U({\bf r})$ where $U(r + R) = U(r)$ for all R in a Bravais lattice, can be chosen to have the form of a plane wave times a function with the periodicity of the Bravais lattice:
>$$\psi_{n\mathbf{k}}(\mathbf{r})\,=\,e^{i\mathbf{k}\,\cdot\,\mathbf{r}}u_{n\mathbf{k}}(\mathbf{r}) = e^{i\mathbf{k}\,\cdot\,\mathbf{r}}u_{n\mathbf{k}}(\mathbf{r}+\mathbf{R})$$
>Which implies:
>$$\psi_{n\mathbf{k}}(\mathbf{r+R})=e^{i\mathbf{k\cdot R}}\psi_{n\mathbf{k}}(\mathbf{r}).$$
>The index $\mathbf{k}$ will be called the crystal momentum (see [[#^3385ae]])

^07c023

>[!remark] The crystal momentum is NOT the electron's momentum
>While the Hamiltonian eigenstates are indexed by $n,\mathbf{k}$, these eigenstates are not eigenstates of the momentum operator, therefore don't even have a determinate momentum, let alone have that be $\mathbf{k}$.
>
>Further, the index $n$ does not indicate energy levels.
> [🔖](zotero://open-pdf/library/items/I2H7EZCQ?page=161&annotation=FZHIM3GZ)
^3385ae

# Allowed Crystal Momentum Values

THE BORN-VON KARMAN BOUNDARY CONDITION [🔖](zotero://open-pdf/library/items/I2H7EZCQ?page=157&annotation=MUP7JXQK)

The Born-von Karman conditions in this case would be:
$$\psi({\bf r\,+\,}N_{i}{\bf a}_{i})\,=\,\psi({\bf r}),\;\;\;\;\;\;i\,=\,1,2,3,$$
where the $a_{i}$ are three [[Crystal Lattice#^da77d0|primitive vectors]]  and the $N_i$ are all integers of order $N^{1/3}$, and $N=N_{1}N_{2}N_{3}$ is the total number of [[Crystal Lattice#^40cc76|primitive cells]]  in the crystal.

It follows that the general form for allowed Bloch wave vectors is\Therefore the general form for allowed Bloch wave vectors is:
$$\mathbf{k}\,=\,\sum_{i\,=\,1}^{3}\,{\frac{m_{i}}{N_{i}}}\,\mathbf{b}_{i},\qquad m_{i}\;\mathrm{integral}$$
And Hence the volume of $\mathbf{k}$-space per allowed momentum value:
$$\Delta{\bf k}=\frac{{\bf b}_{1}}{N_{1}}\,\cdot\,\left(\frac{{\bf b}_{2}}{N_{2}}\times\frac{{\bf b}_{3}}{N_{3}}\right)=\frac{1}{N}\,{\bf b}_{1}\,\cdot\,({\bf b}_{2}\,\times\,{\bf b}_{3}).$$
And hence **the number of allowed wave-vectors in a unit cell of the [[Reciprocal Lattice]] is the number of sites of the crystal**.

Further by using [[Reciprocal Lattice#^d4406d]] :
$$\Delta\mathbf{k}\,=\,\frac{(2\pi)^{3}}{V}.$$
Which is the same result as in the [[Model of Conduction#Drude-Sommerfeld|free electron case]] found in [[SS HW 4]].

# Implications

>[!def] Band Structure of a Solid
We can choose the indices such that (using the periodicity of the lattice):
$$\begin{array}{c}{{\psi_{n,\,\mathbf{k}+\mathbf{k}}(\mathbf{r})\,=\,\psi_{n\mathbf{k}}(\mathbf{r}),}}\\ {{\xi_{n,\,\mathbf{k}+\mathbf{k}}\,=\,\xi_{n\mathbf{k}}.}}\end{array}$$
> $\xi_{n}(\mathbf{k}+\mathbf{k})$ will be called the band structure of the solid

>[!thm] Mean Velocity of Bloch Electron
>$$\mathbf{v}_{n}(\mathbf{k})={\frac{1}{h}}\,\mathbf{V}_{\mathbf{k}}\,\,\mathbf{\xi}_{n}(\mathbf{k}).$$
>[🔖](zotero://open-pdf/library/items/I2H7EZCQ?page=163&annotation=I75G6J53)


# Electrons in a Weak Periodic Potential

From the periodicity of the potential and the wavefunction, the wavefunction can be expanded as a Fourier series abiding. Then, Shcrodinger's equation in k-space becomes:

$$\left[\frac{h^{2}}{2m}({\bf k-K})^{2}\,-\,\varepsilon\right]c_{{\bf k}-{\bf K}}+\sum_{\bf K^{\prime}}U_{{\bf K}^{\prime}-{\mathbf{K}}}\cdot c_{{\bf k}-{\bf K^{\prime}}}=0$$
Where $\mathbf{k}$ is any vector in the first [[Reciprocal Lattice#BRILLOUIN Zone]] , and $\mathbf{K,K'}$ iterate over the reciprocal lattice. Notice that in the above equation, $\varepsilon$ and $c_{\mathbf{k-K}}$ are undetermined. 

Bloch's theorem specifies a form for the eigensolutions of the Schrodinger equation, but doesn't solve it per se. We'd like to solve further in the special case of a weak potential, using [[Perturbation Theory]]. 

In that case, our solution would be close to a free electron ([[Model of Conduction#Drude-Sommerfeld]]). For a free electron, $U\equiv{0}$ and there'd exist some subset $\mathbf{\tilde{K}} \subset \mathbf{K}$ such that for all $\mathbf{\tilde{k}} \in \mathbf{\tilde{K}}$:
$$\varepsilon = \varepsilon_{\mathbf{k-\tilde{k}}}^0\equiv \frac{\hbar^2}{2m}(\mathbf{k-\tilde{k}})^2$$
And for all other $\mathbf{k'}$:
$$c_{\mathbf{k-k'}} = 0$$

For a nearly free electron, i.e. a weak periodic potential, we'll divide the energy eigenbasis to nearly degenerate part $\mathbf{\tilde{K}}$, and the rest:

$$\left|\varepsilon_{\mathrm{k-\tilde{k}_{1}}}^{0}-\,\varepsilon_{\mathrm{k-\tilde{k}_{2}}}^{0}\right| = \begin{cases}
\sim U & \mathbf{k_{1},k_{2} \in \tilde{K}} \\
\gg U  & \mathbf{k_{1} \in \tilde{K}, k_{2} \notin \tilde{K}}
\end{cases}$$
Which gives the approximation:
$$c_{{\bf k}-{\bf K}}={\frac{1}{\varepsilon-\varepsilon_{{\bf k}-{\bf K}}^{0}}}\sum_{\mathbf{\tilde{k}}}\,U_{{\bf \tilde{k}}-{\bf k}}c_{{\bf k}-{\bf \tilde{k}}}+\,O(U^{2}).$$
And the energy level approximation:
$$\varepsilon(\mathbf{k-k'}) = \varepsilon_{\mathbf{k-k'}}^0 + \frac{1}{c_{\mathbf{k-k'}}}\big[\sum_{\mathbf{\tilde{k}}}U_{\mathbf{\tilde{k}-k'}}\cdot c_{\mathbf{k-\tilde{k}}} + \sum_{\mathbf{\tilde{k}}}\sum_{\mathbf{k}''}\frac{U_{\mathbf{k''-k'}}\cdot U_{\mathbf{\tilde{k}-k''}}}{\varepsilon - \varepsilon_{\mathbf{k-k'}}^0}\cdot c_{\mathbf{k-\tilde{k}}} \big] + O(U^3)$$

In the *no degeneracy* case $\lvert \mathbf{\tilde{K}} \rvert = 1$, we get the less tedious:
$$\mathcal{E}\,=\,\mathcal{E}_{\mathbf{k}-\mathbf{k}_{1}}^{0}+\,\sum_{\mathbf{K}}\frac{\left|U_{\mathbf{k}-\mathbf{k}_{1}}\right|^{2}}{\mathcal{E}_{\mathbf{k}-\mathbf{k}_{1}}^{0}-\,\mathcal{E}_{\mathbf{k}-\mathbf{k}}^{0}}\,+\,O(U^{3}).$$
Notice that in the degenerate case, we get a linear correction, whereas in the nondegenerate case the correction is of order 2.

>[!thm] Recitatino formula
>$$\varepsilon(\mathbf{k})=\varepsilon_{0}(\mathbf{k})+\sum_{\mathbf{k}^{\prime}\neq\mathbf{k}}{\frac{\left|\langle\mathbf{k}^{\prime}|V|\mathbf{k}\rangle\right|^{2}}{\varepsilon_{0}(\mathbf{k})-\varepsilon_{0}(\mathbf{k}^{\prime})}}\underset{\uparrow}{=}\varepsilon_{0}(\mathbf{k})+\sum_{\mathbf{G}\neq0}{\frac{\left|V_{\mathbf{G}}\right|^{2}}{\varepsilon_{0}(\mathbf{k})-\varepsilon_{0}(\mathbf{k}+\mathbf{G})}}$$
>$$|\varepsilon_{0}({\bf k})-\varepsilon_{0}({\bf k}+{\bf G})|\,\gg\,|V_{\bf G}|$$

# Electrons in Weak Potential - My explanation

We can represent the above Schrodinger equation in the $\mathbf{k}$ basis presented by [[#^07c023]]. Indeed, setting $\bra{\mathbf{r}}\ket{\mathbf{k}}\equiv e^{i\mathbf{k\cdot r}}$ we see:
$$\bra{\mathbf{k}} H\ket{\mathbf{k'}} = \frac{\hbar^2}{2m}\mathbf{k}^2\delta_{\mathbf{k,k'}} - \varepsilon + \bra{\mathbf{k-k'}} \ket{U} $$
$$\int_{k'}\bra{k} H\ket{k'} \bra{k'} \ket{\psi} = \varepsilon \ket{\psi}$$
But we know from the periodicity, that (letting $G$ the reciprocal lattice and $Q$ the allowed crystal wavevectors):
$$\begin{gathered}
\bra{k-k'} \ket{U}  = \bra{k-k'} \ket{U} \cdot \delta_{k-k' \in G} \\
\bra{k'} \ket{\psi}  = \bra{k'} \ket{\psi} \cdot \delta_{k' \in Q}
\end{gathered}$$
Then fixing $\mathbf{q} \in Q$, we get a countable matrix equation indexed by $G$:
$$[\underbrace{\frac{\hbar^2}{2m}(\mathbf{q-k})^2\cdot\delta_{\mathbf{k,k'}}}_{\mathcal{E}^{0}}  - \varepsilon + \mathcal{U}]\vec{v} = \vec{0}$$
Where:
$$\begin{gathered}
\vec{v}_{\mathbf{k}} = \bra{\mathbf{q-k}}\ket{\psi} \\
\mathcal{U}_{\mathbf{k,k'}} = \bra{\mathbf{q-k}} \ket{\psi} 
\end{gathered}$$
$\mathcal{E}^0$ is the free electron approximation energy (i.e. kinetic energy), and it's already diagonal.

Fix some $\mathbf{k_{0}} \in G$, and decompose $G$ into two subsets $G_{1},G_{2},\mathbf{k_{0}}\in G_{1}$ such that:
$$\begin{align}
\{\mathbf{k_{1},k_{2}}\}  & \subset G_{1} \implies \lvert \mathcal{E}^0_{\mathbf{k_{1},k_{1}}} - \mathcal{E}^0_{\mathbf{k_{2},k_{2}}} \rvert \sim U  \\
 & \not\subset G_{1} \implies\lvert \mathcal{E}^0_{\mathbf{k_{1},k_{1}}} - \mathcal{E}^0_{\mathbf{k_{2},k_{2}}} \rvert \gg U  \\
\end{align}$$
Then decomposing $\mathcal{U = U^{(1)} + U^{(2)}}, \mathcal{U}^{(i)}_{\mathbf{k_{1},k_{2}}} = \mathcal{U}_{\mathbf{k_{1},k_{2}}}\cdot\delta_{\mathbf{k_{2}} \in G_{i}}$ we see (algebra):
$$
(\varepsilon - \mathcal{E^0})v = [\mathcal{U}^{(1)} + \mathcal{U}^{(2)}(\varepsilon - \mathcal{E^0})^{-1}\mathcal{U}^{(1)}]v + O(U^3)
$$
Now, let's look at the row $\mathbf{k_{0}}$ in the above expression. If $\lvert G_{1} \rvert = 1$, i.e. the value $\mathcal{E}^{0}_{\mathbf{k_{0},k_{0}}}$ is unique in $\mathcal{E}^0$ compared with the scale of $U$, then:
$$[\mathcal{U^{(1)}}v]_{\mathbf{k_{0}}} = \mathcal{U}_{\mathbf{k_{0},k_{0}}}v_{\mathbf{k_{0}}} = \bra{\mathbf{0}} \ket{U} \cdot v_{\mathbf{k_{0}}} = 0  $$
Without loss of generality assuming $\bra{\mathbf{0}}\ket{U}=0$. In words, in the case that the kinetic energy is not unique, the correction is linear whereas if it is unique, the correction is of order $U^2$.















If there exists a subset $S \subset \mathbf{G}$ such that:
$$\begin{gathered}
i,j \in S \implies D \sim \mathcal{U} \\
i,j \not\in S \implies D \gg \mathcal{U}
\end{gathered}$$
Then we can set:
$$\mathcal{U} = \mathcal{U}\cdot \mathbb{1}_{S} + \mathcal{U} \cdot \mathbb{1}_{S^c} \equiv \mathcal{U}_{1} + \mathcal{U}_{2}$$
And it follows:
$$D^{-1}\mathcal{U} \approx D^{-1}\mathcal{U}_{1}$$
$$\tilde{\psi} = D^{-1}\mathcal{U}_{1} \tilde{\psi} + O(U^2)$$
Hence:
$$D \tilde{\psi} = \mathcal{U} \; \tilde{\psi} = (\mathcal{U}_{1} + \mathcal{U}_{2}D^{-1}\mathcal{U}_{1})\tilde{\psi} + O(U^3)$$
In our case, we will choose $\varepsilon = \mathcal{E}_{\mathbf{k}_{0}}$ for some $\mathbf{k}_{0}$. Thus, $(\mathbf{k}_{0}, \mathbf{k}_{0}) \in S$. Wlog we can assume $\bra{\mathbf{0}}\ket{U}=0$ and hence $[\mathcal{U}_{1}]_{\mathbf{k}_{0}, \mathbf{k}_{0}}= 0$. If this is the only item in $S$ we get:

$$D \tilde{\psi} = \mathcal{U} \; \tilde{\psi} = \mathcal{U}_{2}D^{-1}\mathcal{U}_{1}\tilde{\psi} + O(U^3)$$