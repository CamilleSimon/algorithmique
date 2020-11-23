# Exercices de logique - Séquences

Ces exercices sont inspirés du site [Brillant.org](https://brilliant.org/daily-problems/)

## Carrés

Soit une séquence évoluant de la façon suivante :

![Séquence de carrés](https://github.com/CamilleSimon/algorithmique/blob/main/exercices-supplementaires/carres.png)

Ecrire un algorithme demandant à l'utilisateur un numéro d'étape et qui retourne le nombre de carrés à cette étape.

## Etoiles et carrés

Soit la séquence de carrés et d'étoiles suivante :

![Séquence de carrés et d'étoiles](https://github.com/CamilleSimon/algorithmique/blob/main/exercices-supplementaires/etoilescarres.png)

Ecrire un algorithme qui demande à l'utilisateur un numéro de colonne et qui retoune `étoile` si la colonne comporte plus d'étoiles et `carré` si la colonne comporte plus de carrés. 

## Grille

Soit un grille évoluant de la façon ci-dessous, chaque figure correspond à une étape, figure 1 => étape 1, figure 2 => étape 2, et ainsi de suite.

![Grille](https://github.com/CamilleSimon/algorithmique/blob/main/exercices-supplementaires/grille.png)

Ecrire un algorithme qui demande à l'utilisateur un numéro d'étape et qui retourne le nombre de `cases vide` de la grille.

## Pyramide

Soit une pyramide construite de la façon suivante :
- Le première étage a un bloc
- Le deuxième étage a trois blocs
- Le troisième étage a 6 blocs

![Pyramide](https://github.com/CamilleSimon/algorithmique/blob/main/exercices-supplementaires/cubes.png)

Ecrire un algorithme qui demande à l'utilisateur un valeur d'étage et qui retourne combien de blocs la pyramide possède.
Exemple d'exécution :

```
Donner un étage :
3
La pyramide comporte 10 blocs.
```

## Tables

On souhaite placer des tables pour une fête. Les tables sont collées les unes aux autres et placées sous forme d'une ligne. Sur chaque côté d'une table ne peut s'assoire d'une seule personne. Une personne ne peut pas s'assoire sur un côté collé à une autre table.
L'illustration ci-dessous représente les différentes lignes de tables possibles.

![Table](https://github.com/CamilleSimon/algorithmique/blob/main/exercices-supplementaires/tables.png)

Ecrire un algorithme qui demande à l'utilisateur un nombre d'invités et qui retourne la forme et le nombre de tables nécessaire pour faire assoire les invités.
Attention, les seuls agencement de tables valides sont ceux où il ne reste pas de place vide, tous les côté sont occupés.

Notes : les forme des tables sont de haut en bas : carrée, pentagone, héxagone, heptagone, octogone. 