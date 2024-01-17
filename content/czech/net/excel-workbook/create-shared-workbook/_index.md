---
title: Vytvořit sdílený sešit
linktitle: Vytvořit sdílený sešit
second_title: Aspose.Cells for .NET API Reference
description: Vytvořte sdílený sešit aplikace Excel pomocí Aspose.Cells for .NET, abyste umožnili souběžnou spolupráci na datech.
type: docs
weight: 70
url: /cs/net/excel-workbook/create-shared-workbook/
---
tomto tutoriálu vás provedeme poskytnutým zdrojovým kódem C#, který vám umožní vytvořit sdílený sešit pomocí Aspose.Cells for .NET. Tuto operaci proveďte podle následujících kroků.

## Krok 1: Nastavte výstupní adresář

```csharp
// Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
```

V tomto prvním kroku definujeme výstupní adresář, kam bude sdílený sešit uložen.

## Krok 2: Vytvořte objekt sešitu

```csharp
// Vytvořte objekt sešit
Workbook wb = new Workbook();
```

Vytváříme nový objekt Workbook, který bude reprezentovat náš excelový sešit.

## Krok 3: Povolte sdílení sešitu

```csharp
// Sdílejte sešit
wb.Settings.Shared = true;
```

 Povolíme funkci sdílení sešitu nastavením`Shared` vlastnost objektu Workbook to`true`.

## Krok 4: Uložte sdílený sešit

```csharp
// Uložte sdílený sešit
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

Sdílený sešit uložíme zadáním cesty a názvu výstupního souboru.

### Ukázkový zdrojový kód pro Create Shared Workbook pomocí Aspose.Cells for .NET 
```csharp
//Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
//Vytvořit objekt sešit
Workbook wb = new Workbook();
//Sdílejte sešit
wb.Settings.Shared = true;
//Uložte sdílený sešit
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Závěr

gratuluji! Naučili jste se vytvořit sdílený sešit pomocí Aspose.Cells for .NET. Sdílený sešit může používat více uživatelů současně ke spolupráci na datech. Experimentujte se svými vlastními daty a dále prozkoumejte funkce Aspose.Cells, abyste mohli vytvářet výkonné a personalizované sešity aplikace Excel.

### Nejčastější dotazy

#### Otázka: Co je sdílený sešit?

Odpověď: Sdílený sešit je sešit aplikace Excel, který může současně používat více uživatelů ke spolupráci na datech. Každý uživatel může provádět změny v sešitu a ostatní uživatelé uvidí aktualizace v reálném čase.

#### Otázka: Jak povolit sdílení sešitu v Aspose.Cells pro .NET?

 A: Chcete-li povolit sdílení sešitu v Aspose.Cells pro .NET, musíte nastavit`Shared` vlastnost objektu Workbook to`true`. To umožní uživatelům pracovat na sešitu současně.

#### Otázka: Mohu omezit uživatelská oprávnění ve sdíleném sešitu?

Odpověď: Ano, můžete omezit uživatelská oprávnění ve sdíleném sešitu pomocí funkcí zabezpečení aplikace Excel. Pro každého uživatele můžete nastavit specifická oprávnění, například možnost upravovat, pouze číst atd.

#### Otázka: Jak mohu sdílet sešit s ostatními uživateli?

Odpověď: Jakmile vytvoříte sdílený sešit, můžete jej sdílet s ostatními uživateli zasláním souboru aplikace Excel. Ostatní uživatelé budou moci soubor otevřít a pracovat na něm současně.

#### Otázka: Jsou ve sdíleném sešitu podporovány všechny funkce Excelu?

Odpověď: Většina funkcí aplikace Excel je podporována ve sdíleném sešitu. Některé pokročilé funkce, jako jsou makra a doplňky, však mohou mít omezení nebo omezení při použití ve sdíleném sešitu.