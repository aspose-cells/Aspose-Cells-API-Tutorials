---
title: Rimuovi le impostazioni della stampante esistenti dei fogli di lavoro
linktitle: Rimuovi le impostazioni della stampante esistenti dei fogli di lavoro
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come rimuovere le impostazioni della stampante esistenti dai fogli di calcolo Excel con Aspose.Cells per .NET.
type: docs
weight: 80
url: /it/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
In questo tutorial, ti guideremo passo dopo passo su come rimuovere le impostazioni della stampante esistenti dai fogli di lavoro in Excel utilizzando Aspose.Cells per .NET. Useremo il codice sorgente C# per illustrare il processo.

## Passaggio 1: configurazione dell'ambiente

Assicurati di avere Aspose.Cells per .NET installato sul tuo computer. Crea anche un nuovo progetto nel tuo ambiente di sviluppo preferito.

## Passaggio 2: importa le librerie necessarie

Nel tuo file di codice, importa le librerie necessarie per lavorare con Aspose.Cells. Ecco il codice corrispondente:

```csharp
using Aspose.Cells;
```

## Passaggio 3: imposta le directory di origine e di output

Impostare rispettivamente le directory di origine e di output in cui si trova il file Excel originale e in cui si desidera salvare il file modificato. Usa il seguente codice:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Assicurati di specificare i percorsi di directory completi.

## Passaggio 4: caricamento del file Excel di origine

Carica il file Excel di origine utilizzando il seguente codice:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Questo caricherà il file Excel specificato nell'oggetto cartella di lavoro.

## Passaggio 5: navigare nei fogli di lavoro

Scorri tutti i fogli di lavoro nella cartella di lavoro usando un ciclo. Usa il seguente codice:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // Il resto del codice verrà aggiunto nel passaggio successivo.
}
```

## Passaggio 6: eliminare le impostazioni della stampante esistenti

Controlla se esistono impostazioni della stampante per ogni foglio di lavoro e cancellale se necessario. Usa il seguente codice:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## Passaggio 7: salvataggio della cartella di lavoro modificata

Salva la cartella di lavoro modificata utilizzando il seguente codice:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Ciò salverà la cartella di lavoro modificata nella directory di output specificata.

### Codice sorgente di esempio per rimuovere le impostazioni della stampante esistente dei fogli di lavoro utilizzando Aspose.Cells per .NET 
```csharp
//Rubrica di origine
string sourceDir = RunExamples.Get_SourceDirectory();
//Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
//Carica il file Excel di origine
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Ottieni il conteggio dei fogli della cartella di lavoro
int sheetCount = wb.Worksheets.Count;
//Itera tutti i fogli
for (int i = 0; i < sheetCount; i++)
{
    //Accedi all'i-esimo foglio di lavoro
    Worksheet ws = wb.Worksheets[i];
    //Accedere all'impostazione della pagina del foglio di lavoro
    PageSetup ps = ws.PageSetup;
    //Controlla se esistono impostazioni della stampante per questo foglio di lavoro
    if (ps.PrinterSettings != null)
    {
        //Stampa il seguente messaggio
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Stampa il nome del foglio e il suo formato carta
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Rimuovere le impostazioni della stampante impostandole su null
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//Se
}//per
//Salva la cartella di lavoro
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Conclusione

Ora hai imparato come rimuovere le impostazioni della stampante esistenti dai fogli di lavoro in Excel utilizzando Aspose.Cells per .NET. Questo tutorial ti ha guidato attraverso ogni fase del processo, dalla configurazione dell'ambiente alla navigazione tra i fogli di calcolo e alla cancellazione delle impostazioni della stampante. Ora puoi usare questa conoscenza per gestire le impostazioni della stampante nei tuoi file Excel.

### FAQ

#### D1: Come faccio a sapere se un foglio di calcolo dispone di impostazioni della stampante esistenti?

 A1: è possibile verificare se esistono impostazioni della stampante per un foglio di lavoro accedendo a`PrinterSettings` proprietà del`PageSetup` oggetto. Se il valore non è nullo, significa che esistono impostazioni della stampante esistenti.

#### D2: Posso eliminare le impostazioni della stampante solo per un foglio di calcolo specifico?

 A2: Sì, è possibile utilizzare lo stesso approccio per rimuovere le impostazioni della stampante per un foglio di lavoro specifico accedendo a quel foglio di lavoro`PageSetup` oggetto.

#### D3: Questo metodo rimuove anche altre impostazioni di layout?

A3: No, questo metodo elimina solo le impostazioni della stampante. Altre impostazioni di layout, come margini, orientamento della carta, ecc., rimangono invariate.

#### D4: Questo metodo funziona per tutti i formati di file Excel, ad esempio .xls e .xlsx?

A4: Sì, questo metodo funziona per tutti i formati di file Excel supportati da Aspose.Cells, inclusi .xls e .xlsx.

#### D5: Le modifiche apportate alle impostazioni della stampante sono permanenti nel file Excel modificato?

R5: Sì, le modifiche alle impostazioni della stampante vengono salvate in modo permanente nel file Excel modificato.