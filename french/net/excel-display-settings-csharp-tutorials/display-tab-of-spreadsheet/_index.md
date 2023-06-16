---
title: Afficher l'onglet de la feuille de calcul
linktitle: Afficher l'onglet de la feuille de calcul
second_title: Référence de l'API Aspose.Cells pour .NET
description: Affichez un onglet de feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 60
url: /fr/net/excel-display-settings-csharp-tutorials/display-tab-of-spreadsheet/
---
Dans ce didacticiel, nous allons vous montrer comment afficher l'onglet d'une feuille de calcul Excel à l'aide du code source C# avec Aspose.Cells pour .NET. Suivez les étapes ci-dessous pour obtenir le résultat souhaité.

## Étape 1 : Importer les bibliothèques nécessaires

Assurez-vous d'avoir installé la bibliothèque Aspose.Cells pour .NET et importez les bibliothèques nécessaires dans votre projet C#.

```csharp
using Aspose.Cells;
```

## Étape 2 : Définir le chemin du répertoire et ouvrir le fichier Excel

 Définissez le chemin d'accès au répertoire contenant votre fichier Excel, puis ouvrez le fichier en instanciant un`Workbook` objet.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Étape 3 : Afficher l'onglet de la feuille de calcul

 Utilisez le`ShowTabs` propriété de la`Workbook.Settings` objet pour afficher l'onglet de la feuille de calcul Excel.

```csharp
workbook.Settings.ShowTabs = true;
```

## Étape 4 : Enregistrer les modifications

 Une fois les modifications nécessaires effectuées, enregistrez le fichier Excel modifié à l'aide de la`Save` méthode de la`Workbook` objet.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Exemple de code source pour l'onglet Afficher de la feuille de calcul à l'aide de Aspose.Cells pour .NET 

```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciation d'un objet Workbook
// Ouverture du fichier Excel
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Masquer les onglets du fichier Excel
workbook.Settings.ShowTabs = true;
// Enregistrement du fichier Excel modifié
workbook.Save(dataDir + "output.xls");
```

### Conclusion

Ce guide étape par étape vous a montré comment afficher l'onglet d'une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. À l'aide du code source C# fourni, vous pouvez facilement personnaliser l'affichage des onglets dans vos fichiers Excel.

### Foire aux questions (FAQ)

#### Qu'est-ce qu'Aspose.Cells pour .NET ?

Aspose.Cells pour .NET est une bibliothèque puissante pour manipuler des fichiers Excel dans des applications .NET.

#### Comment puis-je installer Aspose.Cells pour .NET ?

 Pour installer Aspose.Cells pour .NET, vous devez télécharger le package correspondant à partir de[Aspose Communiqués](https://releases/aspose.com/cells/net/) et ajoutez-le à votre projet .NET.

#### Comment afficher l'onglet d'une feuille de calcul Excel en utilisant Aspose.Cells pour .NET ?

 Vous pouvez utiliser le`ShowTabs` propriété de la`Workbook.Settings` objet et réglez-le sur`true`pour afficher l'onglet de la feuille de calcul.

#### Quels autres formats de fichiers Excel sont pris en charge par Aspose.Cells pour .NET ?

Aspose.Cells pour .NET prend en charge une variété de formats de fichiers Excel, tels que XLS, XLSX, CSV, HTML, PDF, etc.
