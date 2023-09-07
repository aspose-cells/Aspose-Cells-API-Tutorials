---
title: Imposta l'ordine delle pagine di Excel
linktitle: Imposta l'ordine delle pagine di Excel
second_title: Riferimento all'API Aspose.Cells per .NET
description: Guida passo passo per impostare l'ordine delle pagine in Excel utilizzando Aspose.Cells per .NET. Istruzioni dettagliate e codice sorgente inclusi.
type: docs
weight: 120
url: /it/net/excel-page-setup/set-excel-page-order/
---
In questo articolo, ti guideremo passo dopo passo per spiegare il seguente codice sorgente C# per impostare l'ordine delle pagine di Excel utilizzando Aspose.Cells per .NET. Ti mostreremo come configurare la directory dei documenti, creare un'istanza di un oggetto Workbook, ottenere il riferimento PageSetup, impostare l'ordine di stampa della pagina e salvare la cartella di lavoro.

## Passaggio 1: impostazione della directory dei documenti

 Prima di iniziare, è necessario configurare la directory dei documenti in cui si desidera salvare il file Excel. È possibile specificare il percorso della directory sostituendo il valore di`dataDir` variabile con il proprio percorso.

```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## Passaggio 2: creazione di un'istanza di un oggetto cartella di lavoro

Il primo passaggio consiste nell'istanziare un oggetto Workbook. Questo rappresenta la cartella di lavoro di Excel con cui lavoreremo.

```csharp
// Crea un'istanza di un oggetto Workbook
Workbook workbook = new Workbook();
```

## Passaggio 3: ottenere il riferimento PageSetup

Successivamente, dobbiamo ottenere il riferimento all'oggetto PageSetup del foglio di lavoro su cui vogliamo impostare l'ordine delle pagine.

```csharp
// Ottenere il riferimento PageSetup del foglio di lavoro
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Passaggio 4: impostazione dell'ordine di stampa delle pagine

Ora possiamo impostare l'ordine di stampa delle pagine. In questo esempio, stiamo usando l'opzione "OverThenDown", il che significa che le pagine verranno stampate da sinistra a destra, quindi dall'alto verso il basso.

```csharp
// Imposta l'ordine di stampa della pagina su "OverThenDown"
pageSetup.Order = PrintOrderType.OverThenDown;
```

## Passaggio 5: salvare la cartella di lavoro

Infine, salviamo la cartella di lavoro di Excel con le modifiche all'ordine delle pagine.

```csharp
// Salva la cartella di lavoro
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### Esempio di codice sorgente per Imposta ordine pagine Excel utilizzando Aspose.Cells per .NET 
```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Istanziare un oggetto Workbook
Workbook workbook = new Workbook();
// Ottenere il riferimento del PageSetup del foglio di lavoro
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Impostazione dell'ordine di stampa delle pagine su sopra e poi sotto
pageSetup.Order = PrintOrderType.OverThenDown;
// Salva la cartella di lavoro.
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## Conclusione

In questo tutorial, abbiamo spiegato come impostare l'ordine delle pagine in un file Excel utilizzando Aspose.Cells per .NET. Seguendo i passaggi forniti, è possibile configurare facilmente la directory del documento, creare un'istanza di un oggetto Workbook, ottenere il riferimento PageSetup, impostare l'ordine di stampa della pagina e salvare la cartella di lavoro.

### FAQ

#### D1: Perché è importante impostare l'ordine delle pagine in un file Excel?

La definizione dell'ordine delle pagine in un file Excel è importante perché determina come verranno stampate o visualizzate le pagine. Specificando un ordine specifico, è possibile organizzare i dati in modo logico e semplificare la lettura o la stampa del file.

#### D2: Posso utilizzare altri ordini di stampa di pagine con Aspose.Cells per .NET?

Sì, Aspose.Cells per .NET supporta ordini di stampa di più pagine come "DownThenOver", "OverThenDown", "DownThenOverThenDownAgain", ecc. Puoi scegliere quello più adatto alle tue esigenze.

#### D3: Posso impostare opzioni aggiuntive per la stampa di pagine con Aspose.Cells per .NET?

Sì, puoi impostare varie opzioni di stampa della pagina come scala, orientamento, margini, ecc., utilizzando le proprietà dell'oggetto PageSetup in Aspose.Cells per .NET.

#### D4: Aspose.Cells per .NET supporta altri formati di file Excel?

Sì, Aspose.Cells per .NET supporta un'ampia gamma di formati di file Excel come XLSX, XLS, CSV, HTML, PDF, ecc. Puoi convertire facilmente tra questi formati utilizzando le funzionalità fornite dalla libreria.