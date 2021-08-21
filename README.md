# Stage-4eme-annee

# Traitement de données acoustiques passives

Les données sont recueillies à l'aide d'hydrophones attachés sur des éléphants de mer.

## I) Prédiction de la force du vent

A partir de ces données, il faut prédire la fort du vent à chaque heure.

Il y a un premier travail sur les données qui consiste à les formatter correctement. Ensuite il faut se ramener à l'échelle de temps qui nous intéresse : l'heure. Car il arrive qu'il y ait plusieurs mesures dans une même heure.

Afin d'arriver à faire des prédictions sur nos données, la première étape était d'entrainer plusieurs modèles (un modèle de forêt d'arbres de décision et un modèle de deep learning) sur des bases de données déjà labellisées.

Finalement nous obtenons ces résultats à l'aide du transfert d'apprentissage :

- Résultats pour les données du premier spécimen :
![screenshot1](https://github.com/Bessouat40/Stage-4eme-annee/blob/main/Capture1.PNG?raw=true)

- Résultats pour les données du deuxième spécimen :
![screenshot1](https://github.com/Bessouat40/Stage-4eme-annee/blob/main/Capture2.PNG?raw=true)

- Résultats pour les données du troisième spécimen :
![screenshot1](https://github.com/Bessouat40/Stage-4eme-annee/blob/main/Capture3.PNG?raw=true)

## II) Prédiction du taux de précipitation (pluie) :

Pour cette partie, il a fallu d'abord détecter les évènements de pluie (une heure pendant laquelle il pleut plus de 1 millimètre), puis prédire le taux de précipitation pour ces évènements.
Il nous a donc fallu deux algorithmes : un classifieur pour détecter les évènements, et un régresseur pour estimer le niveau de pluie.

Les résultats obtenus pendant l'entrainement des classifieurs et des régresseurs étaient satisfaisants, mais les algorithmes se généralisaient mal. Nous n'avons donc pas pu transférer ces algorithmes à nos données.

## III) Présence de chants de poissons lanterne :

Afin de déterminer la présence de chants (chorus) de poissons lanterne, il a fallu visualiser nos données.
Nous n'avons finalement pas trouvé de signatures acoustiques permettant de conclure sur leur présence.

Toutefois, il y a eu un premier travail d'automatisation de détection de présence acoustique.
Je me suis principalement intéressé à l'explicabilité de ce réseau de neurones.
N'ayant pas eu assez de temps, le réseau de neurones ne fonctionnait pas correctement et donc l'explicabilité de l'algorithme ne permet pas de vérifier la pertinence du réseau de neurones.
