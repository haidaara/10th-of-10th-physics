# A Challenging Problem in Electromagnetism and Special Relativity

#### The Field of a Moving Neutral, Current-Carrying Wire (Polished Canonical Version)

**Physical setup (Lab frame $S$)**
An infinitely long, straight cylindrical wire (radius $a$) lies along the $z$-axis. It contains:

* **Positive ions** fixed in the lattice with linear density $\lambda_+ = +\lambda$.
* **Conduction electrons** drifting with velocity $\vec u = u\,\hat z$ and linear density $\lambda_- = -\lambda$.

Hence, in $S$: neutrality holds $\lambda_{\text{tot}}=\lambda_++\lambda_- = 0$, while the steady current is
$\displaystyle \vec I = \lambda_- u\,\hat z = -\lambda u\,\hat z$ (take $I\equiv |\lambda_-|u>0$).

**Assumptions**
Steady state, cylindrical symmetry, analysis in the **exterior region** $r>a$ (no radiation), SI units with $c^{-2}=\epsilon_0\mu_0$.

---

#### Part 1 — Fields in the Lab Frame $S$

**(a)** Using Gauss’s law and neutrality, determine $\vec E(r)$ for $r>a$.
**(b)** Using Ampère’s law, determine $\vec B(r)$ for $r>a$ and give its direction.

---

#### Part 2 — Field Transformation to $S'$

Let $S'$ move at speed $\vec v = v\,\hat z$ relative to $S$. Using the Lorentz field transformation for a boost along $\hat z$, compute $\vec E'$ and $\vec B'$ from your Part 1 fields. (Here, because $\vec E=0$ in $S$ and the boost is parallel to $\hat z$, you may use the compact forms $\vec E' = \gamma\, (\vec v\times \vec B)$, $\vec B' = \gamma\,\vec B$.)

---

#### Part 3 — Direct Source Transformation in $S'$ (No Paradox)

Work species-wise with **4-current transforms** to avoid length-contraction pitfalls. Define species line 4-currents $\mathcal J_\pm^\mu=(c\,\lambda_\pm,\,I_\pm,\,0,\,0)$, where $I_+=0$ (ions at rest in $S$) and $I_- = \lambda_- u$.

**(a)** Positive ions (rest in $S$):
$\boxed{\;\lambda'_+ = \gamma\,\lambda_+,\qquad I'_+ = -\gamma v\,\lambda_+\;}$
**(b)** Electrons (moving in $S$):
$\boxed{\;\lambda'_- = \gamma\Big(\lambda_- - \tfrac{v}{c^2} I_-\Big),\qquad I'_- = \gamma\big(I_- - v\lambda_-\big)\;}$
(You may compute the electron speed in $S'$ via velocity addition if you wish, but it is **not required** for the densities.)

**(c)** Show that the **total** line charge and current in $S'$ are
$\boxed{\;\lambda'_{\text{tot}} = \lambda'_+ + \lambda'_- = -\gamma\,\frac{v}{c^2}\,I,\qquad I' = I'_+ + I'_-= \gamma I\;}$
with $I\equiv |\lambda_-|u$. Interpret the sign of $\lambda'_{\text{tot}}$ when $v>0$ and current flows along $+\hat z$.

**(d)** Using **Gauss’s law in $S'$** with $\lambda'_{\text{tot}}$, find the direct field
$\boxed{\;\vec E'_{\text{direct}}(r) = \frac{\lambda'_{\text{tot}}}{2\pi\epsilon_0 r}\,\hat r = -\frac{\gamma\mu_0 v I}{2\pi r}\,\hat r\;}$
and compare it to your $\vec E'$ from Part 2. **They match exactly.** (Any “paradox” only appears if one omits the proper source transformation.)

---

#### Part 4 — Self-Consistent Fields in $S'$ from Transformed Sources

**(a)** Using $I'_+$ and $I'_-$ from Part 3, compute the **total** current $I'_{\text{tot}}$ (it must equal $\gamma I$).
**(b)** Apply Ampère’s law in $S'$ to obtain
$\boxed{\;\vec B'(r) = \frac{\mu_0 I'}{2\pi r}\,\hat\phi = \frac{\mu_0\gamma I}{2\pi r}\,\hat\phi\;}$
which coincides with the transformed field from Part 2.
**(c)** Summarize the two **key boosted source relations**:
$\boxed{\;\lambda'_{\text{tot}}=-\gamma\frac{v}{c^2}I,\qquad I' = \gamma I\;}$
leading to the exterior fields
$\boxed{\;\vec E'(r)=\frac{\lambda'_{\text{tot}}}{2\pi\epsilon_0 r}\,\hat r,\qquad \vec B'(r)=\frac{\mu_0 I'}{2\pi r}\,\hat\phi\;}$
in full agreement with Part 2.

---

#### Part 5 — Consistency Checks (Recommended)

**(a) Test charge.** A charge $q$ moving at speed $v$ along $+\hat z$ in $S$ experiences $\vec F=q\,\vec v\times\vec B$. In $S'$ (where that particle is at rest), $\vec F'=q\,\vec E'$. Show the transverse-force scaling $|\vec F'|=\gamma|\vec F|$.

**(b) Field invariants.** Evaluate $\mathcal I_1=E^2-c^2B^2$ and $\mathcal I_2=\vec E\cdot\vec B$ in both frames and confirm $\mathcal I_1<0$, $\mathcal I_2=0$ (magnetically dominated, orthogonal fields in all frames).

---

#### Bonus — Dual Symmetry and Magnetic Monopoles

If magnetic charges $q_m$ exist with densities $(\rho_m,\,\vec J_m)$, the dual-symmetric Maxwell–Lorentz system in SI can be written
$\nabla\cdot\vec E=\rho_e/\epsilon_0,\quad \nabla\times\vec B-\mu_0\epsilon_0\,\partial_t\vec E=\mu_0\vec J_e,$
$\nabla\cdot\vec B=\mu_0\rho_m,\quad -\nabla\times\vec E-\partial_t\vec B=\mu_0\vec J_m,$
with generalized Lorentz force
$\boxed{\;\vec F = q_e(\vec E+\vec v\times\vec B) + q_m\Big(\vec B-\frac{\vec v\times\vec E}{c^2}\Big)\;}$
and corresponding covariant forms using $F^{\mu\nu}$ and its dual ${}^*F^{\mu\nu}$. Show that a pure magnetic current transforms analogously to an electric current under Lorentz boosts (duality).

---

#### Deliverables (for students)

* Derivations for Parts 1–4 with diagrams and explicit directions/signs.
* Short write-up for Part 5 checks.
* (Optional) Dual-symmetry bonus.
