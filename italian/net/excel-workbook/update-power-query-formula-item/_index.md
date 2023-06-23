---
title: Aggiorna elemento formula Power Query
linktitle: Aggiorna elemento formula Power Query
second_title: Riferimento all'API Aspose.Cells per .NET
description: Scopri come aggiornare gli elementi delle formule di Power Query nei file Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 160
url: /it/net/excel-workbook/update-power-query-formula-item/
---
L'aggiornamento di un elemento della formula di Power Query è un'operazione comune quando si lavora con i dati nei file di Excel. Con Aspose.Cells per .NET, puoi facilmente aggiornare un elemento formula di Power Query seguendo questi passaggi:

## Passaggio 1: specificare le directory di origine e di output

Innanzitutto, è necessario specificare la directory di origine in cui si trova il file Excel contenente le formule di Power Query da aggiornare, nonché la directory di output in cui si desidera salvare il file modificato. Ecco come farlo usando Aspose.Cells:

```csharp
// directory di origine
string SourceDir = RunExamples.Get_SourceDirectory();

// Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
```

## Passaggio 2: caricare la cartella di lavoro Excel di origine

Successivamente, è necessario caricare la cartella di lavoro di Excel di origine in cui si desidera aggiornare l'elemento della formula di Power Query. Ecco come farlo:

```csharp
// Carica la cartella di lavoro di Excel di origine
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Passaggio 3: sfoglia e aggiorna gli elementi della formula di Power Query

Dopo aver caricato la cartella di lavoro, puoi passare alla raccolta di formule di Power Query e sfogliare ogni formula e i relativi elementi. In questo esempio, cerchiamo l'elemento formula con il nome "Sorgente" e ne aggiorniamo il valore. Di seguito è riportato un codice di esempio per aggiornare un elemento formula di Power Query:

```csharp
// Accedi alla raccolta di formule di Power Query
DataMashup mashupData = workbook.DataMashup;

// Passa attraverso le formule di Power Query e i relativi elementi
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## Passaggio 4: salvare la cartella di lavoro Excel di output

Dopo aver aggiornato l'elemento della formula di Power Query, è possibile salvare la cartella di lavoro di Excel modificata nella directory di output specificata. Ecco come farlo:

```csharp
// Salva la cartella di lavoro Excel di output
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Codice sorgente di esempio per aggiornare l'elemento della formula di Power Query utilizzando Aspose.Cells per .NET 
```csharp
// Directory di lavoro
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Salva la cartella di lavoro di output.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Conclusione

L'aggiornamento degli elementi della formula di Power Query è un'operazione essenziale quando si utilizza Aspose.Cells per manipolare ed elaborare i dati nei file Excel. Seguendo i passaggi sopra indicati, puoi facilmente aggiornare gli elementi della formula

### Domande frequenti

#### D: Cos'è Power Query in Excel?
     
R: Power Query è una funzionalità di Excel che consente di raccogliere, trasformare e caricare dati da origini diverse. Offre potenti strumenti per pulire, combinare e rimodellare i dati prima di importarli in Excel.

#### D: Come faccio a sapere se un elemento formula di Power Query è stato aggiornato correttamente?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### D: Posso aggiornare più elementi formula di Power Query contemporaneamente?
    
R: Sì, puoi scorrere la raccolta di elementi della formula di Power Query e aggiornare più elementi in un unico ciclo, a seconda delle tue esigenze specifiche.

#### D: Ci sono altre operazioni che posso eseguire sulle formule di Power Query con Aspose.Cells?
    
R: Sì, Aspose.Cells offre una gamma completa di funzionalità per lavorare con le formule di Power Query, inclusa la creazione, l'eliminazione, la copia e la ricerca di formule in una cartella di lavoro di Excel.