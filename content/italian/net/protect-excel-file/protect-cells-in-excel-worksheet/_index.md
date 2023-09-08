---
title: Proteggi le celle nel foglio di lavoro Excel
linktitle: Proteggi le celle nel foglio di lavoro Excel
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come proteggere celle specifiche in Excel con Aspose.Cells per .NET. Tutorial passo passo in C#.
type: docs
weight: 30
url: /it/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
Microsoft Excel è uno strumento ampiamente utilizzato per creare e gestire fogli di calcolo. Una delle funzionalità principali di Excel è la capacità di proteggere determinate celle per preservare l'integrità dei dati. In questo tutorial, ti guideremo passo dopo passo per proteggere celle specifiche in un foglio di calcolo Excel utilizzando Aspose.Cells per .NET. Aspose.Cells per .NET è una potente libreria di programmazione che semplifica la manipolazione dei file Excel con grande flessibilità e funzionalità avanzate. Segui i passaggi forniti per scoprire come proteggere le tue celle importanti e mantenere i tuoi dati al sicuro.

## Passaggio 1: configurazione dell'ambiente

Assicurati di avere Aspose.Cells per .NET installato nel tuo ambiente di sviluppo. Scarica la libreria dal sito Web ufficiale di Aspose e controlla la documentazione per le istruzioni di installazione.

## Passaggio 2: inizializzazione della cartella di lavoro e del foglio di lavoro

Per iniziare, dobbiamo creare una nuova cartella di lavoro e ottenere il riferimento al foglio di lavoro in cui vogliamo proteggere le celle. Utilizza il seguente codice:

```csharp
// Percorso della directory dei documenti.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Crea la directory se non esiste già.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Crea una nuova cartella di lavoro
Workbook workbook = new Workbook();

// Ottieni il primo foglio di lavoro
Worksheet sheet = workbook.Worksheets[0];
```

 In questo frammento di codice definiamo innanzitutto il percorso della directory in cui verrà salvato il file Excel. Successivamente, creiamo una nuova istanza di`Workbook` class e ottieni il riferimento al primo foglio di lavoro utilizzando il file`Worksheets` proprietà.

## Passaggio 3: Definisci lo stile della cella

Ora dobbiamo definire lo stile delle celle che vogliamo proteggere. Utilizza il seguente codice:

```csharp
// Definire l'oggetto di stile
Styling styling;

// Scorri tutte le colonne del foglio di lavoro e sbloccale
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

 In questo codice, utilizziamo un ciclo per scorrere tutte le colonne del foglio di lavoro e sbloccare le relative celle impostando lo stile`IsLocked` proprietà a`false` . Usiamo quindi il`ApplyStyle` metodo per applicare lo stile alle colonne con il`StyleFlag` flag per bloccare le celle.

## Passaggio 4: proteggere celle specifiche

Ora proteggeremo le celle specifiche che vogliamo bloccare. Utilizza il seguente codice:

```csharp
// Blocca le tre celle: A1, B1, C1
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

 In questo codice, otteniamo lo stile di ogni cella specifica utilizzando il file`GetStyle` metodo, quindi impostiamo il file`IsLocked` proprietà dello stile a`true`per chiudere la cella. Infine, applichiamo lo stile aggiornato a ciascuna cella utilizzando il file`SetStyle` metodo.

## Passaggio 5: proteggere il foglio di lavoro

Ora che abbiamo definito le celle da proteggere, possiamo proteggere il foglio di lavoro stesso. Utilizza il seguente codice:

```csharp
// Proteggi il foglio di lavoro
leaf.Protect(ProtectionType.All);
```

 Questo codice utilizza il`Protect` metodo per proteggere il foglio di lavoro con il tipo di protezione specificato, in questo caso`ProtectionType.All` che protegge tutti gli elementi nel foglio di lavoro.

## Passaggio 6: salva il file Excel

Infine, salviamo il file Excel con le modifiche apportate. Utilizza il seguente codice:

```csharp
// Salva il file Excel
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

 In questo codice utilizziamo il file`Save` metodo per salvare la cartella di lavoro nella directory specificata con il file`Excel97To2003` formato.

### Codice sorgente di esempio per Proteggi celle nel foglio di lavoro Excel utilizzando Aspose.Cells per .NET 
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
// Definire l'oggetto styleflag
StyleFlag styleflag;
// Scorri tutte le colonne del foglio di lavoro e sbloccale.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Blocca le tre celle... cioè A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Infine, Proteggi il foglio adesso.
sheet.Protect(ProtectionType.All);
// Salva il file Excel.
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## Conclusione

Congratulazioni! Hai imparato come proteggere celle specifiche in un foglio di calcolo Excel utilizzando Aspose.Cells per .NET. Ora puoi applicare questa tecnica ai tuoi progetti e migliorare la sicurezza dei tuoi file Excel.


### Domande frequenti

#### D: Perché dovrei utilizzare Aspose.Cells for .NET per proteggere le celle in un foglio di calcolo Excel?

R: Aspose.Cells per .NET è una potente libreria che semplifica il lavoro con i file Excel. Offre funzionalità avanzate per proteggere celle, sbloccare intervalli, ecc.

#### D: È possibile proteggere intervalli di celle anziché singole celle?

 R: Sì, puoi definire intervalli di celle specifici da proteggere utilizzando il file`ApplyStyle` metodo con un appropriato`StyleFlag`.

#### D: Come posso aprire il file Excel protetto dopo averlo salvato?

R: Quando apri il file Excel protetto, dovrai fornire la password specificata durante la protezione del foglio di lavoro.

#### D: Esistono altri tipi di protezione che posso applicare a un foglio di calcolo Excel?

R: Sì, Aspose.Cells per .NET supporta più tipi di protezione, come protezione della struttura, protezione delle finestre, ecc. Puoi scegliere il tipo di protezione appropriato in base alle tue esigenze.