---
title: Excel Copia fogli di lavoro tra cartelle di lavoro
linktitle: Excel Copia fogli di lavoro tra cartelle di lavoro
second_title: Riferimento all'API Aspose.Cells per .NET
description: Copia facilmente fogli di lavoro tra cartelle di lavoro di Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 30
url: /it/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
In questo tutorial, ti guideremo attraverso i passaggi per copiare fogli di lavoro tra cartelle di lavoro di Excel utilizzando la libreria Aspose.Cells per .NET. Seguire le istruzioni riportate di seguito per completare questa attività.

## Passaggio 1: preparazione

Assicurati di aver installato Aspose.Cells per .NET e di aver creato un progetto C# nel tuo ambiente di sviluppo integrato (IDE) preferito.

## Passaggio 2: impostare il percorso della directory del documento

 Dichiara un`dataDir` variabile e inizializzarla con il percorso della directory dei documenti. Per esempio :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assicurati di sostituire`"YOUR_DOCUMENTS_DIRECTORY"` con il percorso effettivo della tua directory.

## Passaggio 3: definire il percorso del file di input

 Dichiara un`InputPath` variabile e inizializzarla con il percorso completo del file Excel da cui si desidera copiare il foglio di calcolo. Per esempio :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Assicurati di avere il file Excel`book1.xls` nella directory dei documenti o specificare il nome file e la posizione corretti.

## Passaggio 4: crea una prima cartella di lavoro di Excel

 Usa il`Workbook` class di Aspose.Cells per creare una prima cartella di lavoro di Excel e aprire il file specificato:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Passaggio 5: creare una seconda cartella di lavoro di Excel

Crea una seconda cartella di lavoro di Excel:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Passaggio 6: copiare il foglio di lavoro dalla prima cartella di lavoro alla seconda cartella di lavoro

 Usa il`Copy`metodo per copiare il primo foglio di lavoro dalla prima cartella di lavoro alla seconda cartella di lavoro:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Passaggio 7: salvare il file Excel

Salva il file Excel contenente il foglio di calcolo copiato:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Assicurarsi di specificare il percorso e il nome file desiderati per il file di output.

### Esempio di codice sorgente per Excel Copia fogli di lavoro tra cartelle di lavoro utilizzando Aspose.Cells per .NET 
```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Crea una cartella di lavoro.
// Apri un file nel primo libro.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Crea un'altra cartella di lavoro.
Workbook excelWorkbook1 = new Workbook();
// Copia il primo foglio del primo libro nel secondo libro.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Salva il file.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Conclusione

Congratulazioni! Ora hai imparato come copiare fogli di lavoro tra cartelle di lavoro di Excel utilizzando Aspose.Cells per .NET. Sentiti libero di utilizzare questo metodo nei tuoi progetti per manipolare in modo efficiente i file Excel.

### Domande frequenti

#### D. Quali librerie sono necessarie per utilizzare Aspose.Cells per .NET?

A. Per utilizzare Aspose.Cells per .NET, è necessario includere la libreria Aspose.Cells nel progetto. Assicurati di aver fatto riferimento correttamente a questa libreria nel tuo ambiente di sviluppo integrato (IDE).

#### D. Aspose.Cells supporta altri formati di file Excel, come XLSX?

A. Sì, Aspose.Cells supporta vari formati di file Excel tra cui XLSX, XLS, CSV, HTML e molti altri. È possibile manipolare questi formati di file utilizzando le funzionalità di Aspose.Cells per .NET.

#### D. Posso personalizzare le opzioni di layout durante la copia del foglio di calcolo?

A.  Sì, puoi personalizzare le opzioni di configurazione della pagina quando copi il foglio di calcolo utilizzando le proprietà del file`PageSetup` oggetto. Puoi specificare intestazioni di pagina, piè di pagina, margini, orientamenti, ecc.