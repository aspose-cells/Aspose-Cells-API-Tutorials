---
title: Nascondi e scopri il foglio di lavoro
linktitle: Nascondi e scopri il foglio di lavoro
second_title: Aspose.Cells per riferimento API .NET
description: Una potente libreria per lavorare con file Excel, inclusa la creazione, la modifica e la manipolazione dei dati.
type: docs
weight: 90
url: /it/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
In questo tutorial, ti guideremo passo dopo passo per spiegare il seguente codice sorgente C# che viene utilizzato per nascondere e mostrare un foglio di lavoro utilizzando Aspose.Cells per .NET. Seguire i passaggi seguenti:

## Passaggio 1: preparazione dell'ambiente

Prima di iniziare, assicurati di avere Aspose.Cells per .NET installato sul tuo sistema. Se non lo hai già installato, puoi scaricarlo dal sito ufficiale di Aspose. Una volta installato, puoi creare un nuovo progetto nel tuo ambiente di sviluppo integrato (IDE) preferito.

## Passaggio 2: importa gli spazi dei nomi richiesti

Nel file di origine C#, aggiungi gli spazi dei nomi necessari per utilizzare le funzionalità di Aspose.Cells. Aggiungi le seguenti righe all'inizio del tuo file:

```csharp
using Aspose.Cells;
using System.IO;
```

## Passaggio 3: caricare il file Excel

Prima di nascondere o mostrare un foglio di lavoro, è necessario caricare il file Excel nell'applicazione. Assicurati di avere il file Excel che desideri utilizzare nella stessa directory del tuo progetto. Utilizzare il seguente codice per caricare il file Excel:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

Assicurati di sostituire "PERCORSO DELLA DIRECTORY DOCUMENTI" con il percorso effettivo della directory contenente il file Excel.

## Passaggio 4: accedi al foglio di calcolo

Una volta caricato il file Excel, puoi accedere al foglio di lavoro che desideri nascondere o mostrare. Utilizzare il codice seguente per accedere al primo foglio di lavoro nel file:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Passaggio 5: nascondi il foglio di lavoro

 Ora che hai effettuato l'accesso al foglio di lavoro, puoi nasconderlo utilizzando il file`IsVisible` proprietà. Utilizzare il codice seguente per nascondere il primo foglio di lavoro nel file:

```csharp
worksheet. IsVisible = false;
```

## Passaggio 6: visualizzare nuovamente il foglio di lavoro

Se desideri visualizzare nuovamente il foglio di lavoro precedentemente nascosto, puoi utilizzare lo stesso codice modificando il valore di`IsVisible` proprietà. Utilizzare il codice seguente per visualizzare nuovamente il primo foglio di lavoro:

```csharp
worksheet. IsVisible = true;
```

## Passaggio 7: salva le modifiche

Una volta tu

  hai nascosto o mostrato il foglio di lavoro secondo necessità, è necessario salvare le modifiche nel file Excel. Utilizzare il seguente codice per salvare le modifiche:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Assicurati di specificare il percorso di output corretto per salvare il file Excel modificato.

### Codice sorgente di esempio per nascondere e scoprire il foglio di lavoro utilizzando Aspose.Cells per .NET 

```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creazione di un flusso di file contenente il file Excel da aprire
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Creazione di un'istanza di un oggetto cartella di lavoro con l'apertura del file Excel tramite il flusso di file
Workbook workbook = new Workbook(fstream);
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Nascondere il primo foglio di lavoro del file Excel
worksheet.IsVisible = false;
// Mostra il primo foglio di lavoro del file Excel
//Foglio di lavoro.IsVisible = true;
// Salvataggio del file Excel modificato nel formato predefinito (ovvero Excel 2003).
workbook.Save(dataDir + "output.out.xls");
// Chiusura del flusso di file per liberare tutte le risorse
fstream.Close();
```

## Conclusione

Congratulazioni! Hai imparato come nascondere e mostrare un foglio di calcolo utilizzando Aspose.Cells per .NET. Ora puoi utilizzare questa funzionalità per controllare la visibilità dei tuoi fogli di calcolo nei file Excel.

### Domande frequenti (FAQ)

#### Come posso installare Aspose.Cells per .NET?

 È possibile installare Aspose.Cells per .NET scaricando il relativo pacchetto NuGet da[Rilasci Aspose](https://releases/aspose.com/cells/net/) e aggiungendolo al tuo progetto Visual Studio.

#### Qual è la versione minima richiesta di .NET Framework per utilizzare Aspose.Cells per .NET?

Aspose.Cells per .NET supporta .NET Framework 2.0 e versioni successive.

#### Posso aprire e modificare file Excel esistenti con Aspose.Cells per .NET?

Sì, puoi aprire e modificare file Excel esistenti utilizzando Aspose.Cells per .NET. Puoi accedere a fogli di lavoro, celle, formule e altri elementi del file Excel.

#### Aspose.Cells per .NET supporta il reporting e l'esportazione in altri formati di file?

Sì, Aspose.Cells per .NET supporta la generazione di report e l'esportazione in formati come PDF, HTML, CSV, TXT, ecc.

#### La modifica del file Excel è permanente?

Sì, la modifica del file Excel è permanente una volta salvato. Assicurati di salvare una copia di backup prima di apportare qualsiasi modifica al file originale.