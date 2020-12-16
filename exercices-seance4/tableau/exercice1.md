# Exercice 1

## Enoncé

Ecrire un algorithme qui demande à l’utilisateur une taille pour un tableau, puis l’algorithme inscrit dans le tableau les nombres donnés par l’utilisateur. 

Une fois tous les nombres entrés, l’algorithme affiche : la somme, la moyenne et la plus petit valeur inscrite dans le tableau (sans l’avoir sauvegardé à la saisi).

## Correction

```
Variables
    taille : entier
    tableau[] : tableau de réels
    valeur, somme, moyenne, minimum : réel
Instructions
    taille ← 0 // Initialisation de la taille du tableau volontairement avec un nombre invalide

    Tant que taille <= 0 faire // Tant que la taille du tableau n'est pas valide, l'algo continue de demander une valeur à l'utilisateur
        Ecrire("Quel est le nombre de valeur que vous voulez saisir ?")
        Lire(taille)
    FinTQ

    // Initalisation du tableau
    tableau[] ← tableau[taille]

    // Remplissage du tableau
    Ecrire("Entrer les ", valeur, " valeurs :")
    Pour i de 0 à taille - 1 faire // `taille - 1` car l'index d'un tableau de `n` case va de 0 à `n - 1`
        Lire(valeur)
        tableau[i] ← valeur
    FinPour
        
    // Partie traitement des valeurs
    somme ← 0
    moyenne ← 0
    minimum ← tableau[0]
    Pour i de 0 à taille - 1 faire
        somme ← somme + tableau[i]
        moyenne ← moyenne + tableau[i]
        Si tableau[i] < minimum alors
            minimum ← tableau[i]
        FinSi
    FinPour

    moyenne ← moyenne / taille

    Ecrire("La somme est : ", somme, ", la moyenne est : ", moyenne, " et le minimum est : ", minimum)
```