---
title: Aperçu avant impression du classeur
linktitle: Aperçu avant impression du classeur
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment générer un aperçu avant impression d'un classeur à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 170
url: /fr/net/excel-workbook/workbook-print-preview/
---
L'aperçu avant impression d'un classeur est une fonctionnalité essentielle lorsque vous travaillez avec des fichiers Excel avec Aspose.Cells pour .NET. Vous pouvez facilement générer un aperçu avant impression en suivant ces étapes :

## Étape 1 : Spécifiez le répertoire source

Tout d'abord, vous devez spécifier le répertoire source où se trouve le fichier Excel que vous souhaitez prévisualiser. Voici comment procéder :

```csharp
// répertoire des sources
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Étape 2 : charger le classeur

Ensuite, vous devez charger le classeur Workbook à partir du fichier Excel spécifié. Voici comment procéder :

```csharp
// Charger le classeur Workbook
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Étape 3 : Configurer les options d'image et d'impression

Avant de générer l'aperçu avant impression, vous pouvez configurer l'image et les options d'impression selon vos besoins. Dans cet exemple, nous utilisons les options par défaut. Voici comment procéder :

```csharp
// Options d'image et d'impression
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Étape 4 : générer l'aperçu avant impression du classeur

Vous pouvez maintenant générer l'aperçu avant impression du classeur Workbook à l'aide de la classe WorkbookPrintingPreview. Voici comment procéder :

```csharp
// Aperçu avant impression du classeur
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Étape 5 : générer l'aperçu avant impression de la feuille de calcul

Si vous souhaitez générer l'aperçu avant impression d'une feuille de calcul spécifique, vous pouvez utiliser la classe SheetPrintingPreview. Voici un exemple :

```csharp
// Aperçu avant impression de la feuille de calcul
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Exemple de code source pour l'aperçu avant impression du classeur à l'aide d'Aspose.Cells pour .NET 
```csharp
//Répertoire des sources
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Conclusion

La génération de l'aperçu avant impression d'un classeur est une fonctionnalité puissante offerte par Aspose.Cells pour .NET. En suivant les étapes ci-dessus, vous pouvez facilement prévisualiser votre classeur Excel et obtenir des informations sur le nombre de pages à imprimer.

### FAQ

#### Q : Comment puis-je spécifier un répertoire source différent pour charger mon classeur ?
    
 R : Vous pouvez utiliser le`Set_SourceDirectory` méthode pour spécifier un répertoire source différent. Par exemple:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### Q : Puis-je personnaliser l'image et les options d'impression lors de la génération de l'aperçu avant impression ?
    
 R : Oui, vous pouvez personnaliser les options d'image et d'impression en modifiant les propriétés du`ImageOrPrintOptions` objet. Par exemple, vous pouvez définir la résolution de l'image, le format du fichier de sortie, etc.

#### Q : Est-il possible de générer un aperçu avant impression pour plusieurs feuilles de calcul dans un classeur ?
    
R : Oui, vous pouvez parcourir les différentes feuilles de calcul du classeur et générer un aperçu avant impression pour chaque feuille à l'aide de l'outil`SheetPrintingPreview` classe.

#### Q : Comment enregistrer l'aperçu avant impression sous forme d'image ou de fichier PDF ?
    
 R : Vous pouvez utiliser`ToImage` ou`ToPdf` méthode de`WorkbookPrintingPreview` ou`SheetPrintingPreview` objet pour enregistrer l'aperçu avant impression sous forme d'image ou de fichier PDF.

#### Q : Que puis-je faire avec l'aperçu avant impression une fois généré ?
    
R : Une fois que vous avez généré l'aperçu avant impression, vous pouvez l'afficher à l'écran, l'enregistrer sous forme d'image ou de fichier PDF, ou l'utiliser pour d'autres opérations telles que l'envoi par e-mail ou l'impression.
	