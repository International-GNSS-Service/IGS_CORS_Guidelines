Die folgende Liste gibt einen Überblick über die empfohlenen Empfängereigenschaften zum Zeitpunkt der Veröffentlichung dieser Richtlinien. Neu geplante GNSS-Stationen für das IGS müssen alle aufgeführten Merkmale erfüllen. Stationsbetreiber bestehender Stationen, die momentan nicht aufgerüstet werden können, sollten diese Empfehlungen für zukünftige Updates im Auge behalten.

### Signalverfolgung

- Verfolgung aller verfügbaren Trägerphasen-, Pseudostrecken-, Signal-Rausch-Verhältnisse (SNR) pro Frequenz. Doppler-Beobachtungen sind optional.
- Keine Glättung der Pseudostreckenmessungen.
- Multipath-Unterdrückung muss deaktiviert sein.
- Neu geplante Stationen müssen mindestens GPS, GLONASS, Galileo und BeiDou verfolgen[^1].
- Die Fähigkeit, zukünftige Signale zu beobachten, ist bevorzugt.
- Empfänger auf Verfolgung von Signalen bis zu einer Elevation von 0° eingestellt (5° ist akzeptabel).
- Empfänger auf All-in-View-Verfolgung (einschließlich ungesunder Satelliten) eingestellt.
- Empfänger synchronisiert den tatsächlichen Beobachtungszeitpunkt mit der GPS-Zeit innerhalb von 1 Millisekunde des vollen Sekunden-Epoche.

### Ausgabe

- Aktuelle RTCM SC-104 bei 1 Hz auf mehreren Ports.
- Proprietärer Rohdaten-Stream.
- In der Lage, Daten an mehrere Standorte zu streamen.

### Protokollierung

- Kontinuierliche Protokollierung von ungeglätteten Rohdaten.
- Protokollierung von RINEX-Daten (mindestens: 30-Sekunden-Abtastung, wenn nicht außerhalb des Empfängers generiert).
- Protokollierung von Eingangssensordaten.

Die Firmware eines GNSS-Empfängers ist eine Computersoftware, die die Verfolgung des Geräts steuert. Wie jede andere Software kann auch eine Firmware aktualisiert werden, um entweder Fehler zu beheben oder die Verfolgungsfähigkeiten des Empfängers zu verbessern. Vor dem Upgrade sollte eine neue Firmware gründlich getestet werden und nur an Stationen in Betracht gezogen werden, bei denen sie von der Änderung profitieren. Im Allgemeinen sollte der Empfänger mit der neuesten stabilen Firmware innerhalb von 6 Monaten nach ihrer Veröffentlichung betrieben werden.

[^1]: Stationen, die sich im Empfangsbereich der regionalen Satellitensysteme QZSS und IRNSS befinden, sollten diese zusätzlich verfolgen. Die Fähigkeit zur Verfolgung von SBAS (Satellite-Based Augmentation System) wird empfohlen.