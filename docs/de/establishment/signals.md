Die Qualität eines Satellitensignals, das an einer GNSS-Antenne ankommt, hat einen entscheidenden Einfluss auf die Leistung einer GNSS-Station. Es gibt verschiedene Faktoren, die die Signalqualität beeinflussen können, die in den folgenden Abschnitten beschrieben werden.

## Himmelsichtbarkeit

GNSS-Stationen sollten an Standorten mit minimalen Hindernissen über dem lokalen Horizont platziert werden. Oberhalb von 10° Elevation sollten keine Hindernisse vorhanden sein. Der Empfänger soll so eingestellt sein, dass er alle Satelliten innerhalb einer Elevationsmaske von 0° verfolgt.

## Mehrwegeempfang (Multipath)

Interferenzen durch Mehrwegeempfang treten auf, wenn ein GNSS-Satellitensignal auf verschiedenen Wegen zur Antenne gelangt. Das Signal kommt einmal direkt vom Satelliten und zusätzlich durch Reflexion von anderen Oberflächen an.

Mehrwegequellen können entweder natürlich oder künstlich sein. Tabelle 2 listet mögliche Quellen auf, die starken Mehrwegeempfang erzeugen können.

**Künstliche Quellen:**

- Metallplatten und Schilder
- Dächer
- Wände von Gebäuden
- Drahtzäune
- Solarpaneele

**Natürliche Quellen:**

- Bäume (besonders nasse)
- Wasseroberflächen wie Seen, Flüsse usw.

Diese reflektierenden Körper sollten jederzeit von GNSS-Standorten ferngehalten werden. Vermutete Quellen für Mehrwegeempfang sollten mindestens 20 Meter von der GNSS-Antenne entfernt und unter 5° Elevation liegen.

## Quellen für Funkstörungen (RFI)

Häufige Quellen für Funkfrequenzstörungen (RFI) umfassen:

- Radio-, Fernseh- und Mobilfunksender,
- Mikrowellen-Datenverbindungen,
- Stromleitungen,
- Transformatoren.

Richtfunksender, insbesondere Mikrowellen-Datenverbindungen, die auf den CORS-Standort gerichtet sind, können erhebliche RFI verursachen. Unter anderen Parametern ist die Wirkung von RFI eine Funktion der Frequenz, der abgestrahlten Leistung und der Entfernung zur Quelle. Die Wirkung von RFI wird erheblich verstärkt, wenn die RFI eine Harmonische einer GNSS-Signalfrequenz ist.

Daher ist es schwierig, einen sicheren Betriebsabstand von einer RFI-Quelle zu definieren. RFI kann schwer zu bestätigen sein, und es kann notwendig sein, fachkundigen Rat einzuholen, wenn RFI vermutet wird. Wenn RFI bestätigt wird und an einem vorgeschlagenen CORS-Standort nicht gemindert werden kann, sollte ein alternativer CORS-Standort in Betracht gezogen werden.

!!! note "Hinweis"

    RFI-Quellen beeinträchtigen nicht nur die an der Antenne empfangenen GNSS-Signale, sondern auch die drahtlose (Radio- oder Mobilfunknetz-) Übertragung von Standortdaten. Wenn ein CORS-Standort Daten über eine Funkverbindung überträgt, kann die Funkübertragung selbst eine RFI-Quelle für die GNSS-Signale an der Antenne sein.

Vor der endgültigen Installation eines Monuments wird empfohlen, die Umgebung auf Mehrwegeempfang zu testen und zu überprüfen, ob RFI-Quellen am GNSS-Standort vorhanden sind. Dies kann durch die Installation der GNSS-Ausrüstung auf einem temporären Stativ und die Untersuchung der Datenqualität erfolgen.