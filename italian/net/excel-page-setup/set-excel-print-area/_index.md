---
title: Imposta l'area di stampa di Excel
linktitle: Imposta l'area di stampa di Excel
second_title: Riferimento all'API Aspose.Cells per .NET
description: Guida passo passo per impostare l'area di stampa di Excel utilizzando Aspose.Cells per .NET. Ottimizza e personalizza facilmente le cartelle di lavoro di Excel.
type: docs
weight: 140
url: /it/net/excel-page-setup/set-excel-print-area/
---
L'utilizzo di Aspose.Cells per .NET può facilitare notevolmente la gestione e la manipolazione dei file Excel nelle applicazioni .NET. In questa guida, ti mostreremo come impostare l'area di stampa di una cartella di lavoro di Excel utilizzando Aspose.Cells per .NET. Ti guideremo passo dopo passo attraverso il codice sorgente C# fornito per eseguire questa operazione.

## Passaggio 1: configurazione dell'ambiente

Prima di iniziare, assicurati di aver impostato il tuo ambiente di sviluppo e installato Aspose.Cells per .NET. È possibile scaricare l'ultima versione della libreria dal sito Web ufficiale di Aspose.

## Passaggio 2: importa gli spazi dei nomi richiesti

Nel tuo progetto C#, importa gli spazi dei nomi necessari per lavorare con Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Passaggio 3: impostazione del percorso della directory dei documenti

 Dichiara un`dataDir` variabile per specificare il percorso della directory in cui si desidera salvare il file Excel generato:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assicurati di sostituire`"YOUR_DOCUMENT_DIRECTORY"` con il percorso corretto sul tuo sistema.

## Passaggio 4: creazione di un oggetto cartella di lavoro

Crea un'istanza di un oggetto Workbook che rappresenta la cartella di lavoro di Excel che desideri creare:

```csharp
Workbook workbook = new Workbook();
```

## Passaggio 5: ottenere il riferimento PageSetup del foglio di lavoro

Per impostare l'area di stampa, dobbiamo prima ottenere il riferimento dal PageSetup del foglio di lavoro. Utilizzare il seguente codice per ottenere il riferimento:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Passaggio 6: specificare l'intervallo di celle dell'area di stampa

Ora che abbiamo il riferimento PageSetup, possiamo specificare l'intervallo di celle che compongono l'area di stampa. In questo esempio, imposteremo l'intervallo di celle da A1 a T35 come area di stampa. Usa il seguente codice:

```csharp
pageSetup.PrintArea = "A1:T35";
```

È possibile regolare l'intervallo di celle in base alle proprie esigenze.

## Passaggio 7: salvare la cartella di lavoro di Excel

 Per salvare la cartella di lavoro di Excel con l'area di stampa definita, utilizzare il file`Save` metodo dell'oggetto Workbook:

```csharp
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

Ciò salverà la cartella di lavoro di Excel con il nome file "SetPrintArea_out.xls" nella directory specificata.

### Esempio di codice sorgente per Imposta area di stampa di Excel utilizzando Aspose.Cells per .NET 
```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Istanziare un oggetto Workbook
Workbook workbook = new Workbook();
// Ottenere il riferimento del PageSetup del foglio di lavoro
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Specificare l'intervallo di celle (dalla cella A1 alla cella T35) dell'area di stampa
pageSetup.PrintArea = "A1:T35";
// Salva la cartella di lavoro.
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

## Conclusione

Congratulazioni! Ora hai imparato come impostare l'area di stampa di una cartella di lavoro di Excel utilizzando Aspose.Cells per .NET. Questa libreria potente e intuitiva rende molto più facile lavorare con i file Excel nelle tue applicazioni .NET. Se hai ulteriori domande o incontri difficoltà, non esitare a consultare la documentazione ufficiale di Aspose.Cells per ulteriori informazioni e risorse.

### FAQ

#### 1. Posso personalizzare ulteriormente il layout dell'area di stampa, come orientamento e margini?

Sì, puoi accedere ad altre proprietà di PageSetup come l'orientamento della pagina, i margini, la scala, ecc. per personalizzare ulteriormente il layout dell'area di stampa.

#### 2. Aspose.Cells per .NET supporta altri formati di file Excel, come XLSX e CSV?

Sì, Aspose.Cells per .NET supporta una varietà di formati di file Excel tra cui XLSX, XLS, CSV, HTML, PDF e molti altri.

#### 3. Aspose.Cells per .NET è compatibile con tutte le versioni di .NET Framework?

Aspose.Cells per .NET è compatibile con .NET Framework 2.0 o successivo, comprese le versioni 3.5, 4.0, 4.5, 4.6, ecc.