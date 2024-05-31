## Power Supply

Every CORS needs to be powered by a continuous and reliable source. Mains and solar power are both suitable primary power sources. The choice between solar and mains primary power is a balance of cost, security, availability, and location. A distant connection to the power grid may make solar power with a battery array a more economical choice. Unreliable mains power, with significant power fluctuations, may make solar power preferable, particularly in regional areas.

**Mains Power**
Where mains power is used, a dedicated power circuit for the CORS equipment is recommended to reduce the risk that power loads from other equipment may trip a circuit breaker or residual current device and interrupt the power to the CORS equipment. Install mains power outlets in a manner that minimises inadvertent or wilful disconnection of power to the site equipment. It is recommended to install surge protection to prevent damage from power spikes.

**Solar (Photovoltaic) Power**

Available sunlight is the key factor for solar performance. This is a function of latitude and local climate conditions. One can check with the local weather agencies for average hours of available sunlight in the target area.

A battery system is required for solar powered sites, and is a common secondary power supply for sites with mains primary power. An Uninterruptible Power Supply (UPS) is a common short term power source, providing power during the switchover between the primary and long-term secondary power sources.

A Power Distribution Unit (PDU) is recommended for CORS sites. The PDU manages and conditions the power supply to the site, often with an automatic fall-over/fall-back mechanism to switch between primary and secondary power sources. A remotely managed PDU controls the power system within pre-set limitations and provides system tools, reports and alerts. Depending on the ambient conditions, a PDU may also switch less critical equipment off and back on again. A PDU with a communications link allows the CORS operator to control power to the equipment manually from a remote location.

## Communications

A CORS site requires reliable communications for data transmission, either directly to users, or to an operational data centre (ODC). The design of this communication system is a core design issue affecting data transmission and remote control of the CORS equipment.
There are a range of communication options and service providers available. Common communication systems for data transmission between a CORS site and an ODC include:

- ADSL (Asymmetric Digital Subscriber Line),
- Mobile phone network,
- Corporate WAN (Wide Area Network) between offices,
- Very Small Aperture Terminal (VSAT) satellite link for remote locations.

The communication system design depends on the data bandwidth required, data protocols used, acceptable latency of data, and the services available in the target area.

A secondary independent communication system is recommended to improve site reliability. Secondary communications are important at sites offering real-time services, and at remote sites where the expense of a site visit exceeds the costs of the communication system.

The bandwidth required for CORS data transmission is affected by a number of factors including:

- Normal transmission operations (i.e., data streaming and regular data downloads),
- Irregular downloads such as retrieving data stored on the receiver after a communications outage,
- Uploads for receiver firmware upgrades,
- Additional bandwidth loads such as Graphical User Interface support for GNSS receivers, meteorological stations, and network or power management devices,
- Increased overall data volumes due to GNSS modernisation (i.e., additional signals, satellites, and satellite systems).

Irrespective of the communications method used, data latency from a CORS site to the user for real-time positioning services should not exceed two seconds.
