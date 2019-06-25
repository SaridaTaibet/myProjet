# HTML

### Structure de base html

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
    <script src="bundle.js"></script>

</head>
```


Le fichier html est composé de balises
    
1ère balise `<!DOCTYPE html>` principal but est d'indiquer aux
navigateur comment interpréter le  document ou la page web
elle sert à valider les pages, elle est toujours situer avant la balise `<html>`

```html
<!DOCTYPE html>
    <html lang="fr">
    //Un attribut est toujours à l'intérieur d'une balise 
    
 
</html>
```

L'élément html `<head></head>`fournit des informations générales sur le document,
il contient principalement des données  destinées au traitement automatisé et pas nécessairement
lisibles par des humains.

Les balises meta servent à placer des métadonnées dans une page html
`<meta charset="UTFt8">` c'est un codage conçu pour coder l'ensemble des caractères du répertoire. 
   
L'élément html `<link>` définit la relation entre le document et une 
ressource externe.
 
Pour intégrer ou faire référence à un script exécutable on utilise
la balise `<script></script>`
Exemple

``` htlm
  <script src=index.js></script>
 ```
L'attributs  `src` définit l'URL d'un script et `type` définit le language de script utilisé par le script contenu
dans l'élément ou la référence dans l'attribut `src`.

Modifier le texte dans Les balises `title` ou `body`

```
<title> mon dossier </title>
```


# En-têtes
    
Les balises (h1, h2, h3, h4) sont un moyen de stucturer l'en-tête d'un texte.

 ```
    <h1> titre principal </h1>
    <h2> mon projet 1 </h2>
    <h3> mon projet 2 </h3>
    <h4> mon projet 3 </h4>
```
Pour écrire un paragraphe on utilise la balise <p></p>
 ```
    <p> mon paragraphe 1 </p>
    <p> mon paragraphe 2 </p>
    <p> mon paragraphe 3 </p>
 ```   
    
L'élément html `<div>` signifie diviseur de docuement, il permet d'organiser le contenu sans 
représenter rien de particulier. Il peut être utilisé afin de grouper d'autres éléments pour 
leur appliquer un style (en utilisant les attributs *class* ou *id* ou *lang*) 

 
    <div class="warning">
       <img src="/media/examples/photo.jpg
            alt="my photo.">
              <p>c'est ma photo</p>   
     </div> 
    
Pour rajouter une image on utilise la balise <img>

 
      <img src="photo.png" alt="Une photo :)" />
    
      
Ne jamais oublier alt = (pour les mal-voyant) 


</head>
<body>
    
