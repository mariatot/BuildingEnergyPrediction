# BuildingEnergyPrediction

Projet de prédiction de la consommation énergétique et des émissions de CO2 des bâtiments non résidentiels, basé sur des données structurelles et l’"ENERGY STAR Score". Inclut des étapes de nettoyage, d'analyse exploratoire, de création de nouvelles variables et de modélisation (Gradient Boosting, Ridge).

## Description
Ce projet vise à prédire :  
- **La consommation totale d’énergie** (SiteEnergyUseWN).  
- **Les émissions de CO2** (TotalGHGEmissions).  

Les prédictions s’appuient sur des données structurelles des bâtiments non résidentiels et évaluent l’intérêt de l’"ENERGY STAR Score" comme variable explicative. Le projet s’inscrit dans un objectif de réduction des émissions de carbone d’ici 2050.

## Contenu du projet
1. **Description et nettoyage des données** :  
   - Suppression des lignes/colonnes inutiles ou redondantes.  
   - Traitement des valeurs manquantes et aberrantes.  
   - Transformation de variables (ex. âge du bâtiment, logarithme des cibles).  

2. **Analyse exploratoire** :  
   - Étude des corrélations entre les variables explicatives et les cibles.  
   - Tests statistiques (ANOVA, Kolmogorov-Smirnov).  

3. **Feature Engineering** :  
   - Création de nouvelles variables : pourcentage de surface parking, types d'énergie, etc.  

4. **Modélisation** :  
   - Modèles testés : Dummy Regressor, Ridge, Gradient Boosting, etc.  
   - Sélection finale : **Gradient Boosting Regressor** optimisé par GridSearchCV.  

## Technologies utilisées
- **Python** : pandas, NumPy, scikit-learn, matplotlib, seaborn.  
- **Machine Learning** : Ridge Regression, Gradient Boosting, Random Forest.  

## Résultats
- **Prédiction de la consommation d’énergie** : R² = 0.77, RMSE = 0.560.  
- **Prédiction des émissions de CO2** : R² = 0.83, RMSE = 0.560.  

## Prochaines étapes
- Amélioration des modèles avec d'autres jeux de données.  
- Analyse approfondie des erreurs de prédiction et des variables explicatives.  

Données utilisées : [2016 Building Energy Benchmarking](https://data.seattle.gov/dataset/2016-Building-Energy-Benchmarking/2bpz-gwpy).  


