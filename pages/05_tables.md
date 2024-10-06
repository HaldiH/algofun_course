---
layout: section
---

# Tableaux

---

## Définition

Les tableaux (table ou array en anglais) sont des structures de données qui permettent de stocker plusieurs valeurs de même type dans une seule variable. Les éléments d'un tableau sont indexés, c'est-à-dire qu'ils sont accessibles par un numéro de position.

Les tableaux sont très utilisés en programmation pour stocker des collections de données de manière ordonnée, comme des listes d'entiers, de réels, de chaînes de caractères, etc.

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

En Python:

```python
tab = [0, 1, 2, 3, 4]
for i in range(5):
    print(tab[i])
```

---

## Modification

Pour modifier un élément d'un tableau, on utilise son index:

```c
int tab[5] = {0, 1, 2, 3, 4};
tab[0] = 42;

for (int i = 0; i < 5; i++) {
    printf("%d\n", tab[i]);
}
```

Ce code affiche:

```
42
1
2
3
4
```

---

## Taille

La taille d'un tableau est souvent fixée lors de sa déclaration, mais il est parfois possible de la modifier dynamiquement. Par exemple, en Python:

```python
tab = [0, 1, 2, 3, 4]
tab.append(5) # ajoute un élément à la fin
print(tab) # affiche [0, 1, 2, 3, 4, 5]
```

Pour connaître la taille d'un tableau, on peut utiliser une fonction ou une propriété spécifique. Par exemple, en Python:

```python
n = len(tab)
print(n) # affiche 6
```

Dans d'autres langages, il est parfois nécessaire de stocker la taille du tableau séparément. De plus, il peut être nécessaire de réallouer la mémoire pour agrandir un tableau (c.f. [`realloc`](https://man7.org/linux/man-pages/man3/realloc.3p.html) en C).

---

## Tableaux multidimensionnels

Il est possible de déclarer des tableaux à plusieurs dimensions, c'est-à-dire des tableaux de tableaux. Par exemple, un tableau à deux dimensions peut être utilisé pour représenter une matrice.

Soit une matrice 2x2:

$$A = \begin{pmatrix} 1 & 2 \\ 3 & 4 \end{pmatrix}$$

Ell peut être représentée en Python par un tableau de tableaux:

```python
A = [[1, 2], [3, 4]]
```

Et pour accéder à un élément de la matrice:

```python
x = A[0][1] # deuxième élément de la première ligne
print(x) # affiche 2
```

---

### Exercice

Écrire une fonction `affiche_matrice` qui prend en argument une matrice (tableau à deux dimensions) et l'affiche ligne par ligne.

---

## Opérations sur les tableaux

Il est possible de faire des opérations sur les tableaux, comme les additionner, les multiplier, les trier, etc. Ces opérations dépendent du langage de programmation et des bibliothèques disponibles.

En C, il est possible d'additionner deux tableaux élément par élément:

```c
int a[3] = {1, 2, 3};
int b[3] = {4, 5, 6};
int c[3];

for (int i = 0; i < 3; i++) {
    c[i] = a[i] + b[i];
}
```

En Python, on peut utiliser une boucle `for` ou une compréhension de liste (cf. cours de Python):

```python
a = [1, 2, 3]
b = [4, 5, 6]
c = [x + y for x, y in zip(a, b)]
print(c) # affiche [5, 7, 9]
```

---

### Concaténation

Il est possible de concaténer deux tableaux en les ajoutant bout à bout. Par exemple, en Python:

```python
a = [1, 2, 3]
b = [4, 5, 6]
c = a + b
print(c) # affiche [1, 2, 3, 4, 5, 6]
```

---

### Présence d'un élément

Il est possible de vérifier si un élément est présent dans un tableau en utilisant l'opérateur `in`. Par exemple, en Python:

```python
tab = [1, 2, 3, 4, 5]
if 3 in tab:
    print("3 est dans le tableau")
```

---

### Séquence

Un tableau est une séquence, c'est-à-dire qu'il est possible de le parcourir avec une boucle `for`. Par exemple, en Python:

```python
tab = [1, 2, 3, 4, 5]
for x in tab:
    print(x)
```

---

## Exemple: jours de la semaine

Reprenons l'exemple des jours de la semaine. On peut les stocker dans un tableau:

```python
jours = ["lundi", "mardi", "mercredi", "jeudi", "vendredi", "samedi", "dimanche"]
weekend = [jours[-2], jours[-1]]
```

Et maintenant, on peut vérifier si un jour est un jour de la semaine ou un jour du week-end:

```python
jour = "lundi"
if jour in weekend:
    print("C'est le week-end!")
else:
    print("C'est la semaine!")
```

---

## Exemple: voyelles

Il est possible de vérifier si une lettre est une voyelle en utilisant un tableau:

```python
voyelles = "aeiouy"
mot = "bonjour"
nb_voyelles = 0
for lettre in mot:
    if lettre in voyelles:
        nb_voyelles += 1
print(nb_voyelles)
```

---

## Exemple: moyenne

La moyenne d'un tableau est définie comme la somme de ses éléments divisée par sa taille:

$$\text{moyenne} = \frac{\sum_{i=0}^{n-1} \text{tab}[i]}{n}$$

Il est possible de calculer la moyenne d'un tableau en utilisant une boucle `for`:

```python
tab = [1, 2, 3, 4, 5]
n = len(tab)
s = 0

for i in range(n):
    s += tab[i]

moyenne = s / n
print(moyenne)
```