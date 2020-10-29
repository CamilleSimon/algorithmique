# Exercice 12

## Enoncé

Ecrire un algorithme qui demande deux nombres à l’utilisateur et l’informe ensuite si leur produit est négatif ou positif (on laisse de côté le cas où le produit est nul). Attention toutefois : **on ne doit pas calculer le produit des deux nombres**.

## Correction

```
Variables
    val1, val2 : réels
Instructions
    Ecrire("Entrer un premier nombre :")
    Lire(val1)
    Ecrire("Entrer un deuxième nombre :")
    Lire(val2)
    Si (val1 > 0 ET val2 > 0) OU (val1 < 0 ET val2 < 0) alors
        Ecrire("Le produit des nombres est positif")
    Sinon
        Ecrire("Le produit des nombres est négatif")
    FinSi
```

On peut également écrire une version alternative en testant dans la condition si le produit est négatif cela donne :

```
Si (val1 > 0 ET val2 < 0) OU (val1 < 0 ET val2 > 0) alors
    Ecrire("Le produit des nombres est négatif")
Sinon
    Ecrire("Le produit des nombres est positif")
FinSi
```
