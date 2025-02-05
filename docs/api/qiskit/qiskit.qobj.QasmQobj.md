---
title: QasmQobj
description: API reference for qiskit.qobj.QasmQobj
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.qobj.QasmQobj
---

# QasmQobj

<span id="qiskit.qobj.QasmQobj" />

`qiskit.qobj.QasmQobj(qobj_id=None, config=None, experiments=None, header=None)`

Bases: [`object`](https://docs.python.org/3/library/functions.html#object "(in Python v3.11)")

A QASM Qobj.

Instantiate a new QASM Qobj Object.

Each QASM Qobj object is used to represent a single payload that will be passed to a Qiskit provider. It mirrors the Qobj the published [Qobj specification](https://arxiv.org/abs/1809.03452) for OpenQASM experiments.

**Parameters**

*   **qobj\_id** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)")) – An identifier for the qobj
*   **config** (*QasmQobjRunConfig*) – A config for the entire run
*   **header** ([*QobjHeader*](qiskit.qobj.QobjHeader "qiskit.qobj.QobjHeader")) – A header for the entire run
*   **experiments** ([*list*](https://docs.python.org/3/library/stdtypes.html#list "(in Python v3.11)")) – A list of lists of [`QasmQobjExperiment`](qiskit.qobj.QasmQobjExperiment "qiskit.qobj.QasmQobjExperiment") objects representing an experiment

## Methods

### from\_dict

<span id="qiskit.qobj.QasmQobj.from_dict" />

`classmethod from_dict(data)`

Create a new QASMQobj object from a dictionary.

**Parameters**

**data** ([*dict*](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)")) – A dictionary representing the QasmQobj to create. It will be in the same format as output by [`to_dict()`](#qiskit.qobj.QasmQobj.to_dict "qiskit.qobj.QasmQobj.to_dict").

**Returns**

The QasmQobj from the input dictionary.

**Return type**

[QasmQobj](#qiskit.qobj.QasmQobj "qiskit.qobj.QasmQobj")

### to\_dict

<span id="qiskit.qobj.QasmQobj.to_dict" />

`to_dict()`

Return a dictionary format representation of the QASM Qobj.

Note this dict is not in the json wire format expected by IBMQ and qobj specification because complex numbers are still of type complex. Also this may contain native numpy arrays. When serializing this output for use with IBMQ you can leverage a json encoder that converts these as expected. For example:

```python
import json
import numpy

class QobjEncoder(json.JSONEncoder):
    def default(self, obj):
        if isinstance(obj, numpy.ndarray):
            return obj.tolist()
        if isinstance(obj, complex):
            return (obj.real, obj.imag)
        return json.JSONEncoder.default(self, obj)

json.dumps(qobj.to_dict(), cls=QobjEncoder)
```

**Returns**

A dictionary representation of the QasmQobj object

**Return type**

[dict](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)")

