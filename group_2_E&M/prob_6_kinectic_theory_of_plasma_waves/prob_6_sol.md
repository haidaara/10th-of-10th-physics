# solution of problem 6 kinetic theory 


### Part 1, Question 1: Linearized Vlasov-Maxwell Equations

#### Vlasov Equation for Electrons
The Vlasov equation describes the evolution of the electron distribution function \( f(\vec{r}, \vec{v}, t) \). For electrons in electromagnetic fields, it is:
\[
\frac{\partial f}{\partial t} + \vec{v} \cdot \nabla_r f + \frac{q}{m} (\vec{E} + \vec{v} \times \vec{B}) \cdot \nabla_v f = 0
\]
where \( q = -e \) for electrons (so \( q/m = -e/m \)), \( \vec{E} \) is the electric field, and \( \vec{B} \) is the magnetic field.

#### Maxwell's Equations
Maxwell's equations govern the electromagnetic fields:
\[
\nabla \cdot \vec{E} = \frac{\rho}{\epsilon_0}
\]
\[
\nabla \cdot \vec{B} = 0
\]
\[
\nabla \times \vec{E} = -\frac{\partial \vec{B}}{\partial t}
\]
\[
\nabla \times \vec{B} = \mu_0 \vec{J} + \mu_0 \epsilon_0 \frac{\partial \vec{E}}{\partial t}
\]
where \( \rho = q \int f \, d^3v \) is the charge density and \( \vec{J} = q \int \vec{v} f \, d^3v \) is the current density.

#### Equilibrium and Perturbations
The equilibrium state has:
- A uniform static magnetic field \( \vec{B}_0 = B_0 \hat{z} \).
- No electric field \( \vec{E}_0 = 0 \).
- A Maxwellian electron distribution function:
  \[
  f_0(v) = \frac{n_0}{(2\pi v_{th}^2)^{3/2}} \exp\left(-\frac{v^2}{2 v_{th}^2}\right), \quad v_{th} = \sqrt{\frac{k_B T}{m}}
  \]
- Ions are stationary and neutralize the plasma, so \( \rho = 0 \) and \( \vec{J} = 0 \) in equilibrium.

We introduce small perturbations:
- \( f = f_0 + f_1 \)
- \( \vec{E} = \vec{E}_1 \) (since \( \vec{E}_0 = 0 \))
- \( \vec{B} = \vec{B}_0 + \vec{B}_1 \)

#### Linearization
We assume wave-like perturbations: \( e^{i(\vec{k} \cdot \vec{r} - \omega t)} \), so all first-order quantities have this form. For example, \( f_1(\vec{r}, \vec{v}, t) = f_1(\vec{v}) e^{i(\vec{k} \cdot \vec{r} - \omega t)} \).

**Linearized Vlasov Equation:**
Substitute into the Vlasov equation and keep only first-order terms. The linearized equation becomes:
\[
\frac{\partial f_1}{\partial t} + \vec{v} \cdot \nabla_r f_1 + \frac{q}{m} (\vec{v} \times \vec{B}_0) \cdot \nabla_v f_1 = - \frac{q}{m} (\vec{E}_1 + \vec{v} \times \vec{B}_1) \cdot \nabla_v f_0
\]
here we apply the "Small Perturbation" Rule (Linearization):
it's key of classifying each term by its order of smallness:
*   **Zeroth-order terms:** Contain only equilibrium quantities ($f_0$, $\vec{E}_0$, $\vec{B}_0$). **These must satisfy the equilibrium on their own.**
*   **First-order terms:** Contain only **one** small perturbed quantity (e.g., $f_1$, $\vec{E}_1$, or $\vec{B}_1$).
*   **Second-order terms:** Contain the **product of two** small perturbed quantities (e.g., $\vec{E}_1 \cdot \nabla_v f_1$ or $\vec{v} \times \vec{B}_1 \cdot \nabla_v f_1$).


Using the wave-like dependence, the derivatives become:
- \( \frac{\partial}{\partial t} \rightarrow -i\omega \)
- \( \nabla_r \rightarrow i\vec{k} \)

Thus:
\[
-i\omega f_1 + i\vec{k} \cdot \vec{v} f_1 + \frac{q}{m} (\vec{v} \times \vec{B}_0) \cdot \nabla_v f_1 = - \frac{q}{m} (\vec{E}_1 + \vec{v} \times \vec{B}_1) \cdot \nabla_v f_0
\]

**Linearized Maxwell's Equations:**
The wave assumption is applied to the electromagnetic fields ($\vec{E}_1$, $\vec{B}_1$) because they are not external forces; they are generated self-consistently by the perturbations in the particle distribution ($f_1$). Since $f_1$ has a wave-like form, the fields it produces must also have the same wave-like form.

Similarly, for the fields, we linearize Maxwell's equations. Since \( \rho_1 = q \int f_1 \, d^3v \) and \( \vec{J}_1 = q \int \vec{v} f_1 \, d^3v \), we have:
\[
i\vec{k} \cdot \vec{E}_1 = \frac{\rho_1}{\epsilon_0}
\]
\[
i\vec{k} \cdot \vec{B}_1 = 0
\]
\[
i\vec{k} \times \vec{E}_1 = i\omega \vec{B}_1
\]
\[
i\vec{k} \times \vec{B}_1 = \mu_0 \vec{J}_1 - i\omega \mu_0 \epsilon_0 \vec{E}_1
\]
These equations describe how the perturbations \( \vec{E}_1 \) and \( \vec{B}_1 \) are related to \( f_1 \).

for detailed explanation why the self-consistency appear here, see last part of appendix section

---


>>## **Appendix** : The Maxwillian fontion

>>### 1. What is it?
>>
>>The provided equation is the **Maxwell-Boltzmann distribution** (or Maxwellian) for particle velocities in a plasma (or gas) in thermal equilibrium:
>>
>>\[
>>f_0(v) = \frac{n_0}{(2 \pi v_{th}^2)^{3/2}} \exp \left( -\frac{v^2}{2v_{th}^2} \right)
>>\]
>>
>>Where:
>>- \( f_0(v) \) is the equilibrium distribution function.
>>- \( n_0 \) is the particle number density (e.g., electrons/m³).
>>- \( v_{th} = \sqrt{\frac{k_B T}{m}} \) is the **thermal speed** (a characteristic speed of particles at temperature T).
>>- \( v^2 = v_x^2 + v_y^2 + v_z^2 \) is the square of the speed.
>>- \( k_B \) is Boltzmann's constant.
>>- \( T \) is the temperature.
>>- \( m \) is the particle mass.
>>
>>### 2. Where does it come from? (Physics Behind It)
>>
>>The Maxwellian distribution emerges naturally from **statistical mechanics**:
>>
>>- It describes the most probable distribution of particle speeds in a system that has reached **thermal equilibrium**.
>>- It is derived by maximizing the entropy of the system subject to the constraints of constant total energy and particle number.
>>- In the context of plasma, it represents a plasma where collisions (or other processes) have randomized the particle velocities, resulting in no net energy transfer in any direction—a state of maximum disorder.
>>
>>### 3. When is it used? For what?
>>
>>It is used as the **background** or **equilibrium distribution** function \( f_0 \) in the linearization of the Vlasov equation:
>>
>>- **Equilibrium Assumption**: The plasma is assumed to be in a steady state with no initial electric or magnetic fields (other than the constant \( \vec{B}_0 \)).
>>- **Perturbation Theory**: When studying waves or instabilities, we linearize the Vlasov equation around this equilibrium state. We write the total distribution as \( f = f_0 + f_1 \), where \( f_1 \) is a small perturbation. The Maxwellian \( f_0 \) serves as the reference state.
>>- **Zero Current/Charge in Equilibrium**: For a pure Maxwellian, the average velocity \( \langle \vec{v} \rangle = 0 \), so the equilibrium current density \( \vec{J}_0 = 0 \). Similarly, the charge density is zero if ions provide a neutralizing background.
>>
>>### 4. Difference from a Gaussian
>>
>>- A **Gaussian** in one dimension has the form \( e^{-x^2 / (2\sigma^2)} \).
>>- The Maxwellian is essentially a **product of three Gaussians** (for \( v_x, v_y, v_z \)), normalized so that its integral over all velocity space equals the density \( n_0 \):
>>  \[
>>  \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f_0(\vec{v})  dv_x dv_y dv_z = n_0
>>  \]
>>- So, it is a **multivariate Gaussian distribution in velocity space**. The term "Maxwellian" specifically refers to this Gaussian distribution applied to particle velocities in thermal equilibrium.
>>
>>


>>### **Appendix** : the vlasov eqt's


>>### 1. Where does it come from? The Physics & Relation to BBGKY
>>
>>let's  recall the **BBGKY hierarchy** (Bogoliubov–Born–Green–Kirkwood–Yvon). This is its formal origin.
>>
>>*   **The Full Problem:** In a plasma with $N$ particles, to know everything, you'd need to solve for the $N$-particle distribution function, which depends on $3N$ position and $3N$ velocity coordinates. This is impossible.
>>*   **The BBGKY Hierarchy:** This is a set of coupled equations that describes the evolution of $s$-particle distribution functions ($f_1, f_2, f_3,$ ...). The equation for $f_1$ depends on $f_2$, which depends on $f_3$, and so on. It's an infinite, intractable chain.
>>*   **The Closure Assumption (The Key Step):** To break the chain, we make a physical assumption. The Vlasov equation is derived by assuming that **the two-particle correlation function $f_2$ is negligible**. This is known as the **"mean-field"** approximation.
>>
>>**What does this mean physically?**
>>It means an individual particle doesn't feel the specific, discrete force from every other nearby particle (a two-body collision). Instead, it only feels the **smooth, averaged collective force** generated by the total charge and current densities in the plasma. This is an excellent approximation for most plasmas because the long-range nature of the Coulomb force means a particle interacts with a vast number of others simultaneously, making the collective effect dominate over short-range, binary collisions.
>>
>>**In short: The Vlasov equation is the BBGKY hierarchy truncated at the first level, using the mean-field approximation. It's a collisionless kinetic equation.**
>>
>>---
>>
>>### 2. The Vlasov Equation and its Components
>>
>>The Vlasov equation for a species of charged particles (e.g., electrons) is:
>>
>>$$\frac{\partial f}{\partial t} + \vec{v} \cdot \nabla_r f + \frac{q}{m} (\vec{E} + \vec{v} \times \vec{B}) \cdot \nabla_v f = 0$$
>>
>>This is a equation in **6-dimensional phase space** ($\vec{r}$, $\vec{v}$). The distribution function $f(\vec{r}, \vec{v}, t)$ tells you the density of particles in a small volume $d^3r d^3v$ around the point ($\vec{r}$, $\vec{v}$) at time $t$.
>>
>>Let's give each term a simple, physical meaning. Imagine you are riding along on a tiny spaceship through phase space, following a group of particles with a specific position and velocity.
>>
>>#### Term 1: $\frac{\partial f}{\partial t}$ (The "Time Derivative")
>>*   **Physical Meaning:** The local rate of change of the particle density *at a fixed point* in phase space.
>>*   **Easy to Remember:** It's like a photographer standing in one spot and taking pictures of the crowd density at that spot over time.
>>
>>#### Term 2: $\vec{v} \cdot \nabla_r f$ (The "Spatial Flow" or "Convection" Term)
>>*   **Physical Meaning:** This term accounts for particles with a velocity $\vec{v}$ *flowing into* or *out of* the spatial volume $d^3r$ due to their motion.
>>*   **Easy to Remember:** This is the $\vec{v}$ part. If particles are moving, they naturally carry their distribution function with them. A gradient ($\nabla_r f$) means the density is different from one point to the next, so flow will change the local density.
>>
>>#### Term 3: $\frac{q}{m} (\vec{E} + \vec{v} \times \vec{B}) \cdot \nabla_v f$ (The "Acceleration" or "Force" Term)
>>*   **Physical Meaning:** This is the most crucial term for plasmas. It accounts for particles with a position $\vec{r}$ *flowing into* or *out of* the velocity volume $d^3v$ due to forces accelerating them.
>>*   **Easy to Remember:** This is the $\vec{a}$ part.
>>    *   $\frac{q}{m}(\vec{E} + \vec{v} \times \vec{B})$ is the acceleration $\vec{a}$ of a particle due to the Lorentz force.
>>    *   $\nabla_v f$ is the gradient of the distribution in *velocity space*. If $f$ changes with velocity (e.g., more slow particles than fast ones), acceleration will move particles along the velocity axis, changing the density at a specific velocity $\vec{v}$.
>>
>>#### The Sum ($= 0$): The "Total Derivative"
>>The whole equation states that the **total derivative** of $f$ is zero:
>>>>$$\frac{Df}{Dt} = 0$$
>>>>**Profound Physical Meaning:** As you move along with a group of particles in 6D phase space, the density of that group *does not change*. Particles are neither created nor destroyed (it's a continuity equation in phase space). They just move around in phase space due to their velocity (Term 2) and due to forces (Term 3). This is a beautiful and powerful result.
>>
>>---
>>
>>### Summary and Connection to Your Problem
>>
>>In your problem, you **linearize** this equation. You assume:
>>1.  **Equilibrium ($f_0$):** The smooth, unchanging background state (the Maxwellian you asked about earlier).
>>2.  **Perturbation ($f_1$):** A very small wave-like ripple on top of that background ($f = f_0 + f_1$).
>>3.  **Perturbed Fields ($\vec{E}_1, \vec{B}_1$):** The electromagnetic fields created by the perturbations in charge and current density ($\rho_1, \vec{J}_1$).



>>## **Appendix:** Maxwell's_and_vlasov_eqt


>>the concept of **self-consistency**.
>>
>>The Vlasov equation and Maxwell's equations are not just used together; they are **coupled**. They form a closed, self-consistent system that describes how particles create fields and how fields, in turn, govern the motion of particles.
>>
>>Here’s the purpose and the physics behind their relationship, broken down into a simple cause-and-effect loop.
>>
>>### The Self-Consistency Loop
>>
>>The core idea is that **particles generate fields** and **fields move particles**. This creates a feedback loop:
>>
>>1.  **Particles → Fields (Maxwell's Equations):**
>>    *   The charge density ($\rho$) and current density ($\vec{J}$) of the particles are the **sources** for the electromagnetic fields in Maxwell's equations.
>>    *   $\nabla \cdot \vec{E} = \frac{\rho}{\epsilon_0}$: Electric charges are the source of electric field divergence.
>>    *   $\nabla \times \vec{B} = \mu_0 \vec{J} + \mu_0 \epsilon_0 \frac{\partial \vec{E}}{\partial t}$: Electric currents are the source of magnetic field curl.
>>
>>2.  **Fields → Particles (Vlasov Equation):**
>>    *   The electromagnetic fields ($\vec{E}$ and $\vec{B}$) determine the force on every particle via the Lorentz Force Law: $\vec{F} = q(\vec{E} + \vec{v} \times \vec{B})$.
>>    *   This force dictates how particles **move through phase space** (change their position and velocity), which is exactly what the Vlasov equation describes: $\frac{\partial f}{\partial t} + \vec{v} \cdot \nabla_r f + \frac{q}{m} (\vec{E} + \vec{v} \times \vec{B}) \cdot \nabla_v f = 0$.
>>
>>3.  **The Loop Closes:**
>>    *   The motion of the particles (from step 2) changes their spatial distribution and flow, which **alters the charge density $\rho$ and current density $\vec{J}$**.
>>    *   These new $\rho$ and $\vec{J}$ become the new sources for Maxwell's equations (back to step 1), which modify the $\vec{E}$ and $\vec{B}$ fields.
>>    *   The modified fields then again alter the motion of the particles, and so on.
>>
>>This loop happens continuously in time. To describe a plasma, you **must** solve both sets of equations simultaneously because each one depends on the solution of the other.
>>
>>```mermaid
>>flowchart TD
>>    A[Particles\nDistribution Function f] -- "Define charge & current density<br>ρ = q∫f d³v<br>J = q∫v f d³v" --> B[Maxwell's Equations]
>>    B -- "Generate" --> C[Electromagnetic Fields<br>E, B]
>>    C -- "Exert Lorentz Force<br>F = q(E + v×B)" --> A
>>```
>>
>>### Why is this so crucial for your problem? (Waves and Instabilities)
>>
>>You are studying waves. In a plasma, waves are **self-consistent perturbations** that propagate through this coupled system.
>>
>>1.  **The Perturbation:** You start with an equilibrium (uniform $f_0$, constant $\vec{B}_0$, $\vec{E}_0=0$). Then you "wiggle" the particles a little bit, creating a small perturbed distribution $f_1$.
>>2.  **Particles → Fields:** This "wiggle" in the particles creates oscillating, wave-like perturbations in the charge and current density ($\rho_1$, $\vec{J}_1$).
>>3.  **Fields → Particles:** These oscillating sources, via Maxwell's equations, generate wave-like electromagnetic fields ($\vec{E}_1$, $\vec{B}_1$).
>>4.  **The Key Question:** Do these newly created fields $\vec{E}_1$ and $\vec{B}_1$ reinforce the original "wiggle" ($f_1$), causing it to grow (an **instability**), or do they oppose it, causing it to oscillate (a **wave**) or damp out?
>>5.  **The Dispersion Relation:** The condition for a self-sustaining wave (where the fields created by the particle motion are just the right strength and phase to sustain that motion) leads to a mathematical equation called the **dispersion relation**, which relates the wave's frequency ($\omega$) to its wavelength ($k$). Solving this equation tells you everything about the wave: its existence, its propagation, and its damping.


>>## **Appendix: why lineraiztion on E&M 

>>The short answer is: **The wave assumption is applied to the electromagnetic fields ($\vec{E}_1$, $\vec{B}_1$) because they are not external forces; they are generated self-consistently by the perturbations in the particle distribution ($f_1$). Since $f_1$ has a wave-like form, the fields it produces must also have the same wave-like form.**
>>
>>Let's break down the logic step-by-step:
>>
>>### 1. The Core Principle: Self-Consistency
>>
>>In a plasma, you cannot solve for the particles and the fields separately. They are intrinsically linked in a loop:
>>1.  **Particles create Fields:** The charges and currents from the particles ($\rho$, $\vec{J}$) are the *sources* for the electromagnetic fields in Maxwell's equations.
>>2.  **Fields move Particles:** The electromagnetic fields dictate how the particles move via the Lorentz force in the Vlasov equation.
>>
>>This creates a closed, self-consistent system. You can't have one without the other.
>>
>>### 2. The Logic of the Wave Ansatz
>>
>>Your initial perturbation is the assumption of a wave in the particle distribution:
>>$$f_1(\vec{r}, \vec{v}, t) = f_1(\vec{v}) e^{i(\vec{k} \cdot \vec{r} - \omega t)}$$
>>
>>Now, let's follow the self-consistency loop:
>>
>>*   **Step 1: Particles → Fields**
>>    The perturbed distribution $f_1$ creates perturbed charge and current densities:
>>    $$
>>    \rho_1 = q \int f_1  d^3v \quad \text{and} \quad \vec{J}_1 = q \int \vec{v} f_1  d^3v
>>    $$
>>    If $f_1$ has the form $[\text{something}] \cdot e^{i(\vec{k} \cdot \vec{r} - \omega t)}$, then the integrals $\rho_1$ and $\vec{J}_1$ will also have the **exact same spatial and temporal dependence** $e^{i(\vec{k} \cdot \vec{r} - \omega t)}$. The velocity integration doesn't affect the $\vec{r}$ and $t$ dependence.
>>
>>*   **Step 2: Fields → Particles (completing the loop)**
>>    These wave-like sources ($\rho_1$, $\vec{J}_1$) are now plugged into the linearized Maxwell's equations. For example, Gauss's Law becomes:
>>    $$
>>    \nabla \cdot \vec{E}_1 = \frac{\rho_1}{\epsilon_0}
>>    $$
>>    The left side is a spatial derivative of $\vec{E}_1$. The right side is proportional to $e^{i(\vec{k} \cdot \vec{r} - \omega t)}$. The only way this equation can hold for all positions $\vec{r}$ and time $t$ is if $\vec{E}_1$ itself has the **same wave-like form**:
>>    $$
>>    \vec{E}_1(\vec{r}, t) = \vec{E}_1  e^{i(\vec{k} \cdot \vec{r} - \omega t)}
>>    $$
>>    The same logic applies to all of Maxwell's equations. The wave-like sources *force* the solutions for $\vec{E}_1$ and $\vec{B}_1$ to be waves with the **same $\vec{k}$ and $\omega$**.
>>
>>### 3. Why This is Necessary and Powerful
>>
>>This isn't just a mathematical trick; it's a physical requirement for a **self-sustaining normal mode**. We are looking for solutions where the particle perturbation and the field perturbation oscillate and propagate together in a consistent way.
>>
>>This approach is incredibly powerful because it turns all the differential operators in Maxwell's equations into simple algebra:
>>*   $\frac{\partial}{\partial t} \rightarrow -i\omega$
>>*   $\nabla \rightarrow i\vec{k}$
>>*   $\nabla \times \rightarrow i\vec{k} \times$
>>*   $\nabla \cdot \rightarrow i\vec{k} \cdot$
>>
>>For example, the complex Maxwell's equations you listed:
>>$$
>>\begin{aligned}
>>i\vec{k} \cdot \vec{E}_1 &= \frac{\rho_1}{\epsilon_0} \\
>>i\vec{k} \cdot \vec{B}_1 &= 0 \\
>>i\vec{k} \times \vec{E}_1 &= i\omega \vec{B}_1 \\
>>i\vec{k} \times \vec{B}_1 &= \mu_0 \vec{J}_1 - i\omega \mu_0 \epsilon_0 \vec{E}_1
>>\end{aligned}
>>$$
>>...are now algebraic equations that are much easier to solve than the original PDEs.
>>
>>### Summary
>>
>>| Quantity | Why it has the wave form $e^{i(\vec{k} \cdot \vec{r} - \omega t)}$ |
>>| :--- | :--- |
>>| **$f_1$** | **This is our initial ansatz.** We *assume* a wave-like perturbation in the particle distribution. |
>>| **$\rho_1, \vec{J}_1$** | **Because they are moments of $f_1$.** They inherit the wave dependence from $f_1$. |
>>| **$\vec{E}_1, \vec{B}_1$** | **Because they are generated by $\rho_1$ and $\vec{J}_1$.** Maxwell's equations *force* the fields to have the same $\vec{k}$ and $\omega$ as their sources. |
>>
>>So, you are correct that the wave solution is for $f_1$. But due to the self-consistent, coupled nature of a plasma, this initial assumption *dictates* that every other first-order quantity in the system must share the same wave-like behavior. This is the foundation of linear plasma wave theory.




### Part 1, Question 2: Method of Characteristics and Unperturbed Orbits

The linearized Vlasov equation can be solved using the **method of characteristics**. This involves integrating along the **unperturbed orbits** of particles—the trajectories they follow under only the static magnetic field \( \vec{B}_0 \).

#### Unperturbed Orbits
For a particle in \( \vec{B}_0 = B_0 \hat{z} \), the equation of motion is:
\[
\dot{\vec{v}} = \frac{q}{m} \vec{v} \times \vec{B}_0
\]
This results in **helical motion**: circular gyration in the plane perpendicular to \( \vec{B}_0 \) and uniform motion along \( \vec{B}_0 \). The gyrofrequency is \( \omega_c = \frac{e B_0}{m} \) (for electrons, \( \omega_c \) is positive since \( q = -e \), but the sense of rotation is opposite to that for ions).

#### Expressing \( f_1 \) as an Integral
The left side of the linearized Vlasov equation represents the derivative of \( f_1 \) along the unperturbed orbits. Thus, we can write:
\[
\frac{d f_1}{d t} \bigg|_{\text{orbit}} = - \frac{q}{m} (\vec{E}_1 + \vec{v} \times \vec{B}_1) \cdot \nabla_v f_0
\]
Integrating along the orbit from the infinite past to time \( t \), we obtain:
\[
f_1(\vec{r}, \vec{v}, t) = - \frac{q}{m} \int_{-\infty}^{t} dt' \, \left[ (\vec{E}_1 + \vec{v}' \times \vec{B}_1) \cdot \nabla_v f_0 \right]_{(\vec{r}'(t'), \vec{v}'(t'), t')}
\]
Here:
- \( \vec{r}'(t') \) and \( \vec{v}'(t') \) are the position and velocity along the unperturbed orbit that reaches \( \vec{r} \) and \( \vec{v} \) at time \( t \).
- The integral sums up the effects of the perturbed fields along the particle's history.

#### Effect of Magnetic Field
The magnetic field \( \vec{B}_0 \) affects the orbits by causing gyration, which makes the integral more complex. Specifically:
- The helical motion introduces **cyclotron harmonics** into the response, as the particle experiences the wave fields at multiples of the gyrofrequency.
- This leads to resonances when \( \omega - k_\parallel v_\parallel - n \omega_c = 0 \) for integer \( n \), which are crucial for wave-particle interactions.

This integral form is key for deriving the dielectric tensor in Part 2.

---


>>**Appendix:** Note on the unperturbed motion, *Motion of particle in static magnetic field*



>>### The Physics of Particle Motion in a Magnetic Field
>>
>>Imagine a single electron in a vacuum with a uniform, static magnetic field **B₀ = B₀ ẑ**. No electric fields. The force on the electron is given by the **Lorentz force**:
>>
>>**F** = q(**v** × **B₀**)
>>
>>where q = -e (the electron charge is negative).
>>
>>Let's write the equation of motion (Newton's second law):
>>m (d**v**/dt) = q(**v** × **B₀**)
>>
>>Now, let's split the velocity **v** and the force into components *parallel* to **B₀** (the z-direction) and *perpendicular* to it (the x-y plane).
>>
>>**1. Motion Parallel to B₀ (z-direction):**
>>*   Look at the z-component of the Lorentz force: F_z = q [ (**v** × **B₀**) ]_z
>>*   **v** × **B₀** is always perpendicular to both **v** and **B₀**. Since **B₀** is along z, the cross product has *no z-component*.
>>    *   (**v** × **B₀**)_z = v_x B₀_y - v_y B₀_x. But B₀_y and B₀_x are both 0! So (**v** × **B₀**)_z = 0.
>>*   Therefore, **F_z = 0**.
>>*   From Newton's law: m (dv_z/dt) = 0.
>>*   **Conclusion:** There is no force along the magnetic field line. The particle's velocity in the z-direction, v_∥, is **constant**. The particle drifts along the field line at a constant speed.
>>
>>**2. Motion Perpendicular to B₀ (x-y plane):**
>>*   The entire force F = q(**v** × **B₀**) lies in the x-y plane (it's perpendicular to both **v** and **B₀**).
>>*   This force is always perpendicular to the particle's instantaneous velocity in the plane.
>>*   **A force that is always perpendicular to velocity does no work.** It cannot change the particle's kinetic energy; it can only change the *direction* of its velocity.
>>*   This is exactly the condition for **uniform circular motion**. The magnetic force provides the centripetal force needed to make the particle move in a circle.
>>
>>Let's prove the circular motion mathematically. The magnitude of the force is:
>>|**F**| = |q| |**v**_⟂| |**B₀**|  (since sin(90°) = 1)
>>
>>This must equal the centripetal force:
>>|q| |**v**_⟂| |**B₀**| = m (|**v**_⟂|² / R)
>>Cancel one |**v**_⟂| from both sides:
>>|q| |**B₀**| = m (|**v**_⟂| / R)
>>
>>We define the **cyclotron frequency (or gyrofrequency)** ω_c as the angular frequency of this circular motion:
>>**ω_c = |**v**_⟂| / R = |q| |B₀| / m**
>>
>>For an electron, q = -e, so the magnitude is ω_c = eB₀/m. The radius of the circle is called the **Larmor radius** or **gyroradius**:
>>**ρ = R = |**v**_⟂| / ω_c = (m |**v**_⟂|) / (|q| B₀)**
>>
>>**The Sign (Direction of Rotation):**
>>*   The direction of the force **F** = q(**v** × **B₀**) depends on the sign of q.
>>*   For an **electron** (q = -e), the force is in the opposite direction of the cross product (**v** × **B₀**).
>>*   This means electrons **gyrate in a right-handed helix** around **B₀**. If you point your thumb along **B₀** (toward +z), your fingers curl in the direction of the electron's circular motion. (For positive ions, it's a left-handed helix).
>>
>>### Putting It All Together: The Helix
>>
>>The particle's motion is the **superposition** of these two independent motions:
>>1.  **Constant velocity** along the magnetic field line (the z-axis).
>>2.  **Uniform circular motion** in the plane perpendicular to the field (the x-y plane).
>>
>>The path traced out by this combination of motions is a **helix** (like a slinky or a spiral staircase). The axis of the helix is parallel to **B₀**.
>>
>>Here is a breakdown of the motion into its components, showing how the circular motion in the x-y plane combines with linear motion along the z-axis to form a helix. The key parameters are labeled: the **Larmor Radius (ρ)** defining the helix's width, the **Pitch** defining the distance between turns (determined by v_∥), and the **Cyclotron Frequency (ω_c)** defining how quickly the particle gyrates.
>>
>>### Why is this the "Unperturbed Orbit"?
>>
>>In the context of the Vlasov equation and the method of characteristics:
>>*   The "unperturbed" fields are just the static **B₀** and zero electric field **E₀=0**.
>>*   The orbit of a particle under *only* these fields is precisely the **helical path** we just described.
>>*   When we linearize the equations, we assume the wave perturbations (**E₁**, **B₁**) are very small. So, to first order, the particles still follow these same helical paths. The effect of the perturbations is just a small "kick" or "nudge" that we can calculate by integrating along this unperturbed helical path.
>>
>>>This is the powerful insight: we know the exact solution for the unperturbed orbits (helical motion), so we can use them as a known reference to calculate the small, perturbed response of the plasma to waves. This transforms a very difficult problem into a manageable one.
>>>### another way of deriving it
>
>Of course. You've hit on a key conceptual point. The jump from "force is perpendicular to velocity" to "therefore, uniform circular motion" is a classic physics argument, but it can feel a bit hand-wavy without the math to back it up. Let's bridge that gap with both intuition and a clear, step-by-step algebraic derivation.
>
>### 1. The Intuitive Picture
>
>First, let's solidify the intuition. Why does a perpendicular force cause circular motion?
>
>*   **Velocity** is a vector that points in the direction the particle is moving *right now*.
>*   **Acceleration** is a vector that points in the direction the velocity will change *in the next instant*.
>*   If a force (and thus acceleration) is always perpendicular to the velocity, it **never acts to speed the particle up or slow it down**. It only changes its direction.
>*   If you continuously change an object's direction but not its speed, and you do so with a constant-magnitude force, you trace out a path where every point is the same distance from a center. This is the definition of a **circle**.
>
>Think of spinning a ball on a string. The tension in the string is always perpendicular to the ball's instantaneous velocity, pulling it towards the center of the circle. The magnetic force acts exactly like this "invisible string" for charged particles.
>
>### 2. The Algebraic Derivation (Step-by-Step)
>
>The intuitive picture is confirmed by solving the equations of motion rigorously. Here is a clearer derivation than the one you excerpted.
>
>We start with Newton's Second Law for a particle of charge $q$ and mass $m$ in a magnetic field $\vec{B} = B_0 \hat{z}$:
>
>\[
>m \frac{d\vec{v}}{dt} = q (\vec{v} \times \vec{B}) = q B_0 (v_y \hat{x} - v_x \hat{y})
>\]
>
>This one vector equation gives us three equations, one for each velocity component:
>
>1.  **Parallel Motion ($z$-direction):**
>    \[
>    m \frac{dv_z}{dt} = 0
>    \]
>    The right-hand side is zero because $(\vec{v} \times \vec{B})_z = 0$. This integrates trivially to:
>    \[
>    v_z(t) = \text{constant} = v_{\parallel}
>    \]
>    Motion along the field is unchanged. This is straightforward.
>
>2.  **Perpendicular Motion ($x$- and $y$-directions):**
>    \[
>    m \frac{dv_x}{dt} = q B_0 v_y \quad \text{(1)}
>    \]
>    \[
>    m \frac{dv_y}{dt} = -q B_0 v_x \quad \text{(2)}
>    \]
>    These two equations are **coupled**—the change in $v_x$ depends on $v_y$ and vice versa. To solve them, we need to decouple them.
>
>    *   **Step 1: Differentiate Equation (1) with respect to time.**
>        \[
>        m \frac{d^2v_x}{dt^2} = q B_0 \frac{dv_y}{dt}
>        \]
>
>    *   **Step 2: Substitute Equation (2) into the result.**
>        We know from (2) that $\frac{dv_y}{dt} = -\frac{q B_0}{m} v_x$. Let's plug that in:
>        \[
>        m \frac{d^2v_x}{dt^2} = q B_0 \left( -\frac{q B_0}{m} v_x \right )
>        \]
>        \[
>        \frac{d^2v_x}{dt^2} = -\left( \frac{q^2 B_0^2}{m^2} \right) v_x
>        \]
>
>    *   **Step 3: Recognize the form of the equation.**
>        This is the classic **simple harmonic oscillator** equation:
>        \[
>        \frac{d^2v_x}{dt^2} + \omega_c^2 v_x = 0
>        \]
>        where we have defined the **cyclotron frequency** $\omega_c = \frac{|q|B_0}{m}$. (The absolute value will be important for the direction of motion).
>
>    *   **Step 4: Write the general solution.**
>        The general solution for a simple harmonic oscillator is a sine wave. Let's choose a specific one that makes the math easier later. We can set the phase so that at $t=0$, $v_x$ is at its maximum.
>        \[
>        v_x(t) = v_\perp \cos(\omega_c t) \quad \text{(3)}
>        \]
>        Here, $v_\perp$ is the constant speed of the particle in the perpendicular plane (the magnitude of the velocity vector $(v_x, v_y)$).
>
>    *   **Step 5: Find $v_y(t)$ using Equation (1).**
>        From Eq. (1): $m \frac{dv_x}{dt} = q B_0 v_y$
>        First, differentiate our solution for $v_x$:
>        \[
>        \frac{dv_x}{dt} = -v_\perp \omega_c \sin(\omega_c t)
>        \]
>        Now plug into Eq. (1):
>        \[
>        m \left( -v_\perp \omega_c \sin(\omega_c t) \right) = q B_0 v_y
>        \]
>        \[
>        v_y = -\frac{m}{q B_0} v_\perp \omega_c \sin(\omega_c t)
>        \]
>        Recall that $\omega_c = \frac{|q|B_0}{m}$. Substitute this in:
>        \[
>        v_y = -\frac{m}{q B_0} v_\perp \left( \frac{|q|B_0}{m} \right) \sin(\omega_c t) = -\frac{|q|}{q} v_\perp \sin(\omega_c t) \quad \text{(4)}
>        \]
>
>**This is the crucial step for direction.** The term $\frac{|q|}{q}$ gives the sign.
>*   For a **positive ion** ($q > 0$), $\frac{|q|}{q} = +1$, so $v_y = -v_\perp \sin(\omega_c t)$.
>*   For an **electron** ($q < 0$), $\frac{|q|}{q} = -1$, so $v_y = +v_\perp \sin(\omega_c t)$.
>
>*   **Step 6: Integrate to find the position.**
>    To find the particle's path, integrate the velocities (Eq. 3 and 4).
>    \[
>    x(t) = x_0 + \int v_x  dt = x_0 + \frac{v_\perp}{\omega_c} \sin(\omega_c t)
>    \]
>    \[
>    y(t) = y_0 + \int v_y  dt = y_0 + \frac{|q|}{q} \frac{v_\perp}{\omega_c} \cos(\omega_c t)
>    \]
>
>These are the **parametric equations of a circle** with:
>*   **Center:** $(x_0, y_0)$ (the "guiding center")
>*   **Radius (Larmor Radius):** $r_L = \frac{v_\perp}{\omega_c} = \frac{m v_\perp}{|q| B_0}$
>*   **Direction:**
>    *   If $\frac{|q|}{q} = +1$ (positive charge), $y(t) = y_0 + \frac{v_\perp}{\omega_c} \cos(\omega_c t)$. As time increases, the $y$-position leads the $x$-position by 90 degrees. This is **clockwise** rotation when viewed from above (from $+z$).
>    *   If $\frac{|q|}{q} = -1$ (negative charge), $y(t) = y_0 - \frac{v_\perp}{\omega_c} \cos(\omega_c t)$. This is **counter-clockwise** rotation when viewed from above.
>
>This derivation shows algebraically how the perpendicular force *necessarily* leads to circular motion, and it precisely defines all the parameters of that motion (frequency, radius, and direction).
>
>### Summary
>
>| Concept | Algebraic Result | Physical Meaning |
>| :--- | :--- | :--- |
>| **Parallel Motion** | $v_z = \text{constant}$ | Free streaming along the field line. |
>| **Perp. Frequency** | $\omega_c = \frac{|q|B_0}{m}$ | The rate of gyration. Higher B-field → faster gyration. |
>| **Perp. Radius** | $r_L = \frac{m v_\perp}{|q|B_0}$ | Size of the orbit. Higher B-field → tighter orbit. |
>| **Direction** | Sign of $\frac{|q|}{q}$ in $v_y$ | Positive charges gyrate clockwise, negative (electrons) gyrate counter-clockwise (when $ \vec{B} $ is out of the page). |
>
>This rigorous result for the **unperturbed orbit** is why we can use it as a known path in the Method of Characteristics to solve the linearized Vlasov equation. We know exactly where a particle was in the past ($\vec{r}'(t')$, $\vec{v}'(t')$) based on where it is now, which allows us to integrate the effect of the wave perturbations along that precise helical path.


>> **Appednix: cyclotron and gyration term dicussion


>>Of course. This is an excellent question that gets to the heart of the history and intuition behind plasma physics. The names "cyclotron" and "gyration" are not arbitrary; they come directly from the technology used to discover and study this motion.
>>
>>### 1. Cyclotron Motion
>>
>>The term **"cyclotron"** comes from one of the earliest and most important types of **particle accelerators**, invented by Ernest O. Lawrence and M. Stanley Livingston in 1932.
>>
>>**How a Cyclotron Works:**
>>1.  It consists of two hollow "D"-shaped electrodes (called "dees") placed in a strong, constant vertical magnetic field, **B₀**.
>>2.  A charged particle (e.g., a proton) is injected near the center.
>>3.  The magnetic field forces the particle to move in a **circular path** (just like in our plasma).
>>4.  An oscillating electric field is applied across the gap between the dees. Every time the particle crosses the gap, it gets a "kick" of energy, speeding it up.
>>5.  The key insight is that the **time for one complete circle (the period) is independent of the particle's speed** and radius. The formula is:
>>    $T = \frac{2\pi m}{qB}$
>>    The frequency, $f = \frac{1}{T} = \frac{qB}{2\pi m}$, is the **cyclotron frequency** ($\omega_c = 2\pi f = \frac{qB}{m}$).
>>6.  Because the period is constant, the electric field can be oscillated at a fixed frequency, perfectly timing the "kicks" to accelerate the particle each time it crosses the gap. The particle spirals outward until it reaches the edge and is extracted.
>>
>>**Why the Name?** The device was named for the **cyclical** (circular) path the particles follow and the **electronic** nature of its operation. The motion of particles in a magnetic field was thus named **cyclotron motion** after the device that so perfectly demonstrates it.
>>
>>### 2. Gyration
>>
>>The term **"gyration"** comes from the word **gyre**, which means a circular or spiral motion. It shares a root with words like:
>>*   **Gyroscope:** A device that uses the conservation of angular momentum to maintain its orientation. A spinning gyroscope "gyrates."
>>*   **Gyro:** (as in the food) Named for the rotating spit of meat.
>>*   **Charybdis:** The famous whirlpool from Greek mythology was described as a "giant gyre."
>>
>>In physics, **gyration** is a more general term for this type of circular or spiral motion. When we say an electron *gyrates* around a magnetic field line, we are describing its fundamental circular path in the plane perpendicular to **B₀**.
>>
>>The center point of this circular motion is called the **guiding center**. The radius of the circle is the **Larmor radius** or **gyroradius**.
>>
>>---
>>
>>### Summary: Cyclotron vs. Gyration
>>
>>While often used interchangeably, here’s the subtle difference:
>>
>>| Feature | Cyclotron Motion | Gyration |
>>| :--- | :--- | :--- |
>>| **Origin of Term** | Named after the **cyclotron accelerator**. | From the general word **"gyre"** for a circular motion. |
>>| **Common Usage** | Often used when discussing the **frequency** ($\omega_c$) and the formal physics of the motion. | Often used as a more **general, descriptive term** for the particle's spiral path. |
>>| **Implied Focus** | The periodic, resonant nature of the motion. | The physical, circular path of the particle. |
>>| **Analogy** | It's like saying "engine rotation" based on the RPM of a car engine. | It's like saying "the wheels are spinning." |
>>
>>**Why are there two names?**
>>It's common in science for a single phenomenon to be named after both the device that discovered/proved it (**Cyclotron**) and the fundamental physical action it describes (**Gyration**).
>>
>>**In a nutshell:** A particle **gyrates** in a magnetic field. One full **gyration** occurs at the **cyclotron frequency**. The device that proved this and harnessed it is called a **cyclotron**.
>>
>>This is why the motion is helical: the constant-velocity motion along the field line (unaffected by **B₀**) combined with the circular **gyration** *around* the field line creates a corkscrew-like path, just like the outward spiral of a particle in a cyclotron.