---
title: Implementujte vlastní velikost papíru listu pro vykreslování
linktitle: Implementujte vlastní velikost papíru listu pro vykreslování
second_title: Aspose.Cells for .NET API Reference
description: Podrobný průvodce implementací vlastní velikosti listu s Aspose.Cells pro .NET. Nastavte rozměry, přidejte zprávu a uložte jako PDF.
type: docs
weight: 50
url: /cs/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
Implementace vlastní velikosti listu může být velmi užitečná, když chcete vytvořit dokument PDF s určitou velikostí. V tomto tutoriálu se naučíme, jak pomocí Aspose.Cells for .NET nastavit vlastní velikost listu a poté dokument uložit jako PDF.

## Krok 1: Vytvoření výstupní složky

Než začnete, musíte vytvořit výstupní složku, kam se uloží vygenerovaný soubor PDF. Pro výstupní složku můžete použít jakoukoli cestu, kterou chcete.

```csharp
// Výstupní adresáře
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Ujistěte se, že jste zadali správnou cestu k vaší výstupní složce.

## Krok 2: Vytvoření objektu Sešit

Chcete-li začít, musíte vytvořit objekt Workbook pomocí Aspose.Cells. Tento objekt představuje vaši tabulku.

```csharp
// Vytvořte objekt sešit
Workbook wb = new Workbook();
```

## Krok 3: Přístup k prvnímu listu

Po vytvoření objektu Workbook můžete přistupovat k prvnímu listu v něm.

```csharp
// Přístup k prvnímu pracovnímu listu
Worksheet ws = wb.Worksheets[0];
```

## Krok 4: Nastavení vlastní velikosti listu

 Nyní můžete nastavit vlastní velikost listu pomocí`CustomPaperSize(width, height)` metoda třídy PageSetup.

```csharp
// Nastavit vlastní velikost listu (v palcích)
ws.PageSetup.CustomPaperSize(6, 4);
```

V tomto příkladu jsme nastavili velikost listu na šířku 6 palců a 4 palce na výšku.

## Krok 5: Přístup k buňce B4

Poté můžeme přistupovat ke konkrétní buňce v listu. V tomto případě přistoupíme k buňce B4.

```csharp
// Přístup do buňky B4
Cell b4 = ws.Cells["B4"];
```

## Krok 6: Přidání zprávy do buňky B4

 Nyní můžeme přidat zprávu do buňky B4 pomocí`PutValue(value)` metoda.

```csharp
// Přidejte zprávu do buňky B4
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

V tomto příkladu jsme do buňky B4 přidali zprávu „Velikost stránky PDF: 6,00“ x 4,00.

## Krok 7: Uložení listu ve formátu PDF

 Nakonec můžeme pracovní list uložit ve formátu PDF pomocí`Save(filePath)` metoda objektu Workbook.

```csharp
// Uložte pracovní list ve formátu PDF
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Zadejte požadovanou cestu k vygenerovanému souboru PDF pomocí výstupní složky vytvořené dříve.

### Ukázkový zdrojový kód pro implementaci vlastní velikosti papíru listu pro vykreslování pomocí Aspose.Cells for .NET 
```csharp
//Výstupní adresář
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Vytvořit objekt sešitu
Workbook wb = new Workbook();
//Přístup k prvnímu listu
Worksheet ws = wb.Worksheets[0];
//Nastavte vlastní velikost papíru v jednotkách palců
ws.PageSetup.CustomPaperSize(6, 4);
//Přístup k buňce B4
Cell b4 = ws.Cells["B4"];
//Přidejte zprávu do buňky B4
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Uložte sešit ve formátu pdf
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## Závěry

V tomto tutoriálu jste se naučili implementovat vlastní velikost listu pomocí Aspose.Cells for .NET. Tyto kroky můžete použít k nastavení konkrétních rozměrů pro vaše listy a poté uložit dokumenty ve formátu PDF. Doufáme, že vám tato příručka pomohla při pochopení procesu implementace vlastní velikosti tabulky.

### Často kladené otázky (FAQ)

#### Otázka 1: Mohu dále upravit rozvržení tabulky?

Ano, Aspose.Cells nabízí mnoho možností, jak přizpůsobit rozvržení listu. Můžete nastavit vlastní rozměry, orientaci stránky, okraje, záhlaví a zápatí a mnoho dalšího.

#### Otázka 2: Jaké další výstupní formáty Aspose.Cells podporuje?

Aspose.Cells podporuje mnoho různých výstupních formátů, včetně PDF, XLSX, XLS, CSV, HTML, TXT a mnoha dalších. Můžete si vybrat požadovaný výstupní formát podle svých potřeb.