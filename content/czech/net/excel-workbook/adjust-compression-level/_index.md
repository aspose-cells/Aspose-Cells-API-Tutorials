---
title: Upravte úroveň komprese
linktitle: Upravte úroveň komprese
second_title: Aspose.Cells for .NET API Reference
description: Zmenšete velikost svých excelových sešitů úpravou úrovně komprese pomocí Aspose.Cells for .NET.
type: docs
weight: 50
url: /cs/net/excel-workbook/adjust-compression-level/
---
V tomto tutoriálu krok za krokem vysvětlíme poskytnutý zdrojový kód C#, který vám umožní upravit úroveň komprese pomocí Aspose.Cells for .NET. Chcete-li upravit úroveň komprese v sešitu aplikace Excel, postupujte podle následujících kroků.

## Krok 1: Nastavte zdrojový a výstupní adresář

```csharp
// zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();
// Výstupní adresář
string outDir = RunExamples.Get_OutputDirectory();
```

V tomto prvním kroku definujeme zdrojový a výstupní adresář pro soubory Excel.

## Krok 2: Načtěte sešit aplikace Excel

```csharp
// Načtěte sešit aplikace Excel
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

Sešit Excel načteme ze zadaného souboru pomocí`Workbook` třídy od Aspose.Cells.

## Krok 3: Nastavte možnosti zálohování

```csharp
// Definujte možnosti zálohování
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Vytvoříme instanci`XlsbSaveOptions` třídy pro nastavení možností uložení.

## Krok 4: Upravte úroveň komprese (Úroveň 1)

```csharp
// Upravte úroveň komprese (Úroveň 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Úroveň komprese upravíme nastavením`CompressionType` na`Level1`. Poté sešit Excel uložíme se zadanou možností komprese.

## Krok 5: Upravte úroveň komprese (Úroveň 6)

```csharp
// Upravte úroveň komprese (úroveň 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Opakujeme proces, abychom upravili úroveň komprese`Level6` a uložte sešit Excel s touto možností.

## Krok 6: Upravte úroveň komprese (Úroveň 9)

```csharp
// Upravte úroveň komprese (Úroveň 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Proces zopakujeme naposledy, abychom upravili úroveň komprese`Level9` a uložte sešit Excel s touto možností.

### Ukázkový zdrojový kód pro Upravit úroveň komprese pomocí Aspose.Cells pro .NET 
```csharp
//Zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Závěr

gratuluji! Naučili jste se, jak upravit úroveň komprese v sešitu aplikace Excel pomocí Aspose.Cells for .NET. Experimentujte s různými úrovněmi komprese, abyste našli tu, která nejlépe vyhovuje vašim potřebám.

### Nejčastější dotazy

#### Otázka: Co je komprese v sešitu aplikace Excel?

Odpověď: Komprese v sešitu aplikace Excel je proces zmenšení velikosti souboru pomocí kompresních algoritmů. To snižuje požadovaný úložný prostor a zlepšuje výkon při načítání a manipulaci se souborem.

#### Otázka: Jaké úrovně komprese jsou dostupné s Aspose.Cells?

Odpověď: Pomocí Aspose.Cells můžete upravit úroveň komprese od 1 do 9. Čím vyšší úroveň komprese, tím menší bude velikost souboru, ale může to také prodloužit dobu zpracování.

#### Otázka: Jak mohu vybrat správnou úroveň komprese pro sešit aplikace Excel?

Odpověď: Volba úrovně komprese závisí na vašich konkrétních potřebách. Pokud chcete maximální kompresi a doba zpracování není problém, můžete přejít na úroveň 9. Pokud dáváte přednost kompromisu mezi velikostí souboru a dobou zpracování, můžete zvolit střední úroveň.

#### Otázka: Ovlivňuje komprese kvalitu dat v sešitu aplikace Excel?

Odpověď: Ne, komprese neovlivňuje kvalitu dat v sešitu aplikace Excel. Jednoduše zmenší velikost souboru pomocí kompresních technik, aniž by se změnila samotná data.

#### Otázka: Mohu upravit úroveň komprese po uložení souboru Excel?

Odpověď: Ne, jakmile uložíte soubor Excel se specifickou úrovní komprese, nelze úroveň komprese později upravit. Budete-li jej chtít upravit, budete muset soubor znovu uložit s novou úrovní komprese.