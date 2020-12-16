# Exercice 5

## Enoncé

Ecrire un algorithme qui inscrit des nombres entiers aléatoires compris entre 1 et 20 dans un tableau de 10 cases puis y recherche un nombre entrée par l’utilisateur. Si le nombre n’est pas trouvé, l’algorithme affiche une erreur.

## Correction

```
Variables
    tab[10] : tableau d'entiers
    valeur, iterateur : entier
    trouve : booléen
Instructions

    // Remplissage du tableau
    Pour i de 0 à 9 faire
        tab[i] ← AleatoireEntier(20) + 1
    FinPour

    Ecrire("Donner la valeur à chercher :")
    Lire(valeur)
        
    // Partie traitement 
    trouve ← faux
    iterateur ← 0
    Tant que trouve = faux ET iterateur < 10
        Si tab[iterateur] = valeur alors
            trouve ← vrai
        Sinon
            iterateur ← iterateur + 1
        FinSi
    FinTQ

    Si trouve alors
        Ecrire("La valeur  été trouvée, elle en position : ", iterateur)
    Sinon
        Ecrire("La valeur n'a pas été trouvée")
```

Version alternative :

```
Variables :
    size : entier
    tableau[] : Tableau d'entiers
    number : entier
    occurence : booleen
    
Instructions :
    // Partie Entrées
    
    Ecrire("Entrez une valeur à rechercher (Entre 1 et 20) : ")
    Lire(number)
    
    // Partie Calculs
    
    size ← 10
    occurence ← faux
    tableau[] ← tableau[size]
    
    Pour i de 0 à (size-1) faire
    
        tableau[i] ← AléatoireEntier(20) + 1
    
    FinPour
    
    Pour i de 0 à (size-1) faire
    
        Si ( tableau[i] = number ) alors
            
            occurence ← vrai
            
        FinSi
    
    FinPour
    
    Si ( occurence ) alors
    
        Ecrire("Il y a une occurence dans le tableau.")
        
    Sinon
    
        Ecrire("Erreur, il n'y a pas d'occurence dans le tableau.")
    FinSi
```