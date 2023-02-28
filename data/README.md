# data
In unserem "data" Repository speichern wir alle Datensätze ab, welche wir für diese Challenge bekommen haben, oder selbst erstellt haben.

## Originale Datensätze
Folgende Datensätze haben wir von unserem Dozent @fbenites erhalten. 


| Dateiname                   | Beschreibung                                                                                                              |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| immo_data_202208.csv        | Erster erhaltener Datensatz.                                                                                              |
| immo_data_202208_v2.parquet | Zweiter erhaltener Datensatz. Dieser hat verglichen zum ersten Datensatz mehr Observationen und Features.                 |
| kaggle_uncleaned.parquet    | Kaggle Kompetitionsdatensatz. Dieser ist wie der immo_data_202208_v2.parquet Datensatz aufgebaut, jedoch fehlt der Preis. |

## Bereinigte Datensätze
Folgende Datensätze sind unsere bereinigten Versionen der Datensätze, welche wir für die Challenge erhalten haben.


| Dateiname                  | Beschreibung                                         |
| -------------------------- | ---------------------------------------------------- |
| clean_gde.csv              | Bereinigte Version vom ersten erhaltenen Datensatz.  |
| clean_gde_v2.csv           | Bereinigte Version vom zweiten erhaltenen Datensatz. |
| kaggle_gde_cleaned.parquet | Bereinigte Version vom Kaggle Datensatz.             |

## Bereinigte Datensätze ohne Ortsinformationen
Folgende Datensätze sind unsere bereinigten Versionen der Datensätze, welche wir für die Challenge erhalten haben. Jedoch fehlen hier die Ortsinformationen.


| Dateiname              | Beschreibung                                                                |
| ---------------------- | --------------------------------------------------------------------------- |
| clean.csv              | Bereinigte Version vom ersten erhaltenen Datensatz ohne Ortsinformationen.  |
| clean_v2.csv           | Bereinigte Version vom zweiten erhaltenen Datensatz ohne Ortsinformationen. |
| kaggle_cleaned.parquet | Bereinigte Version vom Kaggle Datensatz ohne Ortsinformationen.             |

## Ortsinformationen für jede Postleitzahl
Folgender Datensatz wurde aus den bereinigten Daten generiert. Hier sind zu jeder Postleitzahl informationen zu diesem Ort aufgelistet.


| Dateiname        | Beschreibung                                                                                                                    |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| plz_data.parquet | Aus clean_gde_v2.csv generierte Ortsinformationen. Fehlende Werte wurden aus kaggle_gde_cleaned.parquet gefüllt oder imputiert. |

## Andere
Hier sind weitere Datensätze aufgelistet.


| Dateiname                  | Beschreibung                                                                                          |
| -------------------------- | ----------------------------------------------------------------------------------------------------- |
| plz_verzeichnis_v2.geojson | Datensatz der Post zu den Postleitzahlen in der Schweiz inkl. geometrische Formen jeder Postleitzahl. |
| plz.xlsx                   | Datensatz von postleitzahlenschweiz.ch, um vorhandene Postleitzahlen und Gemeindenamen zu validieren. |
