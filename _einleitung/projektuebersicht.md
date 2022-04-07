# Projektübersicht *Smart City*

**Autor:** Daniel Fast

## Beschreibung

Beschreibung des Softwareprodukts "Smart City".

## Github Repository

* Link zum Github Repository mit Source Code, Dokumentation, Kanban-Board
  - [Smart City](https://github.com/Smart-City-SoSe-2022)

## Ziele

- Anwendungsbereiche, Motivation, Umfang, Alleinstellungsmerkmale, Marktanforderungen
  - Moderne Webseite für eine Kommune
  - Fortschreitende Digitalisierung in allen Bereichen des Lebens, so auch eine Smart City zur Verknüpfung verschiedener Dienste der Stadt und Beschleunigung und Automatisierung von Prozessen
  - Portal der Stadt, Microservices mit verschiedenen Diensten
  - Single Account für alle Services, Services synchronisieren sich automatisch
  - Sicherheit, Zuverlässigkeit, Performanz
- Informationen zu Zielbenutzergruppen und deren Merkmale (Bildung, Erfahrung, Sachkenntnis)
  - Zielgruppe sind Bewohner der Stadt
  - Hauptsächlich Personen ab 18 Jahren, die den Dienst verschiedener Services benötigen
  - Es sind keinerlei Kenntnisse nötig, um das Portal zu verwenden
- Abgrenzung (Was ist das Softwaresystem _nicht_) TODO
  - Es ersetzt nicht die einzelnen Ämter
  - Bei spezifischen Problemen muss weiterhin persönlich das Problem mit dem jeweiligen Amt gelöst werden

## Risiken

* SWOT-Analyse TODO

**Smart City SWOT-Analyse**

| | Chancen im Markt | Risiken im Markt |
|:---:|---|---|
| **eigene Stärke** | **Chance:** Es werden alltäglich Services der Stadt benötigt <br><br> **Stärke:** Portal verlinkt und synchronisiert verschiedene Services der Stadt, sodass nicht überall einzeln nachgehakt werden muss | **Risiko:** Andere Apps wollen die Verlinkung der Stadt ebenfalls anbieten <br><br> **Stärke:** Praxiserfahrung aus mehreren Projekten |
| **eigene Schwäche** | **Chance:** Viele Dienste wollen in Zukunft digitalisiert werden <br><br> **Schwäche:** Portal beschränkt sich bisher nur auf bereits digitalisierte Dienste | **Risiko:** Kunden wollen gerne wegen der Bequemlichkeit alles digital lösen <br><br> **Schwäche:** Manche Dienste sind nicht genug digitalisiert und können nicht im Portal angeboten werden |


Fazit:
1. Bei der Digitalisierung anderer Dienste mitwirken
2. Schnell neue digitalisierte Dienste in das Portal integrieren

* Verfügen wir über die notwendigen Kompetenzen? (Umsetzbarkeit)
  - Unser Team hat in der Vergangenheit schon mehrmals Webservices aufgebaut. Die Kompetenzen sind vorhanden und das Projekt sollte in größten Teilen umsetzbar sein.
* Welche Risiken und negativen Nebeneffekte sind zu erwarten?
  - Full Stack Development für jedes Teammitglied ist bisher neu
  - Einarbeitung in Front- oder Backend ist zu erwarten
  - Nicht optimaler oder qualitativer Code wegen teilweise neue Technologie wie schon erwähnt, Front- oder Backend
  - Leistungsdruck

## Stakeholder TODO

| Funktion / Relevanz | Name | Kontakt / Verfügbarkeit | Wissen  | Interessen / Ziele  | 
|---|---|---|---|---|
| Product-Owner, Entscheider - als Koordinator der Stakeholderanforderungen | Daniel Fast | daniel.fast@fh-bielefeld.de, GitHub: @mrdanf, 9 - 18 Uhr, Löhne | Produktvision, Stakeholderinput | Qualitatives Produkt erstellen |
| Leiter Stadtverwaltung | Herr Mustermann | Tel.: 057101234, stadtmuster@minden.de, 8 - 16 Uhr, Mitarbeit zu 20 % möglich, Minden | Kennt Prozesse der Stadtverwaltung | Vereinfachung und Automatisierung von Anträgen |
| Administrator, Serverbetreiber | Frau Munter | Tel.: 057187321, munter@mindenservers.de | Erfahrung mit Smarten Diensten, Expertise in Wartungsarbeiten | Stabiler und Sicherer Service mit wenig Ausfallzeiten |
| Leiter der Bibliothek TODO | - | - | - | - |
| Leiter des Verkehrsamts TODO | - | - | - | - |
| - | - | - | - | - |
|**Vorlage:**|---|---|---|---|
| Leiter der Bibliothek, Fachlicher Entscheider  |  Herr Bauer | Tel. 409000, Von 9-19 Uhr telefonisch erreichbar, Mitarbeit zu 30% möglich, Nürnberg  | Kennt das Altsystem aus der Anwendersicht, soll mit dem System arbeiten  | Vereinfachung der Ausleihprozesse  |  
| Administrator, Informationslieferant bzgl. Wartungsanforderungen  | Herr Heiner  | Heiner@gmx.net, Per E-Mail, immer erreichbar, Verfügbarkeit 50%, Nürnberg  | Vertraut mit vergleichbarer Verwaltungssoftware   |  Stabiles System, geringer Wartungsaufwand | 
| Product-Owner, Entscheider - als Koordinator der Stakeholderanforderungen   | Paul Ottmer  |  po@ottmer.de, Per E-Mail und tel. tagsüber, Verfügbarkeit 100%, Nürnberg  | Koordinator für die Inputs der Stakeholder  | ROI des Systems sicherstellen  | 

## Systemübersicht

Dieser Abschnitt zeigt die technische Beschreibung des Softwaresystems
in Form eines Systemarchitekturdiagramms.
Das Diagramm ist statisch und nicht dynamisch und stellt daher keine Abläufe dar. Abläufe werden im Kapitel "Abläufe" dargestellt. Im Kapitel "Systemübersicht" soll genau ein Diagramm dargstellt werden. Das "Box-and-Arrow"-Diagramm soll als Systemarchitekturdiagramm eine abstrakte Übersicht über das Softwaresystem geben. Dazu stellt es die Rechnerknoten und deren Kommunikationsbeziehungen (Protokoll (z.B. HTTP), Datenformat (z.B. JSON)) dar. Also Rechtecke und gerichtete Pfeile. Ähnlich einem UML-Deployment-Diagramm, aber noch abstrakter, denn es zeigt nicht die Verteilung der Softwarebausteine auf die Rechnerknoten. So erlangt der Leser einen schnellen und guten Überblick über das Softwaresystem. 

## Kommunikationsprotokolle und Datenformate

## Funktionale Anforderungen 

- "Globale" Funktionalitäten, die alle Microservices überspannen

## Abläufe

- Abläufe der Kommunikation von Microservices
  in Sequenz- oder Aktivitätsdiagramm darstellen

## Nicht-funktionale Anforderungen 

### Rahmenbedingungen

- Normen, Standards, Protokolle, Hardware, externe Vorgaben

### Betriebsbedingungen

- Vorgaben des Kunden (z.B. Web Browser / Betriebssystem Versionen, Programmiersprache)

### Qualitätsmerkmale

- Externe Qualitätsanforderungen (z.B. Performance, Sicherheit, Zuverlässigkeit, Benutzerfreundlichkeit)

Qualitätsmerkmal | sehr gut | gut | normal | nicht relevant
---|---|---|---|---
**Zuverlässigkeit** | | | | |
Fehlertoleranz |X|-|-|-|
Wiederherstellbarkeit |X|-|-|-|
Ordnungsmäßigkeit |X|-|-|-|
Richtigkeit |X|-|-|-|
Konformität |-|X|-|-|
**Benutzerfreundlichkeit** | | | | |
Installierbarkeit |-|-|X|-|
Verständlichkeit |X|-|-|-|
Erlernbarkeit |-|X|-|-|
Bedienbarkeit |-|X|-|-|
**Performance** | | | | |
Zeitverhalten |-|-|X|-|
Effizienz|-|-|-|X|
**Sicherheit** | | | | |
Analysierbarkeit |X|-|-|-|
Modifizierbarkeit |-|-|-|X|
Stabilität |X|-|-|-|
Prüfbarkeit |X|-|-|-|


## Glossar 

- Definitionen, Abkürzungen, Begriffe

## Referenzen

* Handbücher, Gesetze
* z.B. Datenschutzgrundverordnung




