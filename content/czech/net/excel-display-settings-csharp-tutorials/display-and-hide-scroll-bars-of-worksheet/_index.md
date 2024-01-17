---
title: Zobrazit A Skrýt Posuvníky Listu
linktitle: Zobrazit A Skrýt Posuvníky Listu
second_title: Aspose.Cells for .NET API Reference
description: Zobrazte nebo skryjte posuvníky v listu aplikace Excel pomocí Aspose.Cells for .NET.
type: docs
weight: 50
url: /cs/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
V tomto tutoriálu vám ukážeme, jak zobrazit nebo skrýt svislé a vodorovné posuvníky v listu aplikace Excel pomocí zdrojového kódu C# s Aspose.Cells for .NET. Chcete-li dosáhnout požadovaného výsledku, postupujte podle níže uvedených kroků.

## Krok 1: Importujte potřebné knihovny

Ujistěte se, že máte nainstalovanou knihovnu Aspose.Cells pro .NET a importujte potřebné knihovny do svého projektu C#.

```csharp
using Aspose.Cells;
using System.IO;
```

## Krok 2: Nastavte cestu k adresáři a otevřete soubor Excel

 Nastavte cestu k adresáři obsahujícímu váš soubor Excel a poté soubor otevřete vytvořením datového proudu a vytvořením instance a`Workbook` objekt.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Krok 3: Skryjte posuvníky

 Použijte`IsVScrollBarVisible` a`IsHScrollBarVisible` vlastnosti`Workbook.Settings` objekt, chcete-li skrýt svislé a vodorovné posuvníky listu.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## Krok 4: Uložte změny

 Jakmile provedete potřebné změny, uložte upravený soubor Excel pomocí`Save` metoda`Workbook` objekt.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Ukázkový zdrojový kód pro zobrazení a skrytí posuvníků listu pomocí Aspose.Cells pro .NET 

```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření datového proudu souboru obsahujícího soubor Excel, který se má otevřít
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Vytvoření instance objektu sešitu
// Otevření souboru aplikace Excel prostřednictvím datového proudu souborů
Workbook workbook = new Workbook(fstream);
// Skrytí svislého posuvníku souboru Excel
workbook.Settings.IsVScrollBarVisible = false;
// Skrytí vodorovného posuvníku souboru Excel
workbook.Settings.IsHScrollBarVisible = false;
// Uložení upraveného souboru Excel
workbook.Save(dataDir + "output.xls");
// Zavřením datového proudu souborů uvolníte všechny zdroje
fstream.Close();
```

### Závěr

Tento podrobný průvodce vám ukázal, jak zobrazit nebo skrýt svislé a vodorovné posuvníky v tabulce aplikace Excel pomocí Aspose.Cells pro .NET. Pomocí dodaného zdrojového kódu C# můžete snadno přizpůsobit zobrazení posuvníků v souborech aplikace Excel.

### Často kladené otázky (FAQ)

#### Co je Aspose.Cells pro .NET?

Aspose.Cells for .NET je výkonná knihovna pro manipulaci se soubory aplikace Excel v aplikacích .NET.

#### Jak mohu nainstalovat Aspose.Cells pro .NET?

 Chcete-li nainstalovat Aspose.Cells pro .NET, musíte si stáhnout příslušný balíček z[Aspose Releases](https://releases/aspose.com/cells/net/) a přidejte jej do svého projektu .NET.

#### Jak mohu zobrazit nebo skrýt posuvníky v tabulce aplikace Excel pomocí Aspose.Cells pro .NET?

 Můžete použít`IsVScrollBarVisible` a`IsHScrollBarVisible` vlastnosti`Workbook.Settings` objekt pro zobrazení nebo skrytí svislého a vodorovného posuvníku v listu aplikace Excel.

#### Jaké další formáty souborů aplikace Excel podporuje Aspose.Cells for .NET?

Aspose.Cells for .NET podporuje různé formáty souborů aplikace Excel, jako jsou XLS, XLSX, CSV, HTML, PDF atd.