Die GNSS-Antennenkalibrierung der Station muss im aktuellen [IGS ANTEX-Format](https://files.igs.org/pub/data/format/antex14.txt) verfügbar sein. Diese Datei enthält modellspezifische Antennenkalibrierungen. Obwohl die Verwendung von Typmittelwert-Kalibrierungen der aktuelle Standard in der IGS-Analyse ist, wird empfohlen, jede im IGS-Netzwerk verwendete GNSS-Antenne individuell zu kalibrieren. Es wird empfohlen, dass neue Antennen entweder durch einen Roboter oder in einer Kammer kalibriert werden. Damit die Antennenkalibrierungen gültig sind, muss die GNSS-Antenne mit einer Genauigkeit von ±5° nach Norden ausgerichtet sein. Relative Antennenkalibrierungsmodelle sollten nicht verwendet werden.

Die GNSS-Antenne muss fest und sicher an der Spitze des Stationsmonuments befestigt sein, wie im Abschnitt [Standortstabilität](../../establishment/stability) beschrieben.

Exzentrizitäten zwischen dem Marker und dem Antennenreferenzpunkt (ARP) müssen vermessen und in den IGS-Standortprotokollen und RINEX-Headern mit einer Genauigkeit von ≤1 mm angegeben werden; eine horizontale Exzentrizität von 0 m wird bevorzugt.

Die Verwendung von Choke-Ring-Antennen wird empfohlen. Sie haben sehr stabile und gut verstandene Eigenschaften und bieten eine hohe Mehrwegeunterdrückung.

Die Verwendung von Radomen wird nicht empfohlen. Obwohl sie einen gewissen Schutz vor Witterungseinflüssen bieten, verändern Radome die Lage des Antennenphasenmittelpunkts (APC). Noch schlimmer ist, dass sich die Auswirkungen auf die APC-Lage ändern, da ultraviolettes Licht die Eigenschaften des Radommaterials beeinflusst. Unter bestimmten Umweltbedingungen wie Schneefall, Meeresgischt oder der Wahrscheinlichkeit, dass die Antenne als Sitzplatz für Vögel genutzt wird, kann die Verwendung eines Radoms erforderlich sein. In diesem Fall muss die Kombination aus Antenne und Radom eine gültige Antennenkalibrierung aufweisen. Konische Radome sollten nicht verwendet werden. Entfernen Sie keine Radome von bestehenden GNSS-Antennen.

Erfahrungen zeigen, dass beim Entfernen und Wiederanbringen einer GNSS-Antenne eine Änderung der berechneten Position der Station auftritt, selbst wenn der ARP genau ersetzt wird. Daher sollte die Antenne nur bei Hardwareausfällen oder zur Durchführung notwendiger lokaler Vermessungen entfernt werden. Für letzteres muss dies zwingend in den Stationsmetadaten reflektiert werden. Wenn Sie die Antenne wechseln müssen, sollen Benutzer und Analysezentren im Voraus informiert werden (siehe Abschnitt [Ankündigungen](../../data/announcements)).

Wählen Sie Antennen, die zum Zeitpunkt des Kaufs so viele geplante GNSS-Signale wie möglich empfangen können, um die Notwendigkeit zu verringern, eine Antenne zu entfernen, um neu verfügbare GNSS-Signale zu verfolgen. Um Verwirrung zu vermeiden, muss die IGS-Standard-Namenskonvention für [Antennenmodelle](https://files.igs.org/pub/station/general/rcvr_ant.tab) in den RINEX-Headern und Metadaten verwendet werden.

### Antennentyp

Die Verwendung von einzigartigen („unbekannten“) Antennen ist nicht gestattet. Die Verwendung von Choke-Ring-Antennen mit Dorne-Margolin-Elementen wird bevorzugt.
Die Fähigkeit der Antenne, Satellitensignale zu empfangen, sollte mindestens der des GNSS-Empfängers entsprechen. Für neue Stationen ist diese Anforderung zwingend.
Die Antenne und die Antennenanschlüsse müssen wetterfest und korrosionsbeständig sein.

### Kalibrierungen

Alle IGS-Antennen müssen eine gültige IGS-Absolutantennenkalibrierung aufweisen. Wenn eine Antenne individuell kalibriert wird, sollte die entsprechende ANTEX-Datei dem IGS zur Verfügung gestellt werden. Antennen sollten entweder durch Roboter oder in einer Kammer kalibriert werden.

### Antennenreferenzpunkt und Exzentrizitäten

Alle Antennenversatzmessungen müssen sich auf den Antennenreferenzpunkt (ARP) beziehen. Exzentrizitäten (Ost, Nord, Hoch) vom permanenten Positionsmarker zum ARP müssen mit einer Genauigkeit von ≤1 mm in den Metadaten und RINEX-Headern vermessen und angegeben werden.

### Radom

Die Verwendung eines Radoms wird dringend abgeraten. Wenn die Verwendung eines Radoms absolut notwendig ist, wird die Verwendung eines halbkugelförmigen Radoms mit einer gültigen Absolutantennenkalibrierung empfohlen.
Verwenden Sie keine konischen Radome.

### Antennenausrichtung

Die Antenne muss mit einer Genauigkeit von ±5° nach Norden ausgerichtet sein.
Wenn die Abweichung größer als 5° ist, muss die tatsächliche Ausrichtung in den Metadaten vermerkt werden.