---
title: Kopírovat pracovní list aplikace Excel
linktitle: Kopírovat pracovní list aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Zkopírujte jeden list Excelu do druhého pomocí Aspose.Cells for .NET.
type: docs
weight: 20
url: /cs/net/excel-copy-worksheet/excel-copy-worksheet/
---

V této příručce vysvětlíme, jak zkopírovat pracovní list aplikace Excel pomocí knihovny Aspose.Cells pro .NET. Poskytneme vám zdrojový kód C# a provedeme vás kroky potřebnými k dokončení tohoto úkolu. Na konci vám ukážeme očekávaný výsledek. Začněte podle pokynů níže.

## Krok 1: Příprava

Než začnete, ujistěte se, že jste nainstalovali Aspose.Cells for .NET a vytvořili projekt C# ve vašem preferovaném integrovaném vývojovém prostředí (IDE). Také se ujistěte, že máte kopii souboru Excel, se kterým chcete manipulovat.

## Krok 2: Importujte požadované knihovny

 Ve zdrojovém souboru C# importujte potřebné knihovny z Aspose.Cells pomocí`using` směrnice:

```csharp
using Aspose.Cells;
```

## Krok 3: Nastavte cestu k souboru

 Prohlásit a`dataDir` proměnnou a inicializujte ji adresářem obsahujícím váš soubor Excel. Například :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Nezapomeňte vyměnit`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` se skutečnou cestou k vašemu adresáři.

## Krok 4: Načtěte existující soubor Excel

 Použijte`Workbook` třídy z Aspose.Cells k otevření stávajícího souboru aplikace Excel. Použijte`InputPath` proměnná pro určení cesty k souboru:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Ujistěte se, že jste vyměnili`"book1.xls"` se skutečným názvem souboru Excel.

## Krok 5: Zkopírujte pracovní list

 Nyní zkopírujeme existující list do nového listu. Použijte`Worksheets` vlastnictvím`Workbook` objekt pro přístup ke kolekci pracovních listů:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Poté použijte`AddCopy` způsob kopírování zadaného listu. Chcete-li například zkopírovat „Sheet1“:

```csharp
sheets.AddCopy("Sheet1");
```

## Krok 6: Uložte soubor Excel

 Použijte`Save` metoda`Workbook` objekt pro uložení změn do nového souboru:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Nezapomeňte zadat požadovanou cestu a název souboru pro výstupní soubor.

### Ukázka zdrojového kódu pro Excel Copy Worksheet pomocí Aspose.Cells pro .NET 

```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Otevřete existující soubor aplikace Excel.
Workbook wb = new Workbook(InputPath);
// Vytvořte objekt Listy s odkazem na
// listy Pracovního sešitu.
WorksheetCollection sheets = wb.Worksheets;
// Zkopírujte data do nového listu z existujícího
// list v sešitu.
sheets.AddCopy("Sheet1");
// Uložte soubor aplikace Excel.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Závěr

gratuluji! Nyní jste se naučili kopírovat pracovní list aplikace Excel pomocí Aspose.Cells for .NET. Tento průvodce krok za krokem ukázal, jak importovat potřebné knihovny, načíst existující soubor Excel, zkopírovat list a uložit upravený soubor. Neváhejte použít tuto metodu ve svých vlastních projektech k efektivní manipulaci se soubory Excel.

### Nejčastější dotazy

#### Otázka: Je Aspose.Cells kompatibilní s jinými programovacími jazyky?

A. Ano, Aspose.Cells podporuje více programovacích jazyků včetně C#, Java, Python a mnoha dalších.

#### Otázka: Mohu zkopírovat list do jiného sešitu aplikace Excel?

A.  Ano, můžete použít`AddCopy` metoda kopírování listu do jiného sešitu aplikace Excel.

#### Otázka: Zachová Aspose.Cells při kopírování listu vzorce a formátování?

A. Ano, Aspose.Cells zachovává vzorce, formátování a další vlastnosti při kopírování listu.

#### Otázka: Vyžaduje Aspose.Cells licenci pro komerční použití?

A. Ano, Aspose.Cells je komerční produkt a vyžaduje zakoupení licence pro komerční použití. Další informace o licencích najdete na oficiálních stránkách Aspose.