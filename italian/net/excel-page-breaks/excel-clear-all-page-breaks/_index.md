---
title: Excel Cancella tutte le interruzioni di pagina
linktitle: Excel Cancella tutte le interruzioni di pagina
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come rimuovere tutte le interruzioni di pagina in Excel con Aspose.Cells per .NET. Tutorial passo dopo passo per ripulire i file Excel.
type: docs
weight: 20
url: /it/net/excel-page-breaks/excel-clear-all-page-breaks/
---

La rimozione delle interruzioni di pagina in un file Excel è un passaggio essenziale quando si gestiscono report o fogli di calcolo. In questo tutorial, ti guideremo passo dopo passo per comprendere e implementare il codice sorgente C# fornito per rimuovere tutte le interruzioni di pagina in un file Excel utilizzando la libreria Aspose.Cells per .NET.

## Passaggio 1: preparazione dell'ambiente

 Prima di iniziare, assicurati di avere Aspose.Cells per .NET installato sul tuo computer. È possibile scaricare la libreria dal[Aspose Rilasci](https://releases.aspose.com/cells/net) installarlo seguendo le istruzioni fornite.

Una volta completata l'installazione, crea un nuovo progetto C# nel tuo ambiente di sviluppo integrato (IDE) preferito e importa la libreria Aspose.Cells per .NET.

## Passaggio 2: configurazione del percorso della directory del documento

 Nel codice sorgente fornito, è necessario specificare il percorso della directory in cui si desidera salvare il file Excel generato. Modifica il`dataDir` variabile sostituendo "YOUR DOCUMENT DIRECTORY" con il percorso assoluto della directory sulla tua macchina.

```csharp
// Il percorso della directory dei documenti.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## Passaggio 3: creazione di un oggetto cartella di lavoro

Per iniziare, dobbiamo creare un oggetto Workbook che rappresenti il nostro file Excel. Ciò può essere ottenuto utilizzando la classe Workbook fornita da Aspose.Cells.

```csharp
// Istanziare un oggetto Workbook
Workbook workbook = new Workbook();
```

## Passaggio 4: rimuovere le interruzioni di pagina

 Ora rimuoveremo tutte le interruzioni di pagina nel nostro foglio di lavoro di Excel. Nel codice di esempio, usiamo il`Clear()` metodi per le interruzioni di pagina orizzontali e verticali per rimuoverle tutte.

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
```

## Passaggio 5: salvare il file Excel

 Una volta rimosse tutte le interruzioni di pagina, possiamo salvare il file Excel finale. Usa il`Save()` metodo per specificare il percorso completo del file di output.

```csharp
// Salva il file Excel.
workbook.Save(dataDir + "ClearingPageBreaks_out.xls");
```

### Esempio di codice sorgente per Excel Cancella tutte le interruzioni di pagina utilizzando Aspose.Cells per .NET 

```csharp

// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Istanziare un oggetto Workbook
Workbook workbook = new Workbook();
// Cancellazione di tutte le interruzioni di pagina
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
// Salva il file Excel.
workbook.Save(dataDir + "ClearAllPageBreaks_out.xls");

```

## Conclusione

In questo tutorial, abbiamo imparato come rimuovere tutte le interruzioni di pagina in un file Excel utilizzando Aspose.Cells per .NET. Seguendo i passaggi forniti, puoi gestire e ripulire facilmente le interruzioni di pagina indesiderate nei file Excel generati dinamicamente. Sentiti libero di esplorare ulteriormente le funzionalità offerte da Aspose.Cells per operazioni più avanzate.

### Domande frequenti

#### D: Aspose.Cells per .NET è una libreria gratuita?

R: Aspose.Cells per .NET è una libreria commerciale, ma offre una versione di prova gratuita che puoi utilizzare per valutarne la funzionalità.

#### D: La rimozione delle interruzioni di pagina influisce su altri elementi del foglio di lavoro?

R: No, l'eliminazione delle interruzioni di pagina modifica solo le interruzioni di pagina stesse e non influisce su altri dati o formattazione nel foglio di lavoro.

#### D: Posso rimuovere in modo selettivo alcune interruzioni di pagina specifiche in Excel?

A: Sì, con Aspose.Cells puoi accedere individualmente a ogni interruzione di pagina e rimuoverla se necessario utilizzando metodi appropriati.

#### D: Quali altri formati di file Excel sono supportati da Aspose.Cells per .NET?

R: Aspose.Cells per .NET supporta vari formati di file Excel, come XLSX, XLSM, CSV, HTML, PDF, ecc.

