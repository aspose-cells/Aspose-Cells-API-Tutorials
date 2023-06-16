---
title: Anteprima dell'interruzione di pagina del foglio di lavoro
linktitle: Anteprima dell'interruzione di pagina del foglio di lavoro
second_title: Riferimento all'API Aspose.Cells per .NET
description: Guida passo passo per mostrare l'anteprima dell'interruzione di pagina del foglio di lavoro utilizzando Aspose.Cells per .NET.
type: docs
weight: 110
url: /it/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
In questo tutorial, spiegheremo come mostrare l'anteprima dell'interruzione di pagina di un foglio di lavoro utilizzando Aspose.Cells per .NET. Segui questi passaggi per ottenere il risultato desiderato:

## Passaggio 1: configurazione dell'ambiente

Assicurati di aver installato Aspose.Cells per .NET e di configurare il tuo ambiente di sviluppo. Inoltre, assicurati di avere una copia del file Excel su cui desideri visualizzare l'anteprima dell'interruzione di pagina.

## Passaggio 2: importare le dipendenze necessarie

Aggiungi le direttive necessarie per utilizzare le classi da Aspose.Cells:

```csharp
using Aspose.Cells;
using System.IO;
```

## Passaggio 3: inizializzazione del codice

Inizia inizializzando il percorso della directory contenente i tuoi documenti Excel:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Passaggio 4: apertura del file Excel

 Creare un`FileStream`oggetto contenente il file Excel da aprire:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Istanza a`Workbook` oggetto e aprire il file Excel utilizzando il flusso di file:

```csharp
Workbook workbook = new Workbook(fstream);
```

## Passaggio 5: accesso al foglio di calcolo

Passare al primo foglio di lavoro nel file Excel:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Passaggio 6: visualizzazione dell'anteprima pagina per pagina

Attiva l'anteprima pagina per foglio di lavoro:

```csharp
worksheet. IsPageBreakPreview = true;
```

## Passaggio 7: salvataggio delle modifiche

Salva le modifiche apportate al file Excel:

```csharp
workbook.Save(dataDir + "output.xls");
```

## Passaggio 8: chiusura del flusso di file

Chiudi il flusso di file per rilasciare tutte le risorse:

```csharp
fstream.Close();
```

### Esempio di codice sorgente per l'anteprima dell'interruzione di pagina del foglio di lavoro utilizzando Aspose.Cells per .NET 
```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creazione di un flusso di file contenente il file Excel da aprire
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Istanziare un oggetto Workbook
// Apertura del file Excel tramite il flusso di file
Workbook workbook = new Workbook(fstream);
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Visualizzazione del foglio di lavoro nell'anteprima dell'interruzione di pagina
worksheet.IsPageBreakPreview = true;
// Salvataggio del file Excel modificato
workbook.Save(dataDir + "output.xls");
// Chiusura del flusso di file per liberare tutte le risorse
fstream.Close();
```

## Conclusione

In questo tutorial, hai imparato a visualizzare l'anteprima dell'interruzione di pagina di un foglio di lavoro utilizzando Aspose.Cells per .NET. Seguendo i passaggi descritti, puoi facilmente controllare l'aspetto e il layout dei tuoi file Excel.

### Domande frequenti (FAQ)

#### Cos'è Aspose.Cells per .NET?

Aspose.Cells per .NET è una popolare libreria software per la manipolazione di file Excel nelle applicazioni .NET.

#### Posso mostrare l'anteprima pagina per foglio di lavoro specifico anziché l'intero foglio di lavoro?

Sì, utilizzando Aspose.Cells è possibile abilitare l'anteprima dell'interruzione di pagina per un foglio di lavoro specifico accedendo all'oggetto Worksheet corrispondente.

#### Aspose.Cells supporta altre funzionalità di modifica dei file Excel?

Sì, Aspose.Cells offre una vasta gamma di funzionalità per la modifica e la manipolazione di file Excel, come l'aggiunta di dati, la formattazione, la creazione di grafici, ecc.

#### Aspose.Cells funziona solo con file Excel in formato .xls?

No, Aspose.Cells supporta vari formati di file Excel inclusi .xls e .xlsx.
	