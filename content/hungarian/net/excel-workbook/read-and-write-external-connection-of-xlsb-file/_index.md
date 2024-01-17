---
title: Az XLSB fájl külső kapcsolatának olvasása és írása
linktitle: Az XLSB fájl külső kapcsolatának olvasása és írása
second_title: Aspose.Cells for .NET API Reference
description: Ismerje meg, hogyan olvashatja és módosíthatja az XLSB-fájlok külső kapcsolatait az Aspose.Cells for .NET segítségével.
type: docs
weight: 130
url: /hu/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
A külső kapcsolatok olvasása és írása XLSB-fájlba elengedhetetlen a külső forrásokból származó adatok kezeléséhez az Excel-munkafüzetekben. Az Aspose.Cells for .NET segítségével könnyen olvashat és írhat külső kapcsolatokat a következő lépésekkel:

## 1. lépés: Adja meg a forráskönyvtárat és a kimeneti könyvtárat

Először is meg kell adni a forráskönyvtárat, ahol a külső kapcsolatot tartalmazó XLSB fájl található, valamint azt a kimeneti könyvtárat, ahová a módosított fájlt menteni kívánja. A következőképpen teheti meg az Aspose.Cells használatával:

```csharp
// forráskönyvtár
string sourceDir = RunExamples.Get_SourceDirectory();

// Kimeneti könyvtár
string outputDir = RunExamples.Get_OutputDirectory();
```

## 2. lépés: Töltse be a forrás Excel XLSB fájlt

Ezután be kell töltenie azt a forrás Excel XLSB fájlt, amelyen a külső kapcsolat olvasási és írási műveleteit kívánja végrehajtani. Itt van egy minta kód:

```csharp
// Töltse be a forrás Excel XLSB fájlt
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## 3. lépés: Olvassa el és módosítsa a külső csatlakozást

fájl betöltése után elérheti az első külső kapcsolatot, amely valójában egy adatbázis-kapcsolat. A külső kapcsolat különféle tulajdonságait olvashatja és módosíthatja. Itt van, hogyan:

```csharp
// Olvassa el az első külső kapcsolatot, amely adatbázis-kapcsolat
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Jelenítse meg az adatbázis-kapcsolat nevét, a parancsot és a csatlakozási információkat
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Módosítsa a kapcsolat nevét
dbCon.Name = "NewCustomer";
```

## 4. lépés: Mentse el a kimeneti Excel XLSB fájlt

A szükséges módosítások elvégzése után a módosított Excel XLSB fájlt elmentheti a megadott kimeneti könyvtárba. Íme, hogyan kell csinálni:

```csharp
// Mentse el a kimeneti Excel XLSB fájlt
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Minta forráskód az XLSB-fájlok olvasási és írási külső kapcsolatához az Aspose.Cells for .NET használatával 
```csharp
//Forrás könyvtár
string sourceDir = RunExamples.Get_SourceDirectory();
//Kimeneti könyvtár
string outputDir = RunExamples.Get_OutputDirectory();
//Töltse be a forrás Excel Xlsb fájlt
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Olvassa el az első külső kapcsolatot, amely valójában egy DB-kapcsolat
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Nyomtassa ki a DB-Connection nevét, parancsát és csatlakozási adatait
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Módosítsa a kapcsolat nevét
dbCon.Name = "NewCust";
//Mentse el az Excel Xlsb fájlt
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Következtetés

külső kapcsolatok olvasása és írása XLSB-fájlba lehetővé teszi az Excel-munkafüzetekben lévő külső forrásokból származó adatok kezelését. Az Aspose.Cells for .NET segítségével könnyen elérheti a külső kapcsolatokat, elolvashatja és módosíthatja a kapcsolati információkat, valamint mentheti a változtatásokat. Kísérletezzen saját XLSB-fájljaival, és használja ki a külső kapcsolatok erejét Excel-alkalmazásaiban.

### GYIK

#### K: Mi az a külső kapcsolat egy XLSB fájlban?
    
V: Az XLSB-fájlban lévő külső kapcsolat külső adatforrással, például adatbázissal létrehozott kapcsolatra utal. Lehetővé teszi adatok importálását ebből a külső forrásból az Excel-munkafüzetbe.

#### K: Lehet több külső kapcsolat is egy XLSB fájlban?
     
V: Igen, egy XLSB-fájlban több külső kapcsolat is lehet. Egyenként kezelheti őket az egyes kapcsolati objektumok elérésével.

#### K: Hogyan olvashatom ki a külső kapcsolat részleteit egy XLSB fájlban az Aspose.Cells segítségével?
     
V: Az Aspose.Cells által biztosított funkciók segítségével hozzáférhet egy külső kapcsolat tulajdonságaihoz, például a kapcsolatnévhez, a társított parancshoz és a csatlakozási információkhoz.

#### K: Módosítható egy külső kapcsolat egy XLSB fájlban az Aspose.Cells segítségével?
     
V: Igen, módosíthatja a külső kapcsolat tulajdonságait, például a kapcsolat nevét, hogy megfeleljen sajátos igényeinek. Az Aspose.Cells módszereket biztosít ezeknek a módosításoknak a végrehajtására.

#### K: Hogyan menthetem el a külső kapcsolaton végrehajtott módosításokat XLSB-fájlba az Aspose.Cells segítségével?
     
V: Miután elvégezte a szükséges módosításokat egy külső kapcsolaton, egyszerűen elmentheti a módosított Excel XLSB fájlt az Aspose.Cells által biztosított megfelelő módszerrel.