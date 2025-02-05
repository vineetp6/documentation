---
title: IBMBackend
description: API reference for qiskit_ibm_runtime.IBMBackend
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit_ibm_runtime.IBMBackend
---

# IBMBackend

<span id="qiskit_ibm_runtime.IBMBackend" />

`IBMBackend(configuration, service, api_client, instance=None)`

Backend class interfacing with an IBM Quantum backend.

<Admonition title="Note" type="note">
  *   You should not instantiate the `IBMBackend` class directly. Instead, use the methods provided by an [`QiskitRuntimeService`](qiskit_ibm_runtime.QiskitRuntimeService "qiskit_ibm_runtime.QiskitRuntimeService") instance to retrieve and handle backends.
</Admonition>

This class represents an IBM Quantum backend. Its attributes and methods provide information about the backend. For example, the [`status()`](qiskit_ibm_runtime.IBMBackend#status "qiskit_ibm_runtime.IBMBackend.status") method returns a `BackendStatus` instance. The instance contains the `operational` and `pending_jobs` attributes, which state whether the backend is operational and also the number of jobs in the server queue for the backend, respectively:

```python
status = backend.status()
is_operational = status.operational
jobs_in_queue = status.pending_jobs
```

Here is list of attributes available on the `IBMBackend` class:

> *   name: backend name.
>
> *   backend\_version: backend version in the form X.Y.Z.
>
> *   num\_qubits: number of qubits.
>
> *   target: A `qiskit.transpiler.Target` object for the backend.
>
> *   basis\_gates: list of basis gates names on the backend.
>
> *   gates: list of basis gates on the backend.
>
> *   local: backend is local or remote.
>
> *   simulator: backend is a simulator.
>
> *   conditional: backend supports conditional operations.
>
> *   open\_pulse: backend supports open pulse.
>
> *   memory: backend supports memory.
>
> *   max\_shots: maximum number of shots supported.
>
> *   coupling\_map (list): The coupling map for the device
>
> *   supported\_instructions (List\[str]): Instructions supported by the backend.
>
> *   dynamic\_reprate\_enabled (bool): whether delay between programs can be set dynamically (ie via `rep_delay`). Defaults to False.
>
> *   rep\_delay\_range (List\[float]): 2d list defining supported range of repetition delays for backend in μs. First entry is lower end of the range, second entry is higher end of the range. Optional, but will be specified when `dynamic_reprate_enabled=True`.
>
> *   default\_rep\_delay (float): Value of `rep_delay` if not specified by user and `dynamic_reprate_enabled=True`.
>
> *   n\_uchannels: Number of u-channels.
>
> *   u\_channel\_lo: U-channel relationship on device los.
>
> *   meas\_levels: Supported measurement levels.
>
> *   qubit\_lo\_range: Qubit lo ranges for each qubit with form (min, max) in GHz.
>
> *   meas\_lo\_range: Measurement lo ranges for each qubit with form (min, max) in GHz.
>
> *   dt: Qubit drive channel timestep in nanoseconds.
>
> *   dtm: Measurement drive channel timestep in nanoseconds.
>
> *   rep\_times: Supported repetition times (program execution time) for backend in μs.
>
> *   meas\_kernels: Supported measurement kernels.
>
> *   discriminators: Supported discriminators.
>
> *   hamiltonian: An optional dictionary with fields characterizing the system hamiltonian.
>
> *   channel\_bandwidth (list): Bandwidth of all channels (qubit, measurement, and U)
>
> *   acquisition\_latency (list): Array of dimension n\_qubits x n\_registers. Latency (in units of dt) to write a measurement result from qubit n into register slot m.
>
> *   conditional\_latency (list): Array of dimension n\_channels \[d->u->m] x n\_registers. Latency (in units of dt) to do a conditional operation on channel n from register slot m
>
> *   meas\_map (list): Grouping of measurement which are multiplexed
>
> *   max\_circuits (int): The maximum number of experiments per job
>
> *   sample\_name (str): Sample name for the backend
>
> *   n\_registers (int): Number of register slots available for feedback (if conditional is True)
>
> *   register\_map (list): An array of dimension n\_qubits X n\_registers that specifies whether a qubit can store a measurement in a certain register slot.
>
> *   configurable (bool): True if the backend is configurable, if the backend is a simulator
>
> *   credits\_required (bool): True if backend requires credits to run a job.
>
> *   online\_date (datetime): The date that the device went online
>
> *   display\_name (str): Alternate name field for the backend
>
> *   description (str): A description for the backend
>
> *   tags (list): A list of string tags to describe the backend
>
> *   version: version of `Backend` class (Ex: 1, 2)
>
> *   channels: An optional dictionary containing information of each channel – their purpose, type, and qubits operated on.
>
> *   parametric\_pulses (list): A list of pulse shapes which are supported on the backend. For example: `['gaussian', 'constant']`
>
> *   processor\_type (dict): Processor type for this backend. A dictionary of the form `{"family": <str>, "revision": <str>, segment: <str>}` such as `{"family": "Canary", "revision": "1.0", segment: "A"}`.
>
>     > *   family: Processor family of this backend.
>     > *   revision: Revision version of this processor.
>     > *   segment: Segment this processor belongs to within a larger chip.

IBMBackend constructor.

**Parameters**

*   **configuration** (`Union`\[`QasmBackendConfiguration`, `PulseBackendConfiguration`]) – Backend configuration.
*   **service** ([`QiskitRuntimeService`](qiskit_ibm_runtime.QiskitRuntimeService "qiskit_ibm_runtime.qiskit_runtime_service.QiskitRuntimeService")) – Instance of QiskitRuntimeService.
*   **api\_client** (`BaseBackendClient`) – IBM client used to communicate with the server.

## Attributes

<span id="ibmbackend-coupling-map" />

### coupling\_map

Return the `CouplingMap` object

<span id="ibmbackend-dt" />

### dt

<span id="qiskit_ibm_runtime.IBMBackend.dt" />

`float | None`

Return the system time resolution of input signals

This is required to be implemented if the backend supports Pulse scheduling.

**Returns**

The input signal timestep in seconds. If the backend doesn’t define `dt` `None` will be returned

**Return type**

dt

<span id="ibmbackend-dtm" />

### dtm

<span id="qiskit_ibm_runtime.IBMBackend.dtm" />

`float`

Return the system time resolution of output signals

**Returns**

The output signal timestep in seconds.

**Return type**

dtm

<span id="ibmbackend-id-warning-issued" />

### id\_warning\_issued

<span id="qiskit_ibm_runtime.IBMBackend.id_warning_issued" />

`= False`

<span id="ibmbackend-instruction-durations" />

### instruction\_durations

Return the `InstructionDurations` object.

<span id="ibmbackend-instruction-schedule-map" />

### instruction\_schedule\_map

Return the `InstructionScheduleMap` for the instructions defined in this backend’s target.

<span id="ibmbackend-instructions" />

### instructions

<span id="qiskit_ibm_runtime.IBMBackend.instructions" />

`List[Tuple[Instruction, Tuple[int]]]`

A list of Instruction tuples on the backend of the form `(instruction, (qubits)`

**Return type**

`List`\[`Tuple`\[`Instruction`, `Tuple`\[`int`]]]

<span id="ibmbackend-max-circuits" />

### max\_circuits

<span id="qiskit_ibm_runtime.IBMBackend.max_circuits" />

`int`

The maximum number of circuits

The maximum number of circuits (or Pulse schedules) that can be run in a single job. If there is no limit this will return None.

**Return type**

`int`

<span id="ibmbackend-meas-map" />

### meas\_map

<span id="qiskit_ibm_runtime.IBMBackend.meas_map" />

`List[List[int]]`

Return the grouping of measurements which are multiplexed

This is required to be implemented if the backend supports Pulse scheduling.

**Returns**

The grouping of measurements which are multiplexed

**Return type**

meas\_map

<span id="ibmbackend-num-qubits" />

### num\_qubits

<span id="qiskit_ibm_runtime.IBMBackend.num_qubits" />

`int`

Return the number of qubits the backend has.

**Return type**

`int`

<span id="ibmbackend-operation-names" />

### operation\_names

<span id="qiskit_ibm_runtime.IBMBackend.operation_names" />

`List[str]`

A list of instruction names that the backend supports.

**Return type**

`List`\[`str`]

<span id="ibmbackend-operations" />

### operations

<span id="qiskit_ibm_runtime.IBMBackend.operations" />

`List[Instruction]`

A list of `Instruction` instances that the backend supports.

**Return type**

`List`\[`Instruction`]

<span id="ibmbackend-options" />

### options

Return the options for the backend

The options of a backend are the dynamic parameters defining how the backend is used. These are used to control the [`run()`](qiskit_ibm_runtime.IBMBackend#run "qiskit_ibm_runtime.IBMBackend.run") method.

<span id="ibmbackend-provider" />

### provider

Return the backend Provider.

**Returns**

the Provider responsible for the backend.

**Return type**

Provider

<span id="ibmbackend-service" />

### service

<span id="qiskit_ibm_runtime.IBMBackend.service" />

`QiskitRuntimeService`

Return the `service` object

**Returns**

instance of QiskitRuntimeService

**Return type**

service

<span id="ibmbackend-target" />

### target

<span id="qiskit_ibm_runtime.IBMBackend.target" />

`Target`

A `qiskit.transpiler.Target` object for the backend.

**Return type**

`Target`

**Returns**

Target

<span id="ibmbackend-version" />

### version

<span id="qiskit_ibm_runtime.IBMBackend.version" />

`= 2`

## Methods

<span id="ibmbackend-call" />

### \_\_call\_\_

<span id="qiskit_ibm_runtime.IBMBackend.__call__" />

`IBMBackend.__call__()`

Call self as a function.

**Return type**

[`IBMBackend`](qiskit_ibm_runtime.IBMBackend "qiskit_ibm_runtime.ibm_backend.IBMBackend")

<span id="ibmbackend-acquire-channel" />

### acquire\_channel

<span id="qiskit_ibm_runtime.IBMBackend.acquire_channel" />

`IBMBackend.acquire_channel(qubit)`

Return the acquisition channel for the given qubit.

**Returns**

The Qubit measurement acquisition line.

**Return type**

AcquireChannel

<span id="ibmbackend-check-faulty" />

### check\_faulty

<span id="qiskit_ibm_runtime.IBMBackend.check_faulty" />

`IBMBackend.check_faulty(circuit)`

Check if the input circuit uses faulty qubits or edges.

**Parameters**

**circuit** (`QuantumCircuit`) – Circuit to check.

**Raises**

**ValueError** – If an instruction operating on a faulty qubit or edge is found.

**Return type**

`None`

<span id="ibmbackend-configuration" />

### configuration

<span id="qiskit_ibm_runtime.IBMBackend.configuration" />

`IBMBackend.configuration()`

Return the backend configuration.

Backend configuration contains fixed information about the backend, such as its name, number of qubits, basis gates, coupling map, quantum volume, etc.

The schema for backend configuration can be found in [Qiskit/ibm-quantum-schemas](https://github.com/Qiskit/ibm-quantum-schemas/blob/main/schemas/backend_configuration_schema.json).

**Return type**

`Union`\[`QasmBackendConfiguration`, `PulseBackendConfiguration`]

**Returns**

The configuration for the backend.

<span id="ibmbackend-control-channel" />

### control\_channel

<span id="qiskit_ibm_runtime.IBMBackend.control_channel" />

`IBMBackend.control_channel(qubits)`

Return the secondary drive channel for the given qubit

This is typically utilized for controlling multiqubit interactions. This channel is derived from other channels.

**Parameters**

**qubits** (`Iterable`\[`int`]) – Tuple or list of qubits of the form `(control_qubit, target_qubit)`.

**Returns**

The Qubit measurement acquisition line.

**Return type**

List\[ControlChannel]

<span id="ibmbackend-defaults" />

### defaults

<span id="qiskit_ibm_runtime.IBMBackend.defaults" />

`IBMBackend.defaults(refresh=False)`

Return the pulse defaults for the backend.

The schema for default pulse configuration can be found in [Qiskit/ibm-quantum-schemas](https://github.com/Qiskit/ibm-quantum-schemas/blob/main/schemas/default_pulse_configuration_schema.json).

**Parameters**

**refresh** (`bool`) – If `True`, re-query the server for the backend pulse defaults. Otherwise, return a cached version.

**Return type**

`Optional`\[`PulseDefaults`]

**Returns**

The backend pulse defaults or `None` if the backend does not support pulse.

<span id="ibmbackend-drive-channel" />

### drive\_channel

<span id="qiskit_ibm_runtime.IBMBackend.drive_channel" />

`IBMBackend.drive_channel(qubit)`

Return the drive channel for the given qubit.

**Returns**

The Qubit drive channel

**Return type**

DriveChannel

<span id="ibmbackend-measure-channel" />

### measure\_channel

<span id="qiskit_ibm_runtime.IBMBackend.measure_channel" />

`IBMBackend.measure_channel(qubit)`

Return the measure stimulus channel for the given qubit.

**Returns**

The Qubit measurement stimulus line

**Return type**

MeasureChannel

<span id="ibmbackend-properties" />

### properties

<span id="qiskit_ibm_runtime.IBMBackend.properties" />

`IBMBackend.properties(refresh=False, datetime=None)`

Return the backend properties, subject to optional filtering.

This data describes qubits properties (such as T1 and T2), gates properties (such as gate length and error), and other general properties of the backend.

The schema for backend properties can be found in [Qiskit/ibm-quantum-schemas](https://github.com/Qiskit/ibm-quantum-schemas/blob/main/schemas/backend_properties_schema.json).

**Parameters**

*   **refresh** (`bool`) – If `True`, re-query the server for the backend properties. Otherwise, return a cached version.
*   **datetime** (`Optional`\[`datetime`]) – By specifying datetime, this function returns an instance of the `BackendProperties` whose timestamp is closest to, but older than, the specified datetime. Note that this is only supported using `ibm_quantum` runtime.

**Return type**

`Optional`\[`BackendProperties`]

**Returns**

The backend properties or `None` if the backend properties are not currently available.

**Raises**

*   **TypeError** – If an input argument is not of the correct type.
*   **NotImplementedError** – If datetime is specified when cloud rutime is used.

<span id="ibmbackend-qubit-properties" />

### qubit\_properties

<span id="qiskit_ibm_runtime.IBMBackend.qubit_properties" />

`IBMBackend.qubit_properties(qubit)`

Return QubitProperties for a given qubit.

If there are no defined or the backend doesn’t support querying these details this method does not need to be implemented.

**Parameters**

**qubit** (`Union`\[`int`, `List`\[`int`]]) – The qubit to get the `QubitProperties` object for. This can be a single integer for 1 qubit or a list of qubits and a list of `QubitProperties` objects will be returned in the same order

**Returns**

The `QubitProperties` object for the specified qubit. If a list of qubits is provided a list will be returned. If properties are missing for a qubit this can be `None`.

**Return type**

qubit\_properties

**Raises**

**NotImplementedError** – if the backend doesn’t support querying the qubit properties

<span id="ibmbackend-run" />

### run

<span id="qiskit_ibm_runtime.IBMBackend.run" />

`IBMBackend.run(*args, **kwargs)`

Not supported method

**Return type**

`None`

<span id="ibmbackend-set-options" />

### set\_options

<span id="qiskit_ibm_runtime.IBMBackend.set_options" />

`IBMBackend.set_options(**fields)`

Set the options fields for the backend

This method is used to update the options of a backend. If you need to change any of the options prior to running just pass in the kwarg with the new value for the options.

**Parameters**

**fields** – The fields to update the options

**Raises**

**AttributeError** – If the field passed in is not part of the options

<span id="ibmbackend-status" />

### status

<span id="qiskit_ibm_runtime.IBMBackend.status" />

`IBMBackend.status()`

Return the backend status.

<Admonition title="Note" type="note">
  If the returned `BackendStatus` instance has `operational=True` but `status_msg="internal"`, then the backend is accepting jobs but not processing them.
</Admonition>

**Return type**

`BackendStatus`

**Returns**

The status of the backend.

**Raises**

**IBMBackendApiProtocolError** – If the status for the backend cannot be formatted properly.

<span id="ibmbackend-target-history" />

### target\_history

<span id="qiskit_ibm_runtime.IBMBackend.target_history" />

`IBMBackend.target_history(datetime=None)`

A `qiskit.transpiler.Target` object for the backend. :rtype: `Target` :returns: Target with properties found on datetime

