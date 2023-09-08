---
title: Proteggi riga nel foglio di lavoro Excel
linktitle: Proteggi riga nel foglio di lavoro Excel
second_title: Aspose.Cells per riferimento API .NET
description: Scopri in questo tutorial come proteggere le righe di un foglio di calcolo Excel utilizzando Aspose.Cells per .NET. Tutorial passo passo in C#.
type: docs
weight: 60
url: /it/net/protect-excel-file/protect-row-in-excel-worksheet/
---
In questo tutorial esamineremo alcuni codici sorgente C# che utilizzano la libreria Aspose.Cells per proteggere le righe in un foglio di calcolo Excel. Esamineremo ogni passaggio del codice e spiegheremo come funziona. Seguire attentamente le istruzioni per ottenere i risultati desiderati.

## Passaggio 1: prerequisiti

Prima di iniziare, assicurati di aver installato la libreria Aspose.Cells per .NET. Puoi ottenerlo dal sito ufficiale di Aspose. Assicurati inoltre di avere una versione recente di Visual Studio o qualsiasi altro ambiente di sviluppo C#.

## Passaggio 2: importa gli spazi dei nomi richiesti

Per utilizzare la libreria Aspose.Cells, dobbiamo importare gli spazi dei nomi necessari nel nostro codice. Aggiungi le seguenti righe all'inizio del file sorgente C#:

```csharp
using Aspose.Cells;
```

## Passaggio 3: creazione di una cartella di lavoro Excel

In questo passaggio creeremo una nuova cartella di lavoro Excel. Utilizzare il codice seguente per creare una cartella di lavoro di Excel:

```csharp
// Percorso della directory dei documenti.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Crea una nuova cartella di lavoro.
Workbook wb = new Workbook();
```

 Assicurati di sostituire`"YOUR_DOCUMENTS_DIR"` con il percorso appropriato alla directory dei documenti.

## Passaggio 4: creazione di un foglio di calcolo

Ora che abbiamo creato la cartella di lavoro di Excel, creiamo un foglio di lavoro e otteniamo il primo foglio. Utilizza il seguente codice:

```csharp
// Crea un oggetto foglio di calcolo e ottieni il primo foglio.
Worksheet sheet = wb.Worksheets[0];
```

## Passaggio 5: definizione dello stile

In questo passaggio definiremo lo stile da applicare alle righe del foglio di calcolo. Utilizza il seguente codice:

```csharp
// Definizione dell'oggetto di stile.
Styling styling;
```

## Passaggio 6: esegui il ciclo per sbloccare tutte le colonne

Ora scorreremo tutte le colonne del foglio di lavoro e le sbloccheremo. Utilizza il seguente codice:

```csharp
// Scorri tutte le colonne del foglio di lavoro e sbloccale.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Passaggio 7: bloccare la prima riga

In questo passaggio, bloccheremo la prima riga del foglio di lavoro. Utilizza il seguente codice:

```csharp
// Ottieni lo stile della prima riga.
style = sheet.Cells.Rows[0].Style;
// Blocca lo stile.
style. IsLocked = true;
// Applica lo stile alla prima riga.
sheet.Cells.ApplyRowStyle(0, style);
```

## Passaggio 8: proteggere il foglio di lavoro

Ora che abbiamo impostato gli stili e bloccato le righe, proteggiamo il foglio di calcolo. Utilizza il seguente codice:

```csharp
// Proteggi il foglio di lavoro.
sheet.Protect(ProtectionType.All);
```

## Passaggio 9: salvataggio del file Excel

Infine, salveremo il file Excel modificato. Utilizza il seguente codice:

```csharp
// Salva il file Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Assicurati di specificare il percorso corretto per salvare il file Excel modificato.

### Codice sorgente di esempio per Proteggi riga nel foglio di lavoro Excel utilizzando Aspose.Cells per .NET 
```csharp
//Il percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crea directory se non è già presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Crea una nuova cartella di lavoro.
Workbook wb = new Workbook();
// Creare un oggetto del foglio di lavoro e ottenere il primo foglio.
Worksheet sheet = wb.Worksheets[0];
// Definire l'oggetto di stile.
Style style;
// Definire l'oggetto styleflag.
StyleFlag flag;
// Scorri tutte le colonne del foglio di lavoro e sbloccale.
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
//Istanziare la bandiera.
flag = new StyleFlag();
// Configurare l'impostazione del blocco.
flag.Locked = true;
// Applica lo stile alla prima riga.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Proteggi il foglio.
sheet.Protect(ProtectionType.All);
// Salva il file Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Conclusione

Congratulazioni! Ora disponi di codice sorgente C# che ti consente di proteggere le righe in un foglio di calcolo Excel utilizzando la libreria Aspose.Cells per .NET. Assicurati di seguire attentamente i passaggi e di personalizzare il codice in base alle tue esigenze specifiche.

### FAQ (domande frequenti)

#### Questo codice funziona con le versioni recenti di Excel?

Sì, questo codice funziona con le versioni recenti di Excel, inclusi i file in formato Excel 2010 e versioni successive.

#### Posso proteggere solo righe specifiche anziché tutte le righe nel foglio di lavoro?

Sì, puoi modificare il codice per specificare le righe specifiche che desideri proteggere. Sarà necessario regolare di conseguenza il loop e gli indici.

#### Come posso sbloccare nuovamente le linee bloccate?

 Puoi usare il`IsLocked` metodo del`Style` oggetto a cui impostare il valore`false` e sbloccare le righe.

#### È possibile proteggere più fogli di lavoro nella stessa cartella di lavoro di Excel?

Sì, puoi ripetere i passaggi di creazione di un foglio di lavoro, impostazione dello stile e protezione per ciascun foglio di lavoro nella cartella di lavoro.

#### Come posso modificare la password di protezione del foglio di calcolo?

 È possibile modificare la password utilizzando il`Protect` metodo e specificando una nuova password come argomento.