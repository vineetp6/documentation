---
title: RuntimeOptions
description: API reference for qiskit_ibm_runtime.RuntimeOptions
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit_ibm_runtime.RuntimeOptions
---

# RuntimeOptions

<span id="qiskit_ibm_runtime.RuntimeOptions" />

`RuntimeOptions(backend=None, image=None, log_level=None, instance=None, job_tags=None, max_execution_time=None, session_time=None)`

Class for representing generic runtime execution options.

RuntimeOptions constructor.

**Parameters**

*   **backend** (`Optional`\[`str`]) – target backend to run on. This is required for `ibm_quantum` channel.
*   **image** (`Optional`\[`str`]) – the runtime image used to execute the program, specified in the form of `image_name:tag`. Not all accounts are authorized to select a different image.
*   **log\_level** (`Optional`\[`str`]) – logging level to set in the execution environment. The valid log levels are: `DEBUG`, `INFO`, `WARNING`, `ERROR`, and `CRITICAL`. The default level is `WARNING`.
*   **instance** (`Optional`\[`str`]) – The hub/group/project to use, in that format. This is only supported for `ibm_quantum` channel. If `None`, a hub/group/project that provides access to the target backend is randomly selected.
*   **job\_tags** (`Optional`\[`List`\[`str`]]) – Tags to be assigned to the job. The tags can subsequently be used as a filter in the `jobs()` function call.
*   **max\_execution\_time** (`Optional`\[`int`]) – Maximum execution time in seconds. If a job exceeds this time limit, it is forcibly cancelled.
*   **session\_time** (`Optional`\[`int`]) – Length of session in seconds.

## Attributes

<span id="runtimeoptions-backend" />

### backend

<span id="qiskit_ibm_runtime.RuntimeOptions.backend" />

`str | None = None`

<span id="runtimeoptions-image" />

### image

<span id="qiskit_ibm_runtime.RuntimeOptions.image" />

`str | None = None`

<span id="runtimeoptions-instance" />

### instance

<span id="qiskit_ibm_runtime.RuntimeOptions.instance" />

`str | None = None`

<span id="runtimeoptions-job-tags" />

### job\_tags

<span id="qiskit_ibm_runtime.RuntimeOptions.job_tags" />

`List[str] | None = None`

<span id="runtimeoptions-log-level" />

### log\_level

<span id="qiskit_ibm_runtime.RuntimeOptions.log_level" />

`str | None = None`

<span id="runtimeoptions-max-execution-time" />

### max\_execution\_time

<span id="qiskit_ibm_runtime.RuntimeOptions.max_execution_time" />

`int | None = None`

<span id="runtimeoptions-session-time" />

### session\_time

<span id="qiskit_ibm_runtime.RuntimeOptions.session_time" />

`int | None = None`

## Methods

<span id="runtimeoptions-validate" />

### validate

<span id="qiskit_ibm_runtime.RuntimeOptions.validate" />

`RuntimeOptions.validate(channel)`

Validate options.

**Parameters**

**channel** (`str`) – channel type.

**Raises**

**IBMInputValueError** – If one or more option is invalid.

**Return type**

`None`

