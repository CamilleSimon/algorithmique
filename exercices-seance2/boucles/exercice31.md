# Exercice 31

## Enoncé

Écrire un algorithme qui permette de connaître ses chances de gagner au tiercé, quarté, quinté et autres impôts volontaires. On demande à l’utilisateur le nombre de chevaux partants, et le nombre de chevaux joués. Les deux messages affichés devront être:

```
Dans l’ordre: une chance sur X de gagner
Dans le désordre: une chance sur Y de gagner
```

`X` et `Y` nous sont donnés par la formule suivante, si `n` est le nombre de chevaux partants et `p` le nombre de chevaux joués (on rappelle que le signe `!` signifie "factorielle", comme dans l'exercice 27.

```
X = !n / !(n - p)
Y = !n / ( !p * !(n – p))
```

NB: cet algorithme peut être écrit d’une manière simple, mais relativement peu performante. Ses performances peuvent être singulièrement augmentées par une petite astuce. Vous commencerez par écrire la manière la plus simple, puis vous identifierez le problème, et écrirez une deuxième version permettant de le résoudre.

## Correction

```
Variables
    n, fn, p, fp, fnp, x, y : entiers
Instructions
    Ecrire("Donner le nombre de chevaux partants : ")
    Lire(n)
    Ecrire("Donner le nombre de chevaux joués : ")
    Lire(p)

    fn ← 1
    fp ← 1
    fnp ← 1

    Pour i de 2 à n faire
        fn ← fn * i
    FinPour

    Pour i de 2 à p faire
        fp ← fp * i
    FinPour

    Pour i de 2 à n - p faire
        fnp ← fnp * i
    FinPour

    x ← fn / fnp
    y ← fn / (fp * fnp)

    Ecrire("Dans l'ordre : une chance sur ", x, " de gagner")
    Ecrire("Dans le désordre : une chance sur ", y, " de gagner")
```

Version alternative

```
Variables
    n, fn, p, fp, fnp, i, x, y : entiers
Instructions
    Ecrire("Donner le nombre de chevaux partants : ")
    Lire(n)
    Ecrire("Donner le nombre de chevaux joués : ")
    Lire(p)

    fn ← 1
    fp ← 1
    fnp ← 1
    i ← 2

    Tant que i < n faire
        fn ← fn * i
        
        Si p <= i alors
            fp ← fp * i
        FinSi

        Si n - p <= i alors
            fnp ← fnp * i
        FinSi
        
        i ← i + 1
    FinTQ

    x ← fn / fnp
    y ← fn / (fp * fnp)

    Ecrire("Dans l'ordre : une chance sur ", x, " de gagner")
    Ecrire("Dans le désordre : une chance sur ", y, " de gagner")
```