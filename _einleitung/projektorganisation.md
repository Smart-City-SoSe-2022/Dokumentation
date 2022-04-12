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

- Wie sieht hier ein Codereview aus? TODO
  - Es werden die erledigten Issues vorgestellt
  - Kurz und knapp relevantere und kompliziertere Codeteile, trivialer Code sollte nicht vorgestellt werden

#### Kommunikation

Hauptsächlich kommuniziert das Team über Discord. Per Chat kann man in den verschieden organisierten Kanälen Nachrichten austauschen. Für Meetings, die Online stattfinden, wird der Voice Chat von Discord genutzt. (Verlinkung von GitHub mit Discord / Änderungen auf GitHub werden in Discord übermittelt (Webhook) TODO). Kommentare zu den Issues und Commits werden direkt in GitHub erstellt.

- Wie und womit wird die Teamkommunikation durchgeführt?
  - Hauptsächlich über Discord
    - Per Chat in verschieden organisierten Kanälen
    - Per Voice Chat in Meetings
    - Verlinkung von GitHub mit Discord / Änderungen auf GitHub werden in Discord übermittelt (Webhook) TODO
  - Kommentare zu Issues und Commits in GitHub

#### Dokumentation

- Dokumentation: TODO
  - Entwicklerdokumentation?
    - Swagger TODO
  - Kundendokumentation?
  - Meeting-Protokoll-Dokumentation?
    - Nach jedem Meeting wird ein ausführliches Protokoll angefertigt mit besprochenen Themen und Beschlüssen
- Was ist der Produktlieferzeitplan? (x-Mal-wöchentliche Auslieferungen / Continuous I/D/D) TODO
  - 1 mal wöchentlich am Ende der Woche TODO
- Wie wird der Projektfortschritt gemessen und was passiert, wenn zeitlich verschoben werden muss?
  - Der Projektfortschritt wird mittels des Kanban Boards gemessen
  - Bei zeitlicher Verschiebung muss für den nächsten Sprint neu priorisiert werden
- Wer setzt Erwartungen und Ziele fest und wie werden diese dokumentiert?
  - Jedes Teammitglied stellt seine Idee und Umfang für ein Microservice vor
  - Der Product Owner begutachtet die Idee und den Umfang und achtet zusammen mit DevOps Engineer auf Einhaltung des Ziels und Qualität
- Was passiert, wenn jemand Verbesserungsmöglichkeiten identifiziert?
  - Generell werden Verbesserungsmöglichkeiten immer angehört und bei genug zeitlichem Puffer in einem Issue festgehalten
  - Verbesserung am Code einfach an jeweiliger Stelle im Code bei GitHub kommentieren
  - Können frei im dafür vorgesehenen Discord Text-Channel geäußert werden
- Einschränkungen, Betriebsbedingungen, Faktoren und Risiken, die die Entwicklung beeinflussen können.
  - Unerfahrenheit in der Entwicklung von Microservices
  - Architekturmuster bisher unbekannt
  - Neue Technologien

### Team

- Werte und menschliche Umgangsformen
  - Jedes Teammitglied darf seine Meinung zu verschiedenen Features oder Code frei äußern bzw. sollte es produktive Kritik sein
  - Die Teammitglieder sprechen sich per Du an
  - Alle Teammitglieder sind gleichgestellt, es herrscht eine flache Hierarchie
- Wie werden Meinungsverschiedenheiten gelöst?
  - Wenn keine Mitte unter den Teammitgliedern gefunden werden kann, versucht der Scrum Master eine bestmögliche alternative Lösung für das Problem zu finden
- Wer legt Prioritäten und Zeitpläne fest?
  - Der Product Owner
- Was passiert, wenn ein Teammitglied ein Ziel nicht einhält bzw. die Erwartungen nicht erfüllt?
  - Es wird zusammen mit dem Teammitglied eine Lösung gefunden, sei es Hilfestellung oder Entlastung im nächsten Sprint
  - Notfalls muss neu priorisiert werden

### Technik TODO

- Interne Anforderungen an Softwarequalitätsmerkmale 
  - Erweiterbarkeit
  - Dokumentation
  - automatische und manuelle Tests
    - Code wird auf Kompilierbarkeit geprüft und dann gepushed.
  - Statische Codeanalyse
  - ...

    - ISO25010
- Aufteilung in Repositories gemäß Systemarchitektur? Monorepo?
Repos nach Microservice Architektur
- Versionskontrolle? Git-Workflow?
Jeder hat seinen eigenen Workflow dank eigener Repos. Versionskontrolle mit Git und GitHub.
- Wie werden Änderungen intgriert und ausgeliefert? CI/CD? 
Bei jedem Merge in ein Master Branch wird die neueste Version automatisch mit GitHub Actions deployed.
- Wie wird die Infrastruktur spezifiziert? Containerisierung?
Jeder Microservice wird in einem eigenen Docker Container ausgeführt. Zur Containerverwaltung wird Kubernetes verwendet.
- Implementierung
  - Entwicklungsumgebung.
  - Betriebssysteme.
  - Programmiersprachen.
  - Frameworks.
  - Logging.
    - Globales Error Logging durch RabbitMQ.
- Technologieauswahl: Messaging zum Beispiel mit [RabbitMQ](https://www.rabbitmq.com/) und [AsyncAPI](https://www.asyncapi.com/)

## Rollen und Verantwortlichkeiten

| Person | Rolle | Verantwortlichkeit |
|----------|-----------|-----------|
| Daniel Fast | Scrum Master | Leitung, Kanban-Board, Protokollierung, Prozessqualität |
| Daniel Fast | Product Owner | Produktvision, Integrations-Microservice, Softwareproduktqualität |
| Luca Humke | DevOps Engineer | Github-Repos, Docker, CI/CD, Dokumentation, Support, Infrastrukturqualität | 
| Luca Humke  | Software Architekt | Technische Leitung/Vision, Code Reviews, Mentoring, Technikevaluation, Softwarequalität |
| Marcel Sander | Software Engineer | Microservice [Parkplatz](parkplatz/index) |
| Manuel Wiebe | Software Engineer | Microservice [Krankenhaus](krankenhaus/index) |
| Oskar Schaubert | Software Engineer | Microservice [Krankenhaus](krankenhaus/index) |
| Abdurakhman Vaysert | Software Engineer | Microservice [Krankenhaus](krankenhaus/index) |
| Vadim Balysev | Software Engineer | Microservice [Krankenhaus](krankenhaus/index) |
| Endrina Meta | Software Engineer | Microservice [Krankenhaus](krankenhaus/index) |
| Rene Braun | Software Engineer | Microservice [Krankenhaus](krankenhaus/index) |

Hinweis: Ein Microservice für die Authentifizierung/Autorisierung könnte sinnvoll sein.

## Grober Meilensteinplan

Zusätzlich zum Kanban-Board hier Meilensteine beschreiben.

**Feststehende Termine:**

* **Abgabe Spezifikation:** KW 16 (18.4.-20.4.)
* **Erster Prototyp (MVP):** KW 20 (16.5.-18.5.) / KW 21 (23.5.-25.5.)
* **Softwareprojektabgabe:** Ende Juni 2022 / Anfang Juli 2022
