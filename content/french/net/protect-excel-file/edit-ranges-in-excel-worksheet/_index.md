---
title: Modifier les plages dans la feuille de calcul Excel
linktitle: Modifier les plages dans la feuille de calcul Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Apprenez à modifier des plages spécifiques dans une feuille de calcul Excel avec Aspose.Cells pour .NET. Tutoriel pas à pas en C#.
type: docs
weight: 20
url: /fr/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
Microsoft Excel est un puissant outil de création et de gestion de tableurs, offrant de nombreuses fonctionnalités pour contrôler et sécuriser les données. L'une de ces fonctionnalités consiste à permettre aux utilisateurs de modifier des plages spécifiques dans une feuille de calcul tout en protégeant les autres parties. Dans ce didacticiel, nous vous guiderons étape par étape pour implémenter cette fonctionnalité à l'aide d'Aspose.Cells pour .NET, une bibliothèque populaire pour travailler avec des fichiers Excel par programmation.

L'utilisation d'Aspose.Cells pour .NET vous permettra de manipuler facilement des plages dans une feuille de calcul Excel, offrant une interface conviviale et des fonctionnalités avancées. Suivez les étapes ci-dessous pour permettre aux utilisateurs de modifier des plages spécifiques dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET.
## Étape 1 : Configurer l'environnement

Assurez-vous que Aspose.Cells pour .NET est installé dans votre environnement de développement. Téléchargez la bibliothèque sur le site officiel d'Aspose et consultez la documentation pour les instructions d'installation.

## Étape 2 : Initialisation du classeur et de la feuille de calcul

Pour commencer, nous devons créer un nouveau classeur et obtenir la référence à la feuille de calcul dans laquelle nous voulons autoriser la modification des plages. Utilisez le code suivant pour y parvenir :

```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Créez le répertoire s'il n'existe pas déjà.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Instancier un nouveau classeur
Workbook workbook = new Workbook();

// Obtenir la première feuille de calcul (par défaut)
Worksheet sheet = workbook.Worksheets[0];
```

 Dans cet extrait de code, nous définissons d'abord le chemin d'accès au répertoire où le fichier Excel sera enregistré. Ensuite, nous créons une nouvelle instance de`Workbook` classe et obtenir la référence à la première feuille de calcul en utilisant le`Worksheets` propriété.

## Étape 3 : Obtenir des plages modifiables

Nous devons maintenant récupérer les plages dans lesquelles nous voulons autoriser la modification. Utilisez le code suivant :

```csharp
// Obtenir les plages modifiables
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## Étape 4 : Définir la plage protégée

Avant d'autoriser la modification des plages, nous devons définir une plage protégée. Voici comment:

```csharp
// Définir une plage protégée
ProtectedRange ProtectedRange;

// Créer la gamme
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

 Dans ce code, nous créons une nouvelle instance de`ProtectedRange` classe et utiliser le`Add` méthode pour spécifier la plage à protéger.

## Étape 5 : Spécifiez le mot de passe

Pour renforcer la sécurité, vous pouvez spécifier un mot de passe pour la plage protégée. Voici comment:

```csharp
// Spécifiez le mot de passe
protectedBeach.Password = "YOUR_PASSWORD";
```

## Étape 6 : Protégez la feuille de calcul

Maintenant que nous avons défini la plage protégée, nous pouvons protéger la feuille de calcul pour empêcher toute modification non autorisée. Utilisez le code suivant :

```csharp
// Protéger la feuille de calcul
leaf.Protect(ProtectionType.All);
```

## Étape 7 : Enregistrez le fichier Excel

Enfin, nous enregistrons le fichier Excel avec les modifications apportées. Voici le code nécessaire :

```csharp
// Enregistrez le fichier Excel
workbook.Save(dataDir + "protectedrange.out.xls");
```

### Exemple de code source pour Modifier les plages dans la feuille de calcul Excel à l'aide de Aspose.Cells pour .NET 
```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Créez un répertoire s'il n'est pas déjà présent.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// Instancier un nouveau classeur
Workbook book = new Workbook();

// Obtenir la première feuille de calcul (par défaut)
Worksheet sheet = book.Worksheets[0];

// Obtenir les plages de modification autorisées
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;

// Définir la plage protégée
ProtectedRange proteced_range;

// Créer la gamme
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];

// Spécifiez le mot de passe
proteced_range.Password = "YOUR_PASSWORD";

// Protégez la feuille
sheet.Protect(ProtectionType.All);

// Enregistrez le fichier Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## Conclusion

Félicitation ! Vous avez appris à autoriser les utilisateurs à modifier des plages spécifiques dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Vous pouvez maintenant appliquer cette technique dans vos propres projets et améliorer la sécurité de vos fichiers Excel.


#### FAQ

#### Q : Pourquoi devrais-je utiliser Aspose.Cells pour .NET pour modifier des plages dans une feuille de calcul Excel ?

R : Aspose.Cells pour .NET offre une API puissante et facile à utiliser pour travailler avec des fichiers Excel. Il fournit des fonctionnalités avancées, telles que la manipulation des plages, la protection des feuilles de calcul, etc.

#### Q : Puis-je définir plusieurs plages modifiables dans une feuille de calcul ?

 R : Oui, vous pouvez définir plusieurs plages modifiables à l'aide de la`Add` méthode de la`ProtectedRangeCollection` collection. Chaque plage peut avoir ses propres paramètres de protection.

####  Q : Est-il possible de supprimer une plage modifiable après l'avoir définie ?

 R : Oui, vous pouvez utiliser le`RemoveAt` méthode de la`ProtectedRangeCollection` collection pour supprimer une plage modifiable spécifique en spécifiant son index.

#### Q : Comment puis-je ouvrir le fichier Excel protégé après l'avoir enregistré ?

: Vous devrez fournir le mot de passe spécifié lors de la création de la plage protégée pour ouvrir le fichier Excel protégé. Veillez à conserver le mot de passe dans un endroit sûr pour éviter toute perte d'accès aux données.