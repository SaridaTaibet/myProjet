# HTML
HTML (Hyper Text Markup Langage) est un langage qui définit la structure d'une page web.

### Structure de base html
Les structures de base html :

Exemple :

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>test</title>

    <script src="array.js" type="module"></script>
    <script src="for.js" type="module"></script>
    <script src="object.js" type="module"></script>
    <script src="class.js"></script>
    
</head>
```


Le fichier html est composé de balises
    
1ère balise `<!DOCTYPE html>` principal but est d'indiquer aux
navigateur comment interpréter le  document ou la page web
elle sert à valider les pages, elle est toujours situer avant la balise `<html>`

```html
<!DOCTYPE html>
    <html lang="fr">
    
 
</html>
```
Un attribut est toujours à l'intérieur d'une balise 

L'élément html `<head></head>`fournit des informations générales sur le document,
il contient principalement des données  destinées au traitement automatisé et pas nécessairement
lisibles.

Les balises meta servent à placer des métadonnées dans une page html
`<meta charset="UTFt8">` c'est un codage conçu pour coder l'ensemble des caractères du répertoire. 
   
 `<link>` définit la relation entre le document et une ressource externe.
 
 Exemple
 ```
 <link rel="stylesheeet"href=styles.css> </link>
 ```
 
Pour intégrer ou faire référence à un script exécutable on utilise la balise `<script></script>`.
L'attribut  `src` définit l'URL d'un script dans l'élément ou la référence dans l'attribut `src`.

Exemple

``` htlm
  <script src=index.js></script>
 ```



Nous utilisons la balise `title`  pour écrire le titre de notre page.

Exemple :

```
<title> mon dossier personnel </title>
```


# En-têtes
    
Les balises (h1, h2, h3, h4) sont un moyen de stucturer l'en-tête d'un texte.

 ```
    <h1> titre principal </h1>
    <h2> mon projet 1 </h2>
    <h3> mon projet 2 </h3>
    <h4> mon projet 3 </h4>
```

Il existe plusieurs éléments HTML dont `<p>`, `<div`, `<img>` etc....

Pour écrire un paragraphe on utilise la balise <p></p>
 ```
    <p> mon paragraphe 1 </p>
    <p> mon paragraphe 2 </p>
    <p> mon paragraphe 3 </p>
 ```   
    
L'élément html `<div>` signifie diviseur de docuement, il permet d'organiser le contenu sans 
représenter rien de particulier. Il peut être utilisé afin de grouper d'autres éléments pour 
leur appliquer un style (en utilisant les attributs *class* ou *id* ou *lang*) 

 ```
    <div class="warning">
          
     </div> 
 ```   
 
Pour rajouter une image on utilise la balise <img>

``` 
      <img src="photo.png" alt="Une photo :)" /></img>
 ```
    
      
Ne jamais oublier `alt = (pour les mal-voyant)` 

## Les Attributs Universel

`class` est un attribut qui indique une liste de classe associées à une élément courant.
Elle permettent de manipuler les éléments, via CSS ou JavaScript

Exemple de selecteurs de classe

```
document.getElemtnsByClassName
```
`id` est l'attribut universel qui définit un identifiant qui doit être unique pour l'ensemble du document.
Avec un fragment, cet attribut peut identifier un élément lorsqu'on crée un lien.

Exemple :

```
<p id="the name"></p>
```

`is` indique qu'un élément HTML devrait se comporter comme un élément natif.
Il est utilisé uniquement si l'élément personnalisé a été correctement
défini dans le document ainsi qu'il étend le type d'élément sur lequel il est appliqué. 


</head>
<body>
    
