---
title: Rileva tipi di collegamento
linktitle: Rileva tipi di collegamento
second_title: Aspose.Cells per riferimento API .NET
description: Rileva i tipi di collegamento in una cartella di lavoro di Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 80
url: /it/net/excel-workbook/detect-link-types/
---
In questo tutorial, ti guideremo passo dopo passo attraverso il codice sorgente C# fornito che ti consentirà di rilevare i tipi di collegamento in una cartella di lavoro di Excel utilizzando Aspose.Cells per .NET. Seguire i passaggi seguenti per eseguire questa operazione.

## Passaggio 1: imposta la directory di origine

```csharp
// directory di origine
string SourceDir = RunExamples.Get_SourceDirectory();
```

In questo primo passaggio definiamo la directory di origine in cui si trova la cartella di lavoro Excel contenente i collegamenti.

## Passaggio 2: caricare la cartella di lavoro di Excel

```csharp
// Carica la cartella di lavoro di Excel
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
```

Carichiamo la cartella di lavoro di Excel utilizzando il percorso del file di origine.

## Passaggio 3: ottieni il foglio di calcolo

```csharp
// Ottieni il primo foglio di lavoro (impostazione predefinita)
Worksheet worksheet = workbook.Worksheets[0];
```

 Otteniamo il primo foglio di lavoro della cartella di lavoro. Puoi cambiare il`[0]` indice per accedere a un foglio di lavoro specifico, se necessario.

## Passaggio 4: crea un intervallo di celle

```csharp
// Crea un intervallo di celle A1:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
```

Creiamo un intervallo di celle, in questo esempio dalla cella A1 alla cella A7. È possibile modificare i riferimenti di cella secondo necessità.

## Passaggio 5: ottieni i collegamenti ipertestuali nell'intervallo

```csharp
// Ottieni i collegamenti ipertestuali nell'intervallo
Hyperlink[] hyperlinks = range.Hyperlinks;
```

Otteniamo tutti i collegamenti ipertestuali presenti nell'intervallo specificato.

## Passaggio 6: sfoglia i collegamenti ipertestuali e visualizza i tipi di collegamento

```csharp
foreach (Hyperlink link in hyperlinks)
{
Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
```

Esaminiamo ciascun collegamento e visualizziamo il testo visualizzato e il tipo di collegamento associato.

### Codice sorgente di esempio per Rileva tipi di collegamento utilizzando Aspose.Cells per .NET 
```csharp
//directory di origine
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
// Ottieni il primo foglio di lavoro (predefinito).
Worksheet worksheet = workbook.Worksheets[0];
// Crea un intervallo A2:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
// Ottieni collegamenti ipertestuali nel raggio d'azione
Hyperlink[] hyperlinks = range.Hyperlinks;
foreach (Hyperlink link in hyperlinks)
{
	Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
Console.WriteLine("DetectLinkTypes executed successfully.");
```

## Conclusione

Congratulazioni! Hai imparato come rilevare i tipi di collegamento in una cartella di lavoro di Excel utilizzando Aspose.Cells per .NET. Questa funzionalità ti consente di lavorare con i collegamenti ipertestuali presenti nelle cartelle di lavoro di Excel. Continua a esplorare le funzionalità di Aspose.Cells per espandere le capacità di elaborazione delle cartelle di lavoro di Excel.

### Domande frequenti

#### D: Come posso installare Aspose.Cells per .NET nel mio progetto?

 R: È possibile installare Aspose.Cells per .NET utilizzando il gestore pacchetti NuGet. Cercare[Rilasci Aspose](https://releases.aspose.com/cells/net) nella console di gestione pacchetti NuGet e installare la versione più recente.

#### D: Posso rilevare tipi di collegamento in fogli di lavoro specifici anziché nel primo foglio?

 R: Sì, puoi modificare il file`workbook.Worksheets[0]` indice per accedere a un foglio di lavoro specifico. Ad esempio, per accedere al secondo foglio, utilizzare`workbook.Worksheets[1]`.

#### D: E' possibile modificare le tipologie di collegamenti rilevati nella gamma?

R: Sì, puoi sfogliare i collegamenti ipertestuali ed eseguire operazioni di modifica, come l'aggiornamento degli URL o la rimozione di collegamenti indesiderati.

#### D: Quali tipi di collegamenti sono possibili in Aspose.Cells per .NET?

R: I possibili tipi di collegamento includono collegamenti ipertestuali, collegamenti ad altri fogli di lavoro, collegamenti a file esterni, collegamenti a siti Web, ecc.

#### D: Aspose.Cells per .NET supporta la creazione di nuovi collegamenti in un foglio di calcolo?

 R: Sì, Aspose.Cells per .NET supporta la creazione di nuovi collegamenti utilizzando il file`Hyperlink` classe e le sue proprietà associate. Puoi aggiungere collegamenti ipertestuali, collegamenti a URL, collegamenti ad altri fogli di calcolo, ecc.

#### D: Posso utilizzare Aspose.Cells per .NET nelle applicazioni web?

R: Sì, Aspose.Cells per .NET può essere utilizzato nelle applicazioni web. È possibile incorporarlo in ASP.NET, ASP.NET Core e altri framework Web basati su .NET.

#### D: Esistono limiti alle dimensioni dei file quando si utilizza Aspose.Cells per .NET?

R: Aspose.Cells per .NET può elaborare cartelle di lavoro Excel di grandi dimensioni senza limitazioni specifiche. Tuttavia, la dimensione effettiva del file potrebbe essere limitata dalle risorse di sistema disponibili.