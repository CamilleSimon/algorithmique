# Exercice 22

## Enoncé

Ecrire un algorithme qui demande un nombre compris entre `10` et `20`, jusqu’à ce que la réponse convienne. En cas de réponse supérieure à `20`, on fera apparaître un message: `"Plus petit !"`, et inversement, `"Plus grand !"` si le nombre est inférieur à `10`.

## Correction

```
Variables
    valeur : réel
Instructions
    Ecrire("Donner un nombre entre 10 et 20 (inclut) : ")
    Lire(valeur)
    Tant que valeur < 10 OU valeur > 20 faire
        Si valeur < 10 alors
            Ecrire("Plus grand !")
            Lire(valeur)
        Sinon
            Ecrire("Plus petit !")
            Lire(valeur)
        FinSi
    FinTQ
```
