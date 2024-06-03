Die GNSS-Metadaten enthalten Informationen über die Station, einschließlich Eigentumsverhältnissen, Kontaktdaten, Monumentinformationen, die Standortkoordinaten und eine Historie der installierten Ausrüstung. Zuverlässige und aktuelle Metadaten sind für die Verwaltung und Nutzung einer GNSS-Station von zentraler Bedeutung und liegen in der Verantwortung des Stationsbetreibers.

## IGS Site Log/GeodesyML

Der IGS verlangt, dass CORS ihre Metadaten in einem IGS Site Log (ASCII) oder GeodesyML aufzeichnen und pflegen und dass die Metadaten der IGS und allen Benutzern zur Verfügung gestellt werden. Der IGS verwendet eine [Webanwendung](https://slm.igs.org), um die Stationsmetadaten zu pflegen.

Es ist obligatorisch, dass die Metadaten für alle CORS vervollständigt und veröffentlicht werden, um eine konsistente Methode zur Verteilung relevanter Standortinformationen an Analysezentren und Benutzer bereitzustellen. Ein CORS-Betreiber muss möglicherweise zusätzliche Metadaten für den Standort aufbewahren, um das interne Management und die Betriebsabläufe zu unterstützen.

Alle IGS-Stationen werden anhand einer eindeutigen neunstelligen Abkürzung identifiziert. Die ersten vier Zeichen sollten global eindeutig sein, und der Name wird normalerweise gewählt, um den Vorort, die Stadt oder die Lokalität der Station darzustellen. Der GNSS-Betreiber sollte beim IGS-Netzwerkkoordinator überprüfen, ob der vorgeschlagene vierstellige Bezeichner für ein neues CORS bereits verwendet wird. Darüber hinaus muss jedes IGS-CORS eine [IERS-DOMES-Nummer](domes-request) beantragen. Stellen Sie sicher, dass der beabsichtigte vierstellige Code nicht bereits für andere geodätische Techniken verwendet wurde, indem Sie die [IERS-DOMES-Nummernliste](domes-list) überprüfen.

## RINEX-Header

RINEX-Header müssen mit den in den IGS-Site-Logs aufgezeichneten Metadaten übereinstimmen. RINEX-Dateien müssen bei Abweichungen der Metadaten erneut eingereicht werden. Alle Informationen im RINEX-Header müssen im ASCII-Format kodiert sein. Die Verwendung von Zeichen aus anderen Kodierungsstandards (z. B. UTF-8) kann dazu führen, dass sich die Header-Elemente beim Dekodieren verschieben, z. B. durch die Verwendung von Diakritika. Die folgende Tabelle listet die obligatorischen RINEX-Header-Elemente auf, die für jede RINEX-Datei bereitgestellt werden müssen.

| RINEX-Header-Element  | Empfehlungen | Beispiel |
| --------------------- | --------------- | ------- |
| `MARKER NAME`         | <ul><li>Es wird empfohlen, den neunstelligen Stationscode zu verwenden.</li><li>Alternativ kann der 4-stellige Stationscode verwendet werden.</li><li>Alle Buchstaben müssen in Großbuchstaben angegeben werden.</li></ul> | OUS200NZL<br>OUS2 |
| `MARKER NUMBER`       | IERS-DOMES-Nummer. Alle Buchstaben müssen in Großbuchstaben angegeben werden. | 50212M002 |
| `MARKER TYPE`         | Muss auf GEODETIC gesetzt sein. ||
| `OBSERVER`            | Es wird empfohlen, eine generische E-Mail-Adresse anzugeben. Die maximale Anzahl von Zeichen beträgt 20. | gnss@agency.org |
| `AGENCY`              | Es wird empfohlen, die Organisationsabkürzungen anzugeben, wie sie in den Abschnitten 11 und 12 des IGS-Site-Logs angegeben sind. Wenn mehrere Organisationen aufgeführt sind, sollten sie durch einen Schrägstrich ("/") getrennt werden. Maximale Anzahl von Zeichen beträgt 60. | OUSD/GFZ |
| `REC # / TYPE / VERS` | Alle Empfängerinformationen müssen mit den im IGS-Site-Log angegebenen Metadaten identisch sein. ||
| `ANT # / TYPE`        | Alle Antenneninformationen müssen mit den im IGS-Site-Log angegebenen Metadaten identisch sein. ||
| `APPROX POSITION XYZ` | Die ungefähren Koordinaten müssen mit einer Genauigkeit von 1 m mit denen im IGS-Site-Log angegebenen übereinstimmen. ||
| `ANTENNA: DELTA H/E/N` | Die Antenneneccentricities müssen mit denen im IGS-Site-Log angegebenen übereinstimmen