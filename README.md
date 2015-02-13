# VizElections
=====================
# Présentation
VizElections permet de : 
- visualiser les taux d'abstention sur Paris par arrondissement et par scrutin et d'étudier la corrélation éventuelle de ce taux avec le revenu médian de la population
- visualiser les résultats des différentes élections en cliquant sur un arrondissement et en choissant un scrutin
![Interface taux d abstention](https://github.com/cwamgis/VizElections/blob/master/99_doc/visu_tx_abstention.png)

![Interface resultats](https://github.com/cwamgis/VizElections/blob/master/99_doc/visu_res.png)


# Données
Cette application exploite les données suivantes : 
- les données des élections de 2007 à 2014 de la ville de Paris disponibles sur le site opendata au format json
- les données INSEE/DGFIP, revenus fiscaux localisés des ménages
- la couche géographique des arrondissements de Paris l'APUR (couche shp convertie en kml)

# Description du fonctionnement
![Chaîne de traitement](https://github.com/cwamgis/VizElections/blob/master/99_doc/chaine.png)


La dernière version du logiciel n'utilise plus le KML pour calculer la symbologie de la couche abstention.
En effet, cette version permet à l'utilisateur de choisir un scrutin pour l'affichage des taux d'abstention.
Ainsi, la génération du kml n'est plus nécessaire pour chaque mise à jour et pourrait donc être sortie de la chaine de traitement.

![Affichage des taux d'abstention](https://github.com/cwamgis/VizElections/blob/master/99_doc/processus_visu.png)

Lors d'un choix de scrutin, une requête Ajax est réalisée vers un script php qui renvoie les résultats d'abstention en consultant la base Mongo. Ce résultat au format Json est ensuite parsé côté client. Les classes d'affichage sont de cette manière calculées pour être affectées aux polygones arrondissement et à la légende.

# Arborescence de l'application
## 0_donneesBrutes
Répertoire contenant les données brutes
## 1_alimentation
Scripts python permettant d'alimenter la base MongoDB
## 2_production_kml
Script de génération des fichiers kml
##  3_resultat_dumps_mongodb
Dumps de la base electionsdb
## 3_resultatWeb
Rendu web en php/js/mongo
## 99_doc
Image et vidéo de démo
## 99_qualite
Tests de qualité sur la base
## sprint.txt
Fichier détaillant les sprints pour les développement




# Technologies
Canvas
