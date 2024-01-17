---
title: Excel Přidat zalomení stránek
linktitle: Excel Přidat zalomení stránek
second_title: Aspose.Cells for .NET API Reference
description: Naučte se přidávat konce stránek v Excelu pomocí Aspose.Cells for .NET. Výukový program krok za krokem pro vytváření dobře strukturovaných zpráv.
type: docs
weight: 10
url: /cs/net/excel-page-breaks/excel-add-page-breaks/
---
Přidání zalomení stránek do souboru aplikace Excel je základní funkcí při vytváření velkých sestav nebo dokumentů. V tomto tutoriálu prozkoumáme, jak přidat konce stránek do souboru aplikace Excel pomocí knihovny Aspose.Cells pro .NET. Provedeme vás krok za krokem k pochopení a implementaci poskytnutého zdrojového kódu C#.

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

## Krok 4: Přidání vodorovného konce stránky

Nyní do našeho excelového listu přidáme vodorovný konec stránky. V ukázkovém kódu přidáme vodorovný konec stránky do buňky "Y30" prvního listu.

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
```

## Krok 5: Přidání svislého konce stránky

Podobně můžeme přidat vertikální konec stránky pomocí`VerticalPageBreaks.Add()` metoda. V našem příkladu přidáváme svislý konec stránky do buňky "Y30" prvního listu.

```csharp
workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");
```

## Krok 6: Uložení souboru Excel

 Nyní, když jsme přidali konce stránek, musíme uložit konečný soubor Excel. Použijte`Save()` metoda k určení úplné cesty výstupního souboru.

```csharp
// Uložte soubor aplikace Excel.
workbook.Save(dataDir + "AddingPageBreaks_out.xls");
```
### Ukázkový zdrojový kód pro Excel Přidat zalomení stránek pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření instance objektu sešitu
Workbook workbook = new Workbook();
// Přidejte konec stránky do buňky Y30
workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");
// Uložte soubor aplikace Excel.
workbook.Save(dataDir + "AddingPageBreaks_out.xls");
```

## Závěr

V tomto tutoriálu jsme se naučili přidávat přestávky

  stránku v souboru aplikace Excel pomocí Aspose.Cells for .NET. Podle uvedených kroků budete moci snadno vkládat vodorovné a svislé zalomení stránek do dynamicky generovaných souborů aplikace Excel. Nebojte se více experimentovat s knihovnou Aspose.Cells a objevovat další výkonné funkce, které nabízí.

### Nejčastější dotazy

#### Otázka: Je Aspose.Cells for .NET bezplatná knihovna?

Odpověď: Aspose.Cells for .NET je komerční knihovna, ale nabízí bezplatnou zkušební verzi, kterou můžete použít k vyhodnocení její funkčnosti.

#### Otázka: Mohu do souboru aplikace Excel přidat více zalomení stránek?

Odpověď: Ano, do různých částí tabulky můžete přidat tolik konců stránek, kolik potřebujete.

#### Otázka: Je možné odstranit dříve přidaný konec stránky?

Odpověď: Ano, Aspose.Cells vám umožňuje odstranit existující konce stránek pomocí vhodných metod objektu Worksheet.

#### Otázka: Funguje tato metoda také s jinými formáty souborů aplikace Excel, jako jsou XLSX nebo XLSM?

Odpověď: Ano, metoda popsaná v tomto návodu funguje s různými formáty souborů Excel podporovanými Aspose.Cells.

#### Otázka: Mohu přizpůsobit vzhled zalomení stránek v aplikaci Excel?

Odpověď: Ano, Aspose.Cells nabízí řadu funkcí pro přizpůsobení zalomení stránek, jako je styl, barva a rozměry.
