---
title: Aggiunta di un foglio di lavoro Excel a una cartella di lavoro esistente Tutorial C#
linktitle: Aggiungi foglio di lavoro Excel alla cartella di lavoro esistente
second_title: Riferimento all'API Aspose.Cells per .NET
description: Aggiungi facilmente un nuovo foglio a una cartella di lavoro Excel esistente utilizzando Aspose.Cells per .NET. Tutorial passo passo con esempi di codice.
type: docs
weight: 10
url: /it/net/excel-worksheet-csharp-tutorials/add-excel-worksheet-to-existing-workbook-csharp-tutorial/
---
In questo tutorial, ti guideremo passo dopo passo per spiegare il codice sorgente C# di seguito, che aiuta ad aggiungere un nuovo foglio a una cartella di lavoro Excel esistente utilizzando Aspose.Cells per .NET. Includeremo un codice di esempio per ogni passaggio per aiutarti a comprendere il processo in dettaglio.

## Passaggio 1: definire la directory dei documenti

Per iniziare, devi impostare il percorso della directory in cui si trova il tuo file Excel. Sostituisci "YOUR DOCUMENT DIRECTORY" nel codice con il percorso effettivo del tuo file Excel.

```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Passaggio 2: creare un flusso di file e aprire il file Excel

 Successivamente, è necessario creare un flusso di file e aprire il file Excel utilizzando l'estensione`FileStream` classe.

```csharp
// Creare un flusso di file contenente il file Excel da aprire
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## Passaggio 3: creare un'istanza di un oggetto cartella di lavoro

 Dopo aver aperto il file Excel, è necessario creare un'istanza di a`Workbook` oggetto. Questo oggetto rappresenta la cartella di lavoro di Excel e offre vari metodi e proprietà per manipolare la cartella di lavoro.

```csharp
// Crea un'istanza di un oggetto Workbook
// Apri il file Excel tramite il flusso di file
Workbook workbook = new Workbook(fstream);
```

## Passaggio 4: aggiungi un nuovo foglio alla cartella di lavoro

 Per aggiungere un nuovo foglio di lavoro alla cartella di lavoro, puoi utilizzare il file`Worksheets.Add()` metodo del`Workbook` oggetto. Questo metodo restituisce l'indice del foglio appena aggiunto.

```csharp
// Aggiungi un nuovo foglio alla cartella di lavoro della cartella di lavoro
int i = workbook. Worksheets. Add();
```

## Passaggio 5: imposta il nome del nuovo foglio

 È possibile impostare il nome del foglio appena aggiunto utilizzando il file`Name` proprietà del`Worksheet` oggetto.

```csharp
//Ottenere il riferimento del nuovo foglio aggiunto passando il relativo indice del foglio
Worksheet worksheet = workbook.Worksheets[i];
// Definire il nome del nuovo foglio
worksheet.Name = "My Worksheet";
```

## Passaggio 6: salvare il file Excel

 Una volta aggiunto il nuovo foglio e impostato il suo nome, è possibile salvare il file Excel modificato utilizzando il file`Save()` metodo del`Workbook` oggetto.

```csharp
// Salva il file Excel
workbook.Save(dataDir + "output.out.xls");
```

## Passaggio 7: chiudere il flusso di file e rilasciare le risorse

Infine, è importante chiudere il flusso di file per rilasciare tutte le risorse ad esso associate.

```csharp
// Chiudi flusso di file per rilasciare tutte le risorse
fstream.Close();
```

### Esempio di codice sorgente per l'esercitazione Aggiungi foglio di lavoro Excel alla cartella di lavoro esistente C# utilizzando Aspose.Cells per .NET 
```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creazione di un flusso di file contenente il file Excel da aprire
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Istanziare un oggetto Workbook
// Apertura del file Excel tramite il flusso di file
Workbook workbook = new Workbook(fstream);
// Aggiunta di un nuovo foglio di lavoro all'oggetto Workbook
int i = workbook.Worksheets.Add();
// Ottenere il riferimento del foglio di lavoro appena aggiunto passando il relativo indice del foglio
Worksheet worksheet = workbook.Worksheets[i];
// Impostazione del nome del foglio di lavoro appena aggiunto
worksheet.Name = "My Worksheet";
// Salvataggio del file Excel
workbook.Save(dataDir + "output.out.xls");
// Chiusura del flusso di file per liberare tutte le risorse
fstream.Close();
```

## Conclusione

In questo tutorial abbiamo coperto il processo passo passo di aggiunta di un nuovo fuoco Connetti a una cartella di lavoro Excel esistente utilizzando Aspose.Cells per .NET. Seguendo gli esempi di codice e le spiegazioni fornite, ora dovresti avere una buona conoscenza di come eseguire questa attività nelle tue applicazioni C#. Aspose.Cells per .NET offre un set completo di funzionalità per lavorare con i file Excel, consentendo di automatizzare in modo efficiente varie attività relative a Excel.

### Domande frequenti (FAQ)

#### Cos'è Aspose.Cells per .NET?

Aspose.Cells per .NET è una potente libreria .NET che consente agli sviluppatori di creare, manipolare e convertire file Excel nelle loro applicazioni. Offre una vasta gamma di funzionalità per lavorare con fogli di calcolo, celle, formule, stili e altro ancora.

#### Come posso installare Aspose.Cells per .NET?

Per installare Aspose.Cells per .NET, è possibile scaricare il pacchetto di installazione da Aspose Releases (https://releases.aspose.com/cells/net) e seguire le istruzioni di installazione fornite. Avrai anche bisogno di una licenza valida per utilizzare la libreria nelle tue applicazioni.

#### Posso aggiungere più fogli di calcolo utilizzando Aspose.Cells per .NET?

 Sì, puoi aggiungere più fogli di lavoro a un file Excel utilizzando Aspose.Cells per .NET. Puoi usare il`Worksheets.Add()` metodo del`Workbook` oggetto per aggiungere nuovi fogli di lavoro in diverse posizioni nella cartella di lavoro.

#### Come posso formattare le celle nel file Excel?

Aspose.Cells per .NET offre diversi metodi e proprietà per formattare le celle in un file Excel. Puoi impostare i valori delle celle, applicare opzioni di formattazione come stile del carattere, colore, allineamento, bordi e altro. Vedere la documentazione e il codice di esempio forniti da Aspose.Cells per informazioni più dettagliate sulla formattazione delle celle.

#### Aspose.Cells per .NET è compatibile con diverse versioni di Excel?

Sì, Aspose.Cells per .NET è compatibile con diverse versioni di Excel tra cui Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016, Excel 2019 ed Excel per Office 365. Supporta sia il formato .xls che il più recente . formato XLSX.