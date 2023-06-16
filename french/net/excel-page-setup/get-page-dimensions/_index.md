---
title: Obtenir les dimensions de la page
linktitle: Obtenir les dimensions de la page
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment récupérer les dimensions de page dans Excel à l'aide d'Aspose.Cells pour .NET. Guide étape par étape avec code source en C#.
type: docs
weight: 40
url: /fr/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells pour .NET est une bibliothèque puissante qui permet aux développeurs de travailler avec des fichiers Microsoft Excel par programmation. Il offre un large éventail de fonctionnalités pour manipuler des documents Excel, y compris la possibilité d'obtenir des dimensions de page. Dans ce didacticiel, nous vous guiderons à travers les étapes pour récupérer les dimensions de la page à l'aide de Aspose.Cells pour .NET.

## Étape 1 : Créer une instance de la classe Workbook

Pour commencer, nous devons créer une instance de la classe Workbook, qui représente le classeur Excel. Ceci peut être réalisé en utilisant le code suivant :

```csharp
Workbook book = new Workbook();
```

## Étape 2 : Accéder à la feuille de calcul

Ensuite, nous devons accéder à la feuille de calcul dans le classeur où nous voulons définir les dimensions de la page. Dans cet exemple, supposons que nous voulions travailler avec la première feuille de calcul. Nous pouvons y accéder en utilisant le code suivant :

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Étape 3 : Définissez le format de papier sur A2 et imprimez la largeur et la hauteur en pouces

Nous allons maintenant définir le format de papier sur A2 et imprimer la largeur et la hauteur de la page en pouces. Ceci peut être réalisé en utilisant le code suivant :

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Étape 4 : Définissez le format de papier sur A3 et imprimez la largeur et la hauteur en pouces

Ensuite, nous allons définir le format de papier sur A3 et imprimer la largeur et la hauteur de la page en pouces. Voici le code correspondant :

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Étape 5 : Définissez le format de papier sur A4 et imprimez la largeur et la hauteur en pouces

Nous allons maintenant définir le format de papier sur A4 et imprimer la largeur et la hauteur de la page en pouces. Voici le code :

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Étape 6 : Définissez le format de papier sur Lettre et imprimez la largeur et la hauteur en pouces

Enfin, nous définirons le format de papier sur Lettre et imprimerons la largeur et la hauteur de la page en pouces. Voici le code :

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Exemple de code source pour Get Page Dimensions à l'aide de Aspose.Cells pour .NET 
```csharp
// Créer une instance de la classe Workbook
Workbook book = new Workbook();
// Accéder à la première feuille de calcul
Worksheet sheet = book.Worksheets[0];
// Définissez la taille du papier sur A2 et imprimez la largeur et la hauteur du papier en pouces
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Définissez la taille du papier sur A3 et imprimez la largeur et la hauteur du papier en pouces
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Définissez la taille du papier sur A4 et imprimez la largeur et la hauteur du papier en pouces
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Définissez la taille du papier sur Lettre et imprimez la largeur et la hauteur du papier en pouces
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Conclusion

Félicitation ! Vous avez appris à récupérer des dimensions de page à l'aide d'Aspose.Cells pour .NET. Cette fonctionnalité peut être utile lorsque vous devez effectuer des opérations spécifiques en fonction des dimensions de la page dans vos fichiers Excel.

N'oubliez pas d'explorer davantage la documentation d'Aspose.Cells pour découvrir toutes les fonctionnalités puissantes qu'il offre.

### FAQ

#### 1. Quels autres formats de papier Aspose.Cells pour .NET prend-il en charge ?

Aspose.Cells pour .NET prend en charge une variété de formats de papier, notamment A1, A5, B4, B5, Executive, Legal, Letter et bien d'autres. Vous pouvez consulter la documentation pour la liste complète des formats de papier pris en charge.

#### 2. Puis-je définir des dimensions de page personnalisées avec Aspose.Cells pour .NET ?

Oui, vous pouvez définir des dimensions de page personnalisées en spécifiant la largeur et la hauteur souhaitées. Aspose.Cells offre une flexibilité totale pour personnaliser les dimensions de la page selon vos besoins.

#### 3. Puis-je obtenir des dimensions de page dans des unités autres que les pouces ?

Oui, Aspose.Cells pour .NET vous permet d'obtenir les dimensions de la page dans différentes unités, y compris les pouces, les centimètres, les millimètres et les points.

#### 4. Aspose.Cells pour .NET prend-il en charge d'autres fonctionnalités d'édition des paramètres de page ?

Oui, Aspose.Cells offre une gamme complète de fonctionnalités pour modifier les paramètres de la page, y compris la définition des marges, l'orientation, les en-têtes et les pieds de page, etc.