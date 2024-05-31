## Stromversorgung

Jede CORS-Station benötigt eine kontinuierliche und zuverlässige Stromquelle. Netzstrom und Solarstrom sind beide geeignete primäre Stromquellen. Die Wahl zwischen Solar- und Netzstrom hängt von den Kosten, der Sicherheit, der Verfügbarkeit und dem Standort ab. Eine entfernte Verbindung zum Stromnetz kann Solarstrom mit einem Batteriesystem zu einer wirtschaftlicheren Wahl machen. Unzuverlässiger Netzstrom mit erheblichen Spannungsschwankungen kann Solarstrom, insbesondere in ländlichen Gebieten, bevorzugen.

**Netzstrom**

Wo Netzstrom verwendet wird, wird empfohlen, einen dedizierten Stromkreis für die CORS-Ausrüstung einzurichten, um das Risiko zu verringern, dass Lasten von anderen Geräten einen Leistungsschalter oder Fehlerstromschutzschalter auslösen und die Stromversorgung der CORS-Ausrüstung unterbrechen. Installieren Sie Netzsteckdosen so, dass versehentliche oder vorsätzliche Trennungen der Stromversorgung zur Standortausrüstung minimiert werden. Es wird empfohlen, Überspannungsschutz zu installieren, um Schäden durch Spannungsspitzen zu verhindern.

**Solarstrom (Photovoltaik)**

Verfügbare Sonneneinstrahlung ist der Schlüsselfaktor für die Solarleistung. Dies ist eine Funktion der geografischen Breite und der lokalen klimatischen Bedingungen. Man kann bei den lokalen Wetterbehörden nach den durchschnittlichen Sonnenstunden in der Zielregion fragen.

Ein Batteriesystem ist für solarbetriebene Standorte erforderlich und ist eine häufige sekundäre Stromquelle für Standorte mit primärem Netzstrom. Eine unterbrechungsfreie Stromversorgung (USV) ist eine übliche kurzfristige Stromquelle, die während des Umschaltens zwischen der primären und der langfristigen sekundären Stromquelle Strom liefert.

Eine Stromverteilungseinheit (PDU) wird für CORS-Standorte empfohlen. Die PDU verwaltet und konditioniert die Stromversorgung des Standorts, oft mit einem automatischen Fallback-Mechanismus, um zwischen primären und sekundären Stromquellen zu wechseln. Eine ferngesteuerte PDU steuert das Stromsystem innerhalb voreingestellter Grenzen und bietet Systemtools, Berichte und Warnungen. Abhängig von den Umgebungsbedingungen kann eine PDU auch weniger kritische Geräte ein- und ausschalten. Eine PDU mit Kommunikationsverbindung ermöglicht es dem CORS-Betreiber, die Stromversorgung der Ausrüstung manuell aus der Ferne zu steuern.

## Kommunikation

Ein CORS-Standort benötigt zuverlässige Kommunikation für die Datenübertragung, entweder direkt zu den Nutzern oder zu einem Betriebsdatenzentrum (ODC). Das Design dieses Kommunikationssystems ist ein Kernaspekt, der die Datenübertragung und die Fernsteuerung der CORS-Ausrüstung beeinflusst.
Es gibt eine Vielzahl von Kommunikationsoptionen und Dienstanbietern. Gängige Kommunikationssysteme für die Datenübertragung zwischen einem CORS-Standort und einem ODC umfassen:

- ADSL (Asymmetric Digital Subscriber Line),
- Mobilfunknetz,
- Corporate WAN (Wide Area Network) zwischen Büros,
- Very Small Aperture Terminal (VSAT) Satellitenverbindung für abgelegene Standorte.

Das Design des Kommunikationssystems hängt von der erforderlichen Datenbandbreite, den verwendeten Datenprotokollen, der akzeptablen Datenlatenz und den in der Zielregion verfügbaren Diensten ab.

Ein sekundäres unabhängiges Kommunikationssystem wird empfohlen, um die Standortzuverlässigkeit zu verbessern. Sekundäre Kommunikationssysteme sind an Standorten wichtig, die Echtzeitdienste anbieten, und an abgelegenen Standorten, an denen die Kosten eines Standortbesuchs die Kosten des Kommunikationssystems übersteigen.

Die für die CORS-Datenübertragung erforderliche Bandbreite wird von einer Reihe von Faktoren beeinflusst, darunter:

- Normale Übertragungsvorgänge (d.h. Datenstreaming und regelmäßige Daten-Downloads),
- Unregelmäßige Downloads, wie das Abrufen von Daten, die nach einem Kommunikationsausfall auf dem Empfänger gespeichert wurden,
- Uploads für Empfänger-Firmware-Upgrades,
- Zusätzliche Bandbreitenbelastungen wie die Unterstützung von grafischen Benutzeroberflächen für GNSS-Empfänger, meteorologische Stationen und Netzwerk- oder Energiemanagementgeräte,
- Erhöhte Gesamt-Datenvolumina aufgrund der Modernisierung von GNSS (d.h. zusätzliche Signale, Satelliten und Satellitensysteme).

Unabhängig von der verwendeten Kommunikationsmethode sollte die Datenlatenz von einem CORS-Standort zum Benutzer für Echtzeit-Positionsdienste zwei Sekunden nicht überschreiten.