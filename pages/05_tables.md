---
layout: section
---

# Tableaux

---

## Définition

Les tableaux (table ou array en anglais) sont des structures de données qui permettent de stocker plusieurs valeurs de même type dans une seule variable. Les éléments d'un tableau sont indexés, c'est-à-dire qu'ils sont accessibles par un numéro de position.

Les tableaux sont très utilisés en programmation pour stocker des collections de données, comme des listes d'entiers, de réels, de chaînes de caractères, etc.

Ils sont définis par un nom, une taille et parfois un type (dans les langages de programmation fortement typés). Les éléments d'un tableau sont souvent du même type, mais ce n'est pas une règle absolue.

Par exemple, une chaîne de caractères est un tableau de caractères.

---

## Déclaration

Un tableau peut être déclaré de différentes manières, selon le langage de programmation. Mais il faut nécessairement préciser sa taille, ou la taille maximale qu'il peut atteindre. Il est souvent possible de modifier la taille d'un tableau après sa déclaration.

Par exemple, en Python:

```python
# Déclaration d'un tableau de 5 entiers
tab = [0, 1, 2, 3, 4]
```

En C:

```c
// Déclaration d'un tableau de 5 entiers
int tab[5] = {0, 1, 2, 3, 4};
//      ^ taille, optionelle
```

---

## Accès aux éléments

Pour accéder à un élément d'un tableau, on utilise son index, c'est-à-dire sa position dans le tableau. Les indices commencent souvent à 0, mais ce n'est pas une règle absolue.

Par exemple, pour accéder au premier élément d'un tableau `tab` en C:

```c
int x = tab[0];
```

En Python, on peut aussi utiliser des indices négatifs pour accéder aux éléments en partant de la fin du tableau:

```python
x = tab[-1] # dernier élément
```

---

## Exemple

Par exemple, pour afficher tous les éléments d'un tableau en C:

```c
int tab[5] = {0, 1, 2, 3, 4};
for (int i = 0; i < 5; i++) {
    printf("%d\n", tab[i]);
}
```

