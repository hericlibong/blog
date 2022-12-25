---
title: "Le Fast Food dans la rue"
date: 2022-12-07T00:40:16Z
tags : ['Image Geolocalisation', 'Twitter', 'Verif!cation Quiz Bot']
categories : ['Osint']
featureDimage: "/images/kebab.jpeg"
---
##  Présentation <br>
Parmi les méthodes pratiquées par tous ceux qui utilisent l'Osint (Open Source Intelligence), la géolocalisation par l'image est celle qui, - pour l'instant - me passionne le plus. Sans doute est-ce lié à mes 17 ans passés à la tête du département photo d'une agence de presse et à l'importance que j'ai toujours accordé au poids des images. <br>
Mais je considère que ces formes d'investigations qui mêlent à la fois Intelligence Artificielle, coup d'oeil, intuition, patience, et éventuellement langage de programmation ont une réelle dimension artistique même si l'esthétique de l'image n'entre pas en compte.<br>  
Depuis 2017 [Verif!cation Quiz Bot](https://twitter.com/quiztime), une équipe de journalistes basés en Allemagne pour la plupart, propose quasi-quotidiennement un quiz photo sur [Twitter](https://twitter.com/quiztime).<br> En général, il s'agit de géolocaliser une image - ou une vidéo - parfois de déterminer l'heure de prise de vue, d'expliquer son contexte... en gros de suivre des instructions qui varient en fonction du sujet. L'essentiel, quand on y arrive, est de décrire le processus, d'expliquer les indices de départ, de détailler la méthode et les outils utilisés.<br>
Bien que qu'ayant déjà eu à faire à certains outils de vérification d'images, j'avoue être encore novice concernant les méthodes d'investigation utilisées en Open Source Intelligence.<br>
C'est pourquoi dans le cadre de mon apprentissage, j'ai décidé de consacrer toute une série d'articles aux solutions trouvées par les internautes - et éventuellement par moi même - aux quizs proposés.<br>
L'objectif sera de décortiquer chaque méthode en partant des premiers indices, de suivre la ou les logiques derrières chaque investigation choisie, et de m'appuyer sur mes quelques connaissances en programmation pour présenter les outils utilisés.<br>
Dans la mesure du possible, j'envisage également contacter certains investigateurs pour plus details sur leur pratique.<br>


{{< admonition type=note title=" bonus : La geolocalisation par l'image selon ChatGPT" open=false >}}

La géolocalisation par l'image est une technique importante en Open Source Intelligence (OSINT) qui permet de déterminer l'emplacement géographique d'une image en utilisant les indices visuels qu'elle contient, tels que les paysages, les bâtiments, les panneaux de signalisation, les véhicules, etc. Elle peut être utilisée dans de nombreux domaines, tels que la vérification de l'authenticité de l'information, la recherche de personnes disparues, la détection de fraude, etc.

Pour utiliser cette technique, il est important de commencer par analyser l'image de manière critique, en prenant en compte tous les éléments visuels qui pourraient être utiles pour déterminer l'emplacement géographique. Il peut être utile de comparer l'image avec d'autres images du même lieu pour voir si elles correspondent. Il est également important de vérifier la date de prise de vue de l'image et de tenir compte de tout changement éventuel dans l'environnement depuis cette date.

Il existe plusieurs outils et services en ligne qui peuvent être utilisés pour la géolocalisation par l'image, tels que Google Maps, Google Street View, Yandex Maps, Bing Maps, etc. Il est également possible d'utiliser des outils de reconnaissance de visages, de plaques d'immatriculation, de bâtiments et de paysages pour aider à la géolocalisation.

Il est important de se rappeler que la géolocalisation par l'image n'est pas une science exacte et que les résultats peuvent être imprécis. Il est donc important de vérifier et de confirmer les résultats obtenus en utilisant d'autres sources d'information. Cela peut nécessiter une certaine patience et de la persévérance, mais cela peut également être très gratifiant de découvrir l'emplacement d'une image grâce à ses propres efforts d'investigation.



{{< /admonition >}}

**Le Kebab dans la rue**
<br>
Pour la géolocalisation d'un lieu par l'image, moins il y a d'indices et plus l'investigation sera difficile. C'est une évidence. Et ici, à priori, nous en avons très peu. Une rue qui ressemble à beaucoup de rues d'Europe, et de l'autre côté un fast-food qui de loin, ressemble à un Kebab.
<br>

<blockquote class="twitter-tweet"><p lang="en" dir="ltr"><a href="https://twitter.com/quiztime?ref_src=twsrc%5Etfw">@quiztime</a> Germany is always nice this time of the year. Please geolocate this picture. Bonus points if you don&#39;t use Google Lens 😀<br>🔁 to invite others<br>🤝 cooperation is welcome<br>✅ Solutions below👇🏻 the GIF-tweet<br>💬 Explain how you did it <a href="https://t.co/w6whSYBZSZ">pic.twitter.com/w6whSYBZSZ</a></p>&mdash; Youri (@y_vdw) <a href="https://twitter.com/y_vdw/status/1588211088696512514?ref_src=twsrc%5Etfw">November 3, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<br>
En général, l'erreur que l'on fait quand on débute est de se ruer sur les moteurs de recherche par image inversée.<br> 
Et c'est vrai qu' il est assez tentant ici d'être attiré par le logo situé sur le panneau du Kebab du trottoir d'en face et de faire des zooms improbables.<br> La plupart du temps, c'est une perte de temps.<br>
Dans notre cas, le mieux est de commencer par analyser l'image de manière critique, en prenant en compte tous les éléments visuels qui pourraient être utiles pour déterminer l'emplacement géographique.



### Le premier indice : le panneau de signalisation
<br>

[Phillip Blockh](https://twitter.com/bockph), dévellopeur rédactionnel norvégien a procédé de cette pour trouver la solution.<br>

En fait, nous avons ici l'exemple typique d'une investigation en Open Source Intelligence qui inclut à la fois observation, intuition, expériience personnelle,  connaissance des outils Osint et notions de langage de programmation.<br>

L'indice qui tout de suite interpellé le regard de Philipp c'est la Typographie de type [Frutiger](https://fr.wikipedia.org/wiki/Frutiger_(police_d%27%C3%A9criture)) du panneau situé à gauche de la photo qui précise que l'on se trouve sur une voix limitée aux véhicules 28 tonnes, mais qui, selon son expérience, est typique du mode de signalisation que l'on trouve en Suisse.

> *Comment j'ai fait : le passionné de typographie en moi a immédiatement reconnu Frutiger sur les panneaux routiers suisses, nous sommes donc en Suisse alémanique. La photo nous montre un kebab près d'une rue où le poids est limité à 28 tonnes.*

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">How I did it: the typography nerd in me instantly recognised Frutiger from the Swiss road signs, so we’re in German-speaking Switzerland. The photo shows us a kebab place near a street with a 28-tonne weight limit.</p>&mdash; Philipp Bock (@bockph) <a href="https://twitter.com/bockph/status/1588258749776437248?ref_src=twsrc%5Etfw">November 3, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
<br>

Effectivement, Si l'on fait une recherche via les données [EXIF](https://fr.wikipedia.org/wiki/Exchangeable_image_file_format) à partir de l'indication figurant sur le panneau, "Zubringerdienst gestattet"  entendons ***Service de navette autorisé*** on est quasi systématiquement renvoyé à des [références suisses](https://duckduckgo.com/?q=zubringerdienst+gestattet+exif&atb=v314-1&ia=web).

<br>

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">Yup, if I hadn’t recognised the Swiss road signs, I would probably have searched in Germany too. As it was, I thought there was a chance that the photo was taken very close to the border, possibly even from the German side.</p>&mdash; Philipp Bock (@bockph) <a href="https://twitter.com/bockph/status/1588280975674441728?ref_src=twsrc%5Etfw">November 3, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
<br>

Intuition, observation, expérience personnelle...Pour l'instant à part la petite recherche EXIF et la vérification de la typographie, on a pas eu besoin d'avoir recours au moindre outil.<br> 
Et nous savons maintenant que notre fast food se trouve très probablement en Suisse Allemande, à moins de 200 mètres d'un panneau indiquant que nous sommes sur une voie limitée aux véhicules de moins 28 tonnes, avec un service de navettes autorisé. C'est encore assez vague, mais ça limite déjà pas mal notre champ de recherches.

### Geolocalisation par les outils 
<br>

A ce stade il est nécessaire d'automatiser la recherche et d'utiliser les outils OSINT. Phillip a opté pour [Overpass Turbo](https://overpass-turbo.eu/) qui est une application en ligne gratuite que l'on peut utiliser pour interroger et visualiser les données d'OpenStreetMap (OSM). <br>
Pour infos, 0SM est une base de données de cartographie collaborative qui contient des informations sur les routes, les bâtiments, les points d'intérêt, les limites administratives, etc. pour de nombreux endroits dans le monde.
<br> 
Overpass Turbo peut effectuer des requêtes spécifiques sur ces données pour un lieu précis ou pour une zone géographique.<br>
Le langage principalement utilisé par Overpass Turbo est l'Overpass QL.<br>

Philipp a choisi de centrer ses recherches sur le Nord de la Suisse afin de géolocaliser les voies limitées aux 28 tonnes comme points d'intérêt, situées à 200 mètres d'un fast-food.<br>

La requête peut être directement testée sur la platforme suur ce  lien  : https://overpass-turbo.eu/s/1nni

<blockquote class="twitter-tweet" ><p lang="en" dir="ltr">Then this Overpass Turbo search with the map focused on northern Switzerland produced few enough results to manually search for a suitable street layout, starting in the bigger cities. <a href="https://t.co/TdtNIUU5sm">pic.twitter.com/TdtNIUU5sm</a></p>&mdash; Philipp Bock (@bockph) <a href="https://twitter.com/bockph/status/1588259591225155585?ref_src=twsrc%5Etfw">November 3, 2022</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script><br>

{{< admonition type=note title=" Quelques mots sur le code Overpass Turbo" open=false >}}

La syntaxe d'Overpass QL peut sembler complexe et il peut être difficile de savoir comment écrire une requête pour obtenir les données que l'on cherche, de prime abord.<br> 
Comme pour tous langage, il est nécessaire de passer un peu de temps à apprendre la syntaxe et à comprendre [comment fonctionnent les différentes commandes et opérateurs.](https://wiki.openstreetmap.org/wiki/Overpass_turbo)
<br>
Cela dit, Overpass Turbo propose un assistant bien pratique pour construire ses requêtes de manière plus simple.<br>

Il est également important de connaître [les tags](https://wiki.openstreetmap.org/wiki/Map_features#Religious) utilisés dans les données OpenStreetMap pour pouvoir cibler les éléments que l'on souhaite obtenir dans la requête. <br>
La page [tag info d'OpenStreeMap](https://taginfo.openstreetmap.org/)fournit de précieuses informations sur les nombreux tags disponibles et sur les différentes manières de les associer selon les cas d'utilisation.<br>


{{< /admonition >}}



Il est important de noter que Overpass Turbo ne peut être utilisé que pour interroger et visualiser les données de l'API OSM, et non pour géolocaliser directement une image.<br> Pour géolocaliser une image, il faudra utiliser d'autres outils et sources d'information en plus des données de l'API OSM.<br>

Philip s'est servi d'open street view en passant manuellement, rue par rue. On peut procéder de la sorte, quand il y a peu de points à visualiser, comme dans le cas présent.<br> Mais quand il y a de nombreux points à consulter il est nécessaire d'automatiser sa recherche.<br> 
[Google Earth Pro Desktop](https://www.google.com/earth/versions/) permet d'importer des données d'Overpass au format KML de les afficher sur la carte et de programmer une  visite touristique. 

D'autres outils de cartographie en ligne, comme Mapbox ou Leaflet, permetttent également d'afficher des données géospatiales sur une carte interactive, de les importer au format KML en offrant des fonctionnalités de personnalisation et de style supplémentaires.


<br>
{{< image src="/images/swiss.png" caption=" Vue aérienne des données sur Google Earth Pro" >}}
<br>







