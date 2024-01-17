---
title: Zmrazit Panely Listu
linktitle: Zmrazit Panely Listu
second_title: Aspose.Cells for .NET API Reference
description: Pomocí Aspose.Cells for .NET můžete snadno manipulovat se zmrazenými panely listu aplikace Excel.
type: docs
weight: 70
url: /cs/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
V tomto tutoriálu vám ukážeme, jak zamknout podokna v listu aplikace Excel pomocí zdrojového kódu C# s Aspose.Cells pro .NET. Chcete-li dosáhnout požadovaného výsledku, postupujte podle níže uvedených kroků.

## Krok 1: Importujte potřebné knihovny

Ujistěte se, že máte nainstalovanou knihovnu Aspose.Cells pro .NET a importujte potřebné knihovny do svého projektu C#.

```csharp
using Aspose.Cells;
```

## Krok 2: Nastavte cestu k adresáři a otevřete soubor Excel

 Nastavte cestu k adresáři obsahujícímu váš soubor Excel a poté soubor otevřete vytvořením instance a`Workbook` objekt.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Krok 3: Přejděte do tabulky a použijte nastavení zámku panelu

 Přejděte na první list v souboru aplikace Excel pomocí`Worksheet` objekt. Poté použijte`FreezePanes` způsob použití nastavení zámku panelu.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

Ve výše uvedeném příkladu jsou podokna uzamčena k buňce v řádku 3 a sloupci 2.

## Krok 4: Uložte změny

 Jakmile provedete potřebné změny, uložte upravený soubor Excel pomocí`Save` metoda`Workbook` objekt.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Ukázka zdrojového kódu pro Freeze Panes Of Worksheet pomocí Aspose.Cells pro .NET 

```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření datového proudu souboru obsahujícího soubor Excel, který se má otevřít
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Vytvoření instance objektu sešitu
// Otevření souboru aplikace Excel prostřednictvím datového proudu souborů
Workbook workbook = new Workbook(fstream);
// Přístup k prvnímu listu v souboru aplikace Excel
Worksheet worksheet = workbook.Worksheets[0];
// Použití nastavení zmrazených panelů
worksheet.FreezePanes(3, 2, 3, 2);
// Uložení upraveného souboru Excel
workbook.Save(dataDir + "output.xls");
// Zavřením datového proudu souborů uvolníte všechny zdroje
fstream.Close();
```

## Závěr

Tento podrobný průvodce vám ukázal, jak zamknout podokna v tabulce Excel pomocí Aspose.Cells pro .NET. Pomocí dodaného zdrojového kódu C# můžete snadno přizpůsobit nastavení zámku panelu pro lepší organizaci a vizualizaci dat v souborech aplikace Excel.

### Často kladené otázky (FAQ)

#### Co je Aspose.Cells pro .NET?

Aspose.Cells for .NET je výkonná knihovna pro manipulaci se soubory aplikace Excel v aplikacích .NET.

#### Jak mohu nainstalovat Aspose.Cells pro .NET?

 Chcete-li nainstalovat Aspose.Cells pro .NET, musíte si stáhnout příslušný balíček z[Aspose Releases](https://releases/aspose.com/cells/net/) a přidejte jej do svého projektu .NET.

#### Jak zamknout podokna v listu aplikace Excel pomocí Aspose.Cells pro .NET?

 Můžete použít`FreezePanes` metoda`Worksheet` objekt k uzamčení podoken listu. Určete buňky, které chcete uzamknout, zadáním indexů řádků a sloupců.

#### Mohu upravit nastavení zámku panelu pomocí Aspose.Cells pro .NET?

 Ano, pomocí`FreezePanes` můžete podle potřeby určit, které buňky se mají uzamknout, a poskytnout příslušné indexy řádků a sloupců.
