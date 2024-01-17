---
title: Zkopírujte nastavení stránky z jiného listu
linktitle: Zkopírujte nastavení stránky z jiného listu
second_title: Aspose.Cells for .NET API Reference
description: Naučte se kopírovat nastavení konfigurace stránky z jedné tabulky do druhé pomocí Aspose.Cells for .NET. Podrobný průvodce optimalizací použití této knihovny.
type: docs
weight: 10
url: /cs/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
V tomto článku vás krok za krokem provedeme vysvětlením následujícího zdrojového kódu C#: Zkopírujte nastavení konfigurace stránky z jiné tabulky pomocí Aspose.Cells for .NET. K provedení této operace použijeme knihovnu Aspose.Cells pro .NET. Chcete-li zkopírovat nastavení nastavení stránky z jednoho listu do druhého, postupujte podle následujících kroků.

## Krok 1: Vytvoření sešitu
Prvním krokem je vytvoření sešitu. V našem případě použijeme třídu Workbook poskytovanou knihovnou Aspose.Cells. Zde je kód pro vytvoření sešitu:

```csharp
Workbook wb = new Workbook();
```

## Krok 2: Přidání testovacích listů
Po vytvoření sešitu musíme přidat testovací listy. V tomto příkladu přidáme dva pracovní listy. Zde je kód pro přidání dvou pracovních listů:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Krok 3: Přístup k pracovním listům
Nyní, když jsme přidali listy, potřebujeme k nim mít přístup, abychom mohli změnit jejich nastavení. K pracovním listům "TestSheet1" a "TestSheet2" přistoupíme pomocí jejich názvů. Zde je kód pro přístup:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Krok 4: Nastavení velikosti papíru
 V tomto kroku nastavíme velikost papíru listu "TestSheet1". Budeme používat`PageSetup.PaperSize` vlastnost pro nastavení velikosti papíru. Například nastavíme velikost papíru na "PaperA3ExtraTransverse". Zde je kód pro to:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Krok 5: Kopírování nastavení stránky
Nyní zkopírujeme nastavení konfigurace stránky z listu "TestSheet1" do "TestSheet2". Budeme používat`PageSetup.Copy` způsob provedení této operace. Zde je kód pro to:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Krok 6: Tisk velikostí papíru
 Po zkopírování nastavení stránky vytiskneme velikosti papíru dvou listů. budeme používat`Console.WriteLine` pro zobrazení velikostí papíru. Zde je kód pro to:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Ukázkový zdrojový kód pro kopírování nastavení nastavení stránky z jiného listu pomocí Aspose.Cells pro .NET 
```csharp
//Vytvořte sešit
Workbook wb = new Workbook();
//Přidejte dva zkušební listy
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Přístup k oběma listům jako TestSheet1 a TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Nastavte Paper Size TestSheet1 na PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Vytiskněte velikost papíru obou listů
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Zkopírujte PageSetup z TestSheet1 do TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Vytiskněte velikost papíru obou listů
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Závěr
tomto článku jsme se naučili, jak kopírovat nastavení konfigurace stránky z jednoho listu do druhého pomocí Aspose.Cells for .NET. Prošli jsme následujícími kroky: vytvoření sešitu, přidání zkušebních listů, přístup k listům, nastavení velikosti papíru, zkopírování nastavení nastavení stránky a tisk velikostí papíru. Nyní můžete tyto znalosti využít ke kopírování nastavení konfigurace stránky do svých vlastních projektů.

### Nejčastější dotazy

#### Otázka: Mohu kopírovat nastavení konfigurace stránky mezi různými instancemi sešitu?

 Odpověď: Ano, můžete kopírovat nastavení nastavení stránky mezi různými instancemi sešitu pomocí`PageSetup.Copy` metoda knihovny Aspose.Cells.

#### Otázka: Mohu zkopírovat další nastavení stránky, jako je orientace nebo okraje?

 Odpověď: Ano, další nastavení nastavení stránky můžete zkopírovat pomocí`PageSetup.Copy` metoda s příslušnými možnostmi. Orientaci můžete kopírovat například pomocí`CopyOptions.Orientation` a pomocí okrajů`CopyOptions.Margins`.

#### Otázka: Jak zjistím, jaké možnosti jsou k dispozici pro velikost papíru?

Odpověď: Dostupné možnosti velikosti papíru naleznete v Referenční příručce API knihovny Aspose.Cells. Existuje výčet nazvaný`PaperSizeType` který uvádí různé podporované velikosti papíru.

#### Otázka: Jak si mohu stáhnout knihovnu Aspose.Cells pro .NET?

 A: Knihovnu Aspose.Cells pro .NET si můžete stáhnout z[Aspose Releases](https://releases.aspose.com/cells/net). K dispozici jsou bezplatné zkušební verze a také placené licence pro komerční použití.

#### Otázka: Podporuje knihovna Aspose.Cells další programovací jazyky?

Odpověď: Ano, knihovna Aspose.Cells podporuje více programovacích jazyků včetně C#, Java, Python a mnoha dalších.