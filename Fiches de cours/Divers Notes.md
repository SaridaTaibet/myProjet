# NODE JS EXPRESS

Pour pouvoir utiliser NODE JS, il faut passer par plusieurs étapes :

##  Etape 1 : Créer un projet Firebase

Créer un projet Firebase pour pouvoir l'ajouter à notre application JavaScript.

## Etape 2 : Enregistrez l'application

Ajouter l'application Web au projet Firebase ensuit :
1 - Cliquer sur l'icône Web  dans la page de présentation du projet Firebase pour lancer le flux de travail d'installation.
 
2 - Entrer le surnom de l'application qui sera visible que dans la console Firebase, c'est un indicateur interne de commodité.

3 - Pour l'application Web configurer l'hébergement Firebase (c'est facultatif).

4 - Cliquer et enregistrer l'application.

## Etape 3 Ajouter des SDK Firebase et initaliser Firebase

1 - Installer le SDK JavaScript de Firebase :

a) Exécuter la commande suivante à partir de la racine du projet JavaScript si on ne possède pas le `package.json` fichier.

```node
npm init
```
b) Installer le `firebase` paquet npm et enregistrer dans le `package.json` fichier en exécutant :

```
npm install --save firebase
```

## Relation entre les projets Firebase et Google Cloud Platform (GCP)
et configuréer pour utiliser Firebase et ajouter les SDK Firebase tels que Cloud Firestore, Performance Monitoring et d'autre.

La création d'un nouveau projet Firebase dans la console Firebase, cré en réalité un projet Google Cloud Platform (GCP)
on peut considéré un projet GCP comme un conteneur virtuel pour les donnéesl, le code, la configuration et les serveurs.
### Un projet Firebase est un projet GCP comportant des configurationsm et des services supplémentaires spécifiques à Firebase



Le projet Firebase est l'entité de niveau supérieur pour Firebase

## HTTP

HTTP est un `protocole` le plus utiliser à nos jours.

## GIT

GIT c'est un protocole qui permet de mettre à jour, d'échanger et de partager des fichiers de code (fichiers de texte).

## GIT théorie :

pusher = envoyer dans le (cloud) repositorie dans github

pull = ramener vers soi

re-pusher en modifiant le document qui est dans le repisotorie

revert = revenir en arrière (annuler)

commit = commenter les changements du code avant de le pusher pour avoir plus d'information sur le code

Tous ses mots sont des verbes d'action du protocole GITHUB

##  NODE Théorie :

get = donne moi (tous ou 1 ou 2 objet)

Expemple :

Ce code nous donne tous les objets :
```javascript
app.get ('/read', (req, res) => {
    res.send (hostels).status (200)
});
```
Ce code nous renvoie l'`id` d'un objet:
```javascript
app.get('/read/:id', (req, res) => {
    res.send(hostels[req.params.id]).status(200)
});
```


put = modifier tous

Exemple :

```javascript
app.put('/update/:id', (req, res) => {
    const hostel = hostels.filter(value => value.id !== parseInt(req.params.id));
    hostel.push(req.body);
    res.send(hostel).status(200);
});
```
post = ajouter ou créer un nouveau objet

Exemple :
```javascript

app.post('/create', (req, res) => {
    hostels.push(req.body);
    res.send(hostels).status(201)
 });
```


patch = modifier 1 ou 2 objets


delete = supprimer

Exemple :

Supprime tous l'objet

```javascript
app.delete('/delete', (req, res) => {
    hostels = [];
    hostels.push(req.body);
    res.send(hostels).status(200);
});
```
Supprime l'`id` d'un objet (Les signes `!==` veulent dire inverse de et `===`comparaison)

```javascript

app.delete('/delete/:id', (req, res) => {
    const newhostels = hostels.filter(value => value.id !== parseInt(req.params.id));
    res.send(newhostels).status(200)
});
```

    

postman = client HTTP

express = exprimer

send = envoyer

## NE PAS OUBLIE DE RELANCER SERVEUR ET WATCH

