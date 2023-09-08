---
title: Rimuovi le impostazioni della stampante esistente dei fogli di lavoro
linktitle: Rimuovi le impostazioni della stampante esistente dei fogli di lavoro
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come rimuovere le impostazioni della stampante esistente dai fogli di calcolo Excel con Aspose.Cells per .NET.
type: docs
weight: 80
url: /it/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
In questo tutorial, ti spiegheremo passo dopo passo come rimuovere le impostazioni della stampante esistenti dai fogli di lavoro in Excel utilizzando Aspose.Cells per .NET. Utilizzeremo il codice sorgente C# per illustrare il processo.

## Passaggio 1: configurazione dell'ambiente

Assicurati di avere Aspose.Cells per .NET installato sul tuo computer. Crea anche un nuovo progetto nel tuo ambiente di sviluppo preferito.

## Passaggio 2: importa le librerie necessarie

Nel file di codice, importa le librerie necessarie per lavorare con Aspose.Cells. Ecco il codice corrispondente:

```csharp
using Aspose.Cells;
```

## Passaggio 3: imposta le directory di origine e di output

Imposta rispettivamente le directory di origine e di output in cui si trova il file Excel originale e dove desideri salvare il file modificato. Utilizza il seguente codice:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Assicurati di specificare i percorsi completi delle directory.

## Passaggio 4: caricamento del file Excel di origine

Caricare il file Excel di origine utilizzando il seguente codice:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Ciò caricherà il file Excel specificato nell'oggetto cartella di lavoro.

## Passaggio 5: esplorare i fogli di lavoro

Scorrere tutti i fogli di lavoro nella cartella di lavoro utilizzando un ciclo. Utilizza il seguente codice:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // Il resto del codice verrà aggiunto nel passaggio successivo.
}
```

## Passaggio 6: eliminare le impostazioni della stampante esistenti

Controlla se esistono impostazioni della stampante per ciascun foglio di lavoro ed eliminale se necessario. Utilizza il seguente codice:

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

Salvare la cartella di lavoro modificata utilizzando il seguente codice:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Ciò salverà la cartella di lavoro modificata nella directory di output specificata.

### Codice sorgente di esempio per rimuovere le impostazioni della stampante esistente dei fogli di lavoro utilizzando Aspose.Cells per .NET 
```csharp
//Directory di origine
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
    //Accedi alla configurazione della pagina del foglio di lavoro
    PageSetup ps = ws.PageSetup;
    //Controlla se esistono le impostazioni della stampante per questo foglio di lavoro
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

Ora hai imparato come rimuovere le impostazioni della stampante esistente dai fogli di lavoro in Excel utilizzando Aspose.Cells per .NET. Questo tutorial ti ha guidato attraverso ogni fase del processo, dalla configurazione dell'ambiente alla navigazione nei fogli di calcolo e alla cancellazione delle impostazioni della stampante. Ora puoi utilizzare queste conoscenze per gestire le impostazioni della stampante nei file Excel.

### Domande frequenti

#### Q1: Come faccio a sapere se un foglio di calcolo presenta impostazioni della stampante esistenti?

 A1: È possibile verificare se esistono impostazioni della stampante per un foglio di lavoro accedendo a`PrinterSettings` proprietà del`PageSetup` oggetto. Se il valore è diverso da null, significa che esistono impostazioni della stampante esistenti.

#### Q2: Posso eliminare le impostazioni della stampante solo per un foglio di calcolo specifico?

 R2: Sì, puoi utilizzare lo stesso approccio per rimuovere le impostazioni della stampante per un foglio di lavoro specifico accedendo`PageSetup` oggetto.

#### Q3: Questo metodo rimuove anche altre impostazioni di layout?

R3: No, questo metodo elimina solo le impostazioni della stampante. Altre impostazioni di layout, come margini, orientamento della carta, ecc., rimangono invariate.

#### Q4: questo metodo funziona con tutti i formati di file Excel, come .xls e .xlsx?

A4: Sì, questo metodo funziona per tutti i formati di file Excel supportati da Aspose.Cells, inclusi .xls e .xlsx.

#### D5: Le modifiche apportate alle impostazioni della stampante sono permanenti nel file Excel modificato?

R5: Sì, le modifiche alle impostazioni della stampante vengono salvate in modo permanente nel file Excel modificato.