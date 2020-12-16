# Exercice 2

## Enoncé

Ecrire un algorithme qui inscrit dans un tableau de taille 10 des nombres donnés par l’utilisateur puis teste si les nombres sont classés du plus petit au plus grand.

## Correction

```
Variables
    tableau[10] : tableau de réels
    valeur : réel
    trie : booléen
    iterateur : entier
Instructions

    // Remplissage du tableau
    Ecrire("Entrer les 10 nombres :")
    Pour i de 0 à 9 faire
        Lire(tableau[i])
    FinPour
        
    // Partie traitement des valeurs
    trie ← vrai // Variable qui sert à savoir si le contenu de la case suivante est plus grand que celui de la case courante
    iterateur ← 0 // Itérateur qui prend les valeurs des index du tableau
    Tant que trie = vrai ET iterateur < 8 faire // Tant que les cases précédentes sont triées et que l'itérateur n'a pas parcouru l'ensemble du tableau
        Si tableau[iterateur] > tableau[iterateur + 1] alors // Si le contenu de la case courante est plus grand que celui de la case suivante
            trie ← faux
        Sinon
            iterateur ← iterateur + 1
        FinSi
    FinTQ

    // Ici, il y a deux cas de figures : soit l'itérateur à parcouru l'ensemble du tableau soit trié est faux
    Si trie = faux alors
        Ecrire("Le tableau n'est pas trié")
    Sinon
        Ecrire("Le tableau est trié")
    FinSi
```