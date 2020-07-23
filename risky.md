#Unit 11 HW 
## Risky Business
### Alex Waters 7/21/20
---
**Resampling**

**Naive Random Oversampling**
*balanced accuracy score*= 0.6435975843133463
*confusion matrix*
array([[   53,    34],
       [ 5512, 11606]]

*imbalaced classification report*       
                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.61      0.68      0.02      0.64      0.41        87
   low_risk       1.00      0.68      0.61      0.81      0.64      0.42     17118

avg / total       0.99      0.68      0.61      0.80      0.64      0.42     17205
      
---       
SMOTE Oversampling
*balanced accuracy score*=0.6401801290031466
*confusion matrix*
array([[   53,    34],
       [ 5629, 11489]]
       
*imbalaced classification report*      
                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.61      0.67      0.02      0.64      0.41        87
   low_risk       1.00      0.67      0.61      0.80      0.64      0.41     17118

avg / total       0.99      0.67      0.61      0.80      0.64      0.41     17205
---
Undersampling with Cluster Centroids algorithm
*balanced accuracy score*=0.6401801290031466
*confusion matrix*
array([[   55,    32],
       [10078,  7040]]
       
*imbalaced classification report* 
                  pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.63      0.41      0.01      0.51      0.27        87
   low_risk       1.00      0.41      0.63      0.58      0.51      0.25     17118

avg / total       0.99      0.41      0.63      0.58      0.51      0.25     17205
---
Combination (Over and Under) Sampling using SMOTEENN algorithm
*balanced accuracy score*=0.5217234530298819
*confusion matrix*
array([[  65,   22],
       [7178, 9940]]
*imbalaced classification report* 
                   pre       rec       spe        f1       geo       iba       sup

  high_risk       0.01      0.75      0.58      0.02      0.66      0.44        87
   low_risk       1.00      0.58      0.75      0.73      0.66      0.43     17118

avg / total       0.99      0.58      0.75      0.73      0.66      0.43     17205
---
**Questions**
1. Which model had the best balanced accuracy score? 
    The Naive Random Oversampling had a slightly better score than the SMOTE Oversampling or the combination with SMOTEENN.
2. Which model had the best recall score?
    The Naive Random Oversampling had a slightly better recall score average than the other three models.
3. Which model had the best geometric score?
    The Cluster Centroids had the lowest geometric mean score.
---
---
**Ensemble Learning**
Balanced Random Forest Classifier
*balanced accuracy score*=0.7877672625306695
*confusion matrix*
array([[   58,    29],
       [ 1560, 15558]]
*imbalaced classification report* 
                  pre       rec       spe        f1       geo       iba       sup

  high_risk       0.04      0.67      0.91      0.07      0.78      0.59        87
   low_risk       1.00      0.91      0.67      0.95      0.78      0.62     17118

avg / total       0.99      0.91      0.67      0.95      0.78      0.62     17205


Easy Ensemble AdaBoost Classifier
*balanced accuracy score*=0.9097552082703828
*confusion matrix*
array([[   73,    14],
       [  335, 16783]]
*imbalaced classification report* 
                  pre       rec       spe        f1       geo       iba       sup

  high_risk       0.18      0.84      0.98      0.29      0.91      0.81        87
   low_risk       1.00      0.98      0.84      0.99      0.91      0.83     17118

avg / total       1.00      0.98      0.84      0.99      0.91      0.83     17205

Questions
1. Which model had the best balanced accuracy score?
    The AdaBoost Classifier had the best balanced accuracy score.
2. Which model had the best recall score?
    The AdaBoost Classifier had the highest recall score.
3. Which model had the best geometric mean score?
    The AdaBoost had the best geometric score.
4. What are the top three features?
    Precision, recall and f1 score.  All of the scores where in the high 90's and a quick look at the confusion matric shows low false positives and elevated false negatives, but compare to random forest the numbers were much better.

