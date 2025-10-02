Of course. Here is an advanced electromagnetism problem that sits at the intersection of theory and applied physics, perfect for a strong undergraduate or master's level. It involves the classic topic of scattering but with a twist that requires a solid grasp of boundary conditions and special functions.

---

### **Problem: Electromagnetic Scattering from a Conducting Cylinder – The High-Frequency Limit**

Consider an infinitely long, perfectly conducting cylinder of radius \(a\) whose axis lies along the \(z\)-direction. A plane wave is incident perpendicularly to the cylinder's axis. The incident electric field is polarized parallel to the cylinder axis and is given by:
\[
\mathbf{E}_{\text{inc}} = \hat{\mathbf{z}} E_0 e^{i k x}
\]
where \(k = \omega / c\) is the wavenumber. We are interested in the **high-frequency** or **short-wavelength** limit where \(ka = 2\pi a / \lambda \gg 1\).

1.  **General Formalism:**
    *   Write down the full wave equation for the \(z\)-component of the total electric field, \(E_z\), outside the cylinder. Explain why for this polarization (TM⁠⁠⁠⁠z mode), the boundary condition on the cylinder surface (\( \rho = a \)) is \(E_z(\rho=a) = 0\).
    *   The general solution is a expansion in cylindrical harmonics (Bessel functions). Write down this expansion for the *scattered* field \(E_z^{\text{sc}}\).

2.  **The Physical Optics Approximation:**
    In the high-frequency limit (\(ka \gg 1\)), we can approximate the scattering using a method akin to **physical optics**.
    *   Argue that on the **illuminated** side of the cylinder (\(-\pi/2 < \phi < \pi/2\)), the surface current is approximately \(\mathbf{K} \approx 2 \hat{\mathbf{n}} \times \mathbf{H}_{\text{inc}}\), where \(\hat{\mathbf{n}}\) is the outward normal. What is the surface current on the **shadow** side? Why?
    *   Using this approximation for the surface current \(\mathbf{K}(\phi')\), write the expression for the vector potential \(\mathbf{A}(\mathbf{r})\) in the radiation zone (\(kr \gg 1\)). Find the resulting scattered far-field \(\mathbf{E}_{\text{sc}}^{\text{far}}(\mathbf{r})\).

3.  **The Scattering Cross Section:**
    *   From your result in part (2), derive the **differential scattering cross section** \( \frac{d\sigma}{d\phi} \) for this cylinder.
    *   Integrate this to find the **total scattering cross section per unit length**, \(\sigma_{\text{total}}\).
    *   *Interpret your result for \(\sigma_{\text{total}}\).* Why is it larger than the simple geometric width of the cylinder (\(2a\))? What does the extra factor represent physically?

4.  **Comparison to a Simpler Case:**
    *   Contrast your physical optics result with the exact result for the scattering cross section of a **perfectly conducting flat strip** of width \(2a\). What are the key similarities and differences, and why do they arise?

---

### **Solution Outline & Key Insights**

**1. General Formalism:**
*   The wave equation is the Helmholtz equation: \(( \nabla^2 + k^2 ) E_z = 0\).
*   The boundary condition arises because the tangential component of the total E-field must vanish on a perfect conductor: \(\hat{\boldsymbol{\rho}} \times \mathbf{E}|_{\rho=a} = 0\). For our TM⁠⁠⁠⁠z case, the only tangential component is \(E_z\), so \(E_z(\rho=a)=0\).
*   The scattered field expansion is:
    \[
    E_z^{\text{sc}} = \sum_{n=-\infty}^{\infty} c_n H_n^{(1)}(k\rho) e^{i n \phi}
    \]
    where \(H_n^{(1)}\) is the Hankel function of the first kind (representing outgoing waves). The coefficients \(c_n\) are determined by enforcing the boundary condition.

**2. Physical Optics Approximation:**
*   On the **illuminated side**, the field induces a current. The physical optics approximation assumes \(\mathbf{K} \approx 2 (\hat{\mathbf{n}} \times \mathbf{H}_{\text{inc}})\) for the lit region. On the **shadow** side, the incident field is assumed to be zero, so \(\mathbf{K} \approx 0\). This is the key simplification that avoids the infinite sum of Bessel functions.
*   The vector potential is \(\mathbf{A}(\mathbf{r}) = \frac{\mu_0}{4\pi} \int \frac{\mathbf{K}(\mathbf{r}') e^{i k |\mathbf{r} - \mathbf{r}'|}}{|\mathbf{r} - \mathbf{r}'|} da'\). In the far field, this simplifies significantly. The scattered field is found from \(\mathbf{E}_{\text{sc}} = i \omega (\hat{\mathbf{r}} \times \mathbf{A}) \times \hat{\mathbf{r}}\).
*   The final expression for the far-field will involve an integral over the lit part of the cylinder surface, which can be evaluated using the stationary phase method.

**3. Scattering Cross Section:**
*   The differential cross section will be:
    \[
    \frac{d\sigma}{d\phi} \propto \left| \int_{-\pi/2}^{\pi/2} \text{phase factors} \, d\phi' \right|^2
    \]
*   The total scattering cross section per unit length found from this method is:
    \[
    \sigma_{\text{total}} = 2a \left[ 1 + \frac{1}{(ka)^{4/3}} + \mathcal{O}((ka)^{-2}) \right]
    \]
    *The primary result:* \(\sigma_{\text{total}} \approx 2a\). The geometric width is \(2a\), so this makes sense. However, the exact result from the full wave theory is actually slightly *larger* than \(2a\). The physical optics approximation gives the leading term correctly but misses the smaller, positive contribution from the "creeping waves" or "diffractive corrections" that travel around the shadow side of the cylinder. Your calculated result being exactly \(2a\) is an artifact of the approximation that \(\mathbf{K}=0\) in the shadow region, which ignores these effects. The extra factor in the exact result represents the contribution from these diffracted waves.

**4. Comparison to a Flat Strip:**
*   For a flat strip of width \(2a\), the physical optics approximation gives a total cross section of exactly \(\sigma_{\text{total}}^{\text{strip}} = 2a\). The exact solution for the strip, however, is also approximately \(2a\) in the high-frequency limit. The key difference is that the cylinder has a curvature which supports the previously mentioned "creeping waves," leading to a slightly different diffractive correction term than the strip. The strip's discontinuity at its edges produces a different diffractive pattern.

This problem forces you to move beyond just solving a boundary value problem and to think about approximations, their limits of validity, and the physical origins of the results. It connects the elegant formalism of exact solutions to the practical need for approximate answers in complex real-world scenarios.