---
title: Contrôler le facteur de zoom de la feuille de calcul
linktitle: Contrôler le facteur de zoom de la feuille de calcul
second_title: Référence de l'API Aspose.Cells pour .NET
description: Contrôlez le facteur de zoom de la feuille de calcul Excel avec Aspose.Cells pour .NET.
type: docs
weight: 20
url: /fr/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
Le contrôle du facteur de zoom d'une feuille de calcul est une fonctionnalité essentielle lorsque vous travaillez avec des fichiers Excel à l'aide de la bibliothèque Aspose.Cells pour .NET. Dans ce guide, nous allons vous montrer comment utiliser Aspose.Cells pour contrôler étape par étape le facteur de zoom d'une feuille de calcul à l'aide du code source C#.

## Étape 1 : Importer les bibliothèques requises

Avant de commencer, assurez-vous d'avoir installé la bibliothèque Aspose.Cells pour .NET et importez les bibliothèques nécessaires dans votre projet C#.

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## Étape 2 : Définir le chemin du répertoire et ouvrir le fichier Excel

 Pour commencer, définissez le chemin du répertoire contenant votre fichier Excel, puis ouvrez-le à l'aide d'un`FileStream` objet et instancier un`Workbook` objet pour représenter le classeur Excel.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Étape 3 : accédez à la feuille de calcul et modifiez le facteur de zoom

Dans cette étape, nous accédons à la première feuille de calcul du classeur Excel en utilisant l'index`0` et définissez le facteur de zoom de la feuille de calcul sur`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## Étape 4 : Enregistrez les modifications et fermez le fichier

 Une fois que nous avons modifié le facteur de zoom de la feuille de calcul, nous enregistrons les modifications dans le fichier Excel à l'aide du`Save` méthode du`Workbook` objet. Ensuite, nous fermons le flux de fichiers pour libérer toutes les ressources utilisées.

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### Exemple de code source pour Controll Zoom Factor Of Worksheet à l'aide d'Aspose.Cells pour .NET 

```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Création d'un flux de fichiers contenant le fichier Excel à ouvrir
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciation d'un objet Workbook
// Ouverture du fichier Excel via le flux de fichiers
Workbook workbook = new Workbook(fstream);
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = workbook.Worksheets[0];
// Définir le facteur de zoom de la feuille de calcul sur 75
worksheet.Zoom = 75;
// Sauvegarde du fichier Excel modifié
workbook.Save(dataDir + "output.xls");
// Fermeture du flux de fichiers pour libérer toutes les ressources
fstream.Close();
```

## Conclusion

Ce guide étape par étape vous a montré comment contrôler le facteur de zoom d'une feuille de calcul à l'aide d'Aspose.Cells pour .NET. À l'aide du code source C# fourni, vous pouvez facilement ajuster le facteur de zoom d'une feuille de calcul dans vos applications .NET.

### Foire aux questions (FAQ)

#### Qu’est-ce qu’Aspose.Cells pour .NET ?

Aspose.Cells for .NET est une bibliothèque de classement riche en fonctionnalités permettant de manipuler des fichiers Excel dans des applications .NET.

#### Comment puis-je installer Aspose.Cells pour .NET ?

 Pour installer Aspose.Cells pour .NET, vous devez télécharger le package NuGet correspondant à partir de[Aspose les versions](https://releases/aspose.com/cells/net/) et ajoutez-le à votre projet .NET.

#### Quelles fonctionnalités Aspose.Cells pour .NET offre-t-il ?

Aspose.Cells pour .NET offre des fonctionnalités telles que la création, l'édition, la conversion et la manipulation avancée de fichiers Excel.

#### Quels formats de fichiers sont pris en charge par Aspose.Cells pour .NET ?

Aspose.Cells for .NET prend en charge plusieurs formats de fichiers, notamment XLSX, XLSM, CSV, HTML, PDF et bien d'autres.
