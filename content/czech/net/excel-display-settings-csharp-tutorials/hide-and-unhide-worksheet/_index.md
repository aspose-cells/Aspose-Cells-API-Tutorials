---
title: Skrýt a zobrazit pracovní list
linktitle: Skrýt a zobrazit pracovní list
second_title: Aspose.Cells for .NET API Reference
description: Výkonná knihovna pro práci se soubory Excel, včetně vytváření, úprav a manipulace s daty.
type: docs
weight: 90
url: /cs/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
V tomto tutoriálu vás krok za krokem provedeme vysvětlením následujícího zdrojového kódu C#, který se používá ke skrytí a zobrazení listu pomocí Aspose.Cells for .NET. Postupujte podle následujících kroků:

## Krok 1: Příprava prostředí

Než začnete, ujistěte se, že máte v systému nainstalovaný Aspose.Cells for .NET. Pokud jej ještě nemáte nainstalovaný, můžete si jej stáhnout z oficiálních stránek Aspose. Po instalaci můžete vytvořit nový projekt ve vámi preferovaném integrovaném vývojovém prostředí (IDE).

## Krok 2: Importujte požadované jmenné prostory

Ve zdrojovém souboru C# přidejte potřebné jmenné prostory, abyste mohli používat funkce Aspose.Cells. Na začátek souboru přidejte následující řádky:

```csharp
using Aspose.Cells;
using System.IO;
```

## Krok 3: Načtěte soubor Excel

Před skrytím nebo zobrazením listu musíte načíst soubor aplikace Excel do aplikace. Ujistěte se, že máte soubor Excel, který chcete použít, ve stejném adresáři jako váš projekt. K načtení souboru Excel použijte následující kód:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

Nezapomeňte nahradit "PATH TO YOUR DOCUMENTS DIRECTORY" skutečnou cestou k adresáři obsahujícímu váš soubor Excel.

## Krok 4: Otevřete tabulku

Po načtení souboru Excel můžete přejít na list, který chcete skrýt nebo zobrazit. Pro přístup k prvnímu listu v souboru použijte následující kód:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Krok 5: Skryjte pracovní list

 Nyní, když jste otevřeli list, můžete jej skrýt pomocí`IsVisible` vlastnictví. Pomocí následujícího kódu skryjte první list v souboru:

```csharp
worksheet. IsVisible = false;
```

## Krok 6: Znovu zobrazte list

Pokud chcete znovu zobrazit dříve skrytý list, můžete použít stejný kód změnou hodnoty`IsVisible` vlastnictví. Chcete-li znovu zobrazit první list, použijte následující kód:

```csharp
worksheet. IsVisible = true;
```

## Krok 7: Uložte změny

Jednou ty

  skryli nebo odkryli list podle potřeby, musíte změny uložit do souboru aplikace Excel. K uložení změn použijte následující kód:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Ujistěte se, že jste zadali správnou výstupní cestu pro uložení upraveného souboru Excel.

### Ukázka zdrojového kódu pro Hide And Unhide Worksheet pomocí Aspose.Cells pro .NET 

```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Vytvoření datového proudu souboru obsahujícího soubor Excel, který se má otevřít
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Vytvoření instance objektu Workbook s otevřením souboru aplikace Excel prostřednictvím datového proudu souborů
Workbook workbook = new Workbook(fstream);
// Přístup k prvnímu listu v souboru aplikace Excel
Worksheet worksheet = workbook.Worksheets[0];
// Skrytí prvního listu souboru Excel
worksheet.IsVisible = false;
// Zobrazí první list souboru Excel
//Worksheet.IsVisible = true;
// Uložení upraveného souboru Excel ve výchozím (tj. Excel 2003) formátu
workbook.Save(dataDir + "output.out.xls");
// Zavřením datového proudu souborů uvolníte všechny zdroje
fstream.Close();
```

## Závěr

gratuluji! Naučili jste se, jak skrýt a zobrazit tabulku pomocí Aspose.Cells pro .NET. Tuto funkci nyní můžete použít k ovládání viditelnosti tabulek v souborech aplikace Excel.

### Často kladené otázky (FAQ)

#### Jak mohu nainstalovat Aspose.Cells pro .NET?

 Aspose.Cells for .NET můžete nainstalovat stažením příslušného balíčku NuGet z[Aspose Releases](https://releases/aspose.com/cells/net/) a přidejte jej do projektu sady Visual Studio.

#### Jaká je minimální požadovaná verze .NET Framework pro použití Aspose.Cells pro .NET?

Aspose.Cells for .NET podporuje rozhraní .NET Framework 2.0 a novější.

#### Mohu otevřít a upravit existující soubory aplikace Excel pomocí Aspose.Cells for .NET?

Ano, můžete otevírat a upravovat existující soubory aplikace Excel pomocí Aspose.Cells for .NET. Můžete přistupovat k listům, buňkám, vzorcům a dalším prvkům souboru Excel.

#### Podporuje Aspose.Cells for .NET hlášení a export do jiných formátů souborů?

Ano, Aspose.Cells for .NET podporuje generování sestav a export do formátů jako PDF, HTML, CSV, TXT atd.

#### Je úprava souboru Excel trvalá?

Ano, úprava souboru Excel je po uložení trvalá. Před provedením jakýchkoli změn v původním souboru si uložte záložní kopii.