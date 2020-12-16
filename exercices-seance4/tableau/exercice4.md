# Exercice 4

## Enoncé

Ecrire un algorithme qui fait la somme des contenus de deux tableaux de la façon suivante:

Tableau 1 :

| 5 | 2 | 6 | 1 | 8 |
|---|---|---|---|---|

Tableau 2 :

| 3 | 7 | 1 | 4 | 2 |
|---|---|---|---|---|

Tableau à afficher :

| 8 | 9 | 7 | 5 | 10 |
|---|---|---|---|---|

La taille et le contenu des tableaux sont définis par l’utilisateur. 

## Correction

```
Variables
    tailleTab : entier
    tab1[], tab2[] : tableau de réels
    valeur : réel
Instructions
    tailleTab ← 0 // Initialisation de la taille du tableau volontairement avec un nombre invalide

    Tant que tailleTab <= 0 faire // Tant que la taille du tableau n'est pas valide, l'algo continue de demander une valeur à l'utilisateur
        Ecrire("Quel est la taille des tableaux ?")
        Lire(tailleTab)
    FinTQ

    // Initalisation des tableaux
    tab1[] ← tab1[tailleTab]
    tab2[] ← tab2[tailleTab]

    // Remplissage des tableaux
    Ecrire("Entrer les ", tailleTab, " valeurs du premier tableau :")
    Pour i de 0 à tailleTab - 1 faire
        Lire(tab1[i])
    FinPour

    Ecrire("Entrer les ", tailleTab, " valeurs du deuxième tableau :")
    Pour i de 0 à tailleTab - 1 faire
        Lire(tab2[i])
    FinPour
        
    // Partie traitement 
    Pour i de 0 à tailleTab - 1 faire
        tab2[i] ← tab1[i] + tab[2]
    FinPour

    // Affichage du tableau
    // Attention Ecrire(tab2) n'affiche que le contenu de la première case, pas de l'ensemble du tableau
    Ecrire("La somme des tableaux est le t baleau suivant : ")
    Pour i de 0 à tailleTab - 1 faire
        Ecrire(tab[2], " ")
    FinPour
```