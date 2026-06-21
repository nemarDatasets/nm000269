# BigP3BCI Study A — P300 BCI EEG dataset (13 healthy subjects, Mainsah et al. 2025)

## Overview

Mainsah2025-A is a derivative P300 brain-computer interface dataset containing EEG recordings from 13 healthy subjects (1 session each) performing a visual speller task using a 6x6 checkerboard stimulus paradigm. The dataset comprises 32-channel EEG data sampled at 256 Hz with binary classification of target and non-target events, annotated using HED 8.4.0 schema. This dataset represents Study A of the BigP3BCI collection (10.13026/0byy-ry86), the largest public P300 BCI dataset, and is processed using the MOABB (Mother of All BCI Benchmarks) framework.

## Dataset Summary

| Property | Value |
|---|---|
| Subjects | 13 |
| Channels | 32 |
| Classes | 2 |
| Trial length | 1 s |
| Sampling frequency | 256 Hz |
| Sessions | 1 |

| Paradigm | P300 |

## Data Collection Methods

EEG data were acquired using a g.USBamp amplifier (g.tec) with 32 channels arranged in a standard 10-20 montage, sampled at 256 Hz with a 60 Hz line frequency notch. Subjects performed a visual P300 speller task using a 6x6 checkerboard stimulus paradigm with row-column and random presentation modes. Trial intervals were defined from 0 to 1.0 seconds post-stimulus, with binary classification of target and non-target events.

## How to Access via MOABB

Install MOABB and load this dataset directly:

```python
from moabb.datasets import Mainsah2025_A
from moabb.paradigms import P300
paradigm = P300()

dataset = Mainsah2025_A()
X, y, metadata = paradigm.get_data(dataset)
```

For more details see the [MOABB documentation](https://moabb.neurotechx.com/) and the
[MOABB dataset page](https://moabb.neurotechx.com/docs/generated/moabb.datasets.Mainsah2025_A.html).

## Citation

If you use this dataset please cite the primary publication:

> DOI: [10.13026/0byy-ry86](https://doi.org/10.13026/0byy-ry86)

## NEMAR / MOABB Benchmark Collection

This BIDS-formatted dataset was converted from the original data using the
[MOABB](https://moabb.neurotechx.com/) pipeline and re-hosted on
[NEMAR](https://nemar.org/) as part of the MOABB benchmark collection.
The original data and license terms apply — see `dataset_description.json` for details.
