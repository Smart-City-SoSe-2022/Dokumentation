# Projektorganisation

**Autor:** Daniel Fast

## Richtlinien

### Organisation

#### Vorgehensmodell

Zur Durchführung des Softwareprojekts wird das Vorgehensmodell Scrum angewendet. Dieses Vorgehensmodell ist optimal für die Anwendung der CI/CD Pipeline, sodass die Webanwendung schrittweise aufgebaut wird und früh ein ausführbares Ergebnis vorliegt. Außerdem lässt sich mit dem Modell das Fachwissen einfach erlernen und gleichzeitig anwenden, da das Softwareprodukt schrittweise aufgebaut wird.

#### Meetings

Jede Woche wird ein Sprint Planning und ein Sprint Review stattfinden. <br>
Beim Sprint Planning wird das Projektziel und die dafür verbleibenden Aufgaben betrachtet, welche alle verschieden priorisiert im Product Backlog vorhanden sind. Die wichtigsten Aufgaben werden dann für den kommenden Sprint in das Sprint Backlog verschoben. Dabei versucht sich das Team aufeinander abzustimmen, sodass alle den gleichen Fortschritt im Sprint erreichen und die implementierten Features getestet werden können. <br>
Beim Sprint Review werden die Ergebnisse vorgestellt. Hier wird auch ein Bild davon gemacht, wie gut die implementierten Features zusammen funktionieren und ob Verbesserungsbedarf besteht. Dieses Meeting ist auch optimal dafür geeignet, weitere Vorschläge für das Product Backlog zu sammeln. Weiterhin kann hier auch gesehen werden, wie das Tempo auf das Team wirkt und ob Anpassungen am Tempo und den Prioritäten nötig sind. <br>
Bei Bedarf kann das Team innerhalb eines Sprints Meetings z.B. zur Problembehandlung vereinbaren. In jedem Meeting können auch weitere Themen wie z.B. Projektorganisation besprochen werden.

#### Werkzeuge für die Projektorganisation

Zur Organisation des Projekts wird in GitHub das Feature `Projects (beta)` genutzt. Darin ist ein Scrum Board aufgebaut, welches in mehrere Spalten aufgeteilt ist. Die Spalten sind bekanntlich:
1. Product Backlog
2. Sprint Backlog
3. In Progress
4. In Review
5. Done

#### Verlauf eines Sprints

Die Sprints haben eine Dauer von einer Woche. Es findet am Anfang ein Meeting für das Sprint Planning und am Ende ein Meeting für das Sprint Review statt. Bei Bedarf können zwischendurch weitere Meetings vereinbart werden. Während des Sprints werden die Aufgaben aus dem Sprint Backlog abgearbeitet.

#### Codereview

Bevor neuer Code in den main Branch gemerged werden kann, muss erst mal ein Pull Request gestellt werden. Der DevOps Engineer überprüft dann den neuen Code. Wenn der Code kompiliert und gut ist, wird er in den main Branch gemerged.

#### Kommunikation

Hauptsächlich kommuniziert das Team über Discord. Per Chat kann man in den verschieden organisierten Kanälen Nachrichten austauschen. Für Meetings, die Online stattfinden, wird der Voice Chat von Discord genutzt. Zusätzlich wird in Discord ein Channel mit Hilfe von Webhooks eingerichtet, damit aktuelle Aktivitäten in den Repositories im Channel sichtbar sind. Kommentare zu den Issues und Commits werden direkt in GitHub erstellt.

#### Dokumentation

Für jedes Repository muss eigene Dokumentation erstellt werden, da jedes Repository ein eigenes Front- und Backend und eine Datenbank enthält. Jedes Teammitglied beschreibt die API seines Backends mit Swagger.io. <br>
Für die Meetings werden auch ausführliche Protokolle angefertigt, die auch die Beschlüsse festhalten.

#### Produktlieferzeitplan

Das Produkt wird immer ausgeliefert (deployed), sobald eine neue Version im main Branch verfügbar ist. Somit kann es zu mehreren Produktauslieferungen pro Woche kommen.

#### Organisation des Projektfortschritts

Um den Fortschritt des Projekts im Auge zu behalten und auf Änderungen oder Rückschläge besser reagieren zu können, wird der Projektfortschritt mittels eines Scrum Boards gemessen. Falls Aufgaben nicht rechtzeitig erledigt werden konnten und das Projekt somit teilweise in Verzug gerät, müssen die Aufgaben für den nächsten Sprint neu priorisiert werden. <br>
Die Priorisierung der Aufgaben übernimmt der Product Owner. Auch die Erwartungen und Ziele legt der Product Owner fest, wobei jedes Teammitglied auch seine eigenen Wünsche und Bemerkungen mit dazu beitragen kann. Der Product Owner und der DevOps Engineer achten zusammen auf die Einhaltung des Ziels und der Softwarequalität. <br>
Wenn jemandem Verbesserungsmöglichkeiten einfallen sollte, sollten diese einfach über Discord oder im Meeting geäußert werden. Wenn genug zeitlicher Puffer vorhanden ist, können diese Vorschläge umgesetzt werden. Bei Verbesserungen am Code sollten diese direkt in GitHub vorgeschlagen werden. <br>
Generell ist auch davon auszugehen, dass nicht alles perfekt nach Plan läuft, da das Team bisher noch keine Erfahrung in der Entwicklung einer Webanwendung mit Hilfe von Microservices hat. Neue Technologien und das bisher unbekannte Architekturmuster birgen Risiken, die die Entwicklung beeinflussen können. Neue Priorisierung und Verbesserungsvorschläge sind durchaus erwartet.

### Team

Üblich dem Scrum Modell nach, herrscht im Team eine flache Hierarchie. Alle Teammitglieder sind gleichgestellt. Jedes Teammitglied darf seine Meinung zu verschiedenen Features oder geschriebenen Code frei äußern. Zu beachten ist nur, dass es produktive Kritik sein sollte und niemanden angreifen sollte. <br>
Bei Meinungsverschiedenheiten versuchen die Teammitglieder erst selbst sich abzusprechen. Falls keine Lösung gefunden wird, versucht der Scrum Master eine bestmögliche Entscheidung zur Lösung des Problems zu treffen. <br>
Die Zeitpläne und Prioritäten werden vom Product Owner festgelegt. Falls ein Teammitglied sein Ziel voraussichtlich nicht einhalten kann bzw. nicht im zufriedenstellenden Maße, sollte das Teammitglied früh genug von seinem Problem oder Verzug berichten. Somit kann frühstmöglich Hilfestellung geleistet werden. Sollte am Ende des Sprints immer noch das Ziel nicht erreicht werden, muss die Planung für den nächsten Sprint angepasst werden und eventuell auch neu priorisiert werden.

### Technik

#### Interne Anforderungen an Softwarequalitätsmerkmale

Das Team bemüht sich, die Software nach dem ISO25010 Standard umzusetzen. Das bedeutet, das Team versucht die Softwarequalität hoch zu halten, in dem es leserlichen und erweiterbaren Code schreibt. Das ist notwendig, da die Microservices wöchentlich ein Inkrement erreichen und Features über die Zeit hinzugefügt werden. Zusätzlich sollte der Code mit Kommentaren und Dokumentation wie z.B. JavaDoc versehen werden. Bei selbsterklärenden Methoden und Code kann davon abgesehen werden. <br>
Es wird auf dem develop Branch des Repositorys gearbeitet. Commits werden dann mit einem Pull Request auf den main Branch gepusht. Automatische Tests prüfen den Code auf Kompilierbarkeit, bevor der Code in den main Branch gemerged wird. Bei jedem Merge in ein main Branch wird die neueste Version automatisch mit GitHub Actions deployed. <br>

#### Aufteilung der Repositories

Jeder Microservice erhält sein eigenes Repository, welches je von einem Teammitglied bearbeitet wird. Dadurch kann die Microservice Architektur optimal umgesetzt werden. Zusätzlich wird jedes Microservice in einem eigenen Docker Container ausgeführt. Zur Containerverwaltung wird Kubernetes verwendet. <br>

#### Versionskontrolle

Zur Versionskontrolle wird Git genutzt. Das gesamte Projekt und die Repositories werden in GitHub verwaltet. Einen festen Workflow gibt es, dank eigener Repositories, nicht. Jedes Teammitglied kann seinen eigenen Workflow in seinem Repository einbringen. <br>

#### Entwicklungsumgebung und Betriebssysteme

Für die genutzten Technologien in der Implementierung hat jedes Teammitglied die freie Wahl. Es wird als Entwicklungsumgebung größtenteils IntelliJ IDEA genutzt, dazu kommt auch IntelliJ Datagrip und Rider und auch Visual Studio Code. Die Entwicklung findet auf Windows 10 oder 11 statt, der Code wird jedoch auf Linux Servern laufen.

#### Programmiersprachen

Es werden mehrere Programmiersprachen für die Entwicklung verwendet. Jedes Teammitglied kann für sein Repository die verwendete Sprache bestimmen. Es kommen folgende Programmiersprachen zum Einsatz:
- HTML
- CSS
- JavaScript
- Java
- Python
- C#

#### Datenbank
Es wird in jedem Repository MySQL als Datenbank verwendet.

#### Frameworks

Wie auch bei den Programmiersprachen, kommen für jedes Repository eigene Frameworks zum Einsatz. Diese sind folgende: <br>
Frontend:
- React
- Svelte
- Vue

Backend:
- SpringBoot
- Express
- Django

#### Kommunikationstechnologie zwischen Microservices

Die Kommunikation zwischen den Microservices wird mit [RabbitMQ](https://www.rabbitmq.com/) durchgeführt. Durch RabbitMQ synchronisieren die Server ihre Daten und bleiben immer konsistent.

#### Logging

Für das Logging wird RabbitMQ genutzt. Damit wird ein globales Errorlogging durchgeführt.

## Rollen und Verantwortlichkeiten

| Person | Rolle | Verantwortlichkeit |
|----------|-----------|-----------|
| Daniel Fast | Scrum Master | Leitung, Scrum-Board, Protokollierung, Prozessqualität |
| Daniel Fast | Product Owner | Produktvision, Integrations-Microservice, Softwareproduktqualität |
| Luca Humke | DevOps Engineer | Github-Repos, Docker, CI/CD, Dokumentation, Support, Infrastrukturqualität | 
| Luca Humke  | Software Architekt | Technische Leitung/Vision, Code Reviews, Mentoring, Technikevaluation, Softwarequalität |
| Daniel Fast | Software Engineer | Microservice Portal / Authentifizierung |
| Marcel Sander | Software Engineer | Microservice [Banksystem](banksystem/index) |
| Manuel Wiebe | Software Engineer | Microservice [Stadtwerke](stadtwerke/index) |
| Oskar Schaubert | Software Engineer | Microservice [Bibliothek](bibliothek/index) |
| Abdurakhman Vaysert | Software Engineer | Microservice [Fahrzeugvermietung](fahrzeugvermietung/index) |
| Vadim Balysev | Software Engineer | Microservice [Stadtverwaltung](stadtverwaltung/index) |
| Rene Braun | Software Engineer | Microservice [Local-Finder](local-finder/index) |

## Grober Meilensteinplan

**Feststehende Termine:**

* **Abgabe Spezifikation:** KW 16 18.04.2022
* **Erster Prototyp (MVP):** KW 20 (16.5.-18.5.) / KW 21 (23.5.-25.5.)
* **Softwareprojektabgabe:** Ende Juni 2022 / Anfang Juli 2022
