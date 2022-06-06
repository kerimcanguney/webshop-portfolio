# Security onderzoek
## Inleading
tijd op tijd vinden er data lekken plaats waarbij vele wachtwoorden worden "gekraakt". Doordat deze wachtwoorden zijn gevonden vinden er bepaalde kwetsbaarheden zich binnen het inloggen en is het de taak van programmeurs om er slimme oplossing voor te bedenken om wachtwoorden te zo goed mogelijk te verbergen. Tijdens het ontwerpen van mijn database kwam ik erachter dat wachtwoorden niet direct mochten worden opgeslagen en dat er bepaalde voorzoorgsmaatregelen moeten worden gehanteerd. Ik kwam er achter door deze [post](https://stackoverflow.com/questions/876342/storing-passwords-in-sql-server).

Hoe kan ik nu mijn wachtwoorden veiligopslaan in de database?


## Inhoudsopgave

- Wat is een database?
- Het veilig bewaren van wachtwoorden
- Authorizeren van een gebruiker
- Conclusie

# Wat is een database?
Een database is een digitaal opslag ruimte waarbij we informatie kunnen opslaan. Bij een database kunnen wij zelf specificeren wat, waar en hoe opslaan.
Er zijn verschillende soorten databases waarbij er verschillende soorten talen zijn om ermee te communiceren (zie [docs](https://github.com/kerimcanguney/webshop-portfolio/blob/main/docs/Database-onderzoek.md) voor meer diepgang).

# het veilig bewaren van wachtwoorden

In het geval in een datalek wil je dat de hacker niet de data kan gebruiken. Dit kunnen we bereiken met een aantal voorzorgsmaatregelen. 

### Hashing
De eerste voorzorgsmaatregel is niet direct opslaan van de wachtwoorden in onze database. Door elk wachtwoord van een gebruiker te **"hashen"** met een **hashing algoritme** kunnen we de wachtwoorden niet te herkennen maken. "hashing" is een functie waarbij text in code word omgezet waarbij het process niet om te draaien is, dus inprincipe zou je als applicatie beheerder niet de orginele wachtwoord weten van de gebruiker. Ook zijn alle hashes heel verschillend van elkaar. Stel je hebt een woord en je voegt er een letter aan toe of maakt een letter een hoofdletter. Dan zullen de hashes compleet anders eruit zien. 

### Hashing algoritme
Er zijn veel soorten hashing algoritmes waarbij ze allemaal vrijwel hetzelfde doen alleen de snelheid en veiligheid is anders. Hashing algoritmes op het begin werden snel gekraakt waardoor ze nuteloos werden, maar na ontwikkeling door tijd zijn ze veel krachtiger en soms zelfs sneller geworden. Hierbij is er een simpel vuistregel om te kiezen voor een hashing algoritme als je belang veiligheid is. Kies de nieuwste en meest vertrouwde. Hoe langer een hashing algoritme bestaat destemeer hashes uit deze algoritme worden verzameld wat voor kwetsbaarheden verzorgd.

### Verschil tussen hashin en encryption
Er bleek nog veel onduidelijkheid voor mij te zijn tussen deze twee termen dus heb ik hier nog verder onderzoek gedaan.
Het beste hoe ik dit snel kan antwoorden is dat encryptie terug te draaien is en hashing niet. Denk aan het kooken van een ei, zodra deze gekookt is kun je hem niet meer vloeibaar brengen. Dat zou je kunnen zien als hashing en encryption zou je kunnen zien als het lezen van een taal. Iedereen die geen Nederlands kan lezen/verstaan zal niets qua inhoud begrijpen wat hier staat, maar iedereen wie dat wel kan zal de inhoud wel kunnen begrijpen.

### Rainbowtable
Dit klinkt al helemaal perfect maar toch is dit niet genoeg. Dat komt doordat hackers al een aantal veel gebruikte wachtwoorden en hun "gehashte" versie bewaren in een tabel. Dit tabel is bekend als de **"rainbow table"**. Deze tabel is gevuld van alle hashes die zij wisten terug te werken naar orgineel.

### Salt
Dan komen we naar onze 2de voorzorgsmaatregel, dat is de **salt**. Salt is simpelweg een extra stuk tekst wat willekeurige stuk tekst bevat wat word toegevoegd in bij het wachtwoord. Als we deze salt toevoegen aan het orginele wachtwoord en vervolgens hashen, is de hash niet meer te vinden in deze rainbow table. 
De salt sla je natuurlijk ook op in je database zodat je deze kunnen samenvoegen met een ingevoerde wachtwoord voor een inlog poging tot het account.

### Dictionary attack / Bruteforce
Meeste bedrijven gebruiken de hashes en salts, maar toch vinden hackers er manieren om er weer langs te komen. Met een zogenaamde **"dictionary attack"** en of **"bruteforce"** kan een hacker de wachtwoorden achterhalen. Dit is wel een heel langzaam process *(afhankelijk van het wachtwoord lengte en salt)*, maar toch betekent dit dat er een kleine kwetsbaarheid ligt in het systeem. Deze twee technieken lijken heel veel opelkaar. Een dictionary attack is het gebruiken van combinaties van woorden, wat ook nog te combineren is met persoonlijke informatie van de account eigenaar (b.v straatnaam, huisnummer etc). Bruteforce is een meer indirecte manier, hierbij probeer je elk mogelijke optie. Denk hierbij aan 0000, 0001, 0002 enzovoort. Bij de bruteforce word er elk optie geprobeerd totdat er een match valt, maar het blijft toch ineffiecent.


### Pepper
Dan komen we aan bij het 3de voorzorgs maatregel genaamd **Pepper**. Pepper is hetzelfde als een salt alleen word deze niet opgeslagen in je database, maar in je applicatie. In principe bij een datalek zou de hacker alleen de database hebben en omdat de Pepper mist in zijn formule om het terug te werken is het zo goed als onmogelijk voor hem om alle wachtwoorden te kraken.

[bron hashing](https://www.youtube.com/watch?v=FvstbO787Qo)

[bron bruteforce/dictionary attack](https://www.fortinet.com/resources/cyberglossary/brute-force-attack)

[bron rainbowtable](https://www.beyondidentity.com/glossary/rainbow-table-attack#:~:text=A%20rainbow%20table%20attack%20is,instead%20encrypt%20passwords%20using%20hashes.)

[bron hashing algoritme](https://blog.jscrambler.com/hashing-algorithms#:~:text=A%20hashing%20algorithm%20is%20a,hashing%20algorithms%20have%20been%20compromised.)

[bron hashing algoritme + verschil encryption](https://geekyhumans.com/de/encryption-and-hashing-algorithms/)

[bron hashing algoritme](https://docs.microsoft.com/en-us/aspnet/core/security/data-protection/consumer-apis/password-hashing?view=aspnetcore-5-0)


## Verschil Authenticatie en Authorizatie
Authenticeren is het valideren van een gebruiker d.m.v inlog gegevens. Met deze gegevens kan een applicatie vervolgens identificeren wie jij bent.
Authorizeren aan de andere kant is het verlenen van rechten. Bv alleen een administrator zou alle berichten mogen verwijderen, maar een gebruiker zou alleen zijn eigen berichten kunnen verwijderen en niet die van anderen. Zou een gebruiker een actie willen doen wat niet binnen zijn **rechten** valt passeert hij zo'n authorizatie niet waardoor de actie niet word vericht. 

## Conclusie
Uit mijn onderzoek kan ik concluderen dat ik gebruik zal maken van hashing en salt voor het opslaan van de wachtwoorden. Dit methode is uit mijn onderzoek veilig genoeg en voor de hashing algoritme zal ik gebruik maken van HMACSHA-256, omdat deze redelijk nieuw is en zeer vertrouwd. Verder zal ik ook gebruik maken van JWT, omdat deze opzichzelf scaled wat mijn applicatie kan verhelpen van mogelijke problemen op lange termijn.
