---
title: Déterminer si la taille du papier de la feuille de calcul est automatique
linktitle: Déterminer si la taille du papier de la feuille de calcul est automatique
second_title: Référence de l'API Aspose.Cells pour .NET
description: Apprenez à déterminer si le format de papier d'une feuille de calcul est automatique avec Aspose.Cells pour .NET.
type: docs
weight: 20
url: /fr/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
Dans cet article, nous vous expliquerons étape par étape le code source C# suivant : Déterminez si la taille du papier d'une feuille de calcul est automatique à l'aide d'Aspose.Cells pour .NET. Nous utiliserons la bibliothèque Aspose.Cells pour .NET pour effectuer cette opération. Suivez les étapes ci-dessous pour déterminer si le format de papier d'une feuille de calcul est automatique.

## Étape 1 : Chargement des classeurs
La première étape consiste à charger les classeurs. Nous aurons deux classeurs : l'un avec la taille de papier automatique désactivée et l'autre avec la taille de papier automatique activée. Voici le code pour charger les classeurs :

```csharp
// répertoire des sources
string sourceDir = "YOUR_SOURCE_DIR";
// Répertoire de sortie
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Charger le premier classeur avec le format de papier automatique désactivé
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Charger un deuxième classeur avec le format de papier automatique activé
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Étape 2 : Accéder aux feuilles de calcul
Maintenant que nous avons chargé les classeurs, nous devons accéder aux feuilles de calcul afin de pouvoir vérifier le format de papier automatique. Nous allons passer à la première feuille de travail des deux cahiers. Voici le code pour y accéder :

```csharp
//Accéder à la première feuille de calcul du premier classeur
Worksheet ws11 = wb1.Worksheets[0];

// Accéder à la première feuille de calcul du deuxième classeur
Worksheet ws12 = wb2.Worksheets[0];
```

## Étape 3 : Vérification du format de papier automatique
 Dans cette étape, nous vérifierons si la taille du papier de la feuille de calcul est automatique. Nous utiliserons le`PageSetup.IsAutomaticPaperSize` propriété pour obtenir ces informations. Nous afficherons ensuite le résultat. Voici le code pour cela :

```csharp
// Afficher la propriété IsAutomaticPaperSize de la première feuille de calcul du premier classeur
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Afficher la propriété IsAutomaticPaperSize de la première feuille de calcul dans le deuxième classeur
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Exemple de code source pour déterminer si la taille du papier de la feuille de calcul est automatique à l'aide de Aspose.Cells pour .NET 
```csharp
//Répertoire des sources
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Répertoire de sortie
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Charger le premier classeur ayant un format de papier automatique faux
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Charger le deuxième classeur ayant le format de papier automatique vrai
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Accéder à la première feuille de calcul des deux classeurs
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Imprimer la propriété PageSetup.IsAutomaticPaperSize des deux feuilles de calcul
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Conclusion
Dans cet article, nous avons appris à déterminer si la taille du papier d'une feuille de calcul est automatique à l'aide de Aspose.Cells pour .NET. Nous avons suivi les étapes suivantes : chargement des classeurs,

accès aux feuilles de calcul et vérification automatique du format de papier. Vous pouvez maintenant utiliser ces connaissances pour déterminer si le format de papier de vos feuilles de calcul est automatique.

### FAQ

Q : Comment puis-je charger des classeurs avec Aspose.Cells pour .NET ?
R : Vous pouvez charger des classeurs à l'aide de la classe Workbook de la bibliothèque Aspose.Cells. Utilisez la méthode Workbook.Load pour charger un classeur à partir d'un fichier.

Q : Puis-je vérifier le format de papier automatique pour d'autres feuilles de calcul ?
R : Oui, vous pouvez vérifier le format de papier automatique pour n'importe quelle feuille de calcul en accédant à la propriété PageSetup.IsAutomaticPaperSize de l'objet Worksheet correspondant.

Q : Comment puis-je modifier le format de papier automatique d'une feuille de calcul ?
R : Pour modifier le format de papier automatique d'une feuille de calcul, vous pouvez utiliser la propriété PageSetup.IsAutomaticPaperSize et la définir sur la valeur souhaitée (true ou false).

Q : Quelles autres fonctionnalités Aspose.Cells pour .NET offre-t-il ?
R : Aspose.Cells pour .NET offre de nombreuses fonctionnalités pour travailler avec des feuilles de calcul, telles que la création, la modification et la conversion de classeurs, ainsi que la manipulation de données, de formules et de mise en forme.