---
title: Les fonctions
tags:
  - Javascript
  - Developpement
  - Fondamentaux
  - Functions
  - Typescript
---

# 2024-05-18-17-54-13 Les Functions

## Les functions sont des valeurs

C'est une valeurs qui fait des traitements sur des valeurs.

Une **procedure** ne retourne aucune valeurs
Une **methode** retourne une valeurs

```js
function printHelloWorld() {
  console.log("Hello World");
} // Une procedure, cette fonction ne retourne aucune valeur

function sum(a, b) {
  return a + b;
} // Une methode, cette fonction retourne l' addition de a + b;
```

En javascript les fonction peuvent etre declarer dans des context differends.

Si je declare la fonction avec le mot **function**, cette fonction est accessible dans le **scope global**
c'est a dire dans tout le fichier.

Une fonction peut etre **nomee** ou **anonyme**

#### Fonction Nomee - Fonction Anonyme

```js
function Sum(a, b) {
  return a + b;
}
```

One shot. C'est une fonction qui s'execute a un moment specifique.

```js
const sum = function (a, b) {
  return a + b;
}; // C'est une fonction anonyme
```

Le comportement des fonctions different selon le type de fonction.

```js
const sum = function (a, b) {
  return a + b;
}; // fonction annonyme;

function subStract(a, b) {
  return a - b;
} // fonction nomee

if (true) {
  sum(1, 3); // affiche 3
  subStract(4, 2); // affiche rien du tout
}
```

Le scope de la fonction est important, dans l'exemple au dessus nous avons quatre **scopes**.

- Le scope de la fonction anonyme **sum()**
- Le scope de la fonction nomee **subStract()**
- Le scope de la condition **if**
- Le scope **global** du fichier

La longueur d'un **scope** se definit par ses **accolades** **{}**

Le mot cle **function** declare un fonction dans **TOUT LE PERIMETRE DU CONTEXT GLOBAL**
consequence dans le **context enfant** la function **subStract()** existe.

La fonction anonyme **const sum = ()** existe **UNIQUEMENT DANS LE CONTEXT GLOBAL**
Consequence dans le **scope** du context enfant **if** la fonction annonyme n'existe pas,
ce ne sont pas les memes fonction.
