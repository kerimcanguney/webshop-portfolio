# Learning outcome 7 Business processes
**Learning outcome:** You analyze and describe **simple** business processes that are **related** to your project.

**Clarification:**

**Simple:** Involving stakeholders, predominantly sequential processes with one or two alternative paths.

**Related:** Business processes during which the software that you are developing will be used (business processes that the software must support by fully or partially automating them). or
Business processes needed for the success of your software development project (e.g., product release, market release, financial assurance).

Het business proces dat wij willen gaan onderzoeken is het toevoegen van producten op onze website.
Dit is een proces dat een gebruiker moet voltooien om producten toe te voegen aan het systeem en is een belangrijk onderdeel ervan, ons project is immers een product information management system (PIM).
Een belangrijk punt om mee te nemen bij dit proces is hoe wij ervoor gaan zorgen dat attribuutvelden bij alle producten hetzelfde zijn.
Het zou namelijk zo kunnen zien dat iemand een product aanmaakt met een 'gewicht' veld en de ander maakt hem aan met een 'Gewicht' veld.
Ook zou het zomaar kunnen dat iemand een typefout zou maken en dan dus zoiets als 'gewihct' typt.

Het belangrijkste van dit business proces is dus om ervoor te zorgen dat de attribuutnaam van dit veld in dezelfde vorm blijft staan.
Om dit op te kunnen lossen hebben wij categorieën en types toegevoegd aan het product.
Deze velden geven de bijbehorende attribuutvelden aan een product.
Hierdoor zorgen wij ervoor dat product van hetzelfde type, dezelfde attribuutvelden hebben.

Een ander belangrijk punt binnen dit business proces is wat wij hierboven ook al in de oplossing hebben genoemd, namelijk dezelfde velden voor hetzelfde soort product.
Je wilt namelijk als gebruiker dat de attribuutvelden die bij monitoren horen hetzelfde zijn, zodat je ze met elkaar kunt vergelijken.
Met onze oplossing hebben wij er dus voor gezorgd dat dit geen probleem is.

Behalve deze punten van de gelijkheid bij alle producten is het natuurlijk ook belangrijk om na te denken over hoeveel producten een klant toe gaat voegen.
Als klant wil je natuurlijk niet 500x dezelfde stappen doorlopen om een product toe te voegen, wanneer je een grote lijst met producten hebt.
Om dit proces goed te kunnen weergeven, hebben wij dit proces gemodelleerd.
Zie hieronder:

![image](https://user-images.githubusercontent.com/101703190/172382261-f53a1a3f-131f-4ad3-912d-a93eddf17de6.png)

![image](https://user-images.githubusercontent.com/101703190/172382305-4aaca51b-2836-4e4a-a7aa-6379ab71aa9f.png)

In de bovenstaande modellen kun je zien hoe wij het proces eerst hadden gemodelleerd.
Hierin hebben wij gekeken wat de belangrijkste punten waren en deze hebben we vervolgens gecombineerd in het model hieronder:

![image](https://user-images.githubusercontent.com/101703190/172382346-a40a90e5-2b7b-4135-8629-97ff0deed5ea.png)


In dit model kun je zien dat wij het toevoegen van een product gesplitst hebben van het toevoegen van een lijst van producten.
Deze twee processen vereisen namelijk andere acties.

Bij het aanmaken van 1 product kun je zien dat dit een redelijk simpel proces is.
De gebruiker hoeft namelijk alleen maar de stappen de doorlopen en kan dan een product aanmaken.
Als de klant een lijst van producten wil toevoegen, zou hij een lijst kunnen uploaden.
Dit zou dan bijvoorbeeld een Excel bestand zijn met alle producten en hun attributen erin.
Bij het uploaden van deze lijst wordt uiteraard gecontroleerd of hij in correct formaat staat, mocht dit niet het geval zijn, dan krijg je hier een melding van.

Als deze lijst wel correct is, worden de producten door het systeem uitgelezen en toegevoegd aan de lijst van producten.
De klant krijgt vervolgens te zien of de producten in de correcte vorm staan en of er nog velden info missen.
Deze velden zullen dan nog door de klant moeten worden ingevuld.
Als de klant hiermee klaar is, of alle producten al in correcte vorm stonden, krijgt de klant ook te zien dat alle producten correct zijn toegevoegd.

## Conclusie:
Bij het door ons geanalyseerde proces van product toevoegen op onze website zijn er twee punten die het belangrijkst zijn, namelijk hoeveel producten er worden toegevoegd en dat de producten in de juiste vorm staan.
Omdat wij niet zo’n heel groot project gaan maken is het toevoegen van een grote hoeveelheid producten voor ons niet van toepassing.
Wel is het uiteraard handig om na te denken over hoe je dit toe zou willen passen.

Het proces wat wij nu hebben geanalyseerd zouden wij kunnen bespreken met de opdrachtgever.
Hierop kunnen wij dan feedback krijgen en deze verwerken.
Aan de hand van dit model zouden we dan deze functionaliteit kunnen gaan bouwen.

Helaas zijn wij dit keer pas laat aan het model begonnen, waardoor wij deze mogelijkheid niet hebben.
Bij een volgend project zullen wij zeker eerder een model te maken voor een proces wat we willen gaan maken.
Dit is namelijk overzichtelijk voor ons en de opdrachtgever en een goede manier om erachter te komen wat de opdrachtgever nou precies wil.
