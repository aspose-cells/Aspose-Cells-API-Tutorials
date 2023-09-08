---
title: Proteggi foglio di lavoro Excel
linktitle: Proteggi foglio di lavoro Excel
second_title: Aspose.Cells per riferimento API .NET
description: Scopri in questo tutorial come proteggere un foglio di calcolo Excel utilizzando Aspose.Cells per .NET. Guida passo passo in C#.
type: docs
weight: 50
url: /it/net/protect-excel-file/protect-excel-worksheet/
---
In questo tutorial esamineremo alcuni codici sorgente C# che utilizzano la libreria Aspose.Cells per proteggere un foglio di calcolo Excel. Esamineremo ogni passaggio del codice e spiegheremo come funziona. Assicurati di seguire attentamente le istruzioni per ottenere i risultati desiderati.

## Passaggio 1: prerequisiti

Prima di iniziare, assicurati di aver installato la libreria Aspose.Cells per .NET. Puoi ottenerlo dal sito ufficiale di Aspose. Assicurati inoltre di avere una versione recente di Visual Studio o qualsiasi altro ambiente di sviluppo C#.

## Passaggio 2: importa gli spazi dei nomi richiesti

Per utilizzare la libreria Aspose.Cells, dobbiamo importare gli spazi dei nomi necessari nel nostro codice. Aggiungi le seguenti righe all'inizio del file sorgente C#:

```csharp
using Aspose.Cells;
using System.IO;
```

## Passaggio 3: caricare il file Excel

In questo passaggio caricheremo il file Excel che vogliamo proteggere. Assicurati di specificare il percorso corretto della directory contenente il file Excel. Utilizza il seguente codice per caricare il file:

```csharp
// Percorso della directory dei documenti.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Crea un flusso di file contenente il file Excel da aprire.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Creare un'istanza di un oggetto cartella di lavoro.
//Apri il file Excel tramite flusso di file.
Workbook excel = new Workbook(fstream);
```

 Assicurati di sostituire`"YOUR_DOCUMENTS_DIR"` con il percorso appropriato alla directory dei documenti.

## Passaggio 4: accedi al foglio di calcolo

Ora che abbiamo caricato il file Excel, possiamo accedere al primo foglio di lavoro. Utilizzare il codice seguente per accedere al primo foglio di lavoro:

```csharp
// Accesso al primo foglio di lavoro nel file Excel.
Worksheet worksheet = excel.Worksheets[0];
```

## Passaggio 5: proteggere il foglio di lavoro

In questo passaggio, proteggeremo il foglio di calcolo utilizzando una password. Utilizza il seguente codice per proteggere il foglio di calcolo:

```csharp
// Proteggi il foglio di lavoro con una password.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 Sostituire`"YOUR_PASSWORD"` con la password che desideri utilizzare per proteggere il foglio di calcolo.

## Passaggio 6: salvare il file Excel modificato Ora che lo abbiamo protetto

é il foglio di calcolo, salveremo il file Excel modificato nel formato predefinito. Utilizzare il seguente codice per salvare il file Excel:

```csharp
// Salva il file Excel modificato nel formato predefinito.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Assicurati di specificare il percorso corretto per salvare il file Excel modificato.

## Passaggio 7: chiudere il flusso di file

Per rilasciare tutte le risorse, dobbiamo chiudere il flusso di file utilizzato per caricare il file Excel. Utilizzare il codice seguente per chiudere il flusso di file:

```csharp
// Chiudi il flusso di file per rilasciare tutte le risorse.
fstream.Close();
```

Assicurati di includere questo passaggio alla fine del codice.


### Codice sorgente di esempio per proteggere il foglio di lavoro Excel utilizzando Aspose.Cells per .NET 
```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creazione di un flusso di file contenente il file Excel da aprire
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Creazione di un'istanza di un oggetto cartella di lavoro
// Apertura del file Excel tramite il flusso di file
Workbook excel = new Workbook(fstream);
// Accesso al primo foglio di lavoro nel file Excel
Worksheet worksheet = excel.Worksheets[0];
// Proteggere il foglio di lavoro con una password
worksheet.Protect(ProtectionType.All, "aspose", null);
// Salvataggio del file Excel modificato nel formato predefinito
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// Chiusura del flusso di file per liberare tutte le risorse
fstream.Close();
```

## Conclusione

Congratulazioni! Ora disponi di codice sorgente C# che ti consente di proteggere un foglio di calcolo Excel utilizzando la libreria Aspose.Cells per .NET. Assicurati di seguire attentamente i passaggi e di personalizzare il codice in base alle tue esigenze specifiche.

### FAQ (domande frequenti)

#### È possibile proteggere più fogli di lavoro in un file Excel?

R: Sì, puoi proteggere più fogli di lavoro in un file Excel ripetendo i passaggi 4-6 per ciascun foglio di lavoro.

#### Come posso specificare autorizzazioni specifiche per gli utenti autorizzati?

 R: Puoi utilizzare le opzioni aggiuntive fornite da`Protect`metodo per specificare autorizzazioni specifiche per gli utenti autorizzati. Consulta la documentazione di Aspose.Cells per ulteriori informazioni.

#### Posso proteggere il file Excel stesso con una password?

R: Sì, puoi proteggere con password il file Excel stesso utilizzando altri metodi forniti dalla libreria Aspose.Cells. Fare riferimento alla documentazione per esempi specifici.

#### La libreria Aspose.Cells supporta altri formati di file Excel?

R: Sì, la libreria Aspose.Cells supporta un'ampia gamma di formati di file Excel, inclusi XLSX, XLSM, XLSB, CSV, ecc.