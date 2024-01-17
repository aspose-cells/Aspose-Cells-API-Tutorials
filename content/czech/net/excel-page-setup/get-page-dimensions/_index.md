---
title: Získejte rozměry stránky
linktitle: Získejte rozměry stránky
second_title: Aspose.Cells for .NET API Reference
description: Naučte se, jak načíst rozměry stránky v Excelu pomocí Aspose.Cells for .NET. Průvodce krok za krokem se zdrojovým kódem v C#.
type: docs
weight: 40
url: /cs/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET je výkonná knihovna, která umožňuje vývojářům pracovat se soubory Microsoft Excel programově. Nabízí širokou škálu funkcí pro manipulaci s dokumenty Excel, včetně možnosti získat rozměry stránky. V tomto tutoriálu vás provedeme kroky k načtení rozměrů stránky pomocí Aspose.Cells for .NET.

## Krok 1: Vytvořte instanci třídy Workbook

Pro začátek musíme vytvořit instanci třídy Workbook, která představuje sešit Excel. Toho lze dosáhnout pomocí následujícího kódu:

```csharp
Workbook book = new Workbook();
```

## Krok 2: Přístup k tabulce

Dále musíme přejít na list v sešitu, kde chceme nastavit rozměry stránky. V tomto příkladu předpokládejme, že chceme pracovat s prvním listem. Můžeme k němu přistupovat pomocí následujícího kódu:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Krok 3: Nastavte velikost papíru na A2 a šířku a výšku tisku v palcích

Nyní nastavíme velikost papíru na A2 a vytiskneme šířku a výšku stránky v palcích. Toho lze dosáhnout pomocí následujícího kódu:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Krok 4: Nastavte velikost papíru na A3 a šířku a výšku tisku v palcích

Dále nastavíme velikost papíru na A3 a vytiskneme šířku a výšku stránky v palcích. Zde je odpovídající kód:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Krok 5: Nastavte velikost papíru na A4 a šířku a výšku tisku v palcích

Nyní nastavíme velikost papíru na A4 a vytiskneme šířku a výšku stránky v palcích. Zde je kód:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Krok 6: Nastavte velikost papíru na Letter a vytiskněte šířku a výšku v palcích

Nakonec nastavíme velikost papíru na Letter a vytiskneme šířku a výšku stránky v palcích. Zde je kód:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Ukázkový zdrojový kód pro Get Page Dimensions pomocí Aspose.Cells pro .NET 
```csharp
// Vytvořte instanci třídy Workbook
Workbook book = new Workbook();
// Přístup k prvnímu listu
Worksheet sheet = book.Worksheets[0];
// Nastavte velikost papíru na A2 a tiskněte šířku a výšku papíru v palcích
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Nastavte velikost papíru na A3 a tiskněte šířku a výšku papíru v palcích
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Nastavte velikost papíru na A4 a tiskněte šířku a výšku papíru v palcích
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Nastavte velikost papíru na Letter a tiskněte šířku a výšku papíru v palcích
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Závěr

gratuluji! Naučili jste se, jak načíst rozměry stránky pomocí Aspose.Cells pro .NET. Tato funkce může být užitečná, když potřebujete provést specifické operace založené na rozměrech stránky v souborech aplikace Excel.

Nezapomeňte dále prozkoumat dokumentaci Aspose.Cells, abyste objevili všechny výkonné funkce, které nabízí.

### FAQ

#### 1. Jaké další velikosti papíru Aspose.Cells for .NET podporuje?

Aspose.Cells for .NET podporuje různé velikosti papíru včetně A1, A5, B4, B5, Executive, Legal, Letter a mnoha dalších. Úplný seznam podporovaných velikostí papíru naleznete v dokumentaci.

#### 2. Mohu nastavit vlastní rozměry stránky pomocí Aspose.Cells pro .NET?

Ano, můžete nastavit vlastní rozměry stránky zadáním požadované šířky a výšky. Aspose.Cells nabízí plnou flexibilitu přizpůsobení rozměrů stránky vašim potřebám.

#### 3. Mohu získat rozměry stránky v jiných jednotkách než v palcích?

Ano, Aspose.Cells for .NET umožňuje získat rozměry stránky v různých jednotkách, včetně palců, centimetrů, milimetrů a bodů.

#### 4. Podporuje Aspose.Cells for .NET další funkce úpravy nastavení stránky?

Ano, Aspose.Cells nabízí celou řadu funkcí pro úpravu nastavení stránky, včetně nastavení okrajů, orientace, záhlaví a zápatí atd.