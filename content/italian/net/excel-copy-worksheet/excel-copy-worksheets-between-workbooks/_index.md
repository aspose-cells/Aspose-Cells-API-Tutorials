---
title: Excel Copia fogli di lavoro tra cartelle di lavoro
linktitle: Excel Copia fogli di lavoro tra cartelle di lavoro
second_title: Aspose.Cells per riferimento API .NET
description: Copia facilmente fogli di lavoro tra cartelle di lavoro Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 30
url: /it/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
In questo tutorial, ti guideremo attraverso i passaggi per copiare fogli di lavoro tra cartelle di lavoro Excel utilizzando la libreria Aspose.Cells per .NET. Seguire le istruzioni riportate di seguito per completare questa attività.

## Passaggio 1: preparazione

Assicurati di aver installato Aspose.Cells per .NET e di aver creato un progetto C# nel tuo ambiente di sviluppo integrato (IDE) preferito.

## Passaggio 2: impostare il percorso della directory del documento

 Dichiarare a`dataDir` variabile e inizializzala con il percorso della directory dei documenti. Per esempio :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assicurati di sostituire`"YOUR_DOCUMENTS_DIRECTORY"` con il percorso effettivo della directory.

## Passaggio 3: definire il percorso del file di input

 Dichiarare un`InputPath` variabile e inizializzarla con il percorso completo del file Excel da cui si desidera copiare il foglio di calcolo. Per esempio :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Assicurati di avere il file Excel`book1.xls` nella directory dei documenti o specificare il nome e il percorso corretti del file.

## Passaggio 4: crea una prima cartella di lavoro Excel

 Usa il`Workbook` classe di Aspose.Cells per creare una prima cartella di lavoro Excel e aprire il file specificato:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Passaggio 5: crea una seconda cartella di lavoro Excel

Crea una seconda cartella di lavoro Excel:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Passaggio 6: copiare il foglio di lavoro dalla prima cartella di lavoro alla seconda cartella di lavoro

 Usa il`Copy`metodo per copiare il primo foglio di lavoro dalla prima cartella di lavoro alla seconda cartella di lavoro:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Passaggio 7: salva il file Excel

Salva il file Excel contenente il foglio di calcolo copiato:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Assicurati di specificare il percorso e il nome file desiderati per il file di output.

### Codice sorgente di esempio per copiare fogli di lavoro di Excel tra cartelle di lavoro utilizzando Aspose.Cells per .NET 
```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Crea una cartella di lavoro.
// Apri un file nel primo libro.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Crea un'altra cartella di lavoro.
Workbook excelWorkbook1 = new Workbook();
// Copia il primo foglio del primo libro nel secondo libro.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Salvare il file.
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

A.  Sì, puoi personalizzare le opzioni di impostazione della pagina quando copi il foglio di calcolo utilizzando le proprietà del file`PageSetup` oggetto. È possibile specificare intestazioni di pagina, piè di pagina, margini, orientamenti, ecc.