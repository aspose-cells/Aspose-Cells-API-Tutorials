---
title: Pokročilá nastavení ochrany pro pracovní list aplikace Excel
linktitle: Pokročilá nastavení ochrany pro pracovní list aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Chraňte své soubory Excel nastavením pokročilých nastavení ochrany pomocí Aspose.Cells pro .NET.
type: docs
weight: 10
url: /cs/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
V tomto tutoriálu vás provedeme kroky k nastavení pokročilého nastavení ochrany pro tabulku Excel pomocí knihovny Aspose.Cells pro .NET. Dokončete tento úkol podle níže uvedených pokynů.

## Krok 1: Příprava

Ujistěte se, že jste nainstalovali Aspose.Cells for .NET a vytvořili projekt C# ve vašem preferovaném integrovaném vývojovém prostředí (IDE).

## Krok 2: Nastavte cestu k adresáři dokumentu

 Prohlásit a`dataDir` proměnnou a inicializujte ji s cestou k adresáři vašich dokumentů. Například :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Nezapomeňte vyměnit`"YOUR_DOCUMENTS_DIRECTORY"` se skutečnou cestou k vašemu adresáři.

## Krok 3: Vytvořte datový proud souboru pro otevření souboru Excel

 Vytvořit`FileStream` objekt obsahující soubor Excel k otevření:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Ujistěte se, že máte soubor Excel`book1.xls` v adresáři dokumentů nebo zadejte správný název souboru a umístění.

## Krok 4: Vytvořte instanci objektu Workbook a otevřete soubor aplikace Excel

 Použijte`Workbook`třídy z Aspose.Cells k vytvoření instance objektu Workbook a otevření zadaného souboru aplikace Excel prostřednictvím datového proudu souboru:

```csharp
Workbook excel = new Workbook(fstream);
```

## Krok 5: Otevřete první list

Přejděte na první list souboru Excel:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Krok 6: Nastavte nastavení ochrany listu

Pomocí vlastností objektu Worksheet nastavte ochranu listu podle potřeby. Například :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Podle potřeby nastavte další nastavení ochrany...
```

## Krok 7: Uložte upravený soubor Excel

 Uložte upravený soubor Excel pomocí`Save` metoda objektu Workbook:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Nezapomeňte zadat požadovanou cestu a název souboru pro výstupní soubor.

## Krok 8: Zavřete datový proud souboru

Po uložení zavřete datový proud souboru a uvolněte všechny přidružené zdroje:

```csharp
fstream.Close();
```
	
### Ukázkový zdrojový kód pro Advanced Protection Settings for Excel Worksheet pomocí Aspose.Cells for .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření datového proudu souboru obsahujícího soubor Excel, který se má otevřít
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Vytvoření instance objektu sešitu
// Otevření souboru aplikace Excel prostřednictvím datového proudu souborů
Workbook excel = new Workbook(fstream);
// Přístup k prvnímu listu v souboru aplikace Excel
Worksheet worksheet = excel.Worksheets[0];
// Omezení uživatelů na odstranění sloupců listu
worksheet.Protection.AllowDeletingColumn = false;
// Omezení uživatelů na odstranění řádku listu
worksheet.Protection.AllowDeletingRow = false;
// Omezení uživatelů upravovat obsah listu
worksheet.Protection.AllowEditingContent = false;
// Omezení uživatelů upravovat objekty listu
worksheet.Protection.AllowEditingObject = false;
// Omezení uživatelů na úpravu scénářů listu
worksheet.Protection.AllowEditingScenario = false;
//Omezení filtrování uživatelů
worksheet.Protection.AllowFiltering = false;
// Umožňuje uživatelům formátovat buňky listu
worksheet.Protection.AllowFormattingCell = true;
// Umožňuje uživatelům formátovat řádky listu
worksheet.Protection.AllowFormattingRow = true;
// Umožňuje uživatelům vkládat sloupce do listu
worksheet.Protection.AllowFormattingColumn = true;
// Umožňuje uživatelům vkládat do listu hypertextové odkazy
worksheet.Protection.AllowInsertingHyperlink = true;
// Umožňuje uživatelům vkládat řádky do listu
worksheet.Protection.AllowInsertingRow = true;
// Umožňuje uživatelům vybrat uzamčené buňky listu
worksheet.Protection.AllowSelectingLockedCell = true;
// Umožňuje uživatelům vybrat odemčené buňky listu
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Umožňuje uživatelům třídit
worksheet.Protection.AllowSorting = true;
// Umožňuje uživatelům používat kontingenční tabulky v listu
worksheet.Protection.AllowUsingPivotTable = true;
// Uložení upraveného souboru Excel
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Zavřením datového proudu souborů uvolníte všechny zdroje
fstream.Close();
```

## Závěr

gratuluji! Nyní jste se naučili, jak nastavit pokročilá nastavení ochrany pro tabulku Excel pomocí Aspose.Cells for .NET. Použijte tyto znalosti k zabezpečení souborů aplikace Excel a omezení akcí uživatelů.

### Nejčastější dotazy

#### Otázka: Jak mohu vytvořit nový projekt C# v mém IDE?

A: Kroky k vytvoření nového projektu C# se mohou lišit v závislosti na IDE, které používáte. Podrobné pokyny najdete v dokumentaci vašeho IDE.

#### Otázka: Je možné nastavit vlastní nastavení ochrany jiná než ta, která jsou uvedena v tutoriálu?

Odpověď: Ano, Aspose.Cells nabízí širokou škálu nastavení ochrany, která si můžete přizpůsobit svým konkrétním potřebám. Další podrobnosti najdete v dokumentaci Aspose.Cells.

#### Otázka: Jaký formát souboru se používá k uložení upraveného souboru aplikace Excel v ukázkovém kódu?

Odpověď: V ukázkovém kódu je upravený soubor Excel uložen ve formátu Excel 97-2003 (.xls). V případě potřeby si můžete vybrat jiné formáty podporované Aspose.Cells.

#### Otázka: Jak mohu získat přístup k dalším listům v souboru aplikace Excel?

 Odpověď: K dalším listům můžete přistupovat pomocí indexu nebo názvu listu, například:`Worksheet worksheet = excel.Worksheets[1];` nebo`Worksheet worksheet = excel.Worksheets[" SheetName"];`.