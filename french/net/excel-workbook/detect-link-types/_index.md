---
title: Détecter les types de liens
linktitle: Détecter les types de liens
second_title: Référence de l'API Aspose.Cells pour .NET
description: Détectez les types de liens dans un classeur Excel à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 80
url: /fr/net/excel-workbook/detect-link-types/
---
Dans ce didacticiel, nous vous guiderons pas à pas dans le code source C# fourni qui vous permettra de détecter les types de liens dans un classeur Excel à l'aide d'Aspose.Cells pour .NET. Suivez les étapes ci-dessous pour effectuer cette opération.

## Étape 1 : Définir le répertoire source

```csharp
// répertoire des sources
string SourceDir = RunExamples.Get_SourceDirectory();
```

Dans cette première étape, nous définissons le répertoire source où se trouve le classeur Excel contenant les liens.

## Étape 2 : charger le classeur Excel

```csharp
//Charger le classeur Excel
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
```

Nous chargeons le classeur Excel en utilisant le chemin du fichier source.

## Étape 3 : Obtenir la feuille de calcul

```csharp
// Obtenir la première feuille de calcul (par défaut)
Worksheet worksheet = workbook.Worksheets[0];
```

 Nous obtenons la première feuille de calcul du classeur. Vous pouvez changer le`[0]` index pour accéder à une feuille de calcul spécifique si nécessaire.

## Étape 4 : créer une plage de cellules

```csharp
// Créer une plage de cellules A1 : B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
```

Nous créons une plage de cellules, dans cet exemple de la cellule A1 à la cellule A7. Vous pouvez ajuster les références de cellule selon vos besoins.

## Étape 5 : Obtenez les liens hypertexte à portée

```csharp
// Obtenir les hyperliens de la plage
Hyperlink[] hyperlinks = range.Hyperlinks;
```

Nous obtenons tous les hyperliens présents dans la plage spécifiée.

## Étape 6 : Parcourir les hyperliens et afficher les types de liens

```csharp
foreach (Hyperlink link in hyperlinks)
{
Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
```

Nous parcourons chaque lien et affichons le texte affiché et le type de lien associé.

### Exemple de code source pour détecter les types de liens à l'aide d'Aspose.Cells pour .NET 
```csharp
//répertoire des sources
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
// Obtenir la première feuille de calcul (par défaut)
Worksheet worksheet = workbook.Worksheets[0];
// Créer une plage A2:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
// Obtenir des hyperliens à portée
Hyperlink[] hyperlinks = range.Hyperlinks;
foreach (Hyperlink link in hyperlinks)
{
	Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
Console.WriteLine("DetectLinkTypes executed successfully.");
```

## Conclusion

Félicitation ! Vous avez appris à détecter les types de liens dans un classeur Excel à l'aide d'Aspose.Cells pour .NET. Cette fonctionnalité vous permet de travailler avec les hyperliens présents dans vos classeurs Excel. Continuez à explorer les fonctionnalités d'Aspose.Cells pour étendre vos capacités de traitement de classeur Excel.

### FAQ

#### Q : Comment puis-je installer Aspose.Cells pour .NET dans mon projet ?

 R : Vous pouvez installer Aspose.Cells pour .NET à l'aide du gestionnaire de packages NuGet. Rechercher[Aspose Communiqués](https://releases.aspose.com/cells/net) dans la console NuGet Package Manager et installez la dernière version.

#### Q : Puis-je détecter des types de liens dans des feuilles de calcul spécifiques plutôt que dans la première feuille ?

 R : Oui, vous pouvez modifier le`workbook.Worksheets[0]` index pour accéder à une feuille de calcul spécifique. Par exemple, pour accéder à la deuxième feuille, utilisez`workbook.Worksheets[1]`.

#### : Est-il possible de modifier les types de liens détectés dans la gamme ?

R : Oui, vous pouvez parcourir les hyperliens et effectuer des opérations d'édition, telles que la mise à jour d'URL ou la suppression de liens indésirables.

#### Q : Quels types de liens sont possibles dans Aspose.Cells pour .NET ?

R : Les types de liens possibles incluent les hyperliens, les liens vers d'autres feuilles de calcul, les liens vers des fichiers externes, les liens vers des sites Web, etc.

#### Q : Aspose.Cells pour .NET prend-il en charge la création de nouveaux liens dans une feuille de calcul ?

 R : Oui, Aspose.Cells pour .NET prend en charge la création de nouveaux liens à l'aide de`Hyperlink` classe et ses propriétés associées. Vous pouvez ajouter des hyperliens, des liens vers des URL, des liens vers d'autres feuilles de calcul, etc.

#### Q : Puis-je utiliser Aspose.Cells pour .NET dans des applications Web ?

R : Oui, Aspose.Cells pour .NET peut être utilisé dans des applications Web. Vous pouvez l'intégrer dans ASP.NET, ASP.NET Core et d'autres frameworks Web basés sur .NET.

#### Q : Existe-t-il des limites de taille de fichier lors de l'utilisation d'Aspose.Cells pour .NET ?

: Aspose.Cells pour .NET peut traiter de grands classeurs Excel sans limitation spécifique. Cependant, la taille réelle du fichier peut être limitée par les ressources système disponibles.