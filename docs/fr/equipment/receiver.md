On résume ci-dessous les caractéristiques recommandées pour les récepteurs GNSS à la date de publication de ces directives. Les nouvelles stations GNSS proposées pour l'IGS doivent satisfaire tous les critères répertoriés. Les opérateurs de stations existantes se trouvant dans l'impossibilité de mettre celles-ci à niveau pour le moment doivent garder ces recommandations à l'esprit pour les futures mises à jour.

### Suivi des Signaux

- Tous les signaux de code, de phase et les rapports signal sur bruit (SNR) disponibles sur toutes les fréquences doivent être suivis. Les observations de Doppler sont facultatives.
- Le lissage des mesures de code doit être désactivé.
- L'atténuation des multi-trajets doit être désactivée.
- Les nouvelles stations doivent suivre au moins les constellations GPS, GLONASS, Galileo et BeiDou[^1].
- La capacité à observer les signaux futurs est appréciée.
- Le récepteur doit être réglé pour suivre les signaux jusqu'à une élévation minimum de 0° (5° est acceptable).
- Le récepteur doit être réglé pour suivre tous les satellites en vue (y compris les satellites déclarés inutilisables).
- Le récepteur doit synchroniser l'instant réel de ses observations à moins de 1 milliseconde des secondes entières (en temps GPS).

### Flux de Sortie

- Utilisation du protocole RTCM SC-104 le plus récent, à 1 Hz, sur plusieurs ports.
- Diffusion des données brutes au format constructeur.
- Capacité de diffuser les données vers plusieurs destinations.

### Enregistrements

- Enregistrement continu des données brutes non lissées.
- Enregistrement des données RINEX (échantillonnage toutes les 30 secondes minimum), si elles ne sont pas générées en dehors du récepteur.
- Enregistrement des données du capteur d'entrée.

Le firmware d'un récepteur GNSS est le logiciel informatique qui contrôle le suivi des signaux GNSS par le récepteur. Comme pour tout autre logiciel, un firmware peut être mis à jour soit pour corriger des bugs, soit pour améliorer les capacités de suivi du récepteur. Avant de procéder à la mise à niveau, un nouveau firmware doit être méticuleusement testé et ne doit être installé que sur les stations qui pourraient bénéficier du changement. En général, le récepteur doit être équipé du firmware stable le plus récent dans les 6 mois suivant sa sortie.

[^1]: Les stations situées dans la zone de couverture des systèmes satellitaires régionaux QZSS et IRNSS doivent également suivre ces derniers. La capacité de suivi SBAS est encouragée.
