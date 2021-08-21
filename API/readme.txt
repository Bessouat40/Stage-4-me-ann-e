Instructions d'utilisation du code :

	- Ouvrir le code auto_cdsapi dans GoogleColab,

	- Créer un dossier csv dans l'espace de travail (clic droit dans l'espace de travail, nouveau dossier),

	- Inclure le csv contenant les colonnes : year, month, day, hour, long, lat, prof. 
	  Ce csv donne les informations gps pour chaque heure.

	- Dans la cellule numéro 4 : 
		- Indiquer sa clé utilisateur (clé qu'on peut retrouver dans le lien présent dans la cellule de code),
		- Ne pas changer la variable "variable" (je ne sais pas si l'algo se généralise très bien pour d'autres variables),
		- Dans la variable "year", indiquer avec une chaîne de caractère les années dont on souhaite récupérer les relevés,
		- Variable month : même principe que variable year,
		- Ne pas toucher aux variables "day" et "time", ce n'est pas nécessaire,
		- La variable "area" correspond à la zone géographique dans laquelle on souhaite obtenir les relevés.
		  Il faut la remplir comme ceci : [Nord, Ouest, Sud, Est],
		- Variable "nom_fichier" : correspond juste au nom de notre fichier csv final.

          POUR TOUTES LES VARIABLES, IL FAUT AJOUTER UNE VIRGULE AVANT DE FERMER LES CROCHETS !!!

	  Ex : month = ['10', '11',] -> valide
	       month = ['10', '11'] -> pas valide

	- Exécuter toutes les cellules jusqu'à celle qui appelle la fonction "creation_finale",
	  Dans l'exécution de cette cellule, juste remplacer le premier argument de la fonction par le nom du fichier csv qui est à l'intérieur du dossier csv de colab.
 
	  Ex : Si dans le dossier colab "csv", j'ai mis un dossier csv contenant les coordonnées gps des données : "ml18_294b_coord_finale.csv", 
	       alors le premier argument de ma fonction creation_finale sera "ml18_294b_coord_finale".

	- On exécute ensuite la cellule. Quand elle aura fini de son exécution, dans le dossier csv de colab, il y aura un fichier csv "nom_fichier_final.csv", 
	  on fait un clic droit dessus, et on clic sur télécharger.