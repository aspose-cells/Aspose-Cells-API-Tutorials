---
title: Afficher et masquer les en-têtes de colonne de ligne de la feuille de calcul
linktitle: Afficher et masquer les en-têtes de colonne de ligne de la feuille de calcul
second_title: Référence de l'API Aspose.Cells pour .NET
description: Affichez ou masquez les en-têtes de ligne et de colonne dans la feuille de calcul Excel à l'aide de Aspose.Cells pour .NET.
type: docs
weight: 40
url: /fr/net/excel-display-settings-csharp-tutorials/display-and-hide-row-column-headers-of-worksheet/
---
Dans ce didacticiel, nous allons vous montrer comment afficher ou masquer les en-têtes de ligne et de colonne d'une feuille de calcul Excel à l'aide du code source C# avec Aspose.Cells pour .NET. Suivez les étapes ci-dessous pour obtenir le résultat souhaité.

## Étape 1 : Importer les bibliothèques nécessaires

Assurez-vous d'avoir installé la bibliothèque Aspose.Cells pour .NET et importez les bibliothèques nécessaires dans votre projet C#.

```csharp
using Aspose.Cells;
using System.IO;
```

## Étape 2 : Définir le chemin du répertoire et ouvrir le fichier Excel

 Définissez le chemin d'accès au répertoire contenant votre fichier Excel, puis ouvrez le fichier en créant un flux de fichiers et en instanciant un`Workbook` objet.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Étape 3 : Accédez à la première feuille de calcul et masquez les en-têtes de ligne et de colonne

 Accédez à la première feuille de calcul du fichier Excel à l'aide de la`Worksheets` propriété de la`Workbook` objet. Utilisez ensuite le`IsRowColumnHeadersVisible` propriété de la`Worksheet` objet pour masquer les en-têtes de ligne et de colonne.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. IsRowColumnHeadersVisible = false;
```

## Étape 4 : Enregistrer les modifications

 Une fois les modifications nécessaires effectuées, enregistrez le fichier Excel modifié à l'aide de la`Save` méthode de la`Workbook` objet.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Exemple de code source pour afficher et masquer les en-têtes de colonne de ligne de la feuille de calcul à l'aide de Aspose.Cells pour .NET 
```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Création d'un flux de fichier contenant le fichier Excel à ouvrir
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciation d'un objet Workbook
// Ouverture du fichier Excel via le flux de fichiers
Workbook workbook = new Workbook(fstream);
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = workbook.Worksheets[0];
// Masquer les en-têtes de lignes et de colonnes
worksheet.IsRowColumnHeadersVisible = false;
// Enregistrement du fichier Excel modifié
workbook.Save(dataDir + "output.xls");
// Fermeture du flux de fichiers pour libérer toutes les ressources
fstream.Close(); 
```

## Conclusion

Ce guide étape par étape vous a montré comment afficher ou masquer les en-têtes de ligne et de colonne dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. À l'aide du code source C# fourni, vous pouvez facilement personnaliser l'affichage des en-têtes dans vos fichiers Excel.

### Foire aux questions (FAQ)

#### Qu'est-ce qu'Aspose.Cells pour .NET ?

Aspose.Cells pour .NET est une bibliothèque puissante pour manipuler des fichiers Excel dans des applications .NET.

#### Comment puis-je installer Aspose.Cells pour .NET ?

 Pour installer Aspose.Cells pour .NET, vous devez télécharger le package correspondant à partir de[Aspose Communiqués](https://releases/aspose.com/cells/net/) et ajoutez-le à votre projet .NET.

#### Comment puis-je afficher ou masquer les en-têtes de ligne et de colonne d'une feuille de calcul Excel avec Aspose.Cells pour .NET ?

 Vous pouvez utiliser le`IsRowColumnHeadersVisible` propriété de la`Worksheet`objet pour afficher ou masquer les en-têtes de ligne et de colonne. Réglez-le sur`true` pour les montrer et pour`false` pour les cacher.

#### Quels autres formats de fichiers Excel sont pris en charge par Aspose.Cells pour .NET ?

Aspose.Cells pour .NET prend en charge divers formats de fichiers Excel, tels que XLS, XLSX, CSV, HTML, PDF et bien d'autres.
