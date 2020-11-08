# Exercice 30

## Enoncé

Lire la suite des prix (en euros entiers et terminée par zéro) des achats d’un client. Calculer la somme qu’il doit, lire la somme qu’il paye, et simuler la remise de la monnaie en affichant les textes "10 Euros", "5 Euros" et "1 Euro" autant de fois qu’il y a de coupures de chaque sorte à rendre.

## Correction

```
Variables
    prix, somme, rendu : entier
Instructions
    prix ← 0
    somme ← 0
    rendu ← 0

    Ecrire("Donner un prix : ")
    Lire(prix)
    somme ← prix

    Tant que prix != 0 faire
        Ecrire("Donner un prix : ")
        Lire(prix)
        somme ← somme + prix
    FinTQ
    
    Ecrire("Vous devez payer ", somme, "€")
    Lire(rendu)

    Tant que rendu < somme faire
        Ecrire("Le montant inséré est insuffisant, veuillez rajouter de la monnaie.")
        Lire(prix)
        rendu ← rendu + prix
    FinTQ 

    rendu ← somme - rendu
    
    Tant que rendu > 0 faire
        Si rendu > 10 alors
            Ecrire("10€")
            rendu ← rendu - 10
        Sinon
            Si rendu > 5 alors
                Ecrire("5€")
                rendu ← rendu - 5
            Sinon
                Ecrire("1€")
                rendu ← rendu - 1
            FinSi
        FinSi
    FinTQ 
```
