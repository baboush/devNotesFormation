---
title: Declaration des Variable
tags: ["Javascript", "Typescript", "Variables", "Developpement", "Fondamentaux"]
---

# 2024-05-18-17-03-19 Declaration des Variable

## let - var - const

### Assignement Operateur

**=** est un assignement operateur, il permet d'assigner (hydrater) une variable.

Il existe trois mot cle, **const, let, var**

On fait simple on vire le **var**
Le **var** pollue le context global, il ne respecte pas le **scope**.

On maximise l'utilisation de **const**.
Il permet de garantire l'imutablilite de la variable.

Le mot cle **let** permet de modifier une variable uniquement dans le context local.

Par default une variable a une valeur undefined.

```js
let a; // Pas d'assignement de valeur
typeof a; // undefined

typeof b; // undefined
```

Le fait de declarer ou ne pas declarer une variable ne change rien
Par default une variable definie ou non definie est undefined.

### Tableau ou Object

Une constante une fois declarer ne peut pas etre reassigner.

```js
const a = 3;
a = 4; // TypeError: Assignement to constant variable.
```

En revanche dans un tableau ou un object son comportement differe.

```js
const arr = ["Un", "Deux", "Trois"];
arr[0] = "Quatre";
console.log(arr); //  affiche ['Quatre', 'Deux', 'Trois'];

const obj = { prop1: "Un", prop2: "Deux", prop3: "Trois" };
obj.prop2 = "Quatre";

console.log(obj); // affiche {prop1: 'Un', prop2: 'Quatre', prop3: 'Trois'};

obj.prop4 = "Cinq"; // j'ajoute une nouvelle propriete

console.log(obj); // affiche {prop1: 'Un', prop2: 'Quatre', prop3: 'Trois', prop4: "Cinq"};
```

Le mot cle **const** empeche juste la reassignation avec l'operate **=** 
