## Alimentation

Toutes les CORS doivent être alimentées par des sources d'alimentation continues et fiables. L'alimentation via secteur et l'énergie solaire sont toutes deux des sources d'alimentation principale appropriées. Le choix entre l'énergie solaire et le secteur comme source d'alimentation principale sera déterminé en fonction des questions de coût, de sécurité, de disponibilité et d'emplacement. Un éloignement conséquent du réseau électrique peut rendre l'énergie solaire associée à un système de batteries plus économique. Une alimentation secteur peu fiable, avec des fluctuations de puissance significatives, peut aussi rendre l'énergie solaire préférable.

**Alimentation sur le Secteur**

Lorsque l'électricité secteur est utilisée, un circuit électrique dédié pour l'équipement de la station CORS est recommandé pour réduire le risque que les charges électriques d'autres équipements puissent déclencher un disjoncteur ou un dispositif de courant résiduel, ce qui interromprait l'alimentation de la station CORS. Installez des prises électriques secteur de manière à minimiser la déconnexion volontaire ou involontaire de l'alimentation de l'équipement du site. Il est recommandé d'installer une protection contre les surtensions pour prévenir les dommages causés par les pics de tension.

**Énergie Solaire (Photovoltaïque)**

Le facteur clé pour les performances solaires est l'ensoleillement disponible, qui dépend de la latitude et des conditions climatiques locales. On pourra vérifier auprès des agences météorologiques locales les heures moyennes d'ensoleillement disponibles dans la zone cible.

Un système de batteries est requis pour les sites alimentés par l'énergie solaire, et constitue une source d'alimentation secondaire courante pour les sites alimentés par le secteur. Une alimentation sans interruption (ASI / Uninterruptible Power Supply UPS) est une source d'alimentation à court terme, fournissant de l'électricité pendant le basculement entre les sources d'alimentation primaire et secondaire.

Une unité de distribution électrique (Power Distribution Unit, PDU) est recommandée pour les sites CORS. La PDU gère et conditionne l'alimentation électrique du site, souvent avec un mécanisme automatique de basculement entre les sources d'alimentation primaire et secondaire. Une PDU gérée à distance peut contrôler le système d'alimentation dans des limites prédéfinies et fournit des outils système, des rapports et des alertes. Selon les conditions ambiantes, une PDU peut également éteindre et rallumer des équipements moins critiques. Une PDU avec une liaison de communication permet à l'opérateur CORS de contrôler l'alimentation des équipements à distance.

## Télécommunications

Un site CORS nécessite des télécommunications fiables pour la transmission des données, soit directement aux utilisateurs, soit à un centre de données opérationnel (Operational Data Centre, ODC). Le choix du système de télécommunication est crucial, car il affecte la transmission des données et le contrôle à distance de l'équipement de la station CORS.

Il existe un large éventail d'options en termes de types de télécommunication et de fournisseurs de services. Les systèmes de communication usuels pour la transmission des données entre un site CORS et un ODC comprennent :

- l'ADSL (Asymmetric Digital Subscriber Line),
- les réseaux de téléphonie mobile,
- les réseaux Ethernet d'entreprise (Wide Area Network, WAN), ou
- les systèmes par satellite VSAT (Very Small Aperture Terminal, terminal à très petite ouverture) pour les sites particulièrement distants de tout autre infrastructure.

Le choix du système de télécommunication est fonction de la quantité de données à transmettre, des protocoles de données utilisés, de la latence maximale acceptable pour ces données, et des services disponibles dans la zone cible.

Il est recommandé d'avoir un système de télécommunication secondaire indépendant pour améliorer la fiabilité du site. Les systèmes de télécommunication secondaires sont particulièrement importants sur les sites offrant des services en temps réel, et sur les sites distants où les frais d'une visite sur site dépassent les coûts du système de communication.

La bande passante requise pour une station CORS dépend de plusieurs facteurs, notamment :

- les opérations normales de transmission (c'est-à-dire, la transmission en temps réel et les téléchargements réguliers de données),
- les téléchargements irréguliers tels que la récupération de données stockées sur le récepteur après une interruption de communication,
- les téléchargements pour les mises à niveau du firmware du récepteur,
- les besoins de bande passante supplémentaire (par exemple pour le support de l'interface utilisateur des récepteurs GNSS, pour les stations météorologiques, ou pour les dispositifs de gestion de réseau ou d'alimentation),
- les augmentations globales de volume de données en raison de la modernisation des GNSS (c'est-à-dire, des signaux, des satellites et des systèmes de satellites supplémentaires).

Quelle que soit la méthode de télécommunication utilisée, la latence des données entre un site CORS et un utilisateur de services de positionnement en temps réel ne doit pas dépasser deux secondes.