# 🔁 Chapitre 5 : Les Boucles (Loops) en C\#

---

## 🎯 1. Pourquoi utiliser des boucles ?

Les **boucles** permettent de **répéter** une action plusieurs fois sans écrire le même code plusieurs fois.

مثلاً: طباعة الأرقام من 1 إلى 100، أو جمع عناصر جدول، أو انتظار إدخال صحيح من المستخدم.

---

## 🔄 2. La boucle `for`

### 📦 Syntaxe :

```csharp
for (initialisation; condition; incrément)
{
    // Instructions
}
```

### 🔍 Exemple :

```csharp
for (int i = 0; i < 5; i++)
{
    Console.WriteLine("i = " + i);
}
```

⏳ Ce code affiche :

```
i = 0
i = 1
i = 2
i = 3
i = 4
```

---

## 🔁 3. La boucle `while`

### 📦 Syntaxe :

```csharp
while (condition)
{
    // Instructions
}
```

### 🔍 Exemple :

```csharp
int i = 0;
while (i < 5)
{
    Console.WriteLine("i = " + i);
    i++;
}
```

---

## ♻️ 4. La boucle `do...while`

### 📦 Syntaxe :

```csharp
do
{
    // Instructions
}
while (condition);
```

### 🔍 Exemple :

```csharp
int i = 0;
do
{
    Console.WriteLine("i = " + i);
    i++;
}
while (i < 5);
```

🔎 Elle s’exécute **au moins une fois**, même si la condition est fausse.

---

## 📚 5. La boucle `foreach` (pour les collections)

Utilisée pour **parcourir des tableaux ou des listes**.

```csharp
string[] fruits = { "Pomme", "Banane", "Orange" };

foreach (string fruit in fruits)
{
    Console.WriteLine(fruit);
}
```

---

## ⛔ 6. Interruption de boucle : `break` et `continue`

### 🔴 `break` : quitte complètement la boucle

```csharp
for (int i = 0; i < 10; i++)
{
    if (i == 5)
        break;

    Console.WriteLine(i);
}
```

### 🟡 `continue` : passe à l’**itération suivante**

```csharp
for (int i = 0; i < 10; i++)
{
    if (i % 2 == 0)
        continue;

    Console.WriteLine(i); // Affiche seulement les nombres impairs
}
```

---

## ✅ Résumé du chapitre

| Type de boucle | Quand l'utiliser ?                             |
| -------------- | ---------------------------------------------- |
| `for`          | Nombre d’itérations connu                      |
| `while`        | Répéter tant qu’une condition est vraie        |
| `do...while`   | Même que `while`, mais exécute au moins 1 fois |
| `foreach`      | Parcourir un tableau, une liste, etc.          |
| `break`        | Interrompre la boucle                          |
| `continue`     | Passer à l’itération suivante                  |

---

## ✨ Exercice d'application

Affiche tous les nombres de 1 à 20 **sauf** ceux qui sont divisibles par 3 :

```csharp
for (int i = 1; i <= 20; i++)
{
    if (i % 3 == 0)
        continue;

    Console.WriteLine(i);
}
```
