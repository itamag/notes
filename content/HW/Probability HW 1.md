First let's state:
> [!thm] Jensen's Inequality
> Let (Ω,A,P) be a probability space. Let f:Ω→R be a P-measurable, integrable function and φ:R→R be convex. Then: $$\varphi\left(\int_{\Omega}f\,\mathrm{d}P\right)\leq\int_{\Omega}\varphi\circ f\,\mathrm{d}P$$

Now, assume the $k$-th moment $\mathbb{E}[X^k]$ exists and $k>1$. Then $X^k$ is measurable and integrable. Further we see:
$$X^k = (X^{k-1})^{\frac{k}{k-1}}$$