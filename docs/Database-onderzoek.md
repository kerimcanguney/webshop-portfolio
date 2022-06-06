# Database research

## inleiding
Tijdens het ontwerpen van mijn database ben ik paar problemen opgelopen. Een van die problemen is het vinden van een geschikte database en de bijbehoorende taal.
In het vorige semester zijn we voornamelijk bezig geweest met **SQL**, maar na het lezen van een [artikel](https://fabric.inc/blog/sql-nosql-ecommerce/) ben ik erachter gekomen dat er ook een andere taal is voor het opslaan van data genaamd **NOSQL**. En na verder onderzoek blijken er nog veel meer te zijn. In dit onderzoek ga ik achterhalen welk database ik zal gebruiken voor mijn project, zodat ik verder kan gaan met het ontwerpen van mijn database.

TL;DR: Hoe kan ik bepalen welke database ik moet gebruiken voor mijn applicatie?

## inhouds opgave
- Wat is een database?
- Wat is sql?
- Wat is nosql?
- Wanneer nosql en wanneer sql?
- Conclusie

## wat is een database
Een database is een georganizeerde collectie van on/gestructuurde data. Hierbij kan een programmeur informatie in opslaan, ophalen, aanpassen en verwijderen. Een simpel vergelijking van een database is een excel tabel. Hierin vind collectie informatie/data, je kunt cellen toevoegen, cellen aflezen, cellen aanpassen en verwijderen. In principe zou het ook mogelijk zijn om een excel bestand te gebruiken als een database, maar dit zou tuurlijk wel onhandig zijn aangezien dit niet de bedoeling is van de applicatie en omdat er gespecificeerde applicaties ervoor zijn.
[bron](https://www.oracle.com/in/database/what-is-database/)
Dit is een voorbeeld van een tabel in een database in dit geval SQL-Server van microsoft.
![sql server](https://www.mssqltips.com/tipimages2/2470_img2.gif)

hierbij zie je kolommen met elk andere personen met elk weer andere informatie. In dit voorbeeld is er sprake van structuur, want elk kolom gebruikt hetzelfde soort type data (bv ContactId bevat allemaal nummers, Title bevaat allemaal text). Paar gegevens zien we als NULL, maar deze kunnen we voor nu vergeten.

Dit is een voorbeeld van een tabel in excel.
![excel](https://www.lifewire.com/thmb/ZDVUL6fidsCw_0nW_cJqH46z-As=/713x535/smart/filters:no_upscale()/Capture-5c02fa7ec9e77c00019bc8dc.JPG)

Als je al eerder hebt gewerkt met excel weet je dat je in elk cel kunt doen wat je wilt in tegenstelling tot het vorige voorbeeld. Als gebruiker zou je bij kolom Age mogelijk het woord 21 schrijven i.p.v de cijfer, waardoor er dus geen sprake is van structuur.

## Wat is sql
Sql is de taal wat word gebruikt om te communiceren met je database waarin Sql alleen kan communiceren met **RDB(relational database)**. Wat deze rdb zo speciaal maakt hoe het informatie opslaat. Sql slaat informatie op in tabellen in gestructueerde manier waarbij tabellen ook onderling relaties met elkaar kunnen delen. 
[video bron](https://www.youtube.com/watch?v=27axs9dO7AE)
## Wat is NoSql
NoSql is een vrij nieuwere taal gebruikt om te communiceren met een **database wat precies het tegenovergestelde is van een RDB**. Een NoSql database maakt niet gebruik van tabellen maar van collecties waarbij elk collectie documenten kan bevatten. Elk document hierin staat 'los' van elkaar in de zin van dat ze geen structuur met elkaar hoeven te vormen. In NoSql heb je vrijwel volledige vrijheid in wat je ermee doet en hoe je het gebruikt. Verder kun je ook onderlinge relaties implementeren tussen documenten.
[bron](https://www.mongodb.com/nosql-explained)

## Wanneer nosql en wanneer sql?
Sql en nosql zijn allebei gemaakt voor hun eigen doeleinden. De ene is niet persee beter dan de ander. Het is maar hoe en waar je het gebruikt.
#### waar zou je sql kunnen gebruiken?
sql is het best toegepast bij het opslaan van informatie wat je gestructureerd moet hebben en of wilt linken aan andere informatie. Hierbij kun je denken aan transactionele data. Elk transactie bevat hetzelfde soort informatie en is gelinked aan een b.v account in het systeem. Hierbij zou sql perfect van toepassing zijn vanwege de gestructureerdheid.
[bron](https://thorntech.com/sql-vs-nosql/)
#### waar zou je nosql kunnen gebruiken?
nosql is het best toegepast bij het opslaan van informatie wat geen structuur heeft. Hierbij kun je denken aan kleding op een website. T-shirts zullen informatie bevatten als kleur, stof en maat, maar een schoen bevat andere informatie als **schoenmaat**. Een T-shirt maat en schoenmaat zijn 2 verschillende soorten informatie wat je niet in de verkeerde producten wilt hebben op je website. Hierbij zou dan NoSql perfect van toepassing zijn vanwege de mogelijkheid voor ongestructureerdheid.
[bron](https://stackoverflow.com/a/3486843)
## Conclusie
Omdat sql en nosql beide pluspunten hebben heb ik bedacht om mijn databases te scheiden waarbij ik een gedeelte sql maak en de ander nosql. Hierbij heb ik bedacht om informatie als accounts, transacties etc in de sql database te onderhouden en informatie als producten onderhoud in nosql. De reden hiervoor is, omdat ik denk dat bij het gebruik van beide talen mijn applicatie veelzijdiger maak en , omdat ik mijn horizon wou verbreden.


### overige bronnen
[bron nosql of sql](https://www.red-gate.com/simple-talk/databases/nosql/how-to-choose-between-sql-and-nosql-databases/)
