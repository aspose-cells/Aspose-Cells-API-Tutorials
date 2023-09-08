---
title: Feuille de calcul de copie Excel
linktitle: Feuille de calcul de copie Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Copiez une feuille de calcul Excel sur une autre avec Aspose.Cells pour .NET.
type: docs
weight: 20
url: /fr/net/excel-copy-worksheet/excel-copy-worksheet/
---

Dans ce guide, nous expliquerons comment copier une feuille de calcul Excel à l'aide de la bibliothèque Aspose.Cells pour .NET. Nous vous fournirons le code source C# et vous guiderons à travers les étapes nécessaires pour accomplir cette tâche. A la fin, nous vous montrerons le résultat attendu. Suivez les instructions ci-dessous pour commencer.

## Étape 1 : Préparation

Avant de commencer, assurez-vous d'avoir installé Aspose.Cells pour .NET et créé un projet C# dans votre environnement de développement intégré (IDE) préféré. Assurez-vous également d'avoir une copie du fichier Excel que vous souhaitez manipuler.

## Étape 2 : Importer les bibliothèques requises

 Dans votre fichier source C#, importez les bibliothèques nécessaires depuis Aspose.Cells à l'aide du`using` directif:

```csharp
using Aspose.Cells;
```

## Étape 3 : Définir le chemin du fichier

 Déclarer un`dataDir` variable et initialisez-la avec le répertoire contenant votre fichier Excel. Par exemple :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Assurez-vous de remplacer`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` avec le chemin réel de votre répertoire.

## Étape 4 : Charger le fichier Excel existant

 Utilisez le`Workbook` classe d’Aspose.Cells pour ouvrir le fichier Excel existant. Utilisez le`InputPath` variable pour spécifier le chemin du fichier :

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Assurez-vous d'avoir remplacé`"book1.xls"` avec le nom réel de votre fichier Excel.

## Étape 5 : Copiez la feuille de calcul

 Nous allons maintenant copier la feuille de calcul existante dans une nouvelle feuille de calcul. Utilisez le`Worksheets` propriété du`Workbook` objet pour accéder à la collection de feuilles de calcul :

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Utilisez ensuite le`AddCopy` méthode pour copier la feuille de calcul spécifiée. Par exemple, pour copier « Sheet1 » :

```csharp
sheets.AddCopy("Sheet1");
```

## Étape 6 : Enregistrez le fichier Excel

 Utilisez le`Save` méthode du`Workbook` objet pour enregistrer les modifications dans un nouveau fichier :

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Assurez-vous de spécifier le chemin et le nom de fichier souhaités pour le fichier de sortie.

### Exemple de code source pour une feuille de calcul de copie Excel à l'aide d'Aspose.Cells pour .NET 

```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Ouvrez un fichier Excel existant.
Workbook wb = new Workbook(InputPath);
// Créez un objet Worksheets en référence à
// les feuilles du cahier d'exercices.
WorksheetCollection sheets = wb.Worksheets;
// Copier les données dans une nouvelle feuille à partir d'une feuille existante
// feuille dans le classeur.
sheets.AddCopy("Sheet1");
// Enregistrez le fichier Excel.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Conclusion

Félicitation ! Vous avez maintenant appris à copier une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Ce guide étape par étape a montré comment importer les bibliothèques nécessaires, charger un fichier Excel existant, copier la feuille de calcul et enregistrer le fichier modifié. N'hésitez pas à utiliser cette méthode dans vos propres projets pour manipuler efficacement les fichiers Excel.

### FAQ

#### Q. Aspose.Cells est-il compatible avec d’autres langages de programmation ?

A. Oui, Aspose.Cells prend en charge plusieurs langages de programmation, notamment C#, Java, Python et bien d'autres.

#### Q. Puis-je copier une feuille de calcul vers un autre classeur Excel ?

A.  Oui, vous pouvez utiliser le`AddCopy` méthode pour copier une feuille de calcul dans un autre classeur Excel.

#### Q. Aspose.Cells conserve-t-il les formules et le formatage lors de la copie de la feuille de calcul ?

A. Oui, Aspose.Cells préserve les formules, le formatage et d'autres propriétés lors de la copie d'une feuille de calcul.

#### Q. Aspose.Cells nécessite-t-il une licence pour une utilisation commerciale ?

A. Oui, Aspose.Cells est un produit commercial et nécessite l’achat d’une licence pour une utilisation commerciale. Vous pouvez trouver plus d’informations sur les licences sur le site officiel d’Aspose.