---
title: Imposta l'orientamento della pagina di Excel
linktitle: Imposta l'orientamento della pagina di Excel
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come impostare l'orientamento della pagina di Excel passo dopo passo utilizzando Aspose.Cells per .NET. Ottieni risultati ottimizzati.
type: docs
weight: 130
url: /it/net/excel-page-setup/set-excel-page-orientation/
---
Nell'era digitale odierna, i fogli di calcolo Excel svolgono un ruolo fondamentale nell'organizzazione e nell'analisi dei dati. A volte, diventa necessario personalizzare il layout e l'aspetto dei documenti Excel per soddisfare requisiti specifici. Una di queste personalizzazioni è l'impostazione dell'orientamento della pagina, che determina se la pagina stampata sarà in modalità verticale o orizzontale. In questo tutorial, illustreremo il processo di impostazione dell'orientamento della pagina di Excel utilizzando Aspose.Cells, una potente libreria per lo sviluppo .NET. Immergiamoci!

## Comprendere l'importanza di impostare l'orientamento della pagina di Excel

L'orientamento della pagina di un documento Excel influisce sul modo in cui il contenuto viene visualizzato una volta stampato. Per impostazione predefinita, Excel utilizza l'orientamento verticale, in cui la pagina è più alta che larga. Tuttavia, in alcuni scenari, l'orientamento orizzontale, in cui la pagina è più larga che alta, potrebbe essere più appropriato. Ad esempio, quando si stampano tabelle, grafici o diagrammi di grandi dimensioni, l'orientamento orizzontale offre una migliore leggibilità e rappresentazione visiva.

## Esplorare la libreria Aspose.Cells per .NET

Aspose.Cells è una libreria ricca di funzionalità che consente agli sviluppatori di creare, manipolare e convertire file Excel a livello di codice. Fornisce una vasta gamma di API per eseguire varie attività, inclusa l'impostazione dell'orientamento della pagina. Prima di immergerci nel codice, assicurati di aver aggiunto la libreria Aspose.Cells al tuo progetto .NET.

## Passaggio 1: impostazione della directory dei documenti

Prima di iniziare a lavorare con il file Excel, dobbiamo impostare la directory dei documenti. Sostituisci il segnaposto "YOUR DOCUMENT DIRECTORY" nel frammento di codice con il percorso effettivo della directory in cui desideri salvare il file di output.

```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Passaggio 2: creazione di un'istanza di un oggetto cartella di lavoro

Per lavorare con un file Excel, dobbiamo creare un'istanza della classe Workbook fornita da Aspose.Cells. Questa classe rappresenta l'intero file Excel e fornisce metodi e proprietà per manipolarne il contenuto.

```csharp
// Istanziare un oggetto Workbook
Workbook workbook = new Workbook();
```

## Passaggio 3: accesso al foglio di lavoro nel file Excel

Successivamente, dobbiamo accedere al foglio di lavoro all'interno del file Excel in cui vogliamo impostare l'orientamento della pagina. In questo esempio, lavoreremo con il primo foglio di lavoro (indice 0) della cartella di lavoro.

```csharp
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = workbook.Worksheets[0];
```

## Passaggio 4: impostare l'orientamento della pagina su Verticale

Ora è il momento di impostare l'orientamento della pagina. Aspose.Cells fornisce la proprietà PageSetup per ogni foglio di lavoro, che ci consente di personalizzare varie impostazioni relative alla pagina. Per impostare l'orientamento della pagina, dobbiamo assegnare il valore PageOrientationType.Portrait alla proprietà Orientation dell'oggetto PageSetup.

```csharp
// Impostare l'orientamento su Verticale
worksheet.PageSetup.Orientation = PageOrientationType.Portrait;
```

## Passaggio 5: salvataggio della cartella di lavoro

Dopo aver apportato le modifiche necessarie al foglio di lavoro, possiamo salvare l'oggetto Workbook modificato in un file. Il metodo Save della classe Workbook accetta il percorso del file in cui verrà salvato il file di output

.

```csharp
// Salva la cartella di lavoro.
workbook.Save(dataDir + "PageOrientation_out.xls");
```

### Esempio di codice sorgente per Imposta orientamento pagina Excel utilizzando Aspose.Cells per .NET 

```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Istanziare un oggetto Workbook
Workbook workbook = new Workbook();
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Impostare l'orientamento su Verticale
worksheet.PageSetup.Orientation = PageOrientationType.Portrait;
// Salva la cartella di lavoro.
workbook.Save(dataDir + "PageOrientation_out.xls");
```

## Conclusione

In questo tutorial, abbiamo imparato come impostare l'orientamento della pagina di Excel utilizzando Aspose.Cells per .NET. Seguendo la guida dettagliata, puoi facilmente personalizzare l'orientamento della pagina dei file Excel in base alle tue esigenze specifiche. Aspose.Cells fornisce un set completo di API per manipolare i documenti Excel, dandoti il pieno controllo sul loro aspetto e contenuto. Inizia a esplorare le possibilità con Aspose.Cells e migliora le tue attività di automazione di Excel.

## Domande frequenti

#### D1: Posso impostare l'orientamento della pagina su orizzontale anziché verticale?

 A1: Sì, assolutamente! Invece di assegnare il`PageOrientationType.Portrait` valore, puoi usare`PageOrientationType.Landscape` per impostare l'orientamento della pagina su orizzontale.

#### D2: Aspose.Cells supporta altri formati di file oltre a Excel?

A2: Sì, Aspose.Cells supporta un'ampia gamma di formati di file, inclusi XLS, XLSX, CSV, HTML, PDF e molti altri. Fornisce API per creare, manipolare e convertire file in vari formati.

#### D3: Posso impostare orientamenti di pagina diversi per fogli di lavoro diversi all'interno dello stesso file Excel?

 R3: Sì, puoi impostare diversi orientamenti di pagina per diversi fogli di lavoro accedendo a`PageSetup` oggetto di ogni foglio di lavoro individualmente e modificando il suo`Orientation` proprietà di conseguenza.

#### Q4: Aspose.Cells è compatibile sia con .NET Framework che con .NET Core?

R4: Sì, Aspose.Cells è compatibile sia con .NET Framework che con .NET Core. Supporta un'ampia gamma di versioni .NET, consentendoti di utilizzarlo in vari ambienti di sviluppo.
