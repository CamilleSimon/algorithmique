# Exercice 3

## Enoncé

Ecrire un algorithme qui inscrit 10 entiers donnés par l’utilisateur puis donne le nombre d’occurrence de chaque nombre.

## Correction

```
Variables
    tab[10] : Tableau d'entiers
    valeur, iterateur, compteur : entier
    pasTrouveValeur : booléen
Instructions
    Pour i de 0 à 9 faire
        Ecrire("Donner la valeur de la case", i)
        Lire(tab[i])
    FinPour

    // Paroucr des cases du tableau
    Pour i de 0 à 9 faire
        valeur ← tab[i]

        //Recherche de la valeur dans les cases précédentes (par rapport à i)
        pasTrouveValeur ← vrai
        Si i != 0 alors 
            iterateur ← i - 1
            Tantque pasTrouveValeur ET iterateur != 0 faire
                Si tab[iterateur] = valeur alors
                    pasTrouveValeur ← faux
                Sinon
                    iterateur ← iterateur - 1
                FinSi
            FinTQ
        FinSi

        //Recherche de la valeur dans la suite du tableau (par rapport à i) si c'est la première fois que l'on rencontre cette valeur
        Si pasTrouveValeur alors // Si on a pas trouver la valeur dans les cases précédentes
            compteur ← 1
            Pour j de i + 1 à 9 faire // Parcours des cases suivantes
                Si tab[j] = tab[i] alors // Si on a la même dans les deux cases, on a trouvé à nouveau la valeur
                    compteur ← compteur + 1
                FinSi
            FinPour
            Ecrire("La valeur : ", valeur, " est présente ", compteur, " fois dans le tableau")
        FinSi
    FinPour
```