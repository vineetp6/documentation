---
title: CRZGate
description: API reference for qiskit.circuit.library.CRZGate
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.circuit.library.CRZGate
---

# CRZGate

<span id="qiskit.circuit.library.CRZGate" />

`qiskit.circuit.library.CRZGate(theta, label=None, ctrl_state=None)`

Bases: [`ControlledGate`](qiskit.circuit.ControlledGate "qiskit.circuit.controlledgate.ControlledGate")

Controlled-RZ gate.

This is a diagonal but non-symmetric gate that induces a phase on the state of the target qubit, depending on the control state.

Can be applied to a [`QuantumCircuit`](qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit") with the [`crz()`](qiskit.circuit.QuantumCircuit#crz "qiskit.circuit.QuantumCircuit.crz") method.

**Circuit symbol:**

```python
q_0: ────■────
     ┌───┴───┐
q_1: ┤ Rz(λ) ├
     └───────┘
```

**Matrix representation:**

$$
\begin{split}CRZ(\lambda)\ q_0, q_1 =
    I \otimes |0\rangle\langle 0| + RZ(\lambda) \otimes |1\rangle\langle 1| =
    \begin{pmatrix}
        1 & 0 & 0 & 0 \\
        0 & e^{-i\frac{\lambda}{2}} & 0 & 0 \\
        0 & 0 & 1 & 0 \\
        0 & 0 & 0 & e^{i\frac{\lambda}{2}}
    \end{pmatrix}\end{split}
$$

<Admonition title="Note" type="note">
  In Qiskit’s convention, higher qubit indices are more significant (little endian convention). In many textbooks, controlled gates are presented with the assumption of more significant qubits as control, which in our case would be q\_1. Thus a textbook matrix for this gate will be:

  ```python
       ┌───────┐
  q_0: ┤ Rz(λ) ├
       └───┬───┘
  q_1: ────■────
  ```

  $$
  \begin{split}CRZ(\lambda)\ q_1, q_0 =
      |0\rangle\langle 0| \otimes I + |1\rangle\langle 1| \otimes RZ(\lambda) =
      \begin{pmatrix}
          1 & 0 & 0 & 0 \\
          0 & 1 & 0 & 0 \\
          0 & 0 & e^{-i\frac{\lambda}{2}} & 0 \\
          0 & 0 & 0 & e^{i\frac{\lambda}{2}}
      \end{pmatrix}\end{split}
  $$
</Admonition>

<Admonition title="See also" type="note">
  `CU1Gate`: Due to the global phase difference in the matrix definitions of U1 and RZ, CU1 and CRZ are different gates with a relative phase difference.
</Admonition>

Create new CRZ gate.

## Attributes

<span id="qiskit.circuit.library.CRZGate.condition_bits" />

### condition\_bits

Get Clbits in condition.

<span id="qiskit.circuit.library.CRZGate.ctrl_state" />

### ctrl\_state

Return the control state of the gate as a decimal integer.

<span id="qiskit.circuit.library.CRZGate.decompositions" />

### decompositions

Get the decompositions of the instruction from the SessionEquivalenceLibrary.

<span id="qiskit.circuit.library.CRZGate.definition" />

### definition

Return definition in terms of other basic gates. If the gate has open controls, as determined from self.ctrl\_state, the returned definition is conjugated with X without changing the internal \_definition.

<span id="qiskit.circuit.library.CRZGate.duration" />

### duration

Get the duration.

<span id="qiskit.circuit.library.CRZGate.label" />

### label

Return instruction label

<span id="qiskit.circuit.library.CRZGate.name" />

### name

Get name of gate. If the gate has open controls the gate name will become:

> \<original\_name\_o\<ctrl\_state>

where \<original\_name> is the gate name for the default case of closed control qubits and \<ctrl\_state> is the integer value of the control state for the gate.

<span id="qiskit.circuit.library.CRZGate.num_clbits" />

### num\_clbits

Return the number of clbits.

<span id="qiskit.circuit.library.CRZGate.num_ctrl_qubits" />

### num\_ctrl\_qubits

Get number of control qubits.

**Returns**

The number of control qubits for the gate.

**Return type**

[int](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")

<span id="qiskit.circuit.library.CRZGate.num_qubits" />

### num\_qubits

Return the number of qubits.

<span id="qiskit.circuit.library.CRZGate.params" />

### params

Get parameters from base\_gate.

**Returns**

List of gate parameters.

**Return type**

[list](https://docs.python.org/3/library/stdtypes.html#list "(in Python v3.11)")

**Raises**

[**CircuitError**](circuit#qiskit.circuit.CircuitError "qiskit.circuit.CircuitError") – Controlled gate does not define a base gate

<span id="qiskit.circuit.library.CRZGate.unit" />

### unit

Get the time unit of duration.

## Methods

### inverse

<span id="qiskit.circuit.library.CRZGate.inverse" />

`inverse()`

Return inverse CRZ gate (i.e. with the negative rotation angle).

