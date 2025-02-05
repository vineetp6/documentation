---
title: SwapGate
description: API reference for qiskit.circuit.library.SwapGate
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.circuit.library.SwapGate
---

# SwapGate

<span id="qiskit.circuit.library.SwapGate" />

`qiskit.circuit.library.SwapGate(label=None)`

Bases: [`Gate`](qiskit.circuit.Gate "qiskit.circuit.gate.Gate")

The SWAP gate.

This is a symmetric and Clifford gate.

Can be applied to a [`QuantumCircuit`](qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit") with the [`swap()`](qiskit.circuit.QuantumCircuit#swap "qiskit.circuit.QuantumCircuit.swap") method.

**Circuit symbol:**

```python
q_0: ─X─
      │
q_1: ─X─
```

**Matrix Representation:**

$$
\begin{split}SWAP =
    \begin{pmatrix}
        1 & 0 & 0 & 0 \\
        0 & 0 & 1 & 0 \\
        0 & 1 & 0 & 0 \\
        0 & 0 & 0 & 1
    \end{pmatrix}\end{split}
$$

The gate is equivalent to a state swap and is a classical logic gate.

$$
|a, b\rangle \rightarrow |b, a\rangle
$$

Create new SWAP gate.

## Attributes

<span id="qiskit.circuit.library.SwapGate.condition_bits" />

### condition\_bits

Get Clbits in condition.

<span id="qiskit.circuit.library.SwapGate.decompositions" />

### decompositions

Get the decompositions of the instruction from the SessionEquivalenceLibrary.

<span id="qiskit.circuit.library.SwapGate.definition" />

### definition

Return definition in terms of other basic gates.

<span id="qiskit.circuit.library.SwapGate.duration" />

### duration

Get the duration.

<span id="qiskit.circuit.library.SwapGate.label" />

### label

Return instruction label

<span id="qiskit.circuit.library.SwapGate.name" />

### name

Return the name.

<span id="qiskit.circuit.library.SwapGate.num_clbits" />

### num\_clbits

Return the number of clbits.

<span id="qiskit.circuit.library.SwapGate.num_qubits" />

### num\_qubits

Return the number of qubits.

<span id="qiskit.circuit.library.SwapGate.params" />

### params

return instruction params.

<span id="qiskit.circuit.library.SwapGate.unit" />

### unit

Get the time unit of duration.

## Methods

### control

<span id="qiskit.circuit.library.SwapGate.control" />

`control(num_ctrl_qubits=1, label=None, ctrl_state=None)`

Return a (multi-)controlled-SWAP gate.

One control returns a CSWAP (Fredkin) gate.

**Parameters**

*   **num\_ctrl\_qubits** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")) – number of control qubits.
*   **label** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)") *or None*) – An optional label for the gate \[Default: None]
*   **ctrl\_state** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")  *or*[*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)") *or None*) – control state expressed as integer, string (e.g. ‘110’), or None. If None, use all 1s.

**Returns**

controlled version of this gate.

**Return type**

[ControlledGate](qiskit.circuit.ControlledGate "qiskit.circuit.ControlledGate")

### inverse

<span id="qiskit.circuit.library.SwapGate.inverse" />

`inverse()`

Return inverse Swap gate (itself).

