---
title: Aggiorna elemento formula Power Query
linktitle: Aggiorna elemento formula Power Query
second_title: Aspose.Cells per riferimento API .NET
description: Scopri come aggiornare gli elementi della formula Power Query nei file Excel utilizzando Aspose.Cells per .NET.
type: docs
weight: 160
url: /it/net/excel-workbook/update-power-query-formula-item/
---
L'aggiornamento di un elemento formula di Power Query è un'operazione comune quando si lavora con i dati nei file Excel. Con Aspose.Cells per .NET, puoi aggiornare facilmente un elemento formula Power Query seguendo questi passaggi:

## Passaggio 1: specificare le directory di origine e di output

Innanzitutto è necessario specificare la directory di origine in cui si trova il file Excel contenente le formule di Power Query da aggiornare, nonché la directory di output in cui si desidera salvare il file modificato. Ecco come farlo utilizzando Aspose.Cells:

```csharp
// directory di origine
string SourceDir = RunExamples.Get_SourceDirectory();

// Cartella di destinazione
string outputDir = RunExamples.Get_OutputDirectory();
```

## Passaggio 2: caricare la cartella di lavoro Excel di origine

Successivamente, è necessario caricare la cartella di lavoro di Excel di origine in cui si desidera aggiornare l'elemento formula di Power Query. Ecco come farlo:

```csharp
// Carica la cartella di lavoro Excel di origine
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Passaggio 3: sfogliare e aggiornare gli elementi della formula di Power Query

Dopo aver caricato la cartella di lavoro, è possibile passare alla raccolta di formule di Power Query ed esplorare ogni formula e i relativi elementi. In questo esempio, stiamo cercando l'elemento formula con il nome "Sorgente" e aggiornandone il valore. Ecco un codice di esempio per aggiornare un elemento formula di Power Query:

```csharp
// Accedi alla raccolta di formule di Power Query
DataMashup mashupData = workbook.DataMashup;

// Passare in rassegna le formule di Power Query e i relativi elementi
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

Dopo aver aggiornato l'elemento formula di Power Query, è possibile salvare la cartella di lavoro di Excel modificata nella directory di output specificata. Ecco come farlo:

```csharp
// Salvare la cartella di lavoro Excel di output
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Codice sorgente di esempio per l'aggiornamento dell'elemento formula Power Query utilizzando Aspose.Cells per .NET 
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
// Salvare la cartella di lavoro di output.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Conclusione

L'aggiornamento degli elementi della formula di Power Query è un'operazione essenziale quando si utilizza Aspose.Cells per manipolare ed elaborare i dati nei file Excel. Seguendo i passaggi sopra indicati, puoi aggiornare facilmente gli elementi della formula

### Domande frequenti

#### D: Cos'è Power Query in Excel?
     
R: Power Query è una funzionalità di Excel che consente di raccogliere, trasformare e caricare dati da origini diverse. Offre potenti strumenti per pulire, combinare e rimodellare i dati prima di importarli in Excel.

#### D: come faccio a sapere se un elemento formula di Power Query è stato aggiornato correttamente?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### D: posso aggiornare più elementi della formula Power Query contemporaneamente?
    
R: Sì, puoi scorrere la raccolta di elementi della formula Power Query e aggiornare più elementi in un unico ciclo, a seconda delle tue esigenze specifiche.

#### D: ci sono altre operazioni che posso eseguire sulle formule di Power Query con Aspose.Cells?
    
R: Sì, Aspose.Cells offre una gamma completa di funzionalità per lavorare con le formule di Power Query, inclusa la creazione, l'eliminazione, la copia e la ricerca di formule in una cartella di lavoro di Excel.