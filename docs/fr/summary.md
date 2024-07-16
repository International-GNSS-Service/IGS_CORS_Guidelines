Cette section résume les directives obligatoires et souhaitables que doit respecter une station GNSS permanente (Continuously Operating Reference Station, CORS) pour rejoindre le réseau IGS. Celles-ci sont destinées à s'appliquer aussi bien aux stations IGS actuellement en activité qu'aux stations nouvellement proposées. Dans la mesure du possible, les propriétaires de stations doivent se conformer intégralement à ces directives ; si ce n'est pas possible, ils sont invités à consulter le Comité d'Infrastructure de l'IGS. Les sections suivantes donnent de plus amples détails sur les recommandations résumées ici.

!!! info "Légende"

    :material-check-bold: Minimum Requis

    :fontawesome-solid-triangle-exclamation: Souhaitable

    :x: Non Recommandé

## Général

| Recommandation | Classification  |
| -------------- | --------------- |
| La station appartient à un réseau géodésique national/régional[^1].   | :fontawesome-solid-triangle-exclamation: |
| La station est installée pour une opération permanente et en continu. | :material-check-bold: |
| L'agence opérant la station dispose de toutes les capacités pour les réparations, les améliorations, et l'entretien courant de la station. | :material-check-bold: |

## Fondations et Site d'Installation

| Recommandation | Classification  |
| -------------- | --------------- |
| Roche-mère ou fondation en béton massif.                              | :material-check-bold: |
| Bâtiments ou structures similaires[^2].                               | :x: |
| Vue dégagée sur le ciel sans masque au-dessus de 10° d'élévation.     | :material-check-bold: |
| Le site d'installation est exempt d'obstructions de signal et de RFI. | :material-check-bold: |
| Le site d'installation est exempt de matériaux réfléchissants.        | :material-check-bold: |

## Monument et Supports

| Recommandation | Classification  |
| -------------- | --------------- |
| Pilier en ciment ou trépied/quadripode renforcé.                                                | :material-check-bold: |
| Support en acier fixé à un bâtiment.                                                            | :x: |
| Support maintenant l'antenne en place afin de conserver une orientation et un niveau constants. | :material-check-bold: |
| Support permettant à l'antenne d'être remplacée sans modifier sa position de plus de 0,5 mm ni son orientation de plus de 1°. | :material-check-bold: |

## Alimentation et Télécommunications

| Recommandation | Classification  |
| -------------- | --------------- |
| Assurer le fonctionnement continu de tous les dispositifs de télécommunication. | :fontawesome-solid-triangle-exclamation: |
| Assurer le contrôle à distance de l'accès au récepteur.                         | :material-check-bold: |

## Récepteur

| Recommandation | Classification  |
| -------------- | --------------- |
| Suivi des codes et des phases porteuses de tous les GNSS à toutes les fréquences[^3]. | :material-check-bold: |
| Enregistrement continu des données GNSS brutes.                                       | :fontawesome-solid-triangle-exclamation: |
| Dissémination des données en temps réel (RTCM).                                       | :fontawesome-solid-triangle-exclamation: |
| Suivi de tous les satellites visibles (qu'ils soient déclarés utilisables ou non) jusqu'à un minimum d'élévation de 5° (0° étant recommandé). | :material-check-bold: |
| Désactivation des options de lissage de mesures de code et de phase (pseudorange and phase smoothing). | :material-check-bold: |
| Désactivation des options d'atténuation des multi-trajets.                            | :material-check-bold: |
| Espace de stockage disponible pour une quantité raisonnable de données brutes (en fonction des circonstances locales). | :material-check-bold: |

## Antenne

| Recommandation | Classification  |
| -------------- | --------------- |
| Utilisation d'un type d'antenne disposant d'un étalonnage moyen absolu dans l'[ANTEX officiel de l'IGS](https://files.igs.org/pub/station/general/igs20.atx). | :material-check-bold: |
| Utilisation d'une antenne disposant d'un étalonnage individuel absolu. | :fontawesome-solid-triangle-exclamation: |
| Antenne horizontale et orientée à moins de 5° du nord géographique.    | :material-check-bold: |
| Utilisation d'un radôme de protection.                                 | :x: |

## Données

| Recommandation | Classification  |
| -------------- | --------------- |
| Les données doivent être fournies au format RINEX[^4]. | :material-check-bold: |
| ^^ Si une dissémination en temps réel est disponible[^5]^^, le format doit être “RTCM 3 MSM5 stream for real-time applications”[^6]. | :material-check-bold: |
| Dans le cas d'une coupure des systèmes de télécommunication, les données non transmises doivent être soumises aux centres de données dès le retour de ces systèmes. | :material-check-bold: |
| Le fichier RINEX doit être généré par le récepteur ^^ou^^ traduit du fichier binaire natif. | :material-check-bold: |
| Taux de complétude des fichiers ciblé : | 99% |

### Fichiers RINEX Haute-Fréquence

| Recommandation                 |              | Classification |
| ------------------------------ | ------------ | -------------- |
| Disponibilité de ces fichiers. |              | :fontawesome-solid-triangle-exclamation: |
| Latence.                       | < 5 minutes  | :material-check-bold: |
| Fréquence d'échantillonnage.   | 1 Hz         | :material-check-bold: |
| Durée.                         | 15 minutes   | :material-check-bold: |

### Fichiers RINEX Horaires

| Recommandation                 |              | Classification |
| ------------------------------ | ------------ | -------------- |
| Disponibilité de ces fichiers. |              | :fontawesome-solid-triangle-exclamation: |
| Latence.                       | < 5 minutes  | :material-check-bold: |
| Fréquence d'échantillonnage.   | 30 secondes  | :material-check-bold: |

### Fichiers RINEX Journaliers

| Recommandation                 |              | Classification |
| ------------------------------ | ------------ | -------------- |
| Disponibilité de ces fichiers. |              | :material-check-bold: |
| Latence.                       | < 30 minutes | :material-check-bold: |
| Fréquence d'échantillonnage.   | 30 secondes  | :material-check-bold: |

## Métadonnées

| Recommandation | Classification  |
| -------------- | --------------- |
| Métadonnées complètes et à jour au format GeodesyML ou IGS site log. | :material-check-bold: |
| Identifiant de station à 9 caractères approuvé par l'IGS.            | :material-check-bold: |
| Identifiant DOMES attribué par l'IERS.                               | :material-check-bold: |
| Dans le cas d'une modification de la station, mise à jour du site log de la station sous 24 heures. | :material-check-bold: |
| En-tête des fichiers RINEX correspondant aux métadonnées dans le site log de la station.            | :material-check-bold: |
| Photos de l'installation de l'antenne dans les 4 directions cardinales (N, E, S, O).                | :material-check-bold: |

[^1]: Obligatoire pour les CORS situées dans les emprises des réseaux APREF, EPN, et SIRGAS.
[^2]: Une dérogation peut être accordée après évaluation par le SPC.
[^3]: Les nouvelles stations doivent suivre tous les codes et phases porteuses disponibles.
[^4]: Pour les nouvelles stations, RINEX 3.04 est la version minimale requise ; les données au format RINEX 2.11 ne seront pas acceptées.
[^5]: Il est fortement encouragé que les nouvelles stations fournissent des flux de données en temps réel.
[^6]: Le format MSM7 est encouragé.
