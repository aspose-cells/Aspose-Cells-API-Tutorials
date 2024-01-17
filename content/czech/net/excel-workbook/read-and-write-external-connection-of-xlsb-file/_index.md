---
title: Čtení a zápis externího připojení souboru XLSB
linktitle: Čtení a zápis externího připojení souboru XLSB
second_title: Aspose.Cells for .NET API Reference
description: Naučte se číst a upravovat externí připojení souboru XLSB pomocí Aspose.Cells for .NET.
type: docs
weight: 130
url: /cs/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Čtení a zápis externích připojení do souboru XLSB je nezbytný pro manipulaci s daty z externích zdrojů v sešitech aplikace Excel. S Aspose.Cells for .NET můžete snadno číst a zapisovat externí připojení pomocí následujících kroků:

## Krok 1: Zadejte zdrojový adresář a výstupní adresář

Nejprve musíte zadat zdrojový adresář, kde se nachází soubor XLSB obsahující externí připojení, a také výstupní adresář, kam chcete upravený soubor uložit. Zde je návod, jak to udělat pomocí Aspose.Cells:

```csharp
// zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();

// Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
```

## Krok 2: Načtěte zdrojový soubor Excel XLSB

Dále je třeba načíst zdrojový soubor Excel XLSB, na kterém chcete provádět operace čtení a zápisu externího připojení. Zde je ukázkový kód:

```csharp
// Načtěte zdrojový soubor Excel XLSB
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Krok 3: Přečtěte si a upravte externí připojení

Po načtení souboru můžete přistupovat k prvnímu externímu připojení, které je ve skutečnosti připojení k databázi. Můžete číst a upravovat různé vlastnosti externího připojení. Zde je postup:

```csharp
// Přečtěte si první externí připojení, což je připojení k databázi
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Zobrazte název připojení k databázi, příkaz a informace o připojení
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Upravte název připojení
dbCon.Name = "NewCustomer";
```

## Krok 4: Uložte výstupní soubor Excel XLSB

Jakmile provedete potřebné změny, můžete upravený soubor Excel XLSB uložit do určeného výstupního adresáře. Jak na to:

```csharp
// Uložte výstupní soubor Excel XLSB
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Ukázka zdrojového kódu pro čtení a zápis externího připojení souboru XLSB pomocí Aspose.Cells pro .NET 
```csharp
//Zdrojový adresář
string sourceDir = RunExamples.Get_SourceDirectory();
//Výstupní adresář
string outputDir = RunExamples.Get_OutputDirectory();
//Načtěte zdrojový soubor Excel Xlsb
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Přečtěte si první externí připojení, které je ve skutečnosti DB-Connection
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Vytiskněte název, příkaz a informace o připojení DB-Connection
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Upravte název připojení
dbCon.Name = "NewCust";
//Uložte soubor Excel Xlsb
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Závěr

Čtení a zápis externích připojení do souboru XLSB vám umožňuje manipulovat s daty z externích zdrojů v sešitech aplikace Excel. S Aspose.Cells for .NET můžete snadno přistupovat k externím připojením, číst a upravovat informace o připojení a ukládat změny. Experimentujte se svými vlastními soubory XLSB a využijte výkon externích připojení ve svých aplikacích Excel.

### Nejčastější dotazy

#### Otázka: Co je externí připojení v souboru XLSB?
    
Odpověď: Externí připojení v souboru XLSB odkazuje na připojení vytvořené s externím zdrojem dat, jako je databáze. Umožňuje importovat data z tohoto externího zdroje do sešitu aplikace Excel.

#### Otázka: Mohu mít v souboru XLSB více externích připojení?
     
Odpověď: Ano, v souboru XLSB můžete mít více externích připojení. Můžete je spravovat jednotlivě přístupem ke každému objektu připojení.

#### Otázka: Jak mohu číst podrobnosti o externím připojení v souboru XLSB pomocí Aspose.Cells?
     
Odpověď: Funkci poskytovanou Aspose.Cells můžete použít k přístupu k vlastnostem externího připojení, jako je název připojení, přidružený příkaz a informace o připojení.

#### Otázka: Je možné upravit externí připojení v souboru XLSB pomocí Aspose.Cells?
     
Odpověď: Ano, vlastnosti externího připojení, jako je název připojení, můžete upravit tak, aby vyhovovaly vašim specifickým potřebám. Aspose.Cells poskytuje metody k provedení těchto změn.

#### Otázka: Jak mohu uložit změny provedené v externím připojení do souboru XLSB pomocí Aspose.Cells?
     
Odpověď: Jakmile provedete nezbytné změny externího připojení, můžete jednoduše uložit upravený soubor Excel XLSB pomocí vhodné metody poskytované Aspose.Cells.