---
title: Imposta intestazioni e piè di pagina di Excel
linktitle: Imposta intestazioni e piè di pagina di Excel
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come impostare intestazioni e piè di pagina in Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 100
url: /it/net/excel-page-setup/set-excel-headers-and-footers/
---

In questo tutorial, ti mostreremo passo dopo passo come impostare intestazioni e piè di pagina in Excel utilizzando Aspose.Cells per .NET. Utilizzeremo il codice sorgente C# per illustrare il processo.

## Passaggio 1: configurazione dell'ambiente

Assicurati di avere Aspose.Cells per .NET installato sul tuo computer. Crea anche un nuovo progetto nel tuo ambiente di sviluppo preferito.

## Passaggio 2: importa le librerie necessarie

Nel file di codice, importa le librerie necessarie per lavorare con Aspose.Cells. Ecco il codice corrispondente:

```csharp
using Aspose.Cells;
```

## Passaggio 3: impostare la directory dei dati

Imposta la directory dei dati in cui desideri salvare il file Excel modificato. Utilizza il seguente codice:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Assicurati di specificare il percorso completo della directory.

## Passaggio 4: creazione della cartella di lavoro e del foglio di lavoro

Crea un nuovo oggetto cartella di lavoro e vai al primo foglio di lavoro nella cartella di lavoro utilizzando il seguente codice:

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Ciò creerà una cartella di lavoro vuota con un foglio di lavoro e fornirà l'accesso all'oggetto PageSetup di quel foglio di lavoro.

## Passaggio 5: impostazione delle intestazioni

 Imposta le intestazioni del foglio di calcolo utilizzando il file`SetHeader` metodi dell'oggetto PageSetup. Ecco un codice di esempio:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Ciò imposterà rispettivamente il nome del foglio di lavoro, la data e l'ora correnti e il nome del file nelle intestazioni.

## Passaggio 6: definizione dei piè di pagina

 Imposta i piè di pagina del foglio di calcolo utilizzando il file`SetFooter` metodi dell'oggetto PageSetup. Ecco un codice di esempio:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Ciò imposterà rispettivamente una stringa di testo, il numero di pagina corrente e il numero totale di pagine nei piè di pagina.

## Passaggio 7: salvataggio della cartella di lavoro modificata

Salvare la cartella di lavoro modificata utilizzando il seguente codice:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Ciò salverà la cartella di lavoro modificata nella directory dei dati specificata.

### Codice sorgente di esempio per impostare intestazioni e piè di pagina di Excel utilizzando Aspose.Cells per .NET 
```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creazione di un'istanza di un oggetto cartella di lavoro
Workbook excel = new Workbook();
// Ottenere il riferimento del PageSetup del foglio di lavoro
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Impostazione del nome del foglio di lavoro nella sezione sinistra dell'intestazione
pageSetup.SetHeader(0, "&A");
//Impostazione della data e dell'ora correnti nella sezione centrale dell'intestazione
// e cambiando il carattere dell'intestazione
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Impostazione del nome del file corrente nella sezione destra dell'intestazione e modifica del file
// carattere dell'intestazione
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Impostazione di una stringa nella sezione sinistra del piè di pagina e modifica del carattere
// di una parte di questa stringa ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Impostazione del numero di pagina corrente nella sezione centrale del piè di pagina
pageSetup.SetFooter(1, "&P");
// Impostazione del conteggio delle pagine nella sezione destra del piè di pagina
pageSetup.SetFooter(2, "&N");
// Salva la cartella di lavoro.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Conclusione

Ora hai imparato come impostare intestazioni e piè di pagina in Excel utilizzando Aspose.Cells per .NET. Questo tutorial ti ha guidato attraverso ogni fase del processo, dalla configurazione dell'ambiente al salvataggio della cartella di lavoro modificata. Sentiti libero di esplorare ulteriormente le funzionalità di Aspose.Cells per eseguire ulteriori manipolazioni nei tuoi file Excel.

### Domande frequenti (FAQ)

#### 1. Come posso installare Aspose.Cells per .NET sul mio sistema?
Per installare Aspose.Cells per .NET, è necessario scaricare il pacchetto di installazione dal sito ufficiale Aspose e seguire le istruzioni fornite nella documentazione.

#### 2. Questo metodo funziona con tutte le versioni di Excel?
Sì, il metodo di impostazione di intestazioni e piè di pagina con Aspose.Cells per .NET funziona con tutte le versioni supportate di Excel.

#### 3. Posso personalizzare ulteriormente intestazioni e piè di pagina?
Sì, Aspose.Cells offre una vasta gamma di funzionalità per personalizzare intestazioni e piè di pagina, inclusi posizionamento del testo, colore, carattere, numeri di pagina e altro ancora.

#### 4. Come posso aggiungere informazioni dinamiche alle intestazioni e ai piè di pagina?
È possibile utilizzare variabili speciali e codici di formattazione per aggiungere informazioni dinamiche come data corrente, ora, nome file, numero di pagina, ecc. alle intestazioni e ai piè di pagina.

#### 5. Posso rimuovere intestazioni e piè di pagina dopo averli impostati?
 Sì, puoi rimuovere intestazioni e piè di pagina utilizzando il file`ClearHeaderFooter` metodo del`PageSetup` oggetto. Ciò ripristinerà le intestazioni e i piè di pagina predefiniti.