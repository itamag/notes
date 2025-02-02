The Lienard-Wiechert potentials are the [[Maxwell Equations#Turning Maxwell's Equations into Potential Wave Equations|EM potentials]] of a point charge with known trajectory $\mathbf{w}(t)$. We then know:
$$\rho(\mathbf{r},t) =q\delta(\mathbf{r-w}(t))$$
And hence, using [[Maxwell Equations#Solving the Wave Equations using Green's Functions]]:
>[!thm] Lienard-Wiechert Potentials
> For a charged particle with charge $q$ and known trajectory $\mathbf{w}(t)$
> $$\varphi_{\mathrm{ret}}(\mathbf{r},t)={\frac{q}{[K]}}\;;\;\;\;\;\;\mathbf{A}_{\mathrm{ret}}(\mathbf{r},t)={\frac{q[{\boldsymbol{\beta}}]}{[K]}}\;;$$
> Where $[\cdot]$ denote the [[Retarded Time]], $\mathbf{\beta}\equiv \frac{\mathbf{\dot{w}}}{c}$ is the relative velocity of the particle and:$$K = \lVert \mathbf{R} \rVert - \mathbf{\beta}\cdot \mathbf{R}= \lVert \mathbf{R} \rVert\cdot(1-\mathbf{\beta \cdot \hat{R}})$$
> It is not obvious that indeed the potential we wrote are function of $\mathbf{r},t$ alone. Remember that retarded time bracket $[\cdot]$ parameterize/change variables from the "sender" frame $\mathbf{r'}, t'$ into the mixed frame $t'(\mathbf{r,r'},t),\mathbf{r'}$. In our case, $\mathbf{r'=r'}(t')$ and hence the brackets leave us with functions of the receiver frame $\mathbf{r},t$. 

How should we think of $K$? My take: in classical EM, charges are always charge distributions. Suppose a charge distribution is in the shape of a train. If it's moving towards the test charge (which is at rest), the train will seem elongated in the direction $\mathbf{\hat{R}}$, because the we will see the light from the engine at some past time $t'$ and the light from the back cart at some further past time $t'+\delta t'$. If the train is moving away, by the same effect it will appear shorter. See [[Doppler Effect]]. 

So, $K$ is the usual denominator as in the case of a static point charge, but the charge density is *larger (smaller) when the charge is moving away (towards) from the test charge*, and this relation is linear with the speed of the charge.

The EM field can be derived:
>[!thm]  Lienard-Wiechert EM Field
>The EM field of a moving point charge with trajectory $\mathbf{r'}(t')$, relative velocity $\mathbf{\beta}$ and acceleration $\mathbf{a}_{q}$ is:
> $$\mathbf{E}(\mathbf{r},t)=\underbrace{ q\left[{\frac{(1-\beta^{2})(\mathbf{R}-R\mathbf{\beta})}{K^{3}}}\right] }_{ \mathbf{E}_{v} }+\underbrace{ {\frac{q}{c^{2}}}\left[{\frac{\mathbf{R}\times\left((\mathbf{R}-R\mathbf{\beta})\times\mathbf{a}_{q}\right)}{K^{3}}}\right] }_{ \mathbf{E}_{a} }$$
> $$\mathbf{B}(\mathbf{r},t)=[{\widehat{\mathbf{R}}}]\times\mathbf{E}(\mathbf{r},t)=\underbrace{ [{\widehat{\mathbf{R}}}]\times\mathbf{E}_{v} }_{ \mathbf{B}_{v} }+\underbrace{ [{\widehat{\mathbf{R}}}]\times\mathbf{E}_{a} }_{ \mathbf{B}_{a} }$$

