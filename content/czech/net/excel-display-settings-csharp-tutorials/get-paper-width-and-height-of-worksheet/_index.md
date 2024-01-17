---
title: Získejte šířku a výšku papíru listu
linktitle: Získejte šířku a výšku papíru listu
second_title: Aspose.Cells for .NET API Reference
description: Vytvořte průvodce krok za krokem, který vysvětlí následující zdrojový kód C#, abyste získali šířku a výšku papíru tabulky pomocí Aspose.Cells for .NET.
type: docs
weight: 80
url: /cs/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
tomto tutoriálu vás krok za krokem provedeme vysvětlením následujícího zdrojového kódu C#, abyste získali šířku a výšku papíru listu pomocí Aspose.Cells for .NET. Postupujte podle následujících kroků:

## Krok 1: Vytvořte sešit
 Začněte vytvořením nového sešitu pomocí`Workbook` třída:

```csharp
Workbook wb = new Workbook();
```

## Krok 2: Otevřete první list
 Dále přejděte na první list v sešitu pomocí`Worksheet` třída:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Krok 3: Nastavte velikost papíru na A2 a zobrazte šířku a výšku papíru v palcích
 Použijte`PaperSize` vlastnictvím`PageSetup` objekt pro nastavení velikosti papíru na A2, pak použijte`PaperWidth` a`PaperHeight` vlastnosti, abyste získali šířku a výšku papíru. Zobrazte tyto hodnoty pomocí`Console.WriteLine` metoda:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Krok 4: Opakujte kroky pro další velikosti papíru
Opakujte předchozí kroky, změňte velikost papíru na A3, A4 a Letter a poté zobrazte hodnoty šířky a výšky papíru pro každou velikost:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Ukázka zdrojového kódu pro Get Paper Width And Height Of Worksheet pomocí Aspose.Cells for .NET 

```csharp
//Vytvořte sešit
Workbook wb = new Workbook();
//Přístup k prvnímu listu
Worksheet ws = wb.Worksheets[0];
//Nastavte velikost papíru na A2 a tiskněte šířku a výšku papíru v palcích
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Nastavte velikost papíru na A3 a tiskněte šířku a výšku papíru v palcích
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Nastavte velikost papíru na A4 a tiskněte šířku a výšku papíru v palcích
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Nastavte velikost papíru na Letter a tiskněte šířku a výšku papíru v palcích
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Závěr

Naučili jste se používat Aspose.Cells pro .NET k získání šířky a výšky papíru tabulky. Tato funkce může být užitečná pro konfiguraci a přesné rozvržení vašich dokumentů aplikace Excel.

### Často kladené otázky (FAQ)

#### Co je Aspose.Cells pro .NET?

Aspose.Cells for .NET je výkonná knihovna pro manipulaci a zpracování souborů aplikace Excel v aplikacích .NET. Nabízí mnoho funkcí pro vytváření, úpravu, konverzi a analýzu souborů aplikace Excel.

#### Jak mohu získat velikost papíru tabulky pomocí Aspose.Cells pro .NET?

 Můžete použít`PageSetup` třídy`Worksheet` objekt pro přístup k velikosti papíru. Použijte`PaperSize` vlastnost pro nastavení velikosti papíru a`PaperWidth` a`PaperHeight` vlastnosti, abyste získali šířku a výšku papíru.

#### Jaké velikosti papíru podporuje Aspose.Cells for .NET?

Aspose.Cells for .NET podporuje širokou škálu běžně používaných velikostí papíru, jako je A2, A3, A4 a Letter, stejně jako mnoho dalších vlastních velikostí.

#### Mohu přizpůsobit velikost papíru tabulky pomocí Aspose.Cells pro .NET?

 Ano, můžete nastavit vlastní velikost papíru zadáním přesných rozměrů šířky a výšky pomocí`PaperWidth` a`PaperHeight` vlastnosti`PageSetup` třída.