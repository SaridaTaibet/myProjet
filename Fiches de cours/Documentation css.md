# Titres

## Syntaxe CSS

 Le CSS se compose d'un sélecteur et d'un bloc de déclaration exemple :

`h1 {color:red; font-size:15px;}`

On peut mettre plusieurs décalrations en les séparant par un (;) et chaque déclaration inclut un nom de propriété CSS et une valeur sont séparés par deux points.

**h1** est le selecteur
**color et font-size** sont les propriétés
**red et 15px** sont les values

**Une déclaration CSS se termine toujnours par un point-virgule et les blocs de déclaration sont
entourés d'accolades**.

Tous les éléments  **p**  seront alignés au centre, avec une couleur de texte rouge
pour les propriétés exemple :
 ```
    p {
         Color: red;
         text-align: center;
    }  
  ``` 
  
## Sélecteurs CSS

  
Les sélecteurs CSS permettent de "rechercher" (ou de sélectionner) des éléments HTML en fonction
de leur nom, **id**, **class**, **attribut**, etc..

  
### Le sélecteur d'identifiant

  
Le sélecteur **id** utilise l'attribut id d'un élément HTML pour sélectionner un élément spécifique.
  
**L'identifiant d'un élément doit être unique dans une page, le sélecteur d'identifiant sert donc à
sélectionner un élément unique**
  
**IMPORTANT**
  
Pour sélectionner un élément avec un identifiant spécifique, écrivez un caractère dièse (#), suivi de 
l'identifiant de l'élément.
  
La règle de style ci-dessous sera appliquée à l'élément HTML avec id="para1" :
  
  
      para1{
           text-align: center;
           color: red;
      }
      
**REMARQUE :** un identifiant ne peut pas commencer par un numéro!
  
  
### Le sélecteur de classe


Le sélecteur de calsse sélectionne les éléments avec un attribut de classe spécifique.
  
Pour sélectionner des éléments avec une calsse spécifique, écriver un caractère point (.), suivi  du nom de la classe

Dans l'exemple ci-dessous, tous les éléments HTML avec class = "center" seront en rouge et centrés:
  
  
         .center {
                texte-align: center;
                color: red;
       }
   
   
 Nous pouvons également spécifier que seuls des éléments HTML spécifiques doivent être affecté par une 
 classe.
 
 Dans l'exemple ci-dessous, seuls les éléments **p** avec class="center" seront alignés au centre 
 
 
      p.center {
           text-align: center;
           color:  red;
    }
    
Les éléments HTML peuvent également faire référence à plus d'une classe.
Dans cet exemple <p>  sera stylé selon calss="center" et class="large":

    <p class="center large"> ceci est un paragraphe.</p>
    
        
### Sélecteurs de regroupement


Pour regrouper les sélecteurs, séparez chaque séecteur par une virgule pour minimiser le code
exemple :

    <style>
    h1, h2, h3, p{
            text-align: center;
            color: red;
    }
    </style>
    
    
### Commentaires CSS


Les commentaires sont utilisés pour expliquer le code et peuvent vous aider lorsque vous 
modifiez le code source à une date ulterieure.

Un commentaire CSS commence par / * et se termine par * /.

Ils peuvent également s'étendre sur plusieurs lignes:

Exemple :

    <style>
    p {
       color: red;
         /* Ceci est un commentaire d'une seule ligne*/
         texte-align: center;
    }
    
    /* C'est une
    multiligne commentaire */
    </style>
    
## Trois façons d'insérer du CSS

1ère - Feuille de style externe

2ème - Feuille de style interne

3ème - Style en ligne

### 1ère - Feuille de style externe

La feuille de style externe, nous permet changer l'apparence d'un site Web entier en ne 
modifiant qu'un seul fichier!

Chaque page doit inclure une référence au fichier de feuille de style externe à l'intérieur
de l'élément ``<link>``.  L'élément ``<link>`` va à l'intérieur de la section ``<head>``.


Exemple :

    <head>
    <link rel="stylesheet" type="tex/css" herf="mystyle.css">
    </head>

Une feuille de style externe peut être écrite dans n'importe quel éditeur de texte. Le fichier ne
doit contenir aucune balise HTML. Le fichier de feuille de style doit être enregistré avec une 
extension CSS.

"mystyle.css"

    body {
         background-color: ligntblue;
      }
      
     h1 {
        color: green;
        margin-left: 20px
      }
   
### 2ème - Feuille de  style interne

Une feuille de style interne peut être utilisée si une seule page a un style unique.
Les styles internes sont définis dans l'élément <style>, dans la section ``<head>`` d'une
page HTLM

Exemple  :

    <head>
    <style>
    body {
          backgroud-color: blue;
    }
    
    h1 { 
          color: maroon;
          margin-left: 40px
    }
    </style>
    </head>
    
### 3ème - Styles en ligne

Un style en ligne peut être utilisé pour appliquer un style unique à un seul élément.
Pour utiliser des styles inline, ajoutez l'attribut style à l'élément concerné. L'attribut
style peut contenir n'importe quelle propriété CSS.

L'exemple ci-dessous montre comment changer la couleur et la marge gauche d'un élément ``<h1>``


Exemple:


      <h1 style="color:blue;margin-left:30px;">mon paragraphe</h1>
    

### Couleur de fond

On peut définir la coueur d'arrière-plan des éléments HTML

Exemple:

    <h1 style=background-color:Blue;">Bonjour</h1>
    
    <p style=background-color:green;">Comment allez-vous</p>
    
### Couleur du texte

Pour définir la couleur du texte:

    <h1 style="color:red;">Bonjour</h1>
    <p style="color:blue;">La famille ça va</p>
    
    
### Couleur de la bordure

On peut définir la couleur des bordures :

Exemple:

    <h1 style="border:2px solide red;>bonjour</h1>
    
### CSS Backgrounds (Arrière-plans)

Les propriétés d'arrière-plan CSS permettent de définir les effets d'arrière-plan des éléments

Propriétés d'arrière-plan CSS :

- Couleur de fond
- Image de fond
- Répétition du fond
- Position de fond

### Couleur de fond

La ```background-color``` propriété spécifie la couleur d'arrière-plan d'un élément.

La couleur de fond d'une page est définie comme ceci /

Exemple :

    body {
         background-color: lightblue;
     }
     
Dans un autre exemple  les éléments ```<h1>```, ```<p>```et ```<div>``` ont des couleurs 
d'arrière-plan différentes :

     h1 {
        background-color: green;
     }
     
     div{
        backgroun-color: lightblue;
     }
     
     p {
        backgroune-color: yellow;
     }   
     
### Image de fond

La ```background-image``` propriété spécifie une image ) utiliser comme arrière-plan d'un élément.

Par défaut, l'image est répétée pour couvrir tout l'élément.

L'image de fond d'une page peut être définie comme ceci :

Exemple :

    body {
         backgroune-image: url("paper.gif");
       }

### Image d'arrière-plan répéter horizontalement ou verticalement

Par défaut, la ```background-image``` propriété répète une image horizontalement 
et verticalement.

Certaines images doivent être répétées uniquement horizontalement ou
verticalement, sinon elles auront l’air étrange, comme ceci:

Exemple :

    body {
         background-image: url("gradient_bg.png");
     }      
        
Si l'image ci-dessus est répétée uniquement horizontalement ```(background-repeat: repeat-x;)```
pour répéter verticalement ```(background-repeat: repeat-y;)``` l'arrière plan aura meilleure
apparence

Exemple :

      body {
          background-image: url("gradient_bg.png");
          background-repeat: repeat-x;
        }
    
    
    
     
     


    


 
 
 
    
      
      
  
    
