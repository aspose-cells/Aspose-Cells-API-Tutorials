---
title: Vložit obrázek do záhlaví, zápatí
linktitle: Vložit obrázek do záhlaví, zápatí
second_title: Aspose.Cells for .NET API Reference
description: Naučte se vložit obrázek do záhlaví nebo zápatí dokumentu aplikace Excel pomocí Aspose.Cells for .NET. Průvodce krok za krokem se zdrojovým kódem v C#.
type: docs
weight: 60
url: /cs/net/excel-page-setup/insert-image-in-header-footer/
---
Možnost vložit obrázek do záhlaví nebo zápatí dokumentu aplikace Excel může být velmi užitečná pro přizpůsobení vašich sestav nebo přidání loga společnosti. V tomto článku vás krok za krokem provedeme vložením obrázku do záhlaví nebo zápatí dokumentu aplikace Excel pomocí Aspose.Cells for .NET. Naučíte se, jak toho dosáhnout pomocí zdrojového kódu C#.

## Krok 1: Nastavení prostředí

Než začnete, ujistěte se, že máte na svém počítači nainstalovaný Aspose.Cells for .NET. Vytvořte také nový projekt ve vámi preferovaném vývojovém prostředí.

## Krok 2: Importujte potřebné knihovny

Do souboru kódu importujte knihovny potřebné pro práci s Aspose.Cells. Zde je odpovídající kód:

```csharp
using Aspose.Cells;
```

## Krok 3: Nastavte adresář dokumentů

Nastavte adresář, kde se nachází Excelový dokument, se kterým chcete pracovat. K nastavení adresáře použijte následující kód:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Nezapomeňte zadat úplnou cestu k adresáři.

## Krok 4: Vytvoření objektu sešitu

Objekt Workbook představuje dokument Excel, se kterým budete pracovat. Můžete jej vytvořit pomocí následujícího kódu:

```csharp
Workbook workbook = new Workbook();
```

Tím se vytvoří nový prázdný objekt sešit.

## Krok 5: Uložení adresy URL obrázku

Definujte adresu URL nebo cestu k obrázku, který chcete vložit do záhlaví nebo zápatí. K uložení adresy URL obrázku použijte následující kód:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Ujistěte se, že zadaná cesta je správná a že obrázek v daném umístění existuje.

## Krok 6: Otevření souboru obrázku

K otevření souboru obrázku použijeme objekt FileStream a načteme binární data z obrázku. Zde je odpovídající kód:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Ujistěte se, že cesta k obrázku je správná a že máte správná oprávnění k přístupu k ní.

## Krok 7: Konfigurace PageSetup

Objekt PageSetup se používá k nastavení stránky dokumentu aplikace Excel včetně záhlaví a zápatí. Pomocí následujícího kódu získáte objekt PageSetup prvního listu:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

To vám umožní přístup k nastavení stránky pro první list v sešitu.

## Krok 8: Přidání obrázku do záhlaví

Pomocí metody SetHeaderPicture() objektu PageSetup nastavte obrázek do střední části záhlaví stránky. Zde je odpovídající kód:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Tím se do záhlaví stránky přidá zadaný obrázek.

## Krok 9: Přidání skriptu do záhlaví

Chcete-li přidat skript do záhlaví stránky, použijte metodu SetHeader() objektu PageSetup. Zde je odpovídající kód:

```csharp
pageSetup.SetHeader(1, "&G");
```

Tím se do záhlaví stránky přidá zadaný skript. V tomto příkladu skript "&G" zobrazuje číslo stránky.

## Krok 10: Přidejte název listu do záhlaví

Chcete-li zobrazit název listu v záhlaví stránky, použijte znovu metodu SetHeader() objektu PageSetup. Zde je odpovídající kód:

```csharp
pageSetup.SetHeader(2, "&A");
```

Tím se do záhlaví stránky přidá název listu. Skript "&A" se používá k reprezentaci názvu listu.

## Krok 11: Uložení sešitu

Chcete-li uložit změny do sešitu, použijte metodu Save() objektu Sešit. Zde je odpovídající kód:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Tím se sešit uloží se změnami do zadaného adresáře.

## Krok 12: Zavření FileStream

Po přečtení binárních dat z bitové kopie nezapomeňte zavřít FileStream, abyste uvolnili prostředky. K uzavření FileStream použijte následující kód:

```csharp
inFile.Close();
```

Nezapomeňte FileStreams vždy zavřít, když je skončíte.

### Ukázkový zdrojový kód pro vložení obrázku do záhlaví zápatí pomocí Aspose.Cells pro .NET 
```csharp
//Cesta k adresáři dokumentů.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Vytvoření objektu sešitu
Workbook workbook = new Workbook();
// Vytvoření proměnné řetězce pro uložení adresy URL loga/obrázku
string logo_url = dataDir + "aspose-logo.jpg";
// Deklarace objektu FileStream
FileStream inFile;
// Deklarace bajtového pole
byte[] binaryData;
// Vytvoření instance objektu FileStream pro otevření loga/obrázku ve streamu
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// Instantování bajtového pole velikosti objektu FileStream
binaryData = new Byte[inFile.Length];
// Čte blok bajtů z proudu a zapisuje data do dané vyrovnávací paměti nebo pole bajtů.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Vytvoření objektu PageSetup pro získání nastavení stránky prvního listu sešitu
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Nastavení loga/obrázku ve střední části záhlaví stránky
pageSetup.SetHeaderPicture(1, binaryData);
// Nastavení skriptu pro logo/obrázek
pageSetup.SetHeader(1, "&G");
// Nastavení názvu listu v pravé části záhlaví stránky se skriptem
pageSetup.SetHeader(2, "&A");
// Ukládání sešitu
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//Zavření objektu FileStream
inFile.Close();       
```
## Závěr

gratuluji! Nyní víte, jak vložit obrázek do záhlaví nebo zápatí dokumentu aplikace Excel pomocí Aspose.Cells for .NET. Tento kurz vás provede každým krokem procesu, od nastavení prostředí až po uložení upraveného sešitu. Nebojte se více experimentovat s funkcemi Aspose.Cells a vytvářet personalizované a profesionální dokumenty Excel.

### FAQ

#### Q1: Je možné vložit více obrázků do záhlaví nebo zápatí dokumentu aplikace Excel?

Odpověď 1: Ano, do záhlaví nebo zápatí dokumentu aplikace Excel můžete vložit více obrázků opakováním kroků 8 a 9 pro každý další obrázek.

#### Q2: Jaké formáty obrázků jsou podporovány pro vložení do záhlaví nebo zápatí?
A2: Aspose.Cells podporuje řadu běžných obrazových formátů, jako jsou JPEG, PNG, GIF, BMP atd.

#### Q3: Mohu dále upravit vzhled záhlaví nebo zápatí?

A3: Ano, můžete použít speciální skripty a kódy k dalšímu formátování a přizpůsobení vzhledu záhlaví nebo zápatí. Další informace o možnostech přizpůsobení naleznete v dokumentaci Aspose.Cells.

#### Q4: Funguje Aspose.Cells s různými verzemi aplikace Excel?

Odpověď 4: Ano, Aspose.Cells je kompatibilní s různými verzemi aplikace Excel včetně Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 a Excel 2019.

#### Q5: Je možné vkládat obrázky do jiných částí dokumentu aplikace Excel, jako jsou buňky nebo grafy?

Odpověď 5: Ano, Aspose.Cells poskytuje rozsáhlé funkce pro vkládání obrázků do různých částí dokumentu aplikace Excel, včetně buněk, grafů a nakreslených objektů.