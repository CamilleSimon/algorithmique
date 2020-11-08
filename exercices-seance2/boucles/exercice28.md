# Exercice 28

## Enoncé

Ecrire un algorithme qui demande successivement 20 nombres à l’utilisateur, et qui lui dise ensuite quel était le plus grand parmi ces 20 nombres:

```
Entrez le nombre numéro 1 : 
12
Entrez le nombre numéro 2 : 
14
...
Entrez le nombre numéro 20 : 
6
Le plus grand de ces nombres est: 14
```

Réaliser une deuxième version pour que l'algorithme affiche également en quelle position avait été saisie ce nombre. Exemple :

`C'était le nombre numéro 2`

## Correction

```
Variables
    valeur, max : entier
Instructions
    max ← 0
    Pour compteur de 1 à 20 faire
        Ecrire("Entrez le nombre numéro ", compteur, " : ")
        Lire(valeur)
        Si max < valeur
            max ← valeur
        FinSi
    FinPour
    Ecrire("Le plus grand de ces nombres est ", max)
```

Deuxième version :

```
Variables
    valeur, max, position : entier
Instructions
    max ← 0
    position ← 1
    Pour compteur de 1 à 20 faire
        Ecrire("Entrez le nombre numéro ", compteur, " : ")
        Lire(valeur)
        Si max < valeur
            max ← valeur
            position ← compteur
        FinSi
    FinPour
    Ecrire("Le plus grand de ces nombres est ", max)
    Ecrire("C'était le numéro : ", position)
```
