# Variables

## Qu'est-ce qu'une variable?

Espace de stockage en mémoire, identifié par un nom, et dont la valeur peut changer au cours de l'exécution du programme.

Par exemple

$$x \leftarrow 3$$

Signifie que l'on stocke la valeur 3 dans la variable $x$.

On peut ensuite utiliser la valeur de la variable $x$ dans des calculs.

$$y \leftarrow x + 1$$

Que vaut $y$?
<div v-click>4</div>

---

## Types de variables

Une variable possède un type qui détermine la nature de la donnée stockée.

Par exemple:

<v-click>

- entier
- réel
- caractère
- chaîne de caractères
- booléen
- ...

</v-click>

---

## Types de variables (suite)

Détermine la taille de l'espace de stockage nécessaire.

Le type peut être:

- déterminé automatiquement (inféré) par le langage de programmation
- ou spécifié par le programmeur (statique).

Par exemple:

### Exemple en Python

```python
x = 3 # x est un entier; type inféré
```

### Exemple en C

```c
int x = 3; // x est un entier; type spécifié
```

---

## Langages fortement typés vs. faiblement typés

Un langage est dit fortement typé lorsqu'il garantit que les opérations sont effectuées sur des données du bon type.

Par exemple, si la fonction `somme` ne peut être appliquée qu'à des entiers, alors si on essaie de l'appliquer à un réel, le langage doit signaler une erreur.

On peut définir les deux règles suivantes pour un langage fortement typé:

- la compilation ou l'exécution peuvent détecter des erreurs de typage
- les conversions implicites de type sont interdites

---

## Typage statique vs. dynamique

Un langage est dit à typage statique lorsque le type de chaque variable est connu à la compilation $\rightarrow$ taille de l'espace de stockage nécessaire est connue à l'avance.

En revanche, un langage à typage dynamique assigne un type à chaque variable durant l'exécution du programme.

Dynamique:

- "à la volée"
- plus de flexibilité
- plus de risques d'erreurs

En général, les langages à typage statique sont compilés, et les langages à typage dynamique sont interprétés.

---

## Résumé des types de langages

| Typage    | Fort                       | Faible     |
| --------- | -------------------------- | ---------- |
| Statique  | Java, Rust, Haskell, OCaml | C, C++     |
| Dynamique | Python, Ruby               | JavaScript |

---

## Variables mutables vs. immutables

Mutable: peut changer de valeur au cours de l'exécution du programme.

Immutables (constantes): valeur fixe

Exemple en Rust:

```rust
let mut x = 3; // x est une variable mutable
x = x + 1; // x peut changer de valeur
```

```rust
let x = 3; // x est une constante
x = x + 1; // erreur: x est immuable
```
