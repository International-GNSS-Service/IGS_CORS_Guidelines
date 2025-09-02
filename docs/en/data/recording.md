The bare minimum that an IGS CORS needs to provide is daily RINEX observation files with a sampling rate of 30 seconds. A sampling rate of 15 seconds is acceptable but not encouraged. Furthermore, station operators are asked to provide RINEX navigation files[^1].

It is recommended to provide hourly RINEX files with a sampling rate of 30 seconds. Newly proposed IGS stations are encouraged to provide hourly RINEX files with a sampling rate of 30 seconds and high-rate (1Hz) RINEX files with a duration of 15 minutes if feasible.

Each RINEX data file has to be sent to at least two of the global IGS data centres[^2]. If the station is already included in a regional network (e.g., APREF, EPN, SIRGAS) and data is publicly available, the transmission to one of the global data centres is sufficient. Data transmission will be coordinated through the IGS Network Coordinator.

After a communication outage, missing data files need to be submitted to the data centre(s). An announcement explaining details about the outage shall be sent to the community (see section [Announcements](../announcements) for more information).

The listing below highlights key figures for the signal tracking, data recording and data transmission that should be aimed by each IGS CORS.

**Signal Tracking and Data Archival**

- 99% of the available epochs in a day are fully observed, recorded and archived (<15 minutes of outage per day).
- 99% of the available epochs in a year are fully observed, recorded and archived (<91 hours of total outage per year).

**Data Transmission**

- The latency of an hourly data file for archival should be <5 minutes after the end of each hour.
- The latency of a daily data file for archival should be <30 minutes after the end of the day.

**Resubmission after Outage**

- All missing daily files need to be resubmitted as soon as possible.
- Missing hourly files need to be resubmitted at the minimum for the last complete three days.

## High-Rate Data

In support of Near-Real-Time (NRT) applications, station operators are encouraged to provide 15-minute RINEX observation and navigation files with a data frequency of 1 Hz (if applicable). They could be either generated from real-time streams or recorded by the receiver.
The stations participating in the high-rate data provision are encouraged to provide the files with a delay of 5 minutes or less from the last recorded observation epoch.

## Real-Time Data

In addition to meeting the standards of a conventional IGS station, Real-Time stations are required to stream GNSS observation data with a minimum data interval of 1 Hz. All newly proposed IGS stations must be able to stream data in real-time unless they are considered to be of value to contribute to the reference frame (e.g., by being co-located to a SLR or VLBI station) or are located in a region of geographical need.
The recommendations that need to be fulfilled by an IGS Real-Time station are described in section 2 of the [Guidelines for IGS Real-Time Broadcasters and Stations](https://files.igs.org/pub/resource/guidelines/Guidelines_for_IGS_Real_Time_Broadcasters_and_Stations.pdf).

## Meteorological Data

It is recommended to install precise meteorological equipment on an IGS CORS. Sensor specific guidelines are described in Section [Meteorological Sensors](../equipment/meteo_sensors.md). As a minimum, the data must include pressure and temperature measurements and shall be distributed in RINEX format. The RINEX files should be transmitted on the same schedule as the RINEX observation files (hourly and/or daily).

[^1]: To reduce the number of files, it recommended to send mixed navigation files that contain all navigation data in a single file.
[^2]: A list of IGS global data centres can be found on the IGS website: [https://igs.org/data-access/#data-centers](https://igs.org/data-access/#data-centers)
