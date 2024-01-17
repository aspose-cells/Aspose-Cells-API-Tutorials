---
title: Excel Vymazat všechny konce stránek
linktitle: Excel Vymazat všechny konce stránek
second_title: Aspose.Cells for .NET API Reference
description: Naučte se, jak odstranit všechny konce stránek v Excelu pomocí Aspose.Cells for .NET. Výukový program krok za krokem pro vyčištění souborů aplikace Excel.
type: docs
weight: 20
url: /cs/net/excel-page-breaks/excel-clear-all-page-breaks/
---

Odstranění zalomení stránek v souboru aplikace Excel je nezbytným krokem při práci se sestavami nebo tabulkami. V tomto tutoriálu vás krok za krokem provedeme k pochopení a implementaci poskytnutého zdrojového kódu C# k odstranění všech zalomení stránek v souboru Excel pomocí knihovny Aspose.Cells pro .NET.

## Krok 1: Příprava prostředí

 Než začnete, ujistěte se, že máte na svém počítači nainstalovaný Aspose.Cells for .NET. Knihovnu si můžete stáhnout z[Aspose Releases](https://releases.aspose.com/cells/net) nainstalujte jej podle dodaných pokynů.

Po dokončení instalace vytvořte nový projekt C# ve vašem preferovaném integrovaném vývojovém prostředí (IDE) a importujte knihovnu Aspose.Cells pro .NET.

## Krok 2: Konfigurace cesty k adresáři dokumentu

 V poskytnutém zdrojovém kódu musíte zadat cestu k adresáři, kam chcete uložit vygenerovaný soubor Excel. Upravte`dataDir` proměnnou nahrazením "VÁŠ ADRESÁŘ DOKUMENTŮ" absolutní cestou k adresáři na vašem počítači.

```csharp
//Cesta k adresáři dokumentů.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## Krok 3: Vytvoření objektu sešitu

Chcete-li začít, musíme vytvořit objekt Workbook, který představuje náš soubor Excel. Toho lze dosáhnout pomocí třídy Workbook poskytované Aspose.Cells.

```csharp
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
```

## Krok 4: Odstraňte konce stránek

 Nyní odstraníme všechny konce stránek v našem excelovém listu. V ukázkovém kódu používáme`Clear()` metody pro vodorovné a svislé zalomení stránek k jejich odstranění.

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
```

## Krok 5: Uložení souboru Excel

 Jakmile budou odstraněny všechny konce stránek, můžeme uložit konečný soubor Excel. Použijte`Save()` metoda k určení úplné cesty výstupního souboru.

```csharp
// Uložte soubor aplikace Excel.
workbook.Save(dataDir + "ClearingPageBreaks_out.xls");
```

### Ukázkový zdrojový kód pro Excel Vymazat všechny konce stránek pomocí Aspose.Cells pro .NET 

```csharp

//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
// Vymazání všech konců stránek
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
// Uložte soubor aplikace Excel.
workbook.Save(dataDir + "ClearAllPageBreaks_out.xls");

```

## Závěr

tomto tutoriálu jsme se naučili, jak odstranit všechny konce stránek v souboru aplikace Excel pomocí Aspose.Cells for .NET. Podle uvedených kroků můžete snadno spravovat a čistit nežádoucí konce stránek v dynamicky generovaných souborech aplikace Excel. Neváhejte dále prozkoumat funkce nabízené Aspose.Cells pro pokročilejší operace.

### Nejčastější dotazy

#### Otázka: Je Aspose.Cells for .NET bezplatná knihovna?

Odpověď: Aspose.Cells for .NET je komerční knihovna, ale nabízí bezplatnou zkušební verzi, kterou můžete použít k vyhodnocení její funkčnosti.

#### Otázka: Má odstranění zalomení stránek vliv na jiné prvky listu?

Odpověď: Ne, odstranění konců stránek změní pouze samotné konce stránek a neovlivní žádná další data nebo formátování v listu.

#### Otázka: Mohu selektivně odstranit některé konkrétní konce stránek v aplikaci Excel?

Odpověď: Ano, s Aspose.Cells můžete individuálně přistupovat ke každému zlomu stránky a v případě potřeby jej odstranit pomocí vhodných metod.

#### Otázka: Jaké další formáty souborů aplikace Excel podporuje Aspose.Cells for .NET?

A: Aspose.Cells for .NET podporuje různé formáty souborů Excel, jako jsou XLSX, XLSM, CSV, HTML, PDF atd.

