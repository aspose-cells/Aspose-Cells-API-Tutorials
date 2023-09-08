---
title: Visualizza e nascondi le intestazioni delle colonne delle righe del foglio di lavoro
linktitle: Visualizza e nascondi le intestazioni delle colonne delle righe del foglio di lavoro
second_title: Aspose.Cells per riferimento API .NET
description: Visualizza o nascondi le intestazioni di righe e colonne nel foglio di lavoro di Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 40
url: /it/net/excel-display-settings-csharp-tutorials/display-and-hide-row-column-headers-of-worksheet/
---
In questo tutorial, ti mostreremo come visualizzare o nascondere le intestazioni di righe e colonne di un foglio di lavoro Excel utilizzando il codice sorgente C# con Aspose.Cells per .NET. Seguire i passaggi seguenti per ottenere il risultato desiderato.

## Passaggio 1: importa le librerie necessarie

Assicurati di aver installato la libreria Aspose.Cells per .NET e importa le librerie necessarie nel tuo progetto C#.

```csharp
using Aspose.Cells;
using System.IO;
```

## Passaggio 2: imposta il percorso della directory e apri il file Excel

 Imposta il percorso della directory contenente il tuo file Excel, quindi apri il file creando un flusso di file e istanziando un file`Workbook` oggetto.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Passaggio 3: vai al primo foglio di lavoro e nascondi le intestazioni di righe e colonne

 Accedi al primo foglio di lavoro nel file Excel utilizzando il file`Worksheets` proprietà del`Workbook` oggetto. Quindi utilizzare il`IsRowColumnHeadersVisible` proprietà del`Worksheet` oggetto per nascondere le intestazioni di riga e colonna.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. IsRowColumnHeadersVisible = false;
```

## Passaggio 4: salva le modifiche

 Una volta apportate le modifiche necessarie, salvare il file Excel modificato utilizzando il file`Save` metodo del`Workbook` oggetto.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Codice sorgente di esempio per visualizzare e nascondere le intestazioni delle colonne delle righe del foglio di lavoro utilizzando Aspose.Cells per .NET 
```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creazione di un flusso di file contenente il file Excel da aprire
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Creazione di un'istanza di un oggetto cartella di lavoro
// Apertura del file Excel tramite il flusso di file
Workbook workbook = new Workbook(fstream);
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Nascondere le intestazioni di righe e colonne
worksheet.IsRowColumnHeadersVisible = false;
// Salvataggio del file Excel modificato
workbook.Save(dataDir + "output.xls");
// Chiusura del flusso di file per liberare tutte le risorse
fstream.Close(); 
```

## Conclusione

Questa guida passo passo ti ha mostrato come visualizzare o nascondere le intestazioni di righe e colonne in un foglio di calcolo Excel utilizzando Aspose.Cells per .NET. Utilizzando il codice sorgente C# fornito, puoi personalizzare facilmente la visualizzazione delle intestazioni nei file Excel.

### Domande frequenti (FAQ)

#### Cos'è Aspose.Cells per .NET?

Aspose.Cells per .NET è una potente libreria per manipolare file Excel in applicazioni .NET.

#### Come posso installare Aspose.Cells per .NET?

 Per installare Aspose.Cells per .NET, è necessario scaricare il relativo pacchetto da[Rilasci Aspose](https://releases/aspose.com/cells/net/) e aggiungilo al tuo progetto .NET.

#### Come posso mostrare o nascondere le intestazioni di righe e colonne di un foglio di calcolo Excel con Aspose.Cells per .NET?

 Puoi usare il`IsRowColumnHeadersVisible` proprietà del`Worksheet`oggetto per visualizzare o nascondere le intestazioni di righe e colonne. Impostalo su`true` per mostrarli e per`false` per nasconderli.

#### Quali altri formati di file Excel sono supportati da Aspose.Cells per .NET?

Aspose.Cells per .NET supporta vari formati di file Excel, come XLS, XLSX, CSV, HTML, PDF e molti altri.
