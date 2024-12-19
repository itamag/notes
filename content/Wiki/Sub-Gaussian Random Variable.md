>[!quote]- Sub-Gaussian Appeal
>The class of such distributions, which we call sub-gaussian, deserves special attention. On the one hand, this class is sufficiently wide as it contains Gaussian, Bernoulli and all bounded distributions. On the other hand, as we will see, concentration results like Hoeffding’s inequality can be proved for all sub-gaussian distributions. This makes the class of sub-gaussian distributions a natural, and in many cases the canonical, class where one can develop various results in high dimensional probability theory and its applications. [🔖](zotero://open-pdf/library/items/P5EULUNI?page=28&annotation=ZYMA7CXA)

> [!definition] Sub-Gaussian Random Variable
> A random variable that satisfies one of the conditions 1-3' in [[#^5ee276]]  . We define the norm for these variables:
>  $$\|X\|_{\psi_{2}}=\operatorname*{inf}\left\{t>0:\,\mathbb{E}\exp(X^{2}/t^{2})\leq2\right\}$$

> [!theorem]- Sub-Gaussian Properties
> ![[Pasted image 20241130[[#^fa93cf]] 163204.png]]
> `\begin{proof}`
> 1->2: using [[Probability Theory#^12504d]]  and then change of variables in the integral to use the assumption 1. 
> 2 -> 3: we replace the exponent with its Taylor series, this yields us a series of expressions involving $E[X^{2p}]$ which is workable from 2. Then we need Stirling and an exponential bound on $\frac{1}{1-x}$
> 3 -> 3': By choosing $\lambda$ small enough
> 3' -> 1: Again from the form, it's clear that the way through it to (take power 2 and then) exponentiate and use Markov inequality. 
> 3 -> 4: We have information regarding an expression of the form $e^{x^2}$ and we'd like to prove an inequality involving $e^x$. Therefore it'd be wise to remember: $e^x \leq x + e^{x^2}$ and $2\lambda x \leq x^2 + \lambda^2$. The first inequality will be useful when $|\lambda| \leq 1$ and we can use assumption 3. If $|\lambda| \geq 1$ then we can use the second inequality to get $\lambda$ out of the exponent and continue using 3.
> 4 -> 1: again using the Markov inequality trick and assumption 4 thereafter. Note however, we need to employ it separately for $X \geq t$ and $X \leq -t$
`\end{proof}`
>[🔖](zotero://open-pdf/library/items/P5EULUNI?page=29&annotation=ZQBCKHJX)
^5ee276

> [!remark] Stronger notion of condition 3 in [[#^5ee276]] 
> Property 3 can be rephrased as:
> $$E[e^{\lambda^2X^2}] \leq e^{K_{3}^2\lambda^2}$$
> for all $|\lambda| \leq 1/K_{3}$


> [!remark]
> It was already shown in [[High Dimensional Probability]] that if an r.v. has an MGF then its PDF decays exponentially. Here we see that if $X^2$ has an MGF, then the PDF decays $\sim e^{-t^2}$ i.e. $X$ is sub-Gaussian


