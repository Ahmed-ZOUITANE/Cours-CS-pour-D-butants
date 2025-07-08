# 🌟 Cours C# pour Débutants

## 🔰 Chapitre 1 : Introduction au C\#

### Qu'est-ce que C# ?

* Langage de programmation orienté objet développé par Microsoft.
* Utilisé principalement avec la plateforme .NET pour développer des applications desktop, web, mobile, et jeux (avec Unity).

---

## 📦 Chapitre 2 : Premier programme C\#

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Bonjour, le monde !");
    }
}
```

### Explication :

* `using System;` : importe l’espace de noms `System`.
* `Main()` : point d'entrée du programme.
* `Console.WriteLine()` : affiche du texte dans la console.

---

## 🧮 Chapitre 3 : Variables et Types de Données

| Type     | Description          | Exemple                |
| -------- | -------------------- | ---------------------- |
| `int`    | Nombre entier        | `int x = 10;`          |
| `double` | Nombre décimal       | `double y = 3.14;`     |
| `char`   | Caractère            | `char c = 'A';`        |
| `string` | Chaîne de caractères | `string name = "Ali";` |
| `bool`   | Booléen (true/false) | `bool isTrue = true;`  |

---

## 🔄 Chapitre 4 : Conditions (if / else / switch)

```csharp
int age = 20;
if (age >= 18)
{
    Console.WriteLine("Majeur");
}
else
{
    Console.WriteLine("Mineur");
}
```

---

## 🔁 Chapitre 5 : Boucles (for, while)

```csharp
for (int i = 1; i <= 5; i++)
{
    Console.WriteLine("Nombre : " + i);
}
```

---

## 🧰 Chapitre 6 : Fonctions (Méthodes)

```csharp
static void DireBonjour(string nom)
{
    Console.WriteLine("Bonjour " + nom);
}
```

Appel :

```csharp
DireBonjour("Ahmed");
```

---

## 🧱 Chapitre 7 : Programmation Orientée Objet (POO)

### Exemple simple de classe :

```csharp
class Personne
{
    public string Nom;
    
    public void Parler()
    {
        Console.WriteLine("Bonjour, je suis " + Nom);
    }
}
```

### Utilisation :

```csharp
Personne p = new Personne();
p.Nom = "Ahmed";
p.Parler();
```

---

## 🧪 Chapitre 8 : Projets pratiques

* 🎲 Deviner un nombre aléatoire.
* 🧮 Mini-calculatrice.
* 📋 Application de gestion d’étudiants (avec liste).

