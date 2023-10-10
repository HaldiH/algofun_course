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

## Résumé

- IF `condition` THEN `action 1` ELSE `action 2`: effectue `action 1` si `condition` est vraie, sinon effectue `action 2`.
- `condition` doit être une expression booléenne.
- `action 1` et `action 2` peuvent être des instructions simples ou des blocs d'instructions.
- `action 2` est facultatif (pas de ELSE).
