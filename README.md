# Introduction
Turnstile antennas are a collection of Dipoles phased together as an array to create polarization, all using one axis. It's not an easy antenna to make, though with the help of some tools it can become easier.

The whole premise of turnstiles, and any phased array is going to be addition of multiple weaker signals to create one stronger signal.

## Phase
In order to benefit from receiving the same signal from multiple sources, the signals need to be combined. If two signals are perfectly in phase with one another, they are additive. If the two signals are 180° from one another, they cancel each other out. 
![Alt text](./images/mixing.jpg "Combining two signals")

If the signals are phased apart anywhere in-between, distortion is created. This makes the signal more difficult to read, lose amplitude, and become "muddy". When it comes to antennas, this kind of offset also affects the radiation pattern of the antenna, making an elipses polarization.

### Phase related to polarization
In a 3D space, circular polarization could be represented like a helix. If we flatten this down to two dimensions, and use time as the third, it's possible to illustrate a circularly polarized signal might be received by a simple cross dipole without phasing 

![Alt text](./images/circular_polarization.gif "Circular Polarization")

While this is not a perfect demonstration, it's enough to demonstrate how the signal received by each element would be seen at the receiver at a different point in time.
Given that these appear as waves, and the signal 'pulse' really only represents one point in the phase of the signal- it would result in a cancellation effect if the signals are not in sync.

## Coaxial Cables
We can use coax cables to create a delay in signal, since electrons take time to travel across a wire. (or through any space) Thus, we can measure a different phase at two given points in space, since it does travel. ![Alt text](./images/sampling.jpg "Phase measurement")


Most coaxial cables should have a listed Velocity factor, or Velocity Propogation. This is a number that represents how fast the signal will travel through this specific cable, and it will be a percentage of the speed of light in a vaccum. Most Coax will be somewhere between 60% and 85%. In most RF applications, Vp does not play much of a role, however when creating accurate phase lines it becomes a vital metric.

![Alt text](./images/VF.jpg "Velocity Factor")

here we have two coaxial cables. assuming the same exact signal going through them and same lenght, the cable with a higher propogation factor will get the signal through it faster, and the number of 360° phase changes (one wavelength) that occur in the time it takes to travel across the length will be fewer. If we can precisely measure out a length of coax, we can delay signals so that when they converge, they are in sync. ![Alt text](./images/phased_circular_polarization.gif "Circular Polarization in Phase")

We can see the difference between the phased and [non-phased](https://github.com/ModderMax/Turnstile?tab=readme-ov-file#phase-related-to-polarization) here, as when the signal would be delayed by the appropriate amount, the signals reach the receiver at the same time, thus adding to the amplitude.

# Making Phase Lines

# Circularly Polarized Turnstiles
Circular polarization can be achieved with special design of the elements (eg. QFH and Asymmetric turnstiles) or by using delays, such as phase lines.
## Axial Turnsile & Crossed yagi-uda
## Asymmetric Turnstile
## Quad-Feed Turnstile
