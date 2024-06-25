GNSS metadata is the information about the site, including site ownership, contact details, monument information, the site coordinates and a history of the installed equipment. Reliable and current metadata is central to the management and use of a GNSS station, and is the responsibility of the station operator.

## IGS Site Log/GeodesyML

The IGS requires that CORS record and maintain their metadata in an IGS site log (ASCII) or GeodesyML, and that the metadata is made available to the IGS and to all users. The IGS uses a [web application](https://slm.igs.org) to maintain the station metadata.

It is mandatory that the metadata is completed and published for all CORS to provide a consistent method of distributing relevant site information to analysis centres and users. A CORS operator may need to keep additional metadata for the site to aid internal management and operation.

All IGS stations are identified using a unique Nine-Character abbreviation. The first four characters should be globally unique, and the name is usually chosen to represent the suburb, town or locality of the site. The GNSS operator should check with the IGS Network Coordinator that the proposed four-character identifier for a new CORS is not already in use. Furthermore, each IGS CORS needs to apply for an [IERS DOMES number](domes-request). Make sure that the intended four-character code has not already been used for other geodetic techniques by checking the [IERS DOMES number list](domes-list).

## RINEX Headers

RINEX headers must match the metadata recorded in the IGS site log. RINEX files shall be resubmitted in case of metadata discrepancies. All information in the RINEX header must be ASCII encoded. The usage of characters from other encoding standards (e.g., UTF-8) can lead to a shift of the header elements while decoding, e.g., by using diacritics. The table below lists the mandatory RINEX header elements provided for each RINEX file.

| RINEX Header Element  | Recommendations | Example |
| --------------------- | --------------- | ------- |
| `MARKER NAME`         | <ul><li>It is recommended to use the nine-character station code.</li><li>Alternatively, the 4-character station code can be used.</li><li>All letters must be provided in uppercase.</li></ul> | OUS200NZL<br>OUS2 |
| `MARKER NUMBER`       | IERS Domes number. All letters must be provided in uppercase. | 50212M002 |
| `MARKER TYPE`         | Must be set to GEODETIC. ||
| `OBSERVER`            | It is recommended to provide a generic email address. The maximum number of characters is 20. | gnss@agency.org |
| `AGENCY`              | It is recommended to provide the agency abbreviations as stated in the IGS site log sections 11 and 12. If multiple agencies are listed, they should be separated by a slash (“/”). Maximum number of characters is 60. | OUSD/GFZ |
| `REC # / TYPE / VERS` | All receiver information must be identical to the metadata stated in the IGS site log. ||
| `ANT # / TYPE`        | All antenna information must be identical to the metadata stated in the IGS site log. ||
| `APPROX POSITION XYZ` | The approximate coordinates shall agree to 1 m accuracy to the ones stated in the IGS site log. ||
| `ANTENNA: DELTA H/E/N` | The antenna eccentricities must match the ones stated in the IGS site log. ||

## Digital Photographs

Every CORS must provide pictures of the antenna installation in the four cardinal directions (preferably 8 pictures every 45°), the monument and its vicinity. They need to be updated after each event or hardware change on the site.
The pictures must be labelled and named in the following file naming convention:

`SSSSMRCCC_YYYYMMDD_D[D].fff`

The table below describes the elements of this convention. All elements are separated by an underscore (“_”).

| Component   | Description | Example |
| ----------- | ----------- | ------- |
| `SSSSMRCCC` | The nine-character station code. | NYA200NOR |
| `YYYYMMDD`  | Date of admission (year, month, day) without separation and zero-padded. | 20210131 |
| `D[D]`      | <ul><li>Cardinal direction: N, E, S, W and a two-way combination of them</li><li>Antenna serial number: AS</li><li>Antenna mount: AM</li><li>Receiver: R</li><li>Monument: M</li></ul> | N (North)<br>SE (South-East) |
| `fff`      | The format of the graphic file. Supported are JPEG and PNG. | .jpg |

Alternatively, pictures can be made available to a website hosted by the station operator or the parent organisation.

## Individual Antenna Calibrations

Although not mandatory, it is recommended to provide individual antenna calibrations. They are useful for activities and investigations for different IGS working groups (e.g., Antenna Working Group). The corresponding ANTEX file should be made available to the IGS Network Coordinator.

## Data Protection Compliance

The European Union and other countries implemented regulations on the protection of personal data. Since the IGS is a voluntary federation without a strong legal representation, it is not in the interest of the IGS to deal with the subtleties that each of the regulations bring with them.
We therefore ask, that all personal information in the metadata (IGS site logs/GeodesyML) and RINEX header (full names and email addresses) get replaced by generic names and email lists, e.g.:

- IGS Site Log/GeodesyML:
    - Contact Name: “Agency” Network operator
    - E-Mail: gnss@agency.org
- RINEX Header:
    - Observer: gnss@agency.org
    - Comments with disclaimer information

Stations proposed to the IGS will need to follow these rules prior to their acceptance. Station operators who are updating the metadata of their stations will also be asked to use data protection compliant contact information.

[domes-request]: https://itrf.ign.fr/en/network/domes/request
[domes-list]: https://itrf.ign.fr/en/network/list