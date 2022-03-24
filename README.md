# Personal Key Indicators of Heart Disease
## Goal of the project
The goal of this project is to implement a classifier allowing the prediction of whether a patient may have heart disease based on personal indicators. The dataset can be found on Kaggle [here].(https://www.kaggle.com/kamilpytlak/personal-key-indicators-of-heart-disease)
## Repository layout
* heart-notebook.ipynb : Contains the whole project
* heart_2020_cleaned.csv : Dataset used
## Software requirements 
Python 3.8 and more
As well as the following packages : 
- Numpy
- Pandas
- Seaborn
- Scikit-learn
- Matplotlib
## Content of the project
1. Data loading
2. Global analysis of the dataset
3. Data visualization set and analysis of the correlation between the different variables
4. Application of a set of classification algorithms by analyzing the performance in test : 
    - Random Forrest
    - Extremely Randomized tree
    - Adaboost
    - Gradient Tree Boosting
5. Resampling of the data 

## Performance achieved
### Before data augmentation
|   Algorithm    |   Accuracy (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   Random Forrest              |   90.56   |   55.31   |
|   Extremely randomized Tree   |   89.83   |   57.07   |
|   AdaBoost                    |   91.69   |   56.65   |
|   Gradient Tree Boosting      |   91.77   |   56.19   |

### After up-sampling the data
We did an up-sampling of the data of the minority class : 
|   Classe    |   Before data augmentation |  After data augmentation |
|---      |:-:        |:-:         |
|   No    |  292422   |   292422   |
|   Yes   |  27373    |   120000   |

And we got the following results with the same algorithms:

|   Algorithme choisi    |   Précision en test (%)|  F1 score (%) |
|---      |:-:        |:-:        |
|   Random Forrest              |   94.8    |   93.86   |
|   Extremely randomized Tree   |   95.09   |   94.15   |
|   AdaBoost                    |   78.62   |   71.63   |
|   Gradient Tree Boosting      |   79.12   |   73.20   |
## Notes
- The increase in data had a beneficial effect on the Random Forrest and the Extremely randomized Tree
- The increase of the data had a negative effect on the two other algorithms 
## Conclusion 
In a case like this one where there is a big imbalance between classes, it is preferable to think of making a resampling of our data allowing us to balance the classes, it was noticed at the level of this project by improving greatly the performance.
## To do
- Features selection