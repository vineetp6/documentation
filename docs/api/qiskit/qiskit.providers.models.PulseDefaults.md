---
title: PulseDefaults
description: API reference for qiskit.providers.models.PulseDefaults
in_page_toc_min_heading_level: 1
python_api_type: class
python_api_name: qiskit.providers.models.PulseDefaults
---

# PulseDefaults

<span id="qiskit.providers.models.PulseDefaults" />

`qiskit.providers.models.PulseDefaults(qubit_freq_est, meas_freq_est, buffer, pulse_library, cmd_def, meas_kernel=None, discriminator=None, **kwargs)`

Bases: [`object`](https://docs.python.org/3/library/functions.html#object "(in Python v3.11)")

Description of default settings for Pulse systems. These are instructions or settings that may be good starting points for the Pulse user. The user may modify these defaults for custom scheduling.

Validate and reformat transport layer inputs to initialize. :param qubit\_freq\_est: Estimated qubit frequencies in GHz. :param meas\_freq\_est: Estimated measurement cavity frequencies in GHz. :param buffer: Default buffer time (in units of dt) between pulses. :param pulse\_library: Pulse name and sample definitions. :param cmd\_def: Operation name and definition in terms of Commands. :param meas\_kernel: The measurement kernels :param discriminator: The discriminators :param \*\*kwargs: Other attributes for the super class.

## Attributes

<span id="qiskit.providers.models.PulseDefaults.qubit_freq_est" />

### qubit\_freq\_est

Qubit frequencies in Hertz.

<span id="qiskit.providers.models.PulseDefaults.meas_freq_est" />

### meas\_freq\_est

Measurement frequencies in Hertz.

## Methods

### from\_dict

<span id="qiskit.providers.models.PulseDefaults.from_dict" />

`classmethod from_dict(data)`

Create a new PulseDefaults object from a dictionary.

**Parameters**

**data** ([*dict*](https://docs.python.org/3/library/stdtypes.html#dict "(in Python v3.11)")) – A dictionary representing the PulseDefaults to create. It will be in the same format as output by [`to_dict()`](#qiskit.providers.models.PulseDefaults.to_dict "qiskit.providers.models.PulseDefaults.to_dict").

**Returns**

The PulseDefaults from the input dictionary.

**Return type**

[PulseDefaults](#qiskit.providers.models.PulseDefaults "qiskit.providers.models.PulseDefaults")

### to\_dict

<span id="qiskit.providers.models.PulseDefaults.to_dict" />

`to_dict()`

Return a dictionary format representation of the PulseDefaults. :returns: The dictionary form of the PulseDefaults. :rtype: dict

