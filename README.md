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


## 3) Cadre réglementaire qui enserre le DPE

### a) Cadre réglementaire - DPE

Le DPE doit être établi par un professionnel répondant des conditions de compétences, d’assurance, d’organisation et de moyens mais également d’indépendance et d’impartialité conformément aux dispositions de l’article L.271-6 du CCH.  

L’article D134-4-2 du CCH a modifié la durée de validité des diagnostics de performance énergétique :
- Les diagnostics réalisés à compter du 1er juillet 2021 seront valable dix ans ;
- Ceux réalisés entre le 1er janvier 2013 et le 31 décembre 2017 sont valides jusqu'au 31 décembre 2022 ;
- Et ceux réalisés entre le 1er janvier 2018 et le 30 juin 2021 jusqu'au 31 décembre 2024.

À compter du 1er juillet 2021, le DPE devient opposable : dès lors que l’absence d’information ou l’information erronée lui cause un préjudice, l’acquéreur ou le locataire peut se prévaloir des informations relatives à la performance énergétique à l’encontre du vendeur ou du bailleur pour obtenir réparation. 
Aussi, si un bien est vendu ou loué sous l’étiquette E alors qu’il appartient à la catégorie G, l’acquéreur pourra contraindre le vendeur à réaliser des travaux.  
L’arrêté du 31 mars 2021 relatif au diagnostic de performance énergétique pour les bâtiments ou parties de bâtiments à usage d'habitation en France métropolitaine détermine le contenu des diagnostics de performance énergétiques. Il précise les modalités d'établissement de ces derniers et la méthode de calcul conventionnelle à mobiliser. 

### b) Cadre réglementaire - rénovations thermiques

La loi Énergie-Climat du 8 décembre 2019 vise à lutter contre la précarité énergétique et à limiter les émissions de CO2 de la France. L’objectif étant d’atteindre la neutralité carbone. Pour cela, la loi impose aux bailleurs de rénover certains logements énergivores, souvent nommés « passoires thermiques ». 
Les propriétaires bailleurs ne peuvent pas être soumis à l’obligation de rénover leur logement du jour au lendemain. Pour éliminer les passoires thermiques, un calendrier a été mis en place :
- En 2021, il n’est plus possible d’augmenter le loyer entre deux locataires si aucun chantier de rénovation thermique n’a été réalisé dans le logement.
- En 2022, les propriétaires-bailleurs sont tenus de faire réaliser un audit énergétique de leur bien. Cet audit donnera lieu à des conseils en matière de rénovation thermique.
- À partir de 2025, les propriétaires de logements énergivores consommant plus de 330 kW/m²/an seront tenus d'effectuer des travaux pour améliorer la performance énergétique globale du bâti. Car dès 2025, ces passoires thermiques seront non seulement régulées mais aussi interdites à la location, avec une obligation de « remise à niveau thermique », accompagnée d'un bilan énergétique.
- Dès 2028, cette mesure sera étendue aux logements classés F


## 3) Description rapide de la base de données

Les champs de la base de données retenues sont les suivants : 
 
 

Quelques requêtes SQL permettent d’extraire les informations suivantes : 
La moyenne de la consommation d’énergie pour les 240 000 logements recensés est de 187,1 kWhEP/M2.an, tandis que la médiane est de 190 kWhEP/M2.an.

La moyenne de l’estimation GES en Kg eqCO2/m2.an pour chaque logement est de 23,7 Kg eqCO2/m2.an, tandis que la médiane est de 13 Kg eqCO2/m2.an. Cette différence s’explique notamment par des valeurs d’émissions de GES extrêmes et/ou incohérentes, comprises entre 3261 et 375.

Une courte requête avec un SELECT COUNT sur la colonne classe_consommation_energie et un GROUP BY par classe énergétique permet d’obtenir la répartition suivante : 

*Titre : Nombre d’occurrences de chaque classe énergétique pour les 240 000 entrées de la base de données « DPE Logements ».*

De même, une courte requête avec un SELECT COUNT sur la colonne classe_estimation_ges et un GROUP BY par classe environnementales permet d’obtenir la répartition suivante : 
 
*Titre : Nombre d’occurrences de chaque classe environnementale pour les 240 000 entrées de la base de données « DPE Logements ».*

En outre, la médiane des années de construction se situe autour de 1970, indépendamment des données incohérentes. La plage de construction des logements de cette base de données est donc comprise entre le début du XVIIIe siècle et 2017. Nous fixons la date de construction des premiers logements au début du XVIIIe siècle, ne pouvant attester de la véracité des dates antérieures avancées. 

Une courte requête avec un SELECT COUNT sur la colonne tr001_modele_dpe_type_libelle et un GROUP BY par type de DPE permet d’obtenir la répartition suivante : 
|Type de DPE|Occurrences|
|--------|--------|
| Vente | 165 166 |
| Location | 51 770 |
| Neuf | 18 055 |
| Copropriété | 5001 |
| Bâtiment public | 7 |
| Centre commercial | 1 |
| Total | 240 000 |

Le dictionnaire de données de l’ADEME présente les entrées suivantes pour ce champ : 
 
Une courte requête avec un SELECT COUNT sur la colonne tr002_type_batiment_description et un GROUP BY par type de bâtiment permet d’obtenir la répartition suivante : 
|Type de bâtiment|Occurrences|
|--------|--------|
| Logement | 91 341 |
| Maison Individuelle | 144 829 |
| Bâtiment collectif à usage principal d’habitation | 3 830 |
| Total | 240 000 |

Le dictionnaire de données de l’ADEME présente les entrées suivantes pour ce champ : 
 


# II- Usages et usagers de la base de données

## 1) Les publics cibles de cette base de données

Les données de cette base de données sont accessibles sous différents formats. Chaque format est destiné à un usage différent. 
•	La base « DPE Logements » est accessible sous la forme d’un outil statistique, destiné au grand public comme aux acteurs du bâtiment qui souhaitent obtenir des ordres de grandeur sur la performance des bâtiments en France, tout en tenant compte des limites de cette base de données sur lesquelles nous reviendront. 
•	Elle est également accessible sous la forme d’un tableau interactif, principalement destiné aux organismes publics et entreprises qui travaillent sur un territoire donné et veulent récupérer l’ensemble des informations existantes sur les biens ayant fait l’objet d’un DPE sur le territoire en question. Les données peuvent notamment être extraites sous un format csv. 
•	Enfin, cette base de données est directement accessible en SQL pour les utilisateurs spécialisés dans le traitement des bases de données. Nous avons notamment exporté la base de données en csv, avant de l’importer dans Talend pour étudier la qualité des données et permettre leur intégration directement une base de données en SQL. 

 

 
Nul besoin d’écrire tout ce code avec Xampp qui facilite grandement la création et l’import de base de données. 

## 2) Diagnostics de performance énergétique pour les logements - Classe énergétique

 
*Titre : Diagnostics de performance énergétique pour les logements - Classe énergétique*
*Source : https://data.ademe.fr/datasets/dpe-france*

Cette carte présente les DPE des logements en fonction de leur classe énergétique.
Les diagnostics de performance énergétique sont transmis à l’ADEME à des fins d'études statistiques, d'évaluation et d'amélioration méthodologique en vertu de l’article L134-4-2 du code de la construction et de l’habitation.
À Partir de cette carte interactive, nous avons pu générer un gif permettant de voir l’évolution des DPE. Cette animation a été réalisé à partir de 18 images prises à intervalle régulier entre 6 et 7 ans pour les logements construits entre 1900 et 2021.

GIF DPE low.mp4
https://ezgif.com/maker












## 3) Diagnostics de performance énergétique pour les logements - Classe GES  

 
*Titre : Diagnostics de performance énergétique pour les logements - Classe GES*
*Source : https://data.ademe.fr/datasets/dpe-france*

Cette carte présente les DPE des logements en fonction de leur classe énergétique.
Les diagnostics de performance énergétique (DPE) sont transmis à l’ADEME à des fins d'études statistiques, d'évaluation et d'amélioration méthodologique en vertu de l’article L134-4-2 du code de la construction et de l’habitation.

## 4) Diagnostics de performance énergétique pour les logements - Relation entre classes énergétiques et GES

 
*Titre : Diagnostics de performance énergétique pour les logements - Relation entre classes énergétiques et GES*
*Source : https://data.ademe.fr/datasets/dpe-france*

Cette représentation met en relation les "classes de consommation d'énergie" et les "classes GES" pour les diagnostics de performance énergétique (DPE) des logements.

## 5) Autres usages possibles

### a) Le hackathon RenovAction

Les données contenues dans la base DPE ont été utilisées lors du hackathon RenovAction, du 11 au 22 juin 2020, co-organisé par l'ADEME, le Ministère de la Transition Ecologique et plusieurs partenaires, dont Etalab.
Ce hackathon avait pour objectif de faire émerger des solutions pour la rénovation énergétique. L'évènement a permis de faire émerger de premières propositions d'outils et de plateformes s'appuyant sur les données de la base DPE Logements. 

### b) Le projet Tribu Reno

Le projet Tribu Reno repose sur une plateforme qui permet de regrouper et de manipuler un ensemble de jeux de données issues de plusieurs sources. Il s’agit bien d’un service proposant un parcours de rénovation simplifié et rendant possible la massification via le processus d’achat groupé impliquant la collectivité territoriale dans l’acte de rénovation et le choix du prestataire tout en s’appuyant sur les outils existants

### c) Le projet IMOPE

Le projet IMOPE repose sur une plateforme cartographique permettant de regrouper et de manipuler les données afin d'aider les acteurs territoriaux à caractériser le potentiel de rénovation de chacun des bâtiments de leur territoire.

### d) Le projet Mon Coach Renov

Le projet Mon Coach Renov correspond à une démarche d’accompagnement à la rénovation énergétique des logements, qui croise les données de consommations avec les caractéristiques du logement pour identifier les surconsommations et proposer des travaux en conséquence. Il aussi facilite l’accès à l’information fiable sur la rénovation telle que les coûts des travaux ou les aides disponibles.

### d) Le projet Carto Reno

Le projet Carto Reno est une plateforme permettant de cartographier et de caractériser le parc des logements sociaux en France à partir de l’open data afin de proposer des scénarios de rénovation énergétique pertinents en fonction de la typologie de ces bâtiments.

###e) Le projet Rénover pour tous

	Le projet Rénover pour tous est un dispositif proposant un nouveau mécanisme de financement « d’acquisition-rénovation globale » en séparant la valeur du bâti de celle du foncier. Avec l’acquisition du foncier par un organisme foncier solidaire, ce dispositif permet de solvabiliser les ménages-propriétaires aux revenus modestes dans l’incapacité de financer seuls une rénovation globale de leur logement, et de développer une offre en accession sociale de manière pérenne.

### f) D'autres usages potentiels

La base DPE constitue outil clé des politiques de rénovations énergétiques tant au niveau local que national. La mise à disposition de cette base en open data ouvre la porte à de nombreux usages. Il est dès lors possible de visualiser sur le portail open data de l'ADEME la répartition géographique des classes DPE énergies et gaz à effet de serre. Ces premiers traitements sur la base de données laissent entrevoir les usages attendus d'une exploitation plus précise des données :
•	« Le croisement de la base DPE avec des données de travaux afin d'estimer l'impact de ces derniers sur la consommation d'énergie » ;
•	« Le croisement des données avec les consommations d'énergie des résidences tertiaires » ;
•	« Le croisement des données DPE avec les données d'ancienneté du parc de logements, afin de comprendre la corrélation entre ancienneté des logements et consommation énergétique et d'établir des zonages de bâtis à rénover. »

Les différents travaux de valorisation des données se feraient au bénéfice de nombreux acteurs :
•	Pour les acteurs publics qui souhaitent piloter leurs politiques publiques par la donnée : l'exploitation des données de la base DPE Logements permettrait de mieux caractériser le parc immobilier français, de favoriser le recours à certains modes de consommation, ou encore de d'identifier les zones d'habitat indigne.
•	Pour les acteurs privés qui cherchent à développer des offres de services ou de produits relatifs à la rénovation des bâtiments : la valorisation des données permettrait de mieux cibler les besoins en fonction des territoires et des logements et affinerait l'offre proposée aux particuliers ou aux acteurs publics.
•	Pour le milieu de la recherche ou pour les acteurs de la transition écologique qui souhaitent s'appuyer sur d'important volumes de données afin d'étudier les enjeux de la transition énergétique, en vue de proposer des axes d'améliorations qui s'appuient sur des éléments empiriques.
# III- Limites et perspectives de la base de données

## 1) La non-représentativité des données et leur qualité

L’ADEME souligne d’emblée que les données fournies, sont les données brutes de l’observatoire DPE qui contient l’ensemble des DPE effectués par les diagnostiqueurs immobiliers. Leur interprétation doit être faite avec précaution, en ce sens où le DPE est obligatoire seulement pour une vente, une location ou à l'achèvement de toute nouvelle construction. Aussi, tous les biens ne sont pas dotés d'un DPE. À ce titre, cette base ne couvre pas tout le parc immobilier et n’en donc est pas pleinement représentative.
Pour estimer la performance énergétique et environnementale de l'ensemble du parc français et la distribution nationale des classes DPE, un travail de redressement des données devrait être fait. Il nécessite l’utilisation de la base de données DPE, mais aussi la mobilisation d’autres bases de données telles que le répertoire de logements de l'Insee « Fidéli » ou encore les distributions d'énergies principales de chauffage des résidences principales estimées par le recensement de la population.

Les données mises à disposition sont les données brutes saisies par les diagnostiqueurs, sur lesquelles l’ADEME n’effectue aucune reprise de données. Dans ce cadre, l’ADEME ne peut en aucun cas être tenue responsable de la qualité des données qui lui sont transmises.
Contrairement aux données envoyées sur l’ancien observatoire, néanmoins elles font l’objet de contrôles de cohérence. En cas de non-conformité, le DPE est rejeté si le contrôle est bloquant. 

## 2) Les limites du DPE et donc par extension de la Bdd

Il convient de souligner la principale limite de la base DPE logements et de son exploitation. En effet, les diagnostics sont réalisés de façon à rendre comptable la performance des bâtiments sans tenir compte de leur usage, ni de leur environnement extérieur. Le résultat obtenu est donc seulement une performance standardisée du bâtiment et en aucun cas une image de la performance réelle de ce dernier. De fait, les préconisations faites à l’issue de ces diagnostics ne sont que rarement propre au bâtiment et à ses usages. Les économies qui en découlent sont donc entachées d’erreurs d’appréciation. Il faudrait donc repenser le diagnostic énergétique en prenant en compte l’environnement extérieur de chaque bâtiment, leurs usages, le fonctionnement réel des bâtiments ainsi que les incertitudes qui y sont associées. 

Martin Amiel montre bien dans sa thèse, sur une optimisation du diagnostic de performance énergétique, que pour réussir à rendre performant l’ensemble des projets de rénovation, il est nécessaire de sortir du schéma classique et de travailler sur l’ensemble de la chaîne de valeur de la rénovation : du diagnostic au suivi de la performance, en passant par la préconisation des scénarii de rénovation et leur garantie de performance. 
La plupart des rénovations engagées sont uniquement fondées sur un simple diagnostic énergétique. Ces diagnostics, fondés sur un calcul conventionnel ou des factures de consommations d’énergie, n’ont pas pour objectif de représenter les consommations réelles du bâtiment, mais de pouvoir comparer la formance des bâtiments entre eux, en se fondant sur un usage trop standardisé du bâtiment. 
Seulement, la méthode de calcul des PDE ne prend pas en compte l’ensemble des usages énergétique des bâtiments et les calculs de consommations comprennent nombre de valeurs forfaitaires ne permettant pas de retranscrire les usages, caractéristiques et l’environnement extérieur des bâtiments. 
De fait, les préconisations de travaux et les économies d’énergie qui y sont associées ne peuvent pas être justes. En outre, même en essayant de caractériser le plus fidèlement possible un bâtiment avec son enveloppe, son environnement et ses usages, nombre d’incertitudes subsistent, dont une part demeure inconnue, à l’image de la dégradation de la performance thermique des matériaux dans le temps. 
Aussi pour pallier cette limite, les analyses d’incertitude et de sensibilité des paramètres pris en compte, déjà mis en œuvre lors de la construction de nouveau bâtiment, devraient être mises en place dans le cadre des rénovation énergétiques. 





