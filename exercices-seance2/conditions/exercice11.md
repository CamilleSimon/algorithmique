# Exercice 11

## Enoncé

Ecrire un algorithme qui demande un nombre à l’utilisateur, et l’informe ensuite si ce nombre est positif ou négatif (on laisse de côté le cas où le nombre vaut zéro).

## Correction

```
Variables
    valeur : réel
Instructions
    Ecrire("Entrer un nombre :")
    Lire(valeur)
    Si valeur > 0 alors
        Ecrire("Le nombre est positif")
    Sinon
        Ecrire("Le nombre est négatif")
    FinSi
```
