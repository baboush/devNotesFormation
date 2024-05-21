---
title: Javascript Les types de valeur
tags:
  ["Javascript", "Typescript", "Developpement", "Fondamentaux", "Operateurs"]
---

# 2024-05-16-20-15-40 Javascript Les types de valeur

Les operateurs agissent differement en fonction du type de la valeur.

#### Les variables n'ont pas de type, mais les valeurs en ont !

````js
typeOf -> typeOf 3 = number,
typeOf undefined = undefined,
typeOf 'Hello' = string
typeOf null = 'object' ```

 Bug de Javascript inchangeable.
 Peut jouer pas mal de tour !

#### Exemples et cas specifiques

```js
  console.log(1 + "1") = "11";
  typeOf = 'string';

  console.log(!1) = false;
  typeOf = 'false';

  console.log(!"str") = false;
  typeOf = false;

  console.log(+"1") = 1; // equivalent a parsInt("1");
  typeOf = number;
````

Prenont le cas specifiques suivant:

```js
console.log(!1) = false;
```

Nous sommes dans le cas d'un operateur **[Unaire](2024-05-16-19-40-09%20Javascript%20Les%20operateurs.md)**.
Javascript va caster la valeurs en boolean avec l' operateur **!**
Il va ensuite transformer cette derniere en valeurs inverse,
Dans cette Exemples **1 est une valeurs vrai** Avec l'operateur **!** Javascript inverse **vrai** en **false**

1 = true => !1 = !true = false;

```js
console.log(!0) = true; /// 0 = false => !0 = !false = true;
```

Pour javascript 0 est une valeur dite **[Falsy](2024-05-18-13-55-32%20Les%20valeurs%20Falsy.md)**

```js
console.log(+'') = 0; // Un nombre sur une chaine vide vaux 0
console.log(typeof(+'')); // type number

// convertir un boolen en nombre;
console.log(+true) = 1;
console.log(+false) = 0;
```
