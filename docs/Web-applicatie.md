# Testplan
om de software qualiteit van mijn applicatie te onderhouden/verbeteren zal ik gebruik maken van de volgende:
* Unit tests: controlleerd of functies doen vervolgens de verwachtingen.
* Overzichtelijk code: variablen/method namen zeggen wat ze doen, splitsing van code etc
* Code scans: controlleerd voor mogelijke beveiligings problemen in de code.

Voor elk microservice moet er verschillende soorten testen worden afgelegd en afhankelijk of ze front of back -end zijn bepaald ook hoe je iets moet testen.

**Front-end**

Front-end is alles wat wij als gebruiker te zien krijgen. Om hiervoor tests te kunnen schrijven moeten we in gedachte houden dat we de tests schrijven op basis van waarvoor het word gebruikt. dingen laten zien. 
Aangezien ik met react werk als front-end framework zal ik tests maken door de ingebouwde testing tools te gebruiken van react om te controleren of componenten worden ingeladen.

**Back-end**

Back-end is alles wat we niet te zien krijgen. Ook wel gezien als alles achter de schermen. Om dit te testen moeten we voornamelijk kijken naar functionaliteit. Functies binnen de back-end testen door middel van unit test waarbij informatie word ingevoerd bij bepaalde functies met al een bekende antwoord waarbij we de functie resultaat aan vergelijken.

**Automatisering testen**

Met github actions kun je de applicatie uitvoeren op github waarbij we ook de tests kunnen aanroepen (ookwel CI).

**Handeling als de software de tests niet behaald**

Bij het niet behalen van een test zal ik simpelweg de probleem moeten vinden door middel van de testlog te zoeken/debuggen. Zodra ik het probleem vind los ik deze meteen op. Vervolgens push ik de oplossing aan de branch en controlleer ik het of het dit keer wel werkt. Zo niet herhaal ik het process.


