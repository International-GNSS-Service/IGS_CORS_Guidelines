La qualité du signal provenant d'un satellite et étant reçu par une antenne GNSS a un impact crucial sur la performance de ladite station. Les facteurs pouvant influencer la qualité du signal sont listés dans les sections suivantes.

## Visibilité du Ciel

Les stations GNSS doivent être installées sur des sites permettant une visibilité du ciel la moins obstruée possible. Au-dessus de 10° d'élévation, le ciel de la station ne doit contenir aucun masque. Le récepteur doit être configuré pour recevoir les signaux de tous les satellites, avec un angle de coupure réglé à 0° (voir aussi la Section 4.1).

## Multi-Trajets

Les multi-trajets désignent l'interférence qui se produit quand un même signal GNSS arrive à une antenne en ayant suivi plusieurs chemins. Le même signal peut en effet arriver directement du satellite, mais aussi avoir été réfléchi par certaines surfaces aux alentours de l'antenne.

Les sources de multi-trajets peuvent être naturelles ou artificielles. On liste ci-dessous les sources dont on sait qu'elles peuvent générer des multi-trajets importants.

Sources Artificielles :

- Panneaux en Métal
- Toits
- Murs de Bâtiments
- Clôtures en Métal
- Panneaux Solaires

Sources Naturelles :

- Arbres (en particulier en cas d'humidité)
- Plans d'Eau (lacs, rivières, etc.)

Il est impératif de n'avoir aucun de ces éléments proches d'une station GNSS, afin d'éviter les réflexions pouvant générer des multi-trajets. Les sources pouvant générer des multi-trajets doivent être éloignées à plus de 20 mètres de l'antenne GNSS et situées sous 5° d'élévation.

## Sources d'Interférences de Radiofréquences (RFIs)

Les sources pouvant causer des interférences de radiofréquences (RFIs) peuvent être, par exemple :

- des émetteurs radio, de télévision, et pour téléphones mobiles, 
- des flux de données micro-ondes,
- des lignes électriques, ou
- des transformateurs électriques.

Les transmetteurs directionnels, en particulier les transferts micro-ondes pointant dans la direction du site, peuvent causer des RFIs importantes. Les effets des RFIs sont fonction de divers paramètres dont la fréquence, la puissance émise et la distance à la source. Les effets des RFIs sont particulièrement importants quand leur source émet à une harmonique d'une fréquence porteuse d'un signal GNSS.

Par conséquent, il est difficile de définir un critère de distance minimale par rapport à une source de RFIs. Il peut être compliqué de confirmer la présence de RFIs dans un signal enregistré, et l'avis d'un spécialiste peut être nécessaire si des RFIs sont suspectées. Si des RFIs sont confirmées sur un site envisagé pour une nouvelle stations GNSS permanente, et ne peuvent pas être atténuées, alors un autre site devra être considéré.

!!! note "Note"

Les sources de RFI n'affectent pas seulement les signaux GNSS, mais aussi les réseaux sans fil, notamment ceux utilisés pour la transmission de données (via radio ou réseau de télécommunication). De plus, quand le site transmet ses données via radio, la transmission elle-même peut être une source de RFIs sur les signaux GNSS.

Avant l'installation d'un monument permanent, il est recommandé de tester l'environnement en termes de multi-trajets, et de vérifier si des sources de RFIs sont présentes sur le site. Pour ce faire, on pourra installer l'équipement GNSS sur un trépied temporaire afin d'analyser la qualité des données ainsi acquises.