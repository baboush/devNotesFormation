---
title: Asynchrone
tags: ["Javascript", "Typescript", "Developpement", "Intermediaire"]
---

# 2024-05-19-16-45-58 L'Asynchrone

En javascript **tout** est **Asynchrone**

On utilise le mot cle **Promise**

**Promise** Prend deux parametres, une fonction resolve et un fonction reject.

On dit que l'on **Consomme** une promesse.

Une promesse possede trois etats.

- En attente // Nous somment en attente d'un resultat.
- En cour // La promesse est en court de traitement
- Fini // Le resultat de la promesse est retourner.

```js
const getUserData = new Promise(resolve, reject) => { // On creer une nouvelle Promesse.
  setTimeout(() => {
  resolve({name: 'Arnaud'}, 100);
  })
}
```

Ce code seul n'execute rien, pour recupere la promesse il faut **consommer** cette derniere.
Une **Promesse** se consomme avec les mots cle **then**, **catch**, **finaly**

**then** // La promesse ce consomme et retourne un resultat si cette derniere s'est correctement executer.
**catch** // Si une erreur s'est produit lors de l'execution, le block catch return cette erreur.
**finaly** // Permet d'operer un traintement sur le retour de la promesse peut importe si il y a une erreur ou pas.

```js
const getUserData = new Promise(resolve, reject) => { // On creer une nouvelle Promesse.
  setTimeout(() => {
  resolve({name: 'Arnaud'}, 100);
  })
}

getUser.then(user => console.log(user)) // Promise{<Pending>} affiche {name: "Arnaud"};
```

Le resultat s'affiche 100ms apres avoir etait declencher.
Le traitement est differer dans le temps.

### Effets de bord

Deux **Incertitude** :
❌ Delais
❌ Echec
