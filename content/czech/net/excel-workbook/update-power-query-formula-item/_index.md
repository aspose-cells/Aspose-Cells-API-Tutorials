---
title: Aktualizujte položku vzorce Power Query
linktitle: Aktualizujte položku vzorce Power Query
second_title: Aspose.Cells for .NET API Reference
description: Přečtěte si, jak aktualizovat prvky vzorců Power Query v souborech Excel pomocí Aspose.Cells for .NET.
type: docs
weight: 160
url: /cs/net/excel-workbook/update-power-query-formula-item/
---
Aktualizace položky vzorce Power Query je běžnou operací při práci s daty v souborech aplikace Excel. Pomocí Aspose.Cells for .NET můžete snadno aktualizovat položku vzorce Power Query podle následujících kroků:

## Krok 1: Zadejte zdrojový a výstupní adresář

Nejprve musíte určit zdrojový adresář, kde se nachází soubor Excel obsahující vzorce Power Query k aktualizaci, a také výstupní adresář, kam chcete upravený soubor uložit. Zde je návod, jak to udělat pomocí Aspose.Cells:

```csharp
// zdrojový adresář
string SourceDir = RunExamples.Get_SourceDirectory();

// Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
```

## Krok 2: Načtěte zdrojový sešit aplikace Excel

Dále je třeba načíst zdrojový excelový sešit, ve kterém chcete aktualizovat položku vzorce Power Query. Jak na to:

```csharp
// Načtěte zdrojový excelový sešit
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Krok 3: Procházejte a aktualizujte položky vzorce Power Query

Po načtení sešitu můžete přejít do kolekce vzorců Power Query a procházet každý vzorec a jeho prvky. V tomto příkladu hledáme položku vzorce s názvem "Zdroj" a aktualizujeme její hodnotu. Zde je ukázkový kód pro aktualizaci položky vzorce Power Query:

```csharp
// Přístup ke kolekci vzorců Power Query
DataMashup mashupData = workbook.DataMashup;

// Procházejte vzorce Power Query a jejich prvky
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

## Krok 4: Uložte výstupní excelový sešit

Jakmile aktualizujete položku vzorce Power Query, můžete upravený sešit Excel uložit do určeného výstupního adresáře. Jak na to:

```csharp
// Uložte výstupní excelový sešit
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Ukázka zdrojového kódu pro položku Update Power Query Formula Item pomocí Aspose.Cells for .NET 
```csharp
// Pracovní adresáře
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
// Uložte výstupní sešit.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Závěr

Aktualizace prvků vzorce Power Query je nezbytnou operací při použití Aspose.Cells k manipulaci a zpracování dat v souborech aplikace Excel. Podle výše uvedených kroků můžete snadno aktualizovat prvky vzorce

### Nejčastější dotazy

#### Otázka: Co je Power Query v Excelu?
     
Odpověď: Power Query je funkce v Excelu, která pomáhá shromažďovat, transformovat a načítat data z různých zdrojů. Nabízí výkonné nástroje pro čištění, kombinování a přetváření dat před jejich importem do Excelu.

#### Otázka: Jak zjistím, zda byla položka vzorce Power Query úspěšně aktualizována?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### Otázka: Mohu aktualizovat více položek vzorce Power Query najednou?
    
Odpověď: Ano, můžete procházet kolekci položek vzorců Power Query a aktualizovat více položek v jedné smyčce v závislosti na vašich konkrétních potřebách.

#### Otázka: Existují další operace, které mohu provádět se vzorci Power Query pomocí Aspose.Cells?
    
Odpověď: Ano, Aspose.Cells nabízí celou řadu funkcí pro práci se vzorci Power Query, včetně vytváření, mazání, kopírování a vyhledávání vzorců v excelovém sešitu.