If we have a linear differential operator $L$ and we'd like to solve $Ly(\mathbf{x}) = f(\mathbf{x})$. We can try and solve: 

$$LG(\mathbf{x},\mathbf{x'}) = \delta(\mathbf{x-x'})$$

Which yields:
$$f(\mathbf{x}) = \int f(\mathbf{x'})G(\mathbf{x},\mathbf{x'})d^D\mathbf{x'}$$
Because indeed:
$$L\int f(\mathbf{x'})G(\mathbf{x},\mathbf{x'})d^D\mathbf{x'} \stackrel{(*)}{=} \int f(\mathbf{x'})\delta(\mathbf{x-x'})d^D\mathbf{x'} = f(\mathbf{x})$$
Where we used the fact the $L$ is a differential operator only on the coordinate vector $\mathbf{x}$.

----
Thinking about this another way, say $L$ is a differential operator over a Hilbert  space $H$. In a sense $\delta(\mathbf{r-r'})$ is the position-basis representation of the identity operator:
$$\bra{\mathbf{r}} \ket{\psi}  = \psi(\mathbf{r}) = \int d^3\mathbf{r'}\delta(\mathbf{r-r'})\cdot\psi(\mathbf{r'}) = \int d^3\mathbf{r'}\bra{\mathbf{r}}I\ket{\mathbf{r'}}\bra{\mathbf{r'}} \ket{\psi}   $$
And so our original equation $LG(\mathbf{r,r'})=\delta(\mathbf{r-r'})$ is actually:
$$\bra{\mathbf{r}} \hat{L}\hat{G}\ket{\mathbf{r'}} = \bra{\mathbf{r}} I\ket{\mathbf{r'}} \iff \hat{L}\hat{G}=I $$
*Green's function is the (generalized) right inverse operator to L, presented in the position basis*. Then we can solve for any function:
$$L\psi(\mathbf{r}) = f(\mathbf{r}) \implies \psi(\mathbf{r}) = \bra{\mathbf{r}} \ket{\psi} = \bra{\mathbf{r}} G\ket{f} =  \int d^3\mathbf{r'}G(\mathbf{r},\mathbf{r'})f(\mathbf{r'})$$
*The Green's function/operator isn't necessarily unique. If we impose boundary conditions, some of the Green's functions may be disqualified as solutio.*
# Specific Green's Functions
>[!thm] Green's Function for the Wave Equation
>$$G(\mathbf{r},\mathbf{r'},t,t') = G(\underbrace{ \mathbf{r-r'} }_{ \mathbf{R} },\underbrace{ t-t' }_{ T }) = G^{\begin{pmatrix}
\text{retarded} \\
\text{advanced}
\end{pmatrix}} (\mathbf{R},T) = G^{(\pm)}(\mathbf{R}, T) = \frac{\delta\left( \frac{R}{c}\mp T \right)}{R}$$
>By ([pdf](zotero://open-pdf/library/items/SUG5UC6E?page=8&annotation=LNX768L7))
^011885

>[!thm] Green's Function for the [[Poisson Equation]]
> $$G(\mathbf{r,r'}) = G(\underbrace{ \mathbf{r-r'} }_{ \mathbf{R} }) = \frac{\delta(\mathbf{R})}{R}$$



*All of the below are linear differential operators. Thus they are translation invariant and the Green's function $G(\mathbf{r,r'})$ is a function only of the displacement $G=G(\mathbf{r-r'})$. In the below results, the coordinates describe the vector $\mathbf{x\equiv r-r'}$*.

| Name             | Differential Operator                                                                                | Green's Operator                                                 |
| ---------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| 3D Wave Equation | $\square=\frac{1}{c^{2}}\partial_{t}^{2}-\nabla_{\mathrm{3D}}^{2}$                                   | $-\frac{1}{4\pi}\frac{\delta\left( \frac{r}{c}\mp t \right)}{r}$ |
| 2D Laplace       | $\nabla^2_{\text{2D}} = \frac{ \partial ^2 }{ \partial x^2 } + \frac{ \partial ^2 }{ \partial y^2 }$ | $\frac{1}{2\pi}\ln \rho$                                         |
| Poisson Equation | $\nabla^2_{\text{3D}}$                                                                               | $-\frac{1}{4\pi r}$                                              |

