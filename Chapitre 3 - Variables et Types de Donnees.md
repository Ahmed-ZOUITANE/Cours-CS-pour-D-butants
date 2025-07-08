# 🔢 Chapitre 3 : Variables et Types de Données en C\#

---

## 🎯 1. Qu’est-ce qu’une variable ?

Une **variable** est un **emplacement en mémoire** qui contient une valeur pouvant changer pendant l'exécution du programme.
On lui donne :

* **un nom**,
* **un type** (ex : `int`, `string`, `bool`, etc.),
* et **une valeur**.

---

## 🧠 2. Syntaxe de base

```csharp
type nomDeLaVariable = valeur;
```

### Exemples :

```csharp
int age = 25;
string nom = "Ahmed";
bool estActif = true;
double taille = 1.75;
char initiale = 'A';
```

---

## 📦 3. Les types de données primitifs

| Type     | Description                      | Exemple               |
| -------- | -------------------------------- | --------------------- |
| `int`    | Entier                           | `int x = 10;`         |
| `double` | Nombre décimal (haute précision) | `double pi = 3.14;`   |
| `float`  | Nombre décimal (moins précis)    | `float t = 1.75f;`    |
| `char`   | Caractère (entre `'`)            | `char c = 'A';`       |
| `string` | Chaîne de caractères             | `string nom = "Ali";` |
| `bool`   | Booléen (`true` ou `false`)      | `bool actif = true;`  |

🔸 Remarque : pour `float`, il faut ajouter `f` à la fin (ex : `1.5f`).

---

## 🧪 4. Déclaration sans initialisation

```csharp
int nombre;
nombre = 42;
```

---

## ✍️ 5. Lire une variable depuis la console

```csharp
Console.WriteLine("Quel est ton nom ?");
string nom = Console.ReadLine();

Console.WriteLine("Quel âge as-tu ?");
int age = int.Parse(Console.ReadLine());

Console.WriteLine($"Bonjour {nom}, tu as {age} ans !");
```

🟡 `int.Parse()` permet de convertir le texte saisi en entier.

---

## 🎯 6. Concaténation et interpolation

### 🔹 Concaténation classique :

```csharp
string message = "Salut " + nom + " !";
```

### 🔹 Interpolation de chaîne :

```csharp
string message = $"Salut {nom}, tu as {age} ans.";
```

---

## 📌 7. Constantes

Si tu veux une variable **non modifiable** :

```csharp
const double PI = 3.14159;
```

---

## 🧼 8. Bonnes pratiques

* Les noms de variables commencent par **une minuscule** : `nom`, `ageClient`
* Pas d'espaces, pas de caractères spéciaux (utilise `_` ou camelCase)
* Utiliser des noms **clairs** et **significatifs**

---

## ✅ Résumé du chapitre

| Concept       | Exemple                          |
| ------------- | -------------------------------- |
| Variable      | `int age = 30;`                  |
| Constante     | `const double PI = 3.14;`        |
| Lecture       | `Console.ReadLine()`             |
| Conversion    | `int.Parse()`                    |
| Types de base | `int`, `string`, `bool`, `char`… |
| Interpolation | `$"Salut {nom}"`                 |
