---
title: Odebrat panely listu
linktitle: Odebrat panely listu
second_title: Aspose.Cells for .NET API Reference
description: Průvodce krok za krokem k odstranění podoken z listu aplikace Excel pomocí Aspose.Cells for .NET.
type: docs
weight: 120
url: /cs/net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
V tomto tutoriálu vysvětlíme, jak odstranit panely z listu aplikace Excel pomocí Aspose.Cells for .NET. Chcete-li dosáhnout požadovaného výsledku, postupujte takto:

## Krok 1: Nastavení prostředí

Ujistěte se, že jste nainstalovali Aspose.Cells for .NET a nastavili své vývojové prostředí. Také se ujistěte, že máte kopii souboru aplikace Excel, ze kterého chcete panely odebrat.

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

## Krok 6: Odstranění panelů

 Odstraňte podokna z okna listu pomocí`RemoveSplit` metoda:

```csharp
book.Worksheets[0].RemoveSplit();
```

## Krok 7: Uložení změn

Uložte změny provedené v souboru Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### Ukázka zdrojového kódu pro Remove Panes Of Worksheet pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvořte instanci nového sešitu a otevřete soubor šablony
Workbook book = new Workbook(dataDir + "Book1.xls");
// Nastavte aktivní buňku
book.Worksheets[0].ActiveCell = "A20";
// Rozdělte okno listu
book.Worksheets[0].RemoveSplit();
// Uložte soubor aplikace Excel
book.Save(dataDir + "output.xls");
```

## Závěr

V tomto kurzu jste se naučili, jak odstranit panely z listu aplikace Excel pomocí Aspose.Cells for .NET. Podle popsaných kroků můžete snadno přizpůsobit vzhled a chování svých souborů aplikace Excel.

### Často kladené otázky (FAQ)

#### Co je Aspose.Cells pro .NET?

Aspose.Cells for .NET je oblíbená softwarová knihovna pro manipulaci se soubory Excel v aplikacích .NET.

#### Jak mohu nastavit aktivní buňku listu v Aspose.Cells?

 Aktivní buňku můžete nastavit pomocí`ActiveCell`vlastnost objektu Worksheet.

#### Mohu z okna listu odstranit pouze vodorovné nebo svislé panely?

 Ano, pomocí Aspose.Cells můžete odstranit pouze horizontální nebo vertikální panely pomocí vhodných metod, jako je např`RemoveHorizontalSplit` nebo`RemoveVerticalSplit`.

#### Funguje Aspose.Cells pouze se soubory aplikace Excel ve formátu .xls?

Ne, Aspose.Cells podporuje různé formáty souborů Excel včetně .xls a .xlsx.
	