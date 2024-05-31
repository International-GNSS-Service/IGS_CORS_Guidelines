This section presents an overview of the mandatory and desirable recommendations that need to be fulfilled by a CORS to join the IGS network. They are intended to be applicable both to current active IGS stations and to proposed stations. Full compliance with these Guidelines is clearly desired by the IGS, however where guidelines cannot be complied with, station operators are asked to consult with the Infrastructure Committee. Detailed information about the shown recommendations can be found in subsequent chapters of these Guidelines.

!!! info "Legend"

    :material-check-bold: This feature is the minimum required one.

    :fontawesome-solid-triangle-exclamation: This feature is encouraged but not mandatory.

    :x: This feature is not recommended.

## General

| Recommendation | Classification  |
| -------------- | --------------- |
| Station belongs to a national/regional geodetic network[^1]                                      | :fontawesome-solid-triangle-exclamation: |
| Station planned and installed for continuous and permanent operation                             | :material-check-bold: |
| Station’s operating agency maintains full capability to repair, upgrade and maintain the station | :material-check-bold: |

## Foundation and Location

| Recommendation | Classification  |
| -------------- | --------------- |
| Bedrock or massive concrete base | :material-check-bold: |
| Mounted on buildings or similar structures[^2] | :x: |
| Clear sky view with limited obstructions above 10° | :material-check-bold: |
| Site is clear from signal obstructions or RFI | :material-check-bold: |
| Site is clear from reflective material | :material-check-bold: |

## Monumentation and Mounting

| Recommendation | Classification  |
| -------------- | --------------- |
| Concrete pillar or braced (tri-, quad-, ...)pod monuments | :material-check-bold: |
| (Steel) mounts attached to building | :x: |
| The mount locks the antenna in place to maintain orientation and level | :material-check-bold: |
| The mount allows the antenna to be removed and returned within 0.5 mm and 1° of its original location and orientation | :material-check-bold: |

## Power and Communication

| Recommendation | Classification  |
| -------------- | --------------- |
| Ensure continuous operation of all communication devices | :fontawesome-solid-triangle-exclamation: |
| Ensure remotely controlled access to the receiver | :material-check-bold: |

## Receiver

| Recommendation | Classification  |
| -------------- | --------------- |
| Multi-frequency code and carrier phase tracking for all GNSS[^3] | :material-check-bold: |
| Continuous logging of raw GNSS data | :fontawesome-solid-triangle-exclamation: |
| Real-Time data streaming (RTCM) | :fontawesome-solid-triangle-exclamation: |
| All-in-view satellite tracking (healthy and unhealthy) with a minimum of 5° elevation (0° is encouraged) | :material-check-bold: |
| Disabling pseudorange and phase smoothing | :material-check-bold: |
| Disabling multipath mitigation | :material-check-bold: |
| Ability to store a reasonable amount of raw data (depending on local circumstances) | :material-check-bold: |

## Antenna

| Recommendation | Classification  |
| -------------- | --------------- |
| Use of an antenna with an IGS calibrated absolute antenna phase centre (mean calibration) as included in the official [IGS ANTEX](https://files.igs.org/pub/station/general/igs20.atx) | :material-check-bold: |
| Individually calibrated absolute antenna phase centre | :fontawesome-solid-triangle-exclamation: |
| Antenna levelled and oriented within 5° to true North | :material-check-bold: |
| Antenna radome protection | :x: |

## Data

| Recommendation | Classification  |
| -------------- | --------------- |
| Data must be provided in RINEX format[^4] | :material-check-bold: |
| ^^ Real-Time stream is available[^5]:^^<br>RTCM 3 MSM5 stream for real-time applications[^6] | :material-check-bold: |
| Data must be resubmitted to the data centres after communication outage | :material-check-bold: |
| RINEX data must be generated on-board the receiver ^^or^^ from native binary file | :material-check-bold: |
| File completeness target | 99% |

### High-rate RINEX files

| Recommendation |             | Classification  |
| -------------- | ------------| --------------- |
| Provision      |             | :fontawesome-solid-triangle-exclamation: |
| Latency        | < 5 minutes | :material-check-bold: |
| Sampling rate  | 1 Hz        | :material-check-bold: |
| Duration       | 15 minutes  | :material-check-bold: |

### Hourly RINEX files

| Recommendation |             | Classification  |
| -------------- | ------------| --------------- |
| Provision      |             | :fontawesome-solid-triangle-exclamation: |
| Latency        | < 5 minutes | :material-check-bold: |
| Sampling rate  | 30 seconds  | :material-check-bold: |

### Daily RINEX files

| Recommendation |             | Classification  |
| -------------- | ------------| --------------- |
| Provision      |             | :material-check-bold: |
| Latency        | < 30 minutes| :material-check-bold: |
| Sampling rate  | 30 seconds  | :material-check-bold: |

## Metadata

| Recommendation | Classification  |
| -------------- | --------------- |
| Complete and up-to-date metadata in IGS site log/GeodesyML format | :material-check-bold: |
| Unique nine-character station identifier approved by IGS | :material-check-bold: |
| Assigned with unique IERS DOMES number | :material-check-bold: |
| Update of IGS site log within 24 hours of applied station change(s) | :material-check-bold: |
| RINEX header matches the information in the IGS metadata record | :material-check-bold: |
| Provision of pictures of the antenna installation in the 4 cardinal directions (N, E, S, W) | :material-check-bold: |

[^1]: Mandatory for regional CORS in the footprint of APREF, EPN, and SIRGAS.
[^2]: Waivers may be granted after revision by the SPC.
[^3]: New stations shall track all available frequency code and carrier phases.
[^4]: For new stations: RINEX 3.04 is the minimum accepted version. RINEX 2.11 is not accepted.
[^5]: New stations are highly encouraged to provide real-time streams.
[^6]: MSM7 is encouraged.
