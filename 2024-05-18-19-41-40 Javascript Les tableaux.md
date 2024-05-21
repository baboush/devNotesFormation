---
title: Les tableaux
tags: ["Javascriot", "Typescript", "Tableaux", "Developpement", "Fondamentaux"]
---

# 2024-05-18-19-41-40 Les tableaux

En javascript un tableau se declare avec **[]**;

```js
arr[];
arr = [1,2,3,4,5]; // affiche un tableau [1,2,3,4,5];
arr2 = []

for (let i = 0; i < arr.length; i++) {
  arr2[i].push(arr[i] * 2);
} // [2,4,6,8,10]
```

En javascript on n'utilise pas la boucle **for**

- Utilise une variable intermediaire **i**
- Effet de bord avec l'exterieur **arr[i]** n'a strictement rien a foutre dans le scope de la boucle
- Traitement superieur a une ligne
- Pas de valeur de retour Obliger d'ajouter une nouvelle valeur.

#### For In

```js
arr[];
arr = [1,2,3,4,5]; // affiche un tableau [1,2,3,4,5];
arr2 = [] // on

for(const number in arr){
  arr2.push(number * 2);
}
arr2; // afficher [0,2,4,6,8]
```

Aucun Interret le **for in** boucle sur les index des tableaux

##### For Const

```js
arr[];
arr = [1,2,3,4,5]; // affiche un tableau [1,2,3,4,5];
arr2 = [] // on

for(const number of arr){
  arr2.push(number * 2);
}
arr2; // afficher [2,4,6,8,10]
```

La boucle **for of** fait le travaille.
Cepandant qu'elles sont les differences avec la boucle for classique

- On elimine la variable intermediaire
- Toujours un effet de bord avec l'exterieur
- Toujours un traitement superieur a 1 ligne
- Toujours Pas de valeur de retour

##### ForEach

```js
arr[];
arr = [1,2,3,4,5]; // affiche un tableau [1,2,3,4,5];
arr2 = [] // on

arr.forEach(function(n){
  arr2.push(n * 2)
})
arr2; // afficher [2,4,6,8,10]
```

 La fonction forEach applique un **callBack** (traitement) sur chaque element du tableau

- Pas de variable intermediaire
- Elimine casimment tous les effets de bords
- Peut tenir sur une ligne
- Toujours obliger de retourner la valeur.

##### Map()

```js
const arr = [1, 2, 3, 4, 5]; // affiche un tableau [1,2,3,4,5];
let arr2;
arr2 = arr.map((number) => {
  return nbr * 2;
}); // [2,4,6,8,10]
```

La fonction **map** Toute les conditions sont remplies.
Difference avec **forEach()**
**map()** est plus precis dans le **forEach()** on peut mettre n'importe quoi et traiter n'importe quoi.
