# webshop-portfolio
Documentatie S3 Software project

# Inhoudsopgave
*   [Leeruitkomst 1: Web application](#1-web-application)
*   [Leeruitkomst 2: Software quality](#2-software-quality)
*   [Leeruitkomst 3: Agile method](#3-agile-method)
*   [Leeruitkomst 4: CI/CD](#4-cicd)
*   [Leeruitkomst 5: Cultural differences and ethics](#5-cultural-differences-and-ethics)
*   [Leeruitkomst 6: Requiremens and design](#6-requirements-and-design)
*   [Leeruitkomst 7: Business process](#7-business-processes)
*   [Leeruitkomst 8: Professional](#8-professional)

# 1. Web application
Learning outcome: You design and build user-friendly, full-stack web applications.

User friendly: You apply basic User experience testing and development techniques.

Full-stack: You design and build a full stack application using commonly accepted front end (Javascript-based framework) and back end techniques (e.g. Object Relational Mapping) choosing and implementing relevant communication protocols and addressing asynchronous communication issues.

**User friendly:**

hoe ik mijn applicatie user friendly heb gemaakt kun je [hier](https://github.com/kerimcanguney/webshop-portfolio/blob/main/docs/Web-applicatie.md#ux) terugvinden

**Full stack:**

Voor dat ik was begonnen met het programeren ben ik begonnen met het ontwerpen van een [C4-Model](https://github.com/kerimcanguney/webshop-portfolio/blob/main/docs/Web-applicatie.md#c1-context). Hierin staan alle microservices beschreven.

**Front-end**

Keuze/Onderzoek front-end framework heb ik [hier](https://github.com/kerimcanguney/webshop-portfolio/blob/main/docs/Web-applicatie.md#keuze-front-end-framework) beschreven.

De admin website repo kun je [hier](https://github.com/kerimcanguney/websho-admin) vinden.

De customer website repo kun je [hier](https://github.com/kerimcanguney/webshop) vinden.

**Back-end**

Keuze/Onderzoek back-end framework heb ik [hier](https://github.com/kerimcanguney/webshop-portfolio/blob/main/docs/Web-applicatie.md#keuze-back-end-framework) beschreven.

de backend repo kun je [hier](https://github.com/kerimcanguney/webshop-backend) vinden.

[:point_up: Back to top](#webshop-portfolio)

# 2. Software Quality

You use software tooling and methodology that continuously monitors and improve the software quality during software development.

Tooling and methodology: Carry out, monitor and report on unit integration, regression and system tests, with attention for security and performance aspects, as well as applying static code analysis and code reviews.

zie [test plan](https://github.com/kerimcanguney/webshop-portfolio/blob/main/docs/Web-applicatie.md#testplan) voor de documentatie.

[:point_up: Back to top](#webshop-portfolio)

# 3. Agile method
Learning outcome: You choose and implement the most suitable agile software development method for your software project.

Choose: You are aware of the most popular agile methods and their underlying agile principles. Your choice of a method is motivated and based on well-defined selection criteria and context analyses.

**Wat is agile?**
Bij agile worden er meerdere oplevering gedaan (iteraties) om een x aantal tijd, waarbij op elk oplevering de stakeholder zijn input (feedback) kan geven. Door deze methode krijgt de stakeholder per oplevering meer inzicht in het process ("wat is nu mogelijk?", "is het haalbaar?", "doet de design aan de stakeholder zijn eisen?", etc).

![](https://fthegeniushome.files.wordpress.com/2019/08/artboard-1402x.png)
**Agile methoden**

Agile is de process in grote lijnen, maar van binnen in hebben we verschillende interne processen waarin ze verschillen.

**Scrum**

Scrum is een methode wat ook de meest populaire methode is voor agile. In dit process word er een dagelijkse meeting gehouden. De scrum master (leider) legt uit wat er te doen valt en splits het werk in gedeeltes onder de groep. Wat er doen valt word ook genoteerd in de backlog zodat de groepsleden kunnen zien wat er nog moet gebeuren en waaraan hij/zij aan zou kunnen werken. Volgende meeting word er besproken wat er noch te doen valt EN word er een retrospective gehouden ("heeft iedereen zijn taak kunnen doen?", "liepen we tegen problemen aan?", etc).

[wat is scrum?](https://www.scrum.org/resources/what-is-scrum)

**Kanban**

Bij kanban word er voornamelijk gekeken wat er NU gedaan kan worden. Bij het werken in kanban word er een board gebruikt. Deze board bestaat uit meestal 3 rijen: To-Do, Doing en Done. In kanban wil je zo min mogelijk items in *doing* hebben zodat we werkdruk kunnen minimaliseren. Kanban heeft een vrij simpele workflow: Hebben we plek in onze to-do lijst? ja? plak er maar een item bij zo niet help maar een andere lid met zijn item. dit process word heletijd herhaald tot dat de backlog leeg is.

[bron kanbanize](https://kanbanize.com/kanban-resources/getting-started/what-is-kanban)

**Extreme programming**

Bij XP (extreme programming) word er een nadruk gelegd op het produceren van een hogere qualiteit software. XP is het best toepasselijk bij het produceren van een software wat onduidelijke of veel verandere eisen heeft. Hierbij worden er iteraties gedaan om de 1-2 weken waarbij in het werk process voornaamlijk kleine simpele stukken code bouwt en meteen test, om uiteindelijk de kleine stukjes tot een geheel te vormen.

[extreme programming.org](http://www.extremeprogramming.org/when.html)
[agilealliance.org](https://www.agilealliance.org/glossary/xp)
[video uitleg](https://www.youtube.com/watch?v=hbFOwqYIOcU)

**Hoe hebben wij gebruik gemaakt van agile?**

Wij maken gebruik van scrum, omdat deze goed aansluit op het les systeem, want deze werkt in sprint opleveringen. Na elke oplevering moeten we ook retrospectives opleveren, wat heel erg helpt, want je kijkt hierbij terug in het process van toen naar nu waardoor je verbeteringen kunt maken in de volgende sprint oplevering. Elke dag beginnen we met een standup waarmee we bespreken wat we hebben gedaan en wat we te doen hebben. De taken wat we te doen hebben noteren we als [*Issues*](https://github.com/kerimcanguney/WOC-Front-End/issues) in github wat we vervolgens kunnen bekijken op [*github projects*](https://github.com/users/kerimcanguney/projects/1)

![scrum-img](https://scrumorg-website-prod.s3.amazonaws.com/drupal/inline-images/2021-01/scrumorg-scrum-framework-3000.png)

[:point_up: Back to top](#webshop-portfolio)

# 4. CI/CD
Learning outcome: You design and implement a (semi)automated software release process that matches the needs of the project context.

Design and implement: You design a release process and implement a continuous integration and deployment solution (using e.g. Gitlab CI and Docker).

**CI/CD uitleg**
Continues integration(ci) en continues delivery/ continues deployment(cd) is een methode voor het verbeteren van de process bij het maken van software. Bij de CI word de software getest of het werkt en werkt op basis van de gemaakte tests. CD word op basis van de CI aangeroepen om de software te gebruiken in een omgeving als een server of docker image.

CI/CD Back-end
Bij de CD van een microservice (Account-API) in mijn back-end ben ik problemen opgelopen waarbij ik errors krijg bij het creeëren van een docker image. Ik heb hier veel tijd aan besteed en hulp gevraagd aan mijn groepsgenoten, maar zijn we uiteindelijk niet aan een oplossing toe gekomen. Om toch aan te kunnen tonen dat ik de CD wel kan toepassen zal ik deze aantonen door de andere microservice (Product-api) wel te gebruiken. 

Voor de CI ben ik van plan om codescans te gebruiken en unit tests af te leggen en alleen voor de product api zal ik een docker image maken.

CI/CD Front-end
Voor mijn front end word er codescans gedaan en unit-tests afgelegd om vervolgens een docker image te maken van de applicatie waarbij vervolgens andere systemen deze image kan uitvoeren.

[workflows front-end](https://github.com/kerimcanguney/webshop/tree/main/.github/workflows)

[:point_up: Back to top](#webshop-portfolio)

# 5. Cultural differences and ethics
Learning outcome: You recognize and take into account cultural differences between project stakeholders and ethical aspects in software development.

Recognize: Recognition is based on theoretically substantiated awareness of cultural differences and ethical aspects in software engineering.

Take into account: Adapt your communication, working, and behaviour styles to reflect project stakeholders from different cultures.
Address one of the standard Programming Ethical Guidelines (e.g., ACM Code of Ethics and Professional Conduct) in your work.

#### **Cultuur**

##### **Wat is cultuur**

Cultuur is het gedrag onder een groep in een samenleving. Cultuur heb je op allerlei niveau's, van etnische achtergronden tot hobby's. Een duidelijk verschil in cultuur als je het aan iemand vraagt zal die vaak antwoorden met taal of gerechten alhoewel ik niet geloof dat dat zo zeer klopt, omdat een taal alleen de middel van communiceren is en niet hoe en gerechten zijn meer de middel om je honger te dorsten wat wij dus overal terug zien. Cultuur is het verschil in gedrag. Denk hierbij eerder aan gedrag qua normen. "Is het normaal om te laat te komen?", "Is het gewoonlijk om een cadaeu te brengen op een feest?", "Is het verwacht dat je je schoenen binnen uit doet?". Dat valt voor mij eerder onder cultuur.

##### **wat is mijn cultuur**

Ik ben gegroeid in Nederland maar ik ben opgevoed in een Turkse huishouden. Qua gedrag merk ik vanmezelf niet anders te zijn dan meeste klasgenoten. Behalve als het komt tot sporten. Ik merk dat in de ICT-opleiding een cultuur valt waaronder weinig tot bijna geen sporten. Voor mij is dit een groot verschil aangezien ik een best fanatieke sporter ben. Ik denk dat dit cultuur is ontstaan, omdat meeste tech geïnteresseerde niet veel belang hechten aan fysieke gezondheid / of door een gebrek aan motivatie.

##### **hoe pas je groepscommunicatie aan culturele verschillen**

In ons groep hadden we geen probleem met culturele verschillen, omdat we elkaar al kenden wat groepstaken al soepeler maakte. Voor het werken in een groep maken we gebruik van het "programeren in het engels" door onze methodes, variabelen, bestanden etc engelse benamingen te geven om aan te passen om de huidige moderne cultuur.

#### **Ethiek**

##### **Wat is ethiek**

Ethiek in software engineering is de morale juistheid van gedrag in een groep of de morale juistheid van een applicatie.
Op text zegt moraliteit niet veel, maar dit is wel heel belangrijk bij het ontwikkelen van een product. Als iets moreel onjuist is zal dit negatieve feedback leveren van de gebruikers of immoreel gedrag binnen een groep zal leiden tot ruzie of een onvoltooid product.
In software engineering is het daarom belangrijk een goed ethiek/moraliteit te hebben. Om je Ethiek te kunnen verbeteren kun je simpelweg aardiger/bedachtzamer/voorzichtig instellen. 
In het bedrijf Blizzard was er recent een geval van seksuele intimidaties dit zou je als ethical probleem kunnen zien.

##### **Welke ethische aspecten spelen een rol in het project**

Bij mijn eigen project zal er geen ethische probleem plaats vinden, omdat mijn applicatie weinig tot niets doet met de gebruikers hun informatie. Voor de groeps project verwacht ik ook ethische problemen, omdat we simpelweg juist met elkaar omgaan en, omdat de project niet moraliteit in twijfel trekt, want we maken een PIM systeem waarbij alleen producten worden aangemaakt.

bronnnen:

[waarom ethics belangrijk zijn](https://www.nerdynaut.com/importance-of-ethics-for-a-software-engineer#:~:text=It%20leads%20employees%20and%20employers,will%20cause%20a%20serious%20problem.)
    
[waarom ethics belangrijk zijn](https://online.york.ac.uk/why-ethics-must-be-a-constant-in-software-engineering/)
    
[ethical problemen in bedrijf blizzard](https://screenrant.com/activision-blizzard-sexual-harassment-discrimination-lawsuits-2022-status/#:~:text=Two%20lawsuits%20were%20filed%20against,One%20is%20ongoing.&text=Content%20warning%3A%20The%20following%20article,%2C%20sexual%20abuse%2C%20and%20harassment.)
    
[ethical problemen in bedrijf blizzard](https://ethicsunwrapped.utexas.edu/game-over-for-activision-blizzards-toxic-culture)

[:point_up: Back to top](#webshop-portfolio)


# 6. Requirements and Design
Learning outcome: You analyze (non-functional) requirements, elaborate (architectural) designs and validate them using multiple types of test techniques.

Multiple types of test techniques: You apply user acceptance testing and stakeholder feedback to validate the quality of the requirements. You evaluate the quality of the design (e.g., by testing or prototyping) taking into account the formulated quality properties like security and performance.

Met onze stakeholders hebben we redelijk goed contact gehad waarbij we ons app tonen, plan bespreken en tot slot feedback vragen. 
Hierbij was het plannen op het begin toch wat lastiger, omdat we bij het maken de opdracht creative vrijheid kregen.

Om te starten waren we begonnen met het maken van user stories.

![https://user-images.githubusercontent.com/101703190/172395333-e4fcf325-a833-4378-ba0d-2e01db2af952.png](https://user-images.githubusercontent.com/101703190/172395333-e4fcf325-a833-4378-ba0d-2e01db2af952.png)

Dit zijn voornamelijk functionele aspecten. De userstories werden vervolgens besproken met de stakeholder en vervolgens aangepast aan de eisen van hen.
De user stories zijn ook terug te vinden in onze repo's waarbij we ze hebben toegevoegd als [Issue's](https://github.com/users/kerimcanguney/projects/1)

verder hebben we ook designs gemaakt op basis van wat de stakeholders ons hebben laten zien van hun applicatie.
![design-a](https://user-images.githubusercontent.com/101703190/172389533-02a04491-85db-4216-983c-3b4bf143ce46.jpg)

![design-b](https://user-images.githubusercontent.com/101703190/172389569-5916de2b-1ffd-4072-8b8a-7d970a325cae.jpg)

Om de kwaliteit aan te kunnen tonen hebben wij een aantal tests geprogrammeerd om de back-end te testen om bv functionaliteit te garanderen. Ook maken we gebruik van code scans. Dit is een scan wat word gedaan over de hele code en kijkt hierbij of er "orderlijke" fouten zijn en vermeld deze in onze [repo](https://github.com/kerimcanguney/WOC-Back-End), zodat wij deze later kunnen op pikken en fixen. Uiteindelijk maken we ook gebruik van de feedback wat we krijgen om de applicatie op hun bepaalde punten te verbeteren.

**Conclusie**

Ik heb geleerd dat ontwerpen handiger is dan dat ik gedacht had. Als we de ontwerpen een nadruk hadden gemaakt zouden we zeker weten sneller/verder vooruit kunnen werken. 
ook zou ik de tools voor de front-end designs meer hadden willen bespreken om het gemakkelijker te maken, omdat we als groep zijnde lastig te werken vonden met de huidige library wat we nu gebruikten wat nochal complex was.

Al met al zou ik volgende keer voornamelijk functionaliteit bespreken met de klant, onze ontwerpen tonen, meer contact momenten voor *groen licht* op bepaalde vooruitgang(bv mailtje met een screenshot om kort hun feedback te krijgen) en tot slot meer tijd erin steken.

[:point_up: Back to top](#webshop-portfolio)

# 7. Business processes
Learning outcome: You analyze and describe simple business processes that are related to your project.

Simple: Involving stakeholders, predominantly sequential processes with one or two alternative paths.

Related: Business processes during which the software that you are developing will be used (business processes that the software must support by fully or partially automating them).

or

Business processes needed for the success of your software development project (e.g., product release, market release, financial assurance).

Zie [groeps verslag](https://github.com/kerimcanguney/webshop-portfolio/blob/main/docs/BusinessProcess.md) om het business process/documentatie te vinden.

[:point_up: Back to top](#webshop-portfolio)


# 8. Professional
Learning outcome: You act in a professional manner during software development and learning.

Professional manner:

You actively ask and apply feedback from stakeholders and advise them on the most optimal technical and design (architectural) solutions.

You choose and substantiate solutions for a given problem.

**Individueel project**
Bij het persoonlijke project heb ik geprobeerd zoveel mogelijk feedpulse gesprekken te nemen. Bij deze gesprekken nam ik altijd notities op, maar heb ik weliswaar feedpulse vergeten in te vullen. De feedback is wel genoteerd en altijd meegenomen naar het volgende gesprek. 
De feedback wat word gegeven probeer ik altijd te verwerken en stel zou ik problemen technisch of qua design oplopen, bespreek ik deze ten allen tijden met de docent.


**Groeps project**
Bij het groepsproject speelde ik de leidende rol. Elke dinsdag 'smorgens hield ik een scrum meeting waarbij we dan de user stories/progres van vorige week/huidige problem besproken. Al hoewel de helft van ons groepje laterin de semester met de opleiding wouden stoppen probeerde ik ze alsnog op een of ander manier te betrekken.

Ook als leider leidde ik de video gesprekken met de klant waarbij we de progressies bespraken. De gesprekken eindigden altijd met een stuk feedback wat we uiteindelijk noteerden als een *issue* in onze repo wat we dan later konden op pikken. Verder hield ik ook de dagelijkse stand ups waarbij ik de taken verdeelde en onderlinge problemen verhelpen .

[:point_up: Back to top](#webshop-portfolio)

