# Exercice 7

## Enoncé 

Ecrire une fonction qui prend en entrée une chaîne de caractère et retourne cette chaîne avec un décalage à gauche. 

Trouver deux solutions à cet exercice.

## Exemple

Phrase donnée au sous-algorithme : “Aujourd’hui il ne fait pas beau”

Retour du sous-algorithme : “ujourd’hui il ne fait pas beauA”

```
Sous-algorithme DecalageGaucheMethodeCopieTableau

Paramètres d’entrée :
    phrase[] : tableau de caractères
Paramètres de sortie :
    decalageAGauche[] : tableau de caractères

Instructions
    // Initialisation du tableau contenant le résultat
    decalageAGauche[] ← decalageAGauche[Longueur(phrase)]

    // Remplissage des cases du tbaleau contenant le résultat à l'exception de la dernière case
    Pour i de 0 à Longueur(phrase) - 2 faire
        decalageAGauche[i] ← phrase[i + 1]
    FinPour

    // Ajout du premier caractère de phrase au tableau de décalage
    decalageAGauche[Longueur(phrase) - 1] ← tab1[0]
    // Renvoie automatique de decalageAGauche à la fin du sous algo
```

```
Sous-algorithme DecalageGaucheMethodeCopieCaractere

Paramètres d’entrée :
    phrase[] : tableau de caractères
Paramètres de sortie :
    phrase[] : tableau de caractères

Variables
    c : caractere
Instructions
    c ← phrase[0]

    Pour i de 0 à Longueur(phrase) - 2 faire
        phrase[i] ← phrase[i + 1]
    FinPour

    phrase[Longueur(phrase) - 1] ← c
```