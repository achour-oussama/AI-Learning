# Exercice : Analyse et Prédiction sur le Dataset du Titanic

## Étape 1 : Chargement et exploration initiale
Chargez le fichier de données `train.csv` dans un DataFrame nommé `df`. Affichez ses premières lignes, déterminez ses dimensions exactes (nombre de lignes et de colonnes) et listez les noms de toutes les variables disponibles.

## Étape 2 : Diagnostic des données manquantes
Analysez la structure technique de votre DataFrame. Identifiez précisément quelles colonnes contiennent des valeurs manquantes et calculez le nombre exact de données manquantes pour chacune d'elles.

## Étape 3 : Statistiques descriptives par groupe
Calculez le nombre total de rescapés et de victimes. Ensuite, déterminez le taux de survie moyen selon le sexe des passagers, puis selon leur classe de voyage, afin d'observer les premiers facteurs d'influence.

## Étape 4 : Nettoyage du dataset
Traitez les données manquantes identifiées à l'étape 2 : 
* Remplacez les valeurs manquantes de la colonne des âges par la valeur médiane de cette colonne.
* Remplacez les valeurs manquantes de la colonne d'embarquement par la valeur la plus fréquente (le mode).
* Supprimez définitivement la colonne des cabines car elle contient trop de données manquantes pour être exploitable.

## Étape 5 : Encodage des variables catégorielles
Les variables liées au sexe et au port d'embarquement contiennent du texte. Transformez ces variables textuelles en variables numériques afin qu'elles puissent être interprétées par un modèle de Machine Learning.

## Étape 6 : Visualisation de données
Utilisez une bibliothèque graphique pour générer deux visualisations :
* Un graphique en barres représentant le taux de survie en fonction de la classe des passagers.
* Un histogramme affichant la distribution des âges des passagers.

## Étape 7 : Séparation des données (Split Train/Test)
Isolez la variable cible (ce que l'on cherche à prédire) des variables explicatives (les caractéristiques des passagers). Divisez ensuite votre jeu de données en deux ensembles distincts : un ensemble d'entraînement et un ensemble de test (avec une proportion de 80% / 20%).

## Étape 8 : Entraînement et prédiction d'un premier modèle
Créez et entraînez un modèle de régression logistique sur vos données d'entraînement. Utilisez ensuite ce modèle pour prédire la survie des passagers de votre ensemble de test.
