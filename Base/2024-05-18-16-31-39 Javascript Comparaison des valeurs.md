---
title: Comparaison des valeurs
tags:
  [
    "Javascript",
    "Typescript",
    "Developpement",
    "Valeur",
    "Operateur",
    "Fondamentaux",
  ]
---

# 2024-05-18-16-31-39 Comparaison des valeurs

## === ou ==

### Le double egale ==

Permet de comparer la valeur de deux variable entre des types differents.

### Triple egale ===

Permet de comparer deux variable avec leurs valeurs et leurs types. Comparaison Stricto sensu.
Si on connait a l'avance le types des variables comparer, le triple egale ne change rien a la comparaison.

#### Application

```js
const age = 18;
const age2 = 18 + 0;
const ageStr = "18";

age == age2 = true;
age === age2 = true;
age == ageStr = true; // Le double egale compare entre deux types differents 18 = "18" => true
age === ageStr = false; // Le triple egale compare la valeur et le type. typeof ageStr = string, typeof age = number. string != number = false

// On ajoute l'operateur unaire
age == +ageStr = true;
age === +ageStr = true; // Rappel l'operateur + cast en number l'operande, typeof ageStr = string => typeof +ageStr =  number;
```

#### Comment utiliser le double egale ==

Dans certain cas le double egale doit etre utiliser.

```js
john = { skill: null };

jack = {};

if (
  (john.skill === null || jack.skill === null) &&
  (john.skill === undefined || jack.skill === undefined)
) {
  console.log("No skill in the team"); // affiche No skill in the team
}
if (john.skill == null && jack.skill == null) {
  console.log("No skill in the team"); // affiche No skill in the team
}
```
