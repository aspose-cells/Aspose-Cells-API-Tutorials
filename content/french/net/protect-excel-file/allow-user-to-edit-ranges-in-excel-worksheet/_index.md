---
title: Autoriser l'utilisateur à modifier des plages dans une feuille de calcul Excel
linktitle: Autoriser l'utilisateur à modifier des plages dans une feuille de calcul Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Autorisez les utilisateurs à modifier des plages spécifiques dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Guide étape par étape avec le code source en C#.
type: docs
weight: 10
url: /fr/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
Dans ce guide, nous vous expliquerons comment utiliser Aspose.Cells pour .NET pour permettre à l'utilisateur de modifier des plages spécifiques dans une feuille de calcul Excel. Suivez les étapes ci-dessous pour accomplir cette tâche.

## Étape 1 : Configuration de l'environnement

Assurez-vous d'avoir configuré votre environnement de développement et installé Aspose.Cells pour .NET. Vous pouvez télécharger la dernière version de la bibliothèque sur le site officiel d'Aspose.

## Étape 2 : Importer les espaces de noms requis

Dans votre projet C#, importez les espaces de noms nécessaires pour travailler avec Aspose.Cells :

```csharp
using Aspose.Cells;
```

## Étape 3 : Définition du chemin d'accès au répertoire des documents

 Déclarer un`dataDir` variable pour spécifier le chemin d'accès au répertoire dans lequel vous souhaitez enregistrer le fichier Excel généré :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assurez-vous de remplacer`"YOUR_DOCUMENT_DIRECTORY"` avec le chemin correct sur votre système.

## Étape 4 : Création d'un objet classeur

Instanciez un nouvel objet Workbook qui représente le classeur Excel que vous souhaitez créer :

```csharp
Workbook book = new Workbook();
```

## Étape 5 : Accès à la première feuille de calcul

Accédez à la première feuille de calcul du classeur Excel à l'aide du code suivant :

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Étape 6 : Récupération des plages de modifications autorisées

 Obtenez la collection de plages d'édition autorisées à l'aide de l'outil`AllowEditRanges` propriété:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Étape 7 : Définir une plage protégée

 Définissez une plage protégée à l'aide du`Add` méthode du`AllowEditRanges` collection:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Ici, nous avons créé une plage protégée « r2 » qui s'étend de la cellule A1 à la cellule C3.

## Étape 8 : Spécification du mot de passe

 Spécifiez un mot de passe pour la plage protégée à l'aide du`Password` propriété:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Assurez-vous de remplacer`"YOUR_PASSWORD"` avec le mot de passe souhaité.

## Étape 9 : Protection de la feuille de calcul

 Protégez la feuille de calcul à l'aide du`Protect` méthode du`Worksheet` objet:

```csharp
sheet.Protect(ProtectionType.All);
```

Cela protégera la feuille de calcul en empêchant toute modification en dehors des plages autorisées.

## Étape 10 : Enregistrement du

  fichier Excel

 Enregistrez le fichier Excel généré à l'aide du`Save` méthode du`Workbook` objet:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Assurez-vous de spécifier le nom du fichier souhaité et le chemin correct.

### Exemple de code source pour Autoriser l'utilisateur à modifier des plages dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET 
```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Créez un répertoire s'il n'est pas déjà présent.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Instancier un nouveau classeur
Workbook book = new Workbook();
// Obtenir la première feuille de calcul (par défaut)
Worksheet sheet = book.Worksheets[0];
// Obtenez les plages de modification autorisées
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// Définir ProtectedRange
ProtectedRange proteced_range;
// Créer la gamme
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// Spécifiez le mot de passe
proteced_range.Password = "123";
// Protéger la feuille
sheet.Protect(ProtectionType.All);
// Enregistrez le fichier Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## Conclusion

Vous avez maintenant appris à utiliser Aspose.Cells pour .NET pour permettre à l'utilisateur de modifier des plages spécifiques dans une feuille de calcul Excel. N'hésitez pas à explorer davantage les fonctionnalités offertes par Aspose.Cells pour répondre à vos besoins spécifiques.


### FAQ

#### 1. Comment permettre à l'utilisateur de modifier des plages spécifiques dans une feuille de calcul Excel ?

 Vous pouvez utiliser le`ProtectedRangeCollection` classe pour définir les plages de modification autorisées. Utilisez le`Add` méthode pour créer une nouvelle plage protégée avec les cellules souhaitées.

#### 2. Puis-je définir un mot de passe pour les plages de modifications autorisées ?

 Oui, vous pouvez spécifier un mot de passe à l'aide du`Password` propriété du`ProtectedRange` objet. Cela limitera l'accès uniquement aux utilisateurs disposant du mot de passe.

#### 3. Comment protéger la feuille de calcul une fois les plages autorisées définies ?

 Utilisez le`Protect` méthode du`Worksheet` objet pour protéger la feuille de calcul. Cela empêchera toute modification en dehors des plages autorisées, et éventuellement vous demandera un mot de passe si vous en avez spécifié un.