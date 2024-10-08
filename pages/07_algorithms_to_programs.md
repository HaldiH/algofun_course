---
layout: section
---

# Des algorithmes vers les programmes

---

## Structure de données

Les algorithmes manipulent des données. Ces données sont stockées dans des structures de données. Les structures de données les plus courantes sont les suivantes :

- Les tableaux
- Les dictionnaires
- Les listes chaînées
- Les piles
- Les files
- Les arbres
- Les graphes

En Python, la plupart de ces structures peuveut être implémentées à l'aide de listes. En revanche, les structures plus complexes comme les arbres et les graphes nécessitent souvent des classes spécifiques.

---

## Classes

En Python, les classes permettent de définir des objets. Un objet est une instance d'une classe. Les classes permettent de regrouper des données et des méthodes qui agissent sur ces données.

```python

class Personne:
    def __init__(self, nom, prenom):
        self.nom = nom # Attribut
        self.prenom = prenom # Attribut

    def afficher(self): # Méthode
        print(f"{self.prenom} {self.nom}")

p = Personne("Doe", "John")
p.afficher()
```

---

## Algorithmes de tri

Les algorithmes de tri permettent de trier des données. Il existe de nombreux algorithmes de tri. Les plus connus sont les suivants :

- Le tri par sélection
- Le tri par insertion
- Le quicksort (le plus rapide)

Voir [VisuAlgo - Sorting](https://visualgo.net/en/sorting) pour visualiser ces algorithmes.

---

## Arbres

Les arbres sont des structures de données qui permettent de représenter des hiérarchies. Les arbres sont composés de nœuds. Chaque nœud peut avoir un ou plusieurs enfants. Les arbres peuvent être binaires ou non binaires.

Les arbres peuvent être représentés à l'aide de classes:

```python
class Noeud:
    def __init__(self, valeur):
        self.valeur = valeur
        self.gauche = None
        self.droite = None

arbre = Noeud(1)
arbre.gauche = Noeud(2)
arbre.droite = Noeud(3)
```

---

## Graphes

Les graphes sont des structures de données qui permettent de représenter des relations entre des objets. Les graphes sont composés de sommets et d'arêtes. Les graphes peuvent être orientés ou non orientés.

Les graphes peuvent être représentés à l'aide de matrices d'adjacence ou de listes d'adjacence.

```python
graphe = {
    1: [2, 3],
    2: [1, 3],
    3: [1, 2]
}
```

Voir [VisuAlgo - Graph Data Structures](https://visualgo.net/en/graphds) pour visualiser les graphes.

---

## Algorithmes sur les graphes

Il existe de nombreux algorithmes pour manipuler les graphes. Les plus connus sont les suivants :

- Le parcours en profondeur (DFS)
- Le parcours en largeur (BFS)
- L'algorithme de Dijkstra (plus court chemin)

Voir [VisuAlgo - Single Source Shortest Path](https://visualgo.net/en/sssp) pour visualiser ces algorithmes.

---

## Exercices

1. Implémenter un algorithme de tri par sélection en Python.
2. Implémenter un arbre binaire en Python.
3. Implémenter un graphe non orienté en Python.
