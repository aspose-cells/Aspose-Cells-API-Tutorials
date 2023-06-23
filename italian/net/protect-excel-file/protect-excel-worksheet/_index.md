---
title: Proteggi il foglio di lavoro di Excel
linktitle: Proteggi il foglio di lavoro di Excel
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri in questo tutorial come proteggere un foglio di calcolo Excel utilizzando Aspose.Cells per .NET. Guida passo passo in C#.
type: docs
weight: 50
url: /it/net/protect-excel-file/protect-excel-worksheet/
---
In questo tutorial, esamineremo del codice sorgente C# che utilizza la libreria Aspose.Cells per proteggere un foglio di calcolo Excel. Esamineremo ogni passaggio del codice e spiegheremo come funziona. Assicurati di seguire attentamente le istruzioni per ottenere i risultati desiderati.

## Passaggio 1: prerequisiti

Prima di iniziare, assicurati di aver installato la libreria Aspose.Cells per .NET. Puoi ottenerlo dal sito ufficiale di Aspose. Assicurati inoltre di disporre di una versione recente di Visual Studio o di qualsiasi altro ambiente di sviluppo C#.

## Passaggio 2: importa gli spazi dei nomi richiesti

Per utilizzare la libreria Aspose.Cells, dobbiamo importare gli spazi dei nomi necessari nel nostro codice. Aggiungi le seguenti righe all'inizio del file sorgente C#:

```csharp
using Aspose.Cells;
using System.IO;
```

## Passaggio 3: caricare il file Excel

In questo passaggio, caricheremo il file Excel che vogliamo proteggere. Assicurati di specificare il percorso corretto della directory contenente il file Excel. Utilizzare il seguente codice per caricare il file:

```csharp
// Percorso della directory dei documenti.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Creare un flusso di file contenente il file Excel da aprire.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Crea un'istanza di un oggetto Workbook.
//Apri il file Excel tramite flusso di file.
Workbook excel = new Workbook(fstream);
```

 Assicurati di sostituire`"YOUR_DOCUMENTS_DIR"` con il percorso appropriato alla directory dei documenti.

## Passaggio 4: accedi al foglio di calcolo

Ora che abbiamo caricato il file Excel, possiamo accedere al primo foglio di lavoro. Utilizzare il seguente codice per accedere al primo foglio di lavoro:

```csharp
// Accesso al primo foglio di lavoro nel file Excel.
Worksheet worksheet = excel.Worksheets[0];
```

## Passaggio 5: proteggere il foglio di lavoro

In questo passaggio, proteggeremo il foglio di calcolo utilizzando una password. Utilizzare il seguente codice per proteggere il foglio di calcolo:

```csharp
// Proteggi il foglio di lavoro con una password.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 Sostituire`"YOUR_PASSWORD"` con la password che desideri utilizzare per proteggere il foglio di calcolo.

## Passaggio 6: salva il file Excel modificato Ora che abbiamo protetto

é il foglio di calcolo, salveremo il file Excel modificato nel formato predefinito. Utilizzare il seguente codice per salvare il file Excel:

```csharp
// Salva il file Excel modificato nel formato predefinito.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Assicurati di specificare il percorso corretto per salvare il file Excel modificato.

## Passaggio 7: chiudere il flusso di file

Per rilasciare tutte le risorse, dobbiamo chiudere il flusso di file utilizzato per caricare il file Excel. Utilizzare il codice seguente per chiudere il flusso di file:

```csharp
// Chiudi flusso di file per rilasciare tutte le risorse.
fstream.Close();
```

Assicurati di includere questo passaggio alla fine del codice.


### Esempio di codice sorgente per Protect Excel Worksheet utilizzando Aspose.Cells per .NET 
```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creazione di un flusso di file contenente il file Excel da aprire
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Istanziare un oggetto Workbook
// Apertura del file Excel tramite il flusso di file
Workbook excel = new Workbook(fstream);
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = excel.Worksheets[0];
// Protezione del foglio di lavoro con una password
worksheet.Protect(ProtectionType.All, "aspose", null);
// Salvataggio del file Excel modificato nel formato predefinito
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// Chiusura del flusso di file per liberare tutte le risorse
fstream.Close();
```

## Conclusione

Congratulazioni! Ora disponi del codice sorgente C# che ti consente di proteggere un foglio di calcolo Excel utilizzando la libreria Aspose.Cells per .NET. Assicurati di seguire attentamente i passaggi e personalizzare il codice in base alle tue esigenze specifiche.

### FAQ (Domande frequenti)

#### È possibile proteggere più fogli di lavoro in un unico file Excel?

R: Sì, puoi proteggere più fogli di lavoro in un file Excel ripetendo i passaggi 4-6 per ciascun foglio di lavoro.

#### Come posso specificare autorizzazioni specifiche per gli utenti autorizzati?

 R: È possibile utilizzare le opzioni aggiuntive fornite dal`Protect`metodo per specificare autorizzazioni specifiche per gli utenti autorizzati. Vedere la documentazione di Aspose.Cells per ulteriori informazioni.

#### Posso proteggere il file Excel stesso con una password?

A: Sì, puoi proteggere con password il file Excel stesso utilizzando altri metodi forniti dalla libreria Aspose.Cells. Fare riferimento alla documentazione per esempi specifici.

#### La libreria Aspose.Cells supporta altri formati di file Excel?

R: Sì, la libreria Aspose.Cells supporta un'ampia gamma di formati di file Excel, inclusi XLSX, XLSM, XLSB, CSV, ecc.