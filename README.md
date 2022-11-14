# Base de données DPE Logements de l'ADEME - Vie sociale des données


# I- Description de la base de données

  Aujourd’hui, les modes de production et de consommation de l’énergie sont en train de faire leur révolution, plus ou moins contrainte, afin de préserver les ressources et d’anticiper la disparition programmée des énergies fossiles. 
Parmi les principaux secteurs concernés se trouve le secteur du bâtiment, en tant que premier consommateur d’énergie en France avec 45 % de la consommation, soit près de 70 Mtep et deuxième émetteur de CO2, avec 23 % des émissions nationale. Un des principaux leviers pour faire face à ces contraintes et aux différents engagements des gouvernements successifs passe par la rénovation énergétique et thermique du parc immobilier, afin de réduire les consommations liées à son exploitation. La rénovation énergétique désigne l’ensemble des travaux réalisés sur un bâtiment en vue de diminuer la consommation énergétique du bâtiment et/ou de ses occupants. C’est à l’aune de ces considérations que notre attention se porte sur la base de données « DPE Logements » de l’ADEME, dont les données sont antérieures à juillet 2021.

## 1) Construction de la base de données et DPE

### a) Construction de la base de données

  En 2020, l'ADEME, avec l'appui d'Etalab, a mis à disposition sur les portails data.ademe.fr et data.gouv.fr la base des Diagnostics de Performance Énergétique (DPE) des logements et des bâtiments tertiaires pour l’ensemble du territoire français métropolitain.
La base de données DPE est relativement volumineuse avec plus de 240 000 entrées et près de 4 millions de données, le tout dans un format adaptée à l’open data, puisque cette dernière est diffusée au format CSV et SQL. 
Les équipes de l’ADEME et d’Etalab ont travaillé de concert pour extraire efficacement les données de la base source. Initialement, les données DPE étant saisies par les diagnostiqueurs eux-mêmes, puis agrégées et centralisées dans la base de données de l'ADEME, des erreurs de saisie sont fréquentes, notamment sur les champs correspondants à l'adresse du logement, bâtiment concerné par le DPE ou encore son année de construction.
Etalab a également mis en place un traitement pour le géocodage de la base de données. Le géocodage consiste à affecter des coordonnées géographiques à une adresse postale. 
Etalab a utilisé le géocodeur Addok en s'appuyant sur la Base d'Adresse Nationale (BAN). Enfin, les données DPE ont enfin été enrichies de coordonnées géographiques avec la longitude et latitude, ainsi que d'une adresse « corrigée » récupérée avec la BAN. Une fois le géocodage réalisé, l'ADEME a pu mettre à disposition les données à la maille départementale.

### b) Le DPE

  Selon l’ADEME, le diagnostic de performance énergétique renseigne sur la performance énergétique d’un logement ou d’un bâtiment, en évaluant sa consommation d’énergie et son impact en termes d’émissions de gaz à effet de serre. Il décrit le bâtiment ou le logement, ainsi que ses équipements de chauffage, de production d’eau chaude sanitaire, de refroidissement et de ventilation. Il indique, suivant les cas, soit la quantité d’énergie effectivement consommée sur la base de factures, soit la consommation d’énergie estimée pour une utilisation standardisée du bâtiment.
Le DPE est un diagnostic réalisé en France sur les biens immobiliers. Il doit être présenté lors des transactions immobilières dont les ventes, locations et constructions neuves des logements et des bâtiments tertiaires tels que les bureaux, hôtel ou établissements publics. Il vise à informer le propriétaire et le locataire de la consommation d'énergie du logement ou du bâtiment tertiaire sur son chauffage, son refroidissement, sa production d'eau chaude sanitaire (ECS). L’ADEME rappelle que le DPE de certains bâtiments publics doit également être affiché dans le hall d’accueil du bâtiment. L'ADEME est également l'organisme chargé de collecter les DPE depuis 2013. Il convient d’ajouter que la durée de validité du DPE est de dix ans. 

La lecture du DPE est facilitée par deux étiquettes à sept classes. L’échelle est cotée de A, pour les logements les plus sobres, à G, pour les plus énergivores. La moyenne du parc immobilier français se situe autour de 240 kWhEP/m2.an, soit la classe E.
 
*Titre : Échelle de performance énergétique et environnementale.*
*Source : https://www.limmovation.fr/le-diagnostic-de-performance-energetique-definition-et-evolution/

