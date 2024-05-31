The quality of a satellite signal arriving at a GNSS antenna has a crucial impact on the performance of a GNSS station. There are a variety of factors that can influence the signal quality that are outlined in the following sections.

## Sky Visibility

GNSS stations should be located on sites with minimal obstructions above the local horizon. Above 10° elevation, the station should not show any obstructions. The receiver shall be set to track all satellites within an elevation mask of 0°.

## Multipath

The interference by multipath occurs when a GNSS satellite signal arrives at the antenna on different pathways. The signal arrives once directly from the satellite, and additionally by having reflected off other surfaces.
Multipath sources can be either natural or artificial. Table 2 lists possible sources known to generate strong multipath.

Artificial Sources:

- Metal panels and signs
- Roofs
- Walls of buildings
- Mesh fencing
- Solar panels

Natural Sources:

- Trees (especially wet ones)
- Water surfaces such as lakes, rivers, etc.

Avoid these reflective bodies at GNSS sites at any time. Suspected sources of multipath should be a minimum of 20 metres away from the GNSS antenna and below 5° elevation.

## Radio Interference Sources

Common sources of Radio Frequency Interference (RFI) include:

- Radio, television and mobile phone transmitters,
- Microwave data links,
- Power lines,
- Transformers.

Directional transmitters, particularly microwave data links pointing toward the CORS site, can cause significant RFI.
Among other parameters, the effect of RFI is a function of the frequency, radiated power, and distance to the source. The effect of RFI is significantly increased when the RFI is a harmonic of a GNSS signal frequency.

Therefore, it is difficult to define a safe operating distance from an RFI source. RFI can be difficult to confirm and specialist advice may be necessary if RFI is suspected. If RFI is confirmed, and cannot be mitigated at a proposed CORS site, an alternate CORS site should be considered.

!!! note "Note"

    RFI sources do not only affect the GNSS signals received at the antenna, but also the wireless (radio or mobile phone network) transmission of site data. Where a CORS site is transmitting data via radio link, the radio transmission may itself be a source of RFI on the GNSS signals at the antenna.

Prior to the final installation of a monument, it is recommended to test the multipath environment and check whether RFI sources are present at the GNSS site. This could be done by installing the GNSS equipment on a temporary tripod and investigating the data quality.