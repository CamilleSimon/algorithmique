# Exercice supplémentaire 1

## Enoncé

Ecrire un programme qui demande à l’utilisateur une distance en mètres et transforme cette distance en pieds et pouces (1 pouce = 2,54 cm, 1 pied = 12 pouces = 30,48 cm). 
Donner les pieds et les pouces en nombres entiers. Arrondir vers la valeur la plus proche, on peut utiliser la fonction `Arrondir()` qui retourne l'arondi de la valeur entre les parenthèses. 

## Exemple d’exécution

```
Donner une distance en mètres : 1,81
1,81 m = 5 pieds et 11 pouces
```

## Correction

```
Variables
    pouces, pieds : entiers
    taille : réel
Instructions
    Ecrire("Donner une valeur en mètres : ")
    Lire(taille * 100)

    pouces ← 0
    pieds ← 0

    Tant que taille >= 2,54 faire
        pouces ← pouces + 1
        Si pouces = 12 alors
            pouces ← 0
            pieds ← pieds + 1
        FinSi
    FinTQ

    Si taille >= (2,54 / 2) alors
        pouces ← pouces + 1
        Si pouces = 12 alors
            pouces ← 0
            pieds ← pieds + 1
        FinSi
    FinSi
```

Version alternative

```
Variable :
    resultat, pied, pouce : entiers
    distance, pouce,  : réel
Instructions :
    Ecrire("une distance en metres")
    Lire(distance)
    distance ← distance * 100
    pied ← E(distance, 30.48)
    pouce ← Arrondir((distance % 30.48) / 2.54)

    Si pouce = 12 alors
        pouce ← 0
        pied ← pied + 1
    FinSi
    
    Ecrire(distance / 100, "m = ", pied, " pieds et ", pouce, " pouces")
```