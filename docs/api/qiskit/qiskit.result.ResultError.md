---
title: ResultError
description: API reference for qiskit.result.ResultError
in_page_toc_min_heading_level: 1
python_api_type: exception
python_api_name: qiskit.result.ResultError
---

<span id="qiskit-result-resulterror" />

# qiskit.result.ResultError

<span id="qiskit.result.ResultError" />

`qiskit.result.ResultError(error)`

Exceptions raised due to errors in result output.

It may be better for the Qiskit API to raise this exception.

**Parameters**

**error** ([*dict*](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)")) –

This is the error record as it comes back from the API. The format is like:

```python
error = {'status': 403,
         'message': 'Your credits are not enough.',
         'code': 'MAX_CREDITS_EXCEEDED'}
```

Set the error message.

