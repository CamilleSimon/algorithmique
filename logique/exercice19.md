# Exercice 19

## Enoncé

Les élections législatives, en Guignolerie Septentrionale, obéissent à la règle suivante :

* lorsque l'un des candidats obtient plus de 50 % des suffrages, il est élu dès le premier tour.​
* en cas de deuxième tour, peuvent participer uniquement les candidats ayant obtenu au moins 12,5% des voix au premier tour.​

Vous devez écrire un algorithme qui permette la saisie des scores de quatre candidats au premier tour. Cet algorithme traitera ensuite le candidat numéro 1 (et uniquement lui) : il dira s'il est élu, battu, s'il se trouve en ballottage favorable (il participe au second tour en étant arrivé en tête à l'issue du premier tour) ou défavorable (il participe au second tour sans avoir été en tête au premier tour).​

## Correction

```
Variables
    c1, c2, c3, c4 : réels
Instructions
    Ecrire("Entrer les résultats du premier candidat :")
    Lire(c1)
    Ecrire("Entrer les résultats du deuxième candidat :")
    Lire(c2)
    Ecrire("Entrer les résultats du troisième candidat :")
    Lire(c3)
    Ecrire("Entrer les résultats du quatrième candidat :")
    Lire(c4)
    Si c1 < 12,5  OU c2 > 50 OU c3 > 50 OU c4 > 50  alors
        Ecrire("Le premier candidat est battu")
    FinSI
    Si c1 > 50 alors
        Ecrire("Le premier candidat est élu")
    FinSi
    Si c1 <= 50 ET c1 >= 12,5 ET c1 > c2 ET c1 > c3 ET c1 > c4 alors
        Ecrire("Le premier candidat est au second tour et en ballotage favorable")
    Sinon
        Ecrire("Le premier candidat est au second tour et en ballotage défavorable")
```
