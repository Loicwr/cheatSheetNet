# 🧠 C# Cheatsheet – Branches Conditionnelles

## 🔹 `if`, `else if`, `else`

Permet d'exécuter des blocs de code selon une ou plusieurs conditions.

```csharp
if (condition1)
{
    // Exécuté si condition1 est vraie
}
else if (condition2)
{
    // Exécuté si condition2 est vraie
}
else
{
    // Exécuté si aucune condition précédente n’est vraie
}
```

**Exemple :**
```csharp
int age = 20;
if (age < 18)
{
    Console.WriteLine("Mineur");
}
else if (age < 65)
{
    Console.WriteLine("Adulte");
}
else
{
    Console.WriteLine("Senior");
}
```

---

## 🔹 Opérateur ternaire `?:`

Expression compacte équivalente à `if/else`.

```csharp
type variable = (condition) ? valeur_si_vrai : valeur_si_faux;
```

**Exemple :**
```csharp
int age = 20;
string statut = (age < 18) ? "Mineur" : "Majeur";
Console.WriteLine(statut);
```

---

## 🔹 `switch`

Choisit un bloc de code en fonction de la valeur d’une expression.

```csharp
switch (expression)
{
    case valeur1:
        // instructions
        break;
    case valeur2:
        // instructions
        break;
    default:
        // instructions si aucune valeur ne correspond
        break;
}
```

**Exemple :**
```csharp
string role = "admin";

switch (role)
{
    case "admin":
        Console.WriteLine("Accès complet");
        break;
    case "utilisateur":
        Console.WriteLine("Accès limité");
        break;
    default:
        Console.WriteLine("Rôle inconnu");
        break;
}
```

---

## 🔹 `switch` avec `when` (filtrage par condition)

Disponible depuis C# 7+.

```csharp
switch (variable)
{
    case int n when (n < 0):
        Console.WriteLine("Négatif");
        break;
    case int n when (n == 0):
        Console.WriteLine("Zéro");
        break;
    default:
        Console.WriteLine("Positif");
        break;
}
```

---

## ✅ Bonnes pratiques

- Préférez `switch` pour plusieurs cas basés sur une seule variable.
- Utilisez l’opérateur ternaire pour des affectations simples.
- Attention à toujours utiliser `break` dans un `switch` pour éviter le "fall-through".

---

## 🧾 Récapitulatif des Structures Conditionnelles

| Structure             | Description                                 | Exemple clé                        |
|-----------------------|---------------------------------------------|------------------------------------|
| `if / else if / else` | Choix selon conditions multiples            | `if (x > 0) {...}`                 |
| `switch`              | Choix selon une valeur unique               | `switch (x) { case 1: ... }`       |
| `?:` (ternaire)       | Affectation conditionnelle simple           | `string res = (x > 0) ? "P" : "N"` |
| `switch when`         | `switch` avec condition spécifique          | `case int n when (n < 0):`         |
