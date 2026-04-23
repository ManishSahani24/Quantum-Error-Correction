# Quantum Error Correction

There are very significant challenges that must be overcome before we can reliabily implement the sorts of large-scale quantum computations we hope will one day be possible.

Quantum information is extremely fragile -- You can literally ruin it just by looking at it. For this reason, to correctly operate, quantum computers need to isolate the quantum information they store from the environment around them to an extreme degree.

-> Suspectible to both inaccuracies and environmental noise. 

## Core Objective
The primary challenge in quantum computing is protecting the **logical qubit** from environmental decoherence. This repository explores the mathematical mapping of a single logical state $\alpha|0\rangle + \beta|1\rangle$ into a higher-dimensional **multi-qubit entangled subspace** to enable fault tolerance.

---

## Implementations

### 1. The 3-Qubit Repetition Codes
Protecting against independent Pauli noise:
* **Bit-Flip Code ($X$):** Uses redundancy to protect against state-flip errors.
* **Phase-Flip Code ($Z$):** Uses the Hadamard basis to transform phase errors into bit-flip errors for correction.
* **Syndrome Measurement:** Implementation of ancilla-driven parity checks to detect errors without collapsing the logical superposition.

### 2. The Shor 9-Qubit Code
Shor’s 9-qubit code, introduced by Peter Shor in 1995, is the first quantum error-correcting code designed to protect a single logical qubit from arbitrary single-qubit errors (both bit-flips 
and phase-flips )

The Shor code is constructed through a two-stage concatenated encoding process. 

The standard Shor implementation utilizes a Phase-Flip code as the outer code and a Bit-Flip code as the inner code.

<img width="888" height="351" alt="image" src="https://github.com/user-attachments/assets/9edfcb42-b2d8-41fd-959c-db1d1ecdf41c" />


### 3. Discretization of Error




---

## Technical Implementation Details
* **Framework:** Qiskit (Python)

---
