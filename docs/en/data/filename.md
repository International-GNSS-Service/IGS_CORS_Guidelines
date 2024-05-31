The IGS currently supports three major versions of the RINEX standard, RINEX v.2, RINEX v.3, and RINEX v.4. Every station operator is encouraged to transmit the latest available major/minor version. Newly proposed IGS CORS must submit their data in RINEX 3.04 at a minimum.

## RINEX v.4/v.3

[RINEX v.3](https://files.igs.org/pub/data/format/rinex305.pdf) and [RINEX v.4](https://files.igs.org/pub/data/format/rinex_4.01.pdf) data must be transmitted in the following file naming convention:

*Observation and Meteorological Files*

`SSSSMRCCC_S_YYYYDDDHHMM_DDU_FRU_DT.fff.cmp`

*Navigation Files*

`SSSSMRCCC_S_YYYYDDDHHMM_DDU_DT.fff.cmp`

All elements of the main body of the file name must contain capitalised ASCII letters or numbers and all elements are of a fixed length and separated by an underscore “_”. The file type and compression fields (extension) use a period “.” as a separator and must be lowercase ASCII characters. Fields must be padded with zeros to fill the field width.
In order to further reduce the size of observation files, the [Hatanaka compression toolkit](https://terras.gsi.go.jp/ja/crx2rnx.html) should be used.

=== "SSSSMRCCC"
    The Nine-character IGS Station Name

    - SSSS: 4-character (existing) IGS station name
    - M: monument or marker number (0-9)
    - R: receiver number (0-9)
    - CCC: ISO-3166 country or region code (alpha-3)
    
    Example: POTS00DEU

    Note: To align with the SINEX format, marker and monument numbers other than 0 are currently not supported
                                                                                                                                                                   |
=== "S"
    Data source

    Supported are R (from receiver using vendor or other software) and S (RTCM or another stream format)

=== "YYYYDDDHHMM"

    Start time

    - YYYY: Gregorian year (e.g., 2024)
    - DDD: Day of the year (e.g., 260)
    - HHMM: Hours and minutes of the day (e.g., 1000)

    It is preferred to use the nominal start time of the file. However, using the actual start time of a file is acceptable.

=== "DDU"
    File Period

    - DD: File period
    - U: Unit of the file period
    - Accepted are 15M, 01H, 01D

=== "FRU"
    Data Frequency

    - FR: Data frequency
    - U: Unit of the data frequency
    - Accepted are 01S for high-rate data and 30S or 15S for hourly/daily data

    Not required for RINEX navigation files

=== "DT"
    Data Type

    - Two characters represent the type
    - D: Satellite System (allowed are G, R, E, C, J,S,Iand M(ixed))
    - T: RINEX file type (allowed are O, N, M)

    Example: MO

=== "fff"
    Format of the file. Supported are rnx (RINEX) and crx (compressed RINEX)

=== "cmp"
    Compression format. Supported is gzip (gz).

## RINEX v.2

RINEX v.2 (Gurtner, 2007) data must be transmitted in the following file naming convention:

`ssssdddf.yyt`

The table below describes each element of this file naming convention. Stations transmitting RINEX v.2 files are encouraged to provide gzip compressed files. Even if files are sent in Z-compression, IGS data centres will recompress them and make them publicly available using gzip.


=== "ssss"
    The 4-character IGS station name

    Example: pots

=== "ddd"
    Day of the year of the first record

    Example: 260

=== "f"
    File sequence number/character within day
    
    - Daily files (30 seconds): f=0
    - Hourly files (30 seconds):
        - f=a (00:00:00 to 00:59:30),
        - f=b (01:00:00 to 01:59:30), 
        - ...
        - f=x (23:00:00 to 23:59:30)
    - High-rate files (15M, 1 Hz):
        - f=a00 (00:00:00 to 00:14:59)
        - f=a15 (00:15:00 to 00:29:59) ...
        - f=m30 (12:30:00 to 12:44:59) ...
        - f=x45 (23:45:00 to 23:59:59)

=== "yy"
    Two-digit year (e.g., 24)

=== "t"
    File Type, allowed file types are:

    - O: Observation file
    - D: Hatanaka compressed observation file
    - N: GPS navigation file
    - G: GLONASS navigation file
    - M: Meteorological file
