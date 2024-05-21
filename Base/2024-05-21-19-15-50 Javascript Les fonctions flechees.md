---
title: Arrow Function
tags:
  ["Javascript", "Fondamentaux", "Typescript", "ECMAScript6", "Developpement"]
---

# 2024-05-21-19-15-50 Javascript Les fonctions fleches (Arrow Function)

Les fonctions fleches ont ete introduite en javascript avec ES6 (ECMAScript6)

Elle se caracterise par leur syntaxe **Elegante** et leur **[Scope]**(./2024-05-21-19-20-23 Le Scope.md)

Elles capturent la portée lexicale de l'endroit où elles sont définies, pas la portée d'exécution.

C'est a dire que la fonctions fleches a accees aux bloc d'execution le **SCOPE** dans lequelle elle est declaree.

### Portee lexicale

Portee lexicale: Determine les variables auxquelles une fonction a acces en fonction de l'endroit ou elle est definie dans le code.

### Portee D'execution

Determine les variables auxquelles une fonction a acces en fonction de l'endroit où elle est appelee dans le code


```js
const arnaudEstTresElegant = () => {
  console.log("Oui tout a fait");
  return true;
}; // function fleches
```

```js
function arnaudEstElegant() {
  const adjectif = "Beau"; // variable declarer en dehors du scope de la fonction flechee

  const etIlEstBeau = () => {
    console.log("Arnaud est tres elegant et il est " + adjectif); // Affiche "Variable adjectif" La fonctions fleches fait partie de la portee lexicale de la function dans laquelle elle est declaree
  };

  return etIlEstBeau;
}

const afficherResultat = arnaudEstTresElegant();
arnaudEstTresElegant(); // Affiche Arnaud est tres elegant et il est beau.
```
