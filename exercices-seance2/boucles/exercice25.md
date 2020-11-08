# Exercice 25

## Enoncé

Ecrire un algorithme qui demande un nombre de départ et qui ensuite écrit la table de multiplication de ce nombre, présentée comme suit (cas où l'utilisateur entre le nombre 7) :

```
Table de 7 :
7 × 1 = 7
7 × 2 = 14
...
7 × 10 = 70
```

## Correction

```
Variables
    valeur : entier
Instructions
    Ecrire("Donner un nombre : ")
    Lire(valeur)
    Ecrire("Table de ", valeur)
    Pour compteur de 1 à 10 faire
        Ecrire(valeur, " × ", compteur, " = ", valeur * compteur)
    FinPour
```
