# Stage-4eme-annee

# Traitement de données acoustiques passives

Les données sont recueillies à l'aide d'hydrophones attachés sur des éléphants de mer.

## I) Prédiction de la force du vent

A partir de ces données, il faut prédire la fort du vent à chaque heure.

Il y a un premier travail sur les données qui consiste à les formatter correctement. Ensuite il faut se ramener à l'échelle de temps qui nous intéresse : l'heure. Car il arrive qu'il y ait plusieurs mesures dans une même heure.

Afin d'arriver à faire des prédictions sur nos données, la première étape était d'entrainer plusieurs modèles (un modèle de forêt d'arbres de décision et un modèle de deep learning) sur des bases de données déjà labellisées.

Finalement nous obtenons ces résultats à l'aide du transfert d'apprentissage :
![screenshot1](https://github.com/Bessouat40/dashboard_accidents_de_la_route/blob/main/page_1_1.PNG?raw=true)
