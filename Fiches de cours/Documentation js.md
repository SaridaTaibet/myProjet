# JavaScript

JavaScript est un langage de script léger, orienté par un objet, principalement connu comme le langage
de script des pages web.

Les variables définies avec `const` se comportent comme des variables, sauf qu'elles ne peuvent pas
être réassignées :

## Exemple

    
    <script>

    try {

        const PI = 3.141559;
  
        PI = 3.14;
  
    }

    </script>
   

# Block Scope (Portée du Block)

Déclarer une variable avec `const` est similaire à `let` quand il s'agit de  `Block Scope`.
Le x déclaré dans le bloc, dans cet exemple, n'est pas le même que le x déclaré en dehors du bloc :

## Exemple


           <script>

            var x = 10;

        {

             const x = 2;
  
          }

        document.getElementById("demo").innerHTML = x;

        </script>


## Attribué au moment de la déclaration

Les variables `const` JavaSript doivent se voir attribuer une valeur lorsqu'elles sont déclarées :

## Exemple
 
        Incorrect

          const PI;

         PI = 3.1546565874

        Correct

          const PI = 3.1254879;

       
## Pas de constantes réelles

Le mot-clé `const` est un peu trompeur.

Il ne définit `PAS` une valeur constante. Il définit une référence constante à une valeur.

Pour cette raison, nous ne pouvons pas changer les valeurs primitives constantes, mais nous
pouvons changer les propriétés des objets constants.

## Primitive Values (Valeur Primitive)

La valeur en mémoire d'un type primitif est sa valeur réelle (par exemple, booléen vrai, 
numéro 20). Un type primitif peur être stocké dans la quantitié fixe de mémoire disponible.

- null, undefined, Boolean, Number, String

Si nous assignons une valeur primitive à une constante, nous ne pouvons pas changer la valeur
primitive :

## Exemple

        
        <script>

            try {

            const PI = 5.022222;
  
            PI = 5.02;
  
         }
 
      catch (err) {
            document.getElementById("demo").innerHTML = err;
           }
        </script>

        

## Référence types

Un type de référence peut contenir d'autres valeurs.
Comme le contenu d'un tyhpe de référence ne peut pas tenir dans la quantité fixe
de mémoire disponible pour une variable, la valeur en mémoire d'un type de référence
est la référence elle-même (une adresse mémoire).

- Array (Tableau)
- Object (Objet)
- Function (Fonction)

JavaScript a 2 types de variables `Primitvies et de Référence`. Une quantité
fixe de mémoire est réservée après la création de chaque variable.
Lorsqu'une variable est copiée, sa valeur en mémoire est copiée, le passage d'une variable
à une fonction via un appel crée également une copie de cette variable.

## Types Primitifs

La valeur en mémoire d'un type primitif est sa valeur réelle (par exemple, booléen vrai,
numéro 20). Un type primitif peut être stocké dans la quantité fixe de mémoire disponible.

- null (nul)
- undefined (indéterminé)
- Boolean (booléen)
- Number (Nombre-Nombre)
- String (Cordage-cordage)

# Exemples de code

## Copie une primitive

      
          var a = 11 // assigner '11' à 'a'

          var b = a  // copier la valeur de 'a' sur 'b'

          b = 20    // assigner '20' à 'b'

          console.log(a)   // => 11
 
L'original n'a pas été modifié, nous ne pouvons que changer la copie.

## Copie une référence
 
        var a = {c:11}  

        var b = a 
        
        b.c = 20
        
        console.log(a) //=> {c: 20}    //résultat attendu 20
        
       
      
Assigner la référence d'un nouvel objet à  `'a'`  

Copier la référence de l'objet dans `'a'` vers la nouvelle variable `'b'`

   
Copier la référence de l'objet dans  `'a'` vers la nouvelle variable  `'b'`

`b.c = 20` modifier le contenu de l'objet 'b' fait référence à `console.log(a)`

L'original a également été modifié, puisque la référence a été copiée


## Les objets constants peuvent changer

Vous pouvez modifier les propriétés d'un objet constant :

## Exemple

      
        <script>

          const car = {type:"Fiat", model:"500",

          color:"white"};
        </script>
 

# ATTENTION

Vous ne pouvez PAS réaffecter un objet constant : 

## Exemple
 
      <script>

      try {

            const car = {type:"Fiat", model:"500",
            color:"white"};

         car = {trype:"volvo",  model:"EX60",
  
         color:"red"};
  
            }

        </script>

    

## Object.values (Valeur de l'Objet)

La méthode `Object.values()` renvoie un tableau contenant les valeurs des propriétés propres
énumérables d'un objet dont l'ordre est le même que celui obtenu avec une boucle `for....in` (la boucle
`for-in` est différente car elle parcourt également les propriétés héritées)

## Exemple

       
          const object1 = {
        a: "somestring",
        b: 11,
        c: false
      };
  
       console.log(Object.values(object1));
  
        //résultats escomptés : Array ["somestring", 11, false(faux)]
  
       
## Object.values

`Object.values()` renvoie un tableau dont les éléments sont les valeurs des propriétés
énumérables directement rattachées à l'objet passé en argument. L'ordre du tableau est le même
que celui obtenu lorsqu'on parcourt les propriétés manuellement.
  
## Exemple
  
       
  
       var obj = {toto: "truc",  machin: 42};
  
        console.log(Object.values (obj));  // ['truc', 42]
  
        // un objet semblable à un tableau
  
        var obj = {0: 'a', 1: 'b', 2: 'c'};
  
        console.log (Object.values (obj)) ;   // ['a', 'b', 'c']
  
      
  
Un objet semblable à un tableau dont les clés sont ordonnées aléatoirement lorsque
des clés numériques sont utilisées, les valeurs sont renvoyées selon l'ordre  numérique
des clés.
  
       
  
          var un_obj = {100: 'a', 2: 'b', 7: 'c'};
  
          console.log (object.values (un_obj)); // résultat attendu  ['b', 'c', 'a']
  
         
  
getToto est une propriété qui n'est pas énumérable
   
  
          var mon_obj = Object.create ({}, {getToto; {value: function() {return this.toto;} } } );
  
         mon_obj.toto = "truc";
  
          console.log (Object.values(mon_obj));   // résultat attendu ['truc']
  
      
  
## Object.keys
  
`Object.keys()` renvoie un tableau contenant les noms des propriétés propres à  un objet (qui ne
sont pas héritées via la chaîne de prototypes) et qui sont énumérables. L'ordre de ce tableau est 
le même que celui obtenu par une boucle `for....in` (à la différence qu'une boucle for-in liste
également les propriétés héritées).
   
       const object1 = {
         a: 'somestring',
         b: 42,
         c: false,
       };
    
           console.log(object.keys (object1));
           
    
Résultat attendu :  Array (tableau) `["a", "b", "c"]`
       
    
`Object.keys()`  renvoie un tableau sont les éléments sont les chaînes de caractère des noms des 
propriétés propres et énumérables d'`obj.` L'ordre des propriétés obtenu est le même que celui
obtenu lorsqu'on boucle manuellement sur les propriétés de l'objet.

## Exemple

    
    var arr = ["a", "b", "c"];
    
    console.log(Object.keys(arr)); 
    ```
   
Affichera `['0', '1', '2']`

Un objet semblable à un tableau
 
    var obj = {0: "a", 1: "b", 2: "c"};
     console.log (Object.keys(obj));
    
     
Affichera `['0', '1', '2']`

un objet semblalbe à un tableau avec un ordre de clé aléatoire
 
    var an_obj = {100: "a", 2: "b", 7: "c"};
    
    console.log(Object.keys(an_obj));
    
    
Affichera `['2', '7', '100']`

getToto est une propriété non énumérable

    
        varmonObjet = object.create({}, {
                                       getToto : {
                                                    value:function() {
                                                          return this.Toto }
                                                          }
                                                   });
                                                   
         monObjet.toto = 1;
         
         console.log (Object.keys(monObjet));
        
       
Affichera `[Toto]` 

### Si on souhaite lister toutes les propriétés, y compris celles qui ne sont pas énumérables, on pourra utiliser 

`object.getOwnPropertyNames()`

# ParseInt

## Définition et Utilisation

La fonction `parseInt()` convertit le premier argument en une chaîne, l'analyse et renvoie un entier ou NaN. Si la valeur renvoyée n'est pas NaN, ce sera l'entier représentant le nombre contenu dans la chaîne dans la base donnée. Une base 10 est utilisée pour la base décimale, 8 pour la base octale, 16 pour la base hexadécimale. Pour les bases supérieures à 10, les lettres de l'alphabet seront utilisées pour représenter les chiffres supérieurs à 9. Par exemple, pour la base hexadécimale, on utilisera les lettres A à F.

Si, lors de l'analyse de la chaîne, `parseInt()` rencontre un caractère qui n'est pas un chiffre dans la base donnée, ce caractère, ainsi que les suivants seront ignorés. `parseInt()` tronque les nombres fournies en valeurs entières (attention donc lorsque les chaînes utilisent une notation scientifique : "4e2" donnera la valeur 4 en base 10 et pas 400). Les espaces en début et en fin de chaîne sont autorisés.

Si la base fournie vaut `undefined` ou `0` (ou si elle n'est pas utilisée comme paramètre), le moteur JavaScript procèdera comme suit :

- Si l'argument `string` commence avec "0x" ou "0X", la base considérée sera la base 16 (hexadécimale) et le reste de la chaîne sera analysé et converti.
Si l'argument `string` commence avec "0", la base considérée sera la base 8 (octale) ou la base 10 (décimale). La base exacte qui sera choisie dépendra de l'implémentation. ECMAScript 5 définit que la base 10 doit être utilisée. Cependant, cela n'est pas supporté par tous les navigateurs. C'est pour cette raison qu'il faut

### toujours spécifier une base lorsqu'on utilise `parseInt()`.

- Si l'argument `string` commence avec une autre valeur, la base considérée sera la base 10.

- Si le premier caractère de la chaîne de caractères ne peut pas être converti, `parseInt()` renverra NaN.

Pour des raisons arithmétiques, la valeur `NaN` n'est un nombre pour aucune base. La fonction `isNaN()` peut être utilisée pour déterminer si le résultat obtenu par `parseInt()` vaut`NaN`. Si `NaN` est utilisé dans une opération arithmétique, le résultat de cette opération sera aussi `NaN`

## (on dit que NaN est une valeur « toxique »).

Pour convertir un nombre en une chaîne de caractères dans une base donnée, on utilisera `monEntier.toString(base)`.

## Exemples

Les Exemples suivants  renvoient tous `15`:

   
        parseInt("0xF", 16);
                   
        parseInt("F", 16);
        
        parseInt("17", 8);
        
        parseInt(15.99, 10);
        
        parseInt("15,123", 10);
        
        parseInt("15*3", 10);
        
        parseInt("15px", 10);
        
Les Exemples suivants renvoient `NaN`

        parseInt("coucou", 8); // Ce sont des lettres et pas des chiffres
        
        parseInt("546", 2);    // Ces chiffres ne sont pas valides pour une représentation binaire.
        
# Map()

La méthode `map()` crée un nouveau tableau avec les réultats de l'appel d'une fonction fournie sur chaque élément du tableau appelant.

lorsqu'on utilise `map`, la fonction `callback` fournie en argument est exécutée une fois pour chacun des éléments du tableau, dans l'ordre du tableau. Chaque résultat de l'opération sur un élément sera un élément du nouveau tableau. La fonction `callback` est appelée uniquement pour les indices du tableau pour lesquels il y a des valeurs affectées (y compris si cette valeur est `undefined`). Si les valeurs ont été supprimées ou qu'elles n'ont jamais été initialisées, la fonction ne sera pas appelée.

`callback` est appelée avec trois arguments : la valeur de l'élément du tableau, l'index de cet élément et l'objet `Array` qui est parcouru.

# ATTENTION !
`map()` construit un nouveau tableau. Si on utilise cette méthode sans utiliser le résultat, mieux vaudra utiliser `forEach`
ou `for...of`.  Pour mieux décider si `map()` est adéquat, regardez si vous utilisez la valeur de retour et/ou si vous renvoyez une valeur avec la fonction `callback` : si ce n'est pas le cas, il ne faut pas utiliser `map()`.

`map` ne modifie pas le tableau sur lequel elle est appelée (bien que la fonction `callback`, si elle est appelée, puisse modifier le tableau.

La liste des éléments à traiter lors de l'opération `map` est définie avant le premier appel à `callback`. Les éléments qui sont ajoutés au tableau après que l'appel à `map` ait été initié ne seront pas traités par la fonction `callback`. Si des éléments ont été modifiés, la valeur utilisée par la fonction `callback` sera celle au moment où `map` est utilisée. Les éléments qui sont supprimés ne sont pas traités. De la même façon, si on applique `map` sur un tableau dont certains éléments sont indéfinis, le résultat possèdera également les mêmes éléments indéfinis.

## Exemples

### Crée un tableau de nombres avec une fonction à argument

Ici, on illustre le fonctionnement de `map` avec une fonction à argument. cet argument sera automatiquement remplacé par chaque élément du tableau au fur et à mesure que `map` parcourt le tableau :

        var nombres = [1, 4, 9];
        var doubles = nombres.map(function(num) {
            return num * 2;
            });
            
 Doubles vaut désormais `[2, 8, 18]`
 Nombres vaut toujours  `[1, 4, 9]
 
### Utiliser `map` pour changer le format d'objets dans un tableau

Dans le code qui suit, on utilise un tableau d'objets pour créer un autre tableau contenant de nouveaux objets dans un autre format :

        var tableauOrig = [{clé:1, valeur:10}, {clé:2, valeur:20}, {clé:3, valeur:30}]
        var tableauFormaté = tableauOrig.map(obj => {
                var rObj = {};
                rObj[obj.clé] = obj.valeur;
                return rObj;
                });
                
TableauFormaté vaut maintenant `[{1:10}, {2:20}, {3:30}]`,

TableauOrig vaut toujours

`[{clé:1, valeur:10}`

  `{clé:2, valeur:20,`
  
  `{clé:3, valeur:30}`
 `]`
  
### Utiliser `map` avec `querySelectorAll`  

Dans cet exemple, on illustre comment utiliser la méthode `map` de façon générique, sur un tableau d'objets collectés grâce à `querySelectorAll` :

        var elems = document.querySelectorAll('select option:cheched');
        var values = Array.prototype.map.call(elems, function (obj) {
        return obj.value;
        });
        
        


        







        
# OBJECT

Le constructeur `Object` crée un wrapper d'objet pour la valeur donnée. Si la valeur est `null` ou  `undefined`, il créera et retournera un objet vide, sinon,
        
        
        
        
        
        










    


    
    
   
   
    
  
  



















 
 








