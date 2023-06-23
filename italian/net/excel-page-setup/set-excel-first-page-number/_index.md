---
title: Imposta il numero della prima pagina di Excel
linktitle: Imposta il numero della prima pagina di Excel
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come impostare il numero della prima pagina in Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 90
url: /it/net/excel-page-setup/set-excel-first-page-number/
---
In questo tutorial, ti illustreremo come impostare il numero della prima pagina in Excel utilizzando Aspose.Cells per .NET. Useremo il codice sorgente C# per illustrare il processo.

## Passaggio 1: configurazione dell'ambiente

Assicurati di avere Aspose.Cells per .NET installato sul tuo computer. Crea anche un nuovo progetto nel tuo ambiente di sviluppo preferito.

## Passaggio 2: importa le librerie necessarie

Nel tuo file di codice, importa le librerie necessarie per lavorare con Aspose.Cells. Ecco il codice corrispondente:

```csharp
using Aspose.Cells;
```

## Passaggio 3: impostare la directory dei dati

Impostare la directory dei dati in cui si desidera salvare il file Excel modificato. Usa il seguente codice:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Assicurati di specificare il percorso completo della directory.

## Passaggio 4: creazione della cartella di lavoro e del foglio di lavoro

Crea un nuovo oggetto cartella di lavoro e passa al primo foglio di lavoro nella cartella di lavoro utilizzando il codice seguente:

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Questo creerà una cartella di lavoro vuota con un foglio di lavoro.

## Passaggio 5: impostazione del numero della prima pagina

Impostare il numero della prima pagina delle pagine del foglio di lavoro utilizzando il seguente codice:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Questo imposterà il numero della prima pagina su 2.

## Passaggio 6: salvataggio della cartella di lavoro modificata

Salva la cartella di lavoro modificata utilizzando il seguente codice:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Ciò salverà la cartella di lavoro modificata nella directory dei dati specificata.

### Esempio di codice sorgente per Imposta il numero della prima pagina di Excel utilizzando Aspose.Cells per .NET 
```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Istanziare un oggetto Workbook
Workbook workbook = new Workbook();
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Impostazione del numero della prima pagina delle pagine del foglio di lavoro
worksheet.PageSetup.FirstPageNumber = 2;
// Salva la cartella di lavoro.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Conclusione

Ora hai imparato come impostare il numero della prima pagina in Excel utilizzando Aspose.Cells per .NET. Questo tutorial ti ha guidato attraverso ogni fase del processo, dalla configurazione dell'ambiente all'impostazione del numero della prima pagina. Ora puoi utilizzare questa conoscenza per personalizzare la numerazione delle pagine nei tuoi file Excel.

### FAQ

#### D1: Posso impostare un numero di prima pagina diverso per ogni foglio di lavoro?

 A1: Sì, puoi impostare un numero di prima pagina diverso per ogni foglio di lavoro accedendo a`FirstPageNumber`proprietà del rispettivo foglio di lavoro`PageSetup` oggetto.

#### D2: Come posso controllare il numero della prima pagina di un foglio di lavoro esistente?

 A2: è possibile controllare il numero della prima pagina di un foglio di lavoro esistente accedendo a`FirstPageNumber` proprietà del`PageSetup` oggetto corrispondente a quel foglio di lavoro.

#### D3: La numerazione delle pagine inizia sempre da 1 per impostazione predefinita?

A3: Sì, la numerazione delle pagine inizia da 1 per impostazione predefinita in Excel. Tuttavia, puoi utilizzare il codice mostrato in questo tutorial per impostare un numero di prima pagina diverso.

#### D4: Le modifiche al numero della prima pagina sono permanenti nel file Excel modificato?

R4: Sì, le modifiche apportate al numero della prima pagina vengono salvate in modo permanente nel file Excel modificato.

#### D5: Questo metodo funziona per tutti i formati di file Excel, ad esempio .xls e .xlsx?

A5: Sì, questo metodo funziona per tutti i formati di file Excel supportati da Aspose.Cells, inclusi .xls e .xlsx.