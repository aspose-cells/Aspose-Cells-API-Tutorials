---
title: Obtenir la largeur du papier et la hauteur de la feuille de calcul
linktitle: Obtenir la largeur du papier et la hauteur de la feuille de calcul
second_title: Référence de l'API Aspose.Cells pour .NET
description: Créez un guide étape par étape pour expliquer le code source C# suivant afin d'obtenir la largeur et la hauteur du papier d'une feuille de calcul à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 80
url: /fr/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
Dans ce didacticiel, nous vous expliquerons étape par étape le code source C # suivant pour obtenir la largeur et la hauteur du papier d'une feuille de calcul à l'aide de Aspose.Cells pour .NET. Suivez les étapes ci-dessous :

## Étape 1 : Créer le classeur
 Commencez par créer un nouveau classeur à l'aide de la`Workbook` classe:

```csharp
Workbook wb = new Workbook();
```

## Étape 2 : Accéder à la première feuille de calcul
 Ensuite, accédez à la première feuille de calcul du classeur à l'aide de la`Worksheet` classe:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Étape 3 : Définissez le format de papier sur A2 et affichez la largeur et la hauteur du papier en pouces
 Utilisez le`PaperSize` propriété de la`PageSetup` objet pour définir le format de papier sur A2, puis utilisez`PaperWidth` et`PaperHeight` properties pour obtenir respectivement la largeur et la hauteur du papier. Affichez ces valeurs à l'aide de la`Console.WriteLine` méthode:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Étape 4 : Répétez les étapes pour les autres formats de papier
Répétez les étapes précédentes, en modifiant le format de papier sur A3, A4 et Letter, puis en affichant les valeurs de largeur et de hauteur du papier pour chaque format :

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Exemple de code source pour obtenir la largeur et la hauteur du papier de la feuille de calcul à l'aide de Aspose.Cells pour .NET 

```csharp
//Créer un classeur
Workbook wb = new Workbook();
//Accéder à la première feuille de calcul
Worksheet ws = wb.Worksheets[0];
//Définissez la taille du papier sur A2 et imprimez la largeur et la hauteur du papier en pouces
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Définissez la taille du papier sur A3 et imprimez la largeur et la hauteur du papier en pouces
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Définissez la taille du papier sur A4 et imprimez la largeur et la hauteur du papier en pouces
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Définissez la taille du papier sur Lettre et imprimez la largeur et la hauteur du papier en pouces
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Conclusion

Vous avez appris à utiliser Aspose.Cells pour .NET pour obtenir la largeur et la hauteur du papier d'une feuille de calcul. Cette fonctionnalité peut être utile pour la configuration et la mise en page précise de vos documents Excel.

### Foire aux questions (FAQ)

#### Qu'est-ce qu'Aspose.Cells pour .NET ?

Aspose.Cells pour .NET est une bibliothèque puissante pour manipuler et traiter des fichiers Excel dans des applications .NET. Il offre de nombreuses fonctionnalités pour créer, modifier, convertir et analyser des fichiers Excel.

#### Comment puis-je obtenir la taille du papier d'une feuille de calcul avec Aspose.Cells pour .NET ?

 Vous pouvez utiliser le`PageSetup` classe de la`Worksheet` objet pour accéder au format de papier. Utilisez le`PaperSize` propriété pour définir le format de papier et la`PaperWidth` et`PaperHeight` properties pour obtenir respectivement la largeur et la hauteur du papier.

#### Quels formats de papier Aspose.Cells pour .NET prend-il en charge ?

Aspose.Cells pour .NET prend en charge une large gamme de formats de papier couramment utilisés, tels que A2, A3, A4 et Letter, ainsi que de nombreux autres formats personnalisés.

#### Puis-je personnaliser la taille du papier d'une feuille de calcul avec Aspose.Cells pour .NET ?

 Oui, vous pouvez définir un format de papier personnalisé en spécifiant les dimensions exactes de largeur et de hauteur à l'aide du`PaperWidth` et`PaperHeight` propriétés de la`PageSetup` classe.