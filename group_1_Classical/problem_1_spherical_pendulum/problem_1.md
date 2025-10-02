# Spherical Pendulum with an Offset Spring — Compact Problem

**Setup (use throughout):** Pivot at origin, +z up, gravity $\vec g=-g\hat z$. Rod: length $\ell$ (rigid), mass $m$. Coordinates: $\theta\in[0,\pi]$ from +z, $\phi\in[0,2\pi)$. Bob: $\mathbf r_m=\ell(\sin\theta\cos\phi,\sin\theta\sin\phi,\cos\theta)$. Anchor: $O'=(0,0,-a)$, spring $k,\ell_0$. Distance: $s(\theta)=\sqrt{\ell^2+a^2+2a\ell\cos\theta}$. Energies: $T=\tfrac12 m\ell^2(\dot\theta^2+\sin^2\theta\,\dot\phi^2)$, $U_g=mg\ell\cos\theta$, $U_s=\tfrac12 k(s-\ell_0)^2$. Useful: $\partial s/\partial\theta=-(a\ell\sin\theta)/s$.

1. **Lagrangian.** Write $L=T-U_g-U_s$ explicitly in $\theta,\phi,\dot\theta,\dot\phi$.

2. **Euler–Lagrange equations.** Derive the $\theta$- and $\phi$-equations. Show $\partial L/\partial\phi=0$ (axial symmetry) and substitute $\partial s/\partial\theta$.

3. **Momenta & Energy.** Compute $p_\theta=\partial L/\partial\dot\theta$, $p_\phi=\partial L/\partial\dot\phi$. Obtain the Hamiltonian $H$ via Legendre transform and verify $H=T+U$.

4. **Symmetries & Integrals.** Identify conserved **energy** $H$ and **axial angular momentum** $L_z=p_\phi$. State which components of $\mathbf L$ are not conserved and conclude the system is Liouville‑integrable with $(H,L_z)$.

5. **1D Reduction (effective potential).** For fixed $L_z$, reduce to
   $H=\frac{p_\theta^2}{2m\ell^2}+U_{\rm eff}(\theta;L_z),\quad U_{\rm eff}=\frac{L_z^2}{2m\ell^2\sin^2\theta}+mg\ell\cos\theta+\tfrac12 k(s-\ell_0)^2.$
   Find turning points and classify planar ($L_z=0$) vs. nutational ($L_z\neq0$) motion.

6. **Small Oscillations about bottom.** Let $\psi=\pi-\theta\ll1$; expand $T,U_g,U_s$ to quadratic order. Show isotropic transverse dynamics (no $\phi$ anisotropy) and derive
   $\boxed{\omega_0^2=\dfrac{g}{\ell}+\dfrac{k\,a}{m\ell}\,\dfrac{|\ell-a|-\ell_0}{|\ell-a|}}.$
   Conclude **no linear precession** for vertical offset.

7. **Relative Equilibria (conical motion) & stability.** Assume $\theta=\theta_*$, $\dot\phi=\omega_*$ constant. Derive algebraic existence condition using $s_*=s(\theta_*)$, then linearize to obtain nutation frequency and stability criterion.

8. **Rod Tension (constraint force).** Show
   $\boxed{T=m\ell(\dot\theta^2+\sin^2\theta\,\dot\phi^2)-mg\cos\theta-k\,(s-\ell_0)\,\frac{\ell+a\cos\theta}{s}}$
   and interpret (centripetal vs gravity vs spring). Check limits $k\to0$, $a\to0$.

9. **Special Regimes.** (i) $k=0$: recover standard spherical pendulum, $\omega_0=\sqrt{g/\ell}$. (ii) $g=0$: spring‑only equilibria and small $\omega_0$. (iii) $a=0$: spring adds constant only → same dynamics as standard case.

10. **Parameter Tuning (design knobs).** Find $\ell_0$ for which the spring does **not** change $\omega_0$ (answer: $\ell_0=|\ell-a|$). Determine when the spring **stiffens** vs **softens** the pendulum and explain physically.

11. **Bifurcations / Qualitative changes.** Vary $k,a,\ell_0$ and track equilibria/stability changes via $U_{\rm eff}$; sketch representative phase portraits.

12) **Lateral anchor offset (symmetry breaking).** Shift the anchor to \( \mathbf r_{O'}=(\varepsilon,0,-a) \) with \(0<\varepsilon\ll \ell\). (i) Write \( s(\theta,\phi)=\lVert \mathbf r_m-\mathbf r_{O'}\rVert \) and expand about the bottom (\( \psi=\pi-\theta\ll1\)) to first order in \( \varepsilon\). (ii) Derive the quadratic Lagrangian in local tangent-plane coordinates and show the loss of isotropy. (iii) Compute the two small-angle normal-mode frequencies \( \omega_1,\omega_2\) and show the **linear** frequency splitting \( \omega_2-\omega_1=\mathcal O(\varepsilon)\). (iv) For a nearly planar small oscillation, obtain the **precession rate** of the ellipse’s major axis, e.g. \( \Omega\approx(\omega_2-\omega_1)/2\), and verify \( \Omega\to0\) as \( \varepsilon\to0\). (v) Check consistency with items 6 & 9.

13. **Optional Advanced.** (a) Weakly nonlinear precession: compute leading $\Omega\propto \text{amplitude}^2$. (b) Period–energy relation: express $T_\theta(E,L_z)$ from the 1D reduction (elliptic integral). (c) Action–angle variables: define $J_\phi, J_\theta$ and discuss $(\omega_\theta,\omega_\phi)$ and resonances.

**Deliverables (suggested):** Concise derivations for 1–10; one plot of \(U_{\rm eff}\) and a phase portrait; short answers for 11; optional notes for 12–13.






