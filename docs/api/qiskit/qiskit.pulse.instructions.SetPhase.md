---
title: SetPhase
description: API reference for qiskit.pulse.instructions.SetPhase
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.pulse.instructions.SetPhase
---

# SetPhase

<span id="qiskit.pulse.instructions.SetPhase" />

`qiskit.pulse.instructions.SetPhase(phase, channel, name=None)`

Bases: [`Instruction`](pulse#qiskit.pulse.instructions.Instruction "qiskit.pulse.instructions.instruction.Instruction")

The set phase instruction sets the phase of the proceeding pulses on that channel to `phase` radians.

In particular, a PulseChannel creates pulses of the form

$$
Re[\exp(i 2\pi f jdt + \phi) d_j]
$$

The `SetPhase` instruction sets $\phi$ to the instruction’s `phase` operand.

Instantiate a set phase instruction, setting the output signal phase on `channel` to `phase` \[radians].

**Parameters**

*   **phase** ([*complex*](https://docs.python.org/3/library/functions.html#complex "(in Python v3.11)")  *|*[*ParameterExpression*](qiskit.circuit.ParameterExpression "qiskit.circuit.parameterexpression.ParameterExpression")) – The rotation angle in radians.
*   **channel** (*PulseChannel*) – The channel this instruction operates on.
*   **name** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)") *| None*) – Display name for this instruction.

## Attributes

<span id="qiskit.pulse.instructions.SetPhase.channel" />

### channel

Return the [`Channel`](pulse#qiskit.pulse.channels.Channel "qiskit.pulse.channels.Channel") that this instruction is scheduled on.

<span id="qiskit.pulse.instructions.SetPhase.channels" />

### channels

Returns the channels that this schedule uses.

<span id="qiskit.pulse.instructions.SetPhase.duration" />

### duration

Duration of this instruction.

<span id="qiskit.pulse.instructions.SetPhase.id" />

### id

Unique identifier for this instruction.

<span id="qiskit.pulse.instructions.SetPhase.instructions" />

### instructions

Iterable for getting instructions from Schedule tree.

<span id="qiskit.pulse.instructions.SetPhase.name" />

### name

Name of this instruction.

<span id="qiskit.pulse.instructions.SetPhase.operands" />

### operands

Return instruction operands.

<span id="qiskit.pulse.instructions.SetPhase.parameters" />

### parameters

Parameters which determine the instruction behavior.

<span id="qiskit.pulse.instructions.SetPhase.phase" />

### phase

Return the rotation angle enacted by this instruction in radians.

<span id="qiskit.pulse.instructions.SetPhase.start_time" />

### start\_time

Relative begin time of this instruction.

<span id="qiskit.pulse.instructions.SetPhase.stop_time" />

### stop\_time

Relative end time of this instruction.

## Methods

### append

<span id="qiskit.pulse.instructions.SetPhase.append" />

`append(schedule, name=None)`

Return a new [`Schedule`](qiskit.pulse.Schedule "qiskit.pulse.Schedule") with `schedule` inserted at the maximum time over all channels shared between `self` and `schedule`.

**Parameters**

*   **schedule** (*Union\['Schedule', 'Instruction']*) – Schedule or instruction to be appended
*   **name** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)") *| None*) – Name of the new schedule. Defaults to name of self

**Returns**

A new schedule with `schedule` a this instruction at t=0.

**Return type**

[Schedule](qiskit.pulse.Schedule "qiskit.pulse.Schedule")

### ch\_duration

<span id="qiskit.pulse.instructions.SetPhase.ch_duration" />

`ch_duration(*channels)`

Return duration of the supplied channels in this Instruction.

**Parameters**

**\*channels** ([*List*](https://docs.python.org/3/library/typing.html#typing.List "(in Python v3.11)")*\[*[*Channel*](pulse#qiskit.pulse.channels.Channel "qiskit.pulse.channels.Channel")*]*) – Supplied channels

**Return type**

[int](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")

### ch\_start\_time

<span id="qiskit.pulse.instructions.SetPhase.ch_start_time" />

`ch_start_time(*channels)`

Return minimum start time for supplied channels.

**Parameters**

**\*channels** ([*List*](https://docs.python.org/3/library/typing.html#typing.List "(in Python v3.11)")*\[*[*Channel*](pulse#qiskit.pulse.channels.Channel "qiskit.pulse.channels.Channel")*]*) – Supplied channels

**Return type**

[int](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")

### ch\_stop\_time

<span id="qiskit.pulse.instructions.SetPhase.ch_stop_time" />

`ch_stop_time(*channels)`

Return maximum start time for supplied channels.

**Parameters**

**\*channels** ([*List*](https://docs.python.org/3/library/typing.html#typing.List "(in Python v3.11)")*\[*[*Channel*](pulse#qiskit.pulse.channels.Channel "qiskit.pulse.channels.Channel")*]*) – Supplied channels

**Return type**

[int](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")

### draw

<span id="qiskit.pulse.instructions.SetPhase.draw" />

`draw(dt=1, style=None, filename=None, interp_method=None, scale=1, plot_all=False, plot_range=None, interactive=False, table=True, label=False, framechange=True, channels=None)`

Plot the instruction.

<Admonition title="Deprecated since version 0.23.0" type="danger">
  The method `qiskit.pulse.instructions.instruction.Instruction.draw()` is deprecated as of qiskit-terra 0.23.0. It will be removed no earlier than 3 months after the release date. No direct alternative is being provided to drawing individual pulses. But, instructions can be visualized as part of a complete schedule using `qiskit.visualization.pulse_drawer`.
</Admonition>

**Parameters**

*   **dt** ([*float*](https://docs.python.org/3/library/functions.html#float "(in Python v3.11)")) – Time interval of samples
*   **style** (*Optional\[SchedStyle]*) – A style sheet to configure plot appearance
*   **filename** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)") *| None*) – Name required to save pulse image
*   **interp\_method** ([*Callable*](https://docs.python.org/3/library/typing.html#typing.Callable "(in Python v3.11)") *| None*) – A function for interpolation
*   **scale** ([*float*](https://docs.python.org/3/library/functions.html#float "(in Python v3.11)")) – Relative visual scaling of waveform amplitudes
*   **plot\_all** ([*bool*](https://docs.python.org/3/library/functions.html#bool "(in Python v3.11)")) – Plot empty channels
*   **plot\_range** ([*Tuple*](https://docs.python.org/3/library/typing.html#typing.Tuple "(in Python v3.11)")*\[*[*float*](https://docs.python.org/3/library/functions.html#float "(in Python v3.11)")*] | None*) – A tuple of time range to plot
*   **interactive** ([*bool*](https://docs.python.org/3/library/functions.html#bool "(in Python v3.11)")) – When set true show the circuit in a new window (this depends on the matplotlib backend being used supporting this)
*   **table** ([*bool*](https://docs.python.org/3/library/functions.html#bool "(in Python v3.11)")) – Draw event table for supported instructions
*   **label** ([*bool*](https://docs.python.org/3/library/functions.html#bool "(in Python v3.11)")) – Label individual instructions
*   **framechange** ([*bool*](https://docs.python.org/3/library/functions.html#bool "(in Python v3.11)")) – Add framechange indicators
*   **channels** ([*List*](https://docs.python.org/3/library/typing.html#typing.List "(in Python v3.11)")*\[*[*Channel*](pulse#qiskit.pulse.channels.Channel "qiskit.pulse.channels.Channel")*] | None*) – A list of channel names to plot

**Returns**

A matplotlib figure object of the pulse schedule

**Return type**

matplotlib.figure

### insert

<span id="qiskit.pulse.instructions.SetPhase.insert" />

`insert(start_time, schedule, name=None)`

Return a new [`Schedule`](qiskit.pulse.Schedule "qiskit.pulse.Schedule") with `schedule` inserted within `self` at `start_time`.

**Parameters**

*   **start\_time** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")) – Time to insert the schedule schedule
*   **schedule** (*Union\['Schedule', 'Instruction']*) – Schedule or instruction to insert
*   **name** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)") *| None*) – Name of the new schedule. Defaults to name of self

**Returns**

A new schedule with `schedule` inserted with this instruction at t=0.

**Return type**

[Schedule](qiskit.pulse.Schedule "qiskit.pulse.Schedule")

### is\_parameterized

<span id="qiskit.pulse.instructions.SetPhase.is_parameterized" />

`is_parameterized()`

Return True iff the instruction is parameterized.

**Return type**

[bool](https://docs.python.org/3/library/functions.html#bool "(in Python v3.11)")

### shift

<span id="qiskit.pulse.instructions.SetPhase.shift" />

`shift(time, name=None)`

Return a new schedule shifted forward by time.

**Parameters**

*   **time** ([*int*](https://docs.python.org/3/library/functions.html#int "(in Python v3.11)")) – Time to shift by
*   **name** ([*str*](https://docs.python.org/3/library/stdtypes.html#str "(in Python v3.11)") *| None*) – Name of the new schedule. Defaults to name of self

**Returns**

The shifted schedule.

**Return type**

[Schedule](qiskit.pulse.Schedule "qiskit.pulse.Schedule")

