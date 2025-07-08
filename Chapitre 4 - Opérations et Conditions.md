# 🔣 Chapitre 4 : Opérations et Conditions en C\#

---

## 🧮 1. Les Opérateurs Arithmétiques

| Opérateur | Signification    | Exemple (`int x = 10, y = 3;`) |
| --------- | ---------------- | ------------------------------ |
| `+`       | Addition         | `x + y` → `13`                 |
| `-`       | Soustraction     | `x - y` → `7`                  |
| `*`       | Multiplication   | `x * y` → `30`                 |
| `/`       | Division entière | `x / y` → `3`                  |
| `%`       | Modulo (reste)   | `x % y` → `1`                  |

---

## 🔢 2. Opérateurs de Comparaison

| Opérateur | Signification     | Exemple (`x = 5`, `y = 3`) |
| --------- | ----------------- | -------------------------- |
| `==`      | Égal à            | `x == y` → `false`         |
| `!=`      | Différent de      | `x != y` → `true`          |
| `>`       | Supérieur à       | `x > y`  → `true`          |
| `<`       | Inférieur à       | `x < y`  → `false`         |
| `>=`      | Supérieur ou égal | `x >= 5` → `true`          |
| `<=`      | Inférieur ou égal | `x <= 2` → `false`         |

---

## ⚙️ 3. Les Conditions `if`, `else if`, `else`

### 🧪 Exemple simple :

```csharp
int age = 20;

if (age >= 18)
{
    Console.WriteLine("Tu es majeur.");
}
else
{
    Console.WriteLine("Tu es mineur.");
}
```

---

### 🔁 Avec plusieurs conditions :

```csharp
int note = 14;

if (note >= 16)
{
    Console.WriteLine("Très bien !");
}
else if (note >= 10)
{
    Console.WriteLine("Passable.");
}
else
{
    Console.WriteLine("Échec.");
}
```

---

## 🔗 4. Opérateurs Logiques

| Opérateur | Signification     | Exemple          |                 |         |   |         |
| --------- | ----------------- | ---------------- | --------------- | ------- | - | ------- |
| `&&`      | ET logique (and)  | `x > 0 && y > 0` |                 |         |   |         |
| \`        |                   | \`               | OU logique (or) | \`x > 0 |   | y > 0\` |
| `!`       | NON logique (not) | `!(x > 0)`       |                 |         |   |         |

---

### Exemple avec `&&` et `||` :

```csharp
int age = 25;
bool permis = true;

if (age >= 18 && permis)
{
    Console.WriteLine("Tu peux conduire.");
}
```

---

## ❓ 5. Opérateur Ternaire (if court)

```csharp
int age = 22;
string statut = (age >= 18) ? "majeur" : "mineur";
Console.WriteLine("Tu es " + statut);
```

---

## ⚠️ 6. Attention aux types

Tu ne peux pas comparer directement un `string` et un `int`, ou `bool` et `int`.

```csharp
// Correct
string nom = "Ahmed";
if (nom == "Ahmed") { ... }

// Incorrect
// if (nom == 10) { ... } → erreur
```

---

## ✅ Résumé du chapitre

| Élément     | Exemple                          |   |         |
| ----------- | -------------------------------- | - | ------- |
| Opérateurs  | `+`, `-`, `*`, `/`, `%`          |   |         |
| Comparaison | `==`, `!=`, `>`, `<`, `>=`, `<=` |   |         |
| Conditions  | `if`, `else if`, `else`          |   |         |
| Logique     | `&&`, \`                         |   | `, `!\` |
| Ternaire    | `condition ? vrai : faux`        |   |         |
