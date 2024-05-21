---
title: Filtrer un tableau
tags:
  - Javascript
  - Typescript
  - Developpement
  - Tableaux
  - Fondamentaux
---

# 2024-05-18-20-51-07 Filtrer un tableau

En javascript pour filtrer les elements d'un tableau on utilise la methode **filter**

```js
const numbers = [1, 2, 3, 4, 5];
evenNumbers = [];
eventNumbers = numbers.filter(function (n) {
  return n % 2 === 0; // Si la condition est true
}); // return [2, 4]
```

Javascript check pour chaque element si la condition est true ou false et la return.
