---
title: Volets divisés de la feuille de calcul
linktitle: Volets divisés de la feuille de calcul
second_title: Référence de l'API Aspose.Cells pour .NET
description: Guide étape par étape pour diviser les volets dans une feuille de calcul Excel à l’aide d’Aspose.Cells pour .NET.
type: docs
weight: 130
url: /fr/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
Dans ce didacticiel, nous expliquerons comment diviser les volets dans une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. Suivez ces étapes pour obtenir le résultat souhaité :

## Étape 1 : Configuration de l'environnement

Assurez-vous d'avoir installé Aspose.Cells pour .NET et configuré votre environnement de développement. Assurez-vous également de disposer d'une copie du fichier Excel sur lequel vous souhaitez diviser les volets.

## Étape 2 : Importez les dépendances nécessaires

Ajoutez les directives nécessaires pour utiliser les classes d'Aspose.Cells :

```csharp
using Aspose.Cells;
```

## Étape 3 : initialisation du code

Commencez par initialiser le chemin du répertoire contenant vos documents Excel :

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Étape 4 : Ouverture du fichier Excel

 Instancier un nouveau`Workbook` objet et ouvrez le fichier Excel à l’aide du`Open` méthode:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Étape 5 : Définir la cellule active

 Définissez la cellule active de la feuille de calcul à l'aide du`ActiveCell` propriété:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Étape 6 : Division des rabats

 Divisez la fenêtre de la feuille de calcul à l'aide du`Split` méthode:

```csharp
book.Worksheets[0].Split();
```

## Étape 7 : Enregistrer les modifications

Enregistrez les modifications apportées au fichier Excel :

```csharp
book.Save(dataDir + "output.xls");
```

### Exemple de code source pour les volets divisés d'une feuille de calcul à l'aide d'Aspose.Cells pour .NET 

```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instancier un nouveau classeur et ouvrir un fichier modèle
Workbook book = new Workbook(dataDir + "Book1.xls");
// Définir la cellule active
book.Worksheets[0].ActiveCell = "A20";
// Diviser la fenêtre de la feuille de calcul
book.Worksheets[0].Split();
// Enregistrez le fichier Excel
book.Save(dataDir + "output.xls");
```

## Conclusion

Dans ce didacticiel, vous avez appris à diviser les volets d'une feuille de calcul Excel à l'aide d'Aspose.Cells pour .NET. En suivant les étapes décrites, vous pouvez facilement personnaliser l'apparence et le comportement de vos fichiers Excel.

### Foire aux questions (FAQ)

#### Qu’est-ce qu’Aspose.Cells pour .NET ?

Aspose.Cells for .NET est une bibliothèque logicielle populaire pour manipuler des fichiers Excel dans des applications .NET.

#### Comment puis-je définir la cellule active d’une feuille de calcul dans Aspose.Cells ?

 Vous pouvez définir la cellule active à l'aide du`ActiveCell`propriété de l’objet Worksheet.

#### Puis-je diviser uniquement les volets horizontaux ou verticaux de la fenêtre de la feuille de calcul ?

 Oui, en utilisant Aspose.Cells, vous ne pouvez diviser les volets horizontaux ou verticaux qu'en utilisant les méthodes appropriées telles que`SplitColumn` ou`SplitRow`.

#### Aspose.Cells fonctionne-t-il uniquement avec les fichiers Excel au format .xls ?

Non, Aspose.Cells prend en charge divers formats de fichiers Excel, notamment .xls et .xlsx.