
# In Statistical Physics
Suppose we have a physical system with a discrete set of states described by some quantum numbers, for example the wave vector $\vec{k}$. A quantity associated with the numbers, say $\epsilon$ will also have discrete possible values. Given a value, we can ask what is its multiplicity (usually denoted $g$)? 

In the $\vec{k}$ space (say $\mathbb{R}^d$), and with periodic boundary conditions in a volume $V$, each macrostate "takes up" $\frac{V}{(2\pi)^d}$. So we must have:
$$D( \epsilon)d\epsilon = \text{Number of macrostates having } [\epsilon, \epsilon + d\epsilon] = \frac{|\epsilon ^{-1}|}{V:(2\pi)^d}$$
For example if $\epsilon = v|\vec{k}|$ then $\epsilon ^{-1}( \epsilon_{0}) = \left\{ \vec{k}: |\vec{k}| = \frac{\epsilon_{0}}{v} \right\}$  and so:
$$D( \epsilon)d\epsilon = \frac{\frac{4\pi \epsilon^2}{v^2}\cdot dk}{V:(2\pi)^d} = \frac{4\pi\epsilon^2d\epsilon}{v^3 \cdot V}\cdot (2\pi)^d$$
## Mermin's Take
![[Pasted image 20241128134305.png]]([pdf](zotero://open-pdf/library/items/2CHG866D?page=59&annotation=UMZIT4YW))