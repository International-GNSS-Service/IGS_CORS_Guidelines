This section presents an overview of the mandatory and desirable recommendations that need to be fulfilled by a CORS to join the IGS network. They are intended to be applicable both to current active IGS stations and to proposed stations. Full compliance with these Guidelines is clearly desired by the IGS, however where guidelines cannot be complied with, station operators are asked to consult with the Infrastructure Committee. Detailed information about the shown recommendations can be found in subsequent chapters of these Guidelines.

??? info "Legend"

    !!! success "Minimum"
        This feature is the minimum required one.

    !!! warning "Encouraged"
        This feature is encouraged but not mandatory.

    !!! failure "Not recommended"
        This feature is not recommended.

## General

| Recommendation | Classification  |
| -------------- | --------------- |
| Station belongs to a national/regional geodetic network[^1]                                         | encouraged |
| Station planned and installed for continuous and permanent operation                             | * |
| Station’s operating agency maintains full capability to repair, upgrade and maintain the station | * |

## Foundation and Location

| Recommendation | Classification  |
| -------------- | --------------- |
| Bedrock or massive concrete base | ✳ |
| Mounted on buildings or similar structures[^2] | x |
| Clear sky view with limited obstructions above 10° | ✳ |
| Site is clear from signal obstructions or RFI | ✳ |
| Site is clear from reflective material |  |

## Monumentation and Mounting

| Recommendation | Classification  |
| -------------- | --------------- |
| Concrete pillar or braced (tri-, quad-, ...)pod monuments | ✳ |
| (Steel) mounts attached to building | ❌ |
| The mount locks the antenna in place to maintain orientation and level | ✳ |
| The mount allows the antenna to be removed and returned within 0.5 mm and 1° of its original location and orientation | * |

## Power and Communication

| Recommendation | Classification  |
| -------------- | --------------- |
| Ensure continuous operation of all communication devices | encouraged |
| Ensure remotely controlled access to the receiver | * |

## Receiver

| Recommendation | Classification  |
| -------------- | --------------- |
| Multi-frequency code and carrier phase tracking for all GNSS[^3] | ✳ |
| Continuous logging of raw GNSS data | ▼ |
| Real-Time data streaming (RTCM) | ▼ |
| All-in-view satellite tracking (healthy and unhealthy) with a minimum of 5° elevation (0° is encouraged) | ✳ |
| Disabling pseudorange and phase smoothing | ✳ |
| Disabling multipath mitigation | ✳ |
| Ability to store a reasonable amount of raw data (depending on local circumstances) | * |

## Antenna

| Recommendation | Classification  |
| -------------- | --------------- |
| Use of an antenna with an IGS calibrated absolute antenna phase centre (mean calibration) as included in the official [IGS ANTEX](https://files.igs.org/pub/station/general/igs20.atx) | * |
| Individually calibrated absolute antenna phase centre | ▼ |
| Antenna levelled and oriented within 5° to true North | ✳ |
| Antenna radome protection | x |

## Data

| Recommendation | Classification  |
| -------------- | --------------- |
| Data must be provided in RINEX format[^4] | ✳ |
| ^^ Real-Time stream is available[^5]:^^<br>RTCM 3 MSM5 stream for real-time applications[^6] | ✳ |
| Data must be resubmitted to the data centres after communication outage | ✳ |
| RINEX data must be generated on-board the receiver ^^or^^ from native binary file | ✳ |
| File completeness target | 99% |

### High-rate RINEX files

| Recommendation |             | Classification  |
| -------------- | ------------| --------------- |
| Provision      |             | encouraged |
| Latency        | < 5 minutes | ✳ |
| Sampling rate  | 1 Hz        | ✳ |
| Duration       | 15 minutes  | ✳ |

### Hourly RINEX files

| Recommendation |             | Classification  |
| -------------- | ------------| --------------- |
| Provision      |             | encouraged |
| Latency        | < 5 minutes | ✳ |
| Sampling rate  | 30 seconds  | ✳ |

### Daily RINEX files

| Recommendation |             | Classification  |
| -------------- | ------------| --------------- |
| Provision      |             | * |
| Latency        | < 30 minutes| ✳ |
| Sampling rate  | 30 seconds  | ✳ |

## Metadata

| Recommendation | Classification  |
| -------------- | --------------- |
| Complete and up-to-date metadata in IGS site log/GeodesyML format | ✳ |
| Unique nine-character station identifier approved by IGS | ✳ |
| Assigned with unique IERS DOMES number | ✳ |
| Update of IGS site log within 24 hours of applied station change(s) | ✳ |
| RINEX header matches the information in the IGS metadata record | ✳ |
| Provision of pictures of the antenna installation in the 4 cardinal directions (N, E, S, W) | ✳ |

[^1]: Mandatory for regional CORS in the footprint of APREF, EPN, and SIRGAS.
[^2]: Waivers may be granted after revision by the SPC.
[^3]: New stations shall track all available frequency code and carrier phases.
[^4]: For new stations: RINEX 3.04 is the minimum accepted version. RINEX 2.11 is not accepted.
[^5]: New stations are highly encouraged to provide real-time streams.
[^6]: MSM7 is encouraged.
