# Exercice 23

## Enoncé

Ecrire un algorithme qui demandeun nombre de départ, et qui ensuite affiche les dix nombres suivants. Par exemple, si l'utilisateur entre le nombre `17`, le programme affichera les nombres de `18` à `27`.

## Correction

```
Variables
    valeur, compteur : entiers
Instructions
    Ecrire("Donner un nombre : ")
    Lire(valeur)
    compteur ← 1
    Tant que compteur < 11 faire
        Ecrire(valeur + compteur)
        compteur ← compteur + 1
    FinTQ
```
