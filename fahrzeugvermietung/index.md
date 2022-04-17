# Smart Rent

**Autor:** Abdurakhman Vaysert


## Überblick

- Smart Rent ist für das Vermieten von elektro Fahrezeugen zuständig. Unter elektro Fahrzeuge fallen elektro Fahrräder, elektro Roller und elektro Autos.
Die Fahrzeuge sind alle schnell einsehbar und mit wenigen klicks gemietet.


## Funktionale Anforderungen

* Akteure:
  - Mieter: Der Mieter kann sich alle Fahrzeuge anschauen und auswählen, welches Fahrzeug er mieten möchte.
  - Vermieter: Der Vermieter ist dafür zuständig die Fahrzeuge auf der Homepage auszustellen.
* Use-Case Diagramme:<br>
  ![Vermietung Use-Case Diagramm](media/Vermietung.png)
  ![Ausstellung Use-Case Diagramm](media/Ausstellung.png)
  ![Vermietete Fahrzeuge Use-Case Diagramm](media/Vermietete.png)
* Strukturierung der Diagramme in funktionale Gruppen
* Akteure sowie andere Begriffe der implementierten Fachdomäne definieren
* Begriffe konsistent in der Spezifikation verwenden  
* Begriffe im Glossar darstellen

## Anforderungen im Detail

### Mieter User-Stories:

| **Name**| **In meiner Rolle als**...|   ...**möchte ich**...   | ..., **so dass**... | **Erfüllt, wenn**... | **Priorität**   |
|:-----|:----------:|:-------------------|:-------------|:---------|:----------------|
| Fahrzeug betrachten |Mieter|betrachten welche Fahrzeuge zur Verfügung stehen|ich weiß welche Auswahl ich habe | Fahrzeuge betrachtbar sind | Muss |
| Fahrzeug mieten |Mieter| ein Fahrzeug mieten|ich das Fahrzeug benutzen kann| die Bezahlung erfolgreich absgeschlossen wurde | Muss |
| aktuell gemieteten Fahrzeuge betrachten |Mieter| die von mir aktuell gemieteten Fahrzeuge betrachten| ich diese im Vorfeld zurückgeben oder die Mietdauer verlängern kann| das Fahrzeug bei rückgabe wieder zur Verfügung steht oder bei Mietverlängerung bezahlt wird| Muss|

### Vermieter User-Stories:

| **Name**| **In meiner Rolle als**...|   ...**möchte ich**...   | ..., **so dass**... | **Erfüllt, wenn**... | **Priorität**   |
|:-----|:----------:|:-------------------|:-------------|:---------|:----------------|
| Fahrzeug ausstellen |Vermieter| ein Fahrzeug als Mietobjekt zur Ausstellung stellen| für das Fahrzeug gewirbt wird | Das Fahrzeug zur Verfügung steht und das Fahrzeug angezeigt wird | Muss |
| vermietete Fahrzeuge betrachten |Vermieter| eine Übersicht von den vermieteten Fahrzeugen haben | ich weiß, welche Fahrzeuge vermietet sind und wer diese gemietet hat| alle vermieteten Fahrzeuge und deren Mieter angezeigt werden| Muss |

## Graphische Benutzerschnittstelle

### Auswahlmöglichkeiten der Fahrzeuge für den Mieter:
 ![Fahrzeug auswählen GUI-Mockup](media/MieterFahrzeugauswahl.png)
 [Fahrzeuge betrachten](#mieter-user-stories)
### Betrachten eines Fahrzeugs vom Sicht des Mieters:
 ![Fahrzeug betrachten GUI-Mockup](media/FahrzeugBetrachten.png)
 [Fahrzeuge betrachten](#mieter-user-stories) <br>
 [Fahrzeug mieten](#mieter-user-stories)
### Betrachten der gemieteten Fahrzeuge:
 ![gemieteten Fahrzeuge betrachten GUI-Mockup](media/gemFahrzeuge.png)
 [aktuell gemieteten Fahrzeuge betrachten](#mieter-user-stories)
### Fahrzeugauswahl betrachten vom Sicht des Vermieters:
 ![Fahrzeugauswahl bearbeiten GUI-Mockup](media/VermieterFahrzeugauswahl.png)
 [Fahrzeug ausstellen](#vermieter-user-stories)
### Fahrzeug bearbeiten oder neues Hinzufügen vom Sicht des Vermieters:
 ![Fahrzeug bearbeiten GUI-Mockup](media/FahrzeugBearbeiten.png)
 [Fahrzeug ausstellen](#vermieter-user-stories)
### Betrachten der vermieteten Fahrzeuge:
 ![vermietete Fahrzeuge betrachten GUI-Mockup](media/verFahrzeuge.png)
 [vermietete Fahrzeuge betrachten](#vermieter-user-stories)

### Zustandsdiagramm:
 ![](media/Zustandsdiagramm.png)


## Datenmodell 

### physikalisches Datenmodell
 ![](media/physDatenmodell.png)
### ER Datenmodell
 ![](media/ERDatenmodell.png)

## Abläufe

### Aktivitätsdiagramm für den Ablauf sämtlicher Use Cases
 ![Aktivitätsdiagramm der Use Cases](media/UseCaseAktiv.png)
### Aktivitätsdiagramm für das Mieten eines Fahrzeugs
 ![Aktivitätsdiagramm Fahrzeug mieten](media/AktivMieten.png)

### Ablauf der Kommunikation vom Mieten eines Fahrzeugs als Aktivitätsdiagramm
 ![Aktivitätsdiagramm Fahrzeug mieten Kommunikation](media/AktivMietenKom.png)


## Schnittstellen

### URL

http://smart.city/microservices/autoverleih
http://smart.city/microservices/autoverleih/allrent
http://smart.city/microservices/autoverleih/myrent
http://smart.city/microservices/autoverleih/vehicle/id

### Commands

**Synchronous**

|| **Name** | **Parameter** | **Resultat** |
|:-| :------ | :----- | :------ |
| POST | createCustomer() | int mieterID , String lastname, String firstname, String address, int tel, int birthdate | int result |
|DELETE| deleteOrder() | int mieterID, fahrzeugID | int result |
|POST| createVehicles()| int fahrzeugID, int vermieterID, String type, String vehicleModell, String vehicleColor, int vehicleDistance, int vehicleMaxSpeed, int vehicleMileage, int priceDay, int priceWeek, int priceMonth| int result|
|POST| sendPaymentData()| int mieterID, int priceToPay, int smartRentID| int result|


**Asynchronous**

|| **Name** | **Parameter** | **Resultat** |
|:-| :------ | :----- | :------ |
|POST| createRentContract() | int mieterID, fahrzeugID | int result |
|PUT| changeRentContract() | int mieterID, fahrzeugID | int result |
|PUT| changeVehicleRentable() | int fahrzeugID, int mieterID| int result|
|GET| getBillPaid()| int mieterID, int smartRentID| int result|

### Queries

|| **Name** | **Parameter** | **Resultat** |
|:-| :------ | :----- | :------ |
|GET| getContractsMyRentVehicles() | int mieterID | Contract [] listMyRentVehicles |
|GET| getContractsAllRentVehicles() | - | Contract [] listAllRentVehicles |
|GET| getContractsAllAvailableVehicles() | - | Contract [] listAllAvailableVehicles |

### Dependencies

#### RPC

| **Service** | **Funktion** |
| :------ | :----- | 
| Authorization Service | authenticateUser(), sendPaymentData(), getBillPaid() |


## Technische Umsetzung

### Fehlerbehandlung 

- VermieterID wird bei der Bank von Marcel nicht erkannt / es existieren keine Daten unter dieser ID
  - Die übergebene Daten von Smart City unverändert speichern, damit solche Fehler nicht passieren
- Die Kommunikation zwischen Microservices (z.B. das Übersenden vom Mieter zur Bankseite zum Bezahlen der Rechnung) funktioniert nicht 
  - richtig absprechen wie die Kommunikation funktionieren soll und gegenseitig helfen
- Datenbankserver ist nicht erreichbar, somit ist die komplette Webseite nutzlos
- Übergebene Daten sind vom falschen Typ (z.B. gewollt float, aber man bekommt einen int wert)
  - auch hier richtig absprechen, wie die Kommunikation ablaufen soll


### Verwendete Technologien

* Vue.js
* SpringBoot
* postgreSql
