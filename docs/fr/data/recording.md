Une CORS IGS doit fournir au strict minimum des fichiers RINEX d'observation journaliers avec un taux d'échantillonnage de 30 secondes. Un taux d'échantillonnage de 15 secondes est acceptable mais pas encouragé. Il est également demandé aux opérateurs de stations de fournir les fichiers RINEX de navigation[^1].

Il est recommandé de fournir également des fichiers RINEX horaires avec un taux d'échantillonnage de 30 secondes. Les stations IGS nouvellement proposées sont de plus encouragées à fournir, si possible, des fichiers RINEX à haute fréquence (1 Hz) d'une durée de 15 minutes.

Chaque fichier RINEX doit être envoyé à au moins deux des centres de données mondiaux de l'IGS[^2]. Si la station fait déjà partie d'un réseau régional (par exemple APREF, EPN, SIRGAS) et que les données sont accessibles au public, la transmission vers un seul des centres de données mondiaux est suffisante. La transmission des données sera coordonnée par le coordinateur du réseau IGS.

Après une interruption de communication, les fichiers de données manquants doivent être soumis au(x) centre(s) de données. Une annonce expliquant les détails de la panne devra être envoyée à la communauté (voir la section [Annonces](../announcements) pour plus d'informations).

Les listes ci-dessous résument les critères devant être satisfaits par une CORS IGS en termes de suivi des signaux GNSS et d'enregistrement et de transmission des données.

**Suivi des Signaux et Archivage des Données**

- Au moins 99 % des données disponibles au cours d'une journée doivent être entièrement observées, enregistrées et archivées (<15 minutes de données manquantes par jour).
- Au moins 99 % des données disponibles au cours d'une année doivent être entièrement observées, enregistrées et archivées (<91 heures de données manquantes par année).

**Transmission des Données**

- La latence d'archivage d'un fichier de données horaire doit être <5 minutes après la fin de chaque heure.
- La latence d'archivage d'un fichier de données journalier doit être <30 minutes après la fin de chaque jour.

**Retransmission après une Panne**

- Tous les fichiers journaliers manquants doivent être retransmis aussitôt que possible.
- Les fichiers horaires manquants doivent être retransmis au minimum pour les trois derniers jours.

## Données Haute Fréquence

En appui aux applications en temps quasi réel (NRT), les opérateurs de stations sont encouragés à fournir des fichiers RINEX d'observation et de navigation d’une durée de 15 minutes avec une fréquence d’échantillonnage de 1 Hz. Ceux-ci peuvent être soit générés à partir d’un flux en temps réel, soit enregistrés par le récepteur.

Les stations fournissant des données haute fréquence sont encouragées à fournir les fichiers avec un délai de moins de 5 minutes après la dernière époque d'observation enregistrée.

## Données en Temps Réel

En plus de répondre aux normes d'une station IGS conventionnelle, les stations temps réel doivent diffuser des données d'observation GNSS avec une fréquence minimum de 1 Hz. Toutes les stations IGS nouvellement proposées doivent être capables de diffuser des données en temps réel, à moins qu'elles ne soient considérées comme utiles au repère de référence terrestre (par exemple, en étant colocalisées avec une station SLR ou VLBI) ou qu'elles soient situées dans une région peu couverte par le réseau IGS.

Les spécifications devant être respectées par une station IGS temps réel sont décrites dans la section 2 des « [Guidelines for IGS Real-Time Broadcasters and Stations](https://files.igs.org/pub/resource/guidelines/Guidelines-for-IGS-Real-Time-Broadcasters-and-Stations_v1.0.pdf) ».

## Données Météorologiques

Il est recommandé d’installer des capteurs météorologiques précis sur les sites CORS IGS. Les directives relatives aux capteurs météorologiques sont décrites dans la section 4.4. Au minimum, les données doivent inclure des mesures de pression et de température et doivent être distribuées au format RINEX. Les fichiers RINEX météorologiques doivent être transmis selon le même calendrier que les fichiers RINEX d'observation (horaires et/ou journaliers).

[^1]: Pour réduire le nombre de fichiers, il est recommandé de fournir des fichiers de navigation mixtes contenant l’ensemble des données de navigation.
[^2]: Une liste des centres de données mondiaux de l’IGS peut être trouvée sur le site web de l’IGS : [https://igs.org/data-access/#data-centers](https://igs.org/data-access/#data-centers).