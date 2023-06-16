---
title: Copier les paramètres de mise en page à partir d'une autre feuille de calcul
linktitle: Copier les paramètres de mise en page à partir d'une autre feuille de calcul
second_title: Référence de l'API Aspose.Cells pour .NET
description: Apprenez à copier les paramètres de configuration de page d'une feuille de calcul à une autre à l'aide d'Aspose.Cells pour .NET. Un guide étape par étape pour optimiser l'utilisation de cette bibliothèque.
type: docs
weight: 10
url: /fr/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
Dans cet article, nous vous guiderons pas à pas pour expliquer le code source C# suivant : Copiez les paramètres de configuration de la page à partir d'une autre feuille de calcul à l'aide d'Aspose.Cells pour .NET. Nous utiliserons la bibliothèque Aspose.Cells pour .NET pour effectuer cette opération. Si vous souhaitez copier les paramètres de mise en page d'une feuille de calcul à une autre, suivez les étapes ci-dessous.

## Étape 1 : Création du classeur
La première étape consiste à créer un classeur. Dans notre cas, nous utiliserons la classe Workbook fournie par la bibliothèque Aspose.Cells. Voici le code pour créer un classeur :

```csharp
Workbook wb = new Workbook();
```

## Étape 2 : Ajouter des feuilles de calcul de test
Après avoir créé le classeur, nous devons ajouter des feuilles de calcul de test. Dans cet exemple, nous allons ajouter deux feuilles de calcul. Voici le code pour ajouter deux feuilles de calcul :

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Étape 3 : Accéder aux feuilles de calcul
Maintenant que nous avons ajouté les feuilles de calcul, nous devons y accéder pour pouvoir modifier leurs paramètres. Nous accéderons aux feuilles de calcul "TestSheet1" et "TestSheet2" en utilisant leurs noms. Voici le code pour y accéder :

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Étape 4 : Définition du format de papier
 Dans cette étape, nous allons définir le format de papier de la feuille de calcul "TestSheet1". Nous utiliserons le`PageSetup.PaperSize` propriété pour définir la taille du papier. Par exemple, nous définirons le format de papier sur "PaperA3ExtraTransverse". Voici le code pour cela :

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Étape 5 : copie des paramètres de mise en page
 Nous allons maintenant copier les paramètres de configuration de la page de la feuille de calcul "TestSheet1" vers "TestSheet2". Nous utiliserons le`PageSetup.Copy` méthode pour effectuer cette opération. Voici le code pour cela :

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Étape 6 : Formats de papier d'impression
 Après avoir copié les paramètres de mise en page, nous imprimerons les formats de papier des deux feuilles de calcul. Nous utiliserons`Console.WriteLine` pour afficher les formats de papier. Voici le code pour cela :

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Exemple de code source pour Copier les paramètres de configuration de la page à partir d'une autre feuille de calcul à l'aide d'Aspose.Cells pour .NET 
```csharp
//Créer un classeur
Workbook wb = new Workbook();
//Ajouter deux feuilles de test
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Accéder aux deux feuilles de calcul en tant que TestSheet1 et TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Définissez la taille du papier de TestSheet1 sur PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Imprimer la taille du papier des deux feuilles de calcul
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Copiez le PageSetup de TestSheet1 à TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Imprimer la taille du papier des deux feuilles de calcul
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Conclusion
Dans cet article, nous avons appris à copier les paramètres de configuration de page d'une feuille de calcul à une autre à l'aide d'Aspose.Cells pour .NET. Nous avons suivi les étapes suivantes : création du classeur, ajout de feuilles de calcul de test, accès aux feuilles de calcul, définition du format de papier, copie des paramètres de mise en page et impression des formats de papier. Vous pouvez maintenant utiliser ces connaissances pour copier les paramètres de configuration de la page dans vos propres projets.

### FAQ

Q : Puis-je copier les paramètres de configuration de page entre différentes instances de classeur ?

 R : Oui, vous pouvez copier les paramètres de mise en page entre différentes instances de classeur à l'aide de l'outil`PageSetup.Copy` méthode de la bibliothèque Aspose.Cells.

Q : Puis-je copier d'autres paramètres de mise en page, comme l'orientation ou les marges ?

 R : Oui, vous pouvez copier d'autres paramètres de configuration de page à l'aide de`PageSetup.Copy` méthode avec les options appropriées. Par exemple, vous pouvez copier l'orientation à l'aide de`CopyOptions.Orientation` et les marges en utilisant`CopyOptions.Margins`.

: Comment savoir quelles options sont disponibles pour le format de papier ?

 R : Vous pouvez consulter la référence de l'API de la bibliothèque Aspose.Cells pour connaître les options disponibles pour la taille du papier. Il existe une énumération appelée`PaperSizeType` qui répertorie les différents formats de papier pris en charge.

Q : Comment puis-je télécharger la bibliothèque Aspose.Cells pour .NET ?

 R : Vous pouvez télécharger la bibliothèque Aspose.Cells pour .NET à partir de[Aspose Communiqués](https://releases.aspose.com/cells/net). Des versions d'essai gratuites sont disponibles, ainsi que des licences payantes à usage commercial.

Q : La bibliothèque Aspose.Cells prend-elle en charge d'autres langages de programmation ?

R : Oui, la bibliothèque Aspose.Cells prend en charge plusieurs langages de programmation, notamment C#, Java, Python et bien d'autres.