# Exercice 20

## Enoncé

Ecrivez un algorithme qui après avoir demandé un numéro de jour, de mois et d'année à l'utilisateur, renvoie s'il s'agit ou non d'une date valide.​

Cet exercice est certes d’un manque d’originalité affligeant, mais après tout, en algorithmique comme ailleurs, il faut connaître ses classiques ! Et quand on a fait cela une fois dans sa vie, on apprécie pleinement l’existence d’un type numérique « date » dans certains langages…).​

Il n'est sans doute pas inutile de rappeler rapidement que le mois de février compte 28 jours, sauf si l’année est bissextile, auquel cas il en compte 29. L’année est bissextile si elle est divisible par quatre. Toutefois, les années divisibles par 100 ne sont pas bissextiles, mais les années divisibles par 400 le sont. Ouf !

## Correction

```
Variables
    j, m, a : entiers
Instructions
    Ecrire("Entrer une année")
    Lire(a)
    Ecrire("Entrer un mois")
    Lire(m)
    Ecrire("Entrer un jour")
    Lire(j)

    Si m < 1 OU m > 12 alors
        Ecrire("La date est invalide")
    FinSI

    Si (m = 1 OU m = 3 OU m = 5 OU m = 7 OU m = 8 OU m = 10 OU m = 12) alors
        Si j > 0 ET j <= 31 alors
            Ecrire("La date est valide")
        Sinon
            Ecrire("La date est invalide")
        FinSi
    FinSi
    Si (m = 4 OU m = 6 OU m = 9 OU m = 11) alors
        Si j > 0 ET j <= 30 alors
            Ecrire("La date est valide")
        Sinon
            Ecrire("La date est invalide")
        FinSi
    FinSi
    Si m = 2 alors
        Si (a % 400 = 0 OU (a % 4 = 0 ET a % 100 != 0)) ET (j > 0 ET j <= 28) alors
            Ecrire("La date est valide")
        Sinon
            Ecrire("La date est invalide")
        FinSI
    FinSi
```
