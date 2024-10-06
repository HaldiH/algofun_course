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

## Déclaration de variables

Pour déclarer une variable, on doit spécifier son nom, et éventuellement son type.

Par exemple, en C:

```c
int x; // x est un entier
char c; // c est un caractère
float f; // f est un réel
```

En Python, le type de la variable est inféré automatiquement, lors de l'assignation de la valeur:

```python
x = 3 # x est un entier
c = 'a' # c est un caractère
f = 3.14 # f est un réel
```

---

## Assignation de variables

**Définition**: Assigner une valeur à une variable signifie lier un nom (une variable) à une valeur.

À l'inverse de la déclaration, qui crée le conteneur, l'assignation remplit le conteneur avec une valeur.

Par exemple:

$$x \leftarrow 3$$

On stocke dans la variable $x$ la valeur 3.

On peut ensuite utiliser la valeur de la variable $x$ dans des calculs.

---

### Assignation (suite)

On peut assigner soit un littéral (p.ex. 42, "Hello", ...), soit une expression.

Par exemple:

$$x \leftarrow 3$$

$$y \leftarrow x + 1$$

Dans $y$ on stocke le résultat de l'exécution de l'expression $x + 1$.

L'expression peut contenir autant de variables et de littéraux que l'on veut, tant qu'elle reste valable.

Attention aux types!

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

### Exemple typage fort

Si on essaie d'ajouter un entier et une chaîne de caractères en Python:

```python
x = 3 # x est un entier
y = "3" # y est une chaîne de caractères
z = x + y # erreur: addition d'un entier et d'une chaîne de caractères
```

Ici, Python détecte une erreur de typage lors de l'exécution du programme.

---

### Exemple typage faible

En revanche, en JavaScript:

```javascript
let x = 3; // x est un entier
let y = "3"; // y est une chaîne de caractères
let z = x + y; // z vaut "33"; 3 est converti en chaîne de caractères et concaténé avec "3"
```

JavaScript ne détecte pas d'erreur de typage, et effectue une conversion implicite de type.

En revanche, si on essaie de soustraire un entier d'une chaîne de caractères:

```javascript
let x = 3; // x est un entier
let y = "3"; // y est une chaîne de caractères
let z = x - y; // z vaut 0
```

JavaScript effectue une conversion implicite de type, et z vaut 0.

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

---

## Concaténation

Concaténation: opération qui consiste à mettre bout à bout deux chaînes de caractères (ou séquences) pour en former une seule, plus longue.

Exemple en Python:

```python
x = "Hello"
y = "World"
z = x + " " + y # z vaut "Hello World"
```

---

### Concepts clés

- Concaténation de chaînes de caractères: le type le plus courant de concaténation, utilisé pour joindre des chaînes de caractères.
- Opérateurs de concaténation: `+` en Python et dans de nombreux autres langages.
- Différence de types: selon le langage, la concaténation peut être plus ou moins flexible. Comme on l'a vu, en JavaScript il est possible de concaténer un entier et une chaîne de caractères sans erreur, alors qu'en Python cela provoque une erreur. Pour permettre la concaténation de types différents, il faut souvent effectuer une conversion explicite de type, `str(x)` en Python par exemple.

---

#### Exemples de concaténation

Comme on l'a vu, en Python, on peut concaténer des chaînes de caractères.

```python
x = "Hello"
y = "World"
z = x + " " + y # z vaut "Hello World"
```

---

#### Convertir un entier en chaîne de caractères

En Python, pour concaténer un entier et une chaîne de caractères, il faut convertir l'entier en chaîne de caractères.

```python
year = 2028
event = "Olympics"
message = "Next " + event + " is in " + str(year)
```

Résultat: <div v-click>"Next Olympics is in 2028"</div>

---

#### Cas particulier: chaine vide

Concaténer une chaîne vide à une autre chaîne de caractères ne modifie pas la chaîne.

```python
x = "Hello"
y = ""
z = x + y # z vaut "Hello"
```

---

#### Charactères spéciaux

En Python, on peut utiliser des caractères spéciaux pour formater une chaîne de caractères.

Par exemple:

- `\n` pour un saut de ligne
- `\t` pour une tabulation

```python
x = "Hello\nWorld"
print(x)
```

Ce code affiche:

```
Hello
World
```


## Récupération de l'entrée utilisateur

Pour récupérer une valeur de l'utilisateur, on utilise une fonction spécifique du langage de programmation.

Par exemple, en Python:

```python
x = input("Entrez un nombre: ")
print("Vous avez entré", x)
```

Attention: la fonction `input` renvoie une chaîne de caractères, même si l'utilisateur entre un nombre!

Pour utiliser la valeur comme un nombre, il faut la convertir explicitement.

```python
x = int(input("Entrez un nombre: "))
y = x + 1
print("Le nombre suivant est", y)
```
