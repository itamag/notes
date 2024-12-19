# In a Nutshell

[1] Tensors are a generalization of vector fields. Given a manifold $M$, a vector field is a function assigning an element of the tangent space $T_p$ to each point $P \in M$. [2 Charts and Bases] If we define a coordinates chart $x^i$ of the tangent space at $P$, then the basis vectors are $\vec{e}_{i} = \frac{\partial\vec{s}}{\partial x^i}$, from which the dual basis $\vec{e}^i$ can be found using $\vec{e}^i \cdot \vec{e}_{j} = g^i_{j}$. [3 Coordinate Transformation] If we change the coordinates at $P$, then the vector field will not change, *but its (indexed) components will change* as:
> [!theorem]- Vector Field Components Coordinate Transformation
> 
> $$\begin{array}{r c l}{{A^{\prime\mu}}}&{{=}}&{{\displaystyle{\vec{e\prime}}^{\mu}\cdot{\vec{A}}}}\\ {{}}&{{=}}&{{\displaystyle{\frac{\partial x^{\prime\mu}}{\partial x^{\nu}}}{\bar{e}}^{\nu}\cdot{\vec{A}}}}\\ {{}}&{{=}}&{{\displaystyle{\frac{\partial x^{\prime\mu}}{\partial x^{\nu}}}{A}^{\nu}}}\end{array}$$

>[!theorem]- Tangent Space Basis Coordinate transformation
>$$\vec{e}'_{\nu}=\frac{\partial x^{\mu}}{\partial x^{\prime\nu}}\vec{e}_{\mu}\;\;;\;\;{\vec{e^{\prime}}}^{\nu}={\frac{\partial x^{\mu}}{\partial x^{\prime\nu}}}{\vec{e}^{\mu}}$$
>Proof:
>$$d\vec{s}=d x^{\mu}\vec{e}_{\mu}=d x^{\prime\mu}\vec{e^{\prime}}_{\mu} \rightarrow d x^{\mu}={\frac{\partial x^{\mu}}{\partial x^{\prime\nu}}}d x^{\prime\nu} \rightarrow d x^{\prime\nu}\left(\vec{e^{\prime}}_{\nu}-\frac{\partial x^{\mu}}{\partial x^{\prime\nu}}\vec{e}_{\mu}\right)=0$$



$$d s^{2}=g_{\mu\nu}d x^{\mu}d x^{\nu}$$
$$d\vec{s}=d x^{\mu}\vec{e}_{\mu} \;\;\;\rightarrow \;\;\;\vec{e}_{\mu}\equiv\operatorname*{lim}_{\Delta x^{\mu}\rightarrow0}\frac{\Delta\vec{s}}{\Delta x^{\mu}}\equiv\frac{\partial\vec{s}}{\partial x^{\mu}}$$

$$,$$

# Indexology
$$
\epsilon^{klm}\epsilon_{k\ln} = 2\delta^m_{n}
$$

>[!thm] The product of an antisymmetric and symmetric tensors is zero
>$$
>A_{[i_{1}\dots i_{n}]i_{n+1}\dots}\cdot B^{\{{i_{1}\dots i_{n}}\}i_{n+1}\dots} = 0
>$$

^1fff98

# Derivative-ology

>[!thm] Div curl is always zero
>$\nabla \cdot(\nabla \times X)=0$

^a2c75f

>[!thm] Integral theorems of the exterior product

^fd1ddd

