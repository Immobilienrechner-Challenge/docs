# immoprice-backend
Dieses Backend basiert auf Django v4.1.3. Dependencies werden [hier](https://github.com/Immobilienrechner-Challenge/immoprice-backend/blob/main/requirements.txt) aufgelistet.

## Setup
Um die API auf einer Docker Umgebung zu nutzen, muss man die vorgefertigte Datei [create_docker_container.sh](https://github.com/Immobilienrechner-Challenge/immoprice-backend/blob/main/create_docker_container.sh) starten und den Container Port 8099 durch einen nginx Reverse Proxy freigeben. 

### Setup ohne Reverse Proxy
Falls man die API nicht hinter ein nginx Reverse Proxy laufen lassen will, müsste man die Netzwerkeinstellungen in der [create_docker_container.sh](https://github.com/Immobilienrechner-Challenge/immoprice-backend/blob/main/create_docker_container.sh) Datei anpassen:

![Einstellung Docker](https://github.com/Immobilienrechner-Challenge/docs/raw/main/immoprice-backend/img/EinstellungDocker.png)

## Hosting
Das Hosting des Backends findet auf einer Docker Umgebung statt. Alle Anfragen werden durch den Reverse Proxy von [https://api.immoprice.ch](https://api.immoprice.ch) auf das Backend weitergeleitet. 

![Immoprice Hosting](https://github.com/Immobilienrechner-Challenge/docs/raw/main/immoprice-backend/img/Setup.png)

## Schnittstellen
Nachfolgend wurde die Struktur der relevanten Schnittstelle erfasst:

| model1       | |
|:---|:---|
| URL          | [model1/](https://api.immoprice.ch/model1/) |
| Request Type | GET |
| Beschreibung | Modell zur Vorhersage von Immobilienpreisen auf [immoprice.ch](https://immoprice.ch) |
| Input 1 | living_space(float) |
| Input 2 | type(string) |
| Input 3 | rooms(float) |
| Input 4 | zip_code(int) |
| Input 5 | floor_space(float) |
| Input 6 | plot_area(float) |
| Input 7 | last_refurbishment(int) |
| Input 8 | year_built(int) |
| Output       | price(float) |
| Beispiel     | [Hier](https://api.immoprice.ch/model1/?living_space=200&type=villa&rooms=10&zip_code=8050&floor_space=300&plot_area=500&last_refurbishment=2020&year_built=2010) |

### Swagger Dokumentation
Eine Swagger Dokumentation zu dieser Schnittstelle ist unter [https://app.swaggerhub.com/apis-docs/GABRIELTORRES/immoprice.ch/1.0.0](https://app.swaggerhub.com/apis-docs/GABRIELTORRES/immoprice.ch/1.0.0) verfügbar.

### Bekannte Probleme
Das Modell wurde nur auf einer kleinen Stichprobe von Daten aus der Schweiz trainiert. Deswegen können einige Prognosen eine starke Abweichung vom realen Preis haben.
Das Modell ist nicht in der Lage spezielle Fälle, wie z.B. wertvolle Aussichten, Immobilienlage an einem speziellen Ort, Innenausstattung oder historische Signifikanz miteinzuberechnen. 

## Cross-Origin Restrictions
Es können Cross-Origin-Restriction-Fehler auftreten, da die API so konfiguriert ist, Anfragen von https://immoprice.ch zu verarbeiten. Falls dies auftritt, muss die entsprechende Option im Browser manuell deaktiviert werden.