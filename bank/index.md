# Bank

**Autor:** Marcel Sander


## Überblick

- Die Bank der Stadt … ist für jegliche Geldanlagen zuständig. Hier wird das Geld zwischen Kunden und der Bank oder auch zwischen Kunden und Kunden bewegt.Kunden können hier Auch einen Kredit aufnehmen der nach Ihrer Persöhnlichen Bewertung unterschiedlich Groß ausfallen kann.Kunden können auch online für das Objekt ihrer begierde bezahlen. 
- Konzeptionelles Analyseklassendiagramm (logische Darstellung der Konzepte der Anwendungsdomäne)


## Funktionale Anforderungen

* Welche Akteure Haben wir ?
* -Der Kunde ist ein Nutzer der Seite, welcher auf der Seite sein Wertanlagen verwalten möchte.
* -Der Mitarbeiter wiederum Unterstützt den Kunden und genehmigt Kredite. 


![Use case bild](https://user-images.githubusercontent.com/85035651/163670969-405655d4-05e7-4e99-9aa7-9215399a9f5a.png)



## Anforderungen im Detail

| **Als** | **möchte ich** | **so dass** | **Akzeptanz** |
| :------ | :----- | :------ | :-------- |
| Wer | Was | Warum | Wann akzeptiert |
| Kunde | Möchte ich mich anmelden können | meine Daten geschützt sind  | Anmeldung des Kunden  |
| Kunde | Meinen Konto stand sehen | ich weiß wieviel Geld ich besitze  | Kunde sieht seinen Kontostand |
| Kunde | Geld überweisen | ich objekte online Bezahlen kann  | Geld wird überwiesen  |
| Kunde | einen Kredit aufnehemen | ich mehr Geld auf meinem Konte besitze | Kreditanfrage wird erstellt |
| Mitarbeiter | Kreditanfragen sehen | ich diese annehmen oder ablehnen kann   | Kreditanfrage wird genehmigt oder abgelehnt  |
| Mitarbeiter | Kundendaten einsehen können | ich geld auszahlen zu kann  | Mitarbeiter sieht Kunden Daten |


| **Als** | **möchte ich** | **so dass** | **Akzeptanz** |
| :------ | :----- | :------ | :-------- |
| Wer | Was | Warum | Wann akzeptiert |
| Kunde | Möchte ich mich anmelden können | meine Daten geschützt sind  | Anmeldung des Kunden  |
| Kunde | Meinen Konto stand sehen | ich weiß wieviel Geld ich besitze  | Kunde sieht seinen Kontostand |
| Kunde | Geld überweisen | ich objekte online Bezahlen kann  | Geld wird überwiesen  |
| Kunde | einen Kredit aufnehemen | ich mehr Geld auf meinem Konte besitze | Kreditanfrage wird erstellt |


| **Als** | **möchte ich** | **so dass** | **Akzeptanz** |
| :------ | :----- | :------ | :-------- |
| Wer | Was | Warum | Wann akzeptiert |
| Mitarbeiter | Kreditanfragen sehen | ich diese annehmen oder ablehnen kann   | Kreditanfrage wird genehmigt oder abgelehnt  |
| Mitarbeiter | Kundendaten einsehen können | ich geld auszahlen zu kann  | Mitarbeiter sieht Kunden Daten |


## Graphische Benutzerschnittstelle

![Unbenannt](https://user-images.githubusercontent.com/85035651/165083950-2240ed4d-651c-4cdb-9f6d-c683982b9115.png)


## Datenmodell 

- Begriffe im Glossar darstellen
- Modellierung des physikalischen Datenmodells 


![ER MODELL](https://user-images.githubusercontent.com/85035651/163670979-a801632b-f69b-43be-8d7c-15812aa51151.png)


## Abläufe

- Aktivitätsdiagramm für den Ablauf sämtlicher Use Cases
- Aktivitätsdiagramme für relevante Use Cases
- Aktivitätsdiagramm mit Swimlanes sind in der Regel hilfreich 
  für die Darstellung der Interaktion von Akteuren der Use Cases / User Stories
- Abläufe der Kommunikation von Rechnerknoten (z.B. Client/Server)
  in einem Sequenz- oder Aktivitätsdiagramm darstellen
- Modellieren Sie des weiteren die Diagramme, die für das (eigene) Verständnis des
  Softwaresystems hilfreich sind. 


## Schnittstellen

- Schnittstellenbeschreibung (API), z.B. mit OpenAPI 
- Auflistung der nach außen sichtbaren Schnittstelle des Microservices. Über welche Schnittstelle kann z.B. der Client den Server erreichen?
- In Event-gesteuerten Systemen ebenfalls die Definition der Ereignisse und deren Attribute
- Aufteilen in Commands, Events, Queries
* Abhängigkeiten: Liste mit Kommunikationsabhängigkeiten zu anderen Microservices

**Beispiel:**

### URL

http://smart.city/microservices/bank/{KundenID}

### Commands


**Asynchronous**

| **Name** | **Parameter** | **Resultat** |
| :------ | :----- | :------ |
| getCustomer() | int id | int id |
| getCustomerbankbalance() | int id | int id |


## Technische Umsetzung


### Softwarearchitektur

- Darstellung von Softwarebausteinen (Module, Schichten, Komponenten)

Hier stellen Sie die Verteilung der Softwarebausteine auf die Rechnerknoten dar. Das ist die Softwarearchitektur. Zum Beispiel Javascript-Software auf dem Client und Java-Software auf dem Server. In der Regel wird die Software dabei sowohl auf dem Client als auch auf dem Server in Schichten dargestellt.

* Server
  * Web-Schicht
  * Logik-Schicht
  * Persistenz-Schicht

* Client
  * View-Schicht
  * Logik-Schicht
  * Kommunikation-Schicht

Die Abhängigkeit ist bei diesen Schichten immer unidirektional von "oben" nach "unten". Die Softwarearchitektur aus Kapitel "Softwarearchitektur" ist demnach detaillierter als die Systemübersicht aus dem Kapitel "Systemübersicht". Die Schichten können entweder als Ganzes als ein Softwarebaustein angesehen werden. In der Regel werden die Schichten aber noch weiter detailliert und in Softwarebausteine aufgeteilt. 



### Entwurf

- Detaillierte UML-Diagramme für relevante Softwarebausteine

### Fehlerbehandlung 

* Mögliche Fehler / Exceptions auflisten
* Fehlercodes / IDs sind hilfreich
* Nicht nur Fehler technischer Art ("Datenbankserver nicht erreichbar") definieren, sondern auch fachliche Fehler wie "Kunde nicht gefunden", "Nachricht wurde bereits gelöscht" o.ä. sind relevant. 

### Validierung

* Relevante (Integrations)-Testfälle, die aus den Use Cases abgeleitet werden können
* Testfälle für 
  - Datenmodell
  - API
  - User Interface
* Fokussieren Sie mehr auf Integrationstestfälle als auf Unittests
* Es bietet sich an, die IDs der Use Cases / User Stories mit den Testfällen zu verbinden,
  so dass erkennbar ist, ob Sie alle Use Cases getestet haben.

### Verwendete Technologien

- Verwendete Technologien (Programmiersprachen, Frameworks, etc.)

* Frontend
  -React
  -Javascript
  -CSS
* Backend
  -Visual Studio
* Datenbank
  -Datagrip
  -MySQL
