# Zur Verfügung gestellte Features
Das zur Verfügung gestellte Datenset wurde als `.csv`-Datei abgespeichert und beinhaltet `13378` Zeilen und `108` Spalten. Von diesen 108 Spalten sind aber viele Features in mehrere Spalten aufgeteilt abgelegt, weshalb wir zunächst alle Informationen zu einer Variable in einer Spalte gesammelt haben. Zudem wurden mit `pd.drop_duplicates()` doppelte Einträge entfernt und nicht gültige Werte wurden entfernt.  
Damit erhalten wir ein Datenset von `13048` Zeilen und `63` Spalten:

## Immobilien-Attribute
Unter den `Immobilien-Attributen` fassen wir Variablen zusammen, die eine Immobilie am direktesten definieren. Dazu zählen wir

### Wohnfläche 
Name : `living_space`  
Typ: `float`  
Laut [swisslife](https://www.swisslife.ch/de/private/blog/immo/so-berechnen-sie-die-wohnflaeche.html) gibt es keine einheitliche und rechtsverbindliche Definition, wie die Wohnfläche ausgemessen werden muss. Laut Wikipedia handelt es sich hierbei um einen bestimmenden Faktor für den Mietzins / Kaufpreis

| Count | Mean | Std | Min | Max |
| ----  | ---- | --- | --- | --- |
| 11981 |  158 | 108 | 12 | 1450|

### Zimmeranzahl
Name: `rooms`  
Typ: `float`  
Als ganze Räume werden bei der Vermietung oder beim Verkauf einer Wohnung folgende Räume gezählt: 
- Wohnzimmer
- Schlafzimmer
- Arbeitszimmer
- Kinderzimmer  

Offiziell existiert aber keine Definition dafür, was als ein halbes Zimmer zählt, sodass diese Angaben nur zur Orientierung verwendet werden können. Nicht als Zimmer gezählt werden Badezimmer, Dusche und Küche [Immoscout CH](https://www.immoscout24.ch/de/c/d/immobilien-magazin/definition-halbes-zimmer-schweiz?a=4569)

| Count | Mean | Std | Min | Max |
| ----  | ---- | --- | --- | --- |
| 12487 | 5.2 | 2.22 | 1.5 | 29 |

### Grundstücksfläche
Name: `plot_area`  
Typ: `float`   
Die Grundstücksfläche gibt die Gesamtgröße eines (Bau-)Grundstücks an und wird in Quadratmetern bemessen. [Immoscout DE](https://www.immobilienscout24.de/wissen/verkaufen/grundstuecksflaeche.html)

| Count | Mean | Std | Min | Max |
| ----  | ---- | --- | --- | --- |
| 4829  | 1k  | 5472 | 10  | 247k|

### Nutzfläche
Name: `floor_space`  
Typ: `float`  
Mit der Nutzfläche (kurz: NF) wird der Teil der Gebäudegrundfläche bezeichnet, der gemäß der jeweiligen Zweckbestimmung genutzt werden kann. Welche Räume als Nutzfläche zählen und welche nicht, schreibt [Immoscout DE](https://www.immobilienscout24.de/wissen/bauen/nutzflaeche.html)  

| Count | Mean | Std | Min | Max |
| ----  | ---- | --- | --- | --- |
| 2859  |  209 | 273 | 4   | 7549|

### Stockwerk
Name: `floor`  
Typ: `float`  
Stockwerk, auf welchem sich die Immobilie befindet (wohl nur für Wohnungen interessant, weniger für Häuser).  

| Count |  Median | Std | Min | Max |
| ----  | ----  | --- | --- | --- |
| 5458  |  1.0    | 2.39 | -4  | 23 |


### Typ
Name: `type`  
Typ: `factor`  


| Typ | Anzahl | Beschreibung |
| --- | ------ | ------------ |
| `flat` | 5841 | |
| `detached-house` | 3476 | |
| `villa` | 701 | |
| `semi-detached-house` | 570 | |
| `penthouse` | 540 | |
| `terrace-house` | 510 | | 
| `duplex-maisonette` | 425 | |
| `chalet` | 280 | |
| `attic-flat` | 239 | |
| `stepped-apartment` | 139 | |
| `farmhouse` | 108 | |
| `rustico` | 65 | |
| `stepped-house` | 64 | |
| `studio` | 27 | |
| `loft` | 25 | |
| `furnished-residental-property` | 17 | |
| `castle` | 9 | |
| `attic-room` | 6 | |
| `detached-secondary-suite` | 4 | |
| `secondary-suite` | 1 | |
| `single-room` | 1 | |


## Lokalität
### Gemeinde
Name: `municipality`  
Typ: `string`

| Count | Distinct |
| ----  | -------- |
| 13036 | 1295     |

### Strasse
Name: `street`  
Typ: `string`

| Count | Distinct |
| ----  | -------- |
| 5843  | 3511     |

### Nummer
Name: `street_nr`  
Typ: `string`

| Count | Distinct |
| ----  | -------- |
| 2697  | 451      |

### Postleitzahl
Name: `zip_code`  
Typ: `int`

| Count | Distinct |
| ----  | -------- |
| 13048 | 1943     |

### Kanton
Name: `canton`  
Typ: `categorical`

| Count | Distinct |
| ----  | -------- |
| 13048 | 26       |

### Latitude
Name: `Latitude`  
Typ: `float`

| Count | Distinct |
| ----  | -------- |
| 13048 | 2821     |

### Longitude
Name: `Longitude`  
Typ: `float`

| Count | Distinct |
| ----  | -------- |
| 13048 | 2821     |


## Verfügbarkeit  
Name: `availability`  
Typ: `string`
| Count | Distinct |
| ----  | -------- |
| 13057 | 112      |

## Gemeinde spezifische Daten
ForestDensityL
ForestDensityM
ForestDensityS
Die Korrelieren vermutlich, wenn bestätigt, nur eine verwenden

NoisePollutionRailwayL
NoisePollutionRailwayM
NoisePollutionRailwayS
Die Korrelieren vermutlich, wenn bestätigt, nur eine verwenden

NoisePollutionRoadL
NoisePollutionRoadM
NoisePollutionRoadS
Die Korrelieren vermutlich, wenn bestätigt, nur eine verwenden

PopulationDensityL
PopulationDensityM
PopulationDensityS
Die Korrelieren vermutlich, wenn bestätigt, nur eine verwenden

RiversAndLakesL
RiversAndLakesM
RiversAndLakesS
Die Korrelieren vermutlich, wenn bestätigt, nur eine verwenden

WorkplaceDensityL
WorkplaceDensityM
WorkplaceDensityS
Die Korrelieren vermutlich, wenn bestätigt, nur eine verwenden

distanceToTrainStation

gde_area_agriculture_percentage
gde_area_forest_percentage
gde_area_nonproductive_percentage
gde_area_settlement_percentage
gde_average_house_hold
gde_empty_apartments
gde_foreigners_percentage
gde_new_homes_per_1000
gde_politics_bdp
gde_politics_cvp
gde_politics_evp
gde_politics_fdp
gde_politics_glp
gde_politics_gps
gde_politics_pda
gde_politics_rights
gde_politics_sp
gde_politics_svp
gde_pop_per_km2
gde_population
gde_private_apartments
gde_social_help_quota
gde_tax
gde_workers_sector1
gde_workers_sector2
gde_workers_sector3
gde_workers_total


## Zielvariable
Name: `price`  
Typ: `float`

| Count | Mean | Std | Min | Max |
| ----  | ---- | --- | --- | --- |
| 12026 | 1.2M | 1.4M | 30k | 45M |