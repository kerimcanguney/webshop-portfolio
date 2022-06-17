# Web application
# Inhoudsopgave
-   [Conceptuel diagram](#conceptuel-diagram) 
-   [C1 context](#c1-context)
-   [C2 container](#c2-container)
-   [Keuze Front-end Framework](#keuze-front-end-framework)
-   [Keuze Back-end Framework](#keuze-front-end-framework)
-   [Data Opslag](#keuze-data-opslag)
-   [UX](#ux)
-   [Testplan](#Testplan)
# Conceptuel diagram
![conceptdiagram](https://user-images.githubusercontent.com/79853948/164680365-a521b5ad-2595-436f-875e-67510c01bf00.png)
In mijn diagram zijn er maar 2 soorten gebruikers, admins en klanten. admins kunnen allerlei producten toevoegen aan de webshop en de klanten kunnen vervolgens
bepaalde producten kopen. de admin in dit geval is meteen ook de eigenaar en supplier.
# C1 context
Hieronder zie je de context diagram. Dit is het op simpelste manier mijn applicatie uit te leggen.
![C1model](https://user-images.githubusercontent.com/79853948/164454842-9ea83dcd-d351-4567-bf42-d485b6709271.png)
We hebben een klant en die kan producten zien en of kopen vanuit de webshop app. De producten worden aangemaakt vanuit de admin portal wat de administrator beheerd. En bij een aankoop speelt er een software van derden om het betaalprocess de onderhouden.
# C2 container
Hieronder zie je de container diagram. Dit bevat meer diepgang op het applicatie en wat voor microservices het bevat.
![C2model](https://user-images.githubusercontent.com/79853948/164454929-509462e5-cfd3-44c9-9626-658f478dccd4.png)
Enige verschil hierbij zijn de microservices.
- Customer website: klant kan hiermee producten zien en of kopen. En gebruik maken van een account.
- Admin website: administrator kan hiermee de API's besturen.
- Account API: maakt een gebruiker aan en of logd deze in. (admin kan account hierbij verwijderen)
- Product API: geeft alle producten weer en de hoeveelheid. (admin kan de producten aanpassen)

# Keuze Front-end Framework
Ik heb ervoor gekozen om React te gebruiken, omdat ik zelf al wat ervaring had opgebouwt met dit framework.
Voor mij werkt react gemakkelijk, omdat je in een component structuur werkt en componenten kunt hergebruiken, daardoor zou dit dus ook het meest optimale keuze zijn. 
Het is een heel populaire framework en stackoverflow/youtube zit vol met antwoorden op veel voorkomende vragen.
React heeft in mijn ogen geen nadelen invergelijken met Vue.js (nieuw dus weinig support) of Angular (beperkte vrijheid en hoge learning curve).
![2019-graph-most-used-front-end-framework](https://cdn.shortpixel.ai/client/q_lossless,ret_img,w_767/https://existek.com/wp-content/uploads/2020/01/frame.png)
[treewebsolutions.com artikel](https://treewebsolutions.com/articles/top-front-end-frameworks-in-2020-year-19)
# Keuze Back-end Framework
Voor de back-end heb ik ervoor gekozen om de SQL gedeelte met C# in de .NET framework te maken en de NOSQL gedeelte in Node.js.
**Waarom c# voor sql?**
Ik ben zelf al wat bekend met C#, maar ik beheers het nog niet helemaal en had ik nog niet de kennis hoe je met een ORM werkt in C#.
**Waarom Entity Framework als ORM?**
EF is de grootste ORM voor c# wat nog gesupport word en ook het meest populaire. Deze ORM is goed gedocumenteerd en er is veel online te vinden erover.
**Waarom Node.js voor nosql?**
Node.js is een taal wat ik heel vaak zie terugkomen maar niet veel van afweet. meeste applicaties wat ik gebruik zijn gemaakt in Node.js en daarom leek het me interessant om dit te leren en verwerken in mijn project. Ook is MongoDB heel goed gedocumenteerd in node.js en zijn er veel andere mediums om informatie vandaan te halen.
# Keuze Data-Opslag
SQL Database is gemaakt in 1970 waarbij de focus was om data verdubbeling te verminderen. 
NoSQL Database is gemaakt in het jaar 2000 waarbij de focus was voor flexibiliteit door de snelle applicatie ontwikkeling.
Pros:
*  SQL
    -   Tabellen staan vast dit helpt om met structuur te werken.
    -   Verticaal schaalbaar
    -   Relationeel systeem
*   NoSQL
    -	Tabellen zijn heel flexibel
    -	Horizontaal schaalbaar
Cons:
* SQL
  -	Tabellen staan vast en kunnen hierdoor niet aangepast worden
* NOSQL
    - Items in je tabel kunnen verschillende schema's bevatten
    - Vereist eigen oplossingen voor nieuwe uitdagingen
[Bron MongoDB.com](https://www.mongodb.com/nosql-explained/nosql-vs-sql)
Uit dit informatie heb ik besloten om beste van beide te gebruiken oftewel een hybride systeem.
gestructuurde data(Accounts/Transacties) zal ik met SQL beheren en ongestructueerde data(Producten) met NOSQL.
De meest populaire database's zullen de meeste community support hebben op websites als stackoverflow. Ook heb ik een online poll gevonden op stackoverflow voor meest populaire databases
daaruit is gebleken dat voor NOSQl mongodb het meest gebruikt is. Voor sql ga ik gebruik maken van Microsoft SQL, omdat het meer beveiligd is dan de andere databases.
![peiling_image](https://user-images.githubusercontent.com/79853948/164269996-9374b0ae-a11f-47b2-a7c0-9b2c0836977e.png)
[peiling databases](https://insights.stackoverflow.com/survey/2021#most-popular-technologies-database-prof)
# UX
Voor de gebruiksvriendelijkheid probeer ik de website zo simpel mogelijk te houden.
### User friendly
![landingpage](https://user-images.githubusercontent.com/79853948/172265493-dffedc33-2a78-4931-b4a6-693391ee964a.png)
Voor de landing pagina wou ik iets moois maken. Dit komt omdat ik veel webshops heb bezogd en ik merkte dat de "betere" webshops altijd een mooie landing pagina hebben. Ik heb dit geprobeerd zo simpel/elegant te maken om de gebruiker niet te overweldigen met wat ze op beeld te krijgen zien (wat ik een nadeel vond van andere websites).
![nav](https://user-images.githubusercontent.com/79853948/172265576-0193fb98-2dc9-472b-9997-487fee772357.png)
Links hebben we een knop om de navigatie balk te openen en vervolgens te navigeren. De categorien om te bezoeken zijn dan 2 klikken verwijderd.
Vervolgens hebben we een simpel overzicht van de opgezochte producten.

![shoppingpage](https://user-images.githubusercontent.com/79853948/174210758-cbc5e241-5be4-4900-9672-ea2223c90fa2.png)
![product page](https://user-images.githubusercontent.com/79853948/174210750-531f2997-7115-4412-b1c1-ee4e07d3e791.png)
![shoppingcart](https://user-images.githubusercontent.com/79853948/174210756-e7e4801b-d803-44c1-93aa-9be8f2a2ffb0.png)

vervolgens de product overzicht pagina, de specificiek product overzicht en de checkout pagina.


### Laadsnelheid
![img](https://user-images.githubusercontent.com/79853948/172265070-012052b1-9a74-4554-af81-62fe084bb5bf.png)
Dit is een raport van de website als je hem probeert te bezoeken. Dit is fijn om te hebben want hiermee kun je de performance van je applicatie snel en overzichtelijk zien, waarmee je dus hiermee je code kunt optimaliseren.





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

**Mijn testen in vs**

Voor de back-end api heb ik eental unit tests geschreven. Wat ik helaas niet kon uitvoeren via github actions.

![tests](https://user-images.githubusercontent.com/79853948/174254802-7b57a1f9-15bb-4e69-afcd-a6bc5be121f4.png)


