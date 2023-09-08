---
title: Modifica intervalli nel foglio di lavoro Excel
linktitle: Modifica intervalli nel foglio di lavoro Excel
second_title: Aspose.Cells per riferimento API .NET
description: Impara a modificare intervalli specifici in un foglio di calcolo Excel con Aspose.Cells per .NET. Tutorial passo passo in C#.
type: docs
weight: 20
url: /it/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
Microsoft Excel è un potente strumento per creare e gestire fogli di calcolo, offrendo molte funzionalità per controllare e proteggere i dati. Una di queste funzionalità è consentire agli utenti di modificare intervalli specifici in un foglio di lavoro proteggendo al contempo altre parti. In questo tutorial, ti guideremo passo dopo passo per implementare questa funzionalità utilizzando Aspose.Cells per .NET, una libreria popolare per lavorare con file Excel a livello di codice.

L'utilizzo di Aspose.Cells per .NET ti consentirà di manipolare facilmente gli intervalli in un foglio di calcolo Excel, fornendo un'interfaccia intuitiva e funzionalità avanzate. Seguire i passaggi seguenti per consentire agli utenti di modificare intervalli specifici in un foglio di calcolo Excel utilizzando Aspose.Cells per .NET.
## Passaggio 1: configurazione dell'ambiente

Assicurati di avere Aspose.Cells per .NET installato nel tuo ambiente di sviluppo. Scarica la libreria dal sito Web ufficiale di Aspose e controlla la documentazione per le istruzioni di installazione.

## Passaggio 2: inizializzazione della cartella di lavoro e del foglio di lavoro

Per iniziare, dobbiamo creare una nuova cartella di lavoro e ottenere il riferimento al foglio di lavoro in cui vogliamo consentire la modifica degli intervalli. Utilizzare il seguente codice per ottenere ciò:

```csharp
// Percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Crea la directory se non esiste già.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Creare un'istanza di una nuova cartella di lavoro
Workbook workbook = new Workbook();

// Ottieni il primo foglio di lavoro (impostazione predefinita)
Worksheet sheet = workbook.Worksheets[0];
```

 In questo frammento di codice definiamo innanzitutto il percorso della directory in cui verrà salvato il file Excel. Successivamente, creiamo una nuova istanza di`Workbook` class e ottieni il riferimento al primo foglio di lavoro utilizzando il file`Worksheets` proprietà.

## Passaggio 3: ottieni intervalli modificabili

Ora dobbiamo recuperare gli intervalli in cui vogliamo consentire la modifica. Utilizza il seguente codice:

```csharp
// Ottieni gli intervalli modificabili
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## Passaggio 4: imposta l'intervallo protetto

Prima di consentire la modifica degli intervalli, è necessario definire un intervallo protetto. Ecco come:

```csharp
// Definire un intervallo protetto
ProtectedRange ProtectedRange;

// Crea l'intervallo
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

 In questo codice creiamo una nuova istanza di`ProtectedRange` classe e utilizzare il file`Add` metodo per specificare l'intervallo da proteggere.

## Passaggio 5: specificare la password

Per migliorare la sicurezza, è possibile specificare una password per l'intervallo protetto. Ecco come:

```csharp
// Specificare la password
protectedBeach.Password = "YOUR_PASSWORD";
```

## Passaggio 6: proteggere il foglio di lavoro

Ora che abbiamo impostato l'intervallo protetto, possiamo proteggere il foglio di lavoro per impedire modifiche non autorizzate. Utilizza il seguente codice:

```csharp
// Proteggi il foglio di lavoro
leaf.Protect(ProtectionType.All);
```

## Passaggio 7: salva il file Excel

Infine, salviamo il file Excel con le modifiche apportate. Ecco il codice necessario:

```csharp
// Salva il file Excel
workbook.Save(dataDir + "protectedrange.out.xls");
```

### Codice sorgente di esempio per Modifica intervalli nel foglio di lavoro Excel utilizzando Aspose.Cells per .NET 
```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crea directory se non è già presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// Creare un'istanza di una nuova cartella di lavoro
Workbook book = new Workbook();

// Ottieni il primo foglio di lavoro (predefinito).
Worksheet sheet = book.Worksheets[0];

// Ottieni gli intervalli di modifica consentiti
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;

// Definire l'intervallo protetto
ProtectedRange proteced_range;

// Crea l'intervallo
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];

// Specificare la password
proteced_range.Password = "YOUR_PASSWORD";

// Proteggi il foglio
sheet.Protect(ProtectionType.All);

// Salva il file Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## Conclusione

Congratulazioni! Hai imparato come consentire agli utenti di modificare intervalli specifici in un foglio di calcolo Excel utilizzando Aspose.Cells per .NET. Ora puoi applicare questa tecnica ai tuoi progetti e migliorare la sicurezza dei tuoi file Excel.


#### Domande frequenti

#### D: Perché dovrei utilizzare Aspose.Cells per .NET per modificare gli intervalli in un foglio di calcolo Excel?

R: Aspose.Cells per .NET offre un'API potente e facile da usare per lavorare con file Excel. Fornisce funzionalità avanzate, come la manipolazione della gamma, la protezione del foglio di lavoro, ecc.

#### D: Posso impostare più intervalli modificabili in un foglio di lavoro?

 R: Sì, puoi definire più intervalli modificabili utilizzando`Add` metodo del`ProtectedRangeCollection` collezione. Ciascun intervallo può avere le proprie impostazioni di protezione.

####  D: È possibile eliminare un intervallo modificabile dopo averlo definito?

 R: Sì, puoi utilizzare il`RemoveAt` metodo del`ProtectedRangeCollection` collection per rimuovere un intervallo modificabile specifico specificandone l'indice.

#### D: Come posso aprire il file Excel protetto dopo averlo salvato?

R: Sarà necessario fornire la password specificata durante la creazione dell'intervallo protetto per aprire il file Excel protetto. Assicurati di conservare la password in un luogo sicuro per evitare di perdere l'accesso ai dati.