# Security onderzoek
## Inleading
tijd op tijd vinden er data lekken plaats waarbij vele wachtwoorden worden "gekraakt". Doordat deze wachtwoorden zijn gevonden vinden er bepaalde kwetsbaarheden zich binnen het inloggen en is het de taak van programmeurs om er slimme oplossing voor te bedenken om wachtwoorden te verbergen.



## Inhoudsopgave

- Het veilig bewaren van wachtwoorden
- Authorizeren van een gebruiker

## het veilig bewaren van wachtwoorden

In het geval in een datalek wil je dat de hacker niet de data kan gebruiken. Dit kunnen we bereiken met een aantal voorzorgsmaatregelen. 

De eerste voorzorgsmaatregel is niet direct opslaan van de wachtwoorden in onze database. Door elk wachtwoord van een gebruiker te **"hashen"** kunnen we de wachtwoorden niet te herkennen maken. "hashing" is een functie waarbij text in code word omgezet waarbij het process niet om te draaien is, dus inprincipe zou je als applicatie beheerder niet de orginele wachtwoord weten van de gebruiker. Ook zijn alle hashes heel verschillend van elkaar. Stel je hebt een woord en je voegt er een letter aan toe of maakt een letter een hoofdletter. Dan zullen de hashes compleet anders eruit zien

Dit klinkt al helemaal perfect maar toch is dit niet genoeg. Dat komt doordat hackers al een aantal veel gebruikte wachtwoorden en hun "gehashte" versie bewaren in een tabel. Dit tabel is bekend als de **"rainbow table"**. Deze tabel is gevuld van alle hashes die zij wisten terug te werken naar orgineel.

Dan komen we naar onze 2de voorzorgsmaatregel, dat is de **salt**. Salt is simpelweg een extra stuk tekst wat willekeurige stuk tekst bevat wat word toegevoegd in bij het wachtwoord. Als we deze salt toevoegen aan het orginele wachtwoord en vervolgens hashen, is de hash niet meer te vinden in deze rainbow table. 
De salt sla je natuurlijk ook op in je database zodat je deze kunnen samenvoegen met een ingevoerde wachtwoord voor een inlog poging tot het account.

Meeste bedrijven gebruiken de hashes en salts, maar toch vinden hackers er manieren om er weer langs te komen. Met een zogenaamde **"dictionary attack"** en of **"bruteforce"** kan een hacker de wachtwoorden achterhalen. Dit is wel een heel langzaam process *(afhankelijk van het wachtwoord lengte en salt)*, maar toch betekent dit dat er een kleine kwetsbaarheid ligt in het systeem.

Dan komen we aan bij het 3de voorzorgs maatregel genaamd **Pepper**. Pepper is hetzelfde als een salt alleen word deze niet opgeslagen in je database, maar in je applicatie. In principe bij een datalek zou de hacker alleen de database hebben en omdat de Pepper mist in zijn formule om het terug te werken is het zo goed als onmogelijk voor hem om alle wachtwoorden te kraken.

[bron](https://www.youtube.com/watch?v=FvstbO787Qo)

## Authorizeren van een gebruiker
Authorizeren van een gebruiker is het verlenen van rechten aan een gebruiker, zodat zij bepaalde acties kunnen voeren in onze applicatie. Er zijn 2 type manieren van authorizeren en we gaan ze allebij langs en bespreken de pro's en cons van beide manieren.

De eerste manier is een **Session**. Hierbij krijgt de gebruiker een **Session ID** bij het inloggen wat de applicatie genereert. Ook heeft de applicatie een kopie van deze sessie id om het te controleren. hierbij komt het probleem bij het opslaan van de session id, omdat deze word opgeslagen op één applicatie kunnen andere applicaties van hetzelfde uitgever er niet bij, oftewel je zou opnieuw moeten inloggen.

De tweede manier is een **"JWT"** (json-web-token). Hierbij het inloggen word er niks opgeslagen in de applicatie, de gebruiker krijgt een jwt terug waarbij hij deze kan gebruiken voor authorizatie. Jwt tokens worden opgeslagen in de gebruiker wat problemen kan veroorzaken als het onveilig is opgeslagen. Ook is het **stateless**. Dit betekent dat er verder dan de token zelf niks word bijgehouden om de gebruiker the authorizeren.

om het aftesluiten heb ik een overzichtelijk lijst voor de pro's en cons. 

pros/cons
* *JWT*
    - **Scalability**: de jwt word niet opgeslagen op een server waardoor deze op andere domeinen/servers werkt
    - **Maintainability**: jwt word niet opgeslagen op de server wat memory kan besparen
* *Session*
    - **Data visibility/Control**: je weet wie is ingelogd en kunt een bepaalde ingelogde gebruiker gemakkelijk uitschakelen
    - **Bandwith consumption**: session ids gebruiken heel weinig bandwith, omdat deze klein zijn.

(in het lijst zie je alleen pro's staan, want de cons zijn de voordelen wat ze niet hebben.)

[Bron](https://www.loginradius.com/blog/engineering/guest-post/jwt-vs-sessions)
