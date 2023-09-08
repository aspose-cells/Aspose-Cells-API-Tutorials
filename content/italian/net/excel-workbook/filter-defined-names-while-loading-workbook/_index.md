---
title: Filtra i nomi definiti durante il caricamento della cartella di lavoro
linktitle: Filtra i nomi definiti durante il caricamento della cartella di lavoro
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come filtrare i nomi definiti durante il caricamento di una cartella di lavoro Excel con Aspose.Cells per .NET.
type: docs
weight: 100
url: /it/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
Quando si lavora con cartelle di lavoro di Excel in un'applicazione .NET, è spesso necessario filtrare i dati durante il caricamento. Aspose.Cells per .NET è una potente libreria per manipolare facilmente le cartelle di lavoro di Excel. In questa guida, ti mostreremo come filtrare i nomi definiti durante il caricamento di una cartella di lavoro utilizzando Aspose.Cells per .NET. Segui questi semplici passaggi per ottenere i risultati desiderati:

## Passaggio 1: specificare le opzioni di caricamento

Innanzitutto è necessario specificare le opzioni di caricamento per definire il comportamento di caricamento della cartella di lavoro. Nel nostro caso, vogliamo ignorare i nomi impostati al momento del caricamento. Ecco come farlo utilizzando Aspose.Cells:

```csharp
// Specifica le opzioni di caricamento
LoadOptions opts = new LoadOptions();

// Non caricare nomi definiti
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## Passaggio 2: caricare la cartella di lavoro

Una volta configurate le opzioni di caricamento, è possibile caricare la cartella di lavoro di Excel dal file di origine. Assicurati di specificare il percorso file corretto. Ecco un codice di esempio:

```csharp
// Carica la cartella di lavoro
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## Passaggio 3: salva la cartella di lavoro filtrata

Dopo aver caricato la cartella di lavoro, è possibile eseguire altre operazioni o modifiche secondo necessità. Quindi puoi salvare la cartella di lavoro filtrata in un file di output. Ecco come:

```csharp
// Salva la cartella di lavoro Excel filtrata
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Codice sorgente di esempio per Filtra nomi definiti durante il caricamento della cartella di lavoro utilizzando Aspose.Cells per .NET 
```csharp
//Specificare le opzioni di caricamento
LoadOptions opts = new LoadOptions();
//Non vogliamo caricare nomi definiti
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//Carica la cartella di lavoro
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Salva il file Excel di output, interromperà la formula in C1
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Conclusione

Il filtraggio dei nomi definiti durante il caricamento di una cartella di lavoro di Excel può essere fondamentale per molte applicazioni. Aspose.Cells per .NET semplifica questo compito fornendo opzioni flessibili per caricare e filtrare i dati. Seguendo i passaggi di questa guida, sarai in grado di filtrare in modo efficace i nomi definiti e ottenere i risultati desiderati nelle cartelle di lavoro di Excel.


### Domande frequenti

#### D: Aspose.Cells supporta altri linguaggi di programmazione oltre a C#?
    
R: Sì, Aspose.Cells è una libreria multipiattaforma che supporta molti linguaggi di programmazione come Java, Python, C++e molti altri.

#### D: Posso filtrare altri tipi di dati durante il caricamento di una cartella di lavoro con Aspose.Cells?
    
R: Sì, Aspose.Cells offre una gamma di opzioni di filtro per i dati tra cui formule, stili, macro, ecc.

#### D: Aspose.Cells conserva la formattazione e le proprietà della cartella di lavoro originale?
    
R: Sì, Aspose.Cells mantiene la formattazione, gli stili, le formule e altre proprietà della cartella di lavoro originale quando si lavora con file Excel.