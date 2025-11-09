# Quantum Teleportation in Python with Qiskit

This project demonstrates the quantum teleportation protocol using the Qiskit framework. It provides a step-by-step implementation and verification of teleporting a quantum state, specifically the superposition states |+⟩ and |-⟩.

Description

Quantum teleportation is a process by which the exact state of a quantum system can be transmitted from one location to another, with the help of classical communication and previously shared quantum entanglement. This notebook walks through the process of creating a quantum circuit to achieve this, simulating the experiment, and analyzing the results to verify the fidelity of the teleportation.

The key steps involved in the quantum teleportation protocol implemented here are:

State Preparation: Alice prepares a qubit in a specific quantum state that she wants to teleport. In this project, we use the |+⟩ and |-⟩ superposition states.

Entanglement: A Bell pair, an entangled pair of qubits, is created and shared between Alice and Bob.

Bell Measurement: Alice performs a Bell measurement on her qubit (the one she wants to teleport) and her half of the entangled pair.

Classical Communication: Alice sends the results of her measurement (two classical bits) to Bob.

State Correction: Based on the classical information received from Alice, Bob applies a specific set of quantum gates (or corrections) to his half of the entangled pair.

After these steps, Bob's qubit will be in the exact quantum state that Alice originally prepared.

Getting Started
Dependencies

Python 3

Qiskit

Matplotlib

NumPy

Installation

Clone the repository:

code
Bash
download
content_copy
expand_less
git clone https://github.com/your_username/your_repository.git
 ```
2. Install the required packages:
```bash
 pip install qiskit qiskit-aer matplotlib numpy
 ```

### Executing the program

You can run the Jupyter Notebook `quantum_teleportation.ipynb` in a Jupyter environment to see the experiment in action. The notebook is divided into cells that you can execute sequentially.

## Experiments and Results

The notebook carries out four experiments to comprehensively verify the quantum teleportation protocol:

1.  **Teleporting |+⟩ and measuring in the Z-basis:** This experiment is expected to yield a 50/50 probability of measuring |0⟩ or |1⟩, confirming that a superposition was received.
2.  **Teleporting |+⟩ and measuring in the X-basis:** This should result in measuring |+⟩ (which corresponds to an outcome of '0' in the X-basis) with 100% probability, confirming the correct state was teleported.
3.  **Teleporting |-⟩ and measuring in the Z-basis:** Similar to the first experiment, this should result in a 50/50 probability of measuring |0⟩ or |1⟩.
4.  **Teleporting |-⟩ and measuring in the X-basis:** This should result in measuring |-⟩ (which corresponds to an outcome of '1' in the X-basis) with 100% probability. This is a crucial test to ensure that the relative phase of the superposition was preserved during teleportation.

The results of these experiments, as shown in the notebook, confirm the successful teleportation of the quantum states with high fidelity, demonstrating that the phase information, a key component of quantum states, is correctly transmitted.
