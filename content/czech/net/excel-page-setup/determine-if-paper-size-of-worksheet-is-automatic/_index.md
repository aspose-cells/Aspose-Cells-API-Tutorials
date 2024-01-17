---
title: Zjistěte, zda je velikost papíru listu automaticky
linktitle: Zjistěte, zda je velikost papíru listu automaticky
second_title: Aspose.Cells for .NET API Reference
description: Naučte se, jak určit, zda je velikost papíru tabulky automatická s Aspose.Cells for .NET.
type: docs
weight: 20
url: /cs/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
tomto článku vás krok za krokem provedeme vysvětlením následujícího zdrojového kódu C#: Pomocí Aspose.Cells for .NET zjistěte, zda je velikost papíru v listu automatická. K provedení této operace použijeme knihovnu Aspose.Cells pro .NET. Chcete-li určit, zda je velikost papíru listu automatická, postupujte podle následujících kroků.

## Krok 1: Načtení sešitů
Prvním krokem je načtení sešitů. Budeme mít dva sešity: jeden s vypnutou automatickou velikostí papíru a druhý s povolenou automatickou velikostí papíru. Zde je kód pro načtení sešitů:

```csharp
// zdrojový adresář
string sourceDir = "YOUR_SOURCE_DIR";
// Výstupní adresář
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Vložte první sešit s vypnutou automatickou velikostí papíru
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Vložte druhý sešit s povolenou automatickou velikostí papíru
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Krok 2: Přístup k tabulkám
Nyní, když jsme načetli sešity, potřebujeme získat přístup k sešitům, abychom mohli zkontrolovat automatickou velikost papíru. Přejdeme k prvnímu pracovnímu listu ze dvou sešitů. Zde je kód pro přístup:

```csharp
//Přejděte na první list prvního sešitu
Worksheet ws11 = wb1.Worksheets[0];

// Přejděte na první list druhého sešitu
Worksheet ws12 = wb2.Worksheets[0];
```

## Krok 3: Zkontrolujte automatickou velikost papíru
 V tomto kroku zkontrolujeme, zda je velikost papíru listu automatická. Budeme používat`PageSetup.IsAutomaticPaperSize` nemovitost, abyste tyto informace získali. Následně zobrazíme výsledek. Zde je kód pro to:

```csharp
// Zobrazte vlastnost IsAutomaticPaperSize prvního listu v prvním sešitu
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Zobrazte vlastnost IsAutomaticPaperSize prvního listu v druhém sešitu
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Ukázkový zdrojový kód pro Zjistěte, zda velikost papíru je automatická pomocí Aspose.Cells pro .NET 
```csharp
//Zdrojový adresář
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Výstupní adresář
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Vložte první sešit s automatickou falešnou velikostí papíru
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Vložte druhý sešit s automatickou velikostí papíru true
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Přístup k prvnímu listu obou sešitů
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Vytiskněte vlastnost PageSetup.IsAutomaticPaperSize obou listů
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Závěr
tomto článku jsme se naučili, jak určit, zda je velikost papíru listu automaticky pomocí Aspose.Cells for .NET. Provedli jsme následující kroky: načtení sešitů,

přístup k tabulkám a automatická kontrola velikosti papíru. Nyní můžete tyto znalosti použít k určení, zda je velikost papíru vašich tabulek automatická.

### Nejčastější dotazy

#### Otázka: Jak mohu načíst sešity pomocí Aspose.Cells pro .NET?

Odpověď: Sešity můžete načíst pomocí třídy Workbook z knihovny Aspose.Cells. K načtení sešitu ze souboru použijte metodu Workbook.Load.

#### Otázka: Mohu zkontrolovat automatickou velikost papíru pro jiné tabulky?

Odpověď: Ano, automatickou velikost papíru pro jakýkoli list můžete zkontrolovat přístupem k vlastnosti PageSetup.IsAutomaticPaperSize odpovídajícího objektu Worksheet.

#### Otázka: Jak mohu změnit automatickou velikost papíru tabulky?

Odpověď: Chcete-li změnit automatickou velikost papíru listu, můžete použít vlastnost PageSetup.IsAutomaticPaperSize a nastavit ji na požadovanou hodnotu (true nebo false).

#### Otázka: Jaké další funkce nabízí Aspose.Cells for .NET?

Odpověď: Aspose.Cells for .NET nabízí mnoho funkcí pro práci s tabulkami, jako je vytváření, úprava a převod sešitů, stejně jako manipulace s daty, vzorci a formátování.