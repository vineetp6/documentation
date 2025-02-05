---
title: HighLevelSynthesisPlugin
description: API reference for qiskit.transpiler.passes.synthesis.plugin.HighLevelSynthesisPlugin
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.transpiler.passes.synthesis.plugin.HighLevelSynthesisPlugin
---

# HighLevelSynthesisPlugin

<span id="qiskit.transpiler.passes.synthesis.plugin.HighLevelSynthesisPlugin" />

`qiskit.transpiler.passes.synthesis.plugin.HighLevelSynthesisPlugin`

Bases: [`ABC`](https://docs.python.org/3/library/abc.html#abc.ABC "(in Python v3.11)")

Abstract high-level synthesis plugin class.

This abstract class defines the interface for high-level synthesis plugins.

## Methods

### run

<span id="qiskit.transpiler.passes.synthesis.plugin.HighLevelSynthesisPlugin.run" />

`abstract run(high_level_object, **options)`

Run synthesis for the given Operation.

**Parameters**

*   **high\_level\_object** ([*Operation*](qiskit.circuit.Operation "qiskit.circuit.Operation")) – The Operation to synthesize to a [`DAGCircuit`](qiskit.dagcircuit.DAGCircuit "qiskit.dagcircuit.DAGCircuit") object
*   **options** – The optional kwargs.

**Returns**

**The quantum circuit representation of the Operation**

when successful, and `None` otherwise.

**Return type**

[QuantumCircuit](qiskit.circuit.QuantumCircuit "qiskit.circuit.QuantumCircuit")

