# Exercice 17

## Enoncé

De même que le précédent, cet algorithme doit demander une heure et en afficher une autre. Mais cette fois, il doit gérer également les secondes, et afficher l'heure qu'il sera une seconde plus tard.​
Par exemple, si l'utilisateur tape `21`, puis `32`, puis `8`, l'algorithme doit répondre :

```Dans une seconde, il sera 21 heure(s), 32 minute(s) et 9 seconde(s)".​```

NB : là encore, on suppose que l'utilisateur entre une date valide.

## Correction

```
Variables
    h, m, s : entiers
Instructions
    Ecrire("Entrer l'heure :")
    Lire(h)
    Ecrire("Entrer les minutes :")
    Lire(m)
    Ecrire("Entrer les secondes :")
    Lire(s)
    s ← s + 1
    Si s = 60 alors
        s ← 0
        m ← m + 1
    FinSi
    Si m = 60 alors
        m ← 0
        h ← h + 1
    FinSi
    Si h = 24 alors
        h ← 0
    FinSi
    Ecrire("Dans une minute, il sera : ", h, " heure(s), ", m, " minute(s) et ", s, " seconde(s)")
```
