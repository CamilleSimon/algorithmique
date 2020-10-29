# Exercice 13

## Enoncé

Ecrire un algorithme qui demande un nombre à l’utilisateur, et l’informe ensuite si ce nombre est positif ou négatif (on inclut cette fois le traitement du cas où le nombre vaut zéro).

## Correction

```
Variables
    valeur : réel
Instructions
    Ecrire("Entrer un nombre :")
    Lire(valeur)
    Si valeur = 0 alors
        Ecrire("Le nombre est nul")
    Sinon
        Si valeur > 0 alors
            Ecrire("Le nombre est positif")
        Sinon
            Ecrire("LE nombre est négatif")
        FinSi
    FinSi
```