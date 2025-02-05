---
title: BaseReadoutMitigator
description: API reference for qiskit.result.BaseReadoutMitigator
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.result.BaseReadoutMitigator
---

# BaseReadoutMitigator

<span id="qiskit.result.BaseReadoutMitigator" />

`qiskit.result.BaseReadoutMitigator`

Bases: [`ABC`](https://docs.python.org/3/library/abc.html#abc.ABC "(in Python v3.11)")

Base readout error mitigator class.

## Methods

### expectation\_value

<span id="qiskit.result.BaseReadoutMitigator.expectation_value" />

`abstract expectation_value(data, diagonal, qubits=None, clbits=None, shots=None)`

Calculate the expectation value of a diagonal Hermitian operator.

**Parameters**

*   **data** ([*Counts*](qiskit.result.Counts "qiskit.result.counts.Counts")) – Counts object to be mitigated.
*   **diagonal** ([*Callable*](https://docs.python.org/3/library/typing.html#typing.Callable "(in Python v3.11)")  *|*[*dict*](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)")  *|*[*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)")  *|*[*ndarray*](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.html#numpy.ndarray "(in NumPy v1.25)")) – the diagonal operator. This may either be specified as a string containing I,Z,0,1 characters, or as a real valued 1D array\_like object supplying the full diagonal, or as a dictionary, or as Callable.
*   **qubits** ([*Iterable*](https://docs.python.org/3/library/typing.html#typing.Iterable "(in Python v3.11)")*\[*[*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")*] | None*) – the physical qubits measured to obtain the counts clbits. If None these are assumed to be qubits \[0, …, N-1] for N-bit counts.
*   **clbits** ([*List*](https://docs.python.org/3/library/typing.html#typing.List "(in Python v3.11)")*\[*[*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")*] | None*) – Optional, marginalize counts to just these bits.
*   **shots** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)") *| None*) – Optional, the total number of shots, if None shots will be calculated as the sum of all counts.

**Returns**

The mean and an upper bound of the standard deviation of operator expectation value calculated from the current counts.

**Return type**

[*Tuple*](https://docs.python.org/3/library/typing.html#typing.Tuple "(in Python v3.11)")\[[float](https://docs.python.org/3/library/functions.html#float "(in Python v3.11)"), [float](https://docs.python.org/3/library/functions.html#float "(in Python v3.11)")]

### quasi\_probabilities

<span id="qiskit.result.BaseReadoutMitigator.quasi_probabilities" />

`abstract quasi_probabilities(data, qubits=None, clbits=None, shots=None)`

Convert counts to a dictionary of quasi-probabilities

**Parameters**

*   **data** ([*Counts*](qiskit.result.Counts "qiskit.result.counts.Counts")) – Counts to be mitigated.
*   **qubits** ([*Iterable*](https://docs.python.org/3/library/typing.html#typing.Iterable "(in Python v3.11)")*\[*[*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")*] | None*) – the physical qubits measured to obtain the counts clbits. If None these are assumed to be qubits \[0, …, N-1] for N-bit counts.
*   **clbits** ([*List*](https://docs.python.org/3/library/typing.html#typing.List "(in Python v3.11)")*\[*[*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")*] | None*) – Optional, marginalize counts to just these bits.
*   **shots** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)") *| None*) – Optional, the total number of shots, if None shots will be calculated as the sum of all counts.

**Returns**

**A dictionary containing pairs of \[output, mean] where “output”**

is the key in the dictionaries, which is the length-N bitstring of a measured standard basis state, and “mean” is the mean of non-zero quasi-probability estimates.

**Return type**

QuasiDistibution

