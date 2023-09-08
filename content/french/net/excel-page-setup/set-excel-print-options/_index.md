---
title: Définir les options d'impression Excel
linktitle: Définir les options d'impression Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Apprenez à manipuler des fichiers Excel et à personnaliser facilement les options d'impression à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 150
url: /fr/net/excel-page-setup/set-excel-print-options/
---
Dans ce guide, nous vous expliquerons comment définir les options d'impression pour un classeur Excel à l'aide d'Aspose.Cells pour .NET. Nous vous guiderons étape par étape à travers le code source C# fourni pour accomplir cette tâche.

## Étape 1 : Configuration de l'environnement

Avant de commencer, assurez-vous d'avoir configuré votre environnement de développement et installé Aspose.Cells pour .NET. Vous pouvez télécharger la dernière version de la bibliothèque sur le site officiel d'Aspose.

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

Instanciez un objet Workbook qui représente le classeur Excel que vous souhaitez créer :

```csharp
Workbook workbook = new Workbook();
```

## Étape 5 : Obtention de la référence PageSetup de la feuille de calcul

Pour définir les options d'impression, nous devons d'abord obtenir la référence PageSetup à partir de la feuille de calcul. Utilisez le code suivant pour obtenir la référence :

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Étape 6 : Activer l'impression des lignes de grille

Pour permettre l'impression des lignes de quadrillage, utilisez le code suivant :

```csharp
pageSetup. PrintGridlines = true;
```

## Étape 7 : Activer l’impression des en-têtes de ligne/colonne

Pour activer l'impression des en-têtes de lignes et de colonnes, utilisez le code suivant :

```csharp
pageSetup.PrintHeadings = true;
```

## Étape 8 : Activation du mode d'impression noir et blanc

Pour activer l'impression de la feuille de calcul en mode noir et blanc, utilisez le code suivant :

```csharp
pageSetup.BlackAndWhite = true;
```

## Étape 9 : Activation de l'impression des commentaires

Pour permettre l'impression des commentaires tels qu'ils apparaissent sur la feuille de calcul, utilisez le code suivant :

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## Étape 10 : Activer l'impression en mode brouillon

Pour activer l'impression de la feuille de calcul en mode brouillon, utilisez le code suivant :

```csharp
pageSetup.PrintDraft = true;
```

## Étape 11 : Activer l'impression des erreurs de cellule en tant que N/A

Pour permettre aux erreurs de cellule d'être imprimées sous forme

  que N/A, utilisez le code suivant :

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## Étape 12 : Enregistrement du classeur Excel

 Pour enregistrer le classeur Excel avec les options d'impression définies, utilisez le`Save` méthode de l'objet Workbook :

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

Cela enregistrera le classeur Excel avec le nom de fichier « OtherPrintOptions_out.xls » dans le répertoire spécifié.

### Exemple de code source pour définir les options d'impression Excel à l'aide d'Aspose.Cells pour .NET 
```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciation d'un objet Workbook
Workbook workbook = new Workbook();
// Obtention de la référence du PageSetup de la feuille de calcul
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Permettre d'imprimer un quadrillage
pageSetup.PrintGridlines = true;
// Permettre d'imprimer les en-têtes de lignes/colonnes
pageSetup.PrintHeadings = true;
// Permettre d'imprimer une feuille de calcul en mode noir et blanc
pageSetup.BlackAndWhite = true;
// Permettre d'imprimer les commentaires tels qu'affichés sur la feuille de calcul
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// Permet d'imprimer une feuille de calcul avec une qualité de brouillon
pageSetup.PrintDraft = true;
// Permettre d'imprimer les erreurs de cellule comme N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// Enregistrez le classeur.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## Conclusion

Vous avez maintenant appris à définir les options d'impression pour un classeur Excel à l'aide d'Aspose.Cells pour .NET. Cette bibliothèque puissante et conviviale vous permet de personnaliser les paramètres d'impression de vos classeurs Excel de manière simple et efficace.

### FAQ


#### 1. Puis-je personnaliser davantage les options d'impression, telles que les marges ou l'orientation de la page ?

Oui, Aspose.Cells pour .NET offre une large gamme d'options d'impression personnalisables, telles que les marges, l'orientation de la page, l'échelle, etc.

#### 2. Aspose.Cells for .NET prend-il en charge d'autres formats de fichiers Excel ?

Oui, Aspose.Cells for .NET prend en charge une variété de formats de fichiers Excel, tels que XLSX, XLS, CSV, HTML, PDF, etc.

#### 3. Aspose.Cells for .NET est-il compatible avec toutes les versions de .NET Framework ?

Aspose.Cells for .NET est compatible avec .NET Framework 2.0 ou version ultérieure, y compris les versions 3.5, 4.0, 4.5, 4.6, etc.