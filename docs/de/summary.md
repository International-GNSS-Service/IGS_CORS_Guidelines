Dieser Abschnitt bietet einen Überblick über die verbindlichen und wünschenswerten Empfehlungen, die eine CORS erfüllen muss, um dem IGS-Netzwerk beizutreten. Sie sind sowohl für derzeit aktive IGS-Stationen als auch für vorgeschlagene Stationen anwendbar. Die vollständige Einhaltung dieser Richtlinien wird vom IGS eindeutig gewünscht. Wenn die Richtlinien jedoch nicht eingehalten werden können, werden die Stationsbetreiber gebeten, sich mit dem Infrastrukturkomitee in Verbindung zu setzen. Detaillierte Informationen zu den aufgeführten Empfehlungen finden sich in den folgenden Kapiteln dieser Richtlinien.

!!! info "Legende"

    :material-check-bold: Diese Funktion ist die Mindestanforderung.

    :fontawesome-solid-triangle-exclamation: Diese Funktion ist erwünscht, aber nicht zwingend erforderlich.

    :x: Diese Funktion wird nicht empfohlen.

## Allgemein

| Empfehlung     | Klassifizierung |
| -------------- | --------------- |
| Die Station gehört zu einem nationalen/regionalen geodätischen Netzwerk[^1]                                      | :fontawesome-solid-triangle-exclamation: |
| Die Station ist für kontinuierlichen und dauerhaften Betrieb geplant und installiert                             | :material-check-bold: |
| Die betreibende Organisation der Station besitzt die volle Fähigkeit, die Station zu reparieren, aufzurüsten und zu warten | :material-check-bold: |

## Fundament und Standort

| Empfehlung     | Klassifizierung |
| -------------- | --------------- |
| Fels- oder massive Betonbasis | :material-check-bold: |
| Auf Gebäuden oder ähnlichen Strukturen montiert[^2] | :x: |
| Freier Horizontblick mit begrenzten Hindernissen über 10° | :material-check-bold: |
| Standort ist frei von Signalstörungen oder RFI | :material-check-bold: |
| Standort ist frei von reflektierendem Material | :material-check-bold: |

## Monumentierung und Montage

| Empfehlung     | Klassifizierung |
| -------------- | --------------- |
| Betonpfeiler oder abgestützte (Tri-, Quad-, ...) Pod-Monumente | :material-check-bold: |
| (Stahl-) Befestigungen an Gebäuden | :x: |
| Die Halterung fixiert die Antenne, um Orientierung und Niveau zu halten | :material-check-bold: |
| Die Halterung ermöglicht das Entfernen und Wiedereinsetzen der Antenne innerhalb von 0,5 mm und 1° der ursprünglichen Position und Ausrichtung | :material-check-bold: |

## Stromversorgung und Kommunikation

| Empfehlung     | Klassifizierung |
| -------------- | --------------- |
| Sicherstellung des kontinuierlichen Betriebs aller Kommunikationsgeräte | :fontawesome-solid-triangle-exclamation: |
| Sicherstellung des ferngesteuerten Zugriffs auf den Empfänger | :material-check-bold: |

## Empfänger

| Empfehlung     | Klassifizierung |
| -------------- | --------------- |
| Mehrfrequenz-Code- und Trägerphasenverfolgung für alle GNSS[^3] | :material-check-bold: |
| Kontinuierliche Protokollierung der binären GNSS-Daten | :fontawesome-solid-triangle-exclamation: |
| Echtzeit-Datenstreaming (RTCM) | :fontawesome-solid-triangle-exclamation: |
| Verfolgung aller sichtbaren Satelliten (gesund und ungesund) mit einem Minimum von 5° Elevation (0° wird empfohlen) | :material-check-bold: |
| Deaktivierung der Pseudorange- und Phasenglättung | :material-check-bold: |
| Deaktivierung der Mehrwegeunterdrückung | :material-check-bold: |
| Fähigkeit, eine angemessene Menge an Rohdaten zu speichern (abhängig von den örtlichen Gegebenheiten) | :material-check-bold: |

## Antenne

| Empfehlung     | Klassifizierung |
| -------------- | --------------- |
| Verwendung einer Antenne mit einem vom IGS kalibrierten absoluten Antennenphasenmittelpunkt (Mittelkalibrierung) gemäß der offiziellen [IGS ANTEX](https://files.igs.org/pub/station/general/igs20.atx) | :material-check-bold: |
| Individuell kalibrierter absoluter Antennenphasenmittelpunkt | :fontawesome-solid-triangle-exclamation: |
| Antenne nivelliert und innerhalb von 5° nach Norden ausgerichtet | :material-check-bold: |
| Antennenschutz durch Radom | :x: |

## Daten

| Empfehlung     | Klassifizierung |
| -------------- | --------------- |
| Daten müssen im RINEX-Format bereitgestellt werden[^4] | :material-check-bold: |
| ^^Falls Echtzeitstream verfügbar ist:[^5]:^^<br>RTCM 3 MSM5 Stream für Echtzeitanwendungen[^6] | :material-check-bold: |
| Daten müssen nach einem Kommunikationsausfall erneut an die Datenzentren übermittelt werden | :material-check-bold: |
| RINEX-Daten müssen direkt im Empfänger ^^oder^^ aus der nativen Binärdatei generiert werden | :material-check-bold: |
| Ziel für die Dateivollständigkeit | 99% |

### Hochfrequente RINEX-Dateien

| Empfehlung     |             | Klassifizierung |
| -------------- | ------------| --------------- |
| Bereitstellung |             | :fontawesome-solid-triangle-exclamation: |
| Latenz         | < 5 Minuten | :material-check-bold: |
| Abtastrate     | 1 Hz        | :material-check-bold: |
| Dauer          | 15 Minuten  | :material-check-bold: |

### Stündliche RINEX-Dateien

| Empfehlung     | Klassifizierung |
| -------------- | --------------- |
| Bereitstellung      |             | :fontawesome-solid-triangle-exclamation: |
| Latenz        | < 5 Minuten | :material-check-bold: |
| Abtastrate  | 30 Sekunden  | :material-check-bold: |

### Tägliche RINEX-Dateien

| Empfehlung     | Klassifizierung |
| -------------- | --------------- |
| Bereitstellung      |             | :material-check-bold: |
| Latenz        | < 30 Minuten| :material-check-bold: |
| Abtastrate  | 30 Sekunden  | :material-check-bold: |

## Metadaten

| Empfehlung     | Klassifizierung |
| -------------- | --------------- |
| Vollständige und aktuelle Metadaten im IGS Site Log/GeodesyML-Format | :material-check-bold: |
| Eindeutige neunstellige Stationskennung, die vom IGS genehmigt wurde | :material-check-bold: |
| Vergeben mit einer eindeutigen IERS DOMES Nummer | :material-check-bold: |
| Aktualisierung des IGS Site Log innerhalb von 24 Stunden nach Änderungen an der Station | :material-check-bold: |
| RINEX-Header stimmen mit den Informationen im IGS-Metadatensatz überein | :material-check-bold: |
| Bereitstellung von Bildern der Antenneninstallation in den 4 Himmelsrichtungen (N, O, S, W) | :material-check-bold: |

[^1]: Verbindlich für regionale CORS im Einflussbereich von APREF, EPN und SIRGAS.
[^2]: Ausnahmen können nach Überprüfung durch das SPC gewährt werden.
[^3]: Neue Stationen sollen alle verfügbaren Frequenzcodes und Trägerphasen empfangen können.
[^4]: Für neue Stationen: RINEX 3.04 ist die minimal akzeptierte Version. RINEX 2.11 wird nicht akzeptiert.
[^5]: Neue Stationen werden dringend ermutigt, Echtzeitstreams bereitzustellen.
[^6]: MSM7 wird empfohlen.