# QUANTUM-TELEPORTATION
A beginner-level quantum teleportation project using Python and Qiskit, exploring quantum entanglement, Bell states, quantum gates, classical communication, and quantum-state fidelity through simulation.

# Quantum Teleportation Using Python and Qiskit

## Project Overview

This project explores **quantum teleportation**, a fundamental protocol in quantum information science that allows an unknown quantum state to be transferred from one qubit to another using quantum entanglement, classical communication, and appropriate quantum operations.

The project was developed as a beginner-level learning project to understand the mathematical foundations and circuit implementation of quantum teleportation using Python and Qiskit by me.

## Objectives

* Understand the mathematical representation of a single-qubit quantum state.
* Explore quantum entanglement and Bell states.
* Understand the role of CNOT and Hadamard gates in the teleportation protocol.
* Study Alice's measurements and the classical information sent to Bob.
* Implement Bob's correction operations using Pauli-X and Pauli-Z gates.
* Examine state fidelity to evaluate how closely the recovered state matches the original state.

## Theoretical Background

An arbitrary pure qubit state can be represented as

$$
|\psi\rangle = \alpha|0\rangle+\beta|1\rangle
$$

where \(\alpha\) and \(\beta\) are complex probability amplitudes satisfying

$$
|\alpha|^2+|\beta|^2=1.
$$

Quantum teleportation uses three qubits:

1. **Alice's input qubit:** Contains the quantum state to be transferred.
2. **Alice's entangled qubit:** One half of a shared Bell pair.
3. **Bob's qubit:** The other half of the Bell pair, which is used to reconstruct the input state.

The protocol involves preparing an entangled Bell pair, applying quantum gates, measuring Alice's two qubits, communicating the classical measurement results, and applying conditional correction gates to Bob's qubit.

The correction operations are based on the measurement outcomes:

| Alice's measurement | Bob's correction                                             |
| ------------------- | ------------------------------------------------------------ |
| 00                  | Identity (\(I\))                                             |
| 01                  | Pauli-X (\(X\))                                              |
| 10                  | Pauli-Z (\(Z\))                                              |
| 11                  | Pauli-X and Pauli-Z (\(XZ\), up to global phase conventions) |

**Important:** The measurement labels above use Alice's conceptual bit order. Qiskit's displayed classical bitstrings can appear in the reverse order depending on how classical bits are assigned and displayed.

Quantum teleportation does not physically transport a particle or allow faster-than-light communication. It transfers the quantum state using shared entanglement and classical communication, and the original state is not retained as an independent copy.

## Tools and Technologies

* **Python** — programming and numerical calculations
* **NumPy** — complex numbers, vectors, matrices, and state calculations
* **Qiskit** — quantum circuit construction and simulation
* **Qiskit Aer** — circuit simulation, if used in the implementation
* **Matplotlib** — visualizing results, if used

## Project Workflow

1. Define and normalize the input quantum state.
2. Prepare a Bell pair between Alice and Bob.
3. Apply Alice's CNOT and Hadamard operations.
4. Measure Alice's qubits.
5. Apply the corresponding correction operations to Bob's qubit.
6. Test the protocol with selected input states.
7. Use state fidelity to compare the original and recovered states.

## Testing and Analysis

The project explores the teleportation protocol using selected input states, including computational-basis states and superposition states, where implemented.

State fidelity can be used to quantify the similarity between the original pure state \(|\psi\rangle\) and the recovered state \(|\phi\rangle\):

$$
F=|\langle\psi|\phi\rangle|^2.
$$

For an ideal simulation, a fidelity of \(1\) indicates that the recovered state matches the original state, apart from an irrelevant global phase.

## Key Learning Outcomes

Through this project, I explored:

* The mathematical representation of quantum states.
* The relationship between entanglement and quantum information.
* The use of quantum gates to implement a quantum protocol.
* The role of measurement and classical communication in quantum teleportation.
* The use of state fidelity to assess a reconstructed quantum state.
* The process of building, testing, documenting, and organizing a quantum computing project.

## Limitations

This is an educational simulation project. Its conclusions depend on the implemented circuit and simulator settings. It does not demonstrate a physical teleportation experiment or the transfer of quantum states over a real quantum communication channel.

## Future Improvements

* Test a broader range of normalized input states.
* Compare results across different simulator configurations.
* Investigate the effects of measurement statistics and simulated noise.
* Explore execution on available quantum hardware as a future extension.

## Acknowledgment

This project is part of my independent learning journey in quantum mechanics and quantum computing as an Applied Mathematics undergraduate. It is intended to strengthen my understanding of quantum states, entanglement, quantum circuits, and quantum information protocols.

## References

* [Qiskit Documentation](https://docs.quantum.ibm.com/)
* [IBM Quantum Learning](https://quantum.cloud.ibm.com/learning)
*
