# VizElections
=====================
# Présentation
VizElections permet de : 
- visualiser les taux d'abstention sur Paris par arrondissement et par scrutin et d'étudier la corrélation éventuelle de ce taux avec le revenu médian de la population
- visualiser les résultats des différentes élections en cliquant sur un arrondissement et en choissant un scrutin
![Chaîne de traitement](https://github.com/cwamgis/VizElections/99_doc/chaine.png)
![Résultats](https://github.com/cwamgis/Boot2GeoportalCluster/blob/master/images/architecture_logiciel.png)

# Données
Cette application exploite les données suivantes : 
- les données des élections de 2007 à 2014 de la ville de Paris disponibles sur le site opendata au format json
- les données INSEE/DGFIP, revenus fiscaux localisés des ménages
- la couche géographique des arrondissements de Paris l'APUR (couche shp convertie en kml)

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


# Description du fonctionnement
# Technologies
