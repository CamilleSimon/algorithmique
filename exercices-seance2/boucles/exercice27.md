# Exercice 27

## Enoncé

Ecrire un algorithme qui demandeun nombre de départ, et qui calcule sa factorielle. 
NB: la factorielle de `8`, notée `!8`, vaut : 
`1 x 2 x 3 x 4 x 5 x 6 x 7 x 8`

## Correction

```
Variables
    valeur, factorielle : entier
Instructions
    Ecrire("Donner un nombre : ")
    Lire(valeur)
    factorielle ← 1
    Pour compteur de 1 à valeur faire
        factorielle ← factorielle * compteur
    FinPour
    Ecrire("Factorielle ", valeur, " vaut : ", factorielle)
```
