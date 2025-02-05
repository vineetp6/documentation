---
title: extensions
description: API reference for qiskit.extensions
in_page_toc_min_heading_level: 1
python_api_type: module
python_api_name: qiskit.extensions
---

<span id="module-qiskit.extensions" />

<span id="qiskit-extensions" />

<span id="quantum-circuit-extensions-qiskit-extensions" />

# Quantum Circuit Extensions

<span id="module-qiskit.extensions" />

`qiskit.extensions`

## Unitary Extensions

|                                                                                                                                    |                                                                       |
| ---------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| [`UnitaryGate`](qiskit.extensions.UnitaryGate "qiskit.extensions.UnitaryGate")(data\[, label])                                     | Class quantum gates specified by a unitary matrix.                    |
| [`HamiltonianGate`](qiskit.extensions.HamiltonianGate "qiskit.extensions.HamiltonianGate")(data, time\[, label])                   | Class for representing evolution by a Hamiltonian operator as a gate. |
| [`SingleQubitUnitary`](qiskit.extensions.SingleQubitUnitary "qiskit.extensions.SingleQubitUnitary")(unitary\_matrix\[, mode, ...]) | u = 2\*2 unitary (given as a (complex) numpy.ndarray)                 |

## Simulator Extensions

|                                                                                                                   |                                 |
| ----------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| [`Snapshot`](qiskit.extensions.Snapshot "qiskit.extensions.Snapshot")(label\[, snapshot\_type, num\_qubits, ...]) | Simulator snapshot instruction. |

## Initialization

|                                                                                                                |                                   |
| -------------------------------------------------------------------------------------------------------------- | --------------------------------- |
| [`Initialize`](qiskit.extensions.Initialize "qiskit.extensions.Initialize")(params\[, num\_qubits, normalize]) | Complex amplitude initialization. |

## Uniformly Controlled Rotations

|                                                                                                                 |                                                                     |
| --------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [`UCPauliRotGate`](qiskit.extensions.UCPauliRotGate "qiskit.extensions.UCPauliRotGate")(angle\_list, rot\_axis) | Uniformly controlled rotations (also called multiplexed rotations). |
| [`UCRXGate`](qiskit.extensions.UCRXGate "qiskit.extensions.UCRXGate")(angle\_list)                              | Uniformly controlled rotations (also called multiplexed rotations). |
| [`UCRYGate`](qiskit.extensions.UCRYGate "qiskit.extensions.UCRYGate")(angle\_list)                              | Uniformly controlled rotations (also called multiplexed rotations). |
| [`UCRZGate`](qiskit.extensions.UCRZGate "qiskit.extensions.UCRZGate")(angle\_list)                              | Uniformly controlled rotations (also called multiplexed rotations). |

## Exceptions

The additional gates in this module will tend to raise a custom exception when they encounter problems.

<span id="qiskit.extensions.ExtensionError" />

`qiskit.extensions.ExtensionError(*message)`

Base class for errors raised by extensions module.

Set the error message.

