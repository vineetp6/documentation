---
title: BaseEstimator
description: API reference for qiskit.primitives.BaseEstimator
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.primitives.BaseEstimator
---

# BaseEstimator

<span id="qiskit.primitives.BaseEstimator" />

`qiskit.primitives.BaseEstimator(*, options=None)`

Bases: `BasePrimitive`, [`Generic`](https://docs.python.org/3/library/typing.html#typing.Generic "(in Python v3.11)")\[`T`]

Estimator base class.

Base class for Estimator that estimates expectation values of quantum circuits and observables.

Creating an instance of an Estimator, or using one in a `with` context opens a session that holds resources until the instance is `close()` ed or the context is exited.

**Parameters**

**options** ([*dict*](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)") *| None*) – Default options.

## Attributes

<span id="qiskit.primitives.BaseEstimator.circuits" />

### circuits

Quantum circuits that represents quantum states.

**Returns**

The quantum circuits.

<span id="qiskit.primitives.BaseEstimator.observables" />

### observables

Observables to be estimated.

**Returns**

The observables.

<span id="qiskit.primitives.BaseEstimator.options" />

### options

Return options values for the estimator.

**Returns**

options

<span id="qiskit.primitives.BaseEstimator.parameters" />

### parameters

Parameters of the quantum circuits.

**Returns**

Parameters, where `parameters[i][j]` is the j-th parameter of the i-th circuit.

## Methods

### run

<span id="qiskit.primitives.BaseEstimator.run" />

`run(circuits, observables, parameter_values=None, **run_options)`

Run the job of the estimation of expectation value(s).

`circuits`, `observables`, and `parameter_values` should have the same length. The i-th element of the result is the expectation of observable

```python
obs = observables[i]
```

for the state prepared by

```python
circ = circuits[i]
```

with bound parameters

```python
values = parameter_values[i].
```

**Parameters**

*   **circuits** (*Sequence\[*[*QuantumCircuit*](qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")*] |* [*QuantumCircuit*](qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")) – one or more circuit objects.
*   **observables** (*Sequence\[BaseOperator |* [*PauliSumOp*](http://qiskit.org/documentation/stubs/qiskit.opflow.primitive_ops.PauliSumOp.html#qiskit.opflow.primitive_ops.PauliSumOp "qiskit.opflow.primitive_ops.PauliSumOp")  *|*[*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)")*] | BaseOperator |* [*PauliSumOp*](http://qiskit.org/documentation/stubs/qiskit.opflow.primitive_ops.PauliSumOp.html#qiskit.opflow.primitive_ops.PauliSumOp "qiskit.opflow.primitive_ops.PauliSumOp")  *|*[*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)")) – one or more observable objects. Several formats are allowed; importantly, `str` should follow the string representation format for [`Pauli`](qiskit.quantum_info.Pauli "qiskit.quantum_info.Pauli") objects.
*   **parameter\_values** (*Sequence\[Sequence\[*[*float*](https://docs.python.org/3/library/functions.html#float "(in Python v3.11)")*]] | Sequence\[*[*float*](https://docs.python.org/3/library/functions.html#float "(in Python v3.11)")*] |* [*float*](https://docs.python.org/3/library/functions.html#float "(in Python v3.11)") *| None*) – concrete parameters to be bound.
*   **run\_options** – runtime options used for circuit execution.

**Returns**

The job object of EstimatorResult.

**Raises**

*   [**TypeError**](https://docs.python.org/3/library/exceptions.html#TypeError "(in Python v3.11)") – Invalid argument type given.
*   [**ValueError**](https://docs.python.org/3/library/exceptions.html#ValueError "(in Python v3.11)") – Invalid argument values given.

**Return type**

T

### set\_options

<span id="qiskit.primitives.BaseEstimator.set_options" />

`set_options(**fields)`

Set options values for the estimator.

**Parameters**

**\*\*fields** – The fields to update the options

