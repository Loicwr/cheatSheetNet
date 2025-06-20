# Tableau des différents types : 

| Catégorie             | Description de la catégorie                                                                      | Type C#           | Description détaillée                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------|-------------------|----------------------------------------------------------------------------------------|
| **Types valeur**      | Stockent directement les données. Situés sur la pile, plus rapides et non nullables par défaut.  | `int`             | Entier signé 32 bits. Plage : -2,147,483,648 à 2,147,483,647                           |
|                       |                                                                                                  | `float`           | Virgule flottante 32 bits. Moins précis que `double`, utile pour économiser la mémoire |
|                       |                                                                                                  | `double`          | Virgule flottante 64 bits. Par défaut pour les décimaux en C#                          |
|                       |                                                                                                  | `decimal`         | 128 bits, très haute précision, idéal pour calculs financiers                          |
|                       |                                                                                                  | `bool`            | Booléen. Peut valoir `true` ou `false`                                                 |
|                       |                                                                                                  | `char`            | Caractère Unicode 16 bits. Ex : `'A'`, `'é'`                                           |
|                       |                                                                                                  | `byte`            | Entier non signé 8 bits. Plage : 0 à 255                                               |
|                       |                                                                                                  | `sbyte`           | Entier signé 8 bits. Plage : -128 à 127                                                |
|                       |                                                                                                  | `short`           | Entier signé 16 bits                                                                   |
|                       |                                                                                                  | `ushort`          | Entier non signé 16 bits                                                               |
|                       |                                                                                                  | `long`            | Entier signé 64 bits                                                                   |
|                       |                                                                                                  | `ulong`           | Entier non signé 64 bits                                                               |
|                       |                                                                                                  | `enum`            | Type défini avec un ensemble de constantes nommées                                     |
|                       |                                                                                                  | `struct`          | Type composé personnalisé stocké par valeur                                            |
| **Types référence**   | Stockent une référence vers l’objet réel (situé dans le tas). Peuvent valoir `null`.             | `string`          | Chaîne de caractères Unicode immuable                                                  |
|                       |                                                                                                  | `object`          | Type de base universel de tous les types en C#                                         |
|                       |                                                                                                  | `class`           | Type complexe contenant des champs, méthodes, propriétés                               |
|                       |                                                                                                  | `interface`       | Contrat définissant des membres sans implémentation                                    |
|                       |                                                                                                  | `delegate`        | Pointeur vers une ou plusieurs méthodes (callback, événements)                         |
|                       |                                                                                                  | `array[]`         | Tableau de taille fixe contenant des éléments de même type                             |
|                       |                                                                                                  | `dynamic`         | Typé dynamiquement à l'exécution (non vérifié à la compilation)                        |
| **Types spéciaux**    | Types avancés facilitant l’écriture de code générique, flexible ou fonctionnel.                  | `var`             | Type implicite, inféré automatiquement à la compilation                                |
|                       |                                                                                                  | `int?`            | Type valeur nullable, permet d’avoir `null` pour un `int`                              |
|                       |                                                                                                  | `Tuple<T1, T2>`   | Conteneur de plusieurs valeurs regroupées sans créer un type dédié                     |
|                       |                                                                                                  | `Record`          | Type référence immuable, idéal pour modéliser des données (C# 9+)                      |
|                       |                                                                                                  | `anonymous`       | Objet créé à la volée avec des propriétés sans définir de type nommé                   |
| **Types génériques**  | Permettent la réutilisation de types avec des paramètres, tout en conservant la sécurité de type.| `List<T>`         | Liste générique redimensionnable                                                       |
|                       |                                                                                                  | `Dictionary<K,V>` | Structure de données clé/valeur fortement typée                                        |


# Mémoire : pile (stack) vs tas (heap) :
 
| Aspect                 | Pile (Stack)                                     | Tas (Heap)                                 |
|------------------------|--------------------------------------------------|--------------------------------------------|
| **Type de mémoire**    |Mémoire rapide, organisée en LIFO(pile d'appels)  |Mémoire plus lente, désorganisée, dynamique |
| **Contenu**            |Types valeur (int, bool ,...),pointeurs locaux    |Type référence (Objets, tableaux,string,...)|
| **Allocation**         |Automatique, très rapide                          |Gérée par le Garbage Collector              |
| **Durée de vie**       |Courte, liée au scope de la fonction              |Longue, tant qu'il y a une référence        |
| **Libération mémoire   |Automatique (quitte la pile à la fin du scope)    |Automatique par le garbage Collector (GC)   |
