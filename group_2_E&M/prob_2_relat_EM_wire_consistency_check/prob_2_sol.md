# Detailed Solution — Neutral Current-Carrying Wire (Polished & Canonical)

**Goal.** Solve each part in a path that upgrades intuition to covariant, graduate-ready reasoning. We keep signs explicit and match exactly the problem’s conventions.

**Conventions.** SI units, $c^{-2}=\epsilon_0\mu_0$. Cylindrical $(r,\phi,z)$. Unit vectors $\hat r,\hat\phi,\hat z$. Define the **algebraic** line current in $S$
$I_{\text{tot}}\equiv I_+ + I_- = \lambda_+ u_+ + \lambda_- u = 0 + \lambda_- u = -\lambda u.$
We also use the **magnitude** $I\equiv |\lambda_-|u=\lambda u>0$ when helpful, so $I_{\text{tot}}=-I$ (current points along $-\hat z$ since electrons move $+\hat z$). Lorentz factor $\gamma=1/\sqrt{1-\beta^2}$, $\beta=v/c$.

---

## Part 1 — Fields in the Lab Frame $S$

**(a) Electric field outside ($r>a$).** The wire is neutral in $S$: $\lambda_{\text{tot}}=\lambda_+ + \lambda_-=0$. Take a Gaussian cylinder of radius $r>a$, length $L$. Then
$\oint \vec E\cdot d\vec A = \frac{Q_{\text{enc}}}{\epsilon_0} = \frac{(\lambda_+ + \lambda_-)L}{\epsilon_0}=0.$
By symmetry the only allowed static field would be radial and uniform on the cylindrical surface; the only value consistent with zero flux is
$\boxed{\;\vec E(r>a)=\mathbf 0\;.}$
*Physical note.* In steady DC, surface-charge gradients exist to guide the interior current, but the **net external line charge** is zero, so the **external** $\vec E$ vanishes.

**(b) Magnetic field outside ($r>a$).** For a circular Amperian loop of radius $r$:
$\oint \vec B\cdot d\vec \ell = B_\phi(r)(2\pi r) = \mu_0 I_{\text{enc}} = \mu_0 I_{\text{tot}}.$
Hence
$\boxed{\;\vec B(r>a)=\frac{\mu_0 I_{\text{tot}}}{2\pi r}\,\hat\phi = -\,\frac{\mu_0 I}{2\pi r}\,\hat\phi\;.}$
(With our conventions $I_{\text{tot}}=-I$, the direction is $-\hat\phi$; right-hand rule around the $-\hat z$ current.)

---

## Part 2 — Field Transformation to $S'$

The fundamental idea is that what one observer measures as a pure magnetic field, another observer, moving relative to the first, will measure as a combination of electric and magnetic fields. **Electric and magnetic fields are not separate entities; they are two aspects of a single electromagnetic field, and their appearance depends on your state of motion.**

This is governed by the **Lorentz Transformation equations for the electromagnetic field**.

---

**The Tool:**

Boost $S'$ at $\vec v=v\,\hat z$. For a boost along the field symmetry axis and with $\vec E=\mathbf 0$ in $S$:
$\boxed{\;\vec E' = \gamma\,(\vec v\times\vec B),\qquad \vec B' = \gamma\,\vec B\;.}$
Compute directions. In $S$, $\vec v=+v\,\hat z$, $\vec B= (\mu_0 I_{\text{tot}}/2\pi r)\,\hat\phi$. Using $\hat z\times\hat\phi=-\hat r$:
$\vec v\times\vec B = v\,\hat z\times\Big(\frac{\mu_0 I_{\text{tot}}}{2\pi r}\,\hat\phi\Big) = -\,v\,\frac{\mu_0 I_{\text{tot}}}{2\pi r}\,\hat r.$
Therefore
$\boxed{\;\vec E'(r) = -\,\gamma\,\frac{\mu_0 v I_{\text{tot}}}{2\pi r}\,\hat r,\qquad \vec B'(r)= \gamma\,\frac{\mu_0 I_{\text{tot}}}{2\pi r}\,\hat\phi\;.}$


**Interpretation for \vect{E}':** An observer moving along the wire will measure a **radial electric field**. The direction depends on the signs of $v$ and $I$. If they are moving in the same direction as the conventional current ($v>0$, $I>0$), the field points **inwards** ($-\hat{r}$), meaning the wire appears **negatively charged** to them.

**Interpretation for \vect{B}':** The magnetic field is still there, and it's **stronger** by a factor of $\gamma$. The moving observer also sees a magnetic field because they see a current (the "stationary" ions are now moving backwards from their perspective).

---

## Part 3 — Direct Source Transformation in $S'$ (No Paradox)

Treat ions and electrons via **line 4-currents** $\mathcal J_\pm^\mu=(c\,\lambda_\pm,\,I_\pm,\,0,\,0)$. In $S$: $I_+=0$ (ions at rest), $I_-=\lambda_- u = I_{\text{tot}}$.

A boost along $\hat z$ gives (SI):
$\boxed{\;\lambda' = \gamma\Big(\lambda - \frac{v}{c^2}I\Big),\qquad I' = \gamma\,(I - v\lambda)\;.}$
Apply to each species:
$\lambda'_+ = \gamma\lambda_+,\quad I'_+ = -\gamma v\lambda_+;\qquad \lambda'_- = \gamma\Big(\lambda_- - \frac{v}{c^2}I_-\Big),\quad I'_- = \gamma\big(I_- - v\lambda_-\big).$
Sum to totals, using neutrality $\lambda_+ + \lambda_-=0$:
$\boxed{\;\lambda'_{\text{tot}} = \lambda'_+ + \lambda'_- = -\,\gamma\,\frac{v}{c^2}\,I_{\text{tot}},\qquad I'_{\text{tot}}= I'_+ + I'_- = \gamma\,I_{\text{tot}}\;.}$
*Interpretation.* If $v>0$ while $I_{\text{tot}}<0$ (our case), then $\lambda'_{\text{tot}}>0$: the wire is **positively** charged in $S'$, consistent with the outward $\vec E'$ above.

**Direct Gauss-law check.** Using $\lambda'_{\text{tot}}$ in $S'$:
$\vec E'_{\text{direct}}(r) = \frac{\lambda'_{\text{tot}}}{2\pi\epsilon_0 r}\,\hat r = -\,\gamma\,\frac{v}{c^2}\,\frac{I_{\text{tot}}}{2\pi\epsilon_0 r}\,\hat r = -\,\gamma\,\frac{\mu_0 v I_{\text{tot}}}{2\pi r}\,\hat r,$
which **exactly matches** Part 2. No paradox appears when sources are transformed covariantly.

*(Optional velocity-addition cross-check.)* The electron speed in $S'$ is $u'=(u-v)/(1-uv/c^2)$. One can verify that $I'_- = \lambda'_- u'$ matches the 4-current result above.

## Part 4 — Self-Consistent Fields in $S'$ from Transformed Sources

From Part 3, the **total** line sources in $S'$ are $\lambda'_{\text{tot}}= -\gamma(v/c^2) I_{\text{tot}}$ and $I'_{\text{tot}}=\gamma I_{\text{tot}}$. Outside the wire ($r>a$):

* **Gauss (again):** $\displaystyle \vec E'(r)=\frac{\lambda'_{\text{tot}}}{2\pi\epsilon_0 r}\,\hat r = -\,\gamma\,\frac{\mu_0 v I_{\text{tot}}}{2\pi r}\,\hat r$.
* **Ampère:** $\displaystyle \vec B'(r)=\frac{\mu_0 I'_{\text{tot}}}{2\pi r}\,\hat\phi = \gamma\,\frac{\mu_0 I_{\text{tot}}}{2\pi r}\,\hat\phi$.

These coincide with the transformed fields in Part 2.

**Key boxed relations (remember signs):**
$\boxed{\;\lambda'_{\text{tot}}=-\gamma\,\frac{v}{c^2}\,I_{\text{tot}},\qquad I'_{\text{tot}}=\gamma\,I_{\text{tot}}\;}$
$\boxed{\;\vec E'(r)=\frac{\lambda'_{\text{tot}}}{2\pi\epsilon_0 r}\,\hat r,\qquad \vec B'(r)=\frac{\mu_0 I'_{\text{tot}}}{2\pi r}\,\hat\phi\;.}$




---

>
>## Appendix explanation of part 3_4

>
>
>### Step-by-Step Explanation of the Lorentz Transformation for the 4-Current
>
>In special relativity, the electromagnetic field is described in terms of the **4-current**, which combines charge density and current density into a single four-vector. This allows us to apply Lorentz transformations to find how these quantities change between inertial frames.
>
>#### 1. **Definition of the 4-Current**
>For a continuous distribution, the 4-current is defined as:
>$$
>J^\mu = (c\rho, \vec{J})
>$$
>where:
>- $\rho$ is the volume charge density,
>- $\vec{J}$ is the volume current density vector.
>
>For an infinite straight wire along the $z$-axis, we often work with **linear charge density** $\lambda$ and **current** $I$. The volume densities relate to linear densities as:
>$$
>\rho = \frac{\lambda}{A}, \quad J_z = \frac{I}{A}
>$$
>where $A$ is the cross-sectional area of the wire. Since a boost along the $z$-axis does not affect the transverse dimensions (no contraction perpendicular to motion), $A$ remains invariant. Thus, the linear densities $\lambda$ and $I$ transform similarly to the volume densities $\rho$ and $J_z$. We can define an effective **linear 4-current** for the wire:
>$$
>\mathcal{J}^\mu = (c\lambda, 0, 0, I)
>$$
>where $I$ is the current in the $z$-direction.
>
>#### 2. **Lorentz Transformation for a Boost Along $z$**
>Consider a frame $S'$ moving with velocity $\vec{v} = v \hat{z}$ relative to the lab frame $S$. The Lorentz transformation for a four-vector $A^\mu = (A^0, A^1, A^2, A^3)$ under a boost along $z$ is:
>$$
>\begin{aligned}
>A'^0 &= \gamma (A^0 - \beta A^3) \\
>A'^1 &= A^1 \\
>A'^2 &= A^2 \\
>A'^3 &= \gamma (A^3 - \beta A^0)
>\end{aligned}
>$$
>where $\beta = v/c$ and $\gamma = 1/\sqrt{1 - \beta^2}$.
>
>Applying this to the linear 4-current $\mathcal{J}^\mu = (c\lambda, 0, 0, I)$:
>$$
>\begin{aligned}
>\mathcal{J}'^0 &= \gamma (c\lambda - \beta I) \\
>\mathcal{J}'^3 &= \gamma (I - \beta c\lambda)
>\end{aligned}
>$$
>Since $\mathcal{J}'^1$ and $\mathcal{J}'^2$ are zero, they remain zero in $S'$. Thus, in $S'$, the linear 4-current is:
>$$
>\mathcal{J}'^\mu = (c\lambda', 0, 0, I')
>$$
>where:
>$$
>\boxed{
>\begin{aligned}
>\lambda' &= \gamma \left( \lambda - \frac{v}{c^2} I \right) \\
>I' &= \gamma (I - v \lambda)
>\end{aligned}
>}
>$$
>These equations describe how the linear charge density and current transform under a boost along the wire.
>
>#### 3. **Application to the Neutral Current-Carrying Wire**
>In the lab frame $S$:
>- The wire is neutral: $\lambda_{\text{total}} = \lambda_+ + \lambda_- = 0$.
>- The current is $I_{\text{total}} = \lambda_- u = -I$, where $I = |\lambda_-| u > 0$ is the magnitude of the current (since electrons have $\lambda_- = -\lambda$ and drift with speed $u$).
>
>Substituting into the transformation equations:
>$$
>\begin{aligned}
>\lambda'_{\text{total}} &= \gamma \left( 0 - \frac{v}{c^2} I_{\text{total}} \right) = -\gamma \frac{v}{c^2} I_{\text{total}} \\
>I'_{\text{total}} &= \gamma (I_{\text{total}} - v \cdot 0) = \gamma I_{\text{total}}
>\end{aligned}
>$$
>Using $I_{\text{total}} = -I$:
>$$
>\boxed{
>\begin{aligned}
>\lambda'_{\text{total}} &= \gamma \frac{v}{c^2} I \\
>I'_{\text{total}} &= -\gamma I
>\end{aligned}
>}
>$$
>
>**Interpretation:**
>- In frame $S'$, the wire has a **net charge density** $\lambda'_{\text{total}} \neq 0$. For example, if $v > 0$ and $I > 0$, then $\lambda'_{\text{total}} > 0$, meaning the wire appears positively charged.
>- The current in $S'$ is $I'_{\text{total}} = -\gamma I$, which is larger in magnitude by a factor of $\gamma$ and flows in the negative $z$-direction.
>
>#### 4. **Calculating Fields in $S'$ from Transformed Sources**
>Using the transformed sources, we apply Gauss's law and Ampère's law in frame $S'$ to find the fields.
>
>- **Electric field via Gauss's law:**
>  For an infinite wire with linear charge density $\lambda'_{\text{total}}$, the electric field is radial:
>  $$
>  \vec{E}'(r) = \frac{\lambda'_{\text{total}}}{2\pi \epsilon_0 r} \hat{r} = \frac{\gamma \frac{v}{c^2} I}{2\pi \epsilon_0 r} \hat{r}
>  $$
>  Using $c^2 = 1/(\epsilon_0 \mu_0)$, so $\frac{1}{c^2 \epsilon_0} = \mu_0$:
>  $$
>  \boxed{\vec{E}'(r) = \frac{\gamma \mu_0 v I}{2\pi r} \hat{r}}
>  $$
>
>- **Magnetic field via Ampère's law:**
>  For an infinite wire with current $I'_{\text{total}}$, the magnetic field is azimuthal:
>  $$
>  \vec{B}'(r) = \frac{\mu_0 I'_{\text{total}}}{2\pi r} \hat{\phi} = \frac{\mu_0 (-\gamma I)}{2\pi r} \hat{\phi} = -\frac{\mu_0 \gamma I}{2\pi r} \hat{\phi}
>  $$
>  This matches the result from the field transformation $\vec{B}' = \gamma \vec{B}$, where $\vec{B} = -\frac{\mu_0 I}{2\pi r} \hat{\phi}$ in $S$.
>
>>#### 5. **Consistency with Field Transformation**
>The fields derived directly from the transformed sources in $S'$ agree exactly with those obtained by applying the Lorentz transformation to the fields in $S$. This demonstrates the consistency of electromagnetism with special relativity:
>- The Lorentz transformation of the 4-current correctly accounts for changes in charge and current densities.
>- Maxwell's equations (Gauss's and Ampère's laws) hold in all inertial frames.
>
>The apparent "paradox" (a neutral wire in $S$ appears charged in $S'$) is resolved by recognizing that charge density is not Lorentz invariant when a current is present. This highlights the relativistic unity of electricity and magnetism.
>
>>
>>
>>
>>

---





## Part 5 — Consistency Checks (Recommended)

**(a) Test charge moving with $v$ in $S$.** At radius $r>a$, $\vec F = q\,\vec v\times\vec B = q\,v\,(\mu_0 I_{\text{tot}}/2\pi r)(-\hat r)$. In $S'$ (particle at rest), $\vec F' = q\,\vec E' = q\,\big(-\gamma\mu_0 v I_{\text{tot}}/2\pi r\big)\hat r$. Magnitudes satisfy $|\vec F'|=\gamma|\vec F|$ (transverse-force law), confirming dynamical consistency.

**(b) Field invariants.** In $S$: $E=0$ ⇒ $\mathcal I_1=E^2-c^2B^2=-c^2(\mu_0 I_{\text{tot}}/2\pi r)^2<0$, $\mathcal I_2=\vec E\cdot\vec B=0$. These are invariant; hence in $S'$ also $\mathcal I_1<0$ and $\mathcal I_2=0$: the configuration is **magnetically dominated** with $\vec E'\perp\vec B'$ in all frames and no frame exists where $\vec B$ vanishes.

---

> ## Appendix: Expalanation of Part 5

> **Part 5: The Consistency Checks**. This part is not a new calculation but a crucial verification step. It answers the question: **"Now that we have these answers from different methods, can we prove they make sense within the larger framework of relativity?"**
>
>It does this by testing two fundamental principles:
>1.  The relativistic transformation of force.
>2.  The existence of frame-independent Lorentz invariants.
>
>These checks are the final seal of approval on our solution.
>
>---
>
>### Part 5a: Consistency Check with a Test Charge
>
>**The Goal:** To show that the force on a moving test charge, calculated in two different frames, obeys the correct relativistic transformation law.
>
>**The Setup:**
>*   In the **Lab Frame (S)**: A test charge $q$ is moving with velocity $\vec{v} = v \hat{z}$ (the same velocity as the $S'$ frame). It is at a distance $r$ from the wire.
>*   In the **Moving Frame (S')**: This same test charge is **at rest**.
>
>**Step 1: Calculate the Force in Frame S**
>In frame S:
>*   $\vec{E} = 0$
>*   $\vec{B} = \frac{\mu_0 I}{2\pi r} (-\hat{\phi})$ (assuming electron flow for current)
>*   The force on a moving charge is the Lorentz force:
>    $\vec{F} = q(\vec{E} + \vec{v} \times \vec{B}) = q(\vec{v} \times \vec{B})$
>*   $\vec{v} = v \hat{z}$ and $\vec{B} = B_\phi (-\hat{\phi})$, so:
>    $\vec{v} \times \vec{B} = (v \hat{z}) \times (-B_\phi \hat{\phi}) = -v B_\phi (\hat{z} \times \hat{\phi})$
>*   We know $\hat{z} \times \hat{\phi} = -\hat{r}$, so:
>    $\vec{v} \times \vec{B} = -v B_\phi (-\hat{r}) = v B_\phi \hat{r}$
>*   Therefore, the force is:
>    $\vec{F} = q v B_\phi \hat{r} = q v \left(\frac{\mu_0 I}{2\pi r}\right) \hat{r}$
>*   Its magnitude is $|\vec{F}| = \dfrac{q v \mu_0 I}{2\pi r}$
>
>**Step 2: Calculate the Force in Frame S'**
>In frame S':
>*   The test charge is at rest ($\vec{v}'=0$), so the magnetic force is zero.
>*   The force is purely electric:
>    $\vec{F}' = q \vec{E}'$
>*   From our previous calculations:
>    $\vec{E}' = \frac{\gamma \mu_0 v I}{2\pi r} \hat{r}$
>*   Therefore:
>    $\vec{F}' = q \left(\frac{\gamma \mu_0 v I}{2\pi r}\right) \hat{r}$
>*   Its magnitude is $|\vec{F}'| = \dfrac{q \gamma v \mu_0 I}{2\pi r}$
>
>**Step 3: The Relativistic Force Transformation**
>For a force that is **perpendicular** to the relative motion between frames (a *transverse* force), the special relativistic transformation law is:
>$$\boxed{F'_\perp = \gamma F_\perp}$$
>
>**Compare the Results:**
>*   $F_\perp = |\vec{F}| = \dfrac{q v \mu_0 I}{2\pi r}$
>*   $F'_\perp = |\vec{F}'| = \gamma \dfrac{q v \mu_0 I}{2\pi r} = \gamma F_\perp$
>
>**Conclusion of Check 5a:** The forces calculated in the two different frames obey the correct relativistic law. The magnetic force in S is measured as an electric force in S', and their magnitudes are related by the Lorentz factor $\gamma$. The dynamics are consistent.
>
>---
>
>### Part 5b: Consistency Check with Field Invariants
>
>**The Goal:** To show that our field transformations preserve the fundamental Lorentz invariants built from $\vec{E}$ and $\vec{B}$. These invariants are true for all observers, no matter their inertial frame.
>
>**The Invariants:**
>1.  $\mathcal{I}_1 = E^2 - c^2B^2$ (Scalar Invariant)
>2.  $\mathcal{I}_2 = \vec{E} \cdot \vec{B}$ (Pseudoscalar Invariant)
>
>**Step 1: Calculate the Invariants in Frame S**
>In the lab frame:
>*   $\vec{E} = 0$
>*   $\vec{B} = \frac{\mu_0 I}{2\pi r} (-\hat{\phi})$, so $B^2 = \left(\frac{\mu_0 I}{2\pi r}\right)^2$
>*   $\mathcal{I}_1 = (0)^2 - c^2 \left(\frac{\mu_0 I}{2\pi r}\right)^2 = -c^2 \left(\frac{\mu_0 I}{2\pi r}\right)^2$
>*   $\mathcal{I}_2 = \vec{E} \cdot \vec{B} = 0$
>
>**Step 2: Calculate the Invariants in Frame S'**
>In the moving frame:
>*   $\vec{E}' = \frac{\gamma \mu_0 v I}{2\pi r} \hat{r}$, so $E'^2 = \left(\frac{\gamma \mu_0 v I}{2\pi r}\right)^2$
>*   $\vec{B}' = \gamma \frac{\mu_0 I}{2\pi r} (-\hat{\phi})$, so $B'^2 = \gamma^2 \left(\frac{\mu_0 I}{2\pi r}\right)^2$
>*   $\mathcal{I}_1' = E'^2 - c^2 B'^2 = \gamma^2 \left(\frac{\mu_0 I}{2\pi r}\right)^2 (v^2 - c^2)$
>Notice that $(v^2 - c^2) = -c^2 (1 - v^2/c^2) = -c^2 / \gamma^2$.
>*   Therefore:
>    $\mathcal{I}_1' = \gamma^2 \left(\frac{\mu_0 I}{2\pi r}\right)^2 \left(-\frac{c^2}{\gamma^2}\right) = -c^2 \left(\frac{\mu_0 I}{2\pi r}\right)^2$
>*   $\mathcal{I}_2' = \vec{E}' \cdot \vec{B}' = \left(\frac{\gamma \mu_0 v I}{2\pi r} \hat{r}\right) \cdot \left(\gamma \frac{\mu_0 I}{2\pi r} (-\hat{\phi})\right) = 0$ (since $\hat{r} \cdot \hat{\phi} = 0$)
>
>**Step 3: Compare the Invariants**
>*   $\mathcal{I}_1 = -c^2 \left(\frac{\mu_0 I}{2\pi r}\right)^2$ and $\mathcal{I}_1' = -c^2 \left(\frac{\mu_0 I}{2\pi r}\right)^2$  ✅
>*   $\mathcal{I}_2 = 0$ and $\mathcal{I}_2' = 0$  ✅
>
>**Conclusion of Check 5b:** The values of the Lorentz invariants are identical in both frames. This proves our field transformations are correct and consistent with the structure of relativistic electromagnetism.
>
>**Physical Interpretation of the Invariants:**
>*   $\mathcal{I}_1 < 0$: The field configuration is **magnetically dominated**. There is no inertial frame where the magnetic field vanishes.
>*   $\mathcal{I}_2 = 0$: The electric and magnetic fields are **perpendicular** to each other in all frames.
>
>---
>
>### Summary of Part 5
>
>Part 5 is the "sanity check" that proves our entire solution is self-consistent and conforms to the deeper laws of special relativity. It shows:
>
>1.  **Forces transform correctly**, ensuring the laws of mechanics and electromagnetism agree across different reference frames.
>2.  **The fundamental building blocks of the EM field ($\mathcal{I}_1$ and $\mathcal{I}_2$) are invariant**, proving that our field transformations are mathematically and physically sound.
>
>Without these checks, we would just have two sets of answers that agree numerically. With these checks, we *prove* that they *must* agree, and we demonstrate a profound feature of our universe: the laws of physics are the same for all inertial observers.

---


## Bonus — Dual Symmetry and Magnetic Monopoles (Sketch)

Introduce magnetic charge/current densities $(\rho_m,\,\vec J_m)$ and a magnetic charge $q_m$ for test particles. A dual-symmetric SI formulation:
$\nabla\!\cdot\!\vec E=\rho_e/\epsilon_0,\quad \nabla\!\times\!\vec B-\mu_0\epsilon_0\,\partial_t\vec E=\mu_0\vec J_e,$
$\nabla\!\cdot\!\vec B=\mu_0\rho_m,\quad -\nabla\!\times\!\vec E-\partial_t\vec B=\mu_0\vec J_m.$
Generalized Lorentz force (dyon of charges $q_e,q_m$):
$\boxed{\;\vec F = q_e(\vec E+\vec v\times\vec B)\; +\; q_m\Big(\vec B-\frac{\vec v\times\vec E}{c^2}\Big)\;.}$
Covariantly, $\partial_\mu F^{\mu\nu}=\mu_0 J_e^{\,\nu}$, $\partial_\mu {}^*F^{\mu\nu}=\mu_0 K^{\nu}$ with $K^\nu=(c\rho_m,\vec J_m)$, and 4-force
$f^\mu = q_e F^{\mu\nu}u_\nu + q_m\,{}^*F^{\mu\nu}u_\nu/c.$
Under Lorentz boosts, $J_e^\mu$ and $K^\mu$ transform as 4-vectors; a **pure magnetic current** in one frame generates fields that mix exactly as an electric current does (by duality $F\leftrightarrow {}^*F$). Thus the “electric ↔ magnetic” story mirrors our wire analysis.

---

## Takeaway

* In $S$: $\vec E=0$, $\vec B\propto I_{\text{tot}}/r$.
* Boost along $\hat z$: charge–current mix to $\lambda'_{\text{tot}}=-\gamma(v/c^2)I_{\text{tot}}$, $I'_{\text{tot}}=\gamma I_{\text{tot}}$.
* Outside fields in $S'$: $\vec E'=(\lambda'_{\text{tot}}/2\pi\epsilon_0 r)\hat r$, $\vec B'=(\mu_0 I'_{\text{tot}}/2\pi r)\hat\phi$, matching the direct Lorentz transform.
* Magnetism is the relativistic face of electricity; dual symmetry would make this statement literally two-sided if monopoles existed.


















Of course. Let's break down **Part 2 / B** of the problem, which is the heart of the relativistic revelation. This is the part where you discover that a purely magnetic field in one frame becomes a mix of electric and magnetic fields in another.

### The Core Concept: Relativity of Fields

The fundamental idea is that what one observer measures as a pure magnetic field, another observer, moving relative to the first, will measure as a combination of electric and magnetic fields. **Electric and magnetic fields are not separate entities; they are two aspects of a single electromagnetic field, and their appearance depends on your state of motion.**

This is governed by the **Lorentz Transformation equations for the electromagnetic field**.

---

### Step-by-Step Explanation of Part 2

**Goal:** We are in the lab frame ($S$). We have calculated that for our neutral, current-carrying wire:
*   $\vec{E} = 0$
*   $\vec{B} = \frac{\mu_0 I}{2\pi r} \hat{\phi}$ (or $-\hat{\phi}$ depending on your sign convention for $I$)

Now, we want to find the fields $\vec{E'}$ and $\vec{B'}$ that would be measured by an observer in frame $S'$, which is moving with velocity $\vec{v} = v \hat{z}$ relative to $S$.

**The Tool:** The Lorentz Transformation for Fields for a boost along the $z$-axis:

$$
\begin{aligned}
E'_x &= \gamma(E_x - v B_y) \\
E'_y &= \gamma(E_y + v B_x) \\
E'_z &= E_z \\
\\
B'_x &= \gamma(B_x + (v/c^2) E_y) \\
B'_y &= \gamma(B_y - (v/c^2) E_x) \\
B'_z &= B_z \\
\end{aligned}
$$

**Our Specific Case is Much Simpler:**

1.  In our frame $S$, $\vec{E} = 0$. This immediately simplifies the equations *dramatically*. All terms with $E_x, E_y, E_z$ vanish.

2.  Our magnetic field in $S$ is purely azimuthal: $\vec{B} = (0, B_\phi, 0)$ in Cartesian components. (We have to remember that $\hat{\phi}$ is not a fixed direction like $\hat{x}$ or $\hat{y}$; it depends on the position around the wire. This is crucial).

Because of point 1, the general transformation rules collapse to a very simple form:
$$
\boxed{\vec{E}' = \gamma (\vec{v} \times \vec{B})} \quad \text{and} \quad \boxed{\vec{B}' = \gamma \vec{B}}
$$
*These are the "compact forms" mentioned in the problem statement. They are only valid when $\vec{E}=0$ and the boost is perpendicular to $\vec{B}$.*

**Let's calculate step by step:**

1.  **Calculate $\vec{E}'$:**
    *   $\vec{v} = v \hat{z}$
    *   $\vec{B} = B_\phi \hat{\phi} = \frac{\mu_0 I}{2\pi r} \hat{\phi}$
    *   We need the cross product: $\vec{v} \times \vec{B} = (v \hat{z}) \times (B_\phi \hat{\phi})$

    **This is the key geometric step.** You must know how the cylindrical unit vectors relate to each other. The rule is:
    $\hat{z} \times \hat{\phi} = -\hat{r}$
    *(You can derive this: At a point $(x,y,z)$, $\hat{\phi} = (-\sin\phi, \cos\phi, 0)$ and $\hat{z} = (0,0,1)$. Their cross product is $(-\cos\phi, -\sin\phi, 0) = -\hat{r}$).*

    Therefore:
    $\vec{v} \times \vec{B} = v B_\phi (\hat{z} \times \hat{\phi}) = v B_\phi (-\hat{r}) = -v B_\phi \hat{r}$

    Now plug this into the formula for $\vec{E}'$:
    $\vec{E}' = \gamma (\vec{v} \times \vec{B}) = \gamma (-v B_\phi \hat{r}) = -\gamma v \frac{\mu_0 I}{2\pi r} \hat{r}$

    **Interpretation:** An observer moving along the wire will measure a **radial electric field**. The direction depends on the signs of $v$ and $I$. If they are moving in the same direction as the conventional current ($v>0$, $I>0$), the field points **inwards** ($-\hat{r}$), meaning the wire appears **negatively charged** to them.

2.  **Calculate $\vec{B}'$:**
    *   This one is straightforward from the simplified formula:
    $\vec{B}' = \gamma \vec{B} = \gamma \frac{\mu_0 I}{2\pi r} \hat{\phi}$

    **Interpretation:** The magnetic field is still there, and it's **stronger** by a factor of $\gamma$. The moving observer also sees a magnetic field because they see a current (the "stationary" ions are now moving backwards from their perspective).

---

### Why This Happens: The Physical Picture

The math gives us the answer, but *why* does an electric field appear?

1.  **In Frame $S$ (Lab Frame):**
    *   The positive ions are at rest.
    *   The electrons are moving, creating a current $I$.
    *   The wire is neutral ($\lambda_+ + \lambda_- = 0$), so no *net* electric field.
    *   The current $I$ creates the magnetic field $\vec{B}$.

2.  **In Frame $S'$ (Moving Frame):**
    *   Due to **Lorentz contraction**, distances are not the same.
    *   The **positive ions**, which were at rest in $S$, are now moving backwards with speed $-v$ in $S'$. Their charge density *increases* because the distance between them is contracted: $\lambda'_+ = \gamma \lambda_+$.
    *   The **electrons** were already moving in $S$. Their new speed in $S'$ must be calculated by relativistic velocity addition. Their charge density also changes to $\lambda'_-$.
    *   **Crucially, these two densities do not cancel out anymore!** The Lorentz contraction factor is different for the two species because they have different velocities. The calculation in Part 3 shows that the total charge density becomes $\lambda'_{\text{total}} = -\gamma \frac{v}{c^2} I \neq 0$.
    *   **A wire with a net charge must produce an electric field.** This is exactly what Gauss's law in $S'$ gives us, and it matches perfectly with the $\vec{E}'$ we found by transforming the fields.
    *   The current in $S'$ is also different, leading to the modified magnetic field $\vec{B}' = \gamma \vec{B}$.

**In summary:** The "paradox" is resolved by realizing that **charge density is not Lorentz invariant**. A configuration that is neutral in one frame will not generally be neutral in another frame if there is a current. The Lorentz transformation of the fields (Part 2) and the careful relativistic transformation of the sources (Part 3) are two different ways of calculating the same physical reality, and they must—and do—agree. This is the beautiful consistency of physics.




