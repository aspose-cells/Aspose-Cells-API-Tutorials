---
title: Imposta il numero della prima pagina di Excel
linktitle: Imposta il numero della prima pagina di Excel
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come impostare il numero della prima pagina in Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 90
url: /it/net/excel-page-setup/set-excel-first-page-number/
---
In questo tutorial ti spiegheremo come impostare il numero della prima pagina in Excel utilizzando Aspose.Cells per .NET. Utilizzeremo il codice sorgente C# per illustrare il processo.

## Passaggio 1: configurazione dell'ambiente

Assicurati di avere Aspose.Cells per .NET installato sul tuo computer. Crea anche un nuovo progetto nel tuo ambiente di sviluppo preferito.

## Passaggio 2: importa le librerie necessarie

Nel file di codice, importa le librerie necessarie per lavorare con Aspose.Cells. Ecco il codice corrispondente:

```csharp
using Aspose.Cells;
```

## Passaggio 3: impostare la directory dei dati

Imposta la directory dei dati in cui desideri salvare il file Excel modificato. Utilizza il seguente codice:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Assicurati di specificare il percorso completo della directory.

## Passaggio 4: creazione della cartella di lavoro e del foglio di lavoro

Crea un nuovo oggetto cartella di lavoro e vai al primo foglio di lavoro nella cartella di lavoro utilizzando il seguente codice:

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Questo creerà una cartella di lavoro vuota con un foglio di lavoro.

## Passaggio 5: impostazione del numero della prima pagina

Imposta il numero della prima pagina delle pagine del foglio di lavoro utilizzando il seguente codice:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Ciò imposterà il numero della prima pagina su 2.

## Passaggio 6: salvataggio della cartella di lavoro modificata

Salvare la cartella di lavoro modificata utilizzando il seguente codice:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Ciò salverà la cartella di lavoro modificata nella directory dei dati specificata.

### Codice sorgente di esempio per Imposta il numero della prima pagina di Excel utilizzando Aspose.Cells per .NET 
```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creazione di un'istanza di un oggetto cartella di lavoro
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

### Domande frequenti

#### Q1: posso impostare un numero di prima pagina diverso per ciascun foglio di lavoro?

 R1: Sì, puoi impostare un numero di prima pagina diverso per ciascun foglio di lavoro accedendo a`FirstPageNumber`proprietà del rispettivo foglio di lavoro`PageSetup` oggetto.

#### Q2: Come posso controllare il numero della prima pagina di un foglio di calcolo esistente?

 A2: Puoi controllare il numero della prima pagina di un foglio di lavoro esistente accedendo a`FirstPageNumber` proprietà del`PageSetup` oggetto corrispondente a quel foglio di lavoro.

#### Q3: La numerazione delle pagine inizia sempre da 1 per impostazione predefinita?

R3: Sì, la numerazione delle pagine inizia da 1 per impostazione predefinita in Excel. Tuttavia, puoi utilizzare il codice mostrato in questo tutorial per impostare un numero diverso per la prima pagina.

#### Q4: Le modifiche al numero della prima pagina sono permanenti nel file Excel modificato?

R4: Sì, le modifiche apportate al numero della prima pagina vengono salvate in modo permanente nel file Excel modificato.

#### Q5: questo metodo funziona con tutti i formati di file Excel, come .xls e .xlsx?

A5: Sì, questo metodo funziona per tutti i formati di file Excel supportati da Aspose.Cells, inclusi .xls e .xlsx.