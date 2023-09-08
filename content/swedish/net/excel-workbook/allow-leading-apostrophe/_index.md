---
title: Tillåt ledande apostrof
linktitle: Tillåt ledande apostrof
second_title: Aspose.Cells för .NET API-referens
description: Tillåt ledande apostrof i Excel-arbetsböcker med Aspose.Cells för .NET.
type: docs
weight: 60
url: /sv/net/excel-workbook/allow-leading-apostrophe/
---
denna steg-för-steg handledning kommer vi att förklara den medföljande C#-källkoden som gör att du kan tillåta användningen av en ledande apostrof i en Excel-arbetsbok med Aspose.Cells för .NET. Följ stegen nedan för att utföra denna operation.

## Steg 1: Ställ in käll- och utdatakataloger

```csharp
// källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();
// Utdatakatalog
string outputDir = RunExamples.Get_OutputDirectory();
```

I detta första steg definierar vi käll- och utdatakatalogerna för Excel-filerna.

## Steg 2: Instantiera ett WorkbookDesigner-objekt

```csharp
// Instantiera ett WorkbookDesigner-objekt
WorkbookDesigner designer = new WorkbookDesigner();
```

 Vi skapar en instans av`WorkbookDesigner` klass från Aspose.Cells.

## Steg 3: Ladda Excel-arbetsbok

```csharp
// Ladda Excel-arbetsboken
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Vi laddar Excel-arbetsboken från den angivna filen och inaktiverar den automatiska konverteringen av initiala apostrofer till textstil.

## Steg 4: Ställ in datakälla

```csharp
// Definiera datakällan för designerarbetsboken
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 Vi definierar en lista över dataobjekt och använder`SetDataSource` metod för att ställa in datakällan för designerarbetsboken.

## Steg 5: Bearbeta smarta markörer

```csharp
// Process smarta markörer
designer. Process();
```

 Vi använder`Process` metod för att bearbeta smarta markörer i designerarbetsboken.

## Steg 6: Spara den modifierade Excel-arbetsboken

```csharp
// Spara den ändrade Excel-arbetsboken
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Vi sparar den modifierade Excel-arbetsboken med de ändringar som gjorts.

### Exempel på källkod för Tillåt ledande apostrof med Aspose.Cells för .NET 
```csharp
//Källkatalog
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Instantiera ett WorkbookDesigner-objekt
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Öppna ett designerkalkylblad som innehåller smarta markörer
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Ställ in datakällan för designerkalkylarket
designer.SetDataSource("sampleData", list);
// Bearbeta de smarta markörerna
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Slutsats

Grattis! Du lärde dig hur du tillåter användning av en ledande apostrof i en Excel-arbetsbok med Aspose.Cells för .NET. Experimentera med dina egna data för att ytterligare anpassa dina Excel-arbetsböcker.

### Vanliga frågor

#### F: Vad är ledande apostrofbehörighet i en Excel-arbetsbok?

S: Genom att tillåta den initiala apostrof i en Excel-arbetsbok kan data som börjar med en apostrof visas korrekt utan att konvertera den till en textstil. Detta är användbart när du vill behålla apostrof som en del av data.

#### F: Varför måste jag stänga av automatisk konvertering av initiala apostrofer?

S: Genom att inaktivera den automatiska konverteringen av ledande citat kan du bevara deras användning som den är i dina data. Detta undviker alla oavsiktliga ändringar av data när du öppnar eller manipulerar Excel-arbetsboken.

#### F: Hur ställer man in datakälla i designerarbetsbok?

 S: För att ställa in datakällan i designerarbetsboken kan du använda`SetDataSource` metod som anger namnet på datakällan och en lista över motsvarande dataobjekt.

#### F: Påverkar det att tillåta ledande apostrof andra data i Excel-arbetsboken?

S: Nej, att tillåta den inledande apostrof påverkar bara data som börjar med en apostrof. Övriga data i Excel-arbetsboken förblir oförändrade.

#### F: Kan jag använda den här funktionen med andra Excel-filformat?

S: Ja, du kan använda den här funktionen med andra Excel-filformat som stöds av Aspose.Cells, som .xls, .xlsm, etc.