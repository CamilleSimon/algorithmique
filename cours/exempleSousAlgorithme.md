```
Sous-algorithme MoyenneEtSomme
Paramètres d’entrée :
	tab[] : tableau d'e réels
Paramètres de sortie :
	moyenne : réel
	somme : entier
Variables : // Cette ligne est optionnelle car il n’y a pas d’autres variables dans cette exemple
Instructions :
	somme ← 0
	Pour i de 0 à Longueur(tab) – 1 faire
		moyenne ← moyenne + tab[i]
		somme ← somme + tab[i]
	FinPour
	moyenne ← moyenne / Longueur(tab)
```

```
Algorithme principal
Variables :
    tableauNotes[] : tableau de réels
    moyenne, somme : réels
    taille : entier
Instructions :
    taille ← 0
    Tantque taille <= 0 faire
        Ecrire("Donner le nombre de notes :")
        Lire(taille)
    FinTantQue

    Pour i de 0 à taille - 1 faire
        Ecrire("Donner la ", i + 1, " note :")
        Lire(tableauNotes[i])
    FinPour

    moyenne, somme ← MoyenneEtSomme(tableauNotes)

    Ecrire("La moyenne des notes est : ", moyenne, " et la somme des notes est ", somme)
```