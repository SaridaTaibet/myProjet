# JavaScript

JavaScript est un langage de script léger, orienté par un objet, principalement connu comme le langage
de script des pages web.

Les variables définies avec `const` se comportent comme des variables, sauf qu'elles ne peuvent pas
être réassignées :

## Exemple

    ```
    <script>

    try {

        const PI = 3.141559;
  
        PI = 3.14;
  
    }

    </script>
    ```

# Block Scope (Portée du Block)

Déclarer une variable avec `const` est similaire à `let` quand il s'agit de  `Block Scope`.
Le x déclaré dans le bloc, dans cet exemple, n'est pas le même que le x déclaré en dehors du bloc :

## Exemple


      ```
        <script>

            var x = 10;

        {

             const x = 2;
  
          }

        document.getElementById("demo").innerHTML = x;

        </script>
      ```

## Attribué au moment de la déclaration

Les variables `const` JavaSript doivent se voir attribuer une valeur lorsqu'elles sont déclarées :

## Exemple

      ```
        Incorrect

          const PI;

         PI = 3.1546565874

        Correct

          const PI = 3.1254879;

        ```
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

       ```
        <script>

            try {

            const PI = 5.022222;
  
            PI = 5.02;
  
         }
 
      catch (err) {
            document.getElementById("demo").innerHTML = err;
           }
        </script>

         ```

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

      ```
          var a = 11 // assigner '11' à 'a'

          var b = a  // copier la valeur de 'a' sur 'b'

          b = 20    // assigner '20' à 'b'

          console.log(a)   // => 11

      ```
L'original n'a pas été modifié, nous ne pouvons que changer la copie.

## Copie une référence

      ```
        var a = {c:11}  

        var b = a 
        
        b.c = 20
        
        console.log(a) //=> {c: 20}    //résultat attendu 20
        
      ```   
      
Assigner la référence d'un nouvel objet à  `'a'`  

Copier la référence de l'objet dans `'a'` vers la nouvelle variable `'b'`

   
Copier la référence de l'objet dans  `'a'` vers la nouvelle variable  `'b'`

`b.c = 20` modifier le contenu de l'objet 'b' fait référence à `console.log(a)`

L'original a également été modifié, puisque la référence a été copiée


## Les objets constants peuvent changer

Vous pouvez modifier les propriétés d'un objet constant :

## Exemple

      ```
        <script>

          const car = {type:"Fiat", model:"500",

          color:"white"};
        </script>

      ```

# ATTENTION

Vous ne pouvez PAS réaffecter un objet constant : 

## Exemple

    ```
      <script>

      try {

            const car = {type:"Fiat", model:"500",
            color:"white"};

         car = {trype:"volvo",  model:"EX60",
  
         color:"red"};
  
            }

        </script>

    ```

## Object.values (Valeur de l'Objet)

La méthode `Object.values()` renvoie un tableau contenant les valeurs des propriétés propres
énumérables d'un objet dont l'ordre est le même que celui obtenu avec une boucle `for....in` (la boucle
`for-in` est différente car elle parcourt également les propriétés héritées)

## Exemple

      ```
          const object1 = {
        a: "somestring",
        b: 11,
        c: false
      };
  
       console.log(Object.values(object1));
  
        //résultats escomptés : Array ["somestring", 11, false(faux)]
  
       ```
## Object.values

`Object.values()` renvoie un tableau dont les éléments sont les valeurs des propriétés
énumérables directement rattachées à l'objet passé en argument. L'ordre du tableau est le même
que celui obtenu lorsqu'on parcourt les propriétés manuellement.
  
## Exemple
  
      ```
  
       var obj = {toto: "truc",  machin: 42};
  
        console.log(Object.values (obj));  // ['truc', 42]
  
        // un objet semblable à un tableau
  
        var obj = {0: 'a', 1: 'b', 2: 'c'};
  
        console.log (Object.values (obj)) ;   // ['a', 'b', 'c']
  
      ```
  
Un objet semblable à un tableau dont les clés sont ordonnées aléatoirement lorsque
des clés numériques sont utilisées, les valeurs sont renvoyées selon l'ordre  numérique
des clés.
  
      ```
  
          var un_obj = {100: 'a', 2: 'b', 7: 'c'};
  
          console.log (object.values (un_obj)); // résultat attendu  ['b', 'c', 'a']
  
        ```
  
getToto est une propriété qui n'est pas énumérable
  
        ```
  
          var mon_obj = Object.create ({}, {getToto; {value: function() {return this.toto;} } } );
  
         mon_obj.toto = "truc";
  
          console.log (Object.values(mon_obj));   // résultat attendu ['truc']
  
      ```
  
## Object.keys
  
`Object.keys()` renvoie un tableau contenant les noms des propriétés propres à  un objet (qui ne
sont pas héritées via la chaîne de prototypes) et qui sont énumérables. L'ordre de ce tableau est 
le même que celui obtenu par une boucle `for....in` (à la différence qu'une boucle for-in liste
également les propriétés héritées).
  
     ```
       const object1 = {
         a: 'somestring',
         b: 42,
         c: false,
       };
    
           console.log(object.keys (object1));
        ```    
    
Résultat attendu :  Array (tableau) `["a", "b", "c"]`
       
    
`Object.keys()`  renvoie un tableau sont les éléments sont les chaînes de caractère des noms des 
propriétés propres et énumérables d'`obj.` L'ordre des propriétés obtenu est le même que celui
obtenu lorsqu'on boucle manuellement sur les propriétés de l'objet.

## Exemple

    ```
    var arr = ["a", "b", "c"];
    
    console.log(Object.keys(arr)); 
    ```
   
Affichera `['0', '1', '2']`

Un objet semblable à un tableau

    ```
    var obj = {0: "a", 1: "b", 2: "c"};
     console.log (Object.keys(obj));
     
     ```
     
Affichera `['0', '1', '2']`

un objet semblalbe à un tableau avec un ordre de clé aléatoire

    ```
    var an_obj = {100: "a", 2: "b", 7: "c"};
    
    console.log(Object.keys(an_obj));
    ```
    
Affichera `['2', '7', '100']`

getToto est une propriété non énumérable

    ```
        varmonObjet = object.create({}, {
                                       getToto : {
                                                    value:function() {
                                                          return this.Toto }
                                                          }
                                                   });
                                                   
         monObjet.toto = 1;
         
         console.log (Object.keys(monObjet));
       ```
       
Affichera `[Toto]` 

### Si on souhaite lister toutes les propriétés, y compris celles qui ne sont pas énumérables, on pourra utiliser 

`object.getOwnPropertyNames()`


    


    
    
   
   
    
  
  



















 
 








