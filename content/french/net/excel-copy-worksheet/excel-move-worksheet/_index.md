---
title: Feuille de calcul de déplacement Excel
linktitle: Feuille de calcul de déplacement Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Déplacez facilement une feuille de calcul dans un classeur Excel à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 40
url: /fr/net/excel-copy-worksheet/excel-move-worksheet/
---
Dans ce didacticiel, nous vous guiderons à travers les étapes pour déplacer une feuille de calcul dans un classeur Excel à l'aide de la bibliothèque Aspose.Cells pour .NET. Suivez les instructions ci-dessous pour effectuer cette tâche.


## Étape 1 : Préparation

Assurez-vous d'avoir installé Aspose.Cells pour .NET et créé un projet C# dans votre environnement de développement intégré (IDE) préféré.

## Étape 2 : Définissez le chemin d'accès au répertoire de documents

 Déclarer un`dataDir` variable et initialisez-la avec le chemin d'accès à votre répertoire de documents. Par exemple :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assurez-vous de remplacer`"YOUR_DOCUMENTS_DIRECTORY"` avec le chemin d'accès réel à votre répertoire.

## Étape 3 : Définissez le chemin d'accès au fichier d'entrée

 Déclarer un`InputPath` variable et initialisez-la avec le chemin complet du fichier Excel existant que vous souhaitez modifier. Par exemple :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Assurez-vous d'avoir le fichier Excel`book1.xls` dans votre répertoire de documents ou spécifiez le nom et l'emplacement corrects du fichier.

## Étape 4 : Ouvrez le fichier Excel

 Utilisez le`Workbook` classe de Aspose.Cells pour ouvrir le fichier Excel spécifié :

```csharp
Workbook wb = new Workbook(InputPath);
```

## Étape 5 : Obtenir la collection de feuilles de calcul

 Créer un`WorksheetCollection` objet pour faire référence aux feuilles de calcul dans le classeur :

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

## Étape 6 : Obtenir la première feuille de calcul

Obtenez la première feuille de calcul du classeur :

```csharp
Worksheet worksheet = sheets[0];
```

## Étape 7 : Déplacer la feuille de calcul

 Utilisez le`MoveTo` méthode pour déplacer la première feuille de calcul vers la troisième position dans le classeur :

```csharp
worksheet.MoveTo(2);
```

## Étape 8 : Enregistrez le fichier Excel modifié

Enregistrez le fichier Excel avec la feuille de calcul déplacée :

```csharp
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

Assurez-vous de spécifier le chemin et le nom de fichier souhaités pour le fichier de sortie.

### Exemple de code source pour Excel Move Worksheet à l'aide d'Aspose.Cells pour .NET 
```csharp
// Chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Ouvrez un fichier Excel existant.
Workbook wb = new Workbook(InputPath);
// Créer un objet Worksheets avec référence à
// les feuilles du cahier d'exercices.
WorksheetCollection sheets = wb.Worksheets;
// Obtenez la première feuille de calcul.
Worksheet worksheet = sheets[0];
// Déplacez la première feuille vers la troisième position dans le classeur.
worksheet.MoveTo(2);
// Enregistrez le fichier excel.
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

## Conclusion

Félicitation ! Vous avez maintenant appris à déplacer une feuille de calcul dans un classeur Excel à l'aide d'Aspose.Cells pour .NET. N'hésitez pas à utiliser cette méthode dans vos propres projets pour manipuler efficacement les fichiers Excel.

### FAQ

#### Q. Puis-je déplacer une feuille de calcul vers une autre position dans le même classeur Excel ?

A.  Oui, vous pouvez déplacer une feuille de calcul vers une autre position dans le même classeur Excel en utilisant`MoveTo` méthode de l'objet Worksheet. Spécifiez simplement l'index de la position de destination dans le classeur.

#### Q. Puis-je déplacer une feuille de calcul vers un autre classeur Excel ?

A.  Oui, vous pouvez déplacer une feuille de calcul vers un autre classeur Excel à l'aide de la`MoveTo` méthode de l'objet Worksheet. Spécifiez simplement l'index de la position de destination dans le classeur cible.

#### Q. Le code source fourni fonctionne-t-il avec d'autres formats de fichier Excel, tels que XLSX ?

A. Oui, le code source fourni fonctionne avec d'autres formats de fichiers Excel, y compris XLSX. Aspose.Cells pour .NET prend en charge une variété de formats de fichiers Excel, vous permettant de manipuler et de déplacer une feuille de calcul dans différents types de fichiers.

#### Q. Comment puis-je spécifier le chemin et le nom du fichier de sortie lors de l'enregistrement du fichier Excel modifié ?

A.  Lors de l'enregistrement du fichier Excel modifié, utilisez le`Save` méthode de l'objet Workbook spécifiant le chemin d'accès complet et le nom du fichier de sortie. Assurez-vous de spécifier l'extension de fichier appropriée, telle que`.xls` ou`.xlsx`, selon le format de fichier souhaité.