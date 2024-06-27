Les métadonnées sont des informations sur le site CORS concernant le propriétaire du site, ses coordonnées, la monumentation du site, sa localisation et l’historique des équipements installés. Des métadonnées fiables et à jour sont essentielles à la gestion et à l'utilisation d'une station GNSS et relèvent de la responsabilité de l'opérateur de la station.

## Site Log IGS / GeodesyML

L'IGS exige que chaque opérateur de station renseigne ces métadonnées dans un fichier site log IGS (ASCII) ou au format GeodesyML, et que les métadonnées soient mises à la disposition de l'IGS et de l’ensemble des utilisateurs. L'IGS utilise une [application web](https://slm.igs.org) pour gérer les métadonnées des stations.

Il est impératif que les métadonnées de toutes les CORS IGS soient complètes et publiques de sorte que les centres d’analyse IGS et autres utilisateurs puissent aisément accéder aux informations qui leur sont nécessaires. Un opérateur de CORS peut avoir à fournir des métadonnées supplémentaires à propos du site afin de faciliter son opération et sa maintenance.

Toutes les stations IGS sont identifiées par un code unique à neuf caractères. Les quatre premiers caractères de ce code doivent eux-mêmes constituer un identifiant unique, qui se réfère généralement à la ville ou localité où se trouve le site. Pour chaque nouvelle station, l'opérateur doit vérifier auprès du coordinateur du réseau IGS que l'identifiant à quatre caractères prévu n'est pas déjà utilisé. De plus, chaque nouvelle CORS IGS doit être demander l'affectation d’un [numéro DOMES IERS](domes-request). Assurez-vous que le code à quatre caractères prévu n'a pas déjà été utilisé pour d'autres techniques géodésiques en consultant [la liste des numéros DOMES](domes-list).

## En-Têtes des Fichiers RINEX

Les en-têtes des fichiers RINEX doivent correspondre aux métadonnées renseignées dans le site log IGS. Les fichiers RINEX doivent être soumis à nouveau en cas de divergence dans les métadonnées. Toutes les informations contenues dans les en-têtes des fichiers RINEX doivent être codées en ASCII. L'utilisation de caractères provenant d'autres normes de codage (par exemple des signes diacritiques codés en UTF-8) peut conduire à un décalage des éléments d'en-tête lors du décodage. Le Tableau ci-dessous répertorie les éléments d'en-tête devant être obligatoirement présents dans chaque fichier RINEX.

| RINEX Header Element  | Recommendations | Example |
| --------------------- | --------------- | ------- |
| `MARKER NAME`         | <ul><li>Il est recommandé de renseigner l’identifiant à 9 caractères de la station.</li><li>L’identifiant à 4 caractère de la station peut également être utilisé.</li><li>Toutes les lettres doivent être en majuscules.</li></ul> | OUS200NZL<br>OUS2 |
| `MARKER NUMBER`       | Numéro DOMES IERS. Toutes les lettres doivent être en majuscules. | 50212M002 |
| `MARKER TYPE`         | Doit être : GEODETIC. ||
| `OBSERVER`            | Il est recommandé de fournir une adresse email générique. Le nombre maximum de caractères est de 20. | gnss@agency.org |
| `AGENCY`              | Il est recommandé de renseigner l’abréviation du nom de l’organisme telle qu’indiquée dans les sections 11 et 12 du site log IGS de la station. Si plusieurs organismes sont répertoriés, ils doivent être séparés par une barre oblique (« / »). Le nombre maximum de caractères est de 60. | OUSD/GFZ |
| `REC # / TYPE / VERS` | Toutes les informations sur le récepteur doivent être identiques aux métadonnées renseignées dans le site log IGS de la station. ||
| `ANT # / TYPE`        | Toutes les informations sur l’antenne doivent être identiques aux métadonnées renseignées dans le site log IGS de la station. ||
| `APPROX POSITION XYZ` | Les coordonnées approchées doivent correspondre à mieux que 1 m avec celles renseignées dans le site log IGS de la station. ||
| `ANTENNA: DELTA H/E/N` | L’excentricité de l’antenne doit être identique à celle renseignée dans le site log IGS de la station. ||

## Photographies Numériques

Chaque CORS IGS doit fournir des photographies de l'installation de l'antenne dans les quatre directions cardinales (de préférence 8 photographies séparées de 45° en azimuth), du monument et de ses environs. Les photographies doivent être mises à jour après chaque événement ou changement d’équipement.

Les photographies doivent être nommées de la façon suivante :
`SSSSMRCCC_YYYYMMDD_D[D].fff`

Le Tableau ci-dessous explicite les différents éléments de cette dénomination. Ces éléments doivent être séparés par des tirets bas (“_”).

| Component   | Description | Example |
| ----------- | ----------- | ------- |
| `SSSSMRCCC` | L’identifiant à 9 caractères de la station. | NYA200NOR |
| `YYYYMMDD`  | Date de prise de vue (année, mois, jour), sans séparation. | 20210131 |
| `D[D]`      | <ul><li>Direction cardinale : N, E, S, W ou une combinaison de deux de ces caractères</li><li>Numéro de série de l’antenne : AS</li><li>Support d’antenne : AM</li><li>Récepteur : R</li><li>Monument : M</li></ul> | N (Nord)<br>SE (Sud-Est) |
| `fff`       | Format de la photographie. Sont acceptés : JPEG et PNG. | .jpg |

Les photos peuvent être également être mises à disposition sur un site web hébergé par l'opérateur de la station ou son organisme.

## Étalonnages Individuels d’Antennes

Bien que cela ne soit pas obligatoire, il est recommandé de fournir un étalonnage individuel pour chaque antenne installée sur une CORS IGS. Les étalonnages individuels sont utiles pour les travaux de différents Composants de l'IGS, tel que l’Antenna Committee. Le fichier ANTEX correspondant devra être mis à disposition du coordinateur du réseau IGS.

## Protection des Données

L'Union Européenne et d'autres pays ont mis en œuvre des réglementations sur la protection des données personnelles. L’IGS étant une fédération volontaire sans représentation juridique, il n’est pas dans son intérêt de s’occuper des subtilités qui viennent avec chacune de ces réglementations.
Nous demandons donc que toutes les informations personnelles contenues dans les métadonnées (site logs IGS/GeodesyML) et les en-têtes des fichiers RINEX (noms complets et adresses e-mail) soient remplacées par des noms génériques et des listes de diffusion, par exemple :

- Site logs IGS / GeodesyML :
    - Contact Name: “Agency” Network operator
    - E-Mail: gnss@agency.org
- En-Tête de Fichier RINEX :
    - Observer: gnss@agency.org
    - Comments with disclaimer information

Les stations proposées à l'IGS devront se conformer à ces règles pour être acceptées. Les opérateurs qui mettent à jour les métadonnées de leurs stations sont également invités à utiliser des coordonnées conformes à la protection des données.

[domes-request]: https://itrf.ign.fr/en/network/domes/request
[domes-list]: https://itrf.ign.fr/en/network/list