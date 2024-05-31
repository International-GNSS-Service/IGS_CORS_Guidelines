Der IGS unterstützt derzeit drei Hauptversionen des RINEX-Standards, RINEX v.2, RINEX v.3 und RINEX v.4. Jeder Stationsbetreiber wird ermutigt, die neueste verfügbare Haupt- oder Nebenversion zu übertragen. Neu vorgeschlagene IGS CORS müssen ihre Daten mindestens in RINEX 3.04 übermitteln.

## RINEX v.4/v.3

[RINEX v.3](https://files.igs.org/pub/data/format/rinex305.pdf) und [RINEX v.4](https://files.igs.org/pub/data/format/rinex_4.01.pdf) Daten müssen gemäß der folgenden Dateinamenskonvention übertragen werden:

*Beobachtungs- und meteorologische Dateien*

`SSSSMRCCC_S_YYYYDDDHHMM_DDU_FRU_DT.fff.cmp`

*Navigationsdateien*

`SSSSMRCCC_S_YYYYDDDHHMM_DDU_DT.fff.cmp`

Alle Elemente des Dateinamens müssen aus Großbuchstaben oder Zahlen bestehen und durch einen Unterstrich "_" getrennt sein. Die Dateityp- und Kompressionsfelder (Erweiterung) verwenden einen Punkt "." als Trennzeichen und müssen aus Kleinbuchstaben bestehen. Die Felder müssen mit Nullen aufgefüllt werden, um die Feldbreite zu füllen.
Um die Größe der Beobachtungsdateien weiter zu reduzieren, sollte das [Hatanaka-Komprimierungstoolkit](https://terras.gsi.go.jp/ja/crx2rnx.html) verwendet werden.

=== "SSSSMRCCC"
    Der neunstellige IGS-Station Name

    - SSSS: 4-stelliger (vorhandener) IGS-Station Name
    - M: Monument- oder Markierungsnummer (0-9)
    - R: Empfängernummer (0-9)
    - CCC: ISO-3166 Länder- oder Regionencode (alpha-3)
    
    Beispiel: POTS00DEU

    Hinweis: Zur Anpassung an das SINEX-Format werden derzeit Marker- und Monumentnummern außer 0 nicht unterstützt.

=== "S"
    Datenquelle

    Unterstützt werden R (von Empfänger unter Verwendung von Hersteller- oder anderer Software) und S (RTCM oder ein anderes Stream-Format).

=== "YYYYDDDHHMM"

    Startzeit

    - YYYY: Gregorianisches Jahr (z. B. 2024)
    - DDD: Tag des Jahres (z. B. 260)
    - HHMM: Stunden und Minuten des Tages (z. B. 1000)

    Es wird bevorzugt, die nominale Startzeit der Datei zu verwenden. Die Verwendung der tatsächlichen Startzeit einer Datei ist jedoch akzeptabel.

=== "DDU"
    Dateiperiode

    - DD: Dateiperiode
    - U: Einheit der Dateiperiode
    - Akzeptiert werden 15M, 01H, 01D

=== "FRU"
    Datenfrequenz

    - FR: Datenfrequenz
    - U: Einheit der Datenfrequenz
    - Akzeptiert werden 01S für Hochfrequenzdaten und 30S oder 15S für stündliche/tägliche Daten

    Für RINEX-Navigationsdateien nicht erforderlich.

=== "DT"
    Datentyp

    - Zwei Zeichen repräsentieren den Typ
    - D: Satellitensystem (erlaubt sind G, R, E, C, J, S, I und M(ixed))
    - T: RINEX Dateityp (erlaubt sind O, N, M)

    Beispiel: MO

=== "fff"
    Dateiformat. Unterstützt werden rnx (RINEX) und crx (komprimiertes RINEX).

=== "cmp"
    Kompressionsformat. Unterstützt wird gzip (gz).

## RINEX v.2

RINEX v.2 (Gurtner, 2007) Daten müssen gemäß der folgenden Dateinamenskonvention übertragen werden:

`ssssdddf.yyt`

Die Tabelle unten beschreibt jedes Element dieser Dateinamenskonvention. Stationen, die RINEX v.2-Dateien übertragen, werden ermutigt, komprimierte gzip-Dateien bereitzustellen. Auch wenn Dateien in Z-Komprimierung gesendet werden, werden sie von IGS-Datenzentren erneut komprimiert und öffentlich verfügbar gemacht, indem sie gzip verwenden.


=== "ssss"
    Der 4-stellige IGS-Station Name

    Beispiel: pots

=== "ddd"
    Tag des Jahres des ersten Datensatzes

    Beispiel: 260

=== "f"
    Dateisequenznummer/-zeichen innerhalb des Tages
    
    - Tägliche Dateien (30 Sekunden): f=0
    - Stündliche Dateien (30 Sekunden):
        - f=a (00:00:00 bis 00:59:30),
        - f=b (01:00:00 bis 01: