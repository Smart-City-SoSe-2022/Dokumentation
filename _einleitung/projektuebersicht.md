# Projektübersicht *Smart City*

**Autor:** Daniel Fast

## Beschreibung

Smart City ist ein Portal, das mehrere Smarte Services der Stadt verknüpft, sodass Nutzer einen intelligenten und intuitiven Nutzen aus dem Portal der Stadt ziehen können. Es verknüpft z.B. das Portal mit dem Banksystem und dem Fahrzeugverleih. Es wird nur ein Account benötigt, damit loggt man sich im Portal ein. Das Portal liefert die Nutzerdaten dann an die jeweiligen Services weiter. Wenn ein Nutzer ein Auto mieten möchte, wird der zu zahlende Betrag direkt an das Banksystem vermittelt, ohne das weitere Eingaben nötig sind.

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

Smart City soll der Zeit entsprechend eine moderne Webseite für eine Kommune sein, so wie es von vielen anderen Internetdienstanbietern bekannt ist. Die fortschreitende Digitalisierung in allen Bereichen des Lebens führt dazu, dass auch eine Digitalisierung der Services einer Kommune und deren Vernetzung möglich sind. Ein starker Fokus liegt dabei auf der Beschleunigung und Automatisierung von Prozessen innerhalb einer Kommune, die bekanntlich wegen überforderten Bearbeitern oft im Verzug sind. Aber auch die verschiedenen Dienste und Aktivitäten, die in einer Stadt angeboten werden, können sinnvoll verknüpft werden, um ein besseres und einfacheres Erlebnis zu bieten. <br>
Smart City umfasst das Portal, in dem sich die Nutzer anmelden und registrieren können, und die jeweiligen Microservices, die verschiedene Mehrwerte bieten. Ein besonderes Alleinstellungsmerkmal ist der Single Account für alle Services. Man benötigt nicht mehr einen Account für jeden einzelnen Service. Weiterhin synchronisieren die Services untereinander ihre Daten. <br>
Da es sich um sensible Daten handelt und viele Nutzer gleichzeitig das Portal nutzen, wird es für Sicherheit, Zuverlässigkeit und Performanz optimiert.

- Informationen zu Zielbenutzergruppen und deren Merkmale (Bildung, Erfahrung, Sachkenntnis)
  - Zielgruppe sind Bewohner der Stadt
  - Hauptsächlich Personen ab 18 Jahren, die den Dienst verschiedener Services benötigen
  - Es sind keinerlei Kenntnisse nötig, um das Portal zu verwenden

Die Zielgruppe sind die Bewohner der Stadt. Diese sind hauptsächlich Personen ab 18 Jahren, die den Dienst verschiedener Services benötigen. Damit das Portal einfach nutzbar ist, ist es so gestaltet, dass keine Vorkenntnisse nötig sind.

- Abgrenzung (Was ist das Softwaresystem _nicht_) TODO
  - Es ersetzt nicht die einzelnen Ämter
  - Bei spezifischen Problemen muss weiterhin persönlich das Problem mit dem jeweiligen Amt gelöst werden

Das Portal ersetzt jedoch nicht die einzelnen Ämter. Es wird weiterhin spezielle Probleme geben, die nicht über ein Portal lösbar sind und die persönliche Hilfe eines Bearbeiters in einem Amt bedarf.

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

Das Team hinter Smart City hat schon mehrmals Webservices aufgebaut. Die Kompetenzen sind vorhanden und ausgebaut, sodass das Projekt in größten Teilen umsetzbar sein sollte.

* Welche Risiken und negativen Nebeneffekte sind zu erwarten?
  - Full Stack Development für jedes Teammitglied ist bisher neu
  - Einarbeitung in Front- oder Backend ist zu erwarten
  - Nicht optimaler oder qualitativer Code wegen teilweise neue Technologie wie schon erwähnt, Front- oder Backend
  - Leistungsdruck

Jedoch gibt es auch eine Risiken und Nebeneffekte, die zu erwarten sind. Dazu gehört, dass das Full Stack Development bisher noch nicht von jedem Teammitglied praktiziert wurde, da meistens die Arbeit in Frontend und Backend aufgeteilt wurde. Somit ist eine Einarbeitungszeit in Front- oder Backend erwartet. Das bedeutet gleichzeitig auch, dass das Risiko für den Sourcecode besteht, nicht qualitativ zu werden, da gleichzeitig zur Umsetzung des Front- oder Backend der Umgang mit dieser Technologie auch noch erlernt werden muss. Das alles führt dann wegen der Deadline des Projektes noch zu zusätzlichem Druck.

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

Zur Kommunikation werden die Protokolle TCP/IP und RabbitMQ verwendet. TCP/IP kommt zum Einsatz, wenn die Clients sich mit dem Server verbinden und so Daten austauschen. RabbitMQ wird intern im Server zur Anwendung kommen, wenn die Microservices miteinander kommunizieren. <br>
Die Datenformate der Kommunikation sind zwischen Client und Server JSON. Innerhalb des Servers werden Daten durch Plain Text mit RabbitMQ ausgetauscht. TODO

## Funktionale Anforderungen TODO

- "Globale" Funktionalitäten, die alle Microservices überspannen

## Abläufe

- Abläufe der Kommunikation von Microservices
  in Sequenz- oder Aktivitätsdiagramm darstellen

## Nicht-funktionale Anforderungen TODO

### Rahmenbedingungen

- Normen, Standards, Protokolle, Hardware, externe Vorgaben

#### Normen

Damit das Portal konkurrenzfähig und qualitativ ist, setzen wir die Webanwendung nach dem ISO 25010[^1] Standard durch.

#### Standards und Protokolle

Die Webanwendung wird den Standards der W3C nach entwickelt, um den Nutzern eine einfache Bedienung zu ermöglichen. Die angewendeten Protokolle sind TCP/IP und HTTPS (jedoch kann im Rahmen der Vorlesung kein Zertifikat für HTTPS ausgestellt werden).

#### Hardware

Da die Webanwendung sensible Daten verarbeitet und mit vielen gleichzeitigen Nutzer zu rechnen ist, wird ein Server mit mäßig hohen Anforderungen und sehr guter Stabilität und Sicherheit benötigt. Aufgrund der Stabilität und Sicherheit, wird Linux das Betriebssystem des Servers sein. Die weiteren Anforderungen sind die Rechenleistung und Speicherkapazität. <br>
Es wird eine mittelmäßige Rechenleistung für die gleichzeitigen Nutzer benötigt. Die auszuführende Logik ist größtenteils sehr simpel. Die Speicherkapazität sollte etwas erhöht sein, da es viele verschiedene Microservices gibt, die jeweils ihre eigenen Daten und die Daten der Nutzer einspeichern müssen.

#### Externe Vorgaben TODO



### Betriebsbedingungen

- Vorgaben des Kunden (z.B. Web Browser / Betriebssystem Versionen, Programmiersprache)

Das Portal muss auf allen aktuellen Browsern aufrufbar sein. Es ist für die Anwendung auf Rechnern optimiert. Die Anwendung kann auch mit Smartphones genutzt werden, obwohl es nicht für Smartphones optimiert ist. Zur Nutzung eines aktuellen Browsers sollte mindestens Windows 7 installiert sein. Auf dem Smartphone sollte mindestens Android 8 installiert sein. Programmiersprache TODO

### Qualitätsmerkmale

- Externe Qualitätsanforderungen (z.B. Performance, Sicherheit, Zuverlässigkeit, Benutzerfreundlichkeit)

Qualitätsmerkmal | sehr gut | gut | normal | nicht relevant
---|---|---|---|---
**Zuverlässigkeit** | | | | |
Fehlertoleranz |-|X|-|-|
Wiederherstellbarkeit |X|-|-|-|
Ordnungsmäßigkeit |X|-|-|-|
Richtigkeit |X|-|-|-|
Konformität |-|X|-|-|
**Benutzerfreundlichkeit** | | | | |
Installierbarkeit |-|-|-|X|
Verständlichkeit |X|-|-|-|
Erlernbarkeit |-|X|-|-|
Bedienbarkeit |X|-|-|-|
**Performance** | | | | |
Zeitverhalten |-|X|-|-|
Effizienz|-|X|-|-|
**Sicherheit** | | | | |
Analysierbarkeit |-|X|-|-|
Modifizierbarkeit |X|-|-|-|
Stabilität |X|-|-|-|
Prüfbarkeit |X|-|-|-|


## Glossar 

- Definitionen, Abkürzungen, Begriffe

## Referenzen

* Handbücher, Gesetze
* z.B. Datenschutzgrundverordnung

[^1]: ISO 2510: https://iso25000.com/index.php/en/iso-25000-standards/iso-25010




