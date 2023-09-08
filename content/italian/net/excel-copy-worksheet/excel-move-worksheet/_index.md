---
title: Foglio di lavoro per lo spostamento di Excel
linktitle: Foglio di lavoro per lo spostamento di Excel
second_title: Aspose.Cells per riferimento API .NET
description: Sposta facilmente il foglio di lavoro in una cartella di lavoro Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 40
url: /it/net/excel-copy-worksheet/excel-move-worksheet/
---
In questo tutorial, ti guideremo attraverso i passaggi per spostare un foglio di lavoro in una cartella di lavoro Excel utilizzando la libreria Aspose.Cells per .NET. Seguire le istruzioni riportate di seguito per completare questa attività.


## Passaggio 1: preparazione

Assicurati di aver installato Aspose.Cells per .NET e di aver creato un progetto C# nel tuo ambiente di sviluppo integrato (IDE) preferito.

## Passaggio 2: impostare il percorso della directory del documento

 Dichiarare a`dataDir` variabile e inizializzala con il percorso della directory dei documenti. Per esempio :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assicurati di sostituire`"YOUR_DOCUMENTS_DIRECTORY"` con il percorso effettivo della directory.

## Passaggio 3: definire il percorso del file di input

 Dichiarare un`InputPath` variabile e inizializzarla con il percorso completo del file Excel esistente che si desidera modificare. Per esempio :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Assicurati di avere il file Excel`book1.xls` nella directory dei documenti o specificare il nome e il percorso corretti del file.

## Passaggio 4: apri il file Excel

 Usa il`Workbook` classe di Aspose.Cells per aprire il file Excel specificato:

```csharp
Workbook wb = new Workbook(InputPath);
```

## Passaggio 5: ottieni la raccolta di fogli di calcolo

 Creare un`WorksheetCollection` oggetto per fare riferimento ai fogli di lavoro nella cartella di lavoro:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

## Passaggio 6: ottieni il primo foglio di lavoro

Ottieni il primo foglio di lavoro nella cartella di lavoro:

```csharp
Worksheet worksheet = sheets[0];
```

## Passaggio 7: spostare il foglio di lavoro

 Usa il`MoveTo` metodo per spostare il primo foglio di lavoro nella terza posizione nella cartella di lavoro:

```csharp
worksheet.MoveTo(2);
```

## Passaggio 8: salva il file Excel modificato

Salva il file Excel con il foglio di lavoro spostato:

```csharp
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

Assicurati di specificare il percorso e il nome file desiderati per il file di output.

### Codice sorgente di esempio per il foglio di lavoro Excel Move utilizzando Aspose.Cells per .NET 
```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Apri un file Excel esistente.
Workbook wb = new Workbook(InputPath);
// Creare un oggetto Worksheets con riferimento a
// i fogli del Quaderno degli esercizi.
WorksheetCollection sheets = wb.Worksheets;
// Ottieni il primo foglio di lavoro.
Worksheet worksheet = sheets[0];
// Sposta il primo foglio nella terza posizione nella cartella di lavoro.
worksheet.MoveTo(2);
// Salva il file Excel.
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

## Conclusione

Congratulazioni! Ora hai imparato come spostare un foglio di lavoro in una cartella di lavoro di Excel utilizzando Aspose.Cells per .NET. Sentiti libero di utilizzare questo metodo nei tuoi progetti per manipolare in modo efficiente i file Excel.

### Domande frequenti

#### D. Posso spostare un foglio di lavoro in un'altra posizione nella stessa cartella di lavoro di Excel?

A.  Sì, puoi spostare un foglio di lavoro in un'altra posizione nella stessa cartella di lavoro di Excel utilizzando`MoveTo` metodo dell'oggetto foglio di lavoro. Basta specificare l'indice della posizione di destinazione nella cartella di lavoro.

#### D. Posso spostare un foglio di lavoro in un'altra cartella di lavoro di Excel?

A.  Sì, puoi spostare un foglio di lavoro in un'altra cartella di lavoro di Excel utilizzando il file`MoveTo` metodo dell'oggetto Foglio di lavoro. Basta specificare l'indice della posizione di destinazione nella cartella di lavoro di destinazione.

#### D. Il codice sorgente fornito funziona con altri formati di file Excel, come XLSX?

A. Sì, il codice sorgente fornito funziona con altri formati di file Excel, incluso XLSX. Aspose.Cells per .NET supporta una varietà di formati di file Excel, consentendo di manipolare e spostare il foglio di lavoro in diversi tipi di file.

#### D. Come posso specificare il percorso e il nome del file di output quando salvo il file Excel modificato?

A.  Quando si salva il file Excel modificato, utilizzare il file`Save` metodo dell'oggetto Workbook specificando il percorso completo e il nome del file di output. Assicurati di specificare l'estensione file appropriata, ad esempio`.xls` O`.xlsx`, a seconda del formato file desiderato.