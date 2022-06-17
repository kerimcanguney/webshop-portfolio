# Docker verslag

omdat ik veel problemen ben opgelopen met docker (behalve bij de front-end) wil ik wel even op benadrukken dat ik wel weet hoe docker werkt. Dit verslag is een manier
om te compenseren omdat ik geen docker volledig heb kunnen verwerken in mijn project en om te bewijzen dat ik het wel begrijp.


# Wat is docker
Docker is een software om een virtueele omgeving te creëeren voor je software applicatie, of de gemaakte docker images uit te voeren.

# Waarom docker?

Bij het werken in groepen kan het maar zo zijn dat groepsleden de applicatie niet kunnen uitvoeren op hun systeem, maar dit lukt wel op die van jou. vreemd?
Docker lost dit probleem op!
Docker verwerkt de volledige applicatie in een image (een soort pakket). Deze image kun je vervolgens delen met je collega's die vervolgens met de docker software kunnen uitvoeren.
Omdat deze image de "perfecte" omgeving is voor de applicatie werkt hij ook op andere computer systemen.

# Docker container

een container is een geisoleerde omgeving voor het uit voeren van je applicatie. Ze zijn te vergelijken met een VM (virtual machine). De verschil hierin is dat de containers veel lichter zijn, sneller opstarten, vereisen minder computer kracht, gebruikt de OS van de gebruiker en kunnen in paralel uitgevoerd worden in isolatie.

# Docker file

Een dockerfile is een set instructies voor de dockersoftware om stapgewijs de docker image te bouwen.
Hierbij hebben we ook de dockerignore, zoals je bij de naam al ziet negeert hij bepaalde bestanden.

# Docker compose

Docker compose is een set instructies voor het uitvoeren van de images in een bepaalde container. Hierbij kun je dus bv je API image koppelen aan een SQL image waarbij deze dan met elkaar kunnen werken. 

Zouden de image's los van elkaar geplaatst zijn in verschillende containers zouden ze niet van elkaars bestaan afweten, omdat de containers in compleet isolatie leven.

[bron video](https://www.youtube.com/watch?v=rOTqprHv1YE)

[bron video mosh](https://www.youtube.com/watch?v=pTFZFxd4hOI&t=1445s)

