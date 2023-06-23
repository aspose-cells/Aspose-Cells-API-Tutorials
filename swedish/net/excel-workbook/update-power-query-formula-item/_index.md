---
title: Uppdatera Power Query Formel Objekt
linktitle: Uppdatera Power Query Formel Objekt
second_title: Aspose.Cells för .NET API-referens
description: Lär dig hur du uppdaterar Power Query-formelelement i Excel-filer med Aspose.Cells för .NET.
type: docs
weight: 160
url: /sv/net/excel-workbook/update-power-query-formula-item/
---
Att uppdatera ett Power Query-formelobjekt är en vanlig operation när man arbetar med data i Excel-filer. Med Aspose.Cells för .NET kan du enkelt uppdatera ett Power Query-formelobjekt genom att följa dessa steg:

## Steg 1: Ange käll- och utdatakataloger

Först måste du ange källkatalogen där Excel-filen som innehåller Power Query-formlerna som ska uppdateras finns, samt utdatakatalogen där du vill spara den ändrade filen. Så här gör du med Aspose.Cells:

```csharp
// källkatalog
string SourceDir = RunExamples.Get_SourceDirectory();

// Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
```

## Steg 2: Ladda källarbetsboken för Excel

Därefter måste du läsa in källarbetsboken i Excel som du vill uppdatera Power Query-formelobjektet på. Så här gör du:

```csharp
// Ladda källarbetsboken för Excel
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Steg 3: Bläddra och uppdatera Power Query-formelobjekt

När du har läst in arbetsboken kan du navigera till Power Query-formelsamlingen och bläddra igenom varje formel och dess element. I det här exemplet letar vi efter formelobjektet med namnet "Källa" och uppdaterar dess värde. Här är exempelkod för att uppdatera ett Power Query-formelobjekt:

```csharp
// Få tillgång till Power Query-formelsamlingen
DataMashup mashupData = workbook.DataMashup;

// Gå igenom Power Query-formler och deras element
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

## Steg 4: Spara Excel-arbetsboken

När du har uppdaterat Power Query-formelobjektet kan du spara den modifierade Excel-arbetsboken i den angivna utdatakatalogen. Så här gör du:

```csharp
// Spara Excel-arbetsboken
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Exempel på källkod för Update Power Query Formula Item med Aspose.Cells för .NET 
```csharp
// Arbetskataloger
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
// Spara utdataarbetsboken.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Slutsats

Att uppdatera Power Query-formelelement är en viktig operation när du använder Aspose.Cells för att manipulera och bearbeta data i Excel-filer. Genom att följa stegen ovan kan du enkelt uppdatera formelelement

### Vanliga frågor

#### F: Vad är Power Query i Excel?
     
S: Power Query är en funktion i Excel som hjälper till att samla in, transformera och ladda data från olika källor. Det erbjuder kraftfulla verktyg för att rensa, kombinera och omforma data innan du importerar dem till Excel.

#### F: Hur vet jag om ett Power Query-formelobjekt har uppdaterats?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### F: Kan jag uppdatera flera Power Query-formelobjekt samtidigt?
    
S: Ja, du kan gå igenom Power Query-formelobjektsamlingen och uppdatera flera objekt i en enda loop, beroende på dina specifika behov.

#### F: Finns det andra operationer jag kan utföra på Power Query-formler med Aspose.Cells?
    
S: Ja, Aspose.Cells erbjuder ett komplett utbud av funktioner för att arbeta med Power Query-formler, inklusive att skapa, ta bort, kopiera och söka efter formler i en Excel-arbetsbok.