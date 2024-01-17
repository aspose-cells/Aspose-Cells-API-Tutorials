---
title: Kontrolní faktor zvětšení listu
linktitle: Kontrolní faktor zvětšení listu
second_title: Aspose.Cells for .NET API Reference
description: Ovládejte faktor přiblížení listu aplikace Excel pomocí Aspose.Cells pro .NET.
type: docs
weight: 20
url: /cs/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
Řízení faktoru přiblížení listu je základní funkcí při práci se soubory aplikace Excel pomocí knihovny Aspose.Cells pro .NET. V této příručce vám ukážeme, jak používat Aspose.Cells k ovládání faktoru přiblížení listu pomocí zdrojového kódu C# krok za krokem.

## Krok 1: Importujte požadované knihovny

Než začnete, ujistěte se, že máte nainstalovanou knihovnu Aspose.Cells pro .NET a importujte potřebné knihovny do svého projektu C#.

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## Krok 2: Nastavte cestu k adresáři a otevřete soubor Excel

 Chcete-li začít, nastavte cestu k adresáři obsahujícímu váš soubor Excel a poté jej otevřete pomocí a`FileStream` objekt a instanci a`Workbook` objekt, který bude reprezentovat sešit aplikace Excel.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Krok 3: Otevřete tabulku a změňte faktor přiblížení

 tomto kroku přistupujeme k prvnímu listu excelového sešitu pomocí indexu`0` a nastavte faktor přiblížení listu na`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## Krok 4: Uložte změny a zavřete soubor

 Jakmile změníme faktor přiblížení listu, uložíme změny do souboru aplikace Excel pomocí`Save` metoda`Workbook` objekt. Poté stream souborů zavřeme, aby se uvolnily všechny použité zdroje.

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### Ukázka zdrojového kódu pro Controll Zoom Factor Of Worksheet pomocí Aspose.Cells pro .NET 

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
// Nastavení faktoru přiblížení listu na 75
worksheet.Zoom = 75;
// Uložení upraveného souboru Excel
workbook.Save(dataDir + "output.xls");
// Zavřením datového proudu souborů uvolníte všechny zdroje
fstream.Close();
```

## Závěr

Tento podrobný průvodce vám ukázal, jak ovládat faktor přiblížení listu pomocí Aspose.Cells pro .NET. Pomocí dodaného zdrojového kódu C# můžete snadno upravit faktor přiblížení listu ve vašich aplikacích .NET.

### Často kladené otázky (FAQ)

#### Co je Aspose.Cells pro .NET?

Aspose.Cells for .NET je knihovna souborů s bohatými funkcemi pro manipulaci se soubory aplikace Excel v aplikacích .NET.

#### Jak mohu nainstalovat Aspose.Cells pro .NET?

 Chcete-li nainstalovat Aspose.Cells for .NET, musíte si stáhnout odpovídající balíček NuGet z[Aspose Releases](https://releases/aspose.com/cells/net/) a přidejte jej do svého projektu .NET.

#### Jaké funkce nabízí Aspose.Cells for .NET?

Aspose.Cells for .NET nabízí funkce, jako je vytváření, úpravy, konverze a pokročilá manipulace se soubory aplikace Excel.

#### Jaké formáty souborů podporuje Aspose.Cells for .NET?

Aspose.Cells for .NET podporuje více formátů souborů včetně XLSX, XLSM, CSV, HTML, PDF a mnoha dalších.
