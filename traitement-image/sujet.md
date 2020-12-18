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

Dans la section variables, la déclaration d'une grille peut se faire de deux façons. 

La première lorsque l'on connait déjà la taille de la grille :

```
grille[10][5] : tableau d'entiers
```

La seconde lorsqu'il s'agit d'une grille de taille non définie :

```
grille[][] : tableau d'entiers
```

L'affectation de la taille de la grille dans les instructions se fait ainsi :

```
grille[][] ← grille[10][5] 
```

Le contenu de la première paire de crochets correspond au nombre de colonnes de la grille et le contenu de la deuxième paire de crochets correspond au nombre de lignes de la grille.

<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/grille2D.png">
</p>

### 2.2. Accès à une case de la grille

L'accès à une case de la grille ce fait en utilisant `grille[x][y]` où `x` correspond à l'index des colonnes et `y` à l'index des lignes. 

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

Il faut utiliser deux boucles : une pour se déplacer sur l'axe horizontal et une autre pour se déplacer sur l'axe vertical. La boucle avec l'itérateur `i` parcours les colonnes de la grille et la boucle avec l'itérateur `j` parcours les lignes de la grille.

Lorque l'on dispose d'une grille dont on ignore les dimensions, on peut les récupérer à l'aide de la fonction `Longueur()`. En utilisant directement la variable en paramètre, on obtient la taille de la première dimension, soit le nombre de colonnes. En utilisant la variable suivie d'un index de colonne valide, on obtient la taille de la deuxième dimension soit le nombre de lignes de cette colonne. Exemple :

```
colonnes ← Longueur(grille)
lignes ← Longueur(grille[0])
```

### 2.4. Exercice 1

#### Question 1

Voici une représentation de Mr Monopoly :

<p align="center">
  <img width="460" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/mr-monopoly.png">
</p>

* Quelle est la couleur de la case de coordonnées (`8`,`13`) ?
* Quelle est la couleur de la case de coordonnées (`13`,`8`) ?

(Vous pouvez agrandir l'image en faisant clic droit -> Afficher l'image)

#### Question 2

Ecrire un sous-algorithme nommé `NombreCasesCouleur` qui prend en entrée une grille et affiche combien il y a de cases noires et de cases blanches dans cette grille.

#### Question 3

Ecrire un sous-algorithme intitulé `Inverse` qui prend en entrée une grille et retourne une grille dont les couleurs ont été inversées. C'est-à-dire que les cases noires sont coloriées en blanc et les cases blanches sont coloriées en noir.

## 3. Structure d'une image

Une image est un tableau à trois dimensions. Comme pour la section ci-dessus, les deux premières dimensions représentent les colonnes et les lignes de la grille. Une case de cette grille est appelé `pixel` et est un tableau de taille trois où chaque case contient un entier entre 0 et 255 correspondant respectivement au rouge, vert et bleu.

<p align="center">
  <img width="800" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/grille3D.png">
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

<p align="center">
  <img width="800" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/grille3Dpixels.png">
</p>

### 3.3. Filtre de couleur

Un filtre de couleur permet de ne voir qu'un canal précis de l'image, les autres canaux de l'image sont rempli avec des `0`. Voici le sous-algorithme permettant, à partir d'une image, de ne filtrer que le rouge.

```
Sous-algorithme FiltreRouge
Paramètre d'entrée
    image[][][] : tableau d'entiers
Paramètre de sortie
    rouge[][][] : tableau d'entiers
Variables
    colonnes, lignes : entiers
Instructions
    colonnes ← Longueur(image)
    lignes ← Longueur(image[0])

    rouge[][][] ← rouge[colonnes][lignes][3] // La troisième dimension est obligatoire de taille 3, c'est la particularité des images

    Pour i de 0 à colonnes - 1 faire
        Pour j de 0 à colonnes - 1 faire
            rouge[i][j][0] ← image[i][j][0]
            rouge[i][j][1] ← 0
            rouge[i][j][2] ← 0
    FinPour
```

### 3.4. Exercice 2

#### Question 1 - Filtre bleu et vert

En utilisant le modèle ci-dessus, réaliser un sous-algorithme qui filtre le bleu et un sous-algorithme qui filtre le vert.

**Exemple**

<p align="center">
  <img width="800" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/exercice2q1.jpg">
</p>

#### Question 2 - Symétrique

Ecrire un sous-algorithme qui à pour paramètre d'entrée une image et qui retourne le symétrique vertical de cette image.

**Exemple**

<p align="center">
  <img width="800" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/exercice2q2.jpg">
</p>

### 3.5. Niveaux de gris et noir/blanc

Pour obtenir le niveau de gris d'un pixel coloré, on fait la moyenne de ses composantes. Ce niveau de gris est ensuite affecté à l'ensemble des composantes du pixel.

<p align="center">
  <img width="1000" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/processus-niveau-gris.png">
</p>

<p align="center">
  <img width="1000" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/conversion-niveaux-gris.png">
</p>

### 3.6. Exercice 3

#### Question 1 - Niveau de gris

Écrire un sous-algorithme qui a pour paramètre d'entrée une image et qui retourne une nouvelle version en niveaux de gris.

**Exemple**

<p align="center">
  <img width="800" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/exercice2q3.jpg">
</p>

#### Question 2 - Noir et blanc

Écrire un sous-algorithme qui a pour paramètres d'entrée une image en niveau de gris et un réel. Ce sous-algorithme retourne une nouvelle version de l'image en noir et blanc où tous les pixels plus petit que le seuil sont coloriés en noir et tous les pixels plus grand que le seuil sont colorés en blanc.

**Exemple**

<p align="center">
  <img width="800" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/exercice2q4.jpg">
</p>

### 3.7. Modification de contours

On entre dans la partie la plus difficile de ce devoir maison. Pour effectuer les traitements suivants, il est nécessaire de travailler à partir d'une image en niveaux de gris.

La modification de contour se fait en augmentant ou en diminuant le contraste d'un pixel par rapport à ces voisins. Le "poids" des voisins dans le nouveau calcul de la couleur du pixel est donné par un tableau à deux dimensions appelé matrice de convolution. Voici un exemple :

<p align="center">
  <img width="800" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/calcul-contraste.png">
</p>

On veut calculer la nouvelle couleur du pixel entouré en rouge. Les voisins de ce pixel sont entourés en vert.
La nouvelle couleur du pixel central est la somme de chaque voisin multiplié par la matrice de convolution. La matrice de convolution est un tableau de trois par trois qui, en fonction des valeurs qu'elle contient, va permettre de faire apparaitre ou flouter les contours des objets présents dans l'image. Pour l'exemple ci-dessus, on multiplie les valeurs de gris par le nombre présent dans la matrice de convolution à la même place puis on les ajoute ensemble, ce qui donne : `1 * 170 + 1 * 170 + 1 * 119 + 1 * 170 + 0 * 170 + 1 * 119 + 1 * 119 + 1 * 119 + 1 * 119`.

Si cette nouvelle valeur est supérieure à `255` alors la nouvelle couleur du pixel est `255`, de même si la valeur est inférieure à `0` alors la nouvelle couleur du pixel est `0`. Il ne faudra pas oublier d'affecter cette valeur à tous les canaux.

### 3.8. Exercice 4

Écrire un sous-algorithme qui a pour paramètres d'entrée une image ainsi qu'une matrice de convolution et qui retourne la nouvelle d'image après application de la matrice. Vous veillerez à effectuer toutes les vérifications nécessaires et traiterez les exceptions comme vous le souhaitez.

**Exemple**

<p align="center">
  <img width="800" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/exercice4.jpg">
</p>

### 3.9. Pixellisation d'une image

Le but de ce traitement est de diviser une image en carré de `n` pixels de côté. On effectue ensuite la moyenne de chacun des canaux des `n²` pixels pour obtenir l'image pixellisée.

Ici, la seul pixellisation possible est avec des carrés de 5 cases.

<p align="center">
  <img width="800" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/pixellisation.png">
</p>

### 3.10. Exercice 5

Écrire un sous-algorithme qui a pour paramètres d'entrée une image et qui retourne l'ensemble des pixellisations possibles. Vous veillerez à effectuer toutes les vérifications nécessaires et traiterez les exceptions comme vous le souhaitez.

**Exemple**

<p align="center">
  <img width="800" src="https://github.com/CamilleSimon/algorithmique/blob/main/traitement-image/exercice5.jpg">
</p>