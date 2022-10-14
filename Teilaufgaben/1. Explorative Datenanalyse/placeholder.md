# Zur Verfügung gestellte Features
Das zur Verfügung gestellte Datenset wurde als `.csv`-Datei abgespeichert und beinhaltet `13378` Zeilen und `108` Spalten. Von diesen 108 Spalten sind aber viele in mehrere Spalten aufgeteilt abgelegt, weshalb wir zunächst alle Informationen zu einer Variable in einer Spalte gesammelt haben.

## Immobilien-Attribute
Unter den `Immobilien-Attributen` fassen wir Variablen zusammen, die eine Immobilie am direktesten definieren. Dazu zählen wir

### Wohnfläche 
`float`  
Laut [swisslife](https://www.swisslife.ch/de/private/blog/immo/so-berechnen-sie-die-wohnflaeche.html) gibt es keine einheitliche und rechtsverbindliche Definition, wie eine Wohnung ausgemessen werden muss. Laut Wikipedia handelt es sich hierbei um einen bestimmenden Faktor für den Mietzins / Kaufpreis

| Count | Range | Mean | Std | Min | Max |
| ----  | ----- | ---- | --- | --- | --- |
| 12686 | 50 - 180 | 177 | 273 | 1 | 9681|

### Zimmeranzahl
`float`  
Als ganze Räume werden bei der Vermietung oder beim Verkauf einer Wohnung folgende Räume gezählt: Wohnzimmer, Schlafzimmer, Arbeitszimmer, Kinderzimmer. Offiziell existiert auch keine richtige Definition für ein halbes Zimmer, sodass diese Angaben nur zur Orientierung verwendet werden können. Nicht als Zimmer gezählt werden Badezimmer, Dusche und Küche [Immoscout DE](https://www.immoscout24.ch/de/c/d/immobilien-magazin/definition-halbes-zimmer-schweiz?a=4569)

| Count | Range | Mean | Std | Min | Max |
| ----  | ----- | ---- | --- | --- | --- |
| 12799 | 1-10 | 5.16 | 2.212 | 1.5 | 29 |

### Grundstücksfläche
`float`   
Die Grundstücksfläche gibt die Gesamtgröße eines (Bau-)Grundstücks an und wird in Quadratmetern bemessen. [Immoscout](https://www.immobilienscout24.de/wissen/verkaufen/grundstuecksflaeche.html)

| Count | Range | Mean | Std | Min | Max |
| ----  | ----- | ---- | --- | --- | --- |
| 4953 | 300 - 1200 | 934.84 | 1174.53 | 10 | 9681|

### Nutzfläche
`float`  
Mit der Nutzfläche (kurz: NF) wird der Teil der Gebäudegrundfläche bezeichnet, der gemäß der jeweiligen Zweckbestimmung genutzt werden kann. Welche Räume als Nutzfläche zählen und welche nicht, erfährst Du in diesem Beitrag. [Immoscout DE](https://www.immobilienscout24.de/wissen/bauen/nutzflaeche.html)
| Count | Range | Mean | Std | Min | Max |
| ----  | ----- | ---- | --- | --- | --- |
| 2953 |  | 208 | 269.95 | 4 | 7549|

### Stockwerk
`float`  
Stockwerk, auf welchem sich die Immobilie befindet (wohl nur für Wohnungen interessant, weniger für Häuser).  
| Count | Range | Mean | Std | Min | Max |
| ----  | ----- | ---- | --- | --- | --- |
| 5620 | -1 - 10 | 177 | 273 | -4  | 999 |


### Typ
`factor`  
Kompletter Datensatz  

Werte: 
| Typ | Anzahl | Beschreibung |
| --- | ------ | ------------ |
| `penthouse` | 554 | |
| `terrace-house` | 526 | | 
| `detached-house` | 3568 | |
| `flat` | 5995 | |
| `stepped-house` | 66 | |
| `farmhouse` | 110 | |
| `semi-detached-house` | 592 | |
| `stepped-apartment` | 140 | |
| `duplex-maisonette` | 430 | |
| `attic-flat` | 239 | |
| `loft` | 26 | |
| `chalet` | 284 | |
| `villa` | 718 | |
| `attic-room` | 6 | |
| `secondary-suite` | 1 | |
| `castle` | 9 | |
| `detached-secondary-suite` | 4 | |
| `studio` | 27 | |
| `furnished-residental-property` | 17 | |
| `rustico` | 65 | |
| `single-room` | 1 | |


## Lokalität
Für alle Count: 13378
- Gemeinde
- Strasse (Strassenname und Nummer)
- Postleitzahl
- Kanton
- Latitude
- Longitude

## Verfügbarkeit
Count: 13378

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
Preis