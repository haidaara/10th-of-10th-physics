### **Refined Problem: The Radiation Reaction and the Abraham-Lorentz-Dirac Force**

A point charge \( q \) of mass \( m \) undergoes accelerated motion. Classically, an accelerating charge radiates electromagnetic energy and momentum. This loss of energy must be accounted for in the particle's equation of motion by a **radiation reaction force** \( \vec{F}_{\text{rad}} \) acting back on the particle. This problem explores the profound challenges in defining this force.

#### **Part 1: The Power Radiated and a Naïve Guess**
1.  **Larmor's formula** in SI units for the instantaneous power radiated by a non-relativistic charged particle with acceleration \( \vec{a} \) is:
    \[
    P = \frac{\mu_0 q^2}{6\pi c} a^2 = \frac{q^2}{6\pi \epsilon_0 c^3} a^2.
    \]
2.  From energy conservation, one might guess that the work done by the radiation reaction force equals the negative of the energy radiated: \( \int \vec{F}_{\text{rad}} \cdot \vec{v}  dt = - \int P  dt \). Using Larmor's formula, this suggests \( \vec{F}_{\text{rad}} \cdot \vec{v} = -\frac{\mu_0 q^2}{6\pi c} a^2 \). A candidate expression could be \( \vec{F}_{\text{rad}} = -\frac{\mu_0 q^2}{6\pi c} \vec{a} \), but this has a fatal flaw. For a particle with constant acceleration, this force is non-zero, but the actual radiation reaction force must vanish since \( \dot{\vec{a}} = 0 \). Moreover, radiation still occurs, implying that the energy comes from the **Schott energy** (the energy stored in the near field), not instantaneously from the work done by \( \vec{F}_{\text{rad}} \). Thus, the naïve guess fails.

#### **Part 2: The Abraham-Lorentz Force and its Pathologies**
A rigorous derivation leads to the **Abraham-Lorentz formula** for a non-relativistic particle:
\[
\vec{F}_{\text{rad}} = \frac{\mu_0 q^2}{6\pi c} \dot{\vec{a}} = \frac{q^2}{6\pi \epsilon_0 c^3} \dot{\vec{a}} \equiv m \tau_0 \dot{\vec{a}}
\]
where \( \tau_0 = \frac{q^2}{6\pi \epsilon_0 m c^3} = \frac{2}{3}\frac{r_e}{c} \) is a characteristic time (\( r_e = \frac{q^2}{4\pi \epsilon_0 m c^2} \) is the classical electron radius; for an electron, \( r_e \approx 2.82 \times 10^{-15} \, \text{m} \) and \( \tau_0 \approx 6.26 \times 10^{-24} \, \text{s} \)).

1.  **Equation of Motion:** Newton's second law becomes:
    \[
    m \vec{a} = \vec{F}_{\text{ext}} + m \tau_0 \dot{\vec{a}}.
    \]
2.  **Runaway Solutions:** For \( \vec{F}_{\text{ext}} = 0 \), the equation is \( \dot{\vec{a}} = \frac{1}{\tau_0} \vec{a} \). The solution is \( \vec{a}(t) = \vec{a}_0 e^{t/\tau_0} \), which grows exponentially without bound. This is unphysical because acceleration increases without any external force.
3.  **Preacceleration:** Imposing the boundary condition \( \vec{a}(t) \to 0 \) as \( t \to \infty \), the solution for \( \vec{F}_{\text{ext}} \) that vanishes for \( t > T \) is:
    \[
    \vec{a}(t) = \frac{1}{m \tau_0} \int_{t}^{\infty} e^{-(s-t)/\tau_0} \vec{F}_{\text{ext}}(s)  ds.
    \]
    This shows that the acceleration at time \( t \) depends on the future force, meaning the particle starts accelerating before the force is applied. This is called **preacceleration**.

#### **Part 3: The Relativistic Generalization (ALD Force)**
The relativistic form is the **Abraham-Lorentz-Dirac (ALD) four-force**. Using proper time \( \tau \) (not \( \tau_0 \)) and metric signature \( (+,-,-,-) \), the ALD force is:
\[
F^{\mu}_{\text{rad}} = m \tau_0 \left[ \frac{d^2 u^\mu}{d\tau^2} + \left( \frac{d u^\nu}{d\tau} \frac{d u_\nu}{d\tau} \right) u^\mu \right]
\]
where \( u^\mu \) is the four-velocity.

1.  In the non-relativistic limit, in the particle's instantaneous rest frame, \( u^\mu \approx (1, \vec{v}) \), \( d/d\tau \approx d/dt \), and \( d^2 u^\mu / d\tau^2 \approx (0, \dot{\vec{a}}) \). Also, \( d u^\nu / d\tau \, d u_\nu / d\tau \approx -a^2 \). Thus, the spatial components reduce to \( F^i_{\text{rad}} = m \tau_0 \dot{a}^i \), which is the Abraham-Lorentz force.
2.  To show orthogonality: 
    \[
    F^{\mu}_{\text{rad}} u_\mu = m \tau_0 \left[ \frac{d^2 u^\mu}{d\tau^2} u_\mu + \left( \frac{d u^\nu}{d\tau} \frac{d u_\nu}{d\tau} \right) u^\mu u_\mu \right].
    \]
    Since \( u^\mu u_\mu = 1 \), differentiating gives \( \frac{d u^\mu}{d\tau} u_\mu = 0 \) and \( \frac{d^2 u^\mu}{d\tau^2} u_\mu = - \frac{d u^\mu}{d\tau} \frac{d u_\mu}{d\tau} \). Thus, 
    \[
    F^{\mu}_{\text{rad}} u_\mu = m \tau_0 \left[ - \frac{d u^\mu}{d\tau} \frac{d u_\mu}{d\tau} + \frac{d u^\nu}{d\tau} \frac{d u_\nu}{d\tau} \cdot 1 \right] = 0.
    \]

#### **Part 4: The Landau-Lifshitz Formulation and Practical Application**
The **Landau-Lifshitz equation** is:
\[
m \frac{d u^\mu}{d\tau} \approx F^{\mu}_{\text{ext}} + \tau_0 \left( \delta^\mu_\lambda - u^\mu u_\lambda \right) \frac{d F^{\lambda}_{\text{ext}}}{d\tau}.
\]

1.  The projector operator \( \delta^\mu_\lambda - u^\mu u_\lambda \) ensures that the added term is orthogonal to \( u^\mu \), so that \( u_\mu \frac{d u^\mu}{d\tau} = 0 \) is maintained, preserving the mass-shell condition \( u^\mu u_\mu = 1 \).
2.  For an ultra-relativistic electron in a magnetic field \( \vec{B} \), the Lorentz force is \( F^{\mu}_{\text{ext}} = q F^{\mu\nu} u_\nu \). Using the Landau-Lifshitz form, the radiation reaction force is found to be anti-parallel to the velocity. The radiated power is \( P = \frac{2}{3} r_e^2 c \gamma^2 \beta^2 B^2 \sin^2 \alpha \) (where \( \alpha \) is the pitch angle). For perpendicular motion, \( \sin \alpha = 1 \). The force magnitude is \( F_{\text{rad}} \approx P / c \), as the momentum loss rate per unit time is \( dp/dt = dE/(c \, dt) \) for relativistic particles.

#### **Part 5: Conceptual Discussion and Scales**
1.  For an electron, \( \tau_0 \approx 6.26 \times 10^{-24} \, \text{s} \). Assume acceleration varies on \( \Delta t \sim 10^{-16} \, \text{s} \). Then \( \dot{a} \sim a / \Delta t \). For \( m \tau_0 \dot{a} \sim F_{\text{ext}} \sim 1.6 \times 10^{-9} \, \text{N} \), we find \( a \sim \frac{F_{\text{ext}} \Delta t}{m \tau_0} \approx 3 \times 10^{28} \, \text{m/s}^2 \), which is enormous. Thus, for macroscopic motions, the radiation reaction force is negligible, and the pathologies are unobservable.
2.  The Compton wavelength \( \lambda_c = \hbar / m_e c \approx 3.86 \times 10^{-13} \, \text{m} \) is much larger than \( r_e \approx 2.82 \times 10^{-15} \, \text{m} \). The ratio \( \lambda_c / r_e = 1 / \alpha \approx 137 \), where \( \alpha \) is the fine-structure constant. This indicates that quantum effects become important at scales much larger than the classical electron radius, so classical electrodynamics breaks down before the point particle concept leads to inconsistencies.

#### **Optional Enrichment (Bonus)**
3.  From the ALD equation: \( m \frac{d u^\mu}{d\tau} = F^{\mu}_{\text{ext}} + m \tau_0 \left[ \frac{d^2 u^\mu}{d\tau^2} + (\dot{u} \cdot \dot{u}) u^\mu \right] \). Substitute the zeroth-order approximation \( m \frac{d u^\mu}{d\tau} \approx F^{\mu}_{\text{ext}} \) into the right-hand side:
    \[
    m \frac{d u^\mu}{d\tau} \approx F^{\mu}_{\text{ext}} + \tau_0 \left[ \frac{d F^{\mu}_{\text{ext}}}{d\tau} + \left( \frac{F_{\text{ext}} \cdot F_{\text{ext}}}{m^2} \right) u^\mu \right].
    \]
    Using \( u_\mu \frac{d F^{\mu}_{\text{ext}}}{d\tau} \approx 0 \) and projecting orthogonally to \( u^\mu \), we obtain the Landau-Lifshitz equation.

### **Why This Problem is Profound**
- **Foundational Crisis:** Highlights the tension between point particles and field theory, foreshadowing renormalization in QFT.
- **Mathematical Physics:** Involves pathological solutions and integro-differential equations.
- **Bridging Classical and Quantum:** Shows where classical physics fails and quantum mechanics takes over.
- **Practical Importance:** Crucial for modeling high-energy phenomena like synchrotrons and astrophysical sources.

This problem offers a deep dive into a key issue in theoretical physics, from historical to modern perspectives.