---
title: Implémenter la taille de papier personnalisée de la feuille de calcul pour le rendu
linktitle: Implémenter la taille de papier personnalisée de la feuille de calcul pour le rendu
second_title: Référence de l'API Aspose.Cells pour .NET
description: Guide étape par étape pour implémenter une taille de feuille de calcul personnalisée avec Aspose.Cells pour .NET. Définissez les dimensions, ajoutez un message et enregistrez au format PDF.
type: docs
weight: 50
url: /fr/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
L'implémentation d'une taille personnalisée pour votre feuille de calcul peut être très utile lorsque vous souhaitez créer un document PDF avec une taille spécifique. Dans ce didacticiel, nous allons apprendre à utiliser Aspose.Cells pour .NET pour définir une taille personnalisée pour une feuille de calcul, puis enregistrer le document au format PDF.

## Étape 1 : Création du dossier de sortie

Avant de commencer, vous devez créer un dossier de sortie dans lequel le fichier PDF généré sera enregistré. Vous pouvez utiliser le chemin de votre choix pour votre dossier de sortie.

```csharp
// Répertoires de sortie
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Assurez-vous de spécifier le chemin d'accès correct à votre dossier de sortie.

## Étape 2 : Création de l'objet Workbook

Pour commencer, vous devez créer un objet Workbook à l'aide de Aspose.Cells. Cet objet représente votre feuille de calcul.

```csharp
// Créer l'objet Workbook
Workbook wb = new Workbook();
```

## Étape 3 : Accéder à la première feuille de travail

Après avoir créé l'objet Workbook, vous pouvez accéder à la première feuille de calcul qu'il contient.

```csharp
// Accéder à la première feuille de travail
Worksheet ws = wb.Worksheets[0];
```

## Étape 4 : Définir la taille de la feuille de calcul personnalisée

 Vous pouvez maintenant définir la taille de la feuille de calcul personnalisée à l'aide de`CustomPaperSize(width, height)` méthode de la classe PageSetup.

```csharp
// Définir la taille de la feuille de calcul personnalisée (en pouces)
ws.PageSetup.CustomPaperSize(6, 4);
```

Dans cet exemple, nous avons défini la taille de la feuille de calcul sur 6 pouces de large et 4 pouces de haut.

## Étape 5 : Accès à la cellule B4

Après cela, nous pouvons accéder à une cellule spécifique dans la feuille de calcul. Dans ce cas, nous accéderons à la cellule B4.

```csharp
// Accès à la cellule B4
Cell b4 = ws.Cells["B4"];
```

## Étape 6 : Ajouter le message dans la cellule B4

 Nous pouvons maintenant ajouter un message à la cellule B4 en utilisant le`PutValue(value)` méthode.

```csharp
// Ajouter le message dans la cellule B4
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

Dans cet exemple, nous avons ajouté le message "Taille de la page PDF : 6,00" x 4,00" dans la cellule B4.

## Étape 7 : Enregistrer la feuille de calcul au format PDF

 Enfin, nous pouvons enregistrer la feuille de calcul au format PDF en utilisant le`Save(filePath)` méthode de l'objet Workbook.

```csharp
// Enregistrez la feuille de calcul au format PDF
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Spécifiez le chemin d'accès souhaité au fichier PDF généré, en utilisant le dossier de sortie créé précédemment.

### Exemple de code source pour Implémenter la taille de papier personnalisée de la feuille de calcul pour le rendu à l'aide d'Aspose.Cells pour .NET 
```csharp
//Répertoire de sortie
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Créer un objet classeur
Workbook wb = new Workbook();
//Accéder à la première feuille de calcul
Worksheet ws = wb.Worksheets[0];
//Définir le format de papier personnalisé en pouces
ws.PageSetup.CustomPaperSize(6, 4);
//Accéder à la cellule B4
Cell b4 = ws.Cells["B4"];
//Ajouter le message dans la cellule B4
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Enregistrer le classeur au format pdf
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## conclusion

Dans ce didacticiel, vous avez appris à implémenter la taille personnalisée d'une feuille de calcul à l'aide de Aspose.Cells pour .NET. Vous pouvez utiliser ces étapes pour définir des dimensions spécifiques pour vos feuilles de calcul, puis enregistrer les documents au format PDF. Nous espérons que ce guide vous a été utile pour comprendre le processus de mise en œuvre d'une taille de feuille de calcul personnalisée.

### Foire aux questions (FAQ)

#### Question 1 : Puis-je personnaliser davantage la mise en page de la feuille de calcul ?

Oui, Aspose.Cells offre de nombreuses options pour personnaliser la mise en page de votre feuille de calcul. Vous pouvez définir des dimensions personnalisées, l'orientation de la page, les marges, les en-têtes et les pieds de page, et bien plus encore.

#### Question 2 : Quels autres formats de sortie Aspose.Cells prend-il en charge ?

Aspose.Cells prend en charge de nombreux formats de sortie différents, notamment PDF, XLSX, XLS, CSV, HTML, TXT et bien d'autres. Vous pouvez choisir le format de sortie souhaité en fonction de vos besoins.