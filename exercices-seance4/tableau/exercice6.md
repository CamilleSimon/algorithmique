# Exercice 6

## Enoncé

Ecrire un algorithme qui inscrit des nombres entiers aléatoires entre -1 et 1 dans un tebleau de 50 cases.

Pour chaque valeur (-1, 0 et 1) l'algorithme affiche combien de fois le nombre est présent dans la plus longue occurence.

## Exemple

Pour le tableau suivant :

| 1 | 1 | 1 | -1 | 0 | -1 | -1 | -1 | -1 | 0 |
|---|---|---|---|---|---|---|---|---|---|

La plus longue suite de 1 est de longueur 3, la plus longue suite de 0 est de longueur 1 et la plus longue suite de -1 est de longueur 4.

## Correction

```
Variables
    tab[50] : tableau d'entiers
    valeur, compteur, un, zero, moinsUn : entiers
Instructions

    // Remplissage du tableau
    Pour i de 0 à 50 faire
        tab[i] ← AleatoireEntier(3) - 1
    FinPour
        
    // Partie traitement 
    un ← 0
    zero ← 0
    moinsUn ← 0
    compteur ← 1

    Pour i de 1 à 49 faire
        Si tab[i] = tab[i - 1]
            compteur ← compteur + 1
        Sinon 
            Selon tab[i - 1] faire
                Cas tab[i - 1] = -1 faire
                    moinsUn ← compteur
                Cas tab[i - 1] = 0 faire
                    zero ← compteur
                Cas tab[i - 1] = 1 faire
                    un ← compteur
            FinSelon
            compteur ← 0
        FinSi
    FinPour

    Ecrire("La suite la plus longue de -1 est de longueur ", moinsUn, ", la plus longue suite de 0 est de longueur ", zero, " et la plus longue suite de 1 est de longueur ", un)
```