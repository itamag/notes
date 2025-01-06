In quantum mechanics, we see early that the x-position of a system corresponds to the position operator $\mathbf{X}$

The position eigenbasis {|x,y,z⟩}, eigenvectors of Hermitian position X,Y,Z , is a complete basis for the Hilbert space of a 3-dimensional system, $\mathcal{H}_{\mathbf{r}}$, which can be considered as the tensor product of the three Hilbert spaces Hx⊗Hy⊗Hz, each of which is a L2(−∞,+∞) and is spanned by one of the {|x⟩, {|y⟩}, {|z⟩}.

From a general perspective, the three Cartesian coordinates are not the unique possible choice, and we could think to translate a position eigenket in spherical coordinates as:
$$\ket{x,y,z}\to \ket{r,\theta,\phi}$$
In this case, similarly, we **postulate** the existence of other three Hermitian operators R,Θ,Φ:
- commuting with one another,
- with spectra respectively $[0,\infty),[0,\pi],[0,2\pi],$
- with eigenbasis {|r⟩}, {|θ⟩}, {|ϕ⟩}, spanning respectively $L^2[0,∞), L^2[0,π], L^2[0,2π]$

The total Hilbert space now can be written as  $\mathcal{H}_{r}\otimes\mathcal{H}_{\theta}\otimes\mathcal{H}_{\phi}$, and $|r,\theta,\phi\rangle=|r\rangle\otimes|\theta\rangle\otimes|\phi\rangle$ is their simultaneous eigenvector with eigenvalues r, θ, ϕ.

Equivalently we can write $\ket{\mathbf{\hat{n}}} \equiv \ket{\theta} \otimes \ket{\phi}$.

# Connection to spherical harmonics & angular momentum

The operator $\mathbf{L}$ [[The QM Rotation Operator|is the generator of rotations]]. Therefore, we must have $\mathbf{L}\ket{r} = \ket{r}$. The angular momentum operator $\mathbf{L}$ is Hermitian and hence it defines an Eigenbasis over its Hilbert space. Thus we have two bases for $\mathcal{H}_{\theta}\otimes\mathcal{H}_{\phi}$: $\ket{\theta, \phi}$ and $\ket{l,m}$. Further we find:

$$\bra{\theta,\phi} \ket{l,m} = Y_{lm}(\theta,\phi)$$
Meaning the spherical harmonics are just the eigenfunctions of the angular momentum, in spherical coordinates.