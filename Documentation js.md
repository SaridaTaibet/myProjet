# JavaScript

JavaScript est un langage de script léger, orienté objet, principalement connu comme le langage
de script des pages web.

Les variables définies avec const se comportent comme des variables le, sauf qu'elles ne peuvent pas
être réassignées :

##Exemple
```
<script>

try {

  const PI = 3.141559;
  
  PI = 3.14;
  
}

</script>
```

# Block Scope

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

Il ne définit PAS une valeur constante. Il définit une référence constante à une valeur.

Pour cette raison, nous ne pouvons pas changer les valeurs primitives constantes, mais nous
pouvons changer les propriétés des objets constants.

## Primitive Values

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

```
















 
 








