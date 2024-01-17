---
title: Povolit úvodní apostrof
linktitle: Povolit úvodní apostrof
second_title: Aspose.Cells for .NET API Reference
description: Povolte úvodní apostrof v sešitech aplikace Excel pomocí Aspose.Cells pro .NET.
type: docs
weight: 60
url: /cs/net/excel-workbook/allow-leading-apostrophe/
---
tomto podrobném tutoriálu vysvětlíme poskytnutý zdrojový kód C#, který vám umožní povolit použití úvodního apostrofu v sešitu aplikace Excel pomocí Aspose.Cells for .NET. Tuto operaci proveďte podle následujících kroků.

## Krok 1: Nastavte zdrojový a výstupní adresář

```csharp
// zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();
// Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
```

V tomto prvním kroku definujeme zdrojový a výstupní adresář pro soubory Excel.

## Krok 2: Vytvořte instanci objektu WorkbookDesigner

```csharp
// Vytvořte instanci objektu WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 Vytvoříme instanci`WorkbookDesigner` třídy od Aspose.Cells.

## Krok 3: Načtěte sešit aplikace Excel

```csharp
// Načtěte sešit aplikace Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Načteme sešit Excel ze zadaného souboru a zakážeme automatický převod počátečních apostrofů na styl textu.

## Krok 4: Nastavte zdroj dat

```csharp
// Definujte zdroj dat pro sešit návrháře
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

 Definujeme seznam datových objektů a použijeme`SetDataSource` způsob nastavení zdroje dat pro sešit návrháře.

## Krok 5: Zpracujte chytré značky

```csharp
// Zpracujte chytré značky
designer. Process();
```

 Používáme`Process` způsob zpracování inteligentních značek v sešitu návrháře.

## Krok 6: Uložte upravený sešit aplikace Excel

```csharp
// Uložte upravený sešit aplikace Excel
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Upravený excelový sešit s provedenými změnami uložíme.

### Ukázkový zdrojový kód pro Allow Leading Apostrophe pomocí Aspose.Cells pro .NET 
```csharp
//Zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Vytvoření instance objektu WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Otevřete návrhářskou tabulku obsahující inteligentní značky
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
// Nastavte zdroj dat pro tabulku návrháře
designer.SetDataSource("sampleData", list);
// Zpracujte chytré značky
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Závěr

gratuluji! Naučili jste se, jak povolit použití úvodního apostrofu v sešitu aplikace Excel pomocí Aspose.Cells for .NET. Experimentujte s vlastními daty a dále přizpůsobte své excelové sešity.

### Nejčastější dotazy

#### Otázka: Co je oprávnění pro úvodní apostrof v sešitu aplikace Excel?

Odpověď: Povolení počátečního apostrofu v sešitu aplikace Excel umožňuje správné zobrazení dat, která začínají apostrofem, aniž by bylo nutné je převést na styl textu. To je užitečné, když chcete zachovat apostrof jako součást dat.

#### Otázka: Proč musím vypnout automatický převod počátečních apostrofů?

Odpověď: Vypnutím automatického převodu úvodních uvozovek můžete zachovat jejich použití tak, jak je ve vašich datech. Vyhnete se tak jakékoli nechtěné úpravě dat při otevírání nebo manipulaci s excelovým sešitem.

#### Otázka: Jak nastavit zdroj dat v sešitu návrháře?

 Odpověď: Chcete-li nastavit zdroj dat v sešitu návrháře, můžete použít`SetDataSource` metoda určující název zdroje dat a seznam odpovídajících datových objektů.

#### Otázka: Má povolení úvodního apostrofu vliv na jiná data v sešitu aplikace Excel?

Odpověď: Ne, povolení úvodního apostrofu ovlivní pouze data začínající apostrofem. Ostatní data v excelovém sešitu zůstávají nezměněna.

#### Otázka: Mohu tuto funkci použít s jinými formáty souborů aplikace Excel?

Odpověď: Ano, tuto funkci můžete použít s jinými formáty souborů Excel podporovanými Aspose.Cells, jako jsou .xls, .xlsm atd.