---
title: Extraire le fichier Mol intégré
linktitle: Extraire le fichier Mol intégré
second_title: Référence de l'API Aspose.Cells pour .NET
description: Apprenez à extraire facilement des fichiers MOL intégrés à partir d'un classeur Excel à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 90
url: /fr/net/excel-workbook/extract-embedded-mol-file/
---
Dans ce didacticiel, nous vous expliquerons étape par étape comment extraire un fichier MOL intégré à partir d'un classeur Excel à l'aide de la bibliothèque Aspose.Cells pour .NET. Vous apprendrez à parcourir les feuilles du classeur, à extraire les objets OLE correspondants et à enregistrer les fichiers MOL extraits. Suivez les étapes ci-dessous pour terminer cette tâche avec succès.

## Étape 1 : Définir les répertoires source et de sortie
Tout d'abord, nous devons définir les répertoires source et de sortie dans notre code. Ces répertoires indiquent où se trouve le classeur Excel source et où les fichiers MOL extraits seront enregistrés. Voici le code correspondant :

```csharp
// Annuaires
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Assurez-vous de spécifier les chemins appropriés selon vos besoins.

## Étape 2 : chargement du classeur Excel
L'étape suivante consiste à charger le classeur Excel contenant les objets OLE intégrés et les fichiers MOL. Voici le code pour charger le classeur :

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Assurez-vous de spécifier correctement le nom du fichier source dans le code.

## Étape 3 : Parcourir les feuilles et extraire les fichiers MOL
Nous allons maintenant parcourir chaque feuille du classeur et extraire les objets OLE correspondants, qui contiennent les fichiers MOL. Voici le code correspondant :

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Ce code parcourt chaque feuille du classeur, récupère les objets OLE et enregistre les fichiers MOL extraits dans le répertoire de sortie.

### Exemple de code source pour extraire le fichier Mol intégré à l'aide d'Aspose.Cells pour .NET 
```csharp
//répertoires
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Conclusion
Félicitation ! Vous avez appris à extraire un fichier MOL intégré d'un classeur Excel à l'aide d'Aspose.Cells pour .NET. Vous pouvez maintenant appliquer ces connaissances pour extraire des fichiers MOL de vos propres classeurs Excel. N'hésitez pas à explorer davantage la bibliothèque Aspose.Cells et à découvrir ses autres fonctionnalités puissantes.

### FAQ

#### Q : Qu'est-ce qu'un fichier MOL ?
 
R : Un fichier MOL est un format de fichier utilisé pour représenter des structures chimiques en chimie computationnelle. Il contient des informations sur les atomes, les liaisons et d'autres propriétés moléculaires.

#### Q : Cette méthode fonctionne-t-elle avec tous les types de fichiers Excel ?

R : Oui, cette méthode fonctionne avec tous les types de fichiers Excel pris en charge par Aspose.Cells.

#### Q : Puis-je extraire plusieurs fichiers MOL à la fois ?

R : Oui, vous pouvez extraire plusieurs fichiers MOL à la fois en parcourant les objets OLE sur chaque feuille du classeur.