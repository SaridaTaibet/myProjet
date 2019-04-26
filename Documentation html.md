# cours de html

## comment on fait des titres en html

### Structure de base html

Le fichier html est composé de balises
    
1ère balise `<!DOCTYPE html>` principal but est d'indiquer aux
navigateur comment interpréter le  document ou la page web
elle sert à valider les pages, elle est toujours situer avant la balise <html>

```html
<!DOCTYPE html>
    Un attribut est toujours à l'intérieur d'une balis sans oublier=
    example : lang=
 
    <html lang="fr">
<html>
```

Lélément html `<head></head>`fournit des informations générales sur le document,
il contient principalement des données  destinées au traitement automatisé et pas nécessairement
lisibles par des humains.

<head>
Les balises meta servent à placer des métadonnées dans une page html
`<meta charset="UTFt8">` est un codage de caratères informatiques conçu
pour coder l'ensemble des caractères du  "répertoire universel de
caractères codés"
   
 <meta charset="UTF-8">
 
L'élément html `<link>` définit la relation entre le document courant et une 
ressource externe. Cet élément peut être utilisé pour définir un lien vers une 
feuilles de styles ou un cadre de navigation.
 
 <link rel="stylesheet" href="styles.css">
 
Pour intégrer ou faire référence à un script exécutable on utilise
la balise `<script></script>`
```
  <script src=index.js></script>
 ```
Il existe plusieurs attributs dont **src** qui définit l'URLd'un script 
et *type* qui définit le language de script utilisé par le script contenu
dans l'élément ou référencé via l'attribut src.
Modifier le texte dans Les balises **title** ou **body**

```
<title> mon dossier </title>
```


# En-têtes
    
Les balises (h1, h2, h3, h4, h5, h6) sont un moyen
de stucturer le contenu d'un texte

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
    
L'élément html `<div>` est un conteneur générique qui permet d'organiser le contenu sans 
représenter rien de particulier. Il peut être utilisé afin de grouper d'autres éléments pour 
leur appliquer un style (en utilisant les attributs *class* ou *id* ou *lang*) 

 
    <div class="warning">
       <img src="/media/examples/photo.jpg
            alt="my photo.">
              <p>c'est ma photo</p>   
     </div> 
    
Pour rajouter une image on utilise la balise <img>

 
      <img src="photo.png" alt="Une photo :)" />
    
      
Ne jamais oublier alt= (pour les mal-voyant) 

</head>
<body>
