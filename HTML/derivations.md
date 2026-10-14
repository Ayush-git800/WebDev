# Applied Physics — Unit 1: COMPLETE DERIVATIONS ONLY
### Every derivation done fully — start to finish, no steps skipped

**How to read this document:** Each derivation begins from the most basic starting equation/postulate and ends in a clearly boxed final result. Follow every line — nothing is skipped.

---

## DERIVATION 1: de-Broglie Wavelength of a Photon

**Starting point — two known facts:**

Planck's quantum theory of radiation states that the energy of a photon is:
$$E = h\nu \quad ...(1)$$

Einstein's mass-energy relation states:
$$E = mc^2 \quad ...(2)$$

**Step 1:** Since both (1) and (2) equal E, equate them:
$$h\nu = mc^2$$

**Step 2:** The wave relation says speed = frequency × wavelength, so for light: c = νλ, which gives ν = c/λ. Substitute this in:
$$h\left(\frac{c}{\lambda}\right) = mc^2$$

**Step 3:** Simplify — cancel one factor of c from both sides:
$$\frac{h}{\lambda} = mc$$

**Step 4:** Rearrange to solve for λ:
$$\boxed{\lambda = \frac{h}{mc} = \frac{h}{p}}$$

(since momentum of photon p = mc). **This is the final result — de-Broglie wavelength of a photon.**

---

## DERIVATION 2: de-Broglie Wavelength — General Formula and All Its Forms

**de-Broglie's Hypothesis (starting postulate, 1924):** Every moving particle of mass m and velocity v has a wave associated with it, and by direct analogy with the photon result derived above (Derivation 1), the wavelength of this "matter wave" is:

$$\lambda = \frac{h}{p} = \frac{h}{mv} \quad \text{(base formula — the postulate itself)}$$

Now we derive every other version of this formula starting from this base formula.

### (a) In terms of Kinetic Energy (E)

**Step 1:** Start from the definition of kinetic energy:
$$E = \frac{1}{2}mv^2$$

**Step 2:** Multiply and divide the right side by m to introduce p = mv:
$$E = \frac{1}{2}mv^2 = \frac{m^2v^2}{2m} = \frac{(mv)^2}{2m} = \frac{p^2}{2m}$$

**Step 3:** Solve for p²:
$$p^2 = 2mE$$

**Step 4:** Take square root:
$$p = \sqrt{2mE}$$

**Step 5:** Substitute this into the base formula λ = h/p:
$$\boxed{\lambda = \frac{h}{\sqrt{2mE}}}$$

### (b) In terms of Temperature (T)

**Step 1:** From kinetic theory of gases, the average kinetic energy of a gas molecule at absolute temperature T is:
$$E = \frac{3}{2}kT$$
where k = Boltzmann's constant.

**Step 2:** From part (a) above, we already derived p = √(2mE). Substitute E = (3/2)kT into this:
$$p = \sqrt{2m \times \frac{3}{2}kT} = \sqrt{3mkT}$$

**Step 3:** Substitute into λ = h/p:
$$\boxed{\lambda = \frac{h}{\sqrt{3mkT}}}$$

### (c) For a charged particle (charge q) accelerated through potential difference V

**Step 1:** When a charge q is accelerated through a potential difference V, the work done on it by the electric field equals the kinetic energy it gains:
$$E = qV$$

**Step 2:** Substitute this value of E into p = √(2mE) (from part a):
$$p = \sqrt{2mqV}$$

**Step 3:** Substitute into λ = h/p:
$$\boxed{\lambda = \frac{h}{\sqrt{2mqV}}}$$

### (d) Specifically for an electron accelerated through V volts (numerical form)

**Step 1:** Start from the general charged-particle formula just derived:
$$\lambda = \frac{h}{\sqrt{2mqV}}$$

**Step 2:** Substitute the known constant values for an electron:
- h = 6.63 × 10⁻³⁴ J·s
- mₑ = 9.1 × 10⁻³¹ kg
- q = 1.6 × 10⁻¹⁹ C

$$\lambda = \frac{6.63\times10^{-34}}{\sqrt{2 \times 9.1\times10^{-31} \times 1.6\times10^{-19} \times V}}$$

**Step 3:** Calculate the constant term inside the square root (everything except V):
$$2 \times 9.1\times10^{-31} \times 1.6\times10^{-19} = 2.912\times10^{-49}$$

**Step 4:** So:
$$\lambda = \frac{6.63\times10^{-34}}{\sqrt{2.912\times10^{-49}\times V}} = \frac{6.63\times10^{-34}}{\sqrt{2.912\times10^{-49}}\times\sqrt{V}}$$

**Step 5:** Calculate √(2.912×10⁻⁴⁹) = 5.396×10⁻²⁵

**Step 6:** So:
$$\lambda = \frac{6.63\times10^{-34}}{5.396\times10^{-25}\times\sqrt{V}} = \frac{1.2287\times10^{-9}}{\sqrt{V}} \text{ metres}$$

**Step 7:** Convert 1.2287×10⁻⁹ m into angstroms (1 Å = 10⁻¹⁰ m), so 1.2287×10⁻⁹ m = 12.287 Å:

$$\boxed{\lambda = \frac{12.28}{\sqrt{V}} \text{ Å}}$$

---

## DERIVATION 3: Davisson-Germer Experiment — Verification Calculation

**Starting point — Bragg's Law for constructive interference in a crystal:**
$$2d\sin\theta = n\lambda \quad ...(1)$$
where d = interatomic spacing of the crystal, θ = glancing angle, n = order of diffraction.

**Given data from the experiment:**
- Nickel crystal interatomic spacing: d = 0.914 Å
- Order of diffraction: n = 1
- Strong peak observed at accelerating voltage V = 54 V, at scattering angle φ = 50°
- Geometric relation (from experimental setup, angles in a triangle): θ + θ + φ = 180°

**Step 1:** Solve the geometric relation for θ:
$$2\theta + \varphi = 180°$$
$$2\theta = 180° - 50° = 130°$$
$$\theta = 65°$$

**Step 2:** Substitute d = 0.914 Å, n = 1, θ = 65° into Bragg's Law (1):
$$2 \times 0.914 \times \sin(65°) = \lambda$$

**Step 3:** Calculate sin(65°) = 0.9063 (standard value), so:
$$\lambda = 2 \times 0.914 \times 0.9063$$

**Step 4:** Calculate:
$$\lambda = 1.657 \approx \boxed{1.66 \text{ Å (experimental value)}}$$

**Now compute the theoretical value using de-Broglie's formula (Derivation 2d) for comparison:**

**Step 5:** Using λ = 12.28/√V with V = 54:
$$\lambda = \frac{12.28}{\sqrt{54}}$$

**Step 6:** Calculate √54 = 7.348

**Step 7:** Calculate:
$$\lambda = \frac{12.28}{7.348} = \boxed{1.67 \text{ Å (theoretical value)}}$$

**Conclusion:** The experimental value (1.66 Å) and the theoretical de-Broglie value (1.67 Å) are in excellent agreement, which experimentally confirms de-Broglie's hypothesis of matter waves.

---

## DERIVATION 4: Phase Velocity (Vp)

**Starting point** — consider a plane wave with displacement y, written as:
$$y = a\sin(\omega t - kx) \quad ...(1)$$
where a = amplitude, ω = angular frequency, k = propagation constant (wave vector) = 2π/λ.

**Step 1:** A "plane of constant phase" means the argument inside the sine function stays constant as the wave moves:
$$\omega t - kx = \text{constant} \quad ...(2)$$

**Step 2:** Differentiate equation (2) with respect to time t (x is a function of t here, since we track a moving point of constant phase, while ω and k are fixed constants; differentiating a constant gives 0):
$$\omega - k\frac{dx}{dt} = 0$$

**Step 3:** Rearrange to isolate dx/dt:
$$k\frac{dx}{dt} = \omega$$
$$\frac{dx}{dt} = \frac{\omega}{k}$$

**Step 4:** By definition, dx/dt here is the velocity of the plane of constant phase — this IS the phase velocity Vp:

$$\boxed{V_p = \frac{\omega}{k}}$$

---

## DERIVATION 5: Phase Velocity of a de-Broglie Wave

**Starting point:** We use the result Vp = ω/k derived above (Derivation 4), and substitute expressions for ω and k specific to a de-Broglie (matter) wave.

**Step 1 — express ω:** We know ω = 2πν. Also, from Planck's relation E = hν, we get ν = E/h. So:
$$\omega = 2\pi\nu = \frac{2\pi E}{h}$$

**Step 2 — bring in the relativistic mass-energy relation:** Since E = mc² (m here is the relativistic mass of the particle, c is speed of light):
$$\omega = \frac{2\pi mc^2}{h} \quad ...(A)$$

**Step 3 — express k:** We know k = 2π/λ. Also, from de-Broglie's formula (Derivation 2), λ = h/(mv). Substituting:
$$k = \frac{2\pi}{h/mv} = \frac{2\pi mv}{h} \quad ...(B)$$

**Step 4 — divide (A) by (B) to get Vp = ω/k:**
$$V_p = \frac{\omega}{k} = \frac{\dfrac{2\pi mc^2}{h}}{\dfrac{2\pi mv}{h}}$$

**Step 5:** The 2π, m, and h all cancel from numerator and denominator:
$$V_p = \frac{c^2}{v}$$

$$\boxed{V_p = \frac{c^2}{v}}$$

**Physical consequence:** Since particle velocity v is always less than c, this means Vp > c always — the phase velocity of the matter wave exceeds the speed of light. This does NOT violate relativity because phase velocity carries no energy/information; the particle's actual, information-carrying velocity equals the **group velocity** Vg, not the phase velocity.

**Deriving the relation Vp × Vg = c²:**

**Step 1:** Since particle velocity v equals the group velocity: v = Vg

**Step 2:** Substitute this into the boxed result above:
$$V_p = \frac{c^2}{V_g}$$

**Step 3:** Cross-multiply:
$$\boxed{V_p \times V_g = c^2}$$

---

## DERIVATION 6: Group Velocity (Vg) — Expression from Superposition of Two Waves

**Starting point:** Consider two waves of the same amplitude a, but with slightly different angular frequencies (ω₁, ω₂) and propagation constants (k₁, k₂):
$$y_1 = a\sin(\omega_1 t - k_1 x) \quad ...(1)$$
$$y_2 = a\sin(\omega_2 t - k_2 x) \quad ...(2)$$

**Step 1 — apply the principle of superposition** (add the two waves):
$$y = y_1 + y_2 = a\sin(\omega_1 t - k_1x) + a\sin(\omega_2 t - k_2 x)$$
$$y = a\left[\sin(\omega_1 t - k_1 x) + \sin(\omega_2 t - k_2 x)\right] \quad ...(3)$$

**Step 2 — use the trigonometric identity:**
$$\sin C + \sin D = 2\sin\left(\frac{C+D}{2}\right)\cos\left(\frac{C-D}{2}\right)$$

Here C = ω₁t − k₁x and D = ω₂t − k₂x. So:
$$\frac{C+D}{2} = \frac{(\omega_1+\omega_2)t - (k_1+k_2)x}{2}, \qquad \frac{C-D}{2} = \frac{(\omega_1-\omega_2)t - (k_1-k_2)x}{2}$$

**Step 3 — substitute into equation (3):**
$$y = 2a\sin\left[\frac{(\omega_1+\omega_2)}{2}t - \frac{(k_1+k_2)}{2}x\right]\cos\left[\frac{(\omega_1-\omega_2)}{2}t - \frac{(k_1-k_2)}{2}x\right]$$

**Step 4 — define new symbols to simplify** (standard notation, since ω₁ ≈ ω₂ and k₁ ≈ k₂ for a wave packet):
$$\omega = \frac{\omega_1+\omega_2}{2}, \quad k = \frac{k_1+k_2}{2}, \quad \frac{d\omega}{2} = \frac{\omega_1-\omega_2}{2}, \quad \frac{dk}{2} = \frac{k_1-k_2}{2}$$

**Step 5 — rewrite y using these symbols:**
$$y = 2a\sin(\omega t - kx)\cos\left(\frac{d\omega}{2}t - \frac{dk}{2}x\right)$$

Rearranging (cosine term written first, as the "envelope"):
$$y = \underbrace{2a\cos\left(\frac{d\omega}{2}t - \frac{dk}{2}x\right)}_{\text{Amplitude } A \text{ (slowly varying envelope)}} \times \sin(\omega t - kx)$$

**Step 6 — interpret this result:** This is a wave sin(ωt − kx) — same form as a single wave — but its amplitude A is NOT constant; it varies slowly according to:
$$A = 2a\cos\left(\frac{d\omega}{2}t - \frac{dk}{2}x\right)$$

This slowly-varying amplitude envelope is exactly the **wave packet**. The velocity at which THIS envelope moves is the group velocity. Using the same logic as Derivation 4 (velocity of a point of constant phase/argument):

The argument of the envelope, (dω/2)t − (dk/2)x, is constant for a point moving with the envelope. Differentiating with respect to t:
$$\frac{d\omega}{2} - \frac{dk}{2}\cdot\frac{dx}{dt} = 0$$
$$\frac{dx}{dt} = \frac{d\omega/2}{dk/2} = \frac{d\omega}{dk}$$

**Step 7 — this dx/dt is by definition the group velocity Vg:**

$$\boxed{V_g = \frac{d\omega}{dk}}$$

---

## DERIVATION 7: Relation Between Phase Velocity and Group Velocity

### (A) For a dispersive medium (Vp depends on wavelength λ)

**Starting point:** We use two known results:
$$V_g = \frac{d\omega}{dk} \quad ...(1) \qquad \text{(derived in Derivation 6)}$$
$$V_p = \frac{\omega}{k} \quad ...(2) \qquad \text{(derived in Derivation 4)}$$

**Step 1:** From (2), rearrange to express ω in terms of k and Vp:
$$\omega = kV_p$$

**Step 2:** Differentiate both sides with respect to k. Since Vp itself depends on k (dispersive medium), use the product rule:
$$\frac{d\omega}{dk} = k\frac{dV_p}{dk} + V_p \cdot \frac{dk}{dk} = k\frac{dV_p}{dk} + V_p$$

**Step 3:** Substitute this expression for dω/dk into equation (1):
$$V_g = V_p + k\frac{dV_p}{dk} \quad ...(3)$$

**Step 4:** We now convert dVp/dk into dVp/dλ, since dispersion is usually expressed as a function of wavelength. We know:
$$k = \frac{2\pi}{\lambda}$$

**Step 5:** Differentiate k with respect to λ:
$$\frac{dk}{d\lambda} = -\frac{2\pi}{\lambda^2}$$

**Step 6:** Rearrange to express dk itself:
$$dk = -\frac{2\pi}{\lambda^2}d\lambda$$

**Step 7:** Now use the chain rule to rewrite the term k(dVp/dk):
$$k\frac{dV_p}{dk} = k \cdot \frac{dV_p}{d\lambda}\cdot\frac{d\lambda}{dk}$$

We need dλ/dk, the reciprocal of dk/dλ found in Step 5:
$$\frac{d\lambda}{dk} = \frac{1}{dk/d\lambda} = \frac{1}{-2\pi/\lambda^2} = -\frac{\lambda^2}{2\pi}$$

**Step 8:** Substitute k = 2π/λ and dλ/dk = −λ²/2π into the term:
$$k\frac{dV_p}{dk} = \frac{2\pi}{\lambda}\times\frac{dV_p}{d\lambda}\times\left(-\frac{\lambda^2}{2\pi}\right)$$

**Step 9:** Simplify — the 2π cancels, and one power of λ cancels (λ²/λ = λ):
$$k\frac{dV_p}{dk} = -\lambda\frac{dV_p}{d\lambda}$$

**Step 10:** Substitute this back into equation (3):
$$\boxed{V_g = V_p - \lambda\frac{dV_p}{d\lambda}}$$

**This is the required relation for a dispersive medium.**

### (B) For a non-dispersive medium

**Starting point:** In a non-dispersive medium, phase velocity Vp does NOT change with wavelength, meaning:
$$\frac{dV_p}{d\lambda} = 0$$

**Step 1:** Substitute this into the boxed result from part (A):
$$V_g = V_p - \lambda \times 0$$

**Step 2:** Simplify:
$$\boxed{V_g = V_p}$$

**In a non-dispersive medium, group velocity equals phase velocity exactly.**

---

## DERIVATION 8: Heisenberg's Uncertainty Principle

**Starting point:** We use two known facts.

**Fact 1 — de-Broglie relation, converted to wave-number form:**
$$\lambda = \frac{h}{p}$$
Since wave number k = 2π/λ, substitute λ = h/p:
$$k = \frac{2\pi}{h/p} = \frac{2\pi p}{h}$$

**Step 1:** Since k is directly proportional to p (with constant 2π/h), an uncertainty (small change) in momentum, Δp, produces a corresponding uncertainty in wave number, Δk, by the same proportionality:
$$\Delta k = \frac{2\pi}{h}\Delta p \quad ...(1)$$

**Fact 2 — a standard mathematical property of any localized wave packet** (from Fourier analysis: a wave packet localized within a spatial spread Δx must necessarily be composed of a spread of wave numbers Δk, and the minimum possible product of these two spreads is a fixed number):
$$\Delta x \cdot \Delta k \geq \frac{1}{2} \quad ...(2)$$

**Step 2:** Substitute equation (1) into equation (2), replacing Δk:
$$\Delta x \cdot \frac{2\pi}{h}\Delta p \geq \frac{1}{2}$$

**Step 3:** Multiply both sides of the inequality by h/(2π) to isolate Δx·Δp:
$$\Delta x \cdot \Delta p \geq \frac{1}{2}\times\frac{h}{2\pi}$$

**Step 4:** Simplify the right-hand side:
$$\boxed{\Delta x \cdot \Delta p \geq \frac{h}{4\pi}}$$

**This is Heisenberg's Uncertainty Principle — fully derived.**

**Other forms, each derived directly from the boxed result above:**

**(a) Position–Velocity form:** Since p = mv, an uncertainty in momentum Δp relates to an uncertainty in velocity Δv by Δp = mΔv (for constant mass m). Substitute this into the boxed result:
$$\Delta x \cdot (m\Delta v) \geq \frac{h}{4\pi}$$
$$\boxed{\Delta x \cdot \Delta v \geq \frac{h}{4\pi m}}$$

**(b) Energy–Time form** (stated by exact analogy, since energy and time are related through frequency the same way momentum and position are related through wave number):
$$\boxed{\Delta E \cdot \Delta t \geq \frac{h}{4\pi}}$$

**(c) Angular Position–Angular Momentum form** (by the same analogy):
$$\boxed{\Delta \theta \cdot \Delta L \geq \frac{h}{4\pi}}$$

---

## DERIVATION 9: Time-Dependent Schrödinger Wave Equation

**Starting point:** The general differential equation of wave motion of a particle in one dimension (classical wave equation) is:
$$\frac{\partial^2\Psi}{\partial x^2} = \frac{1}{v^2}\frac{\partial^2\Psi}{\partial t^2} \quad ...(1)$$

The general solution of this standard wave equation is well known to be:
$$\Psi(x,t) = Ae^{-i\omega\left(t-\frac{x}{v}\right)} \quad ...(2)$$

**Step 1:** Substitute ω = 2πν and v = νλ into equation (2):
$$\Psi(x,t) = Ae^{-i2\pi\nu\left(t-\frac{x}{\nu\lambda}\right)} = Ae^{-2\pi i\left(\nu t - \frac{x}{\lambda}\right)}$$

**Step 2:** Now bring in physics: use Planck's relation E = hν, so ν = E/h; and de-Broglie's relation λ = h/p. Substitute both into the exponent:
$$\Psi(x,t) = Ae^{-2\pi i\left(\frac{E}{h}t - \frac{px}{h}\right)} = Ae^{-\frac{2\pi i}{h}(Et - px)}$$

**Step 3:** Define ħ = h/2π (so that 2π/h = 1/ħ). Substitute:
$$\boxed{\Psi(x,t) = Ae^{-\frac{i}{\hbar}(Et-px)}} \quad ...(2')$$

This is the wave function we will now use for all further differentiation.

**Step 4 — differentiate Ψ once with respect to x:**
$$\frac{\partial\Psi}{\partial x} = Ae^{-\frac{i}{\hbar}(Et-px)}\times\left(\frac{i}{\hbar}p\right) = \frac{ip}{\hbar}\Psi$$

**Step 5 — differentiate again with respect to x** (differentiate the Step 4 result):
$$\frac{\partial^2\Psi}{\partial x^2} = Ae^{-\frac{i}{\hbar}(Et-px)}\times\left(\frac{ip}{\hbar}\right)^2 = -\frac{p^2}{\hbar^2}Ae^{-\frac{i}{\hbar}(Et-px)}$$

**Step 6:** Recognize that the exponential term is just Ψ again (from equation 2'):
$$\frac{\partial^2\Psi}{\partial x^2} = -\frac{p^2}{\hbar^2}\Psi$$

**Step 7:** Rearrange to solve for p²:
$$\boxed{p^2 = -\hbar^2\frac{1}{\Psi}\frac{\partial^2\Psi}{\partial x^2}} \quad ...(3)$$

**Step 8 — now differentiate the original Ψ (equation 2') once with respect to t:**
$$\frac{\partial\Psi}{\partial t} = Ae^{-\frac{i}{\hbar}(Et-px)}\times\left(-\frac{i}{\hbar}E\right) = -\frac{iE}{\hbar}\Psi$$

**Step 9:** Rearrange to solve for E. Starting from:
$$\frac{\partial\Psi}{\partial t} = -\frac{iE}{\hbar}\Psi$$
Divide both sides by Ψ:
$$\frac{1}{\Psi}\frac{\partial\Psi}{\partial t} = -\frac{iE}{\hbar}$$
Multiply both sides by ħ:
$$\hbar\cdot\frac{1}{\Psi}\frac{\partial\Psi}{\partial t} = -iE$$
Divide both sides by (−i), noting that 1/(−i) = i:
$$E = i\hbar\cdot\frac{1}{\Psi}\frac{\partial\Psi}{\partial t}$$
$$\boxed{E = \frac{i\hbar}{\Psi}\frac{\partial\Psi}{\partial t}} \quad ...(4)$$

**Step 10 — apply the Principle of Conservation of Energy** (total energy = kinetic energy + potential energy):
$$E = KE + PE = \frac{p^2}{2m} + V \quad ...(5)$$

**Step 11 — substitute the expressions for p² (equation 3) and E (equation 4) into equation (5):**
$$\frac{i\hbar}{\Psi}\frac{\partial\Psi}{\partial t} = \frac{1}{2m}\left(-\hbar^2\frac{1}{\Psi}\frac{\partial^2\Psi}{\partial x^2}\right) + V$$

$$\frac{i\hbar}{\Psi}\frac{\partial\Psi}{\partial t} = -\frac{\hbar^2}{2m\Psi}\frac{\partial^2\Psi}{\partial x^2} + V$$

**Step 12 — multiply every term on both sides by Ψ to clear denominators:**
$$i\hbar\frac{\partial\Psi}{\partial t} = -\frac{\hbar^2}{2m}\frac{\partial^2\Psi}{\partial x^2} + V\Psi$$

**Step 13 — rearrange into standard form** (potential and kinetic terms on the left, time-derivative on the right):

$$\boxed{-\frac{\hbar^2}{2m}\frac{\partial^2\Psi}{\partial x^2} + V\Psi = i\hbar\frac{\partial\Psi}{\partial t}}$$

**This is the Time-Dependent Schrödinger Wave Equation in one dimension — fully derived.**

**Step 14 — extend to three dimensions:** Replace the single second derivative ∂²Ψ/∂x² with the sum of second derivatives in all three directions (this sum is called the Laplacian, ∇²):
$$\frac{\partial^2\Psi}{\partial x^2} \rightarrow \frac{\partial^2\Psi}{\partial x^2}+\frac{\partial^2\Psi}{\partial y^2}+\frac{\partial^2\Psi}{\partial z^2} = \nabla^2\Psi$$

So the 3-D equation becomes:

$$\boxed{-\frac{\hbar^2}{2m}\nabla^2\Psi + V\Psi = i\hbar\frac{\partial\Psi}{\partial t}}$$

**Operator interpretation:** This equation can be written as ĤΨ = ÊΨ, where:
- Ĥ = −ħ²/2m ∇² + V is called the **Hamiltonian operator**
- Ê = iħ ∂/∂t is called the **Energy operator**

---

## DERIVATION 10: Time-Independent Schrödinger Wave Equation

**Starting point:** Exactly as in Derivation 9, begin from the same wave function:
$$\Psi(x,t) = Ae^{-\frac{i}{\hbar}(Et-px)} \quad ...(2)$$

**Step 1 — differentiate once with respect to x:**
$$\frac{\partial\Psi}{\partial x} = Ae^{-\frac{i}{\hbar}(Et-px)}\times\frac{i}{\hbar}p = \frac{ip}{\hbar}\Psi$$

**Step 2 — differentiate again with respect to x:**
$$\frac{\partial^2\Psi}{\partial x^2} = Ae^{-\frac{i}{\hbar}(Et-px)}\times\left(\frac{ip}{\hbar}\right)^2 = -\frac{p^2}{\hbar^2}\Psi \quad \text{(from equation 2)}$$

**Step 3 — rearrange to isolate p²:**
$$\boxed{p^2 = -\hbar^2\frac{1}{\Psi}\frac{\partial^2\Psi}{\partial x^2}} \quad ...(3)$$

(Identical to Step 7 of Derivation 9 — same math.)

**Step 4 — apply the Principle of Conservation of Energy:**
$$E = KE + PE = \frac{p^2}{2m} + V$$

**Step 5 — rearrange to isolate p²:**
$$p^2 = 2m(E-V) \quad ...(6)$$

**Step 6 — since equations (3) and (6) are both expressions for p², set them equal to each other:**
$$2m(E-V) = -\hbar^2\frac{1}{\Psi}\frac{\partial^2\Psi}{\partial x^2}$$

**Step 7 — multiply both sides by Ψ:**
$$2m(E-V)\Psi = -\hbar^2\frac{\partial^2\Psi}{\partial x^2}$$

**Step 8 — divide both sides by −ħ²:**
$$-\frac{2m(E-V)}{\hbar^2}\Psi = \frac{\partial^2\Psi}{\partial x^2}$$

**Step 9 — rearrange so all terms are on one side, equal to zero:**
$$\frac{\partial^2\Psi}{\partial x^2} + \frac{2m}{\hbar^2}(E-V)\Psi = 0$$

$$\boxed{\frac{\partial^2\Psi}{\partial x^2} + \frac{2m}{\hbar^2}(E-V)\Psi = 0}$$

**This is the Time-Independent Schrödinger Wave Equation in one dimension — fully derived.**

**Step 10 — extend to three dimensions** (replace second derivative with the Laplacian, exactly as before):

$$\boxed{\nabla^2\Psi + \frac{2m}{\hbar^2}(E-V)\Psi = 0}$$

**Step 11 — special case: for a FREE PARTICLE, potential energy V = 0.** Substitute V = 0 into the boxed 3-D result:

$$\boxed{\nabla^2\Psi + \frac{2m}{\hbar^2}E\Psi = 0}$$

**This free-particle form is used next, in Derivation 11 (Particle in a Box).**

---

## DERIVATION 11: Particle in a One-Dimensional Box (Complete Derivation)

**Setup:** A particle of mass m moves freely along the x-axis, confined between two rigid walls at x = 0 and x = L. The potential energy is:
$$V(x) = \begin{cases} 0 & 0 < x < L \\ \infty & x \leq 0 \text{ or } x \geq L \end{cases}$$

Since V = ∞ outside the box, the particle can never be found there, so Ψ = 0 for x ≤ 0 and x ≥ L. We now solve for Ψ **inside** the box, where V = 0.

### Part A: Finding the wave function form and applying the boundary conditions

**Step 1:** Inside the box (V = 0), use the free-particle time-independent Schrödinger equation derived in Derivation 10 (final boxed result there):
$$\frac{d^2\Psi}{dx^2} + \frac{2mE}{\hbar^2}\Psi = 0$$

**Step 2:** Define a new constant k² to simplify notation:
$$k^2 = \frac{2mE}{\hbar^2} \quad ...(1)$$

**Step 3:** Substituting, the equation becomes:
$$\frac{d^2\Psi}{dx^2} + k^2\Psi = 0 \quad ...(2)$$

**Step 4:** This is a standard second-order linear differential equation. Its general solution (a well-known standard result for this type of equation) is:
$$\Psi = A\sin(kx) + B\cos(kx) \quad ...(3)$$

where A and B are constants to be determined using the boundary conditions of the box.

**Step 5 — apply the FIRST boundary condition:** At x = 0, the wave function must be zero (Ψ = 0, since the wall is impenetrable):
$$0 = A\sin(k\times 0) + B\cos(k\times 0)$$
$$0 = A(0) + B(1)$$
$$0 = B$$
$$\boxed{B = 0}$$

**Step 6:** Substitute B = 0 back into equation (3):
$$\Psi = A\sin(kx) \quad ...(4)$$

**Step 7 — apply the SECOND boundary condition:** At x = L, the wave function must also be zero:
$$0 = A\sin(kL)$$

**Step 8:** For this equation to hold, either A = 0 or sin(kL) = 0. If A = 0, then from equation (4), Ψ = 0 everywhere inside the box too — meaning there is no particle at all, which is not physically meaningful. So we must have:
$$A \neq 0 \implies \sin(kL) = 0$$

**Step 9:** The sine function equals zero whenever its argument is an integer multiple of π:
$$kL = n\pi \quad \text{where } n = 1, 2, 3, ...$$

(n = 0 is excluded because it would again make Ψ = 0 everywhere, meaning no particle — not physical.)

**Step 10:** Solve for k:
$$\boxed{k = \frac{n\pi}{L}} \quad ...(5)$$

### Part B: Deriving the Energy Eigenvalues

**Step 1:** Take the expression for k found in equation (5) and substitute it into equation (1) (recall equation 1 was k² = 2mE/ħ²):
$$\left(\frac{n\pi}{L}\right)^2 = \frac{2mE}{\hbar^2}$$

**Step 2:** Expand the left side:
$$\frac{n^2\pi^2}{L^2} = \frac{2mE}{\hbar^2}$$

**Step 3:** Solve for E:
$$E = \frac{n^2\pi^2\hbar^2}{2mL^2}$$

**Step 4:** Now substitute ħ = h/2π (so ħ² = h²/4π²) to express the answer in terms of h instead of ħ:
$$E = \frac{n^2\pi^2}{2mL^2}\times\frac{h^2}{4\pi^2}$$

**Step 5:** Simplify — the π² in the numerator cancels with one π² in the denominator:
$$E = \frac{n^2 h^2}{2mL^2 \times 4} = \frac{n^2h^2}{8mL^2}$$

**Step 6:** Since this energy depends on the integer n, we write it as Eₙ (the energy eigenvalue for quantum number n):

$$\boxed{E_n = \frac{n^2h^2}{8mL^2}}, \quad n = 1, 2, 3, ...$$

**This shows energy is quantized** — only specific discrete values are allowed (E₁, E₂, E₃, ... corresponding to n=1,2,3...), unlike classical mechanics where energy can be any value.

Since Eₙ ∝ n², we get: E₂ = 4E₁, E₃ = 9E₁, E₄ = 16E₁, E₅ = 25E₁, and so on. Checking the spacing between consecutive levels: E₂−E₁ = 3E₁, E₃−E₂ = 5E₁, E₄−E₃ = 7E₁ — the spacing keeps increasing, so **energy levels are NOT equally spaced.**

### Part C: Deriving the Normalized Eigenfunctions

**Step 1:** Substitute k = nπ/L (equation 5) into equation (4):
$$\Psi = A\sin\left(\frac{n\pi x}{L}\right) \quad ...(6)$$

We now find the constant A using the **normalization condition**, which states that the total probability of finding the particle anywhere inside the box must equal 1:
$$\int_0^L |\Psi|^2\,dx = 1$$

**Step 2:** Substitute Ψ from equation (6):
$$\int_0^L A^2\sin^2\left(\frac{n\pi x}{L}\right)dx = 1$$

**Step 3:** Use the trigonometric identity sin²θ = (1 − cos2θ)/2, with θ = nπx/L:
$$A^2\int_0^L \frac{1-\cos\left(\dfrac{2n\pi x}{L}\right)}{2}\,dx = 1$$

**Step 4:** Take the constant 1/2 outside the integral:
$$\frac{A^2}{2}\int_0^L \left[1 - \cos\left(\frac{2n\pi x}{L}\right)\right]dx = 1$$

**Step 5:** Integrate term by term. The integral of 1 with respect to x is x. The integral of cos(2nπx/L) with respect to x is (L/2nπ)sin(2nπx/L):
$$\frac{A^2}{2}\left[x - \frac{L}{2n\pi}\sin\left(\frac{2n\pi x}{L}\right)\right]_0^L = 1$$

**Step 6:** Evaluate this at the upper limit x = L:
$$x = L, \qquad \sin\left(\frac{2n\pi \times L}{L}\right) = \sin(2n\pi)$$
Since n is an integer, 2nπ is always a whole multiple of 2π, and sine of any whole multiple of 2π is exactly 0:
$$\sin(2n\pi) = 0$$
So the value at the upper limit is: L − 0 = L

**Step 7:** Evaluate at the lower limit x = 0:
$$x = 0, \qquad \sin(0) = 0$$
So the value at the lower limit is: 0 − 0 = 0

**Step 8:** Subtract (upper limit value) − (lower limit value):
$$\frac{A^2}{2}[L - 0] = 1$$
$$\frac{A^2L}{2} = 1$$

**Step 9:** Solve for A²:
$$A^2 = \frac{2}{L}$$

**Step 10:** Take the square root:
$$\boxed{A = \sqrt{\frac{2}{L}}}$$

**Step 11:** Substitute this value of A back into equation (6) to get the final normalized wave function:

$$\boxed{\Psi_n = \sqrt{\frac{2}{L}}\sin\left(\frac{n\pi x}{L}\right)}$$

**This is the complete, fully normalized eigenfunction — the derivation is now finished.** This Ψₙ is called the normalized eigenfunction (or normalized wave function) corresponding to the energy eigenvalue Eₙ derived in Part B.

---

## SUMMARY — ALL FINAL BOXED RESULTS IN ONE PLACE

| # | Derivation | Final Result |
|---|---|---|
| 1 | de-Broglie wavelength of photon | λ = h/mc = h/p |
| 2a | ...in terms of Kinetic Energy | λ = h/√(2mE) |
| 2b | ...in terms of Temperature | λ = h/√(3mkT) |
| 2c | ...for charge q, potential V | λ = h/√(2mqV) |
| 2d | ...for electron, potential V | λ = 12.28/√V Å |
| 3 | Davisson-Germer (Bragg's law check) | λ(exp) = 1.66 Å ≈ λ(theory) = 1.67 Å |
| 4 | Phase velocity | Vp = ω/k |
| 5 | Phase velocity of matter wave | Vp = c²/v, and Vp·Vg = c² |
| 6 | Group velocity | Vg = dω/dk |
| 7a | Vp-Vg relation (dispersive) | Vg = Vp − λ(dVp/dλ) |
| 7b | Vp-Vg relation (non-dispersive) | Vg = Vp |
| 8 | Heisenberg Uncertainty Principle | Δx·Δp ≥ h/4π |
| 9 | Time-Dependent Schrödinger Equation | −ħ²/2m ∇²Ψ + VΨ = iħ ∂Ψ/∂t |
| 10 | Time-Independent Schrödinger Equation | ∇²Ψ + (2m/ħ²)(E−V)Ψ = 0 |
| 11B | Particle in box — Energy | Eₙ = n²h²/8mL² |
| 11C | Particle in box — Wave function | Ψₙ = √(2/L) sin(nπx/L) |

---

**Exam tip:** For "derive" questions worth 5-7 marks, examiners want to see the starting equation, the key substitution steps, and the final boxed result clearly separated — exactly as laid out above. Write each numbered step; don't jump straight from the starting point to the answer.
