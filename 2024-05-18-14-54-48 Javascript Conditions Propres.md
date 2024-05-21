---
title: Conditions Propres
tags:["Javascript", "Typescript", "Condition", "Bonne-Pratique", "Developpement", "Booleens", "Fondamentaux"]
---

# 2024-05-18-14-54-48 Condition Propre

## Une conditions doit etre explicite.

### Les conditions de Typescript

L'expression de test est convertie **implecitement** en **[Booleens](2024-05-18-14-36-41%20Les%20Booleens.md)**

```js
if (conditionDeTest) {
} // conditionDeTest est convertie en Booleens.

const conditionDeTest = "Hello World";

if (conditionDeTest) {
} // conditionsDeTest === String Mauvaise Pratique.

const conditionDeTest = ["Arnaud", "Laura", "Juan"];
while (conditionDeTest.length) {
  // conditionDeTest === Number Mauvaise Pratique
}
```

Il faut **expliciter** le type de la condition pour empecher Javascript de faire une conversion **implicite**

```js
const input = {value: ''}; // Cette valeur est true. Toutes les valeur en Javascript sont egale a true
!input = false // cast de input avec !, type d'operateur: unaire la valeur booleen est inverse !true = false
!input.value = true // true, la propriete value est une chaine de caractere vide Valeur boolean dite Falsy. !fales = true

// dans le conctexte booleen input = true
if(!input){
  // si la conditon est fause alors je fais ...
  console.log(input); // n'afficher rien;
}
// dans le context booleen input = true
if(!!input) {
  // si la condition est vrai alors je fais ...
  console.log(input); // affiche {value: ''}
}
// dans le conctexte booleen input.value = false
if(!input.value){
  // si la conditon est vrai alors je fais ...
  console.log(input); // affiche {value: ''};
}
// dans le context booleen input.value = false
if(!!input) {
  // si la condition est fausse alors je fais ...
  console.log(input); // affiche rien
}
```

#### Il faut convertir la condition en true ou en false.

On veut toujours obtenire un booleen dans notre condition de test.

Les operateurs de comparaison **<, <, <=, >=, >** convertisse automatiquement en booleen

```js
const nbrString = "14";
typeof nbrString; // valeur de type String

nbrString < 20 // affiche true
typeof nbrString < 20 // boolean, l'operateur de comparaison

const ageMineur = "14";
const ageMajeur = "25";
ageMineur < ageMajeur = true; // l'operateur de comparaison fonctionne avec les chaine de caractere
typeof(ageMineur < ageMajeur); // les operandes sont de type Booleen
```
