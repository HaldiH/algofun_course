# Structures de contrôle

---

## Structures de choix (IF ... then)

- Les structures de choix vous permettent de prendre des décisions en fonction de conditions.
- `IF ... THEN` est la structure de base pour effectuer des actions conditionnelles.

```python
if condition:
    # Code à exécuter si la condition est vraie
else:
    # Code à exécuter si la condition est fausse
```

---
layout: image
image: /images/flowchart_of_if_else_in_c.png
backgroundSize: 40% 65%
---

## Diagramme de flux

---

## Opérateurs de comparaison

- Pour utiliser les structures de choix, vous avez besoin d'opérateurs de comparaison.
- Exemples d'opérateurs de comparaison :
  - `==` (égal)
  - `!=` (différent)
  - `<` (inférieur à)
  - `>` (supérieur à)
  - `<=` (inférieur ou égal à)
  - `>=` (supérieur ou égal à)

---

## Opérateurs logiques

- Vous pouvez combiner plusieurs conditions en utilisant des opérateurs logiques. Les opérateurs logiques s'appliquent à des expressions booléennes.
- Exemples d'opérateurs logiques :
  - `and` (et)
  - `or` (ou)
  - `not` (non)
  - `xor` (ou exclusif)

---

### Table de vérité de l'opérateur `and`

| A     | B     | A and B |
|-------|-------|---------|
| False | False | False   |
| False | True  | False   |
| True  | False | False   |
| True  | True  | True    |

---

### Table de vérité de l'opérateur `or`

| A     | B     | A or B |
|-------|-------|--------|
| False | False | False  |
| False | True  | True   |
| True  | False | True   |
| True  | True  | True   |

---

### Table de vérité de l'opérateur `not`

| A     | not A |
|-------|-------|
| False | True  |
| True  | False |

---

### Table de vérité de l'opérateur `xor`

| A     | B     | A xor B |
|-------|-------|---------|
| False | False | False   |
| False | True  | True    |
| True  | False | True    |
| True  | True  | False   |

---

## Exemple

Par exemple, pour afficher un message si un nombre est positif :

```python
x = 5
if x > 0:
    print("x est positif")
else:
    print("x est négatif ou nul")
```

Quel message sera affiché si `x` vaut -3 ? Et si `x` vaut 0 ?

---

## Exercice

En n'utilisant que les opérateur booléens `and`, `or` et `not`, reproduisez les tables de vérité des opérateurs `xor` et `implies`.

Table de vérité de l'opérateur `implies` :

| A     | B     | A implies B |
|-------|-------|-------------|
| False | False | True        |
| False | True  | True        |
| True  | False | False       |
| True  | True  | True        |

---

## Structures conditionnelles imbriquées

Vous pouvez imbriquer des structures conditionnelles pour des décisions complexes.

Exemple :

```python
if condition1:
    if condition2:
        # Code à exécuter si condition1 et condition2 sont vraies
    else:
        # Code à exécuter si condition1 est vraie et condition2 est fausse
else:
    # Code à exécuter si condition1 est fausse
```

---

### Exemple

Si on souhaite construire un algorithme pour choisir quel véhicule on souhaite prendre et où on souhaite aller :

```python
if not vacances:
    if meteo == "beau":
        print("Je vais au travail en vélo")
    else:
        print("Je vais au travail en bus")
else:
    if meteo == "beau":
        print("Je vais à la plage en voiture")
    else:
        print("Je reste à la maison")
```

---

## Structures de choix multiples

Parfois, vous devez choisir parmi plusieurs options.

Utilisez IF ... ELIF ... ELSE pour gérer plusieurs cas.

```python
if condition1:
    # Code à exécuter si condition1 est vraie
elif condition2:
    # Code à exécuter si condition1 est fausse et condition2 est vraie
else:
    # Code à exécuter si aucune des conditions n'est vraie
```

---

### Exemple

On peut réécrire l'exemple précédent avec des structures de choix multiples :

```python
if meteo == "soleil" and not en_semaine:
    print("Je vais à la plage")
elif meteo == "pluie" and en_semaine:
    print("Je vais au travail")
else:
    print("Je reste à la maison")
```

---

## Structures à choix multiples

- Les structures de choix multiples vous permettent de choisir parmi plusieurs options.

Par exemple, pour choisir une action en fonction d'une valeur numérique :

```python
if jour == 1:
    print("Lundi")
elif jour == 2:
    print("Mardi")
elif jour == 3:
    print("Mercredi")
elif jour == 4:
    print("Jeudi")
elif jour == 5:
    print("Vendredi")
else:
    print("Week-end")
```

Mais cette structure est un peu verbeuse...

---

## Switch / Case

Certains langages de programmation proposent une structure de contrôle spécifique pour les choix multiples, appelée `switch` ou `case`.

En Python, depuis la version 3.10, on peut utiliser `match` :

```python
match jour:
    case 1:
        print("Lundi")
    case 2:
        print("Mardi")
    case 3:
        print("Mercredi")
    case 4:
        print("Jeudi")
    case 5:
        print("Vendredi")
    case _: # dans tous les autres cas
        print("Week-end")
```

Ici, Python va essayé de matcher la valeur de `jour` avec les différentes cases. Si aucune case ne matche, il exécute le code après `case _:`.

---

## Résumé

- IF `condition` THEN `action 1` ELSE `action 2`: effectue `action 1` si `condition` est vraie, sinon effectue `action 2`.
- `condition` doit être une expression booléenne.
- `action 1` et `action 2` peuvent être des instructions simples ou des blocs d'instructions.
- `action 2` est facultatif (pas de ELSE).
- Vous pouvez imbriquer des structures conditionnelles pour des décisions complexes.
- Utilisez IF ... ELIF ... ELSE pour gérer plusieurs cas.
- `switch` / `case` est une structure de contrôle spécifique pour les choix multiples.
