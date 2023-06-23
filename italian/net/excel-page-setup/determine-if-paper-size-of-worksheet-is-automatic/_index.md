---
title: Determina se il formato carta del foglio di lavoro è automatico
linktitle: Determina se il formato carta del foglio di lavoro è automatico
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come determinare se il formato carta di un foglio di calcolo è automatico con Aspose.Cells per .NET.
type: docs
weight: 20
url: /it/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
In questo articolo, ti guideremo passo dopo passo per spiegare il seguente codice sorgente C#: Determina se la dimensione della carta di un foglio di lavoro è automatica utilizzando Aspose.Cells per .NET. Useremo la libreria Aspose.Cells per .NET per eseguire questa operazione. Seguire i passaggi seguenti per determinare se il formato carta di un foglio di lavoro è automatico.

## Passaggio 1: caricamento delle cartelle di lavoro
Il primo passo è caricare le cartelle di lavoro. Avremo due cartelle di lavoro: una con il formato carta automatico disabilitato e l'altra con il formato carta automatico abilitato. Ecco il codice per caricare le cartelle di lavoro:

```csharp
// directory di origine
string sourceDir = "YOUR_SOURCE_DIR";
// Cartella di destinazione
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Carica la prima cartella di lavoro con il formato carta automatico disabilitato
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Carica la seconda cartella di lavoro con il formato carta automatico abilitato
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Passaggio 2: accesso ai fogli di calcolo
Ora che abbiamo caricato le cartelle di lavoro, dobbiamo accedere ai fogli di lavoro in modo da poter controllare il formato carta automatico. Andremo al primo foglio di lavoro delle due cartelle di lavoro. Ecco il codice per accedervi:

```csharp
//Vai al primo foglio di lavoro della prima cartella di lavoro
Worksheet ws11 = wb1.Worksheets[0];

// Vai al primo foglio di lavoro della seconda cartella di lavoro
Worksheet ws12 = wb2.Worksheets[0];
```

## Passaggio 3: controllare il formato carta automatico
 In questo passaggio, verificheremo se il formato carta del foglio di lavoro è automatico. Useremo il`PageSetup.IsAutomaticPaperSize` proprietà per ottenere queste informazioni. Visualizzeremo quindi il risultato. Ecco il codice per questo:

```csharp
// Visualizza la proprietà IsAutomaticPaperSize del primo foglio di lavoro nella prima cartella di lavoro
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Visualizza la proprietà IsAutomaticPaperSize del primo foglio di lavoro nella seconda cartella di lavoro
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Esempio di codice sorgente per determinare se la dimensione della carta del foglio di lavoro è automatica utilizzando Aspose.Cells per .NET 
```csharp
//Rubrica di origine
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Cartella di destinazione
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Carica la prima cartella di lavoro con il formato carta automatico falso
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Carica la seconda cartella di lavoro con il formato carta automatico vero
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Accedi al primo foglio di lavoro di entrambe le cartelle di lavoro
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Stampa la proprietà PageSetup.IsAutomaticPaperSize di entrambi i fogli di lavoro
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Conclusione
In questo articolo, abbiamo imparato come determinare se il formato carta di un foglio di lavoro è automatico utilizzando Aspose.Cells per .NET. Abbiamo seguito i seguenti passaggi: caricamento delle cartelle di lavoro,

accesso a fogli di calcolo e controllo automatico del formato carta. Ora puoi utilizzare questa conoscenza per determinare se il formato carta dei tuoi fogli di calcolo è automatico.

### Domande frequenti

#### D: Come posso caricare cartelle di lavoro con Aspose.Cells per .NET?

A: Puoi caricare cartelle di lavoro usando la classe Workbook dalla libreria Aspose.Cells. Usare il metodo Workbook.Load per caricare una cartella di lavoro da un file.

#### D: Posso controllare il formato carta automatico per altri fogli di calcolo?

R: Sì, puoi controllare il formato carta automatico per qualsiasi foglio di lavoro accedendo alla proprietà PageSetup.IsAutomaticPaperSize dell'oggetto Worksheet corrispondente.

#### D: Come posso modificare il formato carta automatico di un foglio di calcolo?

R: Per modificare il formato carta automatico di un foglio di lavoro, è possibile utilizzare la proprietà PageSetup.IsAutomaticPaperSize e impostarla sul valore desiderato (vero o falso).

#### D: Quali altre funzionalità offre Aspose.Cells per .NET?

R: Aspose.Cells per .NET offre molte funzionalità per lavorare con fogli di calcolo, come la creazione, la modifica e la conversione di cartelle di lavoro, nonché la manipolazione di dati, formule e formattazione.