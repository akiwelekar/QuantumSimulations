# Double Slit Experiment Simulation

This repository contains a Python script that simulates the double-slit experiment, a fundamental demonstration of wave-particle duality in quantum mechanics.

## Overview

The simulation models the behavior of particles (like electrons or photons) as they pass through two narrow slits and hit a screen. When particles are sent through one slit at a time, they build up a distribution on the screen that corresponds to the shape of the slit. However, when both slits are open, an interference pattern emerges on the screen, even when particles are sent one at a time. This pattern is characteristic of waves interfering with each other, suggesting that particles exhibit wave-like behavior.

## Simulation Details

The simulation uses the following steps:

1. **Define Parameters:** Sets up the simulation parameters, including the number of particles, screen width, slit distance, and wavelength of the associated wave.
2. **Calculate Wavefunction:** Calculates the wavefunction for the combined effect of the two slits on the screen, based on the principles of wave superposition. The wavefunction $\Psi(x)$ at a point $x$ on the screen is given by the superposition of the waves from each slit:
   $$ \Psi(x) = \psi_1(x) + \psi_2(x) $$
   where $\psi_1(x)$ and $\psi_2(x)$ are the wavefunctions from slit 1 and slit 2, respectively. In this simulation, we use a Gaussian-modulated wave:
   $$ \psi(x, x_0) = e^{-(x - x_0)^2 / 2\sigma^2} e^{i k (x - x_0)} $$
   where $x_0$ is the center of the slit, $\sigma$ is related to the width of the Gaussian, and $k = 2\pi / \lambda$ is the wave number.

3. **Determine Probability Distribution:** Derives the probability distribution of where particles are likely to hit the screen from the squared magnitude of the wavefunction. The probability density $P(x)$ is given by:
   $$ P(x) = |\Psi(x)|^2 $$
   This probability distribution shows the characteristic interference pattern.

4. **Generate Particle Hits:** Randomly generates particle hit positions on the screen according to the calculated probability distribution.
5. **Animate Particle Detection:** Creates an animation showing the particles hitting the screen one by one, gradually building up the interference pattern.

## Getting Started

To run the simulation, you need to have Python installed along with the following libraries:

- numpy
- matplotlib
- matplotlib.animation

You can install these libraries using pip:
