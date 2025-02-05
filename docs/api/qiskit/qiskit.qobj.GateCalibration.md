---
title: GateCalibration
description: API reference for qiskit.qobj.GateCalibration
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.qobj.GateCalibration
---

# GateCalibration

<span id="qiskit.qobj.GateCalibration" />

`qiskit.qobj.GateCalibration(name, qubits, params, instructions)`

Bases: [`object`](https://docs.python.org/3/library/functions.html#object "(in Python v3.11)")

Each calibration specifies a unique gate by name, qubits and params, and contains the Pulse instructions to implement it.

Initialize a single gate calibration. Instructions may reference waveforms which should be made available in the pulse\_library.

**Parameters**

*   **name** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)")) – Gate name.
*   **qubits** ([*list*](https://docs.python.org/3/library/stdtypes.html#list "(in Python v3.11)")*(*[*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")*)*) – Qubits the gate applies to.
*   **params** ([*list*](https://docs.python.org/3/library/stdtypes.html#list "(in Python v3.11)")*(*[*complex*](https://docs.python.org/3/library/functions.html#complex "(in Python v3.11)")*)*) – Gate parameter values, if any.
*   **instructions** ([*list*](https://docs.python.org/3/library/stdtypes.html#list "(in Python v3.11)")*(*[*PulseQobjInstruction*](qiskit.qobj.PulseQobjInstruction "qiskit.qobj.PulseQobjInstruction")*)*) – The gate implementation.

## Methods

### from\_dict

<span id="qiskit.qobj.GateCalibration.from_dict" />

`classmethod from_dict(data)`

Create a new GateCalibration object from a dictionary.

**Parameters**

**data** ([*dict*](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)")) – A dictionary representing the GateCalibration to create. It will be in the same format as output by [`to_dict()`](#qiskit.qobj.GateCalibration.to_dict "qiskit.qobj.GateCalibration.to_dict").

**Returns**

The GateCalibration from the input dictionary.

**Return type**

[GateCalibration](#qiskit.qobj.GateCalibration "qiskit.qobj.GateCalibration")

### to\_dict

<span id="qiskit.qobj.GateCalibration.to_dict" />

`to_dict()`

Return a dictionary format representation of the Gate Calibration.

**Returns**

The dictionary form of the GateCalibration.

**Return type**

[dict](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)")

