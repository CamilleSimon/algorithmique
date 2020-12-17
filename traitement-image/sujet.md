# Algorithmes pour le traitement des images

## Introduction

Le but de cette section du cours va être d'apprendre à manipuler les tableaux à plusieurs dimensions par la pratique. En l'occurence, nous allons nous intéresser à des algorithmes permettant de modifier des images. Vous avez sans doute déjà utilisé de tels outils en cours de PAO. Voici quelques exemples des algorithme de filtres que nous allons réaliser :

## Version originale
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/original.jpg">
</p>

## Filtre rouge
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/rouge.jpg">
</p>

## Filtre vert
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/vert.jpg">
</p>

## Filtre bleu
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/bleu.jpg">
</p>

## Filtre niveau de gris
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/niveaux-gris.jpg">
</p>

## Filtre noir et blanc
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/noir-blanc.jpg">
</p>

## Symétrie axiale verticale
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/symetrie.jpg">
</p>

## Manipulation de grille

Commençons par une version plus simple de la manipulation d'image. Dans cette section, nous utiliserons une grille (un tableau à 2 dimensions) qui ne contient que deux couleurs : noir et blanc. Le noir est symbolisé par l'entier `0` et le blanc par l'entier `1`.

### Déclaration de la grille

La déclaration, dans la section variable, d'une grille peut se faire de deux façons. La première lorsque l'on connait déjà la taille de la grille et la seconde lorsqu'elle sera transmise dans les instructions :

```
grille[10][5] : tableau d'entiers
```

```
grille[][] : tableau d'entiers
```

L'affectation de la taille de la grille dans les instructions se fait ainsi :

```
grille[][] ← grille[10][5] 
```

Le contenu de la première paire de crochet correspond aux nombre de colonnes de la grille et le contenu de la deuxième paire de crochet correspond au nombre de ligne de la grille.

<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/grille2D.png">
</p>

### Accès à une case de la grille

L'accès à une case de la grille ce fait en utilisant `grille[x][y]` où `x` correspond à l'index de colonne et `y` à l'index des lignes. 

<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/grille2D-coordonnees.png">
</p>

Dans les instructions, on utilise l'accès à une case ainsi :

```
case ← grille[4][2]
grille[6][0] ← 0
```

Le contenu de la case de coordonnée (`4`,`2`) est copié dans la variable `case`.
Le contenu de la case de coordonnée (`6`,`0`) est changé à `0`.

### Parcours de la grille

Généralisons l'accès d'une case à l'ensemble du tableau. L'exemple d'algorithme ci-dessous rempli la grille de case noire.

```
Variable
    grille[10][5] : grille d'entiers
Instructions
    Pour i de 0 à 9 faire
        Pour j de 0 à 4 faire
            grille[i][j] ← 0
        FinPour
    FinPour
```

Il faut utiliser deux boucles : une pour se déplacer sur l'axe horizontal et une autre pour se séplacer sur l'axe vertical. La boucle avec l'itérateur `i` parcours les colonnes de la grille et la boucle avec l'itérateur `parcours` les lignes de la grille.

### Exercice 1

Voici une représentation de Mr Monopoly :

<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/mr-monopoly.png">
</p>

#### Question 1

* Quelle est la couleur de la case de coordonnées (`8`,`13`) ?
* Quelle est la couleur de la case de coordonnées (`13`,`8`) ?

#### Question 2

Ecrire un sous-algorithme qui prend en entrée une grille et affiche combien il y a de cases noires et de cases blanches dans cette grille.

#### Question 3

Ecrire un sous-algorithme qui prend en entrée une grille et retourne une grille dont les couleurs ont été inversées. C'est-à-dire que les cases noires sont coloriées en blancs et les cases blanches sont colorées en noir.

## Structure d'une image

Une image est une grille de pixel. Chaque pixel est un tableau de taille trois où chaque case contient un entier entre 0 et 255 correspondant respectivement au rouge, vert et bleu.


