# Deepki Building Proximity Finder

Ce projet contient un script Python permettant de télécharger des données de bâtiments, d'analyser ces données géographiques, et de déterminer le bâtiment le plus proche du Cristo Redentor à Rio de Janeiro.

## Prérequis

Avant de commencer, vous aurez besoin des éléments suivants :

1. **Python 3.x** : Le script est compatible avec Python 3.
2. **Packages Python nécessaires** :
   - `gdown` : Pour télécharger les fichiers depuis Google Drive.
   - `gzip` : Pour lire les fichiers compressés.
   - `csv` : Pour traiter les fichiers CSV.
   - `geopandas` : Pour manipuler les données géospatiales et effectuer les calculs de distance.
   - `shapely` : Pour manipuler les objets géométriques tels que les points et polygones.

Vous pouvez installer ces packages en utilisant la commande suivante :
```bash
pip install gdown geopandas shapely
```

## Fonctionnement du Script

**Préparer le fichier Google Drive**: 
Téléchargez le fichier open_buildings_v3_polygons_your_own_wkt_polygon.csv.gz depuis le site Google Research Open Buildings.
Uploadez ce fichier dans votre propre Google Drive.

**Récupérer l'ID du fichier Google Drive**:
Pour télécharger le fichier à partir de Google Drive via le script, vous devrez obtenir l'ID du fichier :

Allez dans votre Google Drive et localisez le fichier téléchargé.
Faites un clic droit sur le fichier et sélectionnez Obtenir le lien.
Assurez-vous que le fichier est partagé avec la permission "Quiconque disposant du lien".

Exemple URL :
```bash
https://drive.google.com/file/d/1R1KjJBdFOZzrytrixJukI1a40s0UCNOm/view?usp=sharing
```
L'ID du fichier correspond à la chaîne entre /d/ et /view. Dans cet exemple, l'ID est :
```bash
1R1KjJBdFOZzrytrixJukI1a40s0UCNOm
``` 
