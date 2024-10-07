---
layout: section
---

# Fonctions

---

## Définition

Une fonction est un bloc de code qui effectue une tâche spécifique. Elle peut être appelée (ou invoquée) à partir d'autres parties du programme.

Leur utilisation permet de:

- **Réutiliser** du code
- **Simplifier** et **organiser** le code
- **Décomposer** un problème en sous-problèmes

---

## Structure

Une fonction est composée de:

- Un **nom**
- Une **liste de paramètres** (ou arguments)
- Un **corps** (bloc d'instructions)

---

## Exemple simple de fonction

Une fonction qui affiche un message de salutation:

```
Fonction Salut()
    Afficher("Bonjour, monde!")
FinFonction
```

Appel de la fonction:

```
Salut()
```

Sortie:

```
Bonjour, monde!
```

---

## Paramètres d'une fonction

Les paramètres sont des variables qui stockent des valeurs passées à une fonction. Ces variables sont propres à la fonction et ne sont pas accessibles en dehors de celle-ci.

Exemple:

```
Fonction SalutNom(Prenom)
    Afficher("Bonjour, " + Prenom + "!")
FinFonction
```

Appel de la fonction:

```
SalutNom("Alice")
```

Sortie:

```
Bonjour, Alice!
```

---

## Retour de valeur

Une fonction peut retourner une valeur à l'endroit où elle est appelée. Cette valeur peut être utilisée dans le programme principal.

Exemple:

```
Fonction Carre(x)
    Retourner x * x
FinFonction
```

Appel de la fonction:

```
Resultat = Carre(5)
Afficher(Resultat)
```

Sortie:

```
25
```

---

## Fonction avec plusieurs paramètres

Une fonction peut avoir plusieurs paramètres.

Exemple:

```
Fonction CalculerMoyenne(Note1, Note2, Note3)
    Moyenne = (Note1 + Note2 + Note3) / 3
    Retourner Moyenne
FinFonction
```

Appel de la fonction:

```
Moyenne = CalculerMoyenne(12, 15, 14)
Afficher(Moyenne)
```

Sortie:

```
13.666666666666666
```

---

## Fonction récursive

**Définition:** Une fonction est dite récursive si elle s'appelle elle-même.

Exemple: Calcul du factoriel d'un nombre.

```
Fonction Factoriel(n)
    Si n = 0 ou n = 1 alors
        Retourner 1
    Sinon
        Retourner n * Factoriel(n - 1)
    FinSi
FinFonction
```

Appel de la fonction:

```
Resultat = Factoriel(5)
Afficher(Resultat)
```

Sortie:

```
120
```

---

## Exercice Pratique

Écrire une fonction qui prend en paramètre une liste de nombres et calcule leur moyenne.

Rappel: La moyenne de $n$ nombres est la somme de ces nombres divisée par $n$.

En python, pour connaître la longueur d'une liste, on peut utiliser la fonction `len()`.

---

## Conclusion

- Blocs de code réutilisables
- Simplification et organisation du code
- Décomposition d'un problème en sous-problèmes
- Fonctions récursives
