---
title: Excel Copia foglio di lavoro
linktitle: Excel Copia foglio di lavoro
second_title: Riferimento all'API Aspose.Cells per .NET
description: Copia un foglio di lavoro Excel in un altro con Aspose.Cells per .NET.
type: docs
weight: 20
url: /it/net/excel-copy-worksheet/excel-copy-worksheet/
---

In questa guida, spiegheremo come copiare un foglio di lavoro Excel utilizzando la libreria Aspose.Cells per .NET. Ti forniremo il codice sorgente C# e ti guideremo attraverso i passaggi necessari per completare questa attività. Alla fine, ti mostreremo il risultato atteso. Segui le istruzioni qui sotto per iniziare.

## Passaggio 1: preparazione

Prima di iniziare, assicurati di aver installato Aspose.Cells per .NET e di aver creato un progetto C# nel tuo ambiente di sviluppo integrato (IDE) preferito. Assicurati inoltre di avere una copia del file Excel che desideri manipolare.

## Passaggio 2: importa le librerie richieste

 Nel tuo file sorgente C#, importa le librerie necessarie da Aspose.Cells usando il file`using` direttiva:

```csharp
using Aspose.Cells;
```

## Passaggio 3: impostare il percorso del file

 Dichiara un`dataDir` variabile e inizializzarla con la directory contenente il file Excel. Per esempio :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Assicurati di sostituire`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` con il percorso effettivo della tua directory.

## Passaggio 4: carica il file Excel esistente

 Usa il`Workbook`class da Aspose.Cells per aprire il file Excel esistente. Usa il`InputPath` variabile per specificare il percorso del file:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Assicurati di aver sostituito`"book1.xls"` con il nome effettivo del tuo file Excel.

## Passaggio 5: copia il foglio di lavoro

 Ora copieremo il foglio di lavoro esistente in un nuovo foglio di lavoro. Usa il`Worksheets` proprietà del`Workbook` oggetto per accedere alla raccolta di fogli di lavoro:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Quindi usa il`AddCopy` metodo per copiare il foglio di lavoro specificato. Ad esempio, per copiare "Foglio1":

```csharp
sheets.AddCopy("Sheet1");
```

## Passaggio 6: salvare il file Excel

 Usa il`Save` metodo del`Workbook` oggetto per salvare le modifiche in un nuovo file:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Assicurarsi di specificare il percorso e il nome file desiderati per il file di output.

### Esempio di codice sorgente per Excel Copia foglio di lavoro utilizzando Aspose.Cells per .NET 

```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Apri un file Excel esistente.
Workbook wb = new Workbook(InputPath);
// Crea un oggetto Fogli di lavoro con riferimento a
// i fogli del quaderno.
WorksheetCollection sheets = wb.Worksheets;
// Copia i dati in un nuovo foglio da uno esistente
// foglio all'interno della cartella di lavoro.
sheets.AddCopy("Sheet1");
// Salva il file Excel.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Conclusione

Congratulazioni! Ora hai imparato come copiare un foglio di lavoro Excel utilizzando Aspose.Cells per .NET. Questa guida passo-passo ha mostrato come importare le librerie necessarie, caricare un file Excel esistente, copiare il foglio di lavoro e salvare il file modificato. Sentiti libero di utilizzare questo metodo nei tuoi progetti per manipolare in modo efficiente i file Excel.

### Domande frequenti

#### D. Aspose.Cells è compatibile con altri linguaggi di programmazione?

A. Sì, Aspose.Cells supporta più linguaggi di programmazione tra cui C#, Java, Python e molti altri.

#### D. Posso copiare un foglio di lavoro in un'altra cartella di lavoro di Excel?

A.  Sì, puoi usare il`AddCopy` metodo per copiare un foglio di lavoro in un'altra cartella di lavoro di Excel.

#### D. Aspose.Cells conserva le formule e la formattazione durante la copia del foglio di lavoro?

A. Sì, Aspose.Cells conserva le formule, la formattazione e altre proprietà durante la copia di un foglio di lavoro.

#### D. Aspose.Cells richiede una licenza per uso commerciale?

A. Sì, Aspose.Cells è un prodotto commerciale e richiede l'acquisto di una licenza per uso commerciale. Puoi trovare ulteriori informazioni sulla licenza sul sito Web ufficiale di Aspose.