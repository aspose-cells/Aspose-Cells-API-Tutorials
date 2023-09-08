---
title: Ajuster le niveau de compression
linktitle: Ajuster le niveau de compression
second_title: Référence de l'API Aspose.Cells pour .NET
description: Réduisez la taille de vos classeurs Excel en ajustant le niveau de compression avec Aspose.Cells pour .NET.
type: docs
weight: 50
url: /fr/net/excel-workbook/adjust-compression-level/
---
Dans ce didacticiel étape par étape, nous expliquerons le code source C# fourni qui vous permettra d'ajuster le niveau de compression à l'aide d'Aspose.Cells pour .NET. Suivez les étapes ci-dessous pour ajuster le niveau de compression dans votre classeur Excel.

## Étape 1 : Définir les répertoires source et de sortie

```csharp
// répertoire source
string sourceDir = RunExamples.Get_SourceDirectory();
// Répertoire de sortie
string outDir = RunExamples.Get_OutputDirectory();
```

Dans cette première étape, nous définissons les répertoires source et de sortie des fichiers Excel.

## Étape 2 : Charger le classeur Excel

```csharp
// Charger le classeur Excel
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

Nous chargeons le classeur Excel à partir du fichier spécifié en utilisant le`Workbook` classe d’Aspose.Cells.

## Étape 3 : Définir les options de sauvegarde

```csharp
// Définir les options de sauvegarde
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Nous créons une instance du`XlsbSaveOptions` classe pour définir les options de sauvegarde.

## Étape 4 : Ajustez le niveau de compression (Niveau 1)

```csharp
// Ajuster le niveau de compression (Niveau 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Nous ajustons le niveau de compression en réglant`CompressionType` à`Level1`. Ensuite, nous enregistrons le classeur Excel avec cette option de compression spécifiée.

## Étape 5 : Ajustez le niveau de compression (niveau 6)

```csharp
// Ajustez le niveau de compression (Niveau 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Nous répétons le processus pour ajuster le niveau de compression à`Level6` et enregistrez le classeur Excel avec cette option.

## Étape 6 : Ajustez le niveau de compression (niveau 9)

```csharp
// Ajustez le niveau de compression (Niveau 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Nous répétons le processus une dernière fois pour ajuster le niveau de compression à`Level9` et enregistrez le classeur Excel avec cette option.

### Exemple de code source pour ajuster le niveau de compression à l’aide d’Aspose.Cells pour .NET 
```csharp
//Répertoire source
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Conclusion

Félicitation ! Vous avez appris à ajuster le niveau de compression dans un classeur Excel à l'aide d'Aspose.Cells pour .NET. Expérimentez avec différents niveaux de compression pour trouver celui qui correspond le mieux à vos besoins.

### FAQ

#### Q : Qu’est-ce que la compression dans un classeur Excel ?

R : La compression dans un classeur Excel est un processus de réduction de la taille du fichier à l’aide d’algorithmes de compression. Cela réduit l'espace de stockage requis et améliore les performances lors du chargement et de la manipulation du fichier.

#### Q : Quels niveaux de compression sont disponibles avec Aspose.Cells ?

R : Avec Aspose.Cells, vous pouvez régler le niveau de compression de 1 à 9. Plus le niveau de compression est élevé, plus la taille du fichier sera petite, mais cela peut également augmenter le temps de traitement.

#### Q : Comment choisir le bon niveau de compression pour mon classeur Excel ?

: Le choix du niveau de compression dépend de vos besoins spécifiques. Si vous souhaitez une compression maximale et que le temps de traitement ne soit pas un problème, vous pouvez opter pour le niveau 9. Si vous préférez un compromis entre la taille du fichier et le temps de traitement, vous pouvez choisir un niveau intermédiaire.

#### Q : La compression affecte-t-elle la qualité des données dans le classeur Excel ?

R : Non, la compression n'affecte pas la qualité des données dans le classeur Excel. Il réduit simplement la taille du fichier à l'aide de techniques de compression sans altérer les données elles-mêmes.

#### Q : Puis-je ajuster le niveau de compression après avoir enregistré le fichier Excel ?

R : Non, une fois que vous avez enregistré le fichier Excel avec un niveau de compression spécifique, vous ne pouvez pas ajuster le niveau de compression ultérieurement. Vous devrez enregistrer à nouveau le fichier avec le nouveau niveau de compression si vous souhaitez le modifier.