## But du projet

## Disposition du dépôt
* heart-notebook.ipynb : Contient la totalité du projet réalisé
* heart_2020_cleaned.csv : Dataset disponible sur Kaggle
## Pré-requis logiciels 
Python 3.8 et +
Ainsi que les packages suivant : 
- Numpy
- Pandas
- Seaborn
- Scikit-learn
- Matplotlib
## Contenu du projet
1. Chargement des données
2. Analyse globale des données du dataset
3. Ensemble de visualisation des données et analyse de la corrélation entre les différentes variables
4. Application d'un ensemble d'algorithmes de classification en analysant les performances en test : 
    - Random Forrest
    - Extremely Randomized tree
    - Adaboost
    - Gradient Tree Boosting
5. Resampling des données 

## Performances atteintes
### Avant augmentation des données
|   Algorithme choisi    |   Précision en test (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   Random Forrest              |   90.56   |   88.31   |
|   Extremely randomized Tree   |   89.83   |   88.25   |
|   AdaBoost                    |   91.69   |   89.05   |
|   Gradient Tree Boosting      |   91.77   |   89.02   |
### Après augmentation des données
On a fait un up-sampling des données de la classe minoritaire : 
|   Classe    |   Nombre avant augmentation |  Nombre après augmentation |
|---      |:-:        |:-:         |
|   No    |  292422   |   292422   |
|   Yes   |  27373    |   120000   |
Et on a eu les résultats suivant avec les même algorithmes :
|   Algorithme choisi    |   Précision en test (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   Random Forrest              |   94.8    |   94.88   |
|   Extremely randomized Tree   |   95.09   |   95.14   |
|   AdaBoost                    |   78.62   |   77.59   |
|   Gradient Tree Boosting      |   79.12   |   78.53   |
## Remarques
- L'augmentation des données a eu un effet bénéfique sur le Random Forrest et l'Extremely randomized Tree
- L'augmentation des données a eu un effet négatif sur les deux autre algorithmes 
## A faire
- Features selection