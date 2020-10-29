# Exercice 10

## Enoncé

Ecrire un programme qui lit le prix HT d’un article, le nombre d’articles et le taux de TVA, et qui fournit le prix total TTC correspondant. Faire en sorte que des libellés apparaissent clairement.

## Correction

```
Variables
    ht, tva, ttc : réels
    nb : entier
Instructions
    Ecrire("Entrer le nombre d'articles :")
    Lire(nb)
    Ecrire("Entrer le prix d'un article :")
    Lire(ht)
    Ecrire("Entrer la valeur de la TVA, ("5,5" par exemple pour une TVA à 5,5%))
    Lire(tva)
    ttc ← nb * (ht + (tva * ht) / 100)
    Ecrire("Le prix toutes taxes est : ", ttc)
```
