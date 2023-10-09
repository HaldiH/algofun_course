# Assignation de variables

## Qu'est-ce qu'une assignation?

Assigner une valeur à une variable signifie stocker cette valeur dans la mémoire de l'ordinateur.

Par exemple:

$$x \leftarrow 3$$

On stocke dans la variable $x$ la valeur 3.

On peut ensuite utiliser la valeur de la variable $x$ dans des calculs.

---

## Assignation

On peut assigner soit un littéral (p.ex. 42, "Hello", ...), soit une expression.

Par exemple:

$$x \leftarrow 3$$

$$y \leftarrow x + 1$$

Dans $y$ on stocke le résultat de l'exécution de l'expression $x + 1$.

L'expression peut contenir autant de variables et de littéraux que l'on veut, tant qu'elle reste valable.

Attention aux types!

---

## Exemples

<v-click>

### Langage fortement typé

```python
x = 3 # x est un entier; type inféré
y = "Hello" # y est une chaîne de caractères; type inféré
z = x + y # Erreur! On ne peut pas additionner un entier et une chaîne de caractères
```

</v-click>

<v-click>

### Langage faiblement typé

```javascript
x = 3 // x est un entier; type inféré
y = "Hello" // y est une chaîne de caractères; type inféré
z = x + y // z = "3Hello"... ??!
```

</v-click>
