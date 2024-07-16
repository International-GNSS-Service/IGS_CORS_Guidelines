L'IGS prend actuellement en charge trois versions majeures du format RINEX : RINEX v.2, RINEX v.3 et RINEX v.4. Chaque opérateur de station est encouragé à transmettre ses données dans la dernière version disponible du format RINEX. Les CORS IGS nouvellement proposés doivent soumettre leurs données au minimum dans le format RINEX 3.04.

## RINEX v.4/v.3

Les fichiers au format [RINEX v.3](https://files.igs.org/pub/data/format/rinex305.pdf) ou [RINEX v.4](https://files.igs.org/pub/data/format/rinex_4.01.pdf) doivent être transmis avec les dénominations suivantes :

*Fichiers d’Observation et Fichiers Météorologiques*

`SSSSMRCCC_S_YYYYDDDHHMM_DDU_FRU_DT.fff.cmp`

*Fichiers de Navigation*

`SSSSMRCCC_S_YYYYDDDHHMM_DDU_DT.fff.cmp`

Tous les éléments de la première partie du nom de fichier doivent contenir des lettres ou des chiffres ASCII majuscules. Ces éléments sont de longueur fixe et séparés par un tiret bas « _ ». Les champs de type de fichier (fff) et de compression (cmp) sont séparés par des points « . » et doivent contenir des caractères ASCII minuscules. Chaque champ doit être complété, si nécessaire, par des zéros de sorte à occuper le nombre prévu de caractères (voir Tableau ci-dessous).

Afin de réduire la taille des fichiers d'observation, la compression Hatanaka doit être utilisée. Pour plus d'informations, se référer à [https://terras.gsi.go.jp/ja/crx2rnx.html](https://terras.gsi.go.jp/ja/crx2rnx.html).

=== "SSSSMRCCC"
    Nom de la Station IGS sur 9 Caractères

    - SSSS : identifiant de station à 4 caractères
    - M : numéro de point géodésique (0-9)
    - R : numéro de récepteur (0-9)
    - CCC : code de pays ou de région ISO-3166 (alpha-3)
    
    Example: POTS00DEU.

    Par souci de compatibilité avec le format SINEX, les numéros de point géodésique autres que 0 ne sont actuellement pas acceptés.
                                                                                                                                                                   |
=== "S"
    Source des Données

    Sont autorisés : R (données issues du récepteur via le logiciel constructeur ou un autre logiciel) ou S (données issues d’un flux RTCM ou dans un autre format)

=== "YYYYDDDHHMM"

    Date de Début

    - YYYY : année grégorienne (e.g., 2024)
    - DDD : jour de l’année (001-366, e.g., 260)
    - HHMM : heure et minute (0000-2359, e.g., 1000)

    Il est préférable d'utiliser l'heure nominale de début du fichier, mais acceptable d’utiliser l'heure de début réelle des données.

=== "DDU"
    Durée du Fichier

    - DD : Durée du fichier
    - U : Unité de durée
    - Sont acceptés : 15M, 01H, 01D

=== "FRU"
    Fréquence des Données

    - FR : Fréquence des données
    - U : Unité de fréquence
    - Sont acceptés : 01S pour les données haute fréquence et 30S ou 15S pour les données horaires et journalières
    
    Ce champ n’est pas requis pour les fichiers RINEX de navigation.

=== "DT"
    Type de Données

    - D : Système GNSS (sont autorisés : G, R, E, C,J, S, I et M(ixte))
    - T : Type de fichier RINEX (sont autorisés : O, N, M)

    Exemple : MO.

=== "fff"
    Format du Fichier
    
    - Sont autorisés : rnx (RINEX) and crx (RINEX compressé).
    
=== "cmp"
    Format de Compression
    
    - Seul gzip (gz) est autorisé.

## RINEX v.2

Les fichiers au format RINEX v.2 (Gurtner, 2007) doivent être transmis avec la dénomination suivante :

`ssssdddf.yyt`

Le Tableau ci-dessous décrit les différents éléments de cette dénomination. Les stations transmettant des fichiers RINEX v.2 sont encouragées à fournir des fichiers compressés à l’aide de gzip. Si les fichiers sont envoyés en compression Z, les centres de données IGS les recompresseront et les rendront accessibles en compression gzip (Romero & Ruddick, IGS, 2020).

=== "ssss"
    Nom de la Station IGS sur 4 Caractères

    Exemple : pots.

=== "ddd"
    Jour de l’année de la première observation (001-366).

    Exemple : 260.

=== "f"
    Durée du Fichier
    
    - Fichiers journaliers (30 seconds) : f=0
    - Fichiers horaires (30 seconds) : 
        - f=a (00:00:00 to 00:59:30), 
        - f=b (01:00:00 to 01:59:30), 
        - ...
        - f=x (23:00:00 to 23:59:30)
    - Fichiers haute-fréquence (15M, 1 Hz):
        - f=a00 (00:00:00 to 00:14:59)
        - f=a15 (00:15:00 to 00:29:59)
        - ...
        - f=m30 (12:30:00 to 12:44:59)
        - ...
        - f=x45 (23:45:00 to 23:59:59)
    
=== "yy"
    Année (sur 2 chiffres, e.g., 24).

=== "t"
    Type de fichier.
    
    Sont autorisés :
    
    - O : Fichier d’observation
    - D : Fichier d’observation en compression Hatanaka
    - N : Fichier de navigation GPS
    - G : Fichier de navigation GLONASS
    - M : Fichier météorologique