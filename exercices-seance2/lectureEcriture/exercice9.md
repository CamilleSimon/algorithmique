# Exercice 9

## Enoncé

Ecrire un programme qui demande un nombre à l’utilisateur, puis qui calcule et  affiche le carré de ce nombre.

## Correction

```
Variables
    valeur : réel
Instructions
    Ecrire("Entrer le nombre dont vous voulez les carrée :")
    Lire(valeur)
    valeur ← valeur * valeur
    Ecrire(valeur)
```

Il est également possible de faire `valeur * valeur` directement dans `Ecrire()`.
