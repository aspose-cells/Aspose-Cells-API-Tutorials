---
title: Options d'ajustement aux pages Excel
linktitle: Options d'ajustement aux pages Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment ajuster automatiquement les pages dans une feuille de calcul Excel avec Aspose.Cells pour .NET.
type: docs
weight: 30
url: /fr/net/excel-page-setup/fit-to-excel-pages-options/
---
Dans cet article, nous vous expliquerons étape par étape le code source C# suivant : Options d'ajustement des pages Excel à l'aide d'Aspose.Cells pour .NET. Nous utiliserons la bibliothèque Aspose.Cells pour .NET pour effectuer cette opération. Suivez les étapes ci-dessous pour configurer l'ajustement aux pages dans Excel.

## Étape 1 : Création d'un classeur
La première étape consiste à créer un classeur. Nous allons instancier un objet Workbook. Voici le code pour créer un classeur :

```csharp
// Le chemin d'accès au répertoire des documents
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Instancier un objet Workbook
Workbook workbook = new Workbook();
```

## Étape 2 : Accéder à la feuille de calcul
Maintenant que nous avons créé le classeur, nous devons accéder à la première feuille de calcul. Nous utiliserons l'index 0 pour accéder à la première feuille. Voici le code pour y accéder :

```csharp
// Accès à la première feuille de calcul du classeur
Worksheet worksheet = workbook.Worksheets[0];
```

## Étape 3 : Définition de l'ajustement aux pages
 Dans cette étape, nous allons configurer l'ajustement des pages de la feuille de calcul. Nous utiliserons le`FitToPagesTall` et`FitToPagesWide` propriétés du`PageSetup` objet pour spécifier le nombre de pages souhaité pour la hauteur et la largeur de la feuille de calcul. Voici le code pour cela :

```csharp
// Configurer le nombre de pages pour la hauteur de la feuille de calcul
worksheet.PageSetup.FitToPagesTall = 1;

// Configurer le nombre de pages pour la largeur de la feuille de calcul
worksheet.PageSetup.FitToPagesWide = 1;
```

## Étape 4 : enregistrement du classeur
 Maintenant que nous avons configuré l'ajustement aux pages, nous pouvons enregistrer le classeur. Nous utiliserons le`Save` méthode de l’objet Workbook pour cela. Voici le code pour enregistrer le classeur :

```csharp
// Enregistrez le classeur
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Exemple de code source pour les options Ajuster aux pages Excel à l’aide d’Aspose.Cells pour .NET 
```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciation d'un objet Workbook
Workbook workbook = new Workbook();
// Accéder à la première feuille de calcul du fichier Excel
Worksheet worksheet = workbook.Worksheets[0];
// Définition du nombre de pages sur lequel la longueur de la feuille de calcul sera étendue
worksheet.PageSetup.FitToPagesTall = 1;
//Définition du nombre de pages sur lequel la largeur de la feuille de calcul sera étendue
worksheet.PageSetup.FitToPagesWide = 1;
// Enregistrez le classeur.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Conclusion
Dans cet article, nous avons appris comment configurer l'ajustement aux pages dans Excel à l'aide d'Aspose.Cells pour .NET. Nous avons suivi les étapes suivantes : création du classeur, accès à la feuille de calcul, configuration de l'ajustement aux pages et enregistrement du classeur. Vous pouvez désormais utiliser ces connaissances pour ajuster vos feuilles de calcul aux pages souhaitées.

### FAQ

#### Q : Comment puis-je installer Aspose.Cells pour .NET ?

R : Pour installer Aspose.Cells pour .NET, vous pouvez utiliser le gestionnaire de packages NuGet dans Visual Studio. Recherchez le package "Aspose.Cells" et installez-le dans votre projet.

#### Q : Puis-je adapter les pages en hauteur et en largeur ?

 R : Oui, vous pouvez ajuster la hauteur et la largeur de la feuille de calcul à l'aide du bouton`FitToPagesTall` et`FitToPagesWide` propriétés. Vous pouvez spécifier le nombre de pages souhaité pour chaque dimension.

#### Q : Comment puis-je personnaliser les options Ajuster aux pages ?

R : En plus de spécifier le nombre de pages, vous pouvez également personnaliser d'autres options d'ajustement aux pages telles que l'échelle de la feuille de calcul, l'orientation du papier, les marges, etc. Utilisez les propriétés disponibles dans le`PageSetup` s'opposer à cela.

#### Q : Puis-je utiliser Aspose.Cells pour .NET pour traiter des classeurs existants ?

R : Oui, vous pouvez utiliser Aspose.Cells for .NET pour ouvrir et modifier des classeurs existants. Vous pouvez accéder à des feuilles de calcul, des cellules, des formules, des styles et d'autres éléments de classeur pour effectuer diverses opérations.