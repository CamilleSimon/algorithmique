# Exercice 18

## Enoncé

Un magasin de reprographie facture 0,10 € l'unité les dix premières photocopies, 0,09 € les vingt suivantes et 0,08 € au-delà. Ecrivez un algorithme qui demande à l’utilisateur le nombre de photocopies à effectuées et qui affiche la facture correspondante.

## Correction

```
Variables
    nb : entier
    prix : réel
Instructions
    Ecrire("Entrer le nombre de photocopies :")
    Lire(nb)
    prix ← 0
    Si nb = 0 alors
        Ecrire("Vous devez payer : ", prix, "€")
    FinSi
    Si nb > 0 ET nb <= 10 alors
        prix ← 0.10 * nb
        Ecrire(Vous devez payer : ", prix, "€")
    FinSi
    Si nb > 10 ET nb <= 30 alors
        prix ← 0.10 * 10 + 0.09 * (nb - 10)
        Ecrire(Vous devez payer : ", prix, "€")
    FinSi
    Si nb > 30 alors
        prix ← 0.10 * 10 + 0.09 * 20 + 0.08 * (nb - 30)
        Ecrire(Vous devez payer : ", prix, "€")
    FinSi
```
