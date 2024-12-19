
> [!theorem]- Chernoff's Inequality - easier to prove Hoeffding's theorem
> If $X_{i}$ are i.i.d Bernoulil and $a_i$ are constants then for all $t$
> $$
> P\left( \sum a_{i}X_{i} \geq t \right) \leq e^{ -\frac{t^2}{2\sum a_{i}}}
> $$
> Proof: the strategy is the same as the general case:
> 1. Multiply both sides of the probability inequality by parameter $s$. This DOF will be of use later.
> 2. Exponentiate to make positive r.v. and then use Markov's inequality
> 3. By independence, the expectation of the exponentiated sum will be a product of expectations for each r.v., These can easily be computed because Bernoulli
> 4. Now we can choose $s$ to give us the tightest bound
>
> See Chernoff’s inequality in Vershymin [🔖](zotero://open-pdf/library/items/P5EULUNI?page=21&annotation=PW5C4MBZ)

^ff2fdb

> [!theorem] Hoeffding’s inequality for general bounded random variables
> Let X1, . . . , XN be independent random variables. Assume that Xi ∈ [mi, Mi] almost surely for every i. Then, for any t > 0, we have:
> $$\mathbb{P}\left\{\sum_{i=1}^{N}(X_{i}-\mathbb{E}\,X_{i})\geq t\right\}\leq\exp\left(-{\frac{2t^{2}}{\sum_{i=1}^{N}(M_{i}-m_{i})^{2}}}\right)$$
> And:
> $$\mathbb{P}\left\{\left|\sum_{i=1}^{N}(X_{i}-\mathbb{E}\,X_{i})\right|\geq t\right\}\leq 2\exp\left(-{\frac{2t^{2}}{\sum_{i=1}^{N}(M_{i}-m_{i})^{2}}}\right)$$
> [🔖](zotero://open-pdf/library/items/P5EULUNI?page=20&annotation=IQJARSAG)
^a16f48


> [!example]- Hoeffding and CLT
>Let $X_{i}$ be i.i.d r.v. bounded in $[0,1]$ with expectation $\mu$ then:
> $$
> P\left( \left|\sum \frac{X_{i}}{n} - \mu \right| \geq t \right) = 2 \exp(-2nt^2)
> $$
> So, for fixed $t$, the probability of error decays exponentially! Alas, for nonfixed $t=\frac{1}{\sqrt{ n }}$, the probability of error is fixed.. In other words, our certainty increases exponentially, but our ability to approximate the expectation still increases only as $\sqrt{ n }$, as we got with Chernoff, CLT, Berry Essen..

^da7be3