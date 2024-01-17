---
title: Odebrat existující nastavení tiskárny z listů
linktitle: Odebrat existující nastavení tiskárny z listů
second_title: Aspose.Cells for .NET API Reference
description: Zjistěte, jak odstranit stávající nastavení tiskárny z tabulek aplikace Excel pomocí Aspose.Cells for .NET.
type: docs
weight: 80
url: /cs/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
V tomto tutoriálu vás krok za krokem provedeme, jak odstranit stávající nastavení tiskárny z listů v Excelu pomocí Aspose.Cells for .NET. Pro ilustraci procesu použijeme zdrojový kód C#.

## Krok 1: Nastavení prostředí

Ujistěte se, že máte na svém počítači nainstalovaný Aspose.Cells for .NET. Vytvořte také nový projekt ve vámi preferovaném vývojovém prostředí.

## Krok 2: Importujte potřebné knihovny

Do souboru kódu importujte knihovny potřebné pro práci s Aspose.Cells. Zde je odpovídající kód:

```csharp
using Aspose.Cells;
```

## Krok 3: Nastavte zdrojový a výstupní adresář

Nastavte zdrojový a výstupní adresář, kde se nachází původní soubor Excel a kam chcete uložit upravený soubor. Použijte následující kód:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Nezapomeňte zadat úplné cesty k adresáři.

## Krok 4: Načtení zdrojového souboru Excel

Načtěte zdrojový soubor Excel pomocí následujícího kódu:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Tím se zadaný soubor Excel načte do objektu Sešit.

## Krok 5: Procházejte listy

Procházejte všechny listy v sešitu pomocí smyčky. Použijte následující kód:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // Zbytek kódu bude přidán v dalším kroku.
}
```

## Krok 6: Odstraňte existující nastavení tiskárny

Zkontrolujte, zda pro každý list existují nastavení tiskárny a v případě potřeby je odstraňte. Použijte následující kód:

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

## Krok 7: Uložení upraveného sešitu

Uložte upravený sešit pomocí následujícího kódu:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Tím se upravený sešit uloží do zadaného výstupního adresáře.

### Ukázkový zdrojový kód pro odstranění existujících nastavení tiskárny z pracovních listů pomocí Aspose.Cells pro .NET 
```csharp
//Zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();
//Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
//Načtěte zdrojový soubor Excel
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Získejte počty listů sešitu
int sheetCount = wb.Worksheets.Count;
//Opakujte všechny listy
for (int i = 0; i < sheetCount; i++)
{
    //Otevřete i-tý pracovní list
    Worksheet ws = wb.Worksheets[i];
    //Přístup k nastavení stránky listu
    PageSetup ps = ws.PageSetup;
    //Zkontrolujte, zda existují nastavení tiskárny pro tento list
    if (ps.PrinterSettings != null)
    {
        //Vytiskněte následující zprávu
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Název tiskového listu a jeho velikost papíru
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Odeberte nastavení tiskárny jejich nastavením na hodnotu null
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//-li
}//pro
//Uložte sešit
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Závěr

Nyní jste se naučili, jak odstranit stávající nastavení tiskárny z listů v Excelu pomocí Aspose.Cells for .NET. Tento výukový program vás provede každým krokem procesu, od nastavení prostředí až po procházení tabulkami a vymazání nastavení tiskárny. Nyní můžete tyto znalosti využít ke správě nastavení tiskárny v souborech aplikace Excel.

### FAQ

#### Q1: Jak zjistím, zda tabulka má existující nastavení tiskárny?

 A1: Chcete-li zkontrolovat, zda existují nastavení tiskárny pro list, přejděte na stránku`PrinterSettings` vlastnictvím`PageSetup` objekt. Pokud hodnota není null, znamená to, že existují existující nastavení tiskárny.

#### Q2: Mohu odstranit nastavení tiskárny pouze pro konkrétní tabulku?

 Odpověď 2: Ano, stejný přístup můžete použít k odebrání nastavení tiskárny pro konkrétní list přístupem k tomuto listu`PageSetup` objekt.

#### Q3: Odebere tato metoda také další nastavení rozvržení?

Odpověď 3: Ne, tato metoda odstraní pouze nastavení tiskárny. Ostatní nastavení rozvržení, jako jsou okraje, orientace papíru atd., zůstávají beze změny.

#### Q4: Funguje tato metoda pro všechny formáty souborů aplikace Excel, například .xls a .xlsx?

Odpověď 4: Ano, tato metoda funguje pro všechny formáty souborů aplikace Excel podporované Aspose.Cells, včetně .xls a .xlsx.

#### Q5: Jsou změny provedené v nastavení tiskárny v upraveném souboru Excel trvalé?

Odpověď 5: Ano, změny nastavení tiskárny jsou trvale uloženy v upraveném souboru aplikace Excel.