#models
# List of logistic regression models

### LogisticRegression
| Kriterium              | Wert |
| ---                    | --- |
| Vorteil                | Simples, klassisches Modell |
| Nachteil               |  |
| Python Import          | from sklearn.linear_model import LogisticRegression | 
| Link zur Dokumentation | https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html |
| Bemerkung              | Penalty Parameter vorhanden: penalty{‘l1’, ‘l2’, ‘elasticnet’, ‘none’}, default=’l2’|

### DecisionTreeClassifier
| Kriterium              | Wert |
| ---                    | --- |
| Vorteil                | die in der Lage sind, eine Mehrklassenklassifizierung für einen Datensatz durchzuführen |
| Nachteil               |  |
| Python Import          | from sklearn import tree | 
| Link zur Dokumentation | https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html#sklearn.tree.DecisionTreeClassifier |
| Bemerkung              |  |

### KNeighborsClassifier
| Kriterium              | Wert |
| ---                    | --- |
| Vorteil                |  |
| Nachteil               |  |
| Python Import          | from sklearn.neighbors import NearestNeighbors | 
| Link zur Dokumentation | https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html |
| Bemerkung              |  |

### RandomForestClassifier
| Kriterium              | Wert |
| ---                    | --- |
| Vorteil                | fits a number of decision tree classifiers on various sub-samples of the dataset and uses averaging to improve the predictive accuracy and control over-fitting. |
| Nachteil               |  |
| Python Import          | from sklearn.ensemble import RandomForestClassifier, make_classification | 
| Link zur Dokumentation | https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html |
| Bemerkung              |  |