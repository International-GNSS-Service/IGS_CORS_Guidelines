The listing below gives an overview of recommended receiver characteristics at the date of issue of these Guidelines. Newly built GNSS stations proposed for the IGS shall fulfil all of the listed features. Station operators of established stations that cannot be upgraded at the moment, shall keep these recommendations in mind for future updates.

### Signal Tracking

- Tracking of all available carrier phase, pseudorange, signal-to-noise (SNR) per frequency. Doppler observations are optional.
- No smoothing of pseudorange measurements.
- Multipath mitigation must be disabled.
- Newly proposed stations must track at least GPS, GLONASS, Galileo, and BeiDou[^1].
- Capability to observe future signals is preferred.
- Receiver set to track signals down to 0° elevation (5° is acceptable).
- Receiver set to all-in-view tracking (including unhealthy satellites).
- Receiver synchronises the actual instant of observation with GPS time to within 1 millisecond of the full second epoch.

### Output

- Current RTCM SC-104 at 1 Hz on multiple ports.
- Proprietary raw data streaming.
- Capable of streaming data to multiple locations.

### Logging

- Continuous logging of raw unsmoothed data.
- Logging of RINEX data (minimum: 30 sec sampling, if not generated outside the receiver).
- Logging of input sensor data.


The firmware of a GNSS receiver is a computer software that controls the tracking of the device. As with any other software, a firmware might be updated to either fix bugs or to improve the tracking capabilities of the receiver. Before upgrading, a new firmware should be thoroughly tested and only be considered on stations where it benefits from the change. In general, the receiver should be operated with the latest stable firmware within 6 months of its release.

[^1]: Stations located in the footprint of the regional satellite systems QZSS and IRNSS shall additionally track those. SBAS tracking capability is encouraged.