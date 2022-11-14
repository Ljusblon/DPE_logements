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
 
![image](/main/image.jpg "Titre : Échelle de performance énergétique et environnementale.").


*Titre : Échelle de performance énergétique et environnementale.*
*Source : https://www.limmovation.fr/le-diagnostic-de-performance-energetique-definition-et-evolution/

Cette figure représente les échelles de performance énergétique et environnementale dans le cadre du Diagnostic de Performance Énergétique. Ces dernières sont respectivement exprimées en kWhEP/m2.an et en kg eqCO2/m2.an.
À propos du critère énergétique, kWhEP/m2.an est l’unité la plus répandue et la plus représentative de la performance d’un bâtiment, indépendamment de l’énergie utilisée. Pour le critère environnemental, les émissions de CO2, principal responsable des émissions de GES, restent également le critère le plus connu et utilisé. Seulement, il existe bien d’autres critères que l’on retrouve notamment dans le cadre d’une Analyse de Cycle de Vie, d’autant que résonner sur un seul d’entre eux en cherchant à l’optimiser peut-être sujet à des transferts de pollutions ou des effets rebonds. 

Les étiquettes énergie et climat permettent notamment à chaque ménage français qui souhaite acheter ou louer un bien immobilier de mieux mesurer l’impact de ses choix d’énergie que ce soit le bois, le fioul, le gaz naturel ou électricité, et d’évaluer facilement la performance du logement.
Elle permet aussi aux pouvoirs publics, tant les administrations, que collectivités territoriales, d'identifier les zones où se trouvent les logements énergivores et de mettre en œuvre des politiques publiques de rénovation ciblées.

### c) Calculs et indicateurs du DPE

Le calcul du DPE s'effectue à partir d'une série de critères correspondant aux caractéristiques physiques du logement ou du bâtiment tels que la surface au sol, la surface vitrée, la nature des matériaux de construction ou le type d'isolation, etc, et au type d'énergie utilisé pour le chauffage et l'eau chaude sanitaire.
Ce calcul permet d'établir une consommation énergétique en kilowattheure par mètre carré et par an pour l’étiquette énergie, qui permet de déterminer le nombre de kilos d'équivalent CO2 émis par mètre carré et par an par le logement concerné, pour l’étiquette climat.

La base DPE comporte de nombreux indicateurs. Ces derniers se décomposent en trois catégories :
-	Les informations clef du DPE : données concernant les étiquettes énergie et émissions de gaz à effet de serre du logement. Ces données correspondent aux indicateurs suivants :
o	La consommation énergie en kWhEP/m².an ;
o	Le classement consommation d'énergie ;
o	L’estimation d'émission de GES en Kg eqCO2/m².an ;
o	Le classement GES.
-	Les éléments d'identification et de géolocalisation du logement ou du bâtiment : adresse postale complète, coordonnées géographiques, type de bâtiment.
-	Les éléments techniques qui entrent dans le calcul DPE, soit l'ensemble des caractéristiques physiques du logement ou du bâtiment (surfaces, matériaux), mais aussi :
o	Le type d'installation de chauffage ;
o	Le type d'énergie de chauffage ;
o	Le type d'installation pour l'eau chaude sanitaire (ECS) ;
o	Le type d'énergie d'ECS.

