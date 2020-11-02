# Exercice supplémentaire 2

## Enoncé

Dans cet exercice nous allons analyser un schéma de calcul des impôts et écrire un programme qui calcule l’impôt brut sur le revenu d’un contribuable étant donné :
– sa situation de famille ;
– le nombre de personnes à sa charge ;
– son revenu net imposable.
On va utiliser une version extrêmement simplifiée de la méthode de calcul des impôts en France. L’impôt est calculé en utilisant la formule :

`I = R × T − D × P`

où : `I` est le montant d’impôt brut, `R` est le revenu net imposable, `T` est le taux d’imposition, `D` est la déduction par part et `P` est le nombre de parts.
D’abord, il faut déterminer le nombre de parts `P`. Le contribuable compte pour une part. S’il est marié (ou pacsé), son conjoint compte aussi pour une part. Les deux premiè res personnes à charge comptent pour une demi-part chacune. Les personnes à charge suivantes comptent pour une part chacune. Le taux d’imposition `T` et la déduction `D` dépendent du revenu par part `R/P`. Ils sont déterminés par le tableau suivant.

| R/P entre | T | D |
| -| - | -|
| 0 € et 5 614 €| 0,0 % | 0,00 €|
| 5 614 € et 11 198 € | 5,5 % | 308,77 €|
|11 198 € et 24 872 € | 14,0 % | 1 260,60 € |
| 24 872 € et 66 680 € | 30,0 % | 5 240,12 €|
| plus 66 680 € | 40,0 € | 11 908,12 € | m = 5 pieds et 11 pouces

Le montant de l’impôt est arrondi vers la valeur entière la plus proche.

Ecrire un programme qui demande `a l’utilisateur les inform ´ ations n´ecessaires et qui calcule son impˆot brut.

## Exemple d'exécution

Soit un contribuable marié ayant deux enfants (3 parts) avec un revenu imposable de 24 000 €. Son revenu par part est 8 000 € (compris entre 5 614 e et 11 198 e). Son impôt brut est donc 24000 × 0, 055 − 308, 77 × 3 = 393, 69 € arrondi à 394 €.



