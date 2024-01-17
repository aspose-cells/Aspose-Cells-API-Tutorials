---
title: Náhled tisku sešitu
linktitle: Náhled tisku sešitu
second_title: Aspose.Cells for .NET API Reference
description: Naučte se vygenerovat náhled tisku sešitu pomocí Aspose.Cells for .NET.
type: docs
weight: 170
url: /cs/net/excel-workbook/workbook-print-preview/
---
Náhled sešitu před tiskem je základní funkcí při práci se soubory aplikace Excel pomocí Aspose.Cells for .NET. Náhled tisku můžete snadno vygenerovat pomocí následujících kroků:

## Krok 1: Zadejte zdrojový adresář

Nejprve musíte určit zdrojový adresář, kde se nachází soubor Excel, který chcete zobrazit. Jak na to:

```csharp
// zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Krok 2: Načtěte sešit

Poté je třeba načíst sešit Sešit ze zadaného souboru aplikace Excel. Jak na to:

```csharp
// Načtěte sešit sešit
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Krok 3: Nakonfigurujte možnosti obrázku a tisku

Před vygenerováním náhledu tisku můžete podle potřeby nakonfigurovat možnosti obrázku a tisku. V tomto příkladu používáme výchozí možnosti. Jak na to:

```csharp
// Možnosti obrázku a tisku
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Krok 4: Vygenerujte náhled tisku sešitu

Nyní můžete vygenerovat náhled tisku sešitu Workbook pomocí třídy WorkbookPrintingPreview. Jak na to:

```csharp
// Náhled sešitu před tiskem
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Krok 5: Vygenerujte náhled tisku listu

Pokud chcete vygenerovat náhled tisku konkrétního listu, můžete použít třídu SheetPrintingPreview. Zde je příklad:

```csharp
// Náhled pracovního listu pro tisk
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Ukázkový zdrojový kód pro náhled tisku sešitu pomocí Aspose.Cells pro .NET 
```csharp
//Zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Závěr

Generování náhledu tisku sešitu je výkonná funkce nabízená Aspose.Cells pro .NET. Podle výše uvedených kroků můžete snadno zobrazit náhled sešitu aplikace Excel a získat informace o počtu stránek k tisku.

### Nejčastější dotazy

#### Otázka: Jak mohu určit jiný zdrojový adresář pro načtení mého sešitu?
    
 A: Můžete použít`Set_SourceDirectory` metoda k určení jiného zdrojového adresáře. Například:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### Otázka: Mohu přizpůsobit možnosti obrázku a tisku při generování náhledu tisku?
    
 Odpověď: Ano, můžete upravit možnosti obrázku a tisku změnou vlastností`ImageOrPrintOptions` objekt. Můžete například nastavit rozlišení obrázku, výstupní formát souboru atd.

#### Otázka: Je možné vygenerovat náhled tisku pro více listů v sešitu?
    
Odpověď: Ano, můžete iterovat přes různé listy v sešitu a vytvořit náhled tisku pro každý list pomocí`SheetPrintingPreview` třída.

#### Otázka: Jak uložím náhled tisku jako obrázek nebo soubor PDF?
    
 A: Můžete použít`ToImage` nebo`ToPdf` metoda`WorkbookPrintingPreview` nebo`SheetPrintingPreview` objekt uložit náhled tisku jako obrázek nebo soubor PDF.

#### Otázka: Co mohu dělat s vygenerovaným náhledem tisku?
    
Odpověď: Jakmile vygenerujete náhled tisku, můžete jej zobrazit na obrazovce, uložit jako obrázek nebo soubor PDF nebo jej použít pro jiné operace, jako je odesílání e-mailem nebo tisk.
	