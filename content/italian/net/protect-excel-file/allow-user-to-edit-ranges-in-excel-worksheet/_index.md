---
title: Consenti all'utente di modificare gli intervalli nel foglio di lavoro di Excel
linktitle: Consenti all'utente di modificare gli intervalli nel foglio di lavoro di Excel
second_title: Aspose.Cells per riferimento API .NET
description: Consenti agli utenti di modificare intervalli specifici in un foglio di calcolo Excel utilizzando Aspose.Cells per .NET. Guida passo passo con codice sorgente in C#.
type: docs
weight: 10
url: /it/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
In questa guida ti spiegheremo come utilizzare Aspose.Cells per .NET per consentire all'utente di modificare intervalli specifici in un foglio di calcolo Excel. Seguire i passaggi seguenti per eseguire questa attività.

## Passaggio 1: configurazione dell'ambiente

Assicurati di aver configurato il tuo ambiente di sviluppo e installato Aspose.Cells per .NET. È possibile scaricare l'ultima versione della libreria dal sito Web ufficiale di Aspose.

## Passaggio 2: importa gli spazi dei nomi richiesti

Nel tuo progetto C#, importa gli spazi dei nomi necessari per lavorare con Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Passaggio 3: impostazione del percorso della directory dei documenti

 Dichiarare a`dataDir` variabile per specificare il percorso della directory in cui si desidera salvare il file Excel generato:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Assicurati di sostituire`"YOUR_DOCUMENT_DIRECTORY"` con il percorso corretto sul tuo sistema.

## Passaggio 4: creazione di un oggetto cartella di lavoro

Crea un'istanza di un nuovo oggetto cartella di lavoro che rappresenta la cartella di lavoro di Excel che desideri creare:

```csharp
Workbook book = new Workbook();
```

## Passaggio 5: accesso al primo foglio di lavoro

Passare al primo foglio di lavoro nella cartella di lavoro di Excel utilizzando il codice seguente:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Passaggio 6: recupero degli intervalli di modifica autorizzati

 Ottieni la raccolta degli intervalli di modifica consentiti utilizzando il file`AllowEditRanges` proprietà:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Passaggio 7: definire un intervallo protetto

 Definire un intervallo protetto utilizzando`Add` metodo del`AllowEditRanges` collezione:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Qui abbiamo creato un intervallo protetto "r2" che si estende dalla cella A1 alla cella C3.

## Passaggio 8: specifica della password

 Specificare una password per l'intervallo protetto utilizzando il file`Password` proprietà:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Assicurati di sostituire`"YOUR_PASSWORD"` con la password desiderata.

## Passaggio 9: proteggere il foglio di lavoro

 Proteggi il foglio di lavoro utilizzando il file`Protect` metodo del`Worksheet` oggetto:

```csharp
sheet.Protect(ProtectionType.All);
```

Ciò proteggerà il foglio di calcolo impedendo qualsiasi modifica al di fuori degli intervalli consentiti.

## Passaggio 10: registrazione del

  file Excel

 Salvare il file Excel generato utilizzando il file`Save` metodo del`Workbook` oggetto:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Assicurati di specificare il nome del file desiderato e il percorso corretto.

### Codice sorgente di esempio per Consenti all'utente di modificare gli intervalli nel foglio di lavoro di Excel utilizzando Aspose.Cells per .NET 
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
proteced_range.Password = "123";
// Proteggi il foglio
sheet.Protect(ProtectionType.All);
// Salva il file Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## Conclusione

Ora hai imparato come utilizzare Aspose.Cells per .NET per consentire all'utente di modificare intervalli specifici in un foglio di calcolo Excel. Sentiti libero di esplorare ulteriormente le funzionalità offerte da Aspose.Cells per soddisfare le tue esigenze specifiche.


### Domande frequenti

#### 1. Come consentire all'utente di modificare intervalli specifici nel foglio di calcolo Excel?

 Puoi usare il`ProtectedRangeCollection` classe per definire gli intervalli di modifica consentiti. Usa il`Add` metodo per creare un nuovo intervallo protetto con le celle desiderate.

#### 2. Posso impostare una password per gli intervalli di modifica autorizzati?

 Sì, puoi specificare una password utilizzando il file`Password` proprietà del`ProtectedRange` oggetto. Ciò limiterà l'accesso solo agli utenti con la password.

#### 3. Come posso proteggere il foglio di calcolo una volta impostati gli intervalli consentiti?

 Usa il`Protect` metodo del`Worksheet` oggetto per proteggere il foglio di lavoro. Ciò impedirà qualsiasi modifica al di fuori degli intervalli consentiti, eventualmente richiedendo una password se ne hai specificata una.