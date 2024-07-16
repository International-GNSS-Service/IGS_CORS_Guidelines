Un étalonnage absolu de l'antenne GNSS de la station doit être disponible dans le [fichier ANTEX actuel de l'IGS](https://files.igs.org/pub/data/format/antex14.txt). Ce fichier contient des étalonnages moyens par modèle d'antenne. Bien que l'utilisation d'étalonnages moyens par type d'antenne soit la norme actuelle dans les analyses de l'IGS, il est préférable d'étalonner également individuellement chaque antenne utilisée dans le réseau IGS. Il est recommandé que les nouvelles antennes soient étalonnées à l'aide d'un robot ou dans une chambre anéchoïque. Pour que l'étalonnage de l'antenne puisse être utilisé, celle-ci doit être orientée vers le nord géographique avec une précision de ±5°. Les modèles d'antenne disposant d'un étalonnage relatif ne doivent pas être utilisés.

L'antenne GNSS doit être fixée de manière rigide et sécurisée au sommet du monument de la station comme décrit dans la Section [Stabilité du Site](../../establishment/stability).

L'excentricité entre le point géodésique et le point de référence de l'antenne (ARP) doit être mesurée avec une précision ≤ 1 mm et fournie dans le site log de la station et les en-têtes de ses fichiers RINEX ; une excentricité horizontale nulle est préférable.

L'utilisation d'antennes choke-ring est recommandée. Elles sont en effet très bien caractérisées et permettent une forte atténuation des multi-trajets.

L'utilisation de radômes de protection est déconseillée. Bien qu'ils offrent un certain niveau de protection contre les intempéries, les radômes modifient l'emplacement du centre de phase de l'antenne (APC). Qui plus est, la lumière ultraviolette affecte les propriétés du matériau du radôme, de sorte que son impact sur l'emplacement de l'APC varie au fil du temps. Cependant, les conditions environnementales telles que les chutes de neige, les embruns marins, ou la probabilité que l'antenne puisse être utilisée comme perchoir pour les oiseaux, peuvent nécessiter l'utilisation d'un radôme. Dans ce cas, la combinaison antenne/radôme doit disposer d'un étalonnage absolu dans le fichier ANTEX actuel de l'IGS. Les radômes coniques ne doivent pas être utilisés. Ne retirez pas les radômes des antennes GNSS existantes.

L'expérience montre que lorsqu'une antenne GNSS est retirée et remplacée, la position calculée de la station change, même lorsque l'ARP est remplacé avec précision au même endroit. Par conséquent, ne retirez jamais une antenne pour une raison autre qu'une panne matérielle ou pour mesurer un rattachement de la station à d'autres points géodésiques. Tout retrait d'antenne doit être signalé dans le site log de la station. Si vous devez changer d'antenne, les utilisateurs et les centres d'analyse de l'IGS doivent être prévenus (voir la section [Annonces](../../data/announcements)).

Choisissez une antenne capable de suivre autant de signaux GNSS prévus que possible afin d'éviter de devoir remplacer l'antenne pour suivre les signaux GNSS nouvellement disponibles. Pour éviter toute confusion, la dénomination IGS standard des [modèles d'antennes](https://files.igs.org/pub/station/general/rcvr_ant.tab) doit être utilisée dans les en-têtes des fichiers RINEX et les métadonnées de la station.

### Type d'Antenne

- L'utilisation d'antennes de type non répertorié par l'IGS n'est pas autorisée. Utilisez de préférence des antennes choke-ring avec des éléments Dorne-Margolin.
- Les capacités de l'antenne en termes de suivi des signaux GNSS doivent correspondre ou dépasser celles du récepteur. Pour les nouvelles stations, cette exigence est obligatoire.
- L'antenne et ses connecteurs doivent être résistants aux intempéries et à la corrosion.

### Étalonnages

- Toutes les antennes IGS doivent disposer d'un étalonnage absolu dans le fichier ANTEX actuel de l'IGS. Si une antenne est étalonnée individuellement, le fichier ANTEX correspondant doit être mis à disposition de l'IGS.
- Les antennes doivent être calibrées soit par un robot soit en chambre anéchoïque.

### ARP et Excentricité

- Toutes les mesures de décalage d'antenne doivent se référer à l'ARP.
- L'excentricité entre le point géodésique et l'ARP doit être mesurée selon les directions Est, Nord, verticale avec une précision ≤ 1 mm et fournie dans le site log de la station et les en-têtes de ses fichiers RINEX.

### Radôme

- L'utilisation d'un radôme est fortement déconseillée.
- Si l'utilisation d'un radôme est absolument nécessaire, il est recommandé d'utiliser un radôme hémisphérique tel que la combinaison antenne+radôme dispose d'un étalonnage absolu dans le fichier ANTEX actuel de l'IGS.
- Ne pas utiliser de radômes coniques.

### Orientation de l'Antenne

- L'antenne doit être orientée vers le nord géographique avec une précision de ±5°.
- Si l'écart est supérieur à 5°, l'orientation réelle de l'antenne doit être donnée dans les métadonnées de la station.
