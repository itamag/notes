You're right. Let me combine the accessible narrative with more technical sophistication.

“Lecture notes in the course "Analytical Mechanics” ([pdf](zotero://open-pdf/library/items/XEXRLJPB?page=1&annotation=IUTXEN8T))
# Analytical Mechanics: From Newton to Hamilton

> [!quote] Core Idea
> While Newton gave us $\vec{F}=m\vec{a}$ and direct force calculations, analytical mechanics reveals that nature's laws can be encoded in scalar functions living on geometric spaces. This shift from vectors to geometry and calculus of variations unveils profound insights about physical laws.

## The Path of Least Action

The journey begins with a remarkable principle: the entire motion of a physical system can be derived from a single scalar function - the Lagrangian.

> [!example] Theorem: Lagrangian Mechanics
> On a configuration manifold M, motion follows from:
> $$\frac{d}{dt}\left(\frac{\partial L}{\partial \dot{q}^i}\right) - \frac{\partial L}{\partial q_i} = 0$$
> where $L: TM \to \mathbb{R}$ is typically $L = T - V$

This formulation is powerful because:
1. Constraints become natural (e.g., pendulum restricts motion to a circle)
2. Coordinate transformations are transparent
3. Symmetries directly reveal conservation laws

But why should nature care about the Lagrangian? This leads us to:

> [!abstract] Hamilton's Principle
> Physical trajectories $\gamma: [t_1,t_2] \to M$ minimize the action:
> $$S[\gamma] = \int_{t_1}^{t_2} L(q,\dot{q},t)dt$$
> 
> **Physical Meaning:** Nature is "economical", choosing paths that minimize a certain quantity over time.
> 
> **Mathematical Structure:** We seek critical points of a functional on path space.

## Phase Space: A New Perspective

Rather than positions and velocities, we can work with positions and momenta, leading to a beautiful geometric structure.

> [!note] Hamiltonian Formulation
> Through Legendre transform $FL: TM \to T^*M$:
> $$p_i = \frac{\partial L}{\partial \dot{q}^i}$$
> Motion follows Hamilton's equations on symplectic manifold $(T^*M, \omega)$:
> $$\dot{q}^i = \frac{\partial H}{\partial p_i}, \quad \dot{p}_i = -\frac{\partial H}{\partial q^i}$$
> where $H = p_i\dot{q}^i - L$ is the Hamiltonian.

This symmetric formulation reveals phase space as the fundamental arena where:
- Volume is preserved (Liouville's theorem)
- Symmetries generate canonical transformations
- Classical observables form a Poisson algebra

## The Hamilton-Jacobi Equation: A Bridge to Quantum Mechanics

> [!example] Theorem: Hamilton-Jacobi
> Hamilton's principal function $S(q,t)$ satisfies:
> $$\frac{\partial S}{\partial t} + H\left(q,\frac{\partial S}{\partial q},t\right) = 0$$
> 
> **Key Insight:** This PDE:
> 1. Generates canonical transformations solving the motion
> 2. Connects to quantum mechanics via $\psi \sim e^{iS/\hbar}$
> 3. Leads to action-angle variables for integrable systems

## Key Applications & Techniques

> [!tip] Common Physical Systems
> 1. **Central Force:** $(r,\theta)$ coordinates
>    $$L = \frac{1}{2}m(\dot{r}^2 + r^2\dot{\theta}^2) - V(r)$$
>    - Conservation of angular momentum from rotational symmetry
>    - Kepler problem becomes integrable
> 
> 2. **Rigid Body:** Euler angles $(\phi,\theta,\psi)$
>    $$L = \frac{1}{2}\sum_{i=1}^3 I_i\omega_i^2 - mgh\cos\theta$$
>    - Reveals geometric phases (Hannay angles)
>    - Connects to quantum rotors
> 
> 3. **Small Oscillations:** Normal modes
>    $$L = \frac{1}{2}\dot{q}^T M\dot{q} - \frac{1}{2}q^T Kq$$
>    - Diagonalization reveals normal modes
>    - Bridge to quantum oscillators

## Deep Insights

> [!abstract] Fundamental Connections
> 1. **Symmetry → Conservation**
>    - Noether's theorem: Continuous symmetries yield conserved quantities
>    - Example: Time translation → Energy conservation
>
> 2. **Geometry → Physics**
>    - Phase space is a symplectic manifold
>    - Dynamics preserves geometric structure
>    - Quantum mechanics inherits classical geometry
>
> 3. **Classical → Quantum**
>    - Path integrals extend Hamilton's principle
>    - WKB approximation via Hamilton-Jacobi
>    - Poisson brackets → Commutators

> [!tip] Common Problem-Solving Strategy
> 1. Identify coordinates and constraints
> 2. Write Lagrangian/Hamiltonian
> 3. Use symmetries to find conserved quantities
> 4. Choose appropriate method:
>    - Euler-Lagrange for constrained systems
>    - Hamilton for canonical transformations
>    - Hamilton-Jacobi for complete solutions

Would you like me to expand on any of these aspects or add sections on advanced topics like:
- Perturbation theory
- Action-angle variables
- Adiabatic invariants
- Connection to field theories?

# Hamilton's Principle and Euler-Lagrange Equations for Field Theory

Consider a continuous system described by field variables $\phi^\alpha(\mathbf{x},t)$, where $\alpha$ indexes the field components and $\mathbf{x}$ represents spatial coordinates. The spacetime coordinates are denoted by $x^\mu = (t,\mathbf{x})$.

Hamilton's principle states that the action integral
$$S = \int\int \mathcal{L}(\phi^\alpha, \partial_\mu\phi^\alpha, x^\mu) \, dt\,d^3x$$
is stationary for the actual path of motion, where $\mathcal{L}$ is the Lagrangian density and $\partial_\mu\phi^\alpha$ represents all first derivatives of the fields. This leads to the Euler-Lagrange field equations:
$$\frac{\partial \mathcal{L}}{\partial \phi^\alpha} - \partial_\mu\left(\frac{\partial \mathcal{L}}{\partial(\partial_\mu\phi^\alpha)}\right) = 0$$
> [!example]- String
> For example, consider a string under gravity with vertical displacement field $\phi(x,t)$. The Lagrangian density is
> $$\mathcal{L} = \frac{1}{2}\rho\left(\frac{\partial\phi}{\partial t}\right)^2 - \frac{1}{2}T_0\left(\frac{\partial\phi}{\partial x}\right)^2 - \rho g\phi$$
> where $\rho$ is linear mass density, $T_0$ is string tension, and $g$ is gravitational acceleration. Applying the Euler-Lagrange equations yields the wave equation with gravity:
> $$\rho\frac{\partial^2\phi}{\partial t^2} - T_0\frac{\partial^2\phi}{\partial x^2} + \rho g = 0$$

Here’s a more concise version for the added chapter:  

---

# Canonical Momentum and Hamiltonian Density  

> [!NOTE] **Key Points to Remember**  
> - **Canonical Momentum**:  
>   $$ p = \frac{\partial L}{\partial \dot{q}}, $$  
>   where \( \dot{q} \) is the generalized velocity.  
> - **Canonical Momentum Density**:  
>   $$ \pi = \frac{\partial \mathcal{L}}{\partial \dot{\phi}}, $$  
>   where \( \phi \) is a field and \( \mathcal{L} \) the Lagrangian density.  
> - **Hamiltonian Density**:  
>   $$ \mathcal{H} = \pi \dot{\phi} - \mathcal{L}. $$  

## Overview  

In classical mechanics, **canonical momentum** \( p \) is conjugate to a generalized coordinate \( q \), defined from the Lagrangian \( L \) by:  
$$ p = \frac{\partial L}{\partial \dot{q}}. $$
In field theory, the **canonical momentum density** \( \pi \) generalizes this concept for fields \( \phi(x,t) \):  

$$ \pi = \frac{\partial \mathcal{L}}{\partial \dot{\phi}}, $$
where \( \mathcal{L} \) is the Lagrangian density.  

The **Hamiltonian density** \( \mathcal{H} \) describes the energy density of a field:  
$$ \mathcal{H} = \pi \dot{\phi} - \mathcal{L}. $$
The total Hamiltonian \( H \) is obtained by integrating \( \mathcal{H} \) over the spatial domain:  

$$ H = \int \mathcal{H} \, d^n x. $$
These concepts are pivotal in transitioning between the Lagrangian and Hamiltonian formulations, particularly in field theory and quantum mechanics.  
