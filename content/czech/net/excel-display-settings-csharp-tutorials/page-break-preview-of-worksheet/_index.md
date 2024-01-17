---
title: Náhled Zalomení Listu
linktitle: Náhled Zalomení Listu
second_title: Aspose.Cells for .NET API Reference
description: Průvodce krok za krokem pro zobrazení náhledu konce stránky listu pomocí Aspose.Cells pro .NET.
type: docs
weight: 110
url: /cs/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
V tomto tutoriálu vysvětlíme, jak zobrazit náhled konce stránky listu pomocí Aspose.Cells for .NET. Chcete-li dosáhnout požadovaného výsledku, postupujte takto:

## Krok 1: Nastavení prostředí

Ujistěte se, že jste nainstalovali Aspose.Cells for .NET a nastavili své vývojové prostředí. Také se ujistěte, že máte kopii souboru Excel, ve kterém chcete zobrazit náhled konce stránky.

## Krok 2: Importujte potřebné závislosti

Přidejte potřebné direktivy pro použití tříd z Aspose.Cells:

```csharp
using Aspose.Cells;
using System.IO;
```

## Krok 3: Inicializace kódu

Začněte inicializací cesty k adresáři obsahujícímu vaše dokumenty Excel:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Krok 4: Otevření souboru Excel

 Vytvořit`FileStream` objekt obsahující soubor Excel k otevření:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Instantovat a`Workbook` objekt a otevřete soubor Excel pomocí datového proudu souboru:

```csharp
Workbook workbook = new Workbook(fstream);
```

## Krok 5: Přístup k tabulce

Přejděte na první list v souboru aplikace Excel:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Krok 6: Zobrazení náhledu po jednotlivých stránkách

Povolit náhled po jednotlivých stránkách pro tabulku:

```csharp
worksheet. IsPageBreakPreview = true;
```

## Krok 7: Uložení změn

Uložte změny provedené v souboru Excel:

```csharp
workbook.Save(dataDir + "output.xls");
```

## Krok 8: Zavření datového proudu souborů

Zavřete datový proud souboru a uvolněte všechny prostředky:

```csharp
fstream.Close();
```

### Ukázkový zdrojový kód pro náhled stránky zalomení listu pomocí Aspose.Cells pro .NET 
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
// Zobrazení listu v náhledu konce stránky
worksheet.IsPageBreakPreview = true;
// Uložení upraveného souboru Excel
workbook.Save(dataDir + "output.xls");
// Zavřením datového proudu souborů uvolníte všechny zdroje
fstream.Close();
```

## Závěr

V tomto tutoriálu jste se naučili, jak zobrazit náhled konce stránky listu pomocí Aspose.Cells for .NET. Podle popsaných kroků můžete snadno ovládat vzhled a rozvržení souborů aplikace Excel.

### Často kladené otázky (FAQ)

#### Co je Aspose.Cells pro .NET?

Aspose.Cells for .NET je oblíbená softwarová knihovna pro manipulaci se soubory Excel v aplikacích .NET.

#### Mohu zobrazit náhled po jednotlivých stránkách pro konkrétní list místo celého listu?

Ano, pomocí Aspose.Cells můžete povolit náhled konce stránky pro konkrétní list přístupem k odpovídajícímu objektu Worksheet.

#### Podporuje Aspose.Cells další funkce pro úpravu souborů aplikace Excel?

Ano, Aspose.Cells nabízí širokou škálu funkcí pro úpravu a manipulaci se soubory Excel, jako je přidávání dat, formátování, vytváření grafů atd.

#### Funguje Aspose.Cells pouze se soubory aplikace Excel ve formátu .xls?

Ne, Aspose.Cells podporuje různé formáty souborů Excel včetně .xls a .xlsx.
	