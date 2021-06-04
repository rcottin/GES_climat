# Données d’émissions de GES au niveau entreprise
Juin 2021
raphael.cottin@bpifrance.fr 

Plusieurs sources de données sur l’intensité carbone et les émissions des entreprises sont mobilisées au sein de Bpifrance. Ces sources sont de nature diverses (reportées ou modélisées), et correspondent à des usages différents. Cette note fait le point sur les différentes mesures existant sur la place et donne quelques pistes pour leur utilisation.

## Généralités sur la mesure des émissions de GES et des intensités carbone
La difficulté principale est que l’on ne mesure pas les émissions de CO2 des entreprises, sauf cas particuliers . Les émissions de GES comportent une dimension inobservable, y compris pour les acteurs eux-mêmes. En conséquence, aucune des sources de données ne peut être considérée comme un « étalon or » à l’aune de laquelle on pourrait jauger les autres. 

En pratique, les **émissions directes** (scope 1) sont très liées à la combustion de combustibles fossiles et renouvelables (environ 90% des émissions de GES ). Le problème devient donc d’avoir accès à des données fiables de combustibles. 

> Ce qui se rapproche le plus d’une mesure directe des émissions de GES sont les données reportés dans le cadre du système européen de quotas d’émission (ETS) et recueillies dans le European Union Transaction Log (lien). Ces données sont structurées au niveau des installation industrielles. 

Les **émissions indirectes** (scope 2 et scopes 3) sont obligatoirement estimées. Le scope 2 (émissions liées à l’utilisation d’électricité) est conceptuellement peu controversé (conversion des MWh en CO2eq à partir de facteurs d’émission nationaux) même s’il peut y avoir des difficultés pratiques pour le cas de firmes multinationales ou d’activités transfrontières. 

Les **émissions liées à la chaîne de valeur** (scope 3 amont et aval) sont les plus incertaines. Des types de modélisation différents peuvent donner des résultats variables, le périmètre n’étant pas strictement comparable (cf. infra). Par ailleurs, ces « émissions » comportent un aspect « normatif » dont on doit être conscient lors de leur utilisation. 

## Types et sources de données 
### Types de données

Les données d’intensité carbone et d’émission des entreprises peuvent être classées selon plusieurs axes :
-	Par niveau de granularité : au niveau de l’installation, de l’entreprise, du secteur (et du pays). 
-	Données reportées ou modélisées
-	Types de retraitement effectué

#### Niveau de granularité
Les données d’installation sont très fiables si elles proviennent du système ETS car elles sont auditées régulièrement. Les données au niveau d’un secteur sont potentiellement comparables. Les données au niveau de l’entreprise font l’objet de doutes quant à leur fiabilité et leur comparabilité .

#### Données reportées ou modélisées
Le reporting des émissions de GES au niveau des entreprise font l’objet d’un processus d’harmonisation au niveau international, le Greenhouse gaz protocol. A noter que ce protocole est flou sur les méthodes utilisées pour calculer les émissions provenant des Scopes 3 : la reporting boundary (le périmètre de ce qui rentre dans la comptabilité du scope 3) est laissée à l’appréciation de chaque entité, ce qui a comme conséquence de limiter la comparabilité.

> A noter que le CDP lui-même déconseille l’utilisation d’intensités de scope 3 reportées, y compris après retraitement . 

##### Type de modélisation
Il existe plusieurs méthodes pour modéliser les émissions de scope 3 . Les modèles d’équilibre partiel/général calculables sont appropriées à l’échelle projet ou produit (assurance export). Pour comparer les secteurs entre eux, il est préférable d’utiliser des modélisations issues de modèles d’Input-Output. Ces modèles comportent l’avantage d’être compatible avec des notions de comptabilité nationale et d’être moins sensibles aux hypothèses que les modèles calculés (et les analyses en cycle de vie). Leur défaut est que la maille sectorielle utilisée est généralement peu fine (64 ou 88 catégories)

> Il existe différents types de modèles input output, qui varient dans les hypothèses et techniques de modélisation. Les deux grandes familles sont les Multi-regional Input Output models (MRIO) d’une côté, et les modèles basés sur l’hypothèse de technologie domestique de l’autre. Les premiers sont ceux utilisés par Inrate et l’OFCE ; les seconds par Eurostat et le CGDD. Les résultats des modèles MRIO sont convergents entre eux . Il y a des différences entre les résultats des MRIO et les modèles de traitements nationaux, qui correspondent à des objectifs différents. Les modèles utilisant la technologie domestique répondent à la question « quelle quantité d'émissions dans l’économie domestique si les produits importés étaient produits sur place » .

#### Retraitement des données
Le carbon disclosure project (CDP) effectue un retraitement sur les scopes 1 et 2 pour harmoniser les données reportées et éliminer les valeurs extrêmes. Les données scopes 3 sont également retraitées dans le CDP mais les frontières de reporting sont considérées comme trop variables pour donner lieu à des comparaisons fiables.
Fournisseurs de données

•	**Reuters** : a priori des données publiées par les entreprises. Il importe de savoir :
  + Le périmètre exact (quels scopes sont considérés)
  + Quels types de retraitements sont effectués
•	**CDP** : accès aux données brutes possibles. Rassemble des données reportées par les entreprises, mais effectue un contrôle qualité sur le reporting et une harmonisation ex-post
•	**Inrate** : reprend les données CDP (A VERIFIER), ajouter des données modélisées (provenant de MRIO) pour les scopes 3
•	**ADEME** : les bilans carbones effectués par les entreprises sont consultables sur le site de l’ADEME via une API. Selon l’ADEME, celles-ci ne doivent pas être utilisés pour comparer les entreprises entre elles.

## Utilisations des données d’intensité / d’émissions

Le type de données carbone à privilégier dépend du type d’usage envisagé. 

- **Pour le reporting** (BCE par exemple) : on préfèrera des données granulaires au niveau de la firme, dont l’origine soit traçable quitte à ce que des questions subsistent quant à leur fiabilité. Il n’appartient pas à BPI d’auditer le reporting carbone produit par les entreprises de son portefeuille. Cela pointe vers une source de type Reuters. Les scopes privilégiés seront les scopes 1 et 2. 
- **Pour l’analyse des risques** : il existe un arbitrage entre fiabilité de la donnée d’une part, et niveau de granularité de l’autre. Une utilisation à un niveau moins granulaire (sectoriel) peut être justifiée si cela permet d’avoir un degré de confiance supérieur dans intensités carbone. 
Par ailleurs, la prise en compte du risque de transition et d’actifs échoués nécessite d’avoir une vision plus large que simplement les émissions directes, ce qui implique de considérer les émissions le long de la chaîne de valeur (scopes 3) ; une donnée disponible de manière fiable uniquement au niveau sectoriel (cf. supra). 
