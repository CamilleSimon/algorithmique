# Exercice 14

## Enoncé

​​​Ecrire un algorithme qui demande deux nombres à l’utilisateur et l’informe ensuite si le produit est négatif ou positif (on inclut cette fois le traitement du cas où le produit peut être nul). **Attention toutefois, on ne doit pas calculer le produit !**

## Correction

```
Variables
    val1, val2 : réel
Instructions
    Ecrire("Entrer un premier nombre :")
    Lire(val1)
    Ecrire("Entrer un deuxième nombre :")
    Lire(val2)
    Si val1 = 0 OU val2 = 0 alors
        Ecrire("Le produit des nombres est nul")
    Sinon
        Si (val1 > 0 ET val2 > 0) OU (val1 < 0 ET val2 < 0) alors
            Ecrire("Le produit des nombres est positif")
        Sinon
            Ecrire("Le produit des nombres est négatif")
        FinSi
    FinSi
```
