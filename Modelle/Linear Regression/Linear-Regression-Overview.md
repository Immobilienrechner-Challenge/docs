#models 
# List of linear regression models

### LinearRegression
| Kriterium              | Wert |
| ---                    | --- |
| Vorteil                | Simples, klassisches Modell |
| Nachteil               |  |
| Python Import          | from sklearn.linear_model import LinearRegression | 
| Link zur Dokumentation | https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html |
| Bemerkung              | |

### Ridge
| Kriterium              | Wert |
| ---                    | --- |
| Vorteil                | Gute Gegenmassnahme gegen Overfitting |
| Nachteil               | Bei zu hohen lambda Werten wird das Model underfitted  |
| Python Import          | from sklearn.linear_model import Ridge | 
| Link zur Dokumentation | https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Ridge.html |
| Bemerkung              |  |

### Lasso
| Kriterium              | Wert |
| ---                    | --- |
| Vorteil                | Gute Gegenmassnahme gegen Overfitting, irrelevante Parameter werden ab einem bestimmten lambda Wert zu 0 |
| Nachteil               | Bei zu hohen lambda Werten wird das Model underfitted |
| Python Import          | from sklearn.linear_model import Ridge | 
| Link zur Dokumentation | https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Lasso.html |
| Bemerkung              |  |

### Elastic-Net
| Kriterium              | Wert |
| ---                    | --- |
| Vorteil                |  |
| Nachteil               |  |
| Python Import          | from sklearn.linear_model import ElasticNet | 
| Link zur Dokumentation | https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.ElasticNet.html |
| Bemerkung              | Kombination von Ridge und Lasso Regularisierung |

### GradientBoostingRegressor
| Kriterium              | Wert |
| ---                    | --- |
| Vorteil                |  |
| Nachteil               |  |
| Python Import          | from sklearn.ensemble import GradientBoostingRegressor | 
| Link zur Dokumentation | https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.GradientBoostingRegressor.html |
| Bemerkung              |  |

### xgboost
| Kriterium              | Wert |
| ---                    | --- |
| Vorteil                |  |
| Nachteil               |  |
| Python Import          | import xgboost | 
| Link zur Dokumentation | https://xgboost.readthedocs.io/en/stable/python/python_intro.html |
| Bemerkung              |  |

### HuberRegressor
| Kriterium              | Wert |
| ---                    | --- |
| Vorteil                |  |
| Nachteil               |  |
| Python Import          | from sklearn.linear_model import HuberRegressor, LinearRegression | 
| Link zur Dokumentation | https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.HuberRegressor.html |
| Bemerkung              |  |

### Theil-Sen Regression
| Kriterium              | Wert |
| ---                    | --- |
| Vorteil                |  |
| Nachteil               |  |
| Python Import          | from sklearn.linear_model import LinearRegression, TheilSenRegressor | 
| Link zur Dokumentation | https://scikit-learn.org/stable/auto_examples/linear_model/plot_theilsen.html |
| Bemerkung              |  |
