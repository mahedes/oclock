# Fetch - Conseil technique avancé à un.e apprenant.e


Quand on utilise un url pour aller sur un site, on précède toujours le nom de domaine par http ou https. Exemple : http://wikipedia.com

HTTP est le nom d'un protocole de communication. 
Il en existe plusieurs :
- SMTP : Pour envoyer des email
- FTP : pour transférer des fichiers
- HTTP : pour discuter avec un service web ou un serveur

Le protocole HTTP, c'est un peu comme une sorte de "langage" qu'utilise les ordinateurs/serveurs pour communiquer entre eux. Mais on ne les appelle pas officiellement langage. On les appelle protocole.

HTTP signifie HyperText Transfer Protocol.
C'est donc un protocole qui permet de communiquer avec un site Internet, un serveur. Il va permettre de charger des pages HTML, des styles CSS, des polices de caractères, des images, etc. HTTP nous permet aussi d'envoyer des formulaires et de récupérer et d'envoyer toutes sortes de données depuis ou vers un serveur implémentant ce protocole. Et permet aussi d'échanger des données.

Les méthodes HTTP permettent d'identifier le type de requête que nous souhaitons faire :
- GET : permet de récupérer des ressources (données météo via une API)
- POST : permet de créer ou modifier une ressource (ex: ajout d'un commentaire sur un blog)
- PUT : permet de modifier une ressource (ex: modification du commentaire récemment créer avec POST )
- DELETE : Permet de supprimer une ressource (ex: supprimer le commentaire )

Quand on utilise HTTP, pour demander quelque chose à un serveur, on dit qu'on fait une requète.
Avec Javascript, j'ai la possibilité de faire une requete HTTP pour demander quelques choses à un serveur (ex: récupérer des données sur une API, des données JSON par exemple)

Pour cela je peux utiliser l'ancienne méthode avec XMLHttpRequest ou bien fetch qui est plus récent.
voir documentation: https://developer.mozilla.org/fr/docs/Web/API/Fetch_API/Using_Fetch
voir aussi : https://www.pierre-giraud.com/javascript-apprendre-coder-cours/api-fetch/ 

La syntaxe de base est :
``
let requete = fetch(url, [options])
``

- url – l’URL cible.
- options (paramètres facultatifs : méthode, en-têtes, etc…)



Voici un exemple avec une API météo (www.prevision-meteo.ch)
Ouvrez le lien suivant: https://www.prevision-meteo.ch/services/json/paris
On y trouve des données sous format JSON hébergés sur un serveur distant.
On va pouvoir les récupérer et les intégrer sur notre application grâce à fetch()

``

    fetch("https://www.prevision-meteo.ch/services/json/paris") // je fais une requete HTTP vers le serveur

    .then((response) => response.text()) // je récupère la réponse de la requète

    .then(function (data) { // la réponse est stockée dans data

        let reponse = JSON.parse(data); // je convertis cette donnée en objet Javascript

        console.log(reponse) // j'utilise cette donnée dans l'application (ici je l'affiche seulement dans la console)

    })
``

Si je devais communiquer avec le projet Challenge, je pourrai faire ceci. (Cependant, le code coté serveur devrait avoir quelques ajustements pour retourner une réponse claire)

``

    fetch("https://localhost:8888/students/list")

    .then((response) => response.text()) 

    .then(function (data) { 

        console.log(reponse) 

    })
``

N'hésitez pas à revenir vers moi si vous avez besoin de plus de précisions