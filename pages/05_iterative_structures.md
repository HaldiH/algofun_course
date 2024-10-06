---
layout: section
---

# Structures itératives

---

## Blocs d'instructions

- Un bloc d'instructions est une suite d'instructions regroupées entre des accolades (C-like), des mots clés (Bash), ou indentées (Python).
- Les blocs d'instructions permettent de regrouper des instructions pour les exécuter ensemble.

Par exemple, les instructions contenues dans un bloc `if` ne sont exécutées que si la condition est vraie, et constituent un bloc d'instructions.

---

## Boucle `while`

La boucle `while` permet de répéter un bloc d'instructions tant qu'une condition est vraie.

Par exemple, pour créer un algorithme qui représente les tâches à faire en fonction du jour de la semaine:

```python
jour = 1
while jour < 6: # tant que ce n'est pas le week-end
    travailler()
    manger()
    dormir()
    jour += 1 # on passe au jour suivant
```

Attention à la condition de sortie de la boucle! Si elle n'est jamais vraie, la boucle ne s'arrêtera jamais.

---

## Boucle `for`

La boucle `for` permet de répéter un bloc d'instructions un nombre de fois déterminé, ou pour chaque élément d'une séquence.

Par exemple, pour sommer tous les entiers de 1 à 100, en C:

```c
int somme = 0; // initialisation de la variable somme
for (int i = 1; i <= 100; i++) { // pour i allant de 1 à 100
    somme += i; // somme = somme + i
}
```

En Python, on peut utiliser la fonction `range` pour générer une séquence d'entiers:

```python
somme = 0
for i in range(1, 101): # pour i allant de 1 à 100
    somme += i
```

---

### Itération sur une chaîne de caractères

Une chaîne de charactères est une séquence de caractères. On peut itérer sur les caractères d'une chaîne de caractères.

Par exemple, pour afficher chaque caractère d'une chaîne de caractères (en Python):

```python
chaine = "Hello, world!"
for caractere in chaine:
    print(caractere)
```

Ou en utilisant l'index des caractères (en C):

```c
char chaine[] = "Hello, world!";
for (int i = 0; i < strlen(chaine); i++) {
    printf("%c\n", chaine[i]);
}
```

---

### Exercice

Écrire un programme qui compte le nombre de voyelles dans une chaîne de caractères.

---

## Boucle `do ... while`

La boucle `do ... while` est une variante de la boucle `while` où le bloc d'instructions est exécuté au moins une fois, puis tant qu'une condition est vraie.

Par exemple, pour demander à l'utilisateur de saisir un nombre entre 1 et 10:

```c
int nombre;
do {
    printf("Entrez un nombre entre 1 et 10: ");
    scanf("%d", &nombre);
} while (nombre < 1 || nombre > 10);
```

Ceci est particulièrement utile pour les menus interactifs.

## Résumé

- Les boucles permettent de répéter un bloc d'instructions.
- La boucle `while` répète un bloc d'instructions tant qu'une condition est vraie.
- La boucle `for` répète un bloc d'instructions un nombre de fois déterminé, ou pour chaque élément d'une séquence.
- La boucle `do ... while` répète un bloc d'instructions au moins une fois, puis tant qu'une condition est vraie.
