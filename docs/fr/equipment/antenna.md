The station’s GNSS absolute antenna calibration must be available in the current [IGS ANTEX format](https://files.igs.org/pub/data/format/antex14.txt). This file contains model specific antenna calibrations. Although using type-mean calibrations is the current standard in the IGS analysis, it is preferred to also calibrate each GNSS used in the IGS network individually. It is recommended that new antennas are either calibrated by a robot or in the chamber. For antenna calibrations to be valid, the GNSS antenna must be oriented to True North with an accuracy of ±5°. Relative antenna calibration models should not be used.

The GNSS antenna must be rigidly and securely attached to the top of the station monument as described in section [Site Stability](../../establishment/stability).

Eccentricities between the marker and the Antenna Reference Point (ARP) must be surveyed and reported in the IGS site logs and RINEX headers to ≤1 mm accuracy; a horizontal eccentricity of 0 m is preferred.

The use of choke-ring antennas is recommended. They have very stable and well understood properties, with high multipath mitigation.

The use of radomes is discouraged. Although they provide some level of protection from the elements, radomes alter the location of the Antenna Phase Centre (APC). Even worse, as ultraviolet light affects the properties of the radome material, its impact on the APC's location varies. However, environmental conditions such as snowfall, sea spray or the likelihood that the antenna may be used as a perch for birds may require the use of a radome. In this case, the antenna/radome combination must have a valid antenna calibration. Conical radomes should not be used. Do not remove radomes from existing GNSS antennas.

Experience shows that when a GNSS antenna is removed and replaced there is a change in the computed position of the site, even when the ARP is replaced precisely. Therefore, do not remove the antenna for any reason other than hardware failure or to perform necessary local tie surveys. For the latter reason it is mandatory to reflect this in the station metadata. If you need to change the antenna, users and analysis centres shall be forewarned (see section [Announcements](../../data/announcements)).

Choose antennas that are capable of tracking as many planned GNSS signals as possible at the time of purchase to reduce the need to remove an antenna to track newly available GNSS signals. To avoid confusion, the IGS standard naming convention for [antenna models](https://files.igs.org/pub/station/general/rcvr_ant.tab) must be used in the RINEX headers and metadata.

### Antenna Type

The use of unique (“unknown”) antennas is not permitted. The use of choke-ring antennas with Dorne-Margolin elements if preferred.
The antenna’s satellite signal tracking capabilities should match or exceed the capability of the GNSS receiver. For new stations this requirement is mandatory.
The antenna and antenna connectors must be weatherproof and corrosion resistant.

### Calibrations

All IGS antennas shall have a valid IGS absolute antenna calibration. If an antenna is individually calibrated, the corresponding ANTEX file should be made available to the IGS. Antennas should be either robot or chamber calibrated.

### ARP and Eccentricities

All antenna-offset measurements shall refer to the ARP. Eccentricities (East, North, Up) from the permanent position marker to the ARP must be surveyed and reported in the metadata and RINEX headers with an accuracy of ≤ 1 mm.

### Radome

The use of a radome is strongly discouraged. If the use of a radome is absolutely necessary, the use of a hemispherical radome with a valid absolute antenna
calibration is recommended.
Do not use conical radomes.

### Antenna Orientation

The antenna has to be oriented to True North with an accuracy of ±5°.
If the deviation is greater than 5°, the actual alignment has to be noted in the metadata.
