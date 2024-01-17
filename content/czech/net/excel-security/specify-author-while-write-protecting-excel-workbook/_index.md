---
title: Určete autora při ochraně sešitu aplikace Excel proti zápisu
linktitle: Určete autora při ochraně sešitu aplikace Excel proti zápisu
second_title: Aspose.Cells for .NET API Reference
description: Naučte se, jak chránit a přizpůsobovat sešity aplikace Excel pomocí Aspose.Cells for .NET. Výukový program krok za krokem v C#.
type: docs
weight: 30
url: /cs/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

V tomto tutoriálu vám ukážeme, jak určit autora při ochraně sešitu Excelu proti zápisu pomocí knihovny Aspose.Cells pro .NET.

## Krok 1: Příprava prostředí

Než začnete, ujistěte se, že máte na svém počítači nainstalovaný Aspose.Cells for .NET. Stáhněte si knihovnu z oficiálních stránek Aspose a postupujte podle dodaných pokynů k instalaci.

## Krok 2: Konfigurace zdrojových a výstupních adresářů

 poskytnutém zdrojovém kódu musíte zadat zdrojový a výstupní adresář. Upravte`sourceDir` a`outputDir` proměnných nahrazením "VÁŠ ZDROJOVÝ ADRESÁŘ" a "VÁŠ VÝSTUPNÍ ADRESÁŘ" příslušnými absolutními cestami na vašem počítači.

```csharp
// Zdrojový adresář
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Výstupní adresář
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Krok 3: Vytvoření prázdného sešitu aplikace Excel

Nejprve vytvoříme objekt Workbook, který představuje prázdný sešit aplikace Excel.

```csharp
// Vytvořte prázdný sešit.
Workbook wb = new Workbook();
```

## Krok 4: Ochrana proti zápisu heslem

 Dále určíme heslo pro ochranu sešitu Excelu proti zápisu pomocí`WriteProtection.Password` vlastnost objektu Sešit.

```csharp
// Zápis chránit sešit s heslem.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Krok 5: Specifikace autora

 Nyní určíme autora excelového sešitu pomocí`WriteProtection.Author` vlastnost objektu Sešit.

```csharp
// Určete autora při ochraně sešitu proti zápisu.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Krok 6: Zálohujte chráněný sešit Excel

 Jakmile je určena ochrana proti zápisu a autor, můžeme sešit Excel uložit ve formátu XLSX pomocí`Save()` metoda.

```csharp
// Uložte sešit ve formátu XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Ukázkový zdrojový kód pro sešit aplikace Excel pro specifikaci autora při ochraně proti zápisu pomocí Aspose.Cells pro .NET 
```csharp
//Zdrojový adresář
string sourceDir = "YOUR SOURCE DIRECTORY";

//Výstupní adresář
string outputDir = "YOUR OUTPUT DIRECTORY";

// Vytvořte prázdný sešit.
Workbook wb = new Workbook();

// Zápis chránit sešit s heslem.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Určete autora při ochraně sešitu proti zápisu.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Uložte sešit ve formátu XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Závěr

gratuluji! Nyní jste se naučili, jak určit autora při ochraně sešitu Excelu proti zápisu pomocí Aspose.Cells for .NET. Tyto kroky můžete použít na své vlastní projekty, abyste ochránili a přizpůsobili své sešity Excel.

Neváhejte dále prozkoumat funkce Aspose.Cells for .NET pro pokročilejší operace se soubory Excel.

## Nejčastější dotazy

#### Otázka: Mohu chránit sešit aplikace Excel proti zápisu bez zadání hesla?

 Odpověď: Ano, můžete použít objekt Workbook`WriteProtect()` bez zadání hesla pro ochranu sešitu aplikace Excel proti zápisu. Tím omezíte změny v sešitu bez nutnosti zadání hesla.

#### Otázka: Jak odeberu ochranu proti zápisu ze sešitu aplikace Excel?

 A: Chcete-li odstranit ochranu proti zápisu ze sešitu aplikace Excel, můžete použít`Unprotect()` metoda objektu Worksheet nebo`RemoveWriteProtection()` metoda objektu Workbook, v závislosti na vašem konkrétním případu použití. .

#### Otázka: Zapomněl jsem heslo k ochraně svého excelového sešitu. Co můžu dělat ?

Odpověď: Pokud jste zapomněli heslo k ochraně sešitu aplikace Excel, nemůžete jej přímo odstranit. Můžete však zkusit použít specializované nástroje třetích stran, které poskytují funkce obnovení hesla pro chráněné soubory Excel.

#### Otázka: Je možné určit více autorů při ochraně sešitu Excelu proti zápisu?

Odpověď: Ne, knihovna Aspose.Cells for .NET umožňuje zadat jednoho autora při ochraně sešitu aplikace Excel proti zápisu. Pokud chcete zadat více autorů, budete muset zvážit vlastní řešení přímou manipulací se souborem Excel.