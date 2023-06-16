---
title: Proteggi riga specifica nel foglio di lavoro di Excel
linktitle: Proteggi riga specifica nel foglio di lavoro di Excel
second_title: Riferimento all'API Aspose.Cells per .NET
description: Proteggi una riga specifica in Excel con Aspose.Cells per .NET. Guida passo dopo passo per proteggere i tuoi dati riservati.
type: docs
weight: 90
url: /it/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
La protezione dei dati riservati in un foglio di calcolo Excel è essenziale per garantire la sicurezza delle informazioni. Aspose.Cells per .NET offre una potente soluzione per proteggere righe specifiche in un foglio di calcolo Excel. Questa guida illustra come proteggere una riga specifica in un foglio di lavoro di Excel utilizzando il codice sorgente C# fornito. Segui questi semplici passaggi per configurare la protezione delle righe nei tuoi file Excel.

## Passaggio 1: importa le librerie richieste

Per iniziare, assicurati di avere Aspose.Cells per .NET installato sul tuo sistema. È inoltre necessario aggiungere i riferimenti appropriati nel progetto C# per poter utilizzare la funzionalità di Aspose.Cells. Ecco il codice per importare le librerie richieste:

```csharp
// Aggiungi i riferimenti necessari
using Aspose.Cells;
```

## Passaggio 2: creazione di una cartella di lavoro e di un foglio di calcolo Excel

Dopo aver importato le librerie richieste, puoi creare una nuova cartella di lavoro Excel e un nuovo foglio di lavoro. Ecco come farlo:

```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// Crea una directory se non esiste già.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// Crea una nuova cartella di lavoro.
Workbook wb = new Workbook();

// Crea un oggetto foglio di calcolo e ottieni il primo foglio.
Worksheet sheet = wb.Worksheets[0];
```

## Passaggio 3: impostazione dello stile e del flag di stile

Ora imposteremo lo stile della cella e il flag di stile per sbloccare tutte le colonne nel foglio di lavoro. Ecco il codice necessario:

```csharp
// Imposta lo stile dell'oggetto.
Styling styling;

// Imposta l'oggetto styleflag.
StyleFlag flag;

// Scorri tutte le colonne nel foglio di lavoro e sbloccale.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Passaggio 4: proteggere la linea specifica

Ora proteggeremo la riga specifica nel foglio di lavoro. Bloccheremo la prima riga per impedire qualsiasi modifica. Ecco come:

```csharp
// Ottieni lo stile della prima riga.
style = sheet.Cells.Rows[0].Style;

// Bloccalo.
style. IsLocked = true;

// Crea un'istanza della bandiera.
flag = new StyleFlag();

// Impostare il parametro di blocco.
flag. Locked = true;

// Applicare lo stile alla prima riga.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## Passaggio 5: protezione del foglio di lavoro

Infine, proteggeremo l'intero foglio di lavoro Excel per impedire modifiche non autorizzate. Ecco come:

```csharp
// Proteggi il foglio di lavoro.
sheet.Protect(ProtectionType.All);
```

## Passaggio 6: salvare il file Excel protetto

Una volta che hai finito di proteggere la riga specifica nel foglio di lavoro di Excel, puoi salvare il file Excel protetto sul tuo sistema. Ecco come:

```csharp
// Salva il file Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Dopo aver seguito questi passaggi, avrai protetto con successo una riga specifica nel tuo foglio di calcolo Excel utilizzando Aspose.Cells per .NET.

### Esempio di codice sorgente per Proteggi riga specifica nel foglio di lavoro Excel utilizzando Aspose.Cells per .NET 
```csharp
// Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crea directory se non è già presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Crea una nuova cartella di lavoro.
Workbook wb = new Workbook();
// Crea un oggetto foglio di lavoro e ottieni il primo foglio.
Worksheet sheet = wb.Worksheets[0];
// Definire l'oggetto stile.
Style style;
//Definire l'oggetto styleflag.
StyleFlag flag;
// Passa in rassegna tutte le colonne del foglio di lavoro e sbloccale.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Ottieni lo stile della prima riga.
style = sheet.Cells.Rows[0].Style;
// Bloccalo.
style.IsLocked = true;
// Crea un'istanza della bandiera.
flag = new StyleFlag();
// Impostare l'impostazione di blocco.
flag.Locked = true;
// Applicare lo stile alla prima riga.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Proteggi il foglio.
sheet.Protect(ProtectionType.All);
// Salva il file excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Conclusione

La protezione dei dati nei file Excel è fondamentale per impedire accessi non autorizzati o modifiche indesiderate. Utilizzando la libreria Aspose.Cells per .NET, puoi facilmente proteggere righe specifiche in un foglio di calcolo Excel utilizzando il codice sorgente C# fornito. Segui questa guida dettagliata per aggiungere un ulteriore livello di sicurezza ai tuoi file Excel.

### Domande frequenti

#### La protezione delle righe specifiche funziona in tutte le versioni di Excel?
Sì, la protezione di riga specifica che utilizza Aspose.Cells per .NET funziona in tutte le versioni supportate di Excel.

#### Posso proteggere più righe specifiche in un foglio di calcolo Excel?
Sì, puoi proteggere più righe specifiche utilizzando metodi simili descritti in questa guida.

#### Come posso sbloccare una riga specifica in un foglio di calcolo Excel?
 Per sbloccare una riga specifica, è necessario modificare di conseguenza il codice sorgente utilizzando il file`IsLocked` metodo del`Style` oggetto.