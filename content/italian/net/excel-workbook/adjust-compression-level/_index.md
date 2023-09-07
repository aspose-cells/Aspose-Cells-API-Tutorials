---
title: Regola il livello di compressione
linktitle: Regola il livello di compressione
second_title: Riferimento all'API Aspose.Cells per .NET
description: Riduci le dimensioni delle cartelle di lavoro di Excel regolando il livello di compressione con Aspose.Cells per .NET.
type: docs
weight: 50
url: /it/net/excel-workbook/adjust-compression-level/
---
In questo tutorial passo-passo, spiegheremo il codice sorgente C# fornito che ti permetterà di regolare il livello di compressione usando Aspose.Cells per .NET. Seguire i passaggi seguenti per regolare il livello di compressione nella cartella di lavoro di Excel.

## Passaggio 1: imposta le directory di origine e di output

```csharp
// directory di origine
string sourceDir = RunExamples.Get_SourceDirectory();
// Cartella di destinazione
string outDir = RunExamples.Get_OutputDirectory();
```

In questo primo passaggio, definiamo le directory di origine e di output per i file Excel.

## Passaggio 2: caricare la cartella di lavoro di Excel

```csharp
//Carica la cartella di lavoro di Excel
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

 Carichiamo la cartella di lavoro di Excel dal file specificato utilizzando l'estensione`Workbook` classe da Aspose.Cells.

## Passaggio 3: imposta le opzioni di backup

```csharp
// Definisci le opzioni di backup
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Creiamo un'istanza di`XlsbSaveOptions` class per impostare le opzioni di salvataggio.

## Passaggio 4: regolare il livello di compressione (Livello 1)

```csharp
// Regola il livello di compressione (Livello 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Regoliamo il livello di compressione impostando`CompressionType` A`Level1`. Quindi salviamo la cartella di lavoro di Excel con questa opzione di compressione specificata.

## Passaggio 5: regolare il livello di compressione (Livello 6)

```csharp
// Regola il livello di compressione (Livello 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Ripetiamo il processo per regolare il livello di compressione`Level6` e salva la cartella di lavoro di Excel con questa opzione.

## Passaggio 6: regolare il livello di compressione (livello 9)

```csharp
// Regola il livello di compressione (Livello 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Ripetiamo il processo un'ultima volta per regolare il livello di compressione`Level9` e salva la cartella di lavoro di Excel con questa opzione.

### Esempio di codice sorgente per regolare il livello di compressione utilizzando Aspose.Cells per .NET 
```csharp
//Rubrica di origine
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

## Conclusione

Congratulazioni! Hai imparato come regolare il livello di compressione in una cartella di lavoro di Excel utilizzando Aspose.Cells per .NET. Sperimenta diversi livelli di compressione per trovare quello più adatto alle tue esigenze.

### Domande frequenti

#### D: Cos'è la compressione in una cartella di lavoro di Excel?

R: La compressione in una cartella di lavoro di Excel è un processo di riduzione delle dimensioni del file utilizzando algoritmi di compressione. Ciò riduce lo spazio di archiviazione richiesto e migliora le prestazioni durante il caricamento e la manipolazione del file.

#### D: Quali livelli di compressione sono disponibili con Aspose.Cells?

A: Con Aspose.Cells, puoi regolare il livello di compressione da 1 a 9. Maggiore è il livello di compressione, minore sarà la dimensione del file, ma può anche aumentare il tempo di elaborazione.

#### D: Come faccio a scegliere il giusto livello di compressione per la mia cartella di lavoro di Excel?

R: La scelta del livello di compressione dipende dalle tue esigenze specifiche. Se desideri la massima compressione e il tempo di elaborazione non è un problema, puoi scegliere il livello 9. Se preferisci un compromesso tra dimensione del file e tempo di elaborazione, puoi scegliere un livello intermedio.

#### D: La compressione influisce sulla qualità dei dati nella cartella di lavoro di Excel?

R: No, la compressione non influisce sulla qualità dei dati nella cartella di lavoro di Excel. Riduce semplicemente la dimensione del file utilizzando tecniche di compressione senza alterare i dati stessi.

#### D: Posso regolare il livello di compressione dopo aver salvato il file Excel?

R: No, una volta salvato il file Excel con un livello di compressione specifico, non è possibile regolare il livello di compressione in un secondo momento. Sarà necessario salvare nuovamente il file con il nuovo livello di compressione se si desidera modificarlo.