# Proposal
<b>Probleemstelling</b>

We leven in een tijdperk waarin technologie alomtegenwoordig is: er is geen ontkomen aan. De smartphone is één van deze technologieën. Wereldwijd dragen ruim twee miljard mensen dagelijks een apparaat bij zich dat in staat is om enorme hoeveelheden data over de gebruiker te verzamelen. Met name data betreffende de locatie van de gebruiker is erg waardevol voor meerdere partijen. Eén van deze partijen ligt erg dicht bij de gebruiker; de naaste contacten van de gebruiker (familie en vrienden). 

Een applicatie die het mogelijk maakt om de locatie van de gebruiker te delen met bepaalde contacten biedt voor meerdere partijen een oplossing. Allereerst is het voor ouders met (jonge) kinderen, die tegenwoordig ook vaak over een smartphone met GPS-functionaliteit beschikken, van grote waarde om op elk moment te kunnen zien waar hun kind zich bevindt. Ouders kunnen dan controleren of een kind, op momenten dat het niet onder toezicht is, veilig is.

Een dergelijke applicatie kan ook handig zijn voor vriendengroepen. Op het moment dat vrienden een afspraak maken en elkaar bij aanvang van de afspraak niet kunnen vinden, weten beide partijen van elkaar waar ze zich bevinden, zonder dat ze op een andere manier contact hoeven te leggen (telefonisch, via berichten-apps, etc.). Bovendien kunnen instructies voor het vinden van de juiste locatie met deze informatie veel accurater zijn, wat tijd en frustratie bespaart. 
 
<b>Functies & onderdelen</b>

De applicatie zal worden gebouwd rondom een kaart waarop de locaties van de contacten van de gebruiker staan weergegeven, met daaronder een lijst met de exacte afstand tot elk contact en het tijdstip waarop de locatie voor het laatst bijgewerkt is. De contacten worden georganiseerd in groepen, waaraan mensen toegevoegd kunnen worden. Het delen van de locatie wordt, wanneer dit ingeschakeld is, standaard elke minuut automatisch bijgewerkt. De applicatie zal de gebruiker dan ook de mogelijkheid bieden om het delen van de locatie in of uit te schakelen. Met een knop op een duidelijke locatie kan deze locatie tevens handmatig ververst worden. 

Voordat een gebruiker de applicatie kan benutten, is het nodig dat er een account aangemaakt wordt. De applicatie zal daarom, wanneer deze voor de eerste keer wordt gestart, aan de gebruiker vragen om een account aan te maken. Wanneer iemand reeds een account aangemaakt heeft, kan op hetzelfde scherm gekozen worden om in te loggen. Na het registreren kan de gebruiker ervoor kiezen om ofwel een nieuwe groep aan te maken, of niets te doen. Als voor de laatste optie gekozen wordt ziet de gebruiker na het aanmaken van zijn account alleen zichzelf op de kaart staan. 

De applicatie zal een pagina bevatten waarop voorkeuren aangegeven kunnen worden. Hieronder vallen in ieder geval het in- of uitschakelen van het delen van de locatie, maar ook het interval waarmee de locatie standaard gedeeld wordt. Wanneer er gekozen wordt voor het uitschakelen van de eigen locatie, wordt het delen van de locatie in alle groepen waarin de gebruiker zit gestaakt. De gebruiker kan dan ook niet de locatie zien van anderen, wat middels een melding op de pagina met de kaart zal worden weergegeven. Daarnaast kan een gebruiker in de voorkeuren uitloggen, waarna het inlogscherm getoond zal worden. 

De groepen kunnen worden bereikt via de <i>navigation drawer</i> aan de zijkant van het scherm. Hierin kan de gebruiker zichzelf uit groepen verwijderen en nieuwe groepen aanmaken. Daarnaast kan per groep, middels een aan/uit-schakelaar, de status van het locatie-delen van de gebruiker in de betreffende groep geregeld worden. Bij het maken van een nieuwe groep komt de gebruiker per toe te voegen contact in een nieuwe activity, waarin connectieverzoeken kunnen worden verzonden naar andere gebruikers. 

Tenslotte zal de applicatie een functie bevatten waarmee men foto's met elkaar kan delen, als gebruikers dichtbij elkaar zijn. Deze functie zal worden ondergebracht op het scherm met de kaartweergave, in de vorm van een inbox. In deze nieuwe activity komen foto's binnen van verschillende contacten.
	
<b>Data</b>

De GPS-coördinaten zijn voor de app het belangrijkste onderdeel. Deze coördinaten worden voor elke gebruiker in een Firebase-database gezet. Deze data wordt vervolgens gebruikt om de nieuwe locaties van de contacten van de gebruiker - en de locatie van de gebruiker zelf - weer te geven.
 
<b>Externe componenten</b>

Zoals reeds genoemd, zal de applicatie gebruik maken van Firebase voor het opslaan van gebruikersgegevens (gebruikersnaam, locatie, etc.). Daarnaast zal, voor het weergeven van een kaart waarop de verschillende gebruikers staan aangegeven, de Google Maps API worden gebruikt.
 
<b>Potentiële technische problemen</b>

Het idee is om in de applicatie de locatie standaard elke minuut bij te werken. De afbakening van deze tijdseenheid kan op verschillende manieren geschieden. Beide manieren brengen hun eigen problemen met zich mee:
- Wanneer een minuut aan de hand van een klok-eenheid bepaald wordt, plaatsen alle gebruikers - die de standaard tijdseenheid geselecteerd hebben - tegelijkertijd een request op de database, wat bij een groot aantal gebruikers problematisch kan zijn.
- Het meten van de tijd op het apparaat van de gebruiker voorkomt dit probleem, maar is daarbij ook lastiger te implementeren.
 
<b>Gelijksoortige applicaties</b>

Er zijn een aantal apps in de Google Play Store die hetzelfde doen voor de gebruiker:
- Life360: focust zich op families; er kunnen groepen aangemaakt worden waarbinnen een chatfunctie is toegevoegd.
- Glympse: heeft geen duidelijke doelgroep. Verschilt fundamenteel met de voorgestelde applicatie door de gebruiker voor een van te voren bepaalde periode real-time te volgen. 
- Find My Friends: lijkt erg veel op de voorgestelde app, maar kent een aantal extra functies. Gebruikers kunnen ook hier groepen aanmaken, waarmee gechat kan worden en gebruikers kunnen hun contacten een alert sturen.
 
<b>Minimaal werkbare product (MVP)</b>

Voor deze applicatie zijn een aantal onderdelen essentieel. Allereerst moet de gebruiker een account aan kunnen maken bij het eerste gebruik, of in kunnen loggen wanneer deze uitgelogd is. Vervolgens moet een kaart getoond worden, waarop de locatie van alle contacten van de gebruiker te zien zijn. Contacten moeten tevens kunnen worden toegevoegd en vriendschapsverzoeken moeten geverifieerd kunnen worden door de ontvangende gebruiker. 

Een functie die niet nodig is, maar het product iets completer maakt is ten eerste een <i>I’M HERE</i>-functie. Wanneer een gebruiker in de buurt is van een contact, kan het betreffende contact aangeklikt worden. Als dit gedaan wordt, deze functie ingeschakeld. De functie kan gebruikt worden wanneer men zich bevindt op drukke plekken - bijvoorbeeld op festivals - waardoor elkaar vinden erg lastig wordt. Wanneer deze functie geactiveerd wordt, kleurt het scherm van de gebruiker rood en wordt de helderheid tot het maximale niveau verhoogd. Tevens verschijnt de tekst “I’m here” op het scherm. De gebruiker kan zijn toestel boven zich uit steken en zo de kans op het vinden van de ander vergroten. 

Daarnaast is het wenselijk om voor het uitschakelen van de locatie-tracking om een wachtwoord te vragen. Kwaadwillenden, die de telefoon van een ander in handen zouden kunnen hebben, kunnen zo worden opgespoord.

<b>Optionele functies</b>
- Notificatie als een nieuwe foto binnen komt.
- Gebruikers in staat stellen een verzoek tot het maken van een foto te sturen.

# Schetsen
![alt text](https://github.com/a-deda/share-location/blob/master/doc/1-main.png)
![alt text](https://github.com/a-deda/share-location/blob/master/doc/2-main-request.png)
![alt text](https://github.com/a-deda/share-location/blob/master/doc/3-side-panel.png)
![alt text](https://github.com/a-deda/share-location/blob/master/doc/4-contacts.png)
![alt text](https://github.com/a-deda/share-location/blob/master/doc/5-add-contact.png)
![alt text](https://github.com/a-deda/share-location/blob/master/doc/6-register.png)
