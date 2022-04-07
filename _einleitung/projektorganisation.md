# Projektorganisation

**Autor:** Daniel Fast

## Richtlinien

### Organisation

- Verwendetes Vorgehensmodell.
  - Scrum
- Welche Arten von Meetings finden wöchentlich statt?
  - Sprint Planning TODO
  - Sprint Review TODO
- Geplanter Ablauf der Meetings.
  - Kurzer Bericht des Fortschritts jedes Mitglieds
  - Problembehandlung
  - Vorausschauende Planung
  - Weitere Anmerkungen
- Werkzeuge für Projektorganisation? Kanban-Board?
  - Zur Organisation des Projekts wird in GitHub das Feature `Projects (beta)` genutzt
  - Mit `Projects` wird ein Kanban-Board aufgebaut, welches in mehrere Spalten aufgeteilt ist
    - Todo
    - In Progress
    - In Review
    - Done
- Wie läuft ein typischer Sprint ab?
  - Dauer von einer Woche
  - Am Anfang Sprint Planning
  - Am Ende Sprint Review
  - Bei Bedarf Meeting zwischendurch TODO
- Wie sieht hier ein Codereview aus? TODO
  - Es werden die erledigten Issues vorgestellt
  - Kurz und knapp relevantere und kompliziertere Codeteile, trivialer Code sollte nicht vorgestellt werden
- Wie und womit wird die Teamkommunikation durchgeführt?
  - Hauptsächlich über Discord
    - Per Chat in verschieden organisierten Kanälen
    - Per Voice Chat in Meetings
    - Verlinkung von GitHub mit Discord / Änderungen auf GitHub werden in Discord übermittelt (Webhook) TODO
  - Kommentare zu Issues und Commits in GitHub
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
  - Statische Codeanalyse
  - ...
- Aufteilung in Repositories gemäß Systemarchitektur? Monorepo?
- Versionskontrolle? Git-Workflow?
- Wie werden Änderungen intgriert und ausgeliefert? CI/CD? 
- Wie wird die Infrastruktur spezifiziert? Containerisierung?
- Implementierung
  - Entwicklungsumgebung.
  - Betriebssysteme.
  - Programmiersprachen.
  - Frameworks.
  - Logging.
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
