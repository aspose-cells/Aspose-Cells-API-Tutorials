---
title: Dividi i riquadri del foglio di lavoro
linktitle: Dividi i riquadri del foglio di lavoro
second_title: Riferimento all'API Aspose.Cells per .NET
description: Guida dettagliata per dividere i riquadri in un foglio di lavoro Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 130
url: /it/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
In questo tutorial, spiegheremo come dividere i riquadri in un foglio di lavoro Excel utilizzando Aspose.Cells per .NET. Segui questi passaggi per ottenere il risultato desiderato:

## Passaggio 1: configurazione dell'ambiente

Assicurati di aver installato Aspose.Cells per .NET e di configurare il tuo ambiente di sviluppo. Inoltre, assicurati di avere una copia del file Excel su cui vuoi dividere i riquadri.

## Passaggio 2: importare le dipendenze necessarie

Aggiungi le direttive necessarie per utilizzare le classi da Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Passaggio 3: inizializzazione del codice

Inizia inizializzando il percorso della directory contenente i tuoi documenti Excel:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Passaggio 4: apertura del file Excel

 Crea un'istanza di un nuovo`Workbook` oggetto e aprire il file Excel utilizzando il`Open` metodo:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Passaggio 5: definire la cella attiva

 Imposta la cella attiva del foglio di lavoro utilizzando il`ActiveCell` proprietà:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Tappa 6: Divisione dei lembi

 Dividi la finestra del foglio di lavoro usando il`Split` metodo:

```csharp
book.Worksheets[0].Split();
```

## Passaggio 7: salvataggio delle modifiche

Salva le modifiche apportate al file Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### Esempio di codice sorgente per Dividi riquadri del foglio di lavoro utilizzando Aspose.Cells per .NET 

```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creare un'istanza di una nuova cartella di lavoro e aprire un file modello
Workbook book = new Workbook(dataDir + "Book1.xls");
// Imposta la cella attiva
book.Worksheets[0].ActiveCell = "A20";
// Dividi la finestra del foglio di lavoro
book.Worksheets[0].Split();
// Salva il file excel
book.Save(dataDir + "output.xls");
```

## Conclusione

In questo tutorial, hai imparato a dividere i riquadri in un foglio di lavoro di Excel utilizzando Aspose.Cells per .NET. Seguendo i passaggi descritti, puoi facilmente personalizzare l'aspetto e il comportamento dei tuoi file Excel.

### Domande frequenti (FAQ)

#### Cos'è Aspose.Cells per .NET?

Aspose.Cells per .NET è una popolare libreria software per la manipolazione di file Excel nelle applicazioni .NET.

#### Come posso impostare la cella attiva di un foglio di lavoro in Aspose.Cells?

 È possibile impostare la cella attiva utilizzando il`ActiveCell`proprietà dell'oggetto Worksheet.

#### Posso dividere solo i riquadri orizzontali o verticali della finestra del foglio di lavoro?

 Sì, utilizzando Aspose.Cells puoi dividere solo riquadri orizzontali o verticali utilizzando i metodi appropriati come`SplitColumn` O`SplitRow`.

#### Aspose.Cells funziona solo con file Excel in formato .xls?

No, Aspose.Cells supporta vari formati di file Excel inclusi .xls e .xlsx.