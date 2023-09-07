---
title: Regex Sostituisci
linktitle: Regex Sostituisci
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come eseguire la sostituzione Regex nei file Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 140
url: /it/net/excel-workbook/regex-replace/
---
La sostituzione del testo basata su espressioni regolari (Regex) è un'attività comune durante la manipolazione dei dati nei file Excel. Con Aspose.Cells per .NET, puoi eseguire facilmente una sostituzione Regex seguendo questi passaggi:

## Passaggio 1: specificare la directory di origine e la directory di output

Innanzitutto è necessario specificare la directory di origine in cui si trova il file Excel contenente i dati da sostituire, nonché la directory di output in cui si desidera salvare il file modificato. Ecco come farlo usando Aspose.Cells:

```csharp
// directory di origine
string sourceDir = RunExamples.Get_SourceDirectory();

// Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
```

## Passaggio 2: caricare il file Excel di origine

Successivamente, è necessario caricare il file Excel di origine su cui si desidera eseguire la sostituzione Regex. Ecco come farlo:

```csharp
// Carica il file Excel di origine
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## Passaggio 3: eseguire la sostituzione Regex

Dopo aver caricato il file, puoi impostare le opzioni di sostituzione, inclusa la distinzione tra maiuscole e minuscole e la corrispondenza esatta del contenuto della cella. Ecco il codice di esempio per eseguire la sostituzione Regex:

```csharp
// Imposta le opzioni di sostituzione
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

// Definire che la chiave di ricerca è un'espressione regolare
replace. RegexKey = true;

// Eseguire la sostituzione Regex
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## Passaggio 4: salvare il file Excel di output

Al termine della sostituzione Regex, è possibile salvare il file Excel modificato nella directory di output specificata. Ecco come farlo:

```csharp
// Salva il file Excel di output
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### Esempio di codice sorgente per Regex Replace utilizzando Aspose.Cells per .NET 
```csharp
//Rubrica di origine
string sourceDir = RunExamples.Get_SourceDirectory();
//Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
// Imposta su true per indicare che la chiave cercata è regex
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## Conclusione

La sostituzione Regex è una tecnica potente per modificare dinamicamente i dati in un file Excel. Con Aspose.Cells per .NET, puoi eseguire facilmente una sostituzione Regex seguendo i passaggi descritti sopra. Sperimenta con le tue espressioni regolari e sfrutta la flessibilità offerta da Aspose.Cells.

### Domande frequenti

#### D: Cos'è la sostituzione Regex?
    
R: La sostituzione Regex è una tecnica utilizzata per sostituire modelli di testo basati su espressioni regolari in un file Excel. Ciò consente modifiche rapide e accurate ai dati.

#### D: La sostituzione Regex fa distinzione tra maiuscole e minuscole?
    
R: No, con Aspose.Cells puoi specificare se la sostituzione Regex deve essere sensibile alle maiuscole o meno. Hai il pieno controllo su questa funzione.

#### D: Come posso specificare una corrispondenza esatta del contenuto della cella durante la sostituzione di Regex?
    
A: Aspose.Cells ti consente di definire se la sostituzione Regex deve corrispondere esattamente al contenuto della cella o meno. È possibile regolare questa opzione in base alle proprie esigenze.

#### D: Posso usare espressioni regolari avanzate quando sostituisco Regex con Aspose.Cells?
    
R: Sì, Aspose.Cells supporta espressioni regolari avanzate, consentendoti di eseguire sostituzioni complesse e sofisticate nei tuoi file Excel.

#### D: Come posso verificare se la sostituzione Regex ha avuto successo?
    
R: Dopo aver eseguito la sostituzione Regex, puoi verificare se l'operazione è andata a buon fine controllando l'output e assicurandoti che il file Excel di output sia stato creato correttamente.
	