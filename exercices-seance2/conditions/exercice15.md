# Exercice 15

## Enoncé

Ecrire un algorithme qui demande l’âge d’un enfant à l’utilisateur. Ensuite, il l’informe de sa catégorie : ​

* `Poussin` de 6 à 7 ans​
* `Pupille` de 8 à 9 ans​
* `Minime` de 10 à 11 ans​
* `Cadet` après 12 ans​

Peut-on concevoir plusieurs algorithmes équivalents menant à ce résultat ?

## Correction

```
Variables
    age : entier
Instructions
    Ecrire("Entrer l'âge de l'enfant :")
    Lire(age)
    Selon age alors
        Cas age = 6 OU age = 7 :
            Ecrire("Catégorie \"Poussin\" ")
        Cas age = 8 OU age = 9 :
            Ecrire("Catégorie \"Pupille\" ")
        Cas age = 10 OU age = 11 :
            Ecrire("Catégorie \"Minime\" ")
        Cas age >= 12 :
            Ecrire("Catégorie \"Cadet\" ")
    FinSelon
```

Oui, il est possible de faire une version alternative en utilisant des `si` imbriqués.
