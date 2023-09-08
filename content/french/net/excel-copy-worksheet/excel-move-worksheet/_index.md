---
title: Feuille de calcul de déplacement Excel
linktitle: Feuille de calcul de déplacement Excel
second_title: Référence de l'API Aspose.Cells pour .NET
description: Déplacez facilement une feuille de calcul dans un classeur Excel à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 40
url: /fr/net/excel-copy-worksheet/excel-move-worksheet/
---
Dans ce didacticiel, nous vous guiderons à travers les étapes permettant de déplacer une feuille de calcul vers un classeur Excel à l'aide de la bibliothèque Aspose.Cells pour .NET. Suivez les instructions ci-dessous pour terminer cette tâche.


## Étape 1 : Préparation

Assurez-vous d'avoir installé Aspose.Cells pour .NET et créé un projet C# dans votre environnement de développement intégré (IDE) préféré.

## Étape 2 : Définir le chemin du répertoire du document

 Déclarer un`dataDir` variable et initialisez-la avec le chemin d’accès à votre répertoire de documents. Par exemple :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assurez-vous de remplacer`"YOUR_DOCUMENTS_DIRECTORY"` avec le chemin réel de votre répertoire.

## Étape 3 : Définir le chemin du fichier d’entrée

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

## Étape 5 : Obtenez la collection de feuilles de calcul

 Créer un`WorksheetCollection` objet pour faire référence aux feuilles de calcul du classeur :

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

## Étape 6 : Obtenez la première feuille de calcul

Obtenez la première feuille de calcul du classeur :

```csharp
Worksheet worksheet = sheets[0];
```

## Étape 7 : déplacer la feuille de calcul

 Utilisez le`MoveTo` méthode pour déplacer la première feuille de calcul vers la troisième position du classeur :

```csharp
worksheet.MoveTo(2);
```

## Étape 8 : Enregistrez le fichier Excel modifié

Enregistrez le fichier Excel avec la feuille de calcul déplacée :

```csharp
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

Assurez-vous de spécifier le chemin et le nom de fichier souhaités pour le fichier de sortie.

### Exemple de code source pour la feuille de calcul de déplacement Excel à l'aide d'Aspose.Cells pour .NET 
```csharp
//Le chemin d'accès au répertoire des documents.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Ouvrez un fichier Excel existant.
Workbook wb = new Workbook(InputPath);
// Créez un objet Worksheets en référence à
// les feuilles du cahier d'exercices.
WorksheetCollection sheets = wb.Worksheets;
// Obtenez la première feuille de travail.
Worksheet worksheet = sheets[0];
// Déplacez la première feuille vers la troisième position du classeur.
worksheet.MoveTo(2);
// Enregistrez le fichier Excel.
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

## Conclusion

Félicitation ! Vous avez maintenant appris à déplacer une feuille de calcul vers un classeur Excel à l'aide d'Aspose.Cells pour .NET. N'hésitez pas à utiliser cette méthode dans vos propres projets pour manipuler efficacement les fichiers Excel.

### FAQ

#### Q. Puis-je déplacer une feuille de calcul vers un autre emplacement dans le même classeur Excel ?

A.  Oui, vous pouvez déplacer une feuille de calcul vers un autre emplacement dans le même classeur Excel en utilisant`MoveTo` méthode de l’objet Worksheet. Spécifiez simplement l'index de la position de destination dans le classeur.

#### Q. Puis-je déplacer une feuille de calcul vers un autre classeur Excel ?

A.  Oui, vous pouvez déplacer une feuille de calcul vers un autre classeur Excel à l'aide de l'outil`MoveTo` méthode de l’objet Worksheet. Spécifiez simplement l'index de la position de destination dans le classeur cible.

#### Q. Le code source fourni fonctionne-t-il avec d'autres formats de fichiers Excel, tels que XLSX ?

A. Oui, le code source fourni fonctionne avec d'autres formats de fichiers Excel, notamment XLSX. Aspose.Cells for .NET prend en charge une variété de formats de fichiers Excel, vous permettant de manipuler et de déplacer une feuille de calcul vers différents types de fichiers.

#### Q. Comment puis-je spécifier le chemin et le nom du fichier de sortie lors de l'enregistrement du fichier Excel modifié ?

A.  Lors de l'enregistrement du fichier Excel modifié, utilisez le`Save` méthode de l’objet Workbook spécifiant le chemin complet et le nom du fichier de sortie. Assurez-vous de spécifier l'extension de fichier appropriée, telle que`.xls` ou`.xlsx`, en fonction du format de fichier souhaité.