# Evaluation n°8 - 4 janvier 2021 - Le chiffrement de César 

## Enoncé

Le but de cette exercice est de réaliser deux sous-algorithmes qui reproduisent le chiffrement et le déchiffrement d'un message en utilisant la méthode de César.
Le chiffrement de César est un procédé cryptographique qui permet de coder un message. Chaque lettre de la chaîne de caractères formant le message est remplacée par une autre. La **clé** est un nombre entier entre 1 et 25 qui indique le décalage de l'alphabet nécessaire pour chiffrer ou déchiffrer le message.

Pour chiffrer un message, chaque lettre est remplacée par la nième lettre qui la suit dans l'alphabet. Par exemple pour une clé de 6 : `a` devient `g`, `b` devient `h`, `c` devient `i` et ainsi de suite jusqu'à `z` qui devient `f`.

![Illustration chiffrement de César](https://github.com/CamilleSimon/algorithmique/blob/main/evaluations/letters-wheel.png))]

Le message `bonjour` avec une clé de `6` devient alors le message chiffré : `hurpuax`

Pour déchiffrer un message, on opère de façon inverse, chaque caractère du message est remplacé par le nième caractère précédent dans l'alphabet. Par exemple, avec une clé de 8 et le message chiffré suivant : `qtvmqom` après déchiffrage on obtient `ilneige`.

Pour qu'un message soit valide, il ne doit contenir ni espace ni majuscule.

NB : il n'est pas possible d'utiliser d'opérations arithmétiques sur les caractères (+, -, ...). Ainsi, `a + 4` génèrera une erreur.

### Question

Ecrire deux sous-algorithmes permettant de reproduire le chiffrement de César.

1. Le premier sous-algorithme prendra en paramètres d'entrées un message à coder et une clé. Il retournera le message chiffré.  
2. Le deuxième sous-algorithme prendra en entrées un message chiffré et une clé. Il retournera le message déchiffré.

Dans les deux cas, on suppose que les chaînes de caractères des paramètres d'entrées sont uniquement constituées de caractères en minuscule, sans espace ou caractères spéciaux. Vous veillerez à effectuer toutes les vérifications nécessaires.
