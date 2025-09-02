Das absolute Minimum, das ein IGS CORS bereitstellen muss, sind tägliche RINEX-Beobachtungsdateien mit einer Abtastrate von 30 Sekunden. Eine Abtastrate von 15 Sekunden ist akzeptabel, aber nicht empfohlen. Darüber hinaus werden die Stationsbetreiber gebeten, RINEX-Navigationsdateien bereitzustellen[^1].

Es wird empfohlen, stündliche RINEX-Dateien mit einer Abtastrate von 30 Sekunden bereitzustellen. Neu vorgeschlagene IGS-Stationen werden ermutigt, stündliche RINEX-Dateien mit einer Abtastrate von 30 Sekunden und hochfrequente (1 Hz) RINEX-Dateien mit einer Dauer von 15 Minuten bereitzustellen, sofern dies möglich ist.

Jede RINEX-Datendatei muss an mindestens zwei der globalen IGS-Datenzentren gesendet werden[^2]. Wenn die Station bereits in ein regionales Netzwerk (z. B. APREF, EPN, SIRGAS) einbezogen ist und die Daten öffentlich verfügbar sind, ist die Übertragung an eines der globalen Datenzentren ausreichend. Die Datenübertragung wird über den IGS-Netzwerkkoordinator koordiniert.

Nach einem Kommunikationsausfall müssen fehlende Datendateien an das Datenzentrum bzw. die Datenzentren gesendet werden. Eine Ankündigung mit Details zum Ausfall muss an die Community gesendet werden (siehe Abschnitt [Ankündigungen](../announcements) für weitere Informationen).

Die folgende Liste hebt Schlüsselzahlen für die Signalverfolgung, Datenaufzeichnung und Datenübertragung hervor, die von jedem IGS-CORS angestrebt werden sollten.

**Signalverfolgung und Datenarchivierung**

- 99% der verfügbaren Epochen an einem Tag sind vollständig erfasst, aufgezeichnet und archiviert (<15 Minuten Ausfall pro Tag).
- 99% der verfügbaren Epochen in einem Jahr sind vollständig erfasst, aufgezeichnet und archiviert (<91 Stunden Gesamtausfall pro Jahr).

**Datenübertragung**

- Die Latenzzeit für eine stündliche Datendatei zur Archivierung sollte <5 Minuten nach Ende jeder Stunde betragen.
- Die Latenzzeit für eine tägliche Datendatei zur Archivierung sollte <30 Minuten nach Ende des Tages betragen.

**Erneute Übermittlung nach einem Ausfall**

- Alle fehlenden täglichen Dateien müssen so schnell wie möglich erneut übermittelt werden.
- Fehlende stündliche Dateien müssen mindestens für die letzten drei vollständigen Tage erneut übermittelt werden.

## Hochfrequenzdaten

Zur Unterstützung von Anwendungen in Echtzeit werden die Stationsbetreiber ermutigt, 15-minütige RINEX-Beobachtungs- und Navigationsdateien mit einer Datenfrequenz von 1 Hz bereitzustellen (falls zutreffend). Diese können entweder aus Echtzeitströmen generiert oder vom Empfänger aufgezeichnet werden.
Die Stationen, die an der Bereitstellung von Hochfrequenzdaten teilnehmen, werden ermutigt, die Dateien mit einer Verzögerung von maximal 5 Minuten ab dem letzten erfassten Beobachtungszeitpunkt bereitzustellen.

## Echtzeitdaten

Neben der Erfüllung der Standards einer herkömmlichen IGS-Station müssen Echtzeitstationen GNSS-Beobachtungsdaten mit einer minimalen Datenintervall von 1 Hz streamen. Alle neu vorgeschlagenen IGS-Stationen müssen in der Lage sein, Daten in Echtzeit zu streamen, es sei denn, sie tragen zum Referenzrahmen bei (z. B. durch Koexistenz mit einer SLR- oder VLBI-Station) oder befinden sich in einer Region mit geografischem Bedarf.
Die Anforderungen, die von einer IGS-Echtzeitstation erfüllt werden müssen, sind in Abschnitt 2 der [Leitlinien für IGS-Echtzeit-Broadcaster und -Stationen](https://files.igs.org/pub/resource/guidelines/Guidelines_for_IGS_Real_Time_Broadcasters_and_Stations.pdf) beschrieben.

## Meteorologische Daten

Es wird empfohlen, präzise meteorologische Ausrüstung an einem IGS-CORS zu installieren. Die spezifischen Richtlinien für Sensoren sind im Abschnitt [Meteorologische Sensoren](../equipment/meteo_sensors.md) dargestellt. Als Minimum müssen die Daten Druck- und Temperaturmessungen enthalten und im RINEX-Format verteilt werden. Die RINEX-Dateien sollten nach dem gleichen Zeitplan wie die RINEX-Beobachtungsdateien (stündlich und/oder täglich) übertragen werden.


[^1]: Um die Anzahl der Dateien zu reduzieren, wird empfohlen, gemischte Navigationsdateien zu senden, die alle Navigationsdaten in einer einzigen Datei enthalten.
[^2]: Eine Liste globaler IGS Datenzentren kann auf der IGS Webseite gefunden werden: [https://igs.org/data-access/#data-centers](https://igs.org/data-access/#data-centers)
