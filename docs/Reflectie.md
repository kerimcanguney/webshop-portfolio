# Reflectie

### **Inleiding**

In dit semester heb ik gewerkt aan de IP (individueele project) en de GP (groeps proejct) waarbij er aantal dingen goed en fout gingen. In dit verslag zal ik afgaan wat ik persoonlijk vond wat goed ging en wat fout ging en wat ik volgende keer zou doen.

### **wat ging er goed**

Als groep hebben we regelmatig contact met elkaar waarbij iedereen wel bereikbaar is. We hadden aantal groepsregels opgelegd waardoor we op een professionele wijze met elkaar omgingen bij het werken. Dit hield in het melden van je afwezigheid/aanwezigheid, op de hoogte houden van problemen en melden van zijn progressie op het werk. Ook hebben we redelijk vaak contact gehad met de stakeholders waarbij we ons progressie bespraken, prototypes toonden en feedback vroegen. Verder hebben we goed in groepsverband kunnen werken.

### **wat ging er slecht**

**Agile werken**

In het groep hebben we bepaalde momenten gehad waarbij bepaalde groepslid geen taken opnam, dit zou inprincipe niet mijn probleem moeten zijn, maar mijn handeling hierbij was wel fout. Ik heb als "groeps leider" zijnde geprobeerd om de groepslid aan te sturen om te werken aan bepaalde functionaliteiten. Dit valt niet onder Agile, omdat agile inhoud dat de groepsleden zelf initiatief moeten tonen door zelf een taak op te pikken. 

**Software ontwikkelings process**

Verder vind ik ook dat ik meer bezig kon zijn met ontwerpen (denk hierbij aan flowcharts en front-end designs). Ik heb gemerkt dat zodra zulke ontwerpen worden gemaakt en vervolgens worden gebruikt bij het software ontwikkelings process, dat deze veel effiecenter verloopt EN geeft deze een duidelijker beeld naar het eindproduct.

**CI/CD**

Met de CI/CD ben ik heel laat begonnnen. Ik had de CI wel al eens in de eerste week gemaakt maar kort stuk erna weer gelaten, omdat ik dacht dat deze wel te verwalozen was in het process. Dit was nogmaals een dikke fout van mij aangezien CI/CD was bedacht om het ontwikkelings process te versnellen. Ook (wat ik vind dat er bij hoort) is het testen van mijn applicatie wat ik eigenlijk tijdens het maken ook mijn aandacht aan moest besteden. De manier hoe ik deed testen was het zelf uitproberen en als het werkte ging i,k maar weer verder wat niet een goed idee is.

**Keuze agile methode**

Ook vind ik dat we voor de volgende keer misschien een ander agile methode kunnen gebruiken. Bij het onderzoeken van agile processen hebben we gekozen voor Scrum, omdat meeste al bekend waren met deze methode en omdat het de methode is wat door school gekozen is. Zelf in retrospect vind ik dat bij verder onderzoek dat kanban waarschijnlijk een betere methode zal zijn bij het maken van een applicatie.

Ik heb gemerkt bij het GP dat er meer nadruk gelegd mocht worden op het priotiseren van minder onderdelen tegelijkertijd en werken op deze. Waarbij het afmaken van een onderdeel de bijdragers van dit de andere helpen. Ik denk dat als we deze systeem hadden gebruikt dat we een veel betere product konden opleveren vanwege de overloading van bepaalde groepsgenoten die vast kunnen lopen op bepaalde onderdelen.

**Ontwikkelings process front-end**

Tot slot vind ik dat het een dom keuze was om geen gebruik te maken van een css framework/library. De keus om het niet te gebruiken was, omdat ik dacht was dat de css framework/library ons zou beperken in bepaalde aspecten. Dit is zeker niet het geval en zou juist het tegendeel bewijzen zouden wij het wel gebruikt hebben.

### **wat heb ik hiervan geleerd?**

Ik heb geleerd dat ik voor de volgende keer beter vooruit moet denken en actief stappen moet zetten. Ontwerpen maken is een heel goed manier om ideeën uit te werken en goed te visualizeren. Met ontwerpen kun je voor je zelf een goed beeld vormen voor wat je te doen staat wat heel hulpzaam is bij het software ontwikkelings process.

Verder zal ik met de Agile methode niet als groepsleider meer spelen. Agile is bedacht dat er geen leiding gevende is. Het is een gedecentralizeerde manier van werken. Iedereen pikt zijn taken op van wat er gedaan moet worden. Wellicht voor de volgende keer dat ik merk dat er een groepslid weg valt in de productie van de GP zal ik hem/haar ondersteunen bij zijn/haar taken als dit het probleem zou kunnen zijn.

Ook zal ik eerst overleggen met de groep wat voor een soort agile methode we het fijnste vinden overleggen door alle opties over te gaan. Al hoewel scrum wel een goed manier is om samen te werken denk ik toch dat Kanban een betere manier is aangezien de workload verminderd en of bepaalde taken de moeielijksheidgraad verlaagd door meerdere groepsleden er tegen aan te zetten.

Voor de CI/CD en testen zal ik volgende keer meteen een start aanmaken. Ervoor zorgen dat de applicatie zichzelf automatisch controlleerd op kwetsbaarheden, functionaliteit etc is een grote aanwinst in het onwikkelings process wat ik graag wil meenemen in de toekomstige projecten.

En tot slot zou het een betere keuze zijn geweest om een css framework/library te gebruiken om werkdruk op de front-end te verlagen. Met zo een framework/library zouden we zeker weten een veel duidelijker/mooier front-end kunnen bouwen.


### Eventueele problemen

Met mijn applicatie ben ik tegen paar problemen aangelopen waarbij ik het niet kon oplossen. Hierbij zal ik ze benoemen en kort uitleggen wat het probleem is en hoe ik dit mogelijk kan compenseren.

### Docker images

Voor een van mijn back-end micro services (account-api) was het niet mogelijk om een image te kunnen maken. Ik kreeg hierbij meerdere foutmeldingen waarbij met de hulp van mijn klasgenoten er niet achter konden komen wat de oorzaak was van het probleem. Toch heb ik wel kunnen bewijzen dat ik een image kan bouwen en kan deployen op docker. Met de front-end heb ik een een ge-automatiseerde systeem opgezet waaronder codescans en en dependency's er ook een image word gebouwd en meteen word geplaatst op dockerhub. Deze image is te downloaden en vervolgens te deployen op je local systeem.

### Testing back-end

Ik heb het niet werkend gekregen om de testen te runnen op een van de microservices (product api). Hierbij was het probleem intern met een van de library's wat ik heb gebruikt. Ik ben hier heel lang over aan het doen maar ik heb hierbij op het internet op meerdere pagina's als stackoverflow geen oplossing tegengekomen. Toch heb ik wel de algemene tests geschreven in de .test.js bestand waarbij je kunt zien hoe ik het zou testen. Ook kun je dit verder terug vinden in mijn test plan.

### 3rd party API

Met gebruik van een 3rd party API (stripe) ben ik met het probleem opgelopen om transacties te koppelen aan mijn systeem, omdat ik al reeds aan de einde ben van het semester heb ik met de docent afgesproken om een mock transactie te gebruiken.



