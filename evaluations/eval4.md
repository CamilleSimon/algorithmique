# Evaluation n°4

## Question de cours

Question 1 : Dans quel cas privilégie-t-on une boucle `Pour` ?

Question 2 : La fonction `AléatoireReel()` retourne un nombre compris entre 0 et 1 exclut, on écrit également cet intervalle `[0; 1[`. L'algorithme ci-dessous à pour but de retourner un réel entre deux valeurs données par l'utilisateur, malheureusement il est incomplet.
Remplacer la ligne qui contient `//` pour que l'algorithme retourne une valeur dans l'intervalle `[debut; fin[`.
```
    Variable
        debut, fin, valeur : réels
    Instructions
        Ecrire("Donner la valeur minimum :")
        Lire(debut)
        Ecrire("Donner la valeur maximum :")
        Lire(fin)
        // Remplacer cette ligne
        Ecrire("Un nombre aléatoire entre ", debut, " et ", fin, " : ", valeur)
```

## Exercice de logique

# Enoncé

Les jeux de Nim sont des jeux très courants qui existent en plusieurs variantes. Nous nous intéresserons à une version simple pour laquelle il existe une stratégie gagnante. Le jeu se joue à deux, chacun son tour. A chaque tour le joueur prend des billes d’un tas. Il décide combien de billes il va prendre, mais il est obligé d’en prendre au moins une et il a droit de prendre au plus la moitié des billes du tas. Celui qui prend la dernière bille perd le jeu. Ecrire un programme qui joue contre l’utilisateur. Le nombre de billes de départ est un nombre aléatoire
entre `10` et `100`. Un autre nombre aléatoire détermine qui joue en premier. L’utilisateur a le droit de choisir le mode de jeu de l’ordinateur : `malin` ou `crétin`. En mode crétin l’ordinateur prend un nombre aléatoire de billes entre 1 et la moitié des billes dans le tas. En mode malin l’ordinateur choisit le nombre de billes à prendre de telle façon que le nombre de billes restantes soit un nombre de type `2^n − 1` (c’est à dire 1, 3, 7, 15, 31 ou 63). C’est toujours possible sauf dans le cas où le nombre des billes dans le tas est déjà de type `2^n − 1`. Dans ce dernier cas l’ordinateur joue comme en mode crétin. Vous verrez qu’on ne peut pas battre l’ordinateur en mode malin s’il commence le jeu et si le nombre de billes de départ n’est pas 15, 31 ou 63. Bien sûr, sous les mêmes conditions un humain qui applique la stratégie gagnante battra l’ordinateur.

N'hésitez pas à ajouter des commentaires dans votre code. Les commentaires doivent être précédés de `//`.