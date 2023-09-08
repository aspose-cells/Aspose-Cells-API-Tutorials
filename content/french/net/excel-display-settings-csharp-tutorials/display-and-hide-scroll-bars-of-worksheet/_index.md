---
title: Afficher et masquer les barres de défilement de la feuille de calcul
linktitle: Afficher et masquer les barres de défilement de la feuille de calcul
second_title: Référence de l'API Aspose.Cells pour .NET
description: Affichez ou masquez les barres de défilement dans la feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 50
url: /fr/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
Dans ce didacticiel, nous allons vous montrer comment afficher ou masquer les barres de défilement verticales et horizontales dans une feuille de calcul Excel à l'aide du code source C# avec Aspose.Cells pour .NET. Suivez les étapes ci-dessous pour obtenir le résultat souhaité.

## Étape 1 : Importez les bibliothèques nécessaires

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

## Étape 3 : Masquer les barres de défilement

 Utilisez le`IsVScrollBarVisible` et`IsHScrollBarVisible` propriétés du`Workbook.Settings` objet pour masquer les barres de défilement verticales et horizontales de la feuille de calcul.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## Étape 4 : Enregistrer les modifications

 Une fois que vous avez apporté les modifications nécessaires, enregistrez le fichier Excel modifié à l'aide du`Save` méthode du`Workbook` objet.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Exemple de code source pour afficher et masquer les barres de défilement d'une feuille de calcul à l'aide d'Aspose.Cells pour .NET 

```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Création d'un flux de fichiers contenant le fichier Excel à ouvrir
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciation d'un objet Workbook
// Ouverture du fichier Excel via le flux de fichiers
Workbook workbook = new Workbook(fstream);
// Masquer la barre de défilement verticale du fichier Excel
workbook.Settings.IsVScrollBarVisible = false;
// Masquer la barre de défilement horizontale du fichier Excel
workbook.Settings.IsHScrollBarVisible = false;
// Sauvegarde du fichier Excel modifié
workbook.Save(dataDir + "output.xls");
// Fermeture du flux de fichiers pour libérer toutes les ressources
fstream.Close();
```

### Conclusion

Ce guide étape par étape vous a montré comment afficher ou masquer les barres de défilement verticales et horizontales dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. À l'aide du code source C# fourni, vous pouvez facilement personnaliser l'affichage des barres de défilement dans vos fichiers Excel.

### Foire aux questions (FAQ)

#### Qu’est-ce qu’Aspose.Cells pour .NET ?

Aspose.Cells for .NET est une puissante bibliothèque permettant de manipuler des fichiers Excel dans des applications .NET.

#### Comment puis-je installer Aspose.Cells pour .NET ?

 Pour installer Aspose.Cells pour .NET, vous devez télécharger le package correspondant à partir de[Aspose les versions](https://releases/aspose.com/cells/net/) et ajoutez-le à votre projet .NET.

#### Comment puis-je afficher ou masquer les barres de défilement dans une feuille de calcul Excel avec Aspose.Cells pour .NET ?

 Vous pouvez utiliser le`IsVScrollBarVisible` et`IsHScrollBarVisible` propriétés du`Workbook.Settings` objet pour afficher ou masquer respectivement la barre de défilement verticale et horizontale dans une feuille de calcul Excel.

#### Quels autres formats de fichiers Excel sont pris en charge par Aspose.Cells pour .NET ?

Aspose.Cells for .NET prend en charge une variété de formats de fichiers Excel, tels que XLS, XLSX, CSV, HTML, PDF, etc.