
[[Vershynin-a|Vershynin Prob Book - High Dimensional Probability]]
## Preliminaries %% fold %%
- Reference - Vershimyn - High Dimensional Probability
	- vasserman - all of statistics
	- end of course - terry tao - topics in random matrix theory
- HW
	- not every week
	- deadline arent set in stone I can ask for more time

## Background %% fold %%

- bayes formula

> [!lemma] Inequalities
> markov, chebyshev inequalities. For positive r.v.: $E[X] \geq a \cdot P(X \geq a)$. Chebyshev: for r.v. with finite expectation $\mu$ and nonvanishing variance:
> Generalized Chebyshev (the higher our moments, the closer the PDF to the expectation) ![[Pasted image 20241111165732.png]]
> Moment generating function: When all of the moments of a r.v. $X$ are well defined, we will say $X$ has a MGF if the following function is finite on a set $[-s_0, s_0]$: $$	M_{X}(s) = E[e^{sX}]$$


> [!lemma] If for a r.v. the $k$-th moment exists, then the moment $1,\dots,k$ exists


> [!claim] Claim: if the MGF exists, then all the moments exist
> ![[Pasted image 20241111181614.png]]


>[!claim] The Taylor coefficients of the MFG are the r.v. moments
>$$E[X^n]=M_{X}^{(n)}(0)$$

>[!claim] If an r.v. has MGF, then the PDF decays exponentially (iff TBD)
>$P(X \geq t) = P(e^{sX} \geq e^{st}) \leq [Markov] \leq \inf_{s} \frac{E[e^{sX}]}{e^{st}} = \inf_{s} M_{X}(s)\cdot e^{-st}$

>[!theorem] Law of Large Numbers
![[Pasted image 20241111184519.png]]


# Lecture 2

## Recap

We start with the [[#^96ffaf]]. We then expand to functions of r.v.s using [[#^2e5daa]]. Then, we tackle the question of rate of convergence  (which is unanswered by CLT) using [[#^6f71aa]] and the further assumption that the third moment exists. We see that the maximal distance between the sample mean CDF and the normal distribution is  $\sim \frac{1}{\sqrt{ n }}$ , which is far from ideal. Then, using [[Hoeffding's Theorem#^a16f48]]  and applying it to a CLT case [[Hoeffding's Theorem#^da7be3]]  , we get a much tighter bound, however with the condition that our r.v.s are bounded. Further we get stuck with the same caveat: for a fixed error interval $t$, we get exponential convergence, but if we'd like the error $t$ to diminish as we take more samples $n$, $t$ can only diminish as $\sim \frac{1}{\sqrt{ n }}$.

### Central Limit Theorem %% fold %%

> [!theorem] Central Limit Theorem
> $${\sqrt{n}}\left({\bar{X}}_{n}-\mu\right)\;{\xrightarrow{d}}\;{\mathcal{N}}\left(0,\sigma^{2}\right)$$

^96ffaf

### Discussion %% fold %%
- Exercise: X is a r.v. representing a fair coin toss. How many tosses do we need to estimate $E[X]$ with a given accuracy $\delta=0.1$ with probability $p=0.7$?
	- The probability that the $n$-th average distance from $E[X]$ is larger than $\delta$ can be a[[#^da7be3]] pproximated if we assume $Z_{n}=\frac{\sqrt{n}(\bar{X}_{n} - \mu)}{\sigma}$ to be large enough such that approximately $Z_{n} \sim \mathcal{N}$ by CLT
	- See Jupyter notebook

### The Delta Method %% fold %%

> [!theorem] The Delta Method
> If we have a series of r.v. $X_n$ s.t. $\sqrt{n}(X_{n} - \mu) \xrightarrow{d} N(0, \sigma^2)$ in distribution, and a function $g$ s.t. $g'(\mu) \neq 0$ then:
> $$
>\sqrt{ n }\cdot [g(X_{n)} - g(\mu)] \xrightarrow{d} N(0, \sigma^2\cdot g'(\mu))
> $$

^2e5daa

### Discussion %% fold %%
`\begin{proof}`
Assume $g'$ is continuous and define:
$$
g(x_{n}) = g(\mu) + g'(\tilde{\mu_{n}}) \cdot (x_{n} - \mu)
$$
For $\tilde{\mu}_{n} \in (x_{n}, \mu)$. We know $X_{n} \xrightarrow{P}\mu$ and so $\tilde{\mu_{n}} \xrightarrow{P}\mu$
`\end{proof}`


- Remark: why is this interesting? Why not treat $g(X_n)$ as a series of r.v. and then use the CLT?
- Answer: take for example the sequence $X_n$ of binomial distributions. Then for the sequence $\log(X_{n})$, the CLT won't help ($0$ is a possible outcome of $X_n$), but the aforementioned theorem can be used.


### Berry Essen Theorem %% fold %%

>[!theorem] Berry Essen
>TThere exists a positive constant _C_ such that if $$X_1,X_2,\dots$$ are i.i.d. random variables with $$\operatorname{E}(X_{1})=0,\,\operatorname{E}(X_{1}^{\,2})=\sigma^{2}>0,\,{\mathrm{and}}\,\operatorname{E}(|X_{1}|^{3})=\rho<\infty$$  and if we define
>$$ Y_{n}={X_{1}+X_{2}+\cdots +X_{n} \over n}
>$$
>the sample mean, with $F_{n}$ the cumulative distribution function of
>$$Y_{n}{\sqrt {n}} \over {\sigma }$$
>and Φ the cumulative distribution function of the standard normal distribution, then for all _x_ and _n:
>
>$$|F_{n}(x)-\Phi(x)|\leq{\frac{C\rho}{\sigma^{3}{\sqrt{n}}}}$$
>That is: given a sequence of independent and identically distributed random variables, each having mean zero and positive variance, if additionally the third absolute moment") is finite, then the cumulative distribution functions of the standardized sample mean and the standard normal distribution differ (vertically, on a graph) by no more than the specified amount.
>[image] ([pdf](zotero://open-pdf/library/items/P5EULUNI?page=17&annotation=T43JPUJU))  
([Vershynin, p. 9](zotero://select/library/items/MGQ99CCB))

^6f71aa

^2ffb59
### Monte Carlo Integration %% fold %%

>[!corollary] Monte Carlo Integration
>An integral of a function over a domain is the average or "expectation" of the function times the domain volume. So if we let $f(x)$, and denote $X \sim U(D)$, then:
> $$
> \frac{1}{|D|} \cdot \int_{I^d}f(x) = E[f(X)] \approx \frac{1}{n} \sum_{i=1}^n f(x_{i})
> $$
> In essence, the integral computes the average value (times the domain volume), which we can approximate by sampling uniformly over the domain.
> 
> The upside is that the convergence does not depend on the dimensionality of $f$, so we get a nice method for integrating high-dimensional functions. The downside is that convergence is slow (see [[#^6f71aa]]  )


>[!warning]
>The accuracy of Monte Carlo integration is with respect to the volume of $\mathbf{D}$, NOT with respect to $E[f(X)]$!

#### Discussion %% fold %%
Example in Jupyter notebook: we try to estimate the volume of a hypersphere using Monte Carlo integration. Caveat that is revealed when the dimension gets large (30-dim hypersphere) - The 30 dim. cube is much much larger than the respective hypersphere! We didn't sample any points inside the hypersphere, and so using the above method we estimated that its volume is zero. This is indeed rather accurate, in comparison to the hypercube volume! And so we get:


### Hoeffding %% fold %%
![[Hoeffding's Theorem#^a16f48]] 

> [!Quote]- Context from Vershinyn
> Let us summarize our situation. The Central Limit theorem offers an approximation of a sum of independent random variables $S_{N} = X_{1} + . . . X_N$ by normal distribution. The normal distribution is especially nice since it has very light, exponentially decaying tails. At the same time, the error of approximation in Central Limit Theorem decays too slow, even slower than linear. This big error ruins desired concentration properties for SN , which should guarantee light, exponentially decaying tails for SN . In order to resolve this issue, we need different ways to obtain concentration inequalities for SN . We will now develop a direct approach to concentration, which completely bypasses the Central Limit Theorem. [🔖](zotero://open-pdf/library/items/P5EULUNI?page=17&annotation=I5VMKQK7)

# Lecture 3

- Proved [[Hoeffding's Theorem#^ff2fdb]] :
![[Hoeffding's Theorem#^ff2fdb]] 

- Showed example:
![[Hoeffding's Theorem#^da7be3]]  

- Summary of the main idea around the estimators thus far:
	- [[#^96ffaf|CLT]] tells us that the sample mean of $X$ converges to a normal distribution which gets more and more concentrated around $E[X]$ as we increase the number of samples. 
	- So the general question is: when we take a sample mean $\bar{X}_{n}$, how fast and accurately can we claim $E[\bar{X}_{n}]=E[X]$? We have 3 parameters to play with: $n$, the accuracy $t$ and the probability of error $p=P(\bar{X}_{n}-E[\bar{X}_{n}] \geq t) = p(n,t)$
	- [[#^6f71aa]] gives us bounds for given $n$ and all $t$, under assumptions
	- [[Hoeffding's Theorem#^a16f48|Hoeffding]] give us bounds for given $n,t$ under assumptions. Turns out, when fixing $t$ we get Gaussian-like decay
	- Empirical results:
		- First we fix $t$ and plot $p(n)$:  ![[Pasted image 20241130143108.png]] From the plots the advantage of Hoeffding is clear.
		- Now fix $p$ and plot $n(t)$:![[Pasted image 20241130145530.png]] We see that all estimators give the same asymptotic behavior.

- Can we relax the assumption of bounded r..v in Hoeffding? 
	- First we see that the r.v. $\bar{X}_{n} - E[X]$ in Hoeffding's theorem is [[Sub-Gaussian Random Variable|sub-Gaussian]]. 
	- Display and prove [[Sub-Gaussian Random Variable#^5ee276]] 

- Proved:
![[Probability Theory#^12504d]] 






