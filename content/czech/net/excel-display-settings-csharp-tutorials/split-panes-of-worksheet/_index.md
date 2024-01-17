---
title: Rozdělit Panely Listu
linktitle: Rozdělit Panely Listu
second_title: Aspose.Cells for .NET API Reference
description: Podrobný průvodce rozdělením podoken v listu aplikace Excel pomocí Aspose.Cells pro .NET.
type: docs
weight: 130
url: /cs/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
V tomto tutoriálu vysvětlíme, jak rozdělit podokna v listu aplikace Excel pomocí Aspose.Cells for .NET. Chcete-li dosáhnout požadovaného výsledku, postupujte takto:

## Krok 1: Nastavení prostředí

Ujistěte se, že jste nainstalovali Aspose.Cells for .NET a nastavili své vývojové prostředí. Také se ujistěte, že máte kopii souboru Excel, na který chcete rozdělit podokna.

## Krok 2: Importujte potřebné závislosti

Přidejte potřebné direktivy pro použití tříd z Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Krok 3: Inicializace kódu

Začněte inicializací cesty k adresáři obsahujícímu vaše dokumenty Excel:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Krok 4: Otevření souboru Excel

 Vytvořte nový`Workbook` objekt a otevřete soubor Excel pomocí`Open` metoda:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Krok 5: Definujte aktivní buňku

 Nastavte aktivní buňku listu pomocí`ActiveCell` vlastnictví:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Krok 6: Rozdělení klapek

 Rozdělte okno listu pomocí`Split` metoda:

```csharp
book.Worksheets[0].Split();
```

## Krok 7: Uložení změn

Uložte změny provedené v souboru Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### Ukázka zdrojového kódu pro Split Panes Of Worksheet pomocí Aspose.Cells pro .NET 

```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvořte instanci nového sešitu a otevřete soubor šablony
Workbook book = new Workbook(dataDir + "Book1.xls");
// Nastavte aktivní buňku
book.Worksheets[0].ActiveCell = "A20";
// Rozdělte okno listu
book.Worksheets[0].Split();
// Uložte soubor aplikace Excel
book.Save(dataDir + "output.xls");
```

## Závěr

tomto kurzu jste se naučili, jak rozdělit podokna v listu aplikace Excel pomocí Aspose.Cells for .NET. Podle popsaných kroků můžete snadno přizpůsobit vzhled a chování svých souborů aplikace Excel.

### Často kladené otázky (FAQ)

#### Co je Aspose.Cells pro .NET?

Aspose.Cells for .NET je oblíbená softwarová knihovna pro manipulaci se soubory Excel v aplikacích .NET.

#### Jak mohu nastavit aktivní buňku listu v Aspose.Cells?

 Aktivní buňku můžete nastavit pomocí`ActiveCell`vlastnost objektu Worksheet.

#### Mohu rozdělit pouze horizontální nebo vertikální podokna okna listu?

 Ano, pomocí Aspose.Cells můžete rozdělit pouze horizontální nebo vertikální panely pomocí vhodných metod, jako je např`SplitColumn` nebo`SplitRow`.

#### Funguje Aspose.Cells pouze se soubory aplikace Excel ve formátu .xls?

Ne, Aspose.Cells podporuje různé formáty souborů Excel včetně .xls a .xlsx.