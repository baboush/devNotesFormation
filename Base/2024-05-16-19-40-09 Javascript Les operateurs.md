---
quickshare-date: 2024-05-17 15:05:39
quickshare-url: "https://noteshare.space/note/clwap04wv4113301mwgr3zo81y#8XccXCSGyW1RwlrZUMSTo5hf12dPOdxb89l+g0Bcdik"
title: Javascript Les operateurs
tags: ['Javascript', 'Typescript', 'Developpement', 'Fondamentaux']
---
# 2024-05-16-19-40-09 Javascript Les operateurs

Permet de traiter les valeurs

## Operande
La valeur sur lequel agit l'operateur
#### Attention
Le comportement de l operateur peut varier en fonction de l'operande

#### Exemples:
```js
  - 3 + 3.14 = 6.14000000000000001
  - "Hello" + "world" = "helloworld" // concatenation
  - 3 + "3000" = "3000"
```
#### Type d'operateurs
 - Binaire: 
    - 2 operande -> 2 + 2, 'jhon' + 'doe'...
 - Unaire: 
    - 1 operande -> !true = false, !2...
 - Logique:
    - true && false => false, true || false => true
 - Comparatif:
    - >,>=, <=, <, ==, ===, 4 > 2 

#### Influence du type sur l'operateur selon la valeur de l'operande
L'operateur + unitaire

```js 
+'2' = 2;
typeof +"2" = number // functionne comme la methode parseInt
```
Javascript convertie l'operande en un nombre
