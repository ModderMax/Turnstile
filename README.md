# Introduction
Turnstile antennas are a collection of dipoles phased together as an array to create polarization, all using one axis.  
They are not the easiest antenna to make, though with the help of some tools, construction can become easier.

The premise of turnstiles — and any phased array — is the addition of multiple weaker signals to create one stronger signal.  
⚠ **Check:** This description is broadly correct, but you might clarify that gain depends on proper phasing, spacing, and array factor. Improper phasing can cause loss instead of gain.

---

## Phase
In order to benefit from receiving the same signal from multiple sources, the signals need to be combined.  

- If two signals are perfectly **in phase**, they are additive.
- If the two signals are **180° out of phase**, they cancel each other out.
- If they are phased anywhere in between, distortion occurs — reducing amplitude and creating a “muddy” signal.  

This phase offset also affects the **radiation pattern**, potentially making an *elliptical* polarization.

![Combining two signals](./images/mixing.jpg "Combining two signals")

---

### Phase Related to Polarization
In a 3D space, circular polarization could be represented like a helix.  
If we flatten this to two dimensions and use time as the third, we can illustrate how a circularly polarized signal might be received by a simple cross dipole *without* phasing.

![Circular Polarization](./images/circular_polarization.gif "Circular Polarization")

⚠ **Note:** While not a perfect demonstration, this shows that the signal received by each element reaches the receiver at a different point in time.  
Given that these appear as waves, and a signal “pulse” represents one phase point, a mismatch will cause partial or full cancellation if signals are not synchronized.

---

## Coaxial Cables
We can use coax cables to create a delay in signal, since electromagnetic waves take time to propagate through any medium.  
⚠ **Check:** This is not due to electron drift speed, but rather the wave’s propagation velocity in the dielectric.

![Phase measurement](./images/sampling.jpg "Phase measurement")

Most coaxial cables list a **Velocity Factor** (VF) or **Velocity of Propagation** (Vp) — the fraction of the speed of light in a vacuum at which a signal travels in the cable. Most coax falls between **60%** and **85%**.

![Velocity Factor](./images/VF.jpg "Velocity Factor")

When creating phase lines, VF becomes vital:  
- Two coaxial cables of equal length but different VF will deliver the signal at different times.
- One full **360° phase change** equals one wavelength, but in coax the wavelength is reduced by VF:  

⚠ **Check:** The explanation here could mention frequency dependence — at higher frequencies, the same length produces a greater phase shift.

If we precisely measure coax length, we can delay signals so that, when they converge, they are in sync.

![Circular Polarization in Phase](./images/phased_circular_polarization.gif "Circular Polarization in Phase")

We can compare this to the [non-phased example](#phase-related-to-polarization): with proper delay, both signals reach the receiver in phase, adding to amplitude.

---

## Tips for Making Turnstile Antennas

### Use Coax with a High Velocity Factor
Since a full 360° phase shift requires more *physical* length with higher VF, you can afford slightly larger measurement errors.  
Example:  
- Coax with **60% VF** → ~1° error per cm
- Coax with **80% VF** → ~0.75° error per cm

Here is a [Coax Phase Length Calculator](./docs/calculator.html) to find the length of coax for a given frequency and phase. 

⚠ The example above is not all-inclusive. It was calculated at 50mhz; wavelength decreases as frequency increases.
⚠ The calculator does not include the phase of added connectors. From my experience, a pair of male SMAs add ~25mm @ 100% VF, or about 2.5° per connector at 137mhz.

### Aim for using in VHF or lower frequency ranges.

### Use connectors to your advantage


---

# Circularly Polarized Turnstiles
Circular polarization can be achieved by:
- **Element geometry** (e.g., QFH, asymmetric turnstile)
- **Delays** (phase lines)

---

## Axial Turnstile & Crossed Yagi-Uda
The classic axial-mode turnstile uses a pair of dipoles at a 90° offset.  
Polarization can be switched between **LHCP** and **RHCP** by changing which dipole is delayed by 90°.

⚠ **Note:** Just like dipoles can use directors and reflectors, so can turnstiles.

---

## Asymmetric Turnstile
An asymmetric turnstile does not use phase lines. Instead, it uses angled elements to create an approximate circular polarization.  
⚠ **Check:** This often results in *elliptical* polarization rather than perfectly circular polarization.

---

## Quad-Feed Turnstile
⚠ **TODO:** Add description. Some references describe this as a pair of crossed turnstiles at different heights to improve axial ratio — verify before including details.

## Quad-Feed Turnstile
Double turnstile