---
title: Filtrer les noms définis lors du chargement du classeur
linktitle: Filtrer les noms définis lors du chargement du classeur
second_title: Référence de l'API Aspose.Cells pour .NET
description: Découvrez comment filtrer les noms définis lors du chargement d'un classeur Excel avec Aspose.Cells pour .NET.
type: docs
weight: 100
url: /fr/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
Lorsque vous travaillez avec des classeurs Excel dans une application .NET, il est souvent nécessaire de filtrer les données au chargement. Aspose.Cells for .NET est une bibliothèque puissante permettant de manipuler facilement les classeurs Excel. Dans ce guide, nous allons vous montrer comment filtrer les noms définis lors du chargement d'un classeur à l'aide d'Aspose.Cells pour .NET. Suivez ces étapes simples pour obtenir les résultats souhaités :

## Étape 1 : Spécifier les options de chargement

Tout d’abord, vous devez spécifier les options de chargement pour définir le comportement de chargement du classeur. Dans notre cas, nous voulons ignorer les noms définis lors du chargement. Voici comment procéder à l'aide d'Aspose.Cells :

```csharp
// Spécifie les options de chargement
LoadOptions opts = new LoadOptions();

// Ne chargez pas les noms définis
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## Étape 2 : Charger le classeur

Une fois les options de chargement configurées, vous pouvez charger le classeur Excel à partir du fichier source. Assurez-vous de spécifier le chemin d'accès correct au fichier. Voici un exemple de code :

```csharp
// Charger le classeur
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## Étape 3 : Enregistrez le classeur filtré

Après avoir chargé le classeur, vous pouvez effectuer d'autres opérations ou modifications selon vos besoins. Vous pouvez ensuite enregistrer le classeur filtré dans un fichier de sortie. Voici comment:

```csharp
// Enregistrez le classeur Excel filtré
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Exemple de code source pour filtrer les noms définis lors du chargement du classeur à l'aide d'Aspose.Cells pour .NET 
```csharp
//Spécifier les options de chargement
LoadOptions opts = new LoadOptions();
//Nous ne voulons pas charger les noms définis
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//Charger le classeur
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Enregistrez le fichier Excel de sortie, cela cassera la formule en C1
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Conclusion

Le filtrage des noms définis lors du chargement d'un classeur Excel peut être critique pour de nombreuses applications. Aspose.Cells for .NET facilite cette tâche en fournissant des options flexibles pour le chargement et le filtrage des données. En suivant les étapes de ce guide, vous pourrez filtrer efficacement les noms définis et obtenir les résultats souhaités dans vos classeurs Excel.


### FAQ

#### Q : Aspose.Cells prend-il en charge d'autres langages de programmation que C# ?
    
R : Oui, Aspose.Cells est une bibliothèque multiplateforme qui prend en charge de nombreux langages de programmation tels que Java, Python, C.++et beaucoup plus.

#### Q : Puis-je filtrer d'autres types de données lors du chargement d'un classeur avec Aspose.Cells ?
    
R : Oui, Aspose.Cells propose une gamme d'options de filtrage des données, notamment des formules, des styles, des macros, etc.

#### Q : Aspose.Cells conserve-t-il la mise en forme et les propriétés du classeur d'origine ?
    
R : Oui, Aspose.Cells conserve le formatage, les styles, les formules et autres propriétés du classeur d'origine lorsque vous travaillez avec des fichiers Excel.