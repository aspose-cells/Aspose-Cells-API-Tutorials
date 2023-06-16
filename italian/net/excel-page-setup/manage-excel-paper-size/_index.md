---
title: Gestisci il formato carta di Excel
linktitle: Gestisci il formato carta di Excel
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come gestire le dimensioni della carta in Excel con Aspose.Cells per .NET. Tutorial passo passo con codice sorgente in C#.
type: docs
weight: 70
url: /it/net/excel-page-setup/manage-excel-paper-size/
---
In questo tutorial, ti guideremo passo dopo passo su come gestire le dimensioni della carta nel documento Excel utilizzando Aspose.Cells per .NET. Ti mostreremo come configurare il formato carta usando il codice sorgente C#.

## Passaggio 1: configurazione dell'ambiente

Assicurati di avere Aspose.Cells per .NET installato sul tuo computer. Crea anche un nuovo progetto nel tuo ambiente di sviluppo preferito.

## Passaggio 2: importa le librerie necessarie

Nel tuo file di codice, importa le librerie necessarie per lavorare con Aspose.Cells. Ecco il codice corrispondente:

```csharp
using Aspose.Cells;
```

## Passaggio 3: impostare la directory dei documenti

Imposta la directory in cui si trova il documento Excel con cui vuoi lavorare. Utilizzare il seguente codice per impostare la directory:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Assicurati di specificare il percorso completo della directory.

## Passaggio 4: creazione di un oggetto cartella di lavoro

L'oggetto Workbook rappresenta il documento Excel con cui lavorerai. Puoi crearlo usando il seguente codice:

```csharp
Workbook workbook = new Workbook();
```

Questo crea un nuovo oggetto Workbook vuoto.

## Passaggio 5: accesso al primo foglio di lavoro

Per accedere al primo foglio di calcolo del documento Excel, utilizzare il seguente codice:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

Ciò ti consentirà di lavorare con il primo foglio di lavoro nella cartella di lavoro.

## Passaggio 6: impostazione del formato carta

Utilizzare la proprietà PageSetup.PaperSize dell'oggetto Worksheet per impostare il formato della carta. In questo esempio, imposteremo il formato carta su A4. Ecco il codice corrispondente:

```csharp
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
```

Imposta il formato carta del foglio di calcolo su A4.

## Passaggio 7: salvataggio della cartella di lavoro

Per salvare le modifiche alla cartella di lavoro, utilizzare il metodo Save() dell'oggetto Workbook. Ecco il codice corrispondente:

```csharp
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```

Ciò salverà la cartella di lavoro con le modifiche alla directory specificata.

### Esempio di codice sorgente per Gestisci formato carta Excel utilizzando Aspose.Cells per .NET 
```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Istanziare un oggetto Workbook
Workbook workbook = new Workbook();
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Impostare il formato carta su A4
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
// Salva la cartella di lavoro.
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```
## Conclusione

Ora hai imparato come gestire le dimensioni della carta in un documento Excel utilizzando Aspose.Cells per .NET. Questo tutorial ti ha guidato attraverso ogni fase del processo, dalla configurazione dell'ambiente al salvataggio delle modifiche. Ora puoi utilizzare questa conoscenza per personalizzare il formato carta dei tuoi documenti Excel.

### FAQ

#### D1: Posso impostare un formato carta personalizzato diverso da A4?

R1: Sì, Aspose.Cells supporta una varietà di formati carta predefiniti, nonché la possibilità di impostare un formato carta personalizzato specificando le dimensioni desiderate.

#### D2: Come posso conoscere il formato carta corrente in un documento Excel?

 A2: Puoi usare il`PageSetup.PaperSize` proprietà del`Worksheet` oggetto per ottenere il formato carta attualmente impostato.

#### D3: È possibile impostare margini di pagina extra con il formato carta?

 A3: Sì, puoi usare`PageSetup.LeftMargin`, `PageSetup.RightMargin`, `PageSetup.TopMargin` E`PageSetup.BottomMargin` proprietà per impostare ulteriori margini della pagina oltre al formato della carta.

#### D4: Questo metodo funziona per tutti i formati di file Excel, ad esempio .xls e .xlsx?

R4: Sì, questo metodo funziona per entrambi i formati di file .xls e .xlsx.

#### D5: Posso applicare formati carta diversi a fogli di lavoro diversi nella stessa cartella di lavoro?

 R5: Sì, è possibile applicare formati carta diversi a fogli di lavoro diversi nella stessa cartella di lavoro utilizzando il file`PageSetup.PaperSize` proprietà di ogni foglio di lavoro.