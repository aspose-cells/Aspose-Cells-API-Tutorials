---
title: Obtenir les détails d'Odata
linktitle: Obtenir les détails d'Odata
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment récupérer les détails OData d'un classeur Excel à l'aide d'Aspose.Cells pour .NET.
type: docs
weight: 110
url: /fr/net/excel-workbook/get-odata-details/
---
L'utilisation d'OData est courante lorsqu'il s'agit de récupérer des données structurées à partir de sources de données externes. Avec Aspose.Cells pour .NET, vous pouvez facilement récupérer les détails OData à partir d'un classeur Excel. Suivez les étapes ci-dessous pour obtenir les résultats souhaités :

## Étape 1 : Spécifiez le répertoire source

Tout d’abord, vous devez spécifier le répertoire source dans lequel se trouve le fichier Excel contenant les détails OData. Voici comment procéder à l'aide d'Aspose.Cells :

```csharp
// répertoire source
string SourceDir = RunExamples.Get_SourceDirectory();
```

## Étape 2 : Charger le classeur

Une fois le répertoire source spécifié, vous pouvez charger le classeur Excel à partir du fichier. Voici un exemple de code :

```csharp
// Charger le classeur
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
```

## Étape 3 : Obtenez les détails d’OData

Après avoir chargé le classeur, vous pouvez accéder aux détails OData à l'aide de la collection PowerQueryFormulas. Voici comment:

```csharp
// Récupérer la collection de formules Power Query
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;

// Parcourez chaque formule Power Query
foreach(PowerQueryFormula PQF in PQFcoll)
{
Console.WriteLine("Connection name: " + PQF.Name);

// Récupérer la collection d'éléments de formule Power Query
PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;

// Parcourez chaque élément de formule Power Query
foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
{
Console.WriteLine("Name: " + PQFI.Name);
Console.WriteLine("Value: " + PQFI.Value);
}
}

Console.WriteLine("GetOdataDetails executed successfully.");
```

### Exemple de code source pour obtenir des détails Odata à l’aide d’Aspose.Cells pour .NET 
```csharp
// répertoire source
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;
foreach (PowerQueryFormula PQF in PQFcoll)
{
	Console.WriteLine("Connection Name: " + PQF.Name);
	PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;
	foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
	{
		Console.WriteLine("Name: " + PQFI.Name);
		Console.WriteLine("Value: " + PQFI.Value);
	}
}
Console.WriteLine("GetOdataDetails executed successfully.");
```

## Conclusion

Récupérer les détails OData d'un classeur Excel est désormais facile avec Aspose.Cells pour .NET. En suivant les étapes décrites dans ce guide, vous pourrez accéder et traiter efficacement les données OData. Expérimentez avec vos propres fichiers Excel contenant des détails OData et tirez le meilleur parti de cette fonctionnalité puissante.

### FAQ

#### Q : Aspose.Cells prend-il en charge d'autres sources de données en plus d'OData ?
    
: Oui, Aspose.Cells prend en charge plusieurs sources de données telles que les bases de données SQL, les fichiers CSV, les services Web, etc.

#### Q : Comment puis-je utiliser les détails OData récupérés dans mon application ?
    
R : Une fois que vous avez récupéré les détails OData à l'aide d'Aspose.Cells, vous pouvez les utiliser pour l'analyse de données, la génération de rapports ou toute autre manipulation dans votre application.

#### Q : Puis-je filtrer ou trier les données OData lors de la récupération avec Aspose.Cells ?
    
R : Oui, Aspose.Cells offre des fonctionnalités avancées pour filtrer, trier et manipuler les données OData afin de répondre à vos besoins spécifiques.

#### Q : Puis-je automatiser le processus de récupération des détails OData avec Aspose.Cells ?
    
R : Oui, vous pouvez automatiser le processus de récupération des détails OData en intégrant Aspose.Cells dans vos flux de travail ou en utilisant des scripts de programmation.