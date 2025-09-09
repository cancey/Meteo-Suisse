# Météo-Suisse
Des fonctions pour loaliser des stations météorologiques en Suisse et extraire les données.

## Mode d'emploi 
1. initialiser les fonctions spatiales et météo
2. tracer la carte des stations
3. localiser la station d'intérêt et son nom
4. il est toujours possible de filtrer. Par exemple, pour avoir toutes les stations météo du valais, il suffit de taper
        liste_propriétés_stations[liste_propriétés_stations['canton']=='VS']
5. télécharger les données souhaitées. Différentes fonctions sont proposées :
    * télécharger_variable_station : télécharge la série temporelle correspondante à une variable (parmi huit possibles : température, précipitations, etc) pour une station
    * télécharger_toutes_données_station : télécharge la série temporelle correspondante à chaque variable disponible pour une station, Voir la liste des abréviations
      employées par Météo-Suisse pour l'interprétation
    * télécharger_précipitations :  télécharge la série temporelle des précipitations journalières pour une station
    * synthétiser_information_pluviométrique : synthétise l'information pluviométrique pour un ensemble ou la totalité des stations
6. des exemples de figure sont donnés

En principe il est possible de travailler à différentes granularités (selon le pas de temps de la station de mesure), mais tout n'a pas été testé pour l'heure. Et attention au volume de données !

Dernière mise à jour : mardi 9 septembre 2025 ; le reste est à venir (courant septembre ou octobre 2025)

## Sources
* pour les données Météo-Suisse : voir https://www.meteoswiss.admin.ch/services-and-publications/service/open-data.html

* pour la signification des abréviations employées par Météo-Suisse : voir https://data.geo.admin.ch/ch.meteoschweiz.ogd-smn/ogd-smn_meta_parameters.csv

* pour les méta-données sur les postes manuels : https://opendatadocs.meteoswiss.ch/a-data-groundbased/a5-manual-precipitation-stations

* pour les méta-données sur les postes automatiques : https://opendatadocs.meteoswiss.ch/a-data-groundbased/a1-automatic-weather-stations

Pour les données topographiques, des téléchargements externes peuvent être nécessaires (voir la doc au niveau des exemples). Mais on peut faire sans cela en se servant de plotly. Le cahier hydroshed_extraction.ipynb permet de faire extraction des données hydrographiques pour les cartes.
