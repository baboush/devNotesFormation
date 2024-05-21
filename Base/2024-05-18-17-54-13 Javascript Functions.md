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


```js
const sum = function (a, b) {
  return a + b;
}; // C'est une fonction anonyme
```


```js
const sum = function (a, b) {
  return a + b;
}; // fonction annonyme;

function subStract(a, b) {
  return a - b;
} // fonction nomee

if (true) {
  sum(1, 3); // affiche rien du tout
  subStract(4, 2); // affiche 2
}
```




