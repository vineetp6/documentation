---
title: Layout2qDistance
description: API reference for qiskit.transpiler.passes.Layout2qDistance
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.transpiler.passes.Layout2qDistance
---

# Layout2qDistance

<span id="qiskit.transpiler.passes.Layout2qDistance" />

`qiskit.transpiler.passes.Layout2qDistance(*args, **kwargs)`

Bases: [`AnalysisPass`](qiskit.transpiler.AnalysisPass "qiskit.transpiler.basepasses.AnalysisPass")

Evaluate how good the layout selection was.

Saves in property\_set\[‘layout\_score’] (or the property name in property\_name) the sum of distances for each circuit CX. The lower the number, the better the selection. Therefore, 0 is a perfect layout selection. No CX direction is considered.

Layout2qDistance initializer.

**Parameters**

*   **coupling\_map** (*Union\[*[*CouplingMap*](qiskit.transpiler.CouplingMap "qiskit.transpiler.CouplingMap")*,* [*Target*](qiskit.transpiler.Target "qiskit.transpiler.Target")*]*) – Directed graph represented a coupling map.
*   **property\_name** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)")) – The property name to save the score. Default: layout\_score

## Attributes

<span id="qiskit.transpiler.passes.Layout2qDistance.is_analysis_pass" />

### is\_analysis\_pass

Check if the pass is an analysis pass.

If the pass is an AnalysisPass, that means that the pass can analyze the DAG and write the results of that analysis in the property set. Modifications on the DAG are not allowed by this kind of pass.

<span id="qiskit.transpiler.passes.Layout2qDistance.is_transformation_pass" />

### is\_transformation\_pass

Check if the pass is a transformation pass.

If the pass is a TransformationPass, that means that the pass can manipulate the DAG, but cannot modify the property set (but it can be read).

## Methods

### name

<span id="qiskit.transpiler.passes.Layout2qDistance.name" />

`name()`

Return the name of the pass.

### run

<span id="qiskit.transpiler.passes.Layout2qDistance.run" />

`run(dag)`

Run the Layout2qDistance pass on dag. :param dag: DAG to evaluate. :type dag: DAGCircuit

