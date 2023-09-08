---
title: Inserisci immagine nel piè di pagina dell'intestazione
linktitle: Inserisci immagine nel piè di pagina dell'intestazione
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come inserire un'immagine nell'intestazione o nel piè di pagina di un documento Excel utilizzando Aspose.Cells per .NET. Guida passo passo con codice sorgente in C#.
type: docs
weight: 60
url: /it/net/excel-page-setup/insert-image-in-header-footer/
---
La possibilità di inserire un'immagine nell'intestazione o nel piè di pagina di un documento Excel può essere molto utile per personalizzare i propri report o aggiungere loghi aziendali. In questo articolo, ti guideremo passo dopo passo per inserire un'immagine nell'intestazione o nel piè di pagina di un documento Excel utilizzando Aspose.Cells per .NET. Imparerai come ottenere questo risultato utilizzando il codice sorgente C#.

## Passaggio 1: configurazione dell'ambiente

Prima di iniziare, assicurati di avere Aspose.Cells per .NET installato sul tuo computer. Crea anche un nuovo progetto nel tuo ambiente di sviluppo preferito.

## Passaggio 2: importa le librerie necessarie

Nel file di codice, importa le librerie necessarie per lavorare con Aspose.Cells. Ecco il codice corrispondente:

```csharp
using Aspose.Cells;
```

## Passaggio 3: imposta la directory dei documenti

Imposta la directory in cui si trova il documento Excel con cui vuoi lavorare. Utilizzare il codice seguente per impostare la directory:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Assicurati di specificare il percorso completo della directory.

## Passaggio 4: creazione di un oggetto cartella di lavoro

L'oggetto Workbook rappresenta il documento Excel con cui lavorerai. Puoi crearlo utilizzando il seguente codice:

```csharp
Workbook workbook = new Workbook();
```

Questo crea un nuovo oggetto cartella di lavoro vuoto.

## Passaggio 5: memorizzazione dell'URL dell'immagine

Definisci l'URL o il percorso dell'immagine che desideri inserire nell'intestazione o nel piè di pagina. Utilizza il seguente codice per memorizzare l'URL dell'immagine:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Assicurati che il percorso specificato sia corretto e che l'immagine esista in quella posizione.

## Passaggio 6: apertura del file immagine

Per aprire il file immagine, utilizzeremo un oggetto FileStream e leggeremo i dati binari dall'immagine. Ecco il codice corrispondente:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Assicurati che il percorso dell'immagine sia corretto e di disporre delle autorizzazioni corrette per accedervi.

## Passaggio 7: configurazione di PageSetup

L'oggetto PageSetup viene utilizzato per definire le impostazioni della pagina del documento Excel, inclusi l'intestazione e il piè di pagina. Utilizzare il codice seguente per ottenere l'oggetto PageSetup del primo foglio di lavoro:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

Ciò ti consentirà di accedere alle impostazioni della pagina per il primo foglio di lavoro nella cartella di lavoro.

## Passaggio 8: aggiunta dell'immagine all'intestazione

Utilizzare il metodo SetHeaderPicture() dell'oggetto PageSetup per impostare l'immagine nella sezione centrale dell'intestazione della pagina. Ecco il codice corrispondente:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Ciò aggiungerà l'immagine specificata all'intestazione della pagina.

## Passaggio 9: aggiunta di uno script all'intestazione

Per aggiungere script all'intestazione della pagina, utilizzare il metodo SetHeader() dell'oggetto PageSetup. Ecco il codice corrispondente:

```csharp
pageSetup.SetHeader(1, "&G");
```

Ciò aggiungerà lo script specificato all'intestazione della pagina. In questo esempio, lo script "&G" visualizza il numero di pagina.

## Passaggio 10: aggiungi il nome del foglio all'intestazione

Per visualizzare il nome del foglio nell'intestazione della pagina, utilizzare nuovamente il metodo SetHeader() dell'oggetto PageSetup. Ecco il codice corrispondente:

```csharp
pageSetup.SetHeader(2, "&A");
```

Ciò aggiungerà il nome del foglio all'intestazione della pagina. Lo script "&A" viene utilizzato per rappresentare il nome del foglio.

## Passaggio 11: salvataggio della cartella di lavoro

Per salvare le modifiche alla cartella di lavoro, utilizzare il metodo Save() dell'oggetto Workbook. Ecco il codice corrispondente:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Ciò salverà la cartella di lavoro con le modifiche nella directory specificata.

## Passaggio 12: chiusura di FileStream

Dopo aver letto i dati binari dall'immagine, assicurati di chiudere FileStream per liberare le risorse. Utilizzare il codice seguente per chiudere FileStream:

```csharp
inFile.Close();
```

Assicurati di chiudere sempre FileStreams quando hai finito di usarli.

### Codice sorgente di esempio per Inserisci immagine nel piè di pagina dell'intestazione utilizzando Aspose.Cells per .NET 
```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Creazione di un oggetto cartella di lavoro
Workbook workbook = new Workbook();
// Creazione di una variabile stringa per memorizzare l'URL del logo/immagine
string logo_url = dataDir + "aspose-logo.jpg";
// Dichiarazione di un oggetto FileStream
FileStream inFile;
// Dichiarazione di un array di byte
byte[] binaryData;
// Creazione dell'istanza dell'oggetto FileStream per aprire il logo/l'immagine nello stream
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// Creazione di un'istanza dell'array di byte della dimensione dell'oggetto FileStream
binaryData = new Byte[inFile.Length];
// Legge un blocco di byte dal flusso e scrive i dati in un dato buffer di array di byte.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Creazione di un oggetto PageSetup per ottenere le impostazioni della pagina del primo foglio di lavoro della cartella di lavoro
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Impostazione del logo/immagine nella sezione centrale dell'intestazione della pagina
pageSetup.SetHeaderPicture(1, binaryData);
// Impostazione dello script per il logo/immagine
pageSetup.SetHeader(1, "&G");
// Impostazione del nome del foglio nella sezione destra dell'intestazione della pagina con lo script
pageSetup.SetHeader(2, "&A");
// Salvataggio della cartella di lavoro
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//Chiusura dell'oggetto FileStream
inFile.Close();       
```
## Conclusione

Congratulazioni! Ora sai come inserire un'immagine nell'intestazione o nel piè di pagina di un documento Excel utilizzando Aspose.Cells per .NET. Questo tutorial ti ha guidato attraverso ogni fase del processo, dalla configurazione dell'ambiente al salvataggio della cartella di lavoro modificata. Sentiti libero di sperimentare di più con le funzionalità di Aspose.Cells per creare documenti Excel personalizzati e professionali.

### Domande frequenti

#### Q1: È possibile inserire più immagini nell'intestazione o nel piè di pagina di un documento Excel?

R1: Sì, puoi inserire più immagini nell'intestazione o nel piè di pagina di un documento Excel ripetendo i passaggi 8 e 9 per ogni immagine aggiuntiva.

#### Q2: Quali formati di immagine sono supportati per l'inserimento nell'intestazione o nel piè di pagina?
A2: Aspose.Cells supporta una varietà di formati immagine comuni come JPEG, PNG, GIF, BMP, ecc.

#### Q3: Posso personalizzare ulteriormente l'aspetto dell'intestazione o del piè di pagina?

R3: Sì, puoi utilizzare script e codici speciali per formattare ulteriormente e personalizzare l'aspetto dell'intestazione o del piè di pagina. Fare riferimento alla documentazione Aspose.Cells per ulteriori informazioni sulle opzioni di personalizzazione.

#### Q4: Aspose.Cells funziona con diverse versioni di Excel?

A4: Sì, Aspose.Cells è compatibile con diverse versioni di Excel tra cui Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 ed Excel 2019.

#### Q5: È possibile inserire immagini in altre parti del documento Excel, come celle o grafici?

A5: Sì, Aspose.Cells fornisce funzionalità estese per l'inserimento di immagini in diverse parti del documento Excel, incluse celle, grafici e oggetti di disegno.