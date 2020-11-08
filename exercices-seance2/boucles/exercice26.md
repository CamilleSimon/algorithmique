# Exercice 26

## Enoncé

Ecrire un algorithme qui demandeun nombre de départ, et qui calcule la somme des entiers jusqu’à ce nombre. Par exemple, si l’on entre `5`, le programme doit calculer:
`1 + 2 + 3 + 4 + 5 = 15`

## Correction

```
Variables
    valeur, somme : entier
Instructions
    Ecrire("Donner un nombre : ")
    Lire(valeur)
    somme ← 0
    Pour compteur de 1 à valeur faire
        somme ← somme + compteur
    FinPour
    Ecrire("La somme de 1 à ", valeur, " est ", somme)
```
