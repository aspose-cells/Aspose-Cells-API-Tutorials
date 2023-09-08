---
title: Elimina foglio di lavoro Excel per nome Tutorial C#
linktitle: Elimina foglio di lavoro Excel per nome
second_title: Aspose.Cells per riferimento API .NET
description: Elimina facilmente un foglio di lavoro Excel specifico per nome utilizzando Aspose.Cells per .NET. Tutorial dettagliato con esempi di codice.
type: docs
weight: 40
url: /it/net/excel-worksheet-csharp-tutorials/delete-excel-worksheet-by-name-csharp-tutorial/
---
In questo tutorial, ti guideremo passo dopo passo per spiegare il codice sorgente C# di seguito, che può eliminare un foglio di lavoro Excel utilizzando Aspose.Cells per .NET utilizzando il suo nome. Includeremo un codice di esempio per ogni passaggio per aiutarti a comprendere il processo in dettaglio.

## Passaggio 1: definire la directory dei documenti

Per iniziare, devi impostare il percorso della directory in cui si trova il tuo file Excel. Sostituisci "LA TUA DIRECTORY DOCUMENTI" nel codice con il percorso effettivo del tuo file Excel.

```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Passaggio 2: crea un flusso di file e apri il file Excel

 Successivamente, è necessario creare un flusso di file e aprire il file Excel utilizzando il file`FileStream` classe.

```csharp
// Creare un flusso di file contenente il file Excel da aprire
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## Passaggio 3: creare un'istanza di un oggetto cartella di lavoro

 Dopo aver aperto il file Excel, è necessario istanziare a`Workbook`oggetto. Questo oggetto rappresenta la cartella di lavoro di Excel e offre vari metodi e proprietà per manipolare la cartella di lavoro.

```csharp
// Creare un'istanza di un oggetto cartella di lavoro
// Aprire il file Excel tramite il flusso di file
Workbook workbook = new Workbook(fstream);
```

## Passaggio 4: elimina un foglio di lavoro per nome

 Per rimuovere un foglio di lavoro dal suo nome, puoi utilizzare il file`RemoveAt()` metodo del`Worksheets` oggetto del`Workbook` oggetto. Il nome del foglio di lavoro che desideri eliminare deve essere passato come parametro.

```csharp
// Elimina un foglio di lavoro utilizzando il nome del foglio
workbook.Worksheets.RemoveAt("Sheet1");
```

## Passaggio 5: salvare la cartella di lavoro

 Dopo aver eliminato il foglio di lavoro, puoi salvare la cartella di lavoro Excel modificata utilizzando il file`Save()` metodo del`Workbook` oggetto.

```csharp
// Salva la cartella di lavoro di Excel
workbook.Save(dataDir + "output.out.xls");
```


### Codice sorgente di esempio per Elimina foglio di lavoro Excel per nome Tutorial C# utilizzando Aspose.Cells per .NET 
```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creazione di un flusso di file contenente il file Excel da aprire
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Creazione di un'istanza di un oggetto cartella di lavoro
// Apertura del file Excel tramite il flusso di file
Workbook workbook = new Workbook(fstream);
// Rimozione di un foglio di lavoro utilizzando il nome del foglio
workbook.Worksheets.RemoveAt("Sheet1");
// Salva cartella di lavoro
workbook.Save(dataDir + "output.out.xls");
```

## Conclusione

In questo tutorial, abbiamo trattato il processo passo passo per eliminare un foglio di calcolo Excel per nome utilizzando Aspose.Cells per .NET. Seguendo gli esempi di codice e le spiegazioni fornite, ora dovresti avere una buona conoscenza di come eseguire questa attività nelle tue applicazioni C#. Aspose.Cells per .NET offre un set completo di funzionalità per lavorare con file Excel, consentendo di manipolare facilmente fogli di calcolo e dati correlati.

### Domande frequenti (FAQ)

#### Cos'è Aspose.Cells per .NET?

Aspose.Cells per .NET è una potente libreria che consente agli sviluppatori di creare, manipolare e convertire file Excel nelle loro applicazioni .NET. Offre una vasta gamma di funzionalità per lavorare con fogli di calcolo, celle, formule, stili e altro ancora.

#### Come posso installare Aspose.Cells per .NET?

Per installare Aspose.Cells per .NET, è possibile scaricare il pacchetto di installazione da Aspose Releases (https://releases.aspose.com/cells/net) e seguire le istruzioni fornite. Avrai bisogno di una licenza valida per utilizzare la libreria nelle tue applicazioni.

#### Posso eliminare più fogli di lavoro contemporaneamente?

Sì, puoi eliminare più fogli di lavoro utilizzando Aspose.Cells per .NET. Puoi semplicemente ripetere il passaggio di eliminazione per ogni foglio di lavoro che desideri eliminare.

#### Come faccio a sapere se un foglio di calcolo esiste prima di eliminarlo?

 Prima di eliminare un foglio di lavoro, puoi verificare se esiste utilizzando il file`Contains()` metodo del`Worksheets` oggetto del`Workbook` oggetto. Questo metodo accetta il nome del foglio di calcolo come parametro e restituisce`true` se il foglio di calcolo esiste, altrimenti restituisce`false`.

#### È possibile recuperare un foglio di calcolo eliminato?

Sfortunatamente, una volta eliminato un foglio di calcolo, non può essere recuperato direttamente dal file Excel. Si consiglia di creare un backup del file Excel prima di eliminare un foglio di calcolo per evitare la perdita di dati.