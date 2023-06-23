---
title: Mettre à jour l'élément de formule Power Query
linktitle: Mettre à jour l'élément de formule Power Query
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment mettre à jour des éléments de formule Power Query dans des fichiers Excel à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 160
url: /fr/net/excel-workbook/update-power-query-formula-item/
---
La mise à jour d'un élément de formule Power Query est une opération courante lorsque vous travaillez avec des données dans des fichiers Excel. Avec Aspose.Cells pour .NET, vous pouvez facilement mettre à jour un élément de formule Power Query en suivant ces étapes :

## Étape 1 : Spécifiez les répertoires source et de sortie

Dans un premier temps, vous devez spécifier le répertoire source où se trouve le fichier Excel contenant les formules Power Query à mettre à jour, ainsi que le répertoire de sortie où vous souhaitez enregistrer le fichier modifié. Voici comment procéder avec Aspose.Cells :

```csharp
// répertoire des sources
string SourceDir = RunExamples.Get_SourceDirectory();

// Répertoire de sortie
string outputDir = RunExamples.Get_OutputDirectory();
```

## Étape 2 : Charger le classeur Excel source

Ensuite, vous devez charger le classeur Excel source sur lequel vous souhaitez mettre à jour l'élément de formule Power Query. Voici comment procéder :

```csharp
// Charger le classeur Excel source
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Étape 3 : Parcourir et mettre à jour les éléments de formule Power Query

Après avoir chargé le classeur, vous pouvez accéder à la collection de formules Power Query et parcourir chaque formule et ses éléments. Dans cet exemple, nous recherchons l'élément de formule portant le nom "Source" et mettons à jour sa valeur. Voici un exemple de code pour mettre à jour un élément de formule Power Query :

```csharp
// Accéder à la collection de formules Power Query
DataMashup mashupData = workbook.DataMashup;

// Boucle dans les formules Power Query et leurs éléments
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## Étape 4 : Enregistrer le classeur Excel de sortie

Une fois que vous avez mis à jour l'élément de formule Power Query, vous pouvez enregistrer le classeur Excel modifié dans le répertoire de sortie spécifié. Voici comment procéder :

```csharp
// Enregistrer le classeur Excel de sortie
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Exemple de code source pour l'élément de formule de mise à jour Power Query à l'aide d'Aspose.Cells pour .NET 
```csharp
// Répertoires de travail
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Enregistrez le classeur de sortie.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Conclusion

La mise à jour des éléments de formule Power Query est une opération essentielle lors de l'utilisation d'Aspose.Cells pour manipuler et traiter des données dans des fichiers Excel. En suivant les étapes ci-dessus, vous pouvez facilement mettre à jour les éléments de formule

### FAQ

#### : Qu'est-ce que Power Query dans Excel ?
     
R : Power Query est une fonctionnalité d'Excel qui aide à collecter, transformer et charger des données à partir de différentes sources. Il offre des outils puissants pour nettoyer, combiner et remodeler les données avant de les importer dans Excel.

#### Q : Comment savoir si un élément de formule Power Query a été mis à jour avec succès ?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### Q : Puis-je mettre à jour plusieurs éléments de formule Power Query à la fois ?
    
R : Oui, vous pouvez parcourir la collection d'éléments de formule Power Query et mettre à jour plusieurs éléments en une seule boucle, en fonction de vos besoins spécifiques.

#### Q : Existe-t-il d'autres opérations que je peux effectuer sur les formules Power Query avec Aspose.Cells ?
    
R : Oui, Aspose.Cells offre une gamme complète de fonctionnalités pour travailler avec les formules Power Query, y compris la création, la suppression, la copie et la recherche de formules dans un classeur Excel.