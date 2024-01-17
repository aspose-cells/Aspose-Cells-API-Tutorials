---
title: Chraňte sešit Excel
linktitle: Chraňte sešit Excel
second_title: Aspose.Cells for .NET API Reference
description: V tomto tutoriálu zjistíte, jak chránit tabulku aplikace Excel pomocí Aspose.Cells pro .NET. Průvodce krok za krokem v C#.
type: docs
weight: 50
url: /cs/net/protect-excel-file/protect-excel-worksheet/
---
tomto tutoriálu se podíváme na zdrojový kód C#, který používá knihovnu Aspose.Cells k ochraně tabulky Excel. Projdeme si každý krok kódu a vysvětlíme, jak to funguje. Ujistěte se, že pečlivě dodržujete pokyny, abyste dosáhli požadovaných výsledků.

## Krok 1: Předpoklady

Než začnete, ujistěte se, že jste nainstalovali knihovnu Aspose.Cells pro .NET. Můžete jej získat z oficiálních stránek Aspose. Také se ujistěte, že máte nejnovější verzi sady Visual Studio nebo jiného vývojového prostředí C#.

## Krok 2: Importujte požadované jmenné prostory

Abychom mohli používat knihovnu Aspose.Cells, musíme do našeho kódu importovat potřebné jmenné prostory. Přidejte následující řádky na začátek zdrojového souboru C#:

```csharp
using Aspose.Cells;
using System.IO;
```

## Krok 3: Načtěte soubor Excel

V tomto kroku načteme soubor Excel, který chceme chránit. Ujistěte se, že jste zadali správnou cestu k adresáři obsahujícímu soubor aplikace Excel. K nahrání souboru použijte následující kód:

```csharp
// Cesta k adresáři dokumentů.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Vytvořte proud souborů obsahující soubor Excel, který chcete otevřít.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Vytvořte instanci objektu sešitu.
//Otevřete soubor aplikace Excel prostřednictvím streamu souborů.
Workbook excel = new Workbook(fstream);
```

 Nezapomeňte vyměnit`"YOUR_DOCUMENTS_DIR"` s příslušnou cestou k adresáři vašich dokumentů.

## Krok 4: Otevřete tabulku

Nyní, když jsme načetli soubor Excel, máme přístup k prvnímu listu. Pro přístup k prvnímu listu použijte následující kód:

```csharp
// Přístup k prvnímu listu v souboru Excel.
Worksheet worksheet = excel.Worksheets[0];
```

## Krok 5: Chraňte pracovní list

V tomto kroku ochráníme tabulku pomocí hesla. K ochraně tabulky použijte následující kód:

```csharp
// Chraňte list heslem.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 Nahradit`"YOUR_PASSWORD"` s heslem, které chcete použít k ochraně tabulky.

## Krok 6: Uložte upravený soubor Excel Nyní, když jsme ochránili

é tabulky, uložíme upravený soubor Excel ve výchozím formátu. K uložení souboru Excel použijte následující kód:

```csharp
// Uložte upravený soubor Excel ve výchozím formátu.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Ujistěte se, že jste zadali správnou cestu k uložení upraveného souboru Excel.

## Krok 7: Zavřete File Stream

Abychom uvolnili všechny prostředky, musíme zavřít proud souborů používaný k načtení souboru Excel. K uzavření datového proudu souboru použijte následující kód:

```csharp
// Zavřete datový proud souboru, abyste uvolnili všechny prostředky.
fstream.Close();
```

Nezapomeňte tento krok zahrnout na konec kódu.


### Ukázka zdrojového kódu pro Protect Excel Worksheet pomocí Aspose.Cells pro .NET 
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
// Ochrana listu heslem
worksheet.Protect(ProtectionType.All, "aspose", null);
// Uložení upraveného souboru Excel ve výchozím formátu
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// Zavřením datového proudu souborů uvolníte všechny zdroje
fstream.Close();
```

## Závěr

gratuluji! Nyní máte zdrojový kód C#, který vám umožňuje chránit tabulku aplikace Excel pomocí knihovny Aspose.Cells pro .NET. Ujistěte se, že pečlivě dodržujete kroky a přizpůsobte kód svým konkrétním potřebám.

### Často kladené otázky (FAQ)

#### Je možné chránit více listů v jednom souboru aplikace Excel?

Odpověď: Ano, můžete chránit více listů v jednom souboru aplikace Excel opakováním kroků 4-6 pro každý list.

#### Jak mohu určit konkrétní oprávnění pro oprávněné uživatele?

 Odpověď: Můžete použít další možnosti, které poskytuje`Protect`způsob, jak určit konkrétní oprávnění pro oprávněné uživatele. Další informace naleznete v dokumentaci Aspose.Cells.

#### Mohu chránit samotný soubor Excel heslem?

Odpověď: Ano, samotný soubor Excel můžete chránit heslem pomocí jiných metod poskytovaných knihovnou Aspose.Cells. Konkrétní příklady naleznete v dokumentaci.

#### Podporuje knihovna Aspose.Cells jiné formáty souborů Excel?

Odpověď: Ano, knihovna Aspose.Cells podporuje širokou škálu formátů souborů Excel, včetně XLSX, XLSM, XLSB, CSV atd.