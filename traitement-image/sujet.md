# Algorithmes pour le traitement des images

## 1. Introduction

Le but de cette section du cours va être d'apprendre à manipuler les tableaux à plusieurs dimensions par la pratique. En l'occurence, nous allons nous intéresser à des algorithmes permettant de modifier des images. Vous avez sans doute déjà utilisé de tels outils en cours de PAO. Voici quelques exemples des algorithme de filtres que nous allons réaliser :

### Version originale
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/original.jpg">
</p>

### Filtre rouge
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/rouge.jpg">
</p>

### Filtre vert
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/vert.jpg">
</p>

### Filtre bleu
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/bleu.jpg">
</p>

### Filtre niveau de gris
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/niveaux-gris.jpg">
</p>

### Filtre noir et blanc
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/noir-blanc.jpg">
</p>

### Symétrie axiale verticale
<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/symetrie.jpg">
</p>

## 2. Manipulation de grille

Commençons par une version plus simple de la manipulation d'image. Dans cette section, nous utiliserons une grille (un tableau à 2 dimensions) qui ne contient que deux couleurs : noir et blanc. Le noir est symbolisé par l'entier `0` et le blanc par l'entier `1`.

### 2.1. Déclaration de la grille

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

### 2.2. Accès à une case de la grille

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

### 2.3. Parcours de la grille

Généralisons l'accès d'une case à l'ensemble du tableau. L'exemple d'algorithme ci-dessous rempli la grille de case noire.

```
Algorithme ColorierEnNoir
Variable
    grille[10][5] : grille d'entiers
Instructions
    Pour i de 0 à 9 faire
        Pour j de 0 à 4 faire
            grille[i][j] ← 0
        FinPour
    FinPour
```

Il faut utiliser deux boucles : une pour se déplacer sur l'axe horizontal et une autre pour se séplacer sur l'axe vertical. La boucle avec l'itérateur `i` parcours les colonnes de la grille et la boucle avec l'itérateur `j` parcours les lignes de la grille.

Lorque l'on dispose d'une grille dont on ignore les dimensions, on peut les récupérer à l'aide de la fonction `Longueur`. En utilisant directement la variable en paramètre, on obtient la taille de la première dimension, soit le nombre de colonne. En utilisant la variable suivie d'un index de colonne valide, on obtient la taille de la deuxième dimension soit le nombre de ligne de cette colonne. Exemple :

```
colonnes ← Longueur(grille)
lignes ← Longueur(grille[0])
```

### 2.4. Exercice 1

Voici une représentation de Mr Monopoly :

<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/mr-monopoly.png">
</p>

#### Question 1

* Quelle est la couleur de la case de coordonnées (`8`,`13`) ?
* Quelle est la couleur de la case de coordonnées (`13`,`8`) ?

(Vous pouvez agrandir l'image en faisant clic droit -> Afficher l'image)

#### Question 2

Ecrire un sous-algorithme nommé `nombreCasesCouleur` qui prend en entrée une grille et affiche combien il y a de cases noires et de cases blanches dans cette grille.

#### Question 3

Ecrire un sous-algorithme intitulé `inverse` qui prend en entrée une grille et retourne une grille dont les couleurs ont été inversées. C'est-à-dire que les cases noires sont coloriées en blancs et les cases blanches sont coloriées en noir.

## 3. Structure d'une image

Une image est un tableau à trois dimensions. Comme pour la section ci-dessus, les deux premières dimensions représentent les colonnes et les lignes de la grille. Une case de cette grille est appelé `pixel` et est un tableau de taille trois où chaque case contient un entier entre 0 et 255 correspondant respectivement au rouge, vert et bleu.

<p align="center">
  <img width="600" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/grille3D.png">
</p>

En combinant les valeurs de rouge, vert et bleu de chaque pixel, on obtient la couleur affiché à l'écran.

### 3.1. Déclaration d'une image

Comme pour les autres types de tableaux, on peut déclarer les images de deux façons :

```
image[10][5][3]
```

```
image[][][]
```

Dans le deuxième cas, la déclaration de la taille des tableaux dans les instructions se fait ainsi :
```
image[][][] ← image[10][5][3]
```

### 3.2. Accès aux informations de l'image

L'accès à un pixel de la grille ce fait en utilisant `image[x][y]` où `x` correspond à l'index de colonne et `y` à l'index des lignes. 
`image[x][y]` est un tableau de trois cases.

<p align="center">
  <img width="450" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/pixel0-0.png">
</p>

Pour accéder à la composante rouge du pixel, il est necessire d'utiliser la troisième dimension : `image[x][y][0]` où `0` permet l'accès à la première couche du canal. L'accès à la composante verte se fait avec `image[x][y][1]` et l'accès à la composante bleue avec `image[x][y][2]`.

