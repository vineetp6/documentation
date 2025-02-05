---
title: QasmExperimentCalibrations
description: API reference for qiskit.qobj.QasmExperimentCalibrations
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.qobj.QasmExperimentCalibrations
---

# QasmExperimentCalibrations

<span id="qiskit.qobj.QasmExperimentCalibrations" />

`qiskit.qobj.QasmExperimentCalibrations(gates)`

Bases: [`object`](https://docs.python.org/3/library/functions.html#object "(in Python v3.11)")

A container for any calibrations data. The gates attribute contains a list of GateCalibrations.

Initialize a container for calibrations.

**Parameters**

**gates** ([*list*](https://docs.python.org/3/library/stdtypes.html#list "(in Python v3.11)")*(*[*GateCalibration*](qiskit.qobj.GateCalibration "qiskit.qobj.GateCalibration")*)*) –

## Methods

### from\_dict

<span id="qiskit.qobj.QasmExperimentCalibrations.from_dict" />

`classmethod from_dict(data)`

Create a new GateCalibration object from a dictionary.

**Parameters**

**data** ([*dict*](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)")) – A dictionary representing the QasmExperimentCalibrations to create. It will be in the same format as output by [`to_dict()`](#qiskit.qobj.QasmExperimentCalibrations.to_dict "qiskit.qobj.QasmExperimentCalibrations.to_dict").

**Returns**

The QasmExperimentCalibrations from the input dictionary.

**Return type**

[QasmExperimentCalibrations](#qiskit.qobj.QasmExperimentCalibrations "qiskit.qobj.QasmExperimentCalibrations")

### to\_dict

<span id="qiskit.qobj.QasmExperimentCalibrations.to_dict" />

`to_dict()`

Return a dictionary format representation of the calibrations.

**Returns**

The dictionary form of the GateCalibration.

**Return type**

[dict](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)")

