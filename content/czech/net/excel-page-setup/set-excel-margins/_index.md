---
title: Nastavte okraje aplikace Excel
linktitle: Nastavte okraje aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Naučte se, jak nastavit okraje v Excelu pomocí Aspose.Cells for .NET. Výukový program krok za krokem v C#.
type: docs
weight: 110
url: /cs/net/excel-page-setup/set-excel-margins/
---
V tomto tutoriálu vás krok za krokem provedeme nastavením okrajů v Excelu pomocí Aspose.Cells for .NET. Pro ilustraci procesu použijeme zdrojový kód C#.

## Krok 1: Nastavení prostředí

Ujistěte se, že máte na svém počítači nainstalovaný Aspose.Cells for .NET. Vytvořte také nový projekt ve vámi preferovaném vývojovém prostředí.

## Krok 2: Importujte potřebné knihovny

Do souboru kódu importujte knihovny potřebné pro práci s Aspose.Cells. Zde je odpovídající kód:

```csharp
using Aspose.Cells;
```

## Krok 3: Nastavte Data Directory

Nastavte datový adresář, kam chcete uložit upravený soubor Excel. Použijte následující kód:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Nezapomeňte zadat úplnou cestu k adresáři.

## Krok 4: Vytvoření sešitu a listu

Vytvořte nový objekt Workbook a přejděte na první list v sešitu pomocí následujícího kódu:

```csharp
Workbook workbook = new Workbook();
WorksheetCollection worksheets = workbook. Worksheets;
Worksheet worksheet = worksheets[0];
```

Tím se vytvoří prázdný sešit s listem a poskytne přístup k tomuto listu.

## Krok 5: Nastavení okrajů

Otevřete objekt PageSetup listu a nastavte okraje pomocí vlastností BottomMargin, LeftMargin, RightMargin a TopMargin. Zde je ukázkový kód:

```csharp
PageSetup pageSetup = worksheet.PageSetup;
pageSetup.BottomMargin = 2;
pageSetup.LeftMargin = 1;
pageSetup.RightMargin = 1;
pageSetup.TopMargin = 3;
```

Tím se nastaví spodní, levý, pravý a horní okraj listu.

## Krok 6: Uložení upraveného sešitu

Uložte upravený sešit pomocí následujícího kódu:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Tím se upravený sešit uloží do zadaného datového adresáře.

### Ukázkový zdrojový kód pro Set Excel Margins pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvořte objekt sešitu
Workbook workbook = new Workbook();
// Získejte pracovní listy v sešitu
WorksheetCollection worksheets = workbook.Worksheets;
// Získejte první (výchozí) list
Worksheet worksheet = worksheets[0];
// Získejte objekt nastavení stránky
PageSetup pageSetup = worksheet.PageSetup;
// Nastavte spodní, levý, pravý a horní okraj stránky
pageSetup.BottomMargin = 2;
pageSetup.LeftMargin = 1;
pageSetup.RightMargin = 1;
pageSetup.TopMargin = 3;
// Uložte sešit.
workbook.Save(dataDir + "SetMargins_out.xls");
```

## Závěr

Nyní jste se naučili, jak nastavit okraje v aplikaci Excel pomocí Aspose.Cells pro .NET. Tento kurz vás provede každým krokem procesu, od nastavení prostředí až po uložení upraveného sešitu. Neváhejte dále prozkoumat funkce Aspose.Cells, abyste mohli provádět další manipulace se svými soubory Excel.

### FAQ (často kladené otázky)

#### 1. Jak mohu určit vlastní okraje pro svou tabulku?

 Vlastní okraje můžete určit pomocí`BottomMargin`, `LeftMargin`, `RightMargin` , a`TopMargin` vlastnosti`PageSetup` objekt. Jednoduše nastavte požadované hodnoty pro každou vlastnost a upravte okraje podle potřeby.

#### 2. Mohu nastavit různé okraje pro různé listy ve stejném sešitu?

 Ano, pro každý list ve stejném sešitu můžete nastavit různé okraje. Stačí přístup k`PageSetup` objekt každého listu jednotlivě a pro každý nastavte specifické okraje.

#### 3. Platí definované okraje i pro tisk sešitu?

Ano, okraje nastavené pomocí Aspose.Cells platí i při tisku sešitu. Zadané okraje budou zohledněny při generování tištěného výstupu sešitu.

#### 4. Mohu změnit okraje existujícího souboru Excel pomocí Aspose.Cells?

 Ano, můžete změnit okraje existujícího souboru Excel načtením souboru pomocí Aspose.Cells, přístupem k jednotlivým listům`PageSetup` objekt a změna hodnot vlastností okrajů. Potom uložte upravený soubor a použijte nové okraje.

#### 5. Jak odstraním okraje z tabulky?

 Chcete-li odstranit okraje z listu, můžete jednoduše nastavit hodnoty`BottomMargin`, `LeftMargin`, `RightMargin` a`TopMargin` vlastnosti na nulu. Tím se obnoví výchozí hodnoty okrajů (obvykle nula).