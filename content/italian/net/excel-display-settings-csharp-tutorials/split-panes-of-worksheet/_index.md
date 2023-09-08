---
title: Riquadri divisi del foglio di lavoro
linktitle: Riquadri divisi del foglio di lavoro
second_title: Aspose.Cells per riferimento API .NET
description: Guida dettagliata per dividere i riquadri in un foglio di lavoro Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 130
url: /it/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
In questo tutorial, spiegheremo come dividere i riquadri in un foglio di lavoro Excel utilizzando Aspose.Cells per .NET. Seguire questi passaggi per ottenere il risultato desiderato:

## Passaggio 1: configurazione dell'ambiente

Assicurati di aver installato Aspose.Cells per .NET e configurato il tuo ambiente di sviluppo. Inoltre, assicurati di avere una copia del file Excel su cui desideri dividere i riquadri.

## Passaggio 2: importa le dipendenze necessarie

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

 Istanziarne uno nuovo`Workbook` oggetto e aprire il file Excel utilizzando il file`Open` metodo:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Passaggio 5: definire la cella attiva

 Imposta la cella attiva del foglio di lavoro utilizzando il`ActiveCell` proprietà:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Passaggio 6: divisione dei lembi

 Dividere la finestra del foglio di lavoro utilizzando il file`Split` metodo:

```csharp
book.Worksheets[0].Split();
```

## Passaggio 7: salvataggio delle modifiche

Salvare le modifiche apportate al file Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### Codice sorgente di esempio per i riquadri divisi del foglio di lavoro utilizzando Aspose.Cells per .NET 

```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crea un'istanza di una nuova cartella di lavoro e apri un file modello
Workbook book = new Workbook(dataDir + "Book1.xls");
// Imposta la cella attiva
book.Worksheets[0].ActiveCell = "A20";
// Dividere la finestra del foglio di lavoro
book.Worksheets[0].Split();
// Salva il file Excel
book.Save(dataDir + "output.xls");
```

## Conclusione

In questo tutorial, hai imparato come dividere i riquadri in un foglio di lavoro Excel utilizzando Aspose.Cells per .NET. Seguendo i passaggi descritti, puoi personalizzare facilmente l'aspetto e il comportamento dei tuoi file Excel.

### Domande frequenti (FAQ)

#### Cos'è Aspose.Cells per .NET?

Aspose.Cells for .NET è una popolare libreria software per la manipolazione di file Excel nelle applicazioni .NET.

#### Come posso impostare la cella attiva di un foglio di lavoro in Aspose.Cells?

 È possibile impostare la cella attiva utilizzando il`ActiveCell`proprietà dell'oggetto Foglio di lavoro.

#### Posso dividere solo i riquadri orizzontali o verticali della finestra del foglio di lavoro?

 Sì, utilizzando Aspose.Cells puoi dividere solo i riquadri orizzontali o verticali utilizzando i metodi appropriati come`SplitColumn` O`SplitRow`.

#### Aspose.Cells funziona solo con file Excel in formato .xls?

No, Aspose.Cells supporta vari formati di file Excel inclusi .xls e .xlsx.