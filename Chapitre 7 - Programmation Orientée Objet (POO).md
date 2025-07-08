# 🧱 Chapitre 7 : Programmation Orientée Objet (POO) en C\#

---

## 🧠 1. Qu’est-ce que la POO ?

La **programmation orientée objet** est un **paradigme de programmation** basé sur les **objets**.
Chaque objet représente une **entité réelle ou abstraite** (ex : personne, voiture, compte…).

### Elle repose sur 4 piliers :

1. **Encapsulation**
2. **Héritage**
3. **Polymorphisme**
4. **Abstraction**

---

## 🧩 2. Créer une classe simple

```csharp
class Personne
{
    // Attributs (champs)
    public string Nom;
    public int Age;

    // Méthode
    public void SePresenter()
    {
        Console.WriteLine($"Bonjour, je m'appelle {Nom} et j'ai {Age} ans.");
    }
}
```

---

## 👤 3. Créer et utiliser un objet

```csharp
Personne p1 = new Personne();
p1.Nom = "Ahmed";
p1.Age = 22;
p1.SePresenter();
```

---

## 🏗️ 4. Constructeur (méthode spéciale)

Permet d'**initialiser** un objet dès sa création :

```csharp
class Personne
{
    public string Nom;
    public int Age;

    public Personne(string nom, int age)
    {
        Nom = nom;
        Age = age;
    }

    public void SePresenter()
    {
        Console.WriteLine($"Je suis {Nom}, j’ai {Age} ans.");
    }
}
```

### Appel :

```csharp
Personne p2 = new Personne("Sara", 30);
p2.SePresenter();
```

---

## 🔐 5. Encapsulation (accès privé/public)

On peut cacher des données avec `private` et y accéder via des **getters/setters**.

```csharp
class CompteBancaire
{
    private double solde;

    public void Deposer(double montant)
    {
        solde += montant;
    }

    public double ObtenirSolde()
    {
        return solde;
    }
}
```

---

## 🧬 6. Héritage (Inheritance)

Permet à une classe d’**hériter** d’une autre classe.

```csharp
class Animal
{
    public void Manger()
    {
        Console.WriteLine("Je mange.");
    }
}

class Chien : Animal
{
    public void Aboyer()
    {
        Console.WriteLine("Wouf !");
    }
}
```

### Utilisation :

```csharp
Chien c = new Chien();
c.Manger();  // hérité
c.Aboyer();  // propre à Chien
```

---

## 🌀 7. Polymorphisme (surcharge & substitution)

### 🔹 Surcharge (overloading) : même nom, paramètres différents

```csharp
class Calculatrice
{
    public int Additionner(int a, int b) => a + b;
    public double Additionner(double a, double b) => a + b;
}
```

### 🔹 Substitution (override) : méthode redéfinie dans une classe dérivée

```csharp
class Animal
{
    public virtual void Crier()
    {
        Console.WriteLine("Cri d’animal");
    }
}

class Chat : Animal
{
    public override void Crier()
    {
        Console.WriteLine("Miaou !");
    }
}
```

---

## 🎓 Résumé du chapitre

| Concept       | Exemple                               |
| ------------- | ------------------------------------- |
| Classe        | `class Voiture { ... }`               |
| Objet         | `Voiture v = new Voiture();`          |
| Constructeur  | `public Voiture(string modele) {...}` |
| Encapsulation | `private`, `public`, getters/setters  |
| Héritage      | `class B : A`                         |
| Polymorphisme | `override`, `overload`                |

---

## 🧪 Exercice d’application

1. Crée une classe `Etudiant` avec :

   * Attributs : `Nom`, `Note`
   * Méthode `AfficherResultat()` qui affiche "Admis" si la note ≥ 10, sinon "Ajourné".
