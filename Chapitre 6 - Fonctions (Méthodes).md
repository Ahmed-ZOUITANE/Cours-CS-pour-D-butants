# 📦 Chapitre 6 : Fonctions (Méthodes) en C\#

---

## 🎯 1. Qu’est-ce qu’une méthode ?

Une **méthode** (ou fonction) est un **bloc de code nommé** qu’on peut **réutiliser** plusieurs fois.

> Elle permet de **diviser un programme en petites parties logiques** et de rendre le code plus clair et plus maintenable.

---

## 🧠 2. Syntaxe d’une méthode en C\#

```csharp
[modificateur] typeRetour NomDeLaMéthode([paramètres])
{
    // instructions
    return valeur;
}
```

### 🔍 Exemple simple :

```csharp
static void DireBonjour()
{
    Console.WriteLine("Bonjour !");
}
```

### Et pour l’utiliser :

```csharp
DireBonjour();
```

---

## 🔁 3. Méthode avec paramètres

```csharp
static void Saluer(string nom)
{
    Console.WriteLine($"Bonjour {nom} !");
}
```

### Appel :

```csharp
Saluer("Ahmed");
```

---

## 🔙 4. Méthode avec valeur de retour

```csharp
static int Additionner(int a, int b)
{
    return a + b;
}
```

### Appel :

```csharp
int somme = Additionner(5, 3);
Console.WriteLine("Résultat : " + somme);
```

---

## 📥 5. Plusieurs types de retour possibles

| Type retour     | Exemple                             |
| --------------- | ----------------------------------- |
| `void`          | Pas de retour (`Console.WriteLine`) |
| `int`, `double` | Retourne un nombre                  |
| `string`        | Retourne une chaîne                 |
| `bool`          | Retourne vrai ou faux               |

---

## 📚 6. Surcharge de méthodes (Overloading)

Tu peux définir **plusieurs méthodes avec le même nom**, si les **paramètres sont différents** :

```csharp
static int Multiplier(int x, int y)
{
    return x * y;
}

static double Multiplier(double x, double y)
{
    return x * y;
}
```

---

## 🧩 7. Bonnes pratiques

* Les noms des méthodes commencent **par une majuscule** : `CalculerTotal`, `AfficherMenu`
* Une méthode doit faire **une seule chose** bien précise
* Utilise des noms **clairs** pour les paramètres

---

## ✅ Résumé du chapitre

| Élément        | Exemple                                |
| -------------- | -------------------------------------- |
| Méthode simple | `static void DireBonjour()`            |
| Avec paramètre | `static void Saluer(string nom)`       |
| Avec retour    | `static int Additionner(int a, int b)` |
| Appel          | `Saluer("Ali")`                        |
| Surcharge      | `Multiplier(int x, int y)` + `double`  |

---

## 🧪 Exercice proposé

Écris une méthode `EstPair(int nombre)` qui retourne `true` si le nombre est pair, `false` sinon.

```csharp
static bool EstPair(int nombre)
{
    return nombre % 2 == 0;
}
```