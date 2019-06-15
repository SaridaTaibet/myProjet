NODEJS

Node.js est un environnement de serveur ouvert qui nous permet d'utiliser et d'exécuter le langage JavaScript sur le serveur.

NODE fonctione sur diverses plates-formes (Windows, Mac OS X etc...)

MODULES NODE.JS

C'est comme une bibliothèque JavaScript, avec des fonctions que nous pouvons inclure dans notre application.

MODULES INTEGRES

Nous pouvons utilisez sans installation ces modules qui sont intégrés dans node.js.

Exemple :

assert : Provides a set of assertion tests (fournit un ensemble de tests d'affirmation)
Ce module est utiliser pour tester les expressions de valeur 0 ou la valeur false, un échec d'assertion est provoqué et le programme s'arrête.

child_process : To run a child process (Pour exécuter un processus enfant)

http et https : To make Node.js act as an HTTP server (Pour que Node.js agisse comme un serveur HTTP);

net : To create serves and clients (Pour créer des serveurs et des clients).

MODULE DU SYSTEME DE FICHIERS NODE.JS

Le module http est intégré dans Node.js pour transférer des données via le protocole http
Pour pouvoir inclure le module http utiliser la méthode require():
Exemple :

var http = require ('http');

NODE.JS EN TANT QUE SERVEUR WEB 
http peux écouté les ports du serveur et renvoyer une réponse au client en créant un serveur http via le module http.
Pour cela on utilise la méthode créateServer() pour créer un serveur http :

Exemple



