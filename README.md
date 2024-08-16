# Analog Circuit Design for Active Noise Cancellation in Headphones

## Overview

This repository contains the documentation and code for an experiment focused on designing and implementing an analog circuit for active noise cancellation (ANC) in headphones. The goal was to achieve significant noise attenuation while ensuring system stability through compensator design.

## Experiment Details

### Introduction

The objective of this experiment was to design an analog circuit capable of active noise cancellation for headphones. The design involved:
- Using a microphone to capture surrounding noise.
- Implementing a compensator to produce signals that cancel out this noise.

### Aim

- *Attenuation*: Achieve a 20 dB attenuation at a noise frequency of 100 Hz.
- *Compensator Design*: Stabilize the system with appropriate loop shaping of the loop transfer function.

### Experimental Setup

1. *Setup*:
   - Connected the headphone setup to a function generator and Digital Storage Oscilloscope (DSO).
   - Applied a sinusoidal waveform with frequencies ranging from 100 Hz to 5000 Hz.
   - Collected data to plot magnitude and phase responses.

2. *Design*:
   - Designed an amplifier to ensure 20 dB attenuation at 100 Hz.
   - Used MATLAB to plot Bode plots for the transfer function and design a compensator.
   - Aimed for a gain margin of at least 5 dB and a phase margin of at least 30 degrees for stability.

3. *Evaluation*:
   - Measured output-to-noise ratios at 100 Hz, 500 Hz, and 1000 Hz to evaluate performance.

### Design Algorithm

- *Bode Plots*:
  - Plotted magnitude and phase Bode plots for the original and compensated systems.
  - Ensured stability by tuning poles and zeros to maintain positive phase and gain margins.
  
![Magnitude Bode Plot](Magnitude_Bode_Plot.jpg)
![Phase Bode Plot](Phase_Bode_Plot.jpg)

- *Transfer Function*:
  - Transfer Function: 40*(s+2000)^2 / ((s+50)*(s+100))


### Problems and Solutions

1. *Gain Margin Issue*:
   - Problem: Achieved attenuation of 20 dB, but gain margin calculations showed instability.
   - Solution: Recalculated resistor and capacitor values, tuned poles and zeros, and maintained positive gain margin.

2. *Circuit Issues*:
   - Problem: Defective opamp and human error in circuit assembly.
   - Solution: Replaced faulty components and corrected assembly errors.

### Results

- *Attenuation*: Achieved 11 dB attenuation.
- *Closed Loop Gain*: Approximately -10 dB.
- *Phase Margin*: 34 degrees.
- *Gain Margin*: 9 dB.
