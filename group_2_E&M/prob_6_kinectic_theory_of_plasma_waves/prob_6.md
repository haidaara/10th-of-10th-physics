### **Advanced Problem: Kinetic Theory of Plasma Waves**

**Units**: SI units are used throughout. Thermal speed is defined as \( v_{th} = \sqrt{\frac{k_B T}{m}} \). For the plasma dispersion function, the Landau prescription implies \( \Im(\zeta) > 0 \).

Consider a homogeneous, magnetized plasma with electron density \( n_0 \), temperature \( T \), and a uniform static magnetic field \( \vec{B}_0 = B_0 \hat{z} \). Ions are stationary and form a neutralizing background. The equilibrium electron distribution function is Maxwellian:
\[
f_0(v) = \frac{n_0}{(2\pi v_{th}^2)^{3/2}} \exp\left(-\frac{v^2}{2 v_{th}^2}\right), \quad v_{th} = \sqrt{\frac{k_B T}{m}}.
\]

#### **Part 1: Vlasov-Maxwell Equations in Magnetized Plasma** [Core]
1. Write down the Vlasov equation for the electron distribution function \( f(\vec{r}, \vec{v}, t) \) and Maxwell's equations for the electromagnetic fields. Linearize these equations around the equilibrium for small perturbations, assuming wave-like dependence \( e^{i(\vec{k} \cdot \vec{r} - \omega t)} \).

2. Using the method of characteristics, express the perturbed distribution function \( f_1 \) as an integral along the unperturbed orbits. Discuss how the magnetic field \( \vec{B}_0 \) affects the orbits and the integral.

#### **Part 2: Dielectric Tensor and General Dispersion Relation** [Core]
3. Derive the expression for the induced current density \( \vec{J}_1 \) in terms of the electric field \( \vec{E}_1 \), and show that it leads to the dielectric tensor \( \epsilon_{ij} \). Write the general dispersion relation for electromagnetic waves in the form:
   \[
   \det \left( \frac{c^2 k^2}{\omega^2} \left( \frac{k_i k_j}{k^2} - \delta_{ij} \right) + \epsilon_{ij} \right) = 0.
   \]

4. For a Maxwellian distribution, the dielectric tensor components involve sums over cyclotron harmonics. Show that:
   \[
   \epsilon_{ij} = \delta_{ij} + \frac{\omega_p^2}{\omega^2} \sum_{n=-\infty}^{\infty} \int d^3v \, \frac{v_\perp \partial f_0 / \partial v_\perp + (n \omega_c / v_\perp) \partial f_0 / \partial v_\parallel}{\omega - k_\parallel v_\parallel - n \omega_c} \left[ \cdots \right]
   \]
   but more precisely, with finite Larmor radius (FLR) effects, the tensor components include terms like \( e^{-b_e} I_n(b_e) \) where \( b_e = k_\perp^2 \rho_e^2 \), \( \rho_e = v_{th}/\omega_c \) is the thermal Larmor radius, and \( I_n \) is the modified Bessel function. The plasma dispersion function \( Z(\zeta_n) \) appears with \( \zeta_n = (\omega - n \omega_c)/(k_\parallel v_{th}) \).

#### **Part 3: Wave Modes in Magnetized Plasma** [Core]
5. For waves propagating perpendicular to \( \vec{B}_0 \) (i.e., \( k_\parallel = 0 \)), derive the dispersion relation for the ordinary mode (O-mode) and show that it is identical to the unmagnetized case. Explain why the magnetic field has no effect on this mode.

6. For perpendicular propagation, derive the dispersion relation for the extraordinary mode (X-mode) in the cold plasma limit. Identify the upper hybrid resonance frequency \( \omega_h = \sqrt{\omega_p^2 + \omega_c^2} \) and discuss its significance.

   **EBW Add-on**: In the kinetic regime, for \( k_\parallel \rho_e \ll 1 \) and \( b_e \gtrsim 1 \), electron Bernstein waves (EBW) appear. These are electrostatic waves with frequencies near harmonics of \( \omega_c \). Briefly mention that the dispersion relation for EBW involves a determinant with strong FLR effects.

7. For waves propagating parallel to \( \vec{B}_0 \) (i.e., \( k_\perp = 0 \)), derive the dispersion relation for the right-hand circularly polarized mode (R-mode) in the cold plasma limit. Discuss the resonance at \( \omega = \omega_c \) and how it leads to wave absorption.

   **Cold-limit checkpoint**: Recover the Stix parameters \( S, D, P \) from the cold plasma dielectric tensor and write the Appleton-Hartree equation for perpendicular propagation.

#### **Part 4: Kinetic Effects and Damping** [Core]
8. In an unmagnetized plasma, transverse waves do not experience Landau damping. Explain why, using the resonance condition \( \omega = \vec{k} \cdot \vec{v} \) and the orientation of the electric field. How does the presence of a magnetic field allow for Landau damping of transverse waves for oblique propagation?

9. For the R-mode wave propagating parallel to \( \vec{B}_0 \), use the kinetic dispersion relation and the asymptotic form of the plasma dispersion function to derive the cyclotron damping rate. Recall that \( Z'(\zeta) = -2(1 + \zeta Z(\zeta)) \) and for \( \omega \lesssim \omega_c \), \( \Im Z(\zeta) \sim \sqrt{\pi} e^{-\zeta^2} \). Calculate the damping rate \( \gamma \) for parameters \( \omega_p = 10^{10} \) rad/s, \( \omega_c = 2 \times 10^{10} \) rad/s, \( v_{th} = 10^6 \) m/s, at frequency \( \omega = 0.99 \omega_c \). Assume \( k \) is given by the cold plasma dispersion relation.

#### **Part 5: Relativistic Effects** [Extension]
10. For high-temperature plasmas where \( k_B T \sim mc^2 \), the equilibrium distribution function becomes relativistic. Write down the relativistic Maxwellian (Jüttner distribution):
    \[
    f_0(\vec{p}) = \frac{n_0}{4\pi m^3 c^3 \theta K_2(1/\theta)} \exp\left( -\frac{\gamma}{\theta} \right), \quad \gamma = \sqrt{1 + \frac{p^2}{m^2 c^2}}, \quad \theta = \frac{k_B T}{m c^2}.
    \]
    Discuss how relativity affects the dispersion relation for transverse waves, focusing on changes in the plasma frequency and resonance conditions.

#### **Part 6: Nonlinear Phenomena** [Extension]
11. Consider a large-amplitude electromagnetic wave. Derive the equation of motion for an electron in the wave field and show that it can be written as a pendulum equation. Find the trapping width in velocity space.

12. Explain how nonlinear Landau damping leads to saturation of wave growth in the bump-on-tail instability. Describe the role of particle trapping and wave-particle interactions.

#### **Part 7: Numerical Evaluation** [Extension]
13. Using parameters \( \omega_p = 10^{10} \) rad/s, \( \omega_c = 2 \times 10^{10} \) rad/s, and \( v_{th} = 10^6 \) m/s, plot the dispersion relation \( \omega(k) \) for the O-mode, X-mode, and R-mode for both cold and hot plasma cases. Highlight the regions where damping occurs for the hot plasma.

    **Numerics guardrails**: Use the Faddeeva function \( w(z) \) to compute \( Z(\zeta) \) numerically. For summing over harmonics in the dielectric tensor, use a cutoff \( n_{\max} \approx b_e + 3\sqrt{b_e} \). Plot the real part \( \omega_r(k) \) and the damping rate \( \gamma(k) \) separately, and annotate cutoffs and resonances.

14. Compute the dielectric tensor component \( \epsilon_{xx} \) for a range of \( \omega \) and \( k_\parallel \) for the magnetized plasma and visualize the results using a contour plot. Discuss the features observed.

#### **Part 8: Conceptual Questions** [Core]
15. Compare and contrast Landau damping and collisional damping. Why is Landau damping considered reversible in principle but irreversible in practice?

16. What is quasi-linear theory? How does it describe the evolution of the distribution function due to wave-particle interactions? Write the quasi-linear diffusion equation.

17. How does the presence of a magnetic field break the symmetry and allow for new wave modes? Give examples from astrophysical plasmas, such as solar wind or pulsar magnetospheres.

---

### **Formula Cheat-Sheet**
- Plasma frequency: \( \omega_p = \sqrt{\frac{n_0 e^2}{\epsilon_0 m}} \)
- Cyclotron frequency: \( \omega_c = \frac{e B_0}{m} \)
- Thermal speed: \( v_{th} = \sqrt{\frac{k_B T}{m}} \)
- Larmor radius: \( \rho_e = \frac{v_{th}}{\omega_c} \)
- Plasma dispersion function: \( Z(\zeta) = \frac{1}{\sqrt{\pi}} \int_{-\infty}^{\infty} \frac{e^{-x^2}}{x - \zeta} dx \), with \( \Im(\zeta) > 0 \)
- Asymptotic expansion: \( Z(\zeta) \approx i \sqrt{\pi} e^{-\zeta^2} - \frac{1}{\zeta} \left(1 + \frac{1}{2\zeta^2} + \frac{3}{4\zeta^4} + \cdots \right) \) for \( |\zeta| \gg 1 \)
- Faddeeva function: \( w(z) = e^{-z^2} \text{erfc}(-iz) \), so \( Z(\zeta) = i \sqrt{\pi} w(\zeta) \)

### **Python Starter for Numerical Evaluation**
```python
import numpy as np
from scipy.special import wofz
import matplotlib.pyplot as plt

# Plasma dispersion function using Faddeeva function
def Z(z):
    return 1j * np.sqrt(np.pi) * wofz(z)

# Example: Plot Z for real z
z_real = np.linspace(-5, 5, 100)
z_complex = z_real + 1j * 1e-6  # small imaginary part for Landau prescription
Z_values = Z(z_complex)

plt.figure()
plt.plot(z_real, Z_values.real, label='Re Z')
plt.plot(z_real, Z_values.imag, label='Im Z')
plt.xlabel('ζ')
plt.ylabel('Z(ζ)')
plt.legend()
plt.title('Plasma Dispersion Function')
plt.show()

# For dispersion relation plotting, students need to solve for ω(k) numerically.
# This might involve root-finding for the dispersion relation.
```
