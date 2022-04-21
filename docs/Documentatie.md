# Web application

# Inhoudsopgave

-   [C1](#C1)
-   [C2](#C2)
-   [C3](#C3)
-   [Keuze Front-end Framework](#Keuze-Front-end-Framework)
-   [Data Opslag](#keuze-data-opslag)
-   [Data diagram](#Data-diagram)



# C1 context
![C1model](https://user-images.githubusercontent.com/79853948/164454842-9ea83dcd-d351-4567-bf42-d485b6709271.png)
# C2
![C2model](https://user-images.githubusercontent.com/79853948/164454929-509462e5-cfd3-44c9-9626-658f478dccd4.png)
# C3

# Keuze Front-end Framework

Ik heb ervoor gekozen om React te gebruiken, omdat ik zelf al wat ervaring had opgebouwt met dit framework.
Voor mij werkt react gemakkelijk, omdat je in een component structuur werkt en componenten kunt hergebruiken, daardoor zou dit dus ook het meest optimale keuze zijn. 
Het is een heel populaire framework en stackoverflow/youtube zit vol met antwoorden op veel voorkomende vragen.

React heeft in mijn ogen geen nadelen invergelijken met Vue.js (weinig support) of Angular (beperkte vrijheid en hoge learning curve).

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

<!-- # Data diagram
![sql-img](https://user-images.githubusercontent.com/79853948/164265722-031f5f0d-6bbf-43d6-a7c8-5ce85fe5e514.png)
![nosql-img](https://user-images.githubusercontent.com/79853948/164265909-753a37d5-ccf2-43c7-bd77-dc9b2b25706f.png)

Met de blauwe kleur geef ik de SQL database aan en groen NOSQL. -->
