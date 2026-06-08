# Audio Equalizer + High-Pass Filter (Proof of Concept)

## Overview

This directory contains the **Proof of Concept (PoC)** developed prior to the PCB design of a 5-band analog audio equalizer.

The objective of this stage was to validate the behavior of each filter section individually and verify that the proposed architecture met the intended frequency response requirements before committing to hardware fabrication.

The equalizer is composed of the following frequency bands:

| Band | Description |
|--------|-------------|
| Sub | Sub-bass frequencies |
| Bass | Low-frequency content |
| Mid | Mid-range frequencies |
| High | Upper mid/high frequencies |
| Treble | High-frequency content |

Additionally, a **variable high-pass filter** was implemented, allowing a continuous frequency sweep from approximately **50 Hz** to **above 20 kHz**.

---

## Objectives

The proof-of-concept stage was conducted to:

- Validate the theoretical filter designs.
- Verify cutoff frequencies of each filter stage.
- Confirm expected attenuation slopes.
- Evaluate gain behavior within the passband.
- Identify practical limitations before PCB implementation.
- Compare simulation results with real-world measurements.

---

## Methodology

### 1. Circuit Simulation

Each filter stage was initially designed and analyzed through circuit simulation.

The simulations were used to:

- Estimate cutoff frequencies.
- Observe passband behavior.
- Verify expected attenuation rates.
- Confirm unity-gain operation where applicable.
- Detect potential design issues prior to prototyping.

---

### 2. Breadboard Prototype

After simulation, the circuits were assembled on a solderless breadboard.

The prototype allowed validation of:

- Real component tolerances.
- Operational amplifier behavior.
- Interaction between stages.
- Practical implementation constraints.

---

### 3. Laboratory Validation

The assembled circuits were tested using:

- DC power supply
- AC signal source
- Digilent Analog Discovery

Measurements were performed to compare theoretical and practical responses.

---

## Frequency Response Analysis

The primary validation method consisted of generating and analyzing **Bode diagrams** for each filter section.

The Analog Discovery was used to perform frequency sweeps and obtain:

- Magnitude response
- Cutoff frequencies
- Passband gain
- Roll-off characteristics

The measurements were compared against simulation results to verify compliance with the design objectives.

---

## Validation Criteria

The proof of concept was considered successful when the following conditions were met:

- Cutoff frequencies matched design expectations.
- Passband gain remained approximately unity where required.
- Filter transitions occurred at the expected frequencies.
- Attenuation slopes followed theoretical predictions.
- No significant instability or unexpected resonances were observed.

---

## Results

The experimental measurements demonstrated that the proposed filter stages behaved consistently with the simulated designs.

The Bode plots confirmed:

- Correct cutoff frequencies.
- Expected attenuation behavior.
- Stable operation across the audio spectrum.
- Proper functionality of the variable high-pass filter across its tuning range.

These results provided sufficient confidence to proceed with the PCB design stage.

---

## Development Flow

```text
Filter Design
      │
      ▼
Circuit Simulation
      │
      ▼
Breadboard Prototype
      │
      ▼
Bode Analysis (Analog Discovery)
      │
      ▼
Design Validation
      │
      ▼
PCB Development
