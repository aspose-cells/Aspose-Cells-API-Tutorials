---
title: Přesunout list aplikace Excel
linktitle: Přesunout list aplikace Excel
second_title: Aspose.Cells for .NET API Reference
description: Pomocí Aspose.Cells for .NET můžete snadno přesunout list do sešitu aplikace Excel.
type: docs
weight: 40
url: /cs/net/excel-copy-worksheet/excel-move-worksheet/
---
tomto tutoriálu vás provedeme kroky k přesunutí listu do sešitu aplikace Excel pomocí knihovny Aspose.Cells pro .NET. Dokončete tento úkol podle níže uvedených pokynů.


## Krok 1: Příprava

Ujistěte se, že jste nainstalovali Aspose.Cells for .NET a vytvořili projekt C# ve vašem preferovaném integrovaném vývojovém prostředí (IDE).

## Krok 2: Nastavte cestu k adresáři dokumentu

 Prohlásit a`dataDir` proměnnou a inicializujte ji s cestou k adresáři vašich dokumentů. Například :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Nezapomeňte vyměnit`"YOUR_DOCUMENTS_DIRECTORY"` se skutečnou cestou k vašemu adresáři.

## Krok 3: Definujte cestu k vstupnímu souboru

 Prohlásit an`InputPath` proměnnou a inicializujte ji úplnou cestou existujícího souboru Excel, který chcete upravit. Například :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Ujistěte se, že máte soubor Excel`book1.xls` v adresáři dokumentů nebo zadejte správný název souboru a umístění.

## Krok 4: Otevřete soubor aplikace Excel

 Použijte`Workbook` třídy Aspose.Cells k otevření zadaného souboru Excel:

```csharp
Workbook wb = new Workbook(InputPath);
```

## Krok 5: Získejte kolekci tabulek

 Vytvořit`WorksheetCollection` objekt odkazovat na listy v sešitu:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

## Krok 6: Získejte první pracovní list

Získejte první pracovní list v sešitu:

```csharp
Worksheet worksheet = sheets[0];
```

## Krok 7: Přesuňte list

 Použijte`MoveTo` metoda přesunutí prvního listu na třetí pozici v sešitu:

```csharp
worksheet.MoveTo(2);
```

## Krok 8: Uložte upravený soubor Excel

Uložte soubor Excel s přesunutým listem:

```csharp
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

Nezapomeňte zadat požadovanou cestu a název souboru pro výstupní soubor.

### Ukázka zdrojového kódu pro Excel Move Worksheet pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Otevřete existující soubor aplikace Excel.
Workbook wb = new Workbook(InputPath);
// Vytvořte objekt Listy s odkazem na
// listy Pracovního sešitu.
WorksheetCollection sheets = wb.Worksheets;
// Získejte první pracovní list.
Worksheet worksheet = sheets[0];
// Přesuňte první list na třetí pozici v sešitu.
worksheet.MoveTo(2);
// Uložte soubor aplikace Excel.
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

## Závěr

gratuluji! Nyní jste se naučili, jak přesunout list do sešitu aplikace Excel pomocí Aspose.Cells for .NET. Neváhejte použít tuto metodu ve svých vlastních projektech k efektivní manipulaci se soubory Excel.

### Nejčastější dotazy

#### Otázka: Mohu přesunout list na jiné místo ve stejném sešitu aplikace Excel?

A.  Ano, list můžete přesunout na jinou pozici ve stejném excelovém sešitu pomocí`MoveTo` metoda objektu Worksheet. Stačí zadat index cílové pozice v sešitu.

#### Q. Mohu přesunout list do jiného sešitu aplikace Excel?

A.  Ano, list můžete přesunout do jiného sešitu aplikace Excel pomocí`MoveTo` metoda objektu Worksheet. Stačí zadat index cílové pozice v cílovém sešitu.

#### Otázka: Funguje dodaný zdrojový kód s jinými formáty souborů Excel, jako je XLSX?

A. Ano, poskytnutý zdrojový kód funguje s jinými formáty souborů Excel, včetně XLSX. Aspose.Cells for .NET podporuje různé formáty souborů aplikace Excel, což vám umožňuje manipulovat a přesouvat listy do různých typů souborů.

#### Otázka: Jak mohu určit cestu a název výstupního souboru při ukládání upraveného souboru aplikace Excel?

A.  Při ukládání upraveného souboru Excel použijte`Save` metoda objektu Workbook určující úplnou cestu a název výstupního souboru. Nezapomeňte zadat příslušnou příponu souboru, jako např`.xls` nebo`.xlsx`, v závislosti na požadovaném formátu souboru.