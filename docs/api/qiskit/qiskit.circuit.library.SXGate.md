---
title: SXGate
description: API reference for qiskit.circuit.library.SXGate
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.circuit.library.SXGate
---

# SXGate

<span id="qiskit.circuit.library.SXGate" />

`qiskit.circuit.library.SXGate(label=None)`

Bases: [`Gate`](qiskit.circuit.Gate "qiskit.circuit.gate.Gate")

The single-qubit Sqrt(X) gate ($\sqrt{X}$).

Can be applied to a [`QuantumCircuit`](qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit") with the [`sx()`](qiskit.circuit.QuantumCircuit#sx "qiskit.circuit.QuantumCircuit.sx") method.

**Matrix Representation:**

$$
\begin{split}\sqrt{X} = \frac{1}{2} \begin{pmatrix}
        1 + i & 1 - i \\
        1 - i & 1 + i
    \end{pmatrix}\end{split}
$$

**Circuit symbol:**

```python
     ┌────┐
q_0: ┤ √X ├
     └────┘
```

<Admonition title="Note" type="note">
  A global phase difference exists between the definitions of $RX(\pi/2)$ and $\sqrt{X}$.

  $$
  \begin{split}RX(\pi/2) = \frac{1}{\sqrt{2}} \begin{pmatrix}
              1 & -i \\
              -i & 1
            \end{pmatrix}
          = e^{-i \pi/4} \sqrt{X}\end{split}
  $$
</Admonition>

Create new SX gate.

## Attributes

<span id="qiskit.circuit.library.SXGate.condition_bits" />

### condition\_bits

Get Clbits in condition.

<span id="qiskit.circuit.library.SXGate.decompositions" />

### decompositions

Get the decompositions of the instruction from the SessionEquivalenceLibrary.

<span id="qiskit.circuit.library.SXGate.definition" />

### definition

Return definition in terms of other basic gates.

<span id="qiskit.circuit.library.SXGate.duration" />

### duration

Get the duration.

<span id="qiskit.circuit.library.SXGate.label" />

### label

Return instruction label

<span id="qiskit.circuit.library.SXGate.name" />

### name

Return the name.

<span id="qiskit.circuit.library.SXGate.num_clbits" />

### num\_clbits

Return the number of clbits.

<span id="qiskit.circuit.library.SXGate.num_qubits" />

### num\_qubits

Return the number of qubits.

<span id="qiskit.circuit.library.SXGate.params" />

### params

return instruction params.

<span id="qiskit.circuit.library.SXGate.unit" />

### unit

Get the time unit of duration.

## Methods

### control

<span id="qiskit.circuit.library.SXGate.control" />

`control(num_ctrl_qubits=1, label=None, ctrl_state=None)`

Return a (multi-)controlled-SX gate.

One control returns a CSX gate.

**Parameters**

*   **num\_ctrl\_qubits** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")) – number of control qubits.
*   **label** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)") *or None*) – An optional label for the gate \[Default: None]
*   **ctrl\_state** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")  *or*[*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)") *or None*) – control state expressed as integer, string (e.g. ‘110’), or None. If None, use all 1s.

**Returns**

controlled version of this gate.

**Return type**

[ControlledGate](qiskit.circuit.ControlledGate "qiskit.circuit.ControlledGate")

### inverse

<span id="qiskit.circuit.library.SXGate.inverse" />

`inverse()`

Return inverse SX gate (i.e. SXdg).

