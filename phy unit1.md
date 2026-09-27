# Applied Physics — Unit 1: Fundamentals of Quantum Mechanics
### Complete Notes from Zero Background (AKTU B.Tech First Year)

---

## PART 0: Basic Physics Refresher (things you forgot from school)

You need only these few facts to understand everything below. Memorize this box.

| Quantity | Symbol | Formula | Meaning |
|---|---|---|---|
| Momentum | p | p = mv | mass × velocity |
| Kinetic Energy | E or KE | E = ½mv² = p²/2m | energy of motion |
| Wave relation | — | v = νλ | speed = frequency × wavelength |
| Angular frequency | ω | ω = 2πν | |
| Wave number | k | k = 2π/λ | |
| Planck's constant | h | 6.63 × 10⁻³⁴ J·s | fixed constant |
| Reduced Planck's constant | ħ (h-bar) | ħ = h/2π | |
| Photon energy (Planck) | E | E = hν | energy of light packet |
| Mass-energy (Einstein) | E | E = mc² | |
| 1 electron-volt | 1 eV | 1.6 × 10⁻¹⁹ J | energy unit |
| Mass of electron | mₑ | 9.1 × 10⁻³¹ kg | |
| Mass of proton/neutron | mₚ, mₙ | 1.67 × 10⁻²⁷ kg | |
| 1 Å (angstrom) | — | 10⁻¹⁰ m | |
| 1 nm | — | 10⁻⁹ m | |

That's it. Every formula below is built from just these.

**Why does this whole unit exist?**
Classical (Newtonian) physics works great for big things (cars, planets) but completely fails for tiny things (electrons, photons, atoms). This failure is called the **inadequacy of classical mechanics**, and it's why physicists built a new theory: **Quantum Mechanics**.

---

## TOPIC 1: Inadequacy (Limitations) of Classical Mechanics

Classical mechanics **could not explain**:
1. Spectrum of Black Body Radiation
2. Compton Effect
3. Photoelectric Effect
4. Raman Effect
5. Stability of atoms (why electrons don't spiral into the nucleus)
6. Variation of specific heat of metals/gases with temperature

**Note (write this in exam):** *The inadequacy of classical mechanics led to the development of Quantum Mechanics.*

### Classical Mechanics vs Quantum Mechanics (table — very likely to be asked)

| Classical Mechanics | Quantum Mechanics |
|---|---|
| Deals with macroscopic objects (planets, cars, balls) | Deals with microscopic objects (electron, photon, atom) |
| Based on Newton's laws of motion | Based on Schrödinger's wave equation & principles of quantum theory |
| Position AND momentum of a particle can be known exactly at the same time | Exact position and momentum can NEVER be known simultaneously (Heisenberg's Uncertainty Principle) |
| Light has only wave nature | Light has dual nature: wave AND particle |
| Cannot explain photoelectric effect, Compton effect, Raman effect | Successfully explains all of these |

---

## TOPIC 2: De-Broglie Concept of Matter Waves

**De-Broglie Hypothesis (1924):** *"Every moving particle has a wave associated with it."*
This wave is called a **matter wave** or **de-Broglie wave**.

### Main formula (learn this first — everything else is a variation of it)

$$\lambda = \frac{h}{p} = \frac{h}{mv}$$

where λ = de-Broglie wavelength, h = Planck's constant, p = momentum, m = mass, v = velocity.

### Derivation for a photon
Using Planck: E = hν ...(1)
Using Einstein: E = mc² ...(2)
Equating (1) and (2): hν = mc² → h(c/λ) = mc² (since ν = c/λ)

$$\lambda = \frac{h}{mc}$$

### Other important forms of de-Broglie wavelength (AKTU loves asking these as numericals — memorize all 4)

**(1) In terms of Kinetic Energy (E):**
Since E = p²/2m → p = √(2mE)

$$\lambda = \frac{h}{\sqrt{2mE}}$$

**(2) In terms of Temperature (T):**
Since E = (3/2)kT (average thermal KE), where k = Boltzmann's constant = 1.38 × 10⁻²³ J/K

$$\lambda = \frac{h}{\sqrt{3mkT}}$$

**(3) For a charged particle (charge q) accelerated through potential V:**
KE gained = qV, so E = qV

$$\lambda = \frac{h}{\sqrt{2mqV}}$$

**(4) Specifically for an ELECTRON accelerated through potential V volts** (most common numerical):
Plug in mₑ = 9.1×10⁻³¹ kg, q = 1.6×10⁻¹⁹ C, h = 6.63×10⁻³⁴:

$$\lambda = \frac{12.28}{\sqrt{V}} \text{ Å}$$

**This is the single most-used formula for numericals — memorize it.**

### Properties of Matter Waves (theory question — write all points)
1. Matter waves are associated with a moving particle and do **not depend on charge** (so even neutral particles like neutrons have matter waves).
2. Matter waves do NOT have any associated electric/magnetic field (unlike light waves).
3. Matter waves do NOT travel through vacuum (unlike EM waves) — actually associated wave exists wherever particle exists.
4. Matter waves are NOT electromagnetic in nature.
5. Velocity of matter waves is generally **more than** velocity of light (this is phase velocity — see Topic 4). [Note: some versions state differently for group velocity — group velocity = particle velocity < c]
6. de-Broglie wavelength of a **lighter** particle is **greater** than that of a heavier particle (since λ ∝ 1/√m).
7. de-Broglie wavelength of a **slow** particle is **greater** than that of a fast particle (since λ ∝ 1/v).
8. Example: electron beam.

### Quick numerical shortcuts (from your notes)
- Electron, V volts → λ = 12.28/√V Å
- α-particle (q=2e, m=4mₚ), 200V → λ ≈ 0.00717 Å (mass being ~7000× electron makes λ tiny)
- Neutron with λ = 1Å → v ≈ 3.96×10³ m/s, KE ≈ 1.309×10⁻²⁰ J

---

## TOPIC 3: Davisson–Germer Experiment (Experimental Proof of Matter Waves)

**Purpose:** In 1927, Davisson and Germer gave the **first experimental evidence** of matter waves (predicted by de-Broglie in 1924). They confirmed electrons behave as waves AND measured the wavelength.

### Setup (draw this diagram in exam — it's guaranteed to be asked)
- **Electron gun**: tungsten filament (F) heated by Low Tension Battery (L.T.B.) → thermionic emission produces electrons
- Electrons accelerated by **High Tension Battery (H.T.B.)** through potential V
- Electron beam strikes a **Nickel (Ni) crystal**
- Electrons scatter off the crystal at angle φ (scattering angle) — measured from incident direction; θ is the angle from the crystal plane
- A **movable electron collector (detector)** connected to a **galvanometer (G)** captures scattered electrons at various angles
- Deflection of galvanometer ∝ intensity of electrons received
- Entire setup enclosed in a **vacuum chamber**
- Experiment run at various accelerating voltages; significant intensity peaks observed between **44V and 68V**

### Result
- Graphs of intensity vs scattering angle φ were plotted for 44V, 48V, 54V, 64V
- A "bump" (peak) starts appearing at 44V
- **Strongest peak observed at V = 54V, at scattering angle φ = 50°**
- Beyond this, the bump size decreases with further increase in voltage

### Conclusion (calculation — memorize the logic)
The peak intensity = **constructive interference**, so **Bragg's Law** applies (crystal diffraction):

$$2d\sin\theta = n\lambda$$

From geometry: θ + θ + φ = 180° → with φ = 50°: 2θ = 130° → **θ = 65°**

Given: d (interatomic spacing of Ni) = 0.914 Å, n = 1

$$\lambda = 2 \times 0.914 \times \sin 65° = 1.66 \text{ Å (experimental value)}$$

Compare with de-Broglie's theoretical formula (λ = 12.28/√V) at V = 54V:

$$\lambda = \frac{12.28}{\sqrt{54}} = 1.67 \text{ Å (theoretical value)}$$

**Conclusion to write:** Since the experimental value (1.66 Å) closely matches the theoretical de-Broglie value (1.67 Å), this is excellent proof that de-Broglie's hypothesis of matter waves is correct.

---

## TOPIC 4: Phase Velocity and Group Velocity

### Phase Velocity (Vp)
**Definition:** The velocity with which a monochromatic wave (single frequency, single wavelength) travels through a medium. It is the characteristic of an **individual wave**.

Take a wave: y = a sin(ωt − kx)
For a point of constant phase: ωt − kx = constant. Differentiating w.r.t. t:
ω − k(dx/dt) = 0 → dx/dt = ω/k

$$V_p = \frac{\omega}{k}$$

### Phase velocity of de-Broglie wave (important derivation)
Using ω = 2πE/h (since E=hν) and k = 2πmv/h (since λ=h/mv), and E = mc²:

$$V_p = \frac{c^2}{v}$$

Since v (particle speed) < c, this means **Vp > c** — phase velocity of matter wave is greater than speed of light! This seems to violate relativity, but it's fine because phase velocity is NOT the velocity at which energy/information travels — that's the **group velocity**.

Since particle velocity v = group velocity Vg:

$$V_p \times V_g = c^2$$

### Wave Packet
A **wave packet** is a group of waves with slightly different wavelengths and velocities, such that they interfere **constructively** over a small region (where the particle is located) and interfere **destructively** everywhere else (amplitude → 0 outside). This localized packet represents the particle.

### Group Velocity (Vg)
**Definition:** The velocity with which a wave packet (group of waves) travels. It is the characteristic of a **group of waves**, and it equals the actual velocity of the particle.

$$V_g = \frac{d\omega}{dk}$$

### Derivation of Group Velocity
Take two waves of nearly equal amplitude, slightly different frequency/wavelength:
y₁ = a sin(ω₁t − k₁x), y₂ = a sin(ω₂t − k₂x)

By superposition and using sinC + sinD = 2 sin((C+D)/2) cos((C−D)/2):

$$y = 2a\cos\left(\frac{d\omega}{2}t - \frac{dk}{2}x\right)\sin(\omega t - kx)$$

This is a wave sin(ωt − kx) with amplitude A = 2a cos(dω/2 · t − dk/2 · x) that varies slowly — this slowly-varying envelope IS the wave packet, and it moves with velocity:

$$V_g = \frac{d\omega}{dk}$$

### Relation between Phase Velocity and Group Velocity

**For a dispersive medium** (velocity depends on wavelength):

$$V_g = V_p - \lambda\frac{dV_p}{d\lambda}$$

(Derived using ω = kVp, differentiating w.r.t. k, and converting to λ using k = 2π/λ)

**For a non-dispersive medium** (Vp doesn't depend on λ, so dVp/dλ = 0):

$$V_g = V_p$$

---

## TOPIC 5: Heisenberg's Uncertainty Principle (1927) — VERY IMPORTANT

### Statement
*"It is impossible to determine simultaneously and accurately the exact position and exact momentum of a microscopic particle."*

If Δx = uncertainty in position, Δpₓ = uncertainty in momentum:

$$\Delta x \cdot \Delta p_x \geq \frac{h}{4\pi}$$

Also written as: Δx·Δpₓ ≥ ħ/2, where ħ = h/2π

**Meaning:** If you measure position very precisely (Δx small), momentum becomes very uncertain (Δp large), and vice versa. You can NEVER know both perfectly at once.

### Different forms of the Uncertainty Principle
1. Position & Momentum: Δx·Δp ≥ h/4π
2. Position & Velocity: Δx·Δv ≥ h/4πm (derived by putting Δp = mΔv)
3. Energy & Time: ΔE·Δt ≥ h/4π
4. Angular Position & Angular Momentum: Δθ·ΔL ≥ h/4π

### Derivation (from de-Broglie wave packet)
de-Broglie wavelength: λ = h/p → wave number k = 2π/λ = 2πp/h
So a small uncertainty in momentum Δp gives uncertainty in k: **Δk = (2π/h)Δp** ...(3)

For a localized wave packet (from wave theory): **Δx·Δk ≥ 1/2** ...(4)

Putting (3) into (4): Δx·(2π/h)Δp ≥ 1/2
Multiply both sides by h/2π:

$$\Delta x \cdot \Delta p_x \geq \frac{h}{4\pi}$$

### Numerical Method (this is THE most common numerical type)
**Formulas to use directly:**
- Δx·Δp ≥ h/4π  → Δp ≥ h/(4π·Δx)
- Δx·Δv ≥ h/4πm → Δv ≥ h/(4πm·Δx)

**Sample Q:** Uncertainty in position of electron is 1 Å. Find uncertainty in momentum and velocity.
- Δx = 10⁻¹⁰ m
- Δp ≥ h/(4πΔx) = 6.626×10⁻³⁴/(4π×10⁻¹⁰) ≈ **5.27×10⁻²⁵ kg·m/s**
- Δv ≥ h/(4πmΔx) = ...≈ **5.79×10⁵ m/s**

**Sample Q type 2:** Momentum measured with accuracy of X%. Given p, find Δx.
- Δp = (X/100) × p, then use Δx ≥ h/(4πΔp)

**Sample Q type 3:** Velocity measured with accuracy of X%. Given v, find Δx.
- Δv = (X/100) × v, then use Δx ≥ h/(4πmΔv)

### Applications of Uncertainty Principle (theory — write all 5 with brief reasoning)

**(1) Electron cannot exist inside the nucleus:**
Nucleus size Δx ≈ 10⁻¹⁴ m (extremely small) → by Δp ≥ h/4πΔx, Δp becomes extremely LARGE → electron would need enormous kinetic energy (much more than observed) → so electrons cannot be confined inside a nucleus.

**(2) Stability of the Atom:**
If electron fell into the nucleus, Δx would become very small → Δp (and KE) would become extremely large → this large energy would push the electron back out → hence electron cannot collapse into nucleus → **this explains why atoms are stable.**

**(3) Non-existence of electrons at rest in an atom:**
An electron confined in an atom has some position uncertainty Δx (finite, not infinite) → by the principle, Δp can never be exactly zero → so **the electron's momentum can never be exactly zero** → an electron in an atom can never be completely at rest.

**(4) Zero-Point Energy:**
A confined particle can never have exactly zero position uncertainty AND zero momentum uncertainty simultaneously → therefore, even at absolute zero temperature, microscopic particles retain some minimum energy → this is called **zero-point energy**.

**(5) Natural Broadening of Spectral Lines:**
Using energy-time form: ΔE·Δt ≥ h/4π. If an excited atom stays in an excited state for only a short time Δt, then its energy cannot be precisely defined (ΔE is large) → so the emitted radiation has a *range* of frequencies rather than one exact frequency → this causes natural broadening of spectral lines.

---

## TOPIC 6: Schrödinger Wave Equation

### Wave Function (Ψ, "psi")
The **wave function Ψ** represents the state of a particle at any instant — it's the quantity whose variation builds up the matter wave.

There are two forms of the Schrödinger equation:
### (i) Time-Dependent Schrödinger Wave Equation

**Derivation logic (write briefly in exam):**
Start with the general wave equation and its solution: Ψ(x,t) = Ae^(−iω(t−x/v))
Substitute ω = 2πν, v = νλ, then use ν = E/h and λ = h/p (de-Broglie), simplify using ħ = h/2π to get:

$$\Psi(x,t) = Ae^{-\frac{i}{\hbar}(Et-px)}$$

Differentiate twice w.r.t. x → get p² in terms of ∂²Ψ/∂x²
Differentiate once w.r.t. t → get E in terms of ∂Ψ/∂t
Apply conservation of energy: **E = KE + PE = p²/2m + V**

Substituting both expressions and simplifying gives the **final required equation:**

$$-\frac{\hbar^2}{2m}\frac{\partial^2\Psi}{\partial x^2} + V\Psi = i\hbar\frac{\partial\Psi}{\partial t}$$

In 3-dimensions (using ∇² = ∂²/∂x² + ∂²/∂y² + ∂²/∂z²):

$$-\frac{\hbar^2}{2m}\nabla^2\Psi + V\Psi = i\hbar\frac{\partial\Psi}{\partial t}$$

This can be written as: **(Ĥ)Ψ = (Ê)Ψ**, where:
- −ħ²/2m ∇² + V is called the **Hamiltonian operator**
- iħ ∂/∂t is called the **Energy operator**

### (ii) Time-Independent Schrödinger Wave Equation
Follow the same derivation but this time apply conservation of energy differently, ending with (in 1-D):

$$\frac{\partial^2\Psi}{\partial x^2} + \frac{2m}{\hbar^2}(E-V)\Psi = 0$$

In 3-D:

$$\nabla^2\Psi + \frac{2m}{\hbar^2}(E-V)\Psi = 0$$

**For a FREE PARTICLE (V = 0)** — this is the version used in "particle in a box" (Topic 7):

$$\nabla^2\Psi + \frac{2m}{\hbar^2}E\Psi = 0$$

### Physical Interpretation of Wave Function (Born Interpretation, 1926, by Max Born)
- Ψ is a **complex function** (may contain i)
- The **probability of finding a particle** at a point (x,y,z) at time t is proportional to **|Ψ|²**, called the **probability density**
- Ψ itself is called the **probability amplitude**
- Since the particle is certainly *somewhere* in space, total probability = 1:

$$\iiint |\Psi|^2 \, dx\,dy\,dz = 1$$

This is called the **Normalization Condition**, and Ψ satisfying this is called a **normalized wave function**.

### Eigenvalues and Eigenfunctions
The specific energy values E for which the time-independent Schrödinger equation can be solved are called **eigenvalues**, and the corresponding wave functions are called **eigenfunctions**.

### Characteristics (properties) of a valid wave function — MUST memorize (very common 2-mark question)
1. It must be **normalized** (satisfies the normalization condition above)
2. It must be **finite everywhere**
3. It must be **single-valued**
4. It must be **continuous**, and its first derivative should also be continuous

---

## TOPIC 7: Particle in a One-Dimensional Box (Infinite Potential Well)

This is the **most important application** — practically guaranteed in the exam (both theory derivation AND numerical).

### Setup
A particle of mass m moves freely along the x-axis between two rigid, infinitely high walls at x = 0 (wall A) and x = L (wall B). The particle is free to move *between* the walls but cannot exist outside them.

**Potential function:**
$$V(x) = \begin{cases} 0 & 0 < x < L \text{ (inside box)} \\ \infty & x < 0 \text{ and } x > L \text{ (outside/at walls)} \end{cases}$$

Since V = ∞ outside, Ψ = 0 outside the box (particle can never be found there).

### Step-by-step Derivation

**Step 1:** Use the time-independent Schrödinger equation for a free particle (V=0) inside the box:

$$\frac{d^2\Psi}{dx^2} + \frac{2mE}{\hbar^2}\Psi = 0$$

Let k² = 2mE/ħ² ...(1), so:

$$\frac{d^2\Psi}{dx^2} + k^2\Psi = 0 \quad ...(2)$$

**Step 2:** General solution of equation (2):

$$\Psi = A\sin(kx) + B\cos(kx) \quad ...(3)$$

**Step 3: Apply first boundary condition** — at x = 0, Ψ = 0:
0 = A·sin(0) + B·cos(0) = 0 + B → **B = 0**

Putting B = 0 in (3):

$$\Psi = A\sin(kx) \quad ...(4)$$

**Step 4: Apply second boundary condition** — at x = L, Ψ = 0:
0 = A sin(kL). Since A ≠ 0 (otherwise Ψ = 0 everywhere, meaning no particle at all — not physical), we need:

sin(kL) = 0 → kL = ±nπ

$$k = \frac{n\pi}{L} \quad ...(5), \quad n = 1, 2, 3, ...$$

**Step 5: Find Energy (Eigenvalues)** — put k from (5) into (1):

$$\frac{2mE}{\hbar^2} = \left(\frac{n\pi}{L}\right)^2$$

Since ħ = h/2π, solving gives the famous result:

$$E_n = \frac{n^2h^2}{8mL^2}, \quad n = 1, 2, 3, ...$$

**This is THE most important formula of this unit — memorize it completely.**

So energy is **quantized** (discrete, not continuous):
- E₁ = h²/8mL² (ground state, lowest energy)
- E₂ = 4h²/8mL² = 4E₁
- E₃ = 9h²/8mL² = 9E₁
- E₄ = 16E₁, E₅ = 25E₁, and so on (Eₙ = n²E₁)

**Important observation:** Energy level spacing is NOT constant:
E₂−E₁ = 3E₁, E₃−E₂ = 5E₁, E₄−E₃ = 7E₁, E₅−E₄ = 9E₁ → **energy levels are not equally spaced** (spacing keeps increasing).

**Step 6: Find Eigenfunctions using Normalization**
Put k from (5) into (4): Ψ = A sin(nπx/L) ...(6)

Apply normalization: ∫₀ᴸ |Ψ|² dx = 1
∫₀ᴸ A²sin²(nπx/L) dx = 1

Using sin²θ = (1−cos2θ)/2, solving the integral gives:
A²L/2 = 1 → **A = √(2/L)**

**Final normalized eigenfunction (memorize this too):**

$$\Psi_n = \sqrt{\frac{2}{L}}\sin\left(\frac{n\pi x}{L}\right)$$

### Graphs (draw these — commonly asked)
For n = 1, 2, 3, 4, sketch three graphs side by side:
1. **Energy levels (Eₙ)**: horizontal lines at increasing (unequal) spacing
2. **Wave function (Ψ)**: n=1 is a single hump, n=2 has one node in middle (looks like one full sine wave), n=3 has 2 nodes, n=4 has 3 nodes
3. **Probability density (|Ψ|²)**: always positive humps — n=1 has 1 hump, n=2 has 2 humps, n=3 has 3 humps, n=4 has 4 humps

### Numerical formula to use directly
$$E_n = \frac{n^2h^2}{8mL^2}$$

Plug in n, h = 6.63×10⁻³⁴, m (mass of particle — electron/neutron/proton), L (box width in meters). Convert answer to eV by dividing by 1.6×10⁻¹⁹.

**Sample results from your notes (use as sanity check for your own calculations):**
- Electron in box of width 2.5×10⁻¹⁰ m → E₁ = 6.04 eV, E₂ = 24.15 eV
- Neutron in box of width 10⁻¹⁴ m (nucleus size) → lowest energy E₁ = 2.05 MeV
- Electron in box of width 3.5×10⁻⁹ m → E₁ = 3.08×10⁻² eV, E₂ = 12.32×10⁻² eV
- Electron in 1 Å box, energy needed to go from ground state to 1st excited state: ΔE = E₂−E₁ = 113.1 eV (this equals 3E₁, since E₂−E₁ = 4E₁−E₁ = 3E₁)

---

## MASTER FORMULA SHEET (revise this 30 minutes before exam)

| Concept | Formula |
|---|---|
| de-Broglie wavelength | λ = h/p = h/mv |
| ...in terms of KE | λ = h/√(2mE) |
| ...in terms of Temperature | λ = h/√(3mkT) |
| ...for charge q, potential V | λ = h/√(2mqV) |
| ...for electron, potential V | λ = 12.28/√V Å |
| Bragg's Law (Davisson-Germer) | 2d sinθ = nλ |
| Phase velocity | Vp = ω/k |
| Phase velocity (de-Broglie) | Vp = c²/v |
| Group velocity | Vg = dω/dk |
| Vp–Vg relation | Vp·Vg = c² |
| Vg (dispersive medium) | Vg = Vp − λ(dVp/dλ) |
| Vg (non-dispersive medium) | Vg = Vp |
| Heisenberg (position-momentum) | Δx·Δp ≥ h/4π |
| Heisenberg (position-velocity) | Δx·Δv ≥ h/4πm |
| Heisenberg (energy-time) | ΔE·Δt ≥ h/4π |
| Schrödinger (time-dependent) | −ħ²/2m ∇²Ψ + VΨ = iħ ∂Ψ/∂t |
| Schrödinger (time-independent) | ∇²Ψ + (2m/ħ²)(E−V)Ψ = 0 |
| Normalization condition | ∭\|Ψ\|² dxdydz = 1 |
| Particle in box — Energy | Eₙ = n²h²/8mL² |
| Particle in box — Wave function | Ψₙ = √(2/L) sin(nπx/L) |

---

## LIKELY EXAM QUESTIONS (compiled from all your DPPs)

1. What are the limitations/inadequacy of classical mechanics?
2. State de-Broglie hypothesis. Derive the expression for de-Broglie wavelength (in terms of KE, temperature, accelerating potential).
3. Describe the Davisson-Germer experiment with a neat diagram. How does it verify de-Broglie's hypothesis?
4. Define phase velocity and group velocity. Derive the relation between them for dispersive and non-dispersive media.
5. Define wave packet with a diagram.
6. State and prove/derive Heisenberg's Uncertainty Principle. Write its applications.
7. Numerical: given Δx (or Δv, or Δp with % accuracy), find the other uncertainty.
8. Derive time-dependent and time-independent Schrödinger wave equations.
9. Explain the physical significance (Born interpretation) of the wave function.
10. Derive the Schrödinger equation for a particle in a one-dimensional box. Find energy eigenvalues and normalized eigenfunctions.
11. Numerical: find lowest 1-2 energy levels of an electron/neutron in a given box width.
12. Numerical: find energy difference between ground state and first excited state for particle in a box.

**Good luck for your exam tomorrow — you now have every single concept and formula from all 6 lectures in one place.**
