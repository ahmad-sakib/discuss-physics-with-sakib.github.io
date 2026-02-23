---
layout: single
title: "Nuclear Physics"
date: 2026-02-23 23:00:00 +0600
categories: [Personal]
tags: [friends, life]
description: "A beginner-friendly, step-by-step guide to creating a GitHub Pages blog using the Jekyll static site generator on Arch Linux. This post covers setting up a Ruby environment, configuring local gem paths, installing Jekyll and Bundler, resolving common pitfalls (including the `webrick` requirement for Ruby 3+), running the site locally, and pushing your project to GitHub with fully explained bash command snippets for self-documentation."

---

# Nuclear Binding Energy & Mass Models — Answers

---

## **1. Definition: Nuclear Binding Energy**

The mass of a nucleus ($M$) is always less than the sum of the masses of its individual nucleons (protons and neutrons). When free nucleons combine to form a nucleus, energy is released in the form of photons; this energy is the **nuclear binding energy** ($B$).  

It is also the energy required to **break a nucleus into its constituent protons and neutrons**.

**Formula:**
  
$$
B = [Z m(^1\text{H}) + N m_n - m(^A X)] c^2
$$

where:  
- $m(^1\text{H})$ = mass of a hydrogen atom  
- $m_n$ = mass of a neutron  
- $m(^A X)$ = mass of the nucleus

---

## **2. The Average Binding Energy per Nucleon Curve**

- **$B/A$ vs $A$ curve** shows nuclear stability across elements.  

### Regions:

1. **Constant Region ($A \approx 30–100$):**  
   - Average $B/A \approx 7.8$ MeV, peak $\approx 8.7$ MeV  
   - Shows **short-range nuclear forces**; each nucleon interacts with nearest neighbors

2. **Heavy Nuclei ($A > 100$):**  
   - $B/A$ decreases slowly due to **Coulomb repulsion** ($\propto Z^2$)

3. **Light Nuclei ($A < 30$):**  
   - $B/A$ decreases because **surface nucleons** are less bound

- **Stability:** Nuclei of intermediate mass are the most stable.  
- **Energy release:** Fission (splitting heavy nuclei) or fusion (joining light nuclei) moves nuclei toward this peak.

---

## **3. SEMF — Underlying Assumptions**

The **Semi-Empirical Mass Formula (SEMF)** is based on the **liquid-drop model**:

- **Uniform Density:** Nucleus has constant interior density, dropping abruptly at surface
- **Volume Proportionality:** $V \propto A$, radius $R \propto A^{1/3}$
- **Saturation of Nuclear Forces:** Volume term $\propto A$; each nucleon interacts with nearest neighbors
- **Correction Factors:**
  - **Surface term:** nucleons at edge are less bound
  - **Coulomb term:** proton-proton repulsion
  - **Asymmetry term:** favors $N = Z$
  - **Pairing term:** favors even numbers of protons/neutrons

---

## **4. SEMF: Percentage Contribution to $B/A$**

**Constants:** $a_v = 15.5$ MeV, $a_s = 16.8$ MeV, $a_c = 0.72$ MeV, $a_{sym} = 23$ MeV

| Mass Number ($A$) | Volume | Surface | Coulomb | Asymmetry |
|------------------|--------|---------|---------|-----------|
| **60** (Z ≈ 27)  | +15.5  | -4.30   | -2.23   | -0.23     |
| **240** (Z ≈ 92) | +15.5  | -2.70   | -4.39   | -1.25     |

**Percentage of total $B/A$:**

- **A = 60 ($B/A \approx 8.74$ MeV)**  
  - Volume: 177%  
  - Surface: -49%  
  - Coulomb: -25.5%  
  - Asymmetry: -2.6%

- **A = 240 ($B/A \approx 7.16$ MeV)**  
  - Volume: 216%  
  - Surface: -38%  
  - Coulomb: -61%  
  - Asymmetry: -17%

---

## **5. SEMF: Comparison of Isotopes**

**Formula:**  
\[
B/A = a_v - a_s A^{-1/3} - a_c Z^2 A^{-4/3} - a_{sym} \frac{(A-2Z)^2}{A^2}
\]

- **$^{21}\text{Ne}$ (A=21, Z=10):** $B/A \approx 8.11$ MeV/nucleon (low due to surface effects)  
- **$^{56}\text{Fe}$ (A=56, Z=26):** $B/A \approx 8.71$ MeV/nucleon (peak stability)  
- **$^{235}\text{U}$ (A=235, Z=92):** $B/A \approx 7.50$ MeV/nucleon (lower due to Coulomb repulsion)

---

## **6. Mass Parabola ($M$ vs $Z$) for A = 128**

- **Even A = 128 → two parabolas** due to **pairing term ($\delta$)**

  1. **Even-even nuclei** (Z even, N even): lower parabola → more stable  
  2. **Odd-odd nuclei** (Z odd, N odd): upper parabola → less stable

- **Implication:** Enables **double beta decay** where nucleus decays from lower parabola to lower parabola, skipping odd-odd states.

---

**Analogy:** Nuclear binding energy is like a **communal bank account**. Nucleons "pay" some mass to join. Tiny nuclei are inefficient (surface nucleons not fully contributing), huge nuclei unstable (too much Coulomb "bickering"), but medium nuclei like Iron-56 are optimally organized, holding resources most tightly.
# Nuclear Radius & Stability — Answers

---

## **1. Radius Calculation: $^{238}\text{U}$**

The radius of a nucleus is given by:

\[
R = R_0 A^{1/3}
\]

- $R_0 \approx 1.2 \text{ fm}$  
- For $^{238}\text{U}$, $A = 238$:

\[
R = 1.2 \times (238)^{1/3} \approx 1.2 \times 6.2 \approx 7.44 \text{ fm}
\]

> The nuclear radius is approximately **7.44 fm**.

---

## **2. Stability Calculation: Most Stable Nucleus among Light Nuclei**

Average binding energy per nucleon ($B/A$) determines stability.

**Total binding energy formula:**

\[
B = [Z m_p + N m_n - M] c^2, \quad c^2 = 931.5 \text{ MeV/u}
\]

| Nucleus | Z | N | B (MeV) | B/A (MeV/nucleon) |
|---------|---|---|----------|------------------|
| $^{3}_{2}\text{He}$ | 2 | 1 | 7.717 | 2.57 |
| $^{3}_{1}\text{H}$ | 1 | 2 | 8.481 | 2.83 |
| $^{4}_{2}\text{He}$ | 2 | 2 | 29.318 | 7.33 |

> **Most stable:** $^{4}_{2}\text{He}$ (alpha particle), highest $B/A$.

---

## **3. Isobar Stability ($A=128$)**

- For a fixed mass number $A$, the most stable isobar occurs at **$Z_{\text{min}}$**, bottom of the **mass parabola**:

\[
Z_{\text{min}} \approx \frac{A}{2} \cdot \frac{1}{1 + \frac{1}{4} A^{2/3} (a_c / a_{\text{asym}})}
\]

- Constants: $a_c = 0.72$ MeV, $a_{\text{asym}} = 23$ MeV  
- For $A = 128$:

\[
Z_{\text{min}} \approx \frac{128/2}{1.199} \approx 53.39
\]

> Most stable isobars: **$Z=53$ (Iodine)** or **$Z=54$ (Xenon)**.

---

## **4. Isobar Stability ($A=112$)**

- Using the same formula for $A=112$:

\[
Z_{\text{min}} \approx \frac{112/2}{1.182} \approx 47.39
\]

> Most stable isobars: **$Z=47$ (Silver)** or **$Z=48$ (Cadmium)**.

---

## **Analogy**

- **Nuclear radius:** Like the **size of a stadium crowd**; more nucleons → larger nucleus ($R \propto A^{1/3}$)  
- **Stability ($B/A$):** Like the **strength of handshakes** in the crowd; tighter binding → harder to split, more stable
### **Topic 3: Radioactivity (Kinetics & Series)**

#### **1. Definition: What is radioactivity?**
**Radioactivity** is the property of certain nuclei that are unstable and spontaneously **emit particles or radiation** to reach a more stable state. Typically, while most mass numbers ($A$) have one or two stable isobars, all others are unstable and undergo decay processes, specifically **alpha ($\alpha$), beta ($\beta$), and gamma ($\gamma$) decay**. This spontaneous disintegration occurs in heavy or unbalanced nuclei as they "slide down" the curve of binding energy toward stability.

#### **2. Derivation: Show that a radioactive element decays exponentially with time.**
The radioactive decay law is derived from the principle that the **rate of decay ($\frac{dN}{dt}$)** is proportional to the number of existing radioactive nuclei ($N$) at that moment.
1.  We define this proportional relationship using a **decay constant ($\lambda$)**:  
    $$\frac{dN}{dt} = -\lambda N$$.
2.  Rearranging the terms to separate variables:  
    $$\frac{dN}{N} = -\lambda dt$$.
3.  Integrating both sides from the initial number of nuclei ($N_0$) at time $t=0$ to the number ($N$) at time $t$:  
    $$\int_{N_0}^{N} \frac{dN}{N} = -\int_{0}^{t} \lambda dt$$.
4.  Solving the integral results in:  
    $$\ln\left(\frac{N}{N_0}\right) = -\lambda t$$.
5.  Taking the exponential of both sides gives the **radioactive decay law**:  
    **$N(t) = N_0 e^{-\lambda t}$**.

#### **3. Radioactive Series**
Most naturally occurring radionuclides belong to one of **four radioactive series**, each beginning with a long-lived parent and ending in a stable isotope.

| Series Name | Parent Nucleus | Half-Life (Years) | Stable End Product |
| :--- | :--- | :--- | :--- |
| **Thorium** | $^{232}_{90}\text{Th}$ | $1.39 \times 10^{10}$ | $^{208}_{82}\text{Pb}$ |
| **Neptunium** | $^{237}_{93}\text{Np}$ | $2.25 \times 10^6$ | $^{209}_{83}\text{Bi}$ |
| **Uranium** | $^{238}_{92}\text{U}$ | $4.47 \times 10^9$ | $^{206}_{82}\text{Pb}$ |
| **Actinium** | $^{235}_{92}\text{U}$ | $7.07 \times 10^8$ | $^{207}_{82}\text{Pb}$ |
*(Source:)*

#### **4. Decay Plot (Parent > Daughter): Transient Equilibrium**
In the case where the **parent nucleus ($N_1$) is longer-lived than the daughter ($N_2$)**, the system eventually reaches **transient equilibrium**. The plot shows $N_1$ decaying as a steady exponential. The daughter nuclei $N_2$ initially grow from zero, reach a peak where their rate of formation equals their rate of decay, and then decay at a rate determined by the parent's half-life, with the $N_2$ curve remaining slightly above $N_1$.

#### **5. Decay Plot (Daughter > Parent)**
When the **daughter nucleus is longer-lived than the parent**, the parent ($N_1$) decays quickly to zero. The daughter ($N_2$) grows to a maximum value as the parent disappears and then **decays at its own, slower characteristic rate**. Because $\lambda_2 < \lambda_1$, the daughter curve does not parallel the parent but rather becomes the dominant activity in the sample after the parent has vanished.

#### **6. Decay Plot (Short-lived Parent): $X_1 \rightarrow X_2 \rightarrow X_3$**
For a successive decay where the parent ($X_1$) is **very short-lived** compared to the daughter ($X_2$), the parent population $N_1$ drops **precipitously toward zero** almost immediately. The daughter population $N_2$ rises rapidly to a peak and then follows its own slower exponential decay curve, effectively independent of the parent's continued existence.

#### **7. Complex Decay Calculation**
To find the **activity of alpha decay** after 10 minutes, we must consider the total decay of the parent nuclei due to both alpha and beta branches.

**Step 1: Calculate the decay constants ($\lambda$).**
*   $\lambda_{\alpha} = \frac{\ln 2}{t_{1/2,\alpha}} = \frac{0.693}{3.0 \text{ min}} = 0.231 \text{ min}^{-1}$.
*   $\lambda_{\beta} = \frac{\ln 2}{t_{1/2,\beta}} = \frac{0.693}{0.98 \text{ min}} = 0.707 \text{ min}^{-1}$.
*   The **total decay constant** is $\lambda_{tot} = \lambda_{\alpha} + \lambda_{\beta} = 0.231 + 0.707 = 0.938 \text{ min}^{-1}$.

**Step 2: Find the number of Parent nuclei ($N_X$) remaining after 10 minutes.**
*   $N(10) = N_0 e^{-\lambda_{tot}t} = (5 \times 10^{34}) \times e^{-(0.938 \times 10)}$.
*   $N(10) = 5 \times 10^{34} \times e^{-9.38} \approx 5 \times 10^{34} \times (8.44 \times 10^{-5}) = 4.22 \times 10^{30}$ nuclei.

**Step 3: Calculate the Alpha Activity ($A_{\alpha}$).**
*   $A_{\alpha} = \lambda_{\alpha} N(10) = 0.231 \text{ min}^{-1} \times 4.22 \times 10^{30}$.
*   **$A_{\alpha} = 9.75 \times 10^{29}$ decays/minute.**

***

**Analogy:** You can think of radioactive decay like a **leaky bucket**. The amount of water leaking out (activity) depends on how much water is currently in the bucket (number of nuclei). If you have two holes in the bucket (alpha and beta decay), the total water level drops faster, but the "activity" of just one specific hole is still determined by the size of that hole multiplied by the current water level.

### **Topic 4: Alpha & Beta Decay Mechanisms**

#### **1. Alpha Decay (Emission): Why $\alpha$-particles?**
Alpha emission is primarily a **Coulomb repulsion effect** that becomes dominant in heavy nuclei where the disruptive force of protons increases as $Z^2$. The $\alpha$-particle is chosen because it is an **exceptionally stable and tightly bound** structure, resulting in a small mass compared to its constituents, which maximizes the release of kinetic energy. For a typical heavy nucleus like $^{232}\text{U}$, spontaneous decay is energetically **impossible** for neighboring light particles such as protons, neutrons, deuterons, or $^3\text{He}$ ($Q < 0$), but it is **positive** for the $\alpha$-particle ($+5.41 \text{ MeV}$). While even heavier clusters like $^{12}\text{C}$ may have positive $Q$-values, their **disintegration constants are vanishingly small** compared to $\alpha$-emission due to the massive potential barrier they must penetrate.

#### **2. Alpha Decay (Energy): The 98% Q-value Distribution**
In a spontaneous alpha decay where the parent nucleus is at rest, the energy released ($Q$) is shared between the $\alpha$-particle ($T_\alpha$) and the recoiling daughter nucleus ($T_D$).
*   **Conservation of Energy:** $Q = T_D + T_\alpha$.
*   **Conservation of Momentum:** $P_D = P_\alpha$, so $m_D v_D = m_\alpha v_\alpha$.
*   Since $T = P^2 / 2m$, it follows that $T_D = T_\alpha (m_\alpha / m_D)$.
*   Substituting this into the energy equation: $Q = T_\alpha (m_\alpha / m_D) + T_\alpha = T_\alpha (1 + m_\alpha / m_D)$.
*   Rearranging gives: **$T_\alpha = Q \frac{m_D}{m_\alpha + m_D} \approx Q \frac{A-4}{A}$**.
For a typical heavy nucleus like $^{232}\text{U}$ ($A=232$), $T_\alpha = Q (228 / 232) \approx \mathbf{0.983 Q}$, proving that the $\alpha$-particle carries approximately **98%** of the decay energy.

#### **3. Beta Decay (Condition): Parent vs. Daughter Mass**
A spontaneous beta decay can only occur if the process results in a **positive energy release** ($Q > 0$), which requires the initial mass of the system to be greater than the final mass.
*   **For $\beta^-$ decay:** $Q_{\beta^-} = [m(^AX) - m(^AX')]c^2$, which is positive only if **$m(^AX) > m(^AX')$**.
*   **For $\beta^+$ decay:** $Q_{\beta^+} = [m(^AX) - m(^AX') - 2m_e]c^2$, meaning the parent atom must be heavier than the daughter by at least **two electron masses** ($1.022 \text{ MeV}$).
*   **For Electron Capture:** $Q_\epsilon = [m(^AX) - m(^AX')]c^2 - B_n$ (where $B_n$ is the electron binding energy), requiring **$m(^AX) > m(^AX')$**.

#### **4. Beta Spectrum: Contrasting $\beta^-$ and $\beta^+$ in $^{64}\text{Cu}$**
The energy spectra of electrons ($\beta^-$) and positrons ($\beta^+$) from $^{64}\text{Cu}$ show a similar continuous shape but differ significantly at lower energies. 
*   The **$\beta^+$ spectrum** contains fewer low-energy particles than the theory initially predicts, while the **$\beta^-$ spectrum** shows an excess of low-energy particles.
*   This difference arises from the **Coulomb interaction** with the daughter nucleus. The positive nuclear charge **repels the positron**, pushing it toward higher kinetic energies, while it **attracts the electron**, slowing it down and shifting the distribution toward the lower energy range.

#### **5. Cluster Decay Comparison: Q-values for $^{226}\text{Ra}$**
*   For the decay $^{226}\text{Ra} \rightarrow ^{212}\text{Pb} + ^{12}\text{C}$, the $Q$-value is significantly higher than that of alpha decay because the emission of a more massive, tightly bound cluster like $^{12}\text{C}$ leads to a **larger release of binding energy**.
*   For the alpha decay $^{226}\text{Ra} \rightarrow ^{222}\text{Rn} + ^{4}\text{He}$, the $Q$-value is approximately **$4.87 \text{ MeV}$**.
*   In contrast, a similar carbon cluster decay ($^{14}\text{C}$) from radium results in a $Q$-value of roughly **$31.8 \text{ MeV}$**. Although cluster decays have much higher $Q$-values, they are far rarer because their **Gamow factors** are much larger, making barrier penetration extremely difficult.

#### **6. Cluster Decay Half-life: $^{220}\text{Th} \rightarrow ^{208}\text{Po} + ^{12}\text{C}$**
Using the single-level barrier penetration theory for the emission of a $^{12}\text{C}$ cluster from $^{220}\text{Th}$ with $Q = 32.1 \text{ MeV}$, the calculated half-life is **$2.3 \times 10^6$ seconds**. This is approximately **13 orders of magnitude longer** than the $\alpha$-decay half-life of the same isotope, explaining why alpha decay usually masks these heavier cluster emissions.

***

**Analogy:** Imagine a nucleus as a **high-security prison**. An $\alpha$-particle is like a small, highly coordinated **escape team** of four that can slip through a narrow tunnel ($4.87 \text{ MeV}$ barrier penetration). A $^{12}\text{C}$ cluster is like a massive **prison break** involving a dozen people; while they have a much bigger "reward" (a $32.1 \text{ MeV}$ $Q$-value), they are so bulky that they almost never manage to fit through the tunnel, making their escape incredibly rare compared to the smaller team.

### **Topic 5: Nuclear Reactions, Fission & Fusion**

#### **1. Conservation Laws: What quantities are conserved in a nuclear reaction?**
In a nuclear reaction, several physical quantities must be conserved between the initial and final states:
*   **Mass-energy:** The total energy (including rest mass energy) remains constant.
*   **Linear momentum:** The vector sum of the momenta of the reacting particles is conserved.
*   **Angular momentum:** The total spin and orbital angular momentum are conserved.
*   **Charge number (Z):** The total number of protons (and thus the total electric charge) remains the same.
*   **Baryon number (A):** The total number of nucleons (protons + neutrons) is conserved.
*   **Parity:** The spatial symmetry of the system is preserved.
*   *Note:* Quantities like magnetic dipole moment and electric quadrupole moment are **not** conserved.

#### **2. Particle Identification: Identify unknown particle X**
For the reaction ${}^{26}_{12}Mg({}^{1}_{1}H, X){}^{24}_{11}Na$:
*   **Conservation of Mass Number (A):** $26 + 1 = 24 + A_X \implies A_X = 3$.
*   **Conservation of Atomic Number (Z):** $12 + 1 = 11 + Z_X \implies Z_X = 2$.
The particle with $Z=2$ and $A=3$ is **${}^{3}_{2}He$ (Helium-3)**.

#### **3. Q-Value Definition**
The **Q-value** of a nuclear reaction is defined as the difference between the kinetic energy of the final products and the kinetic energy of the incident particle (assuming the target is at rest). Alternatively, it is defined as the difference in rest mass energy between the initial reactants and the final products: **$Q = [(m_{initial}) - (m_{final})]c^2$**.

#### **4. Q-Value Expression for $X(a,b)Y$**
In the laboratory frame (where target $X$ is at rest), the Q-value can be expressed using the kinetic energy of the light product ($T_b$), the incident particle ($T_a$), and the angle of emission ($\theta$):
**$Q = (1 + \frac{m_b}{m_Y})T_b - (1 - \frac{m_a}{m_Y})T_a - \frac{2\sqrt{m_a m_b T_a T_b}}{m_Y} \cos\theta$**.

#### **5. Fission (Binding Energy): Last neutron of ${}^{236}U$**
When a ${}^{235}U$ nucleus captures a neutron ($n + {}^{235}U \rightarrow {}^{236}U^*$), the binding energy of the last neutron ($B_n$) is the excitation energy provided to the compound nucleus.
Using the semi-empirical mass formula parameters ($a_1 = 0.01691u, a_2 = 0.01911u, a_3 = 0.000763u, a_4 = 0.10175u, a_5 = 0.012u$):
**$B_n = \{[M({}^{235}U) + M_n] - [M({}^{236}U)]\}c^2 = 6.6 \text{ MeV}$**.

#### **6. Fission (Induction): Why use energetic neutrons for ${}^{238}U$?**
Thermal neutrons can induce fission in ${}^{235}U$ because its excitation energy (6.5 MeV) exceeds its activation energy (fission barrier) of 6.2 MeV. However, for **${}^{238}U$**, the excitation energy provided by a thermal neutron is only **4.8 MeV**, while its activation energy is **6.6 MeV**. Because the excitation energy is lower than the barrier, fission is inhibited unless the incident neutron is **energetic** (fast) to provide the additional kinetic energy required to surmount the barrier.

#### **7. Fission (Energy Equivalent): 500g of ${}^{235}U$**
*   Each fission event of ${}^{235}U$ releases approximately **200 MeV** of energy.
*   500g of ${}^{235}U$ contains approximately $1.28 \times 10^{24}$ atoms.
*   Total energy release $\approx (1.28 \times 10^{24} \text{ atoms}) \times (200 \text{ MeV/atom}) \times (1.6 \times 10^{-13} \text{ J/MeV}) \approx \mathbf{4.1 \times 10^{13} \text{ Joules}}$.
*(Information not in sources: This energy is equivalent to burning approximately **1,300 to 1,500 tons of coal**, depending on the coal's grade).*

#### **8. Fusion (Definition & Chain): CNO cycle**
**Fusion** is the process where two light nuclei are joined to form a heavier nucleus, releasing energy as they move toward the peak of the binding energy curve. In stars 1.5 times or more heavier than the sun, the **carbon-carbon chain (CNO cycle)** is the dominant energy source:
1.  ${}^{12}C + {}^{1}H \rightarrow {}^{13}N + \gamma$
2.  ${}^{13}N \rightarrow {}^{13}C + e^+ + \nu$
3.  ${}^{13}C + {}^{1}H \rightarrow {}^{14}N + \gamma$
4.  ${}^{14}N + {}^{1}H \rightarrow {}^{15}O + \gamma$
5.  ${}^{15}O \rightarrow {}^{15}N + e^+ + \nu$
6.  ${}^{15}N + {}^{1}H \rightarrow {}^{12}C + {}^{4}He$
The net reaction is **$4{}^{1}H \rightarrow {}^{4}He + 2e^+ + 2\nu$** with $Q = 26.7 \text{ MeV}$.

#### **9. Fusion (Coulomb Barrier): Temperature calculations**
The temperature required for fusion is determined by the need to overcome the **Coulomb barrier ($V_C$)**, which is roughly $V_C = \frac{1.44 Z_1 Z_2}{R_1 + R_2} \text{ MeV}$.
*   **For ${}^{1}_{1}H + {}^{1}_{1}H$:** The barrier is approximately **0.6 MeV**. In the Sun, this occurs with appreciable probability at a temperature of **$1.5 \times 10^7 \text{ K}$** ($kT \approx 1 \text{ keV}$) because of the high-energy tail of the Maxwell-Boltzmann distribution and tunneling.
*   **For ${}^{1}_{1}H + {}^{12}_{6}C$:** The barrier is significantly higher, approximately **2.2 MeV**. Consequently, the CNO cycle requires "higher temperatures" to proceed appreciably, generally occurring in stars where the core temperature exceeds **$2 \times 10^7 \text{ K}$**.

***

**Analogy:** Induced fission is like a **ball trapped in a valley** (the potential well). For ${}^{235}U$, dropping a tiny pebble (a thermal neutron) into the valley gives the ball enough energy to bounce right over the surrounding hills (the barrier). For ${}^{238}U$, the valley is deeper and the hills are higher; you must throw the pebble with great speed (a fast neutron) to provide the extra "kick" needed to get the ball out of the valley.