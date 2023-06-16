---
title: Implementa il formato carta personalizzato del foglio di lavoro per il rendering
linktitle: Implementa il formato carta personalizzato del foglio di lavoro per il rendering
second_title: Riferimento all'API Aspose.Cells per .NET
description: Guida dettagliata per implementare dimensioni personalizzate del foglio di lavoro con Aspose.Cells per .NET. Imposta le dimensioni, aggiungi un messaggio e salva come PDF.
type: docs
weight: 50
url: /it/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
L'implementazione di una dimensione personalizzata per il tuo foglio di lavoro può essere molto utile quando desideri creare un documento PDF con una dimensione specifica. In questo tutorial impareremo come utilizzare Aspose.Cells per .NET per impostare una dimensione personalizzata per un foglio di lavoro e quindi salvare il documento come PDF.

## Passaggio 1: creazione della cartella di output

Prima di iniziare, è necessario creare una cartella di output in cui verrà salvato il file PDF generato. Puoi utilizzare qualsiasi percorso desideri per la tua cartella di output.

```csharp
// Directory di output
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Assicurati di specificare il percorso corretto della cartella di output.

## Passaggio 2: creazione dell'oggetto cartella di lavoro

Per iniziare, devi creare un oggetto Workbook utilizzando Aspose.Cells. Questo oggetto rappresenta il tuo foglio di calcolo.

```csharp
// Creare l'oggetto cartella di lavoro
Workbook wb = new Workbook();
```

## Passaggio 3: accesso al primo foglio di lavoro

Dopo aver creato l'oggetto Workbook, puoi accedere al primo foglio di lavoro al suo interno.

```csharp
// Accesso al primo foglio di lavoro
Worksheet ws = wb.Worksheets[0];
```

## Passaggio 4: impostazione delle dimensioni personalizzate del foglio di lavoro

 Ora puoi impostare le dimensioni personalizzate del foglio di lavoro utilizzando`CustomPaperSize(width, height)` metodo della classe PageSetup.

```csharp
// Imposta la dimensione del foglio di lavoro personalizzato (in pollici)
ws.PageSetup.CustomPaperSize(6, 4);
```

In questo esempio, abbiamo impostato la dimensione del foglio di lavoro su 6 pollici di larghezza e 4 pollici di altezza.

## Passaggio 5: accesso alla cella B4

Successivamente, possiamo accedere a una cella specifica nel foglio di lavoro. In questo caso, accederemo alla cella B4.

```csharp
// Accesso alla cella B4
Cell b4 = ws.Cells["B4"];
```

## Passaggio 6: aggiunta del messaggio nella cella B4

 Ora possiamo aggiungere un messaggio alla cella B4 utilizzando il`PutValue(value)` metodo.

```csharp
// Aggiungi il messaggio nella cella B4
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

In questo esempio, abbiamo aggiunto il messaggio "PDF Page Size: 6.00" x 4.00" nella cella B4.

## Passaggio 7: salvare il foglio di lavoro in formato PDF

 Infine, possiamo salvare il foglio di lavoro in formato PDF utilizzando il file`Save(filePath)` metodo dell'oggetto Workbook.

```csharp
// Salva il foglio di lavoro in formato PDF
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Specificare il percorso desiderato per il file PDF generato, utilizzando la cartella di output creata in precedenza.

### Esempio di codice sorgente per l'implementazione della dimensione carta personalizzata del foglio di lavoro per il rendering utilizzando Aspose.Cells per .NET 
```csharp
//Cartella di destinazione
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Crea oggetto cartella di lavoro
Workbook wb = new Workbook();
//Accedi al primo foglio di lavoro
Worksheet ws = wb.Worksheets[0];
//Imposta il formato carta personalizzato in unità di pollici
ws.PageSetup.CustomPaperSize(6, 4);
//Accedere alla cella B4
Cell b4 = ws.Cells["B4"];
//Aggiungi il messaggio nella cella B4
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Salva la cartella di lavoro in formato pdf
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## Conclusioni

In questo tutorial, hai imparato come implementare dimensioni personalizzate di un foglio di lavoro utilizzando Aspose.Cells per .NET. È possibile utilizzare questi passaggi per impostare dimensioni specifiche per i fogli di lavoro e quindi salvare i documenti in formato PDF. Ci auguriamo che questa guida sia stata utile per comprendere il processo di implementazione di un formato di foglio di calcolo personalizzato.

### Domande frequenti (FAQ)

#### Domanda 1: posso personalizzare ulteriormente il layout del foglio di calcolo?

Sì, Aspose.Cells offre molte opzioni per personalizzare il layout del foglio di lavoro. Puoi impostare dimensioni personalizzate, orientamento della pagina, margini, intestazioni e piè di pagina e molto altro.

#### Domanda 2: quali altri formati di output supporta Aspose.Cells?

Aspose.Cells supporta molti formati di output diversi, inclusi PDF, XLSX, XLS, CSV, HTML, TXT e molti altri. È possibile scegliere il formato di output desiderato in base alle proprie esigenze.