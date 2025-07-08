# 📚 Chapitre 8 : Les Collections en C\#

---

## 🎯 1. Qu’est-ce qu’une collection ?

Une **collection** est une **structure de données** qui permet de stocker **plusieurs éléments** (comme une boîte contenant plusieurs objets).

🟢 En C#, on a plusieurs types de collections :

| Type              | Description                       |
| ----------------- | --------------------------------- |
| `Array`           | Tableau à taille fixe             |
| `List<T>`         | Liste dynamique (taille variable) |
| `Dictionary<K,V>` | Paires clé/valeur                 |

---

## 🧱 2. Les Tableaux (Arrays)

### 📦 Déclaration :

```csharp
int[] nombres = new int[3]; // Tableau de 3 entiers
nombres[0] = 10;
nombres[1] = 20;
nombres[2] = 30;
```

### 🧪 Accès :

```csharp
Console.WriteLine(nombres[1]); // Affiche 20
```

### 🔁 Parcourir un tableau :

```csharp
foreach (int n in nombres)
{
    Console.WriteLine(n);
}
```

---

## 📘 3. Les Listes (List<T>)

Plus flexibles que les tableaux, taille **dynamique**.

```csharp
using System.Collections.Generic;

List<string> fruits = new List<string>();
fruits.Add("Pomme");
fruits.Add("Banane");
fruits.Add("Orange");

foreach (string fruit in fruits)
{
    Console.WriteLine(fruit);
}
```

### Autres opérations :

```csharp
fruits.Remove("Banane");
bool contient = fruits.Contains("Pomme");
int taille = fruits.Count;
```

---

## 🧾 4. Les Dictionnaires (Dictionary\<K,V>)

Structure **clé-valeur** (comme un petit dictionnaire réel).

```csharp
Dictionary<string, int> ages = new Dictionary<string, int>();
ages.Add("Ahmed", 25);
ages["Sara"] = 30;

Console.WriteLine(ages["Ahmed"]); // Affiche 25
```

### Parcourir :

```csharp
foreach (KeyValuePair<string, int> element in ages)
{
    Console.WriteLine($"{element.Key} a {element.Value} ans.");
}
```

---

## 🛠️ 5. Comparaison rapide

| Collection        | Taille    | Accès     | Clés |
| ----------------- | --------- | --------- | ---- |
| `Array`           | Fixe      | Par index | ❌    |
| `List<T>`         | Dynamique | Par index | ❌    |
| `Dictionary<K,V>` | Dynamique | Par clé   | ✅    |

---

## 🧪 Exemple pratique :

Liste des noms et affichage trié :

```csharp
List<string> noms = new List<string>() { "Yassine", "Ahmed", "Khadija" };
noms.Sort();

foreach (var nom in noms)
{
    Console.WriteLine(nom);
}
```

---

## ✅ Résumé du chapitre

| Type         | Exemple                                |
| ------------ | -------------------------------------- |
| Tableau      | `int[] a = {1, 2, 3};`                 |
| Liste        | `List<string> l = new List<string>();` |
| Dictionnaire | `Dictionary<string, int> d = new...`   |
| Parcours     | `foreach (...) { ... }`                |

