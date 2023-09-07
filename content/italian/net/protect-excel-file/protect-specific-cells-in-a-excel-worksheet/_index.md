---
title: Proteggi celle specifiche in un foglio di lavoro Excel
linktitle: Proteggi celle specifiche in un foglio di lavoro Excel
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come proteggere celle specifiche in Excel con Aspose.Cells per .NET. Tutorial passo passo in C#.
type: docs
weight: 70
url: /it/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
In questo tutorial, esamineremo il codice sorgente C# che utilizza la libreria Aspose.Cells per proteggere celle specifiche in un foglio di calcolo Excel. Esamineremo ogni passaggio del codice e spiegheremo come funziona. Seguire attentamente le istruzioni per ottenere i risultati desiderati.

## Passaggio 1: prerequisiti

Prima di iniziare, assicurati di aver installato la libreria Aspose.Cells per .NET. Puoi ottenerlo dal sito ufficiale di Aspose. Assicurati inoltre di disporre di una versione recente di Visual Studio o di qualsiasi altro ambiente di sviluppo C#.

## Passaggio 2: importa gli spazi dei nomi richiesti

Per utilizzare la libreria Aspose.Cells, dobbiamo importare gli spazi dei nomi necessari nel nostro codice. Aggiungi le seguenti righe all'inizio del file sorgente C#:

```csharp
using Aspose.Cells;
```

## Passaggio 3: creazione di una cartella di lavoro di Excel

In questo passaggio, creeremo una nuova cartella di lavoro di Excel. Utilizzare il codice seguente per creare una cartella di lavoro di Excel:

```csharp
// Percorso della directory dei documenti.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Crea una nuova cartella di lavoro.
Workbook wb = new Workbook();
```

 Assicurati di sostituire`"YOUR_DOCUMENTS_DIR"` con il percorso appropriato alla directory dei documenti.

## Passaggio 4: creazione di un foglio di calcolo

Ora che abbiamo creato la cartella di lavoro di Excel, creiamo un foglio di lavoro e otteniamo il primo foglio. Usa il seguente codice:

```csharp
// Crea un oggetto foglio di calcolo e ottieni il primo foglio.
Worksheet sheet = wb.Worksheets[0];
```

## Passaggio 5: definizione dello stile

In questo passaggio, definiremo lo stile da applicare a celle specifiche. Usa il seguente codice:

```csharp
// Definizione dell'oggetto stile.
Styling styling;
```

## Passaggio 6: loop per sbloccare tutte le colonne

Ora passeremo in rassegna tutte le colonne del foglio di lavoro e le sbloccheremo. Usa il seguente codice:

```csharp
// Passa in rassegna tutte le colonne del foglio di lavoro e sbloccale.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Passaggio 7: blocco di celle specifiche

In questo passaggio, bloccheremo celle specifiche. Usa il seguente codice:

```csharp
//Blocco di tutte e tre le celle... cioè A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## Passaggio 8: protezione del foglio di lavoro

Infine, proteggeremo il foglio di lavoro per impedire la modifica di celle specifiche. Usa il seguente codice:

```csharp
// Proteggi il foglio di lavoro.
sheet.Protect(ProtectionType.All);
```

## Passaggio 9: salvare il file Excel

Ora salveremo il file Excel modificato. Usa il seguente codice:

```csharp
// Salva il file Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Assicurati di specificare il percorso corretto per salvare il file Excel modificato.

### Esempio di codice sorgente per Proteggi celle specifiche in un foglio di lavoro Excel utilizzando Aspose.Cells per .NET 
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
// Definire l'oggetto styleflag
StyleFlag styleflag;
// Passa in rassegna tutte le colonne del foglio di lavoro e sbloccale.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Blocca le tre celle ... cioè A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Infine, proteggi il foglio ora.
sheet.Protect(ProtectionType.All);
// Salva il file excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Conclusione

Congratulazioni! Ora hai il codice sorgente C# che ti consente di proteggere celle specifiche in un foglio di lavoro di Excel utilizzando la libreria Aspose.Cells per .NET. Sentiti libero di personalizzare il codice in base alle tue esigenze specifiche.

### FAQ (Domande frequenti)

#### Questo codice funziona con le versioni recenti di Excel?

Sì, questo codice funziona con le versioni recenti di Excel, inclusi i file in formato Excel 2010 e versioni successive.

#### Posso proteggere altre celle oltre ad A1, B1 e C1?

Sì, puoi modificare il codice per bloccare altre celle specifiche regolando i riferimenti di cella nelle righe di codice corrispondenti.

#### Come posso sbloccare nuovamente le celle bloccate?

 Puoi usare`SetStyle` metodo con`IsLocked` impostato`false` per sbloccare le celle.

#### Posso aggiungere più fogli di lavoro alla cartella di lavoro?

 Sì, puoi aggiungere altri fogli di lavoro alla cartella di lavoro utilizzando il file`Worksheets.Add()`metodo e ripetere i passaggi di protezione della cella per ogni foglio di lavoro.

#### Come posso modificare il formato di salvataggio del file Excel?

 È possibile modificare il formato di salvataggio utilizzando il file`SaveFormat` metodo con il formato desiderato, ad esempio`SaveFormat.Xlsx` per Excel 2007 e versioni successive.