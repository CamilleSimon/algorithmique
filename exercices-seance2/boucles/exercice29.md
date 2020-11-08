# Exercice 29

## Enoncé

Réécrire l’algorithme précédent, mais cette fois-ci on ne connaît pas d’avance combien l’utilisateur souhaite saisir de nombres. La saisie des nombres s’arrête lorsque l’utilisateur entre un zéro.

## Correction

```
Variables
    valeur, compteur, max : entier
Instructions
    max ← 0
    valeur ← 0
    compteur ← 1

    Ecrire("Entrez le nombre numéro ", compteur, " : ")
    Lire(valeur)

    compteur ← compteur + 1

    Tant que valeur != 0 faire
        Ecrire("Entrez le nombre numéro ", compteur, " : ")
        Lire(valeur)
        Si max < valeur
            max ← valeur
        FinSi
        compteur ← compteur + 1
    FinTQ
    Ecrire("Le plus grand de ces nombres est ", max)
```

Version affichant également la position

```
Variables
    valeur, compteur, max, position : entier
Instructions
    max ← 0
    valeur ← 0
    compteur ← 1
    position ← 1

    Ecrire("Entrez le nombre numéro ", compteur, " : ")
    Lire(valeur)

    Tant que valeur != 0 faire
        compteur ← compteur + 1
        Ecrire("Entrez le nombre numéro ", compteur, " : ")
        Lire(valeur)
        Si max < valeur
            max ← valeur
            position ← compteur
        FinSi
    FinTQ
    Ecrire("Le plus grand de ces nombres est ", max)
```
