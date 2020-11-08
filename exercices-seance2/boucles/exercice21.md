# Exercice 21

## Enoncé

Ecrire un algorithme qui demande à l’utilisateur un nombre compris entre 1 et 3 jusqu’à ce que la réponse convienne.

## Correction

```
Variables
    valeur : réel
Instructions
    Ecrire("Donner un nombre entre 1 et 3 (inclut) : ")
    Lire(valeur)
    Tant que valeur < 1 OU valeur > 3 faire
        Ecrire("Donner un nombre entre 1 et 3 (inclut) : ")
        Lire(valeur)
    FinTQ
```
