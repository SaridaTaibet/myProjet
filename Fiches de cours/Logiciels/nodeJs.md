Historique :
• Node.js est créé par Ryan Dahl en 2009
• Sponsorisé par Joyent
• Développé sur la base de la VM V8 de Google
• Version actuelle : Node v7.7.3 (14 Mars 2017)




# NODEJS

`Node.js` est un environnement de serveur ouvert qui nous permet d'utiliser et d'exécuter le langage JavaScript sur le serveur.

NODE fonctione sur diverses plates-formes (Windows, Mac OS X etc...)

## MODULES NODE.JS

C'est comme une bibliothèque JavaScript, avec des fonctions que nous pouvons inclure dans notre application.

## MODULES INTEGRES

Nous pouvons utilisez sans installation ces modules qui sont intégrés dans node.js.

Exemple :

`assert` : Provides a set of assertion tests (fournit un ensemble de tests d'affirmation)
Ce module est utiliser pour tester les expressions de valeur 0 ou la valeur false, un échec d'assertion est provoqué et le programme s'arrête.

`child_process` : To run a child process (Pour exécuter un processus enfant)

`http et https` : To make Node.js act as an HTTP server (Pour que Node.js agisse comme un serveur HTTP);

`net` : To create serves and clients (Pour créer des serveurs et des clients).

# MODULE DU SYSTEME DE FICHIERS NODE.JS

Le module http est intégré dans `Node.js` pour transférer des données via le protocole `http`
Pour pouvoir inclure le module `http` utiliser la méthode `require()`:

Exemple :

     const http = require ('http');


## NODE.JS EN TANT QUE SERVEUR WEB 

`http` peux écouté les ports du serveur et renvoyer une réponse au client en créant un serveur `http` via le `module http`.
Pour cela on utilise la méthode créateServer() pour créer un `serveur http` :

Exemple :

     http.createServer(function (req, res) {

      res.write ('Coucou');

       res.end();

      }).

##  LA CHAINE DE REQUETE

`req` qui est dans la fonction `http.createServer()` représente la demande du client sous forme d'objet dont la propriété `url` suit le nom de domaine :

`demo_http_url.js`

    const http = require('http');
    http.creatServer(function (req, res) {
    res.vriteHead(200, {'Content-Type': 'text/html'});
    res.wrute(req.url);
    res.end();
    }).listen(8080);
    
Lorsque qu'il aura une connexion sur le port 8080 la méthode `http.creatServer()`
s'exécutera grace à la fonction transmise à cette méthode.

## FRACTIONNER LA CHAINE DE REQUETE

Pour scinder la chaine de requête en parties lisibles, il faut intégrés des modules telles que URL

Exemple

     const http = require('http');
     const url = require('url');
     
     http.createServer(function(req, res) {
     res.writeHead(200, {'Content-Type': 'text/html'});
     const q = url.parse(req.url, true).query;
     const txt = q.year + " " + q.month;
     res.end(txt);
     }).listen(8080);
     
      


