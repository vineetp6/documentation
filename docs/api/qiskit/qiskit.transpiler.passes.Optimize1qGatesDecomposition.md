---
title: Optimize1qGatesDecomposition
description: API reference for qiskit.transpiler.passes.Optimize1qGatesDecomposition
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.transpiler.passes.Optimize1qGatesDecomposition
---

# Optimize1qGatesDecomposition

<span id="qiskit.transpiler.passes.Optimize1qGatesDecomposition" />

`qiskit.transpiler.passes.Optimize1qGatesDecomposition(*args, **kwargs)`

Bases: [`TransformationPass`](qiskit.transpiler.TransformationPass "qiskit.transpiler.basepasses.TransformationPass")

Optimize chains of single-qubit gates by combining them into a single gate.

**The decision to replace the original chain with a new resynthesis depends on:**

*   whether the original chain was out of basis: replace
*   whether the original chain was in basis but resynthesis is lower error: replace
*   whether the original chain contains a pulse gate: do not replace
*   whether the original chain amounts to identity: replace with null

Error is computed as a multiplication of the errors of individual gates on that qubit.

Optimize1qGatesDecomposition initializer.

**Parameters**

*   **basis** ([*list*](https://docs.python.org/3/library/stdtypes.html#list "(in Python v3.11)")*\[*[*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)")*]*) – Basis gates to consider, e.g. \[‘u3’, ‘cx’]. For the effects of this pass, the basis is the set intersection between the basis parameter and the Euler basis. Ignored if `target` is also specified.
*   **target** (*Optional\[*[*Target*](qiskit.transpiler.Target "qiskit.transpiler.Target")*]*) – The [`Target`](qiskit.transpiler.Target "qiskit.transpiler.Target") object corresponding to the compilation target. When specified, any argument specified for `basis_gates` is ignored.

## Attributes

<span id="qiskit.transpiler.passes.Optimize1qGatesDecomposition.is_analysis_pass" />

### is\_analysis\_pass

Check if the pass is an analysis pass.

If the pass is an AnalysisPass, that means that the pass can analyze the DAG and write the results of that analysis in the property set. Modifications on the DAG are not allowed by this kind of pass.

<span id="qiskit.transpiler.passes.Optimize1qGatesDecomposition.is_transformation_pass" />

### is\_transformation\_pass

Check if the pass is a transformation pass.

If the pass is a TransformationPass, that means that the pass can manipulate the DAG, but cannot modify the property set (but it can be read).

## Methods

### name

<span id="qiskit.transpiler.passes.Optimize1qGatesDecomposition.name" />

`name()`

Return the name of the pass.

### run

<span id="qiskit.transpiler.passes.Optimize1qGatesDecomposition.run" />

`run(dag)`

Run the Optimize1qGatesDecomposition pass on dag.

**Parameters**

**dag** ([*DAGCircuit*](qiskit.dagcircuit.DAGCircuit "qiskit.dagcircuit.DAGCircuit")) – the DAG to be optimized.

**Returns**

the optimized DAG.

**Return type**

[DAGCircuit](qiskit.dagcircuit.DAGCircuit "qiskit.dagcircuit.DAGCircuit")

