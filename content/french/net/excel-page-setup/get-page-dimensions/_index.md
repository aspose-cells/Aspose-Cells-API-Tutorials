---
title: Obtenir les dimensions de la page
linktitle: Obtenir les dimensions de la page
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment récupérer les dimensions d'une page dans Excel à l'aide d'Aspose.Cells pour .NET. Guide étape par étape avec le code source en C#.
type: docs
weight: 40
url: /fr/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET est une bibliothèque puissante qui permet aux développeurs de travailler avec des fichiers Microsoft Excel par programme. Il offre un large éventail de fonctionnalités pour manipuler des documents Excel, notamment la possibilité d'obtenir les dimensions des pages. Dans ce didacticiel, nous vous guiderons à travers les étapes permettant de récupérer les dimensions d'une page à l'aide d'Aspose.Cells for .NET.

## Étape 1 : Créer une instance de la classe Workbook

Pour commencer, nous devons créer une instance de la classe Workbook, qui représente le classeur Excel. Ceci peut être réalisé en utilisant le code suivant :

```csharp
Workbook book = new Workbook();
```

## Étape 2 : Accéder à la feuille de calcul

Ensuite, nous devons accéder à la feuille de calcul du classeur où nous souhaitons définir les dimensions de la page. Dans cet exemple, supposons que nous souhaitions travailler avec la première feuille de calcul. Nous pouvons y accéder en utilisant le code suivant :

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Étape 3 : Définissez le format de papier sur A2 et la largeur et la hauteur d'impression en pouces.

Nous allons maintenant définir le format de papier sur A2 et imprimer la largeur et la hauteur de la page en pouces. Ceci peut être réalisé en utilisant le code suivant :

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Étape 4 : Définissez le format de papier sur A3 et la largeur et la hauteur d'impression en pouces.

Ensuite, nous définirons le format de papier sur A3 et imprimerons la largeur et la hauteur de la page en pouces. Voici le code correspondant :

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Étape 5 : Définissez le format de papier sur A4 et la largeur et la hauteur d'impression en pouces.

Nous allons maintenant définir le format de papier sur A4 et imprimer la largeur et la hauteur de la page en pouces. Voici le code :

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Étape 6 : Définissez le format du papier sur Lettre et imprimez la largeur et la hauteur en pouces.

Enfin, nous définirons le format du papier sur Lettre et imprimerons la largeur et la hauteur de la page en pouces. Voici le code :

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Exemple de code source pour obtenir les dimensions de la page à l'aide d'Aspose.Cells pour .NET 
```csharp
// Créer une instance de la classe Workbook
Workbook book = new Workbook();
// Accéder à la première feuille de calcul
Worksheet sheet = book.Worksheets[0];
// Définissez le format de papier sur A2 et imprimez la largeur et la hauteur du papier en pouces.
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Définissez le format de papier sur A3 et imprimez la largeur et la hauteur du papier en pouces.
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Définissez le format de papier sur A4 et imprimez la largeur et la hauteur du papier en pouces.
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Définissez le format du papier sur Lettre et imprimez la largeur et la hauteur du papier en pouces.
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Conclusion

Félicitation ! Vous avez appris à récupérer les dimensions d'une page à l'aide d'Aspose.Cells pour .NET. Cette fonctionnalité peut être utile lorsque vous devez effectuer des opérations spécifiques basées sur les dimensions de la page dans vos fichiers Excel.

N'oubliez pas d'explorer davantage la documentation d'Aspose.Cells pour découvrir toutes les fonctionnalités puissantes qu'il offre.

### FAQ

#### 1. Quels autres formats de papier Aspose.Cells for .NET prend-il en charge ?

Aspose.Cells for .NET prend en charge une variété de formats de papier, notamment A1, A5, B4, B5, Executive, Legal, Letter et bien d'autres. Vous pouvez consulter la documentation pour la liste complète des formats de papier pris en charge.

#### 2. Puis-je définir des dimensions de page personnalisées avec Aspose.Cells pour .NET ?

Oui, vous pouvez définir des dimensions de page personnalisées en spécifiant la largeur et la hauteur souhaitées. Aspose.Cells offre une flexibilité totale pour personnaliser les dimensions de la page selon vos besoins.

#### 3. Puis-je obtenir les dimensions des pages dans des unités autres que les pouces ?

Oui, Aspose.Cells pour .NET vous permet d'obtenir les dimensions de la page dans différentes unités, notamment les pouces, les centimètres, les millimètres et les points.

#### 4. Aspose.Cells for .NET prend-il en charge d'autres fonctionnalités d'édition des paramètres de page ?

Oui, Aspose.Cells offre une gamme complète de fonctionnalités pour modifier les paramètres de page, notamment la définition des marges, de l'orientation, des en-têtes et des pieds de page, etc.