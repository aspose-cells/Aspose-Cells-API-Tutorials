---
title: Stoppa konvertering eller laddning med Interrupt Monitor
linktitle: Stoppa konvertering eller laddning med Interrupt Monitor
second_title: Aspose.Cells .NET Excel Processing API
description: Lär dig att stoppa konvertering av arbetsbok i Aspose.Cells för .NET med Interrupt Monitor, med detaljerad, steg-för-steg handledning.
type: docs
weight: 26
url: /sv/net/workbook-operations/stop-conversion-or-loading/
---
## Introduktion
Att arbeta med stora Excel-filer innebär ofta långa processer som kan äta upp tid och resurser. Men tänk om du kunde stoppa konverteringsprocessen halvvägs när du inser att något behöver förändras? Aspose.Cells för .NET har en funktion som kallas Interrupt Monitor, som låter dig avbryta en arbetsboks konvertering till ett annat format som PDF. Detta kan vara en livräddare, särskilt när du arbetar med betydande datafiler. I den här guiden går vi igenom hur du avbryter konverteringsprocessen med hjälp av Interrupt Monitor i Aspose.Cells för .NET.
## Förutsättningar
Innan du dyker in, se till att du har följande på plats:
1.  Aspose.Cells för .NET - Ladda ner det[här](https://releases.aspose.com/cells/net/).
2. .NET-utvecklingsmiljö - Som Visual Studio.
3. Grundläggande kunskaper om C#-programmering - Bekantskap med C#-syntax hjälper dig att följa med.
## Importera paket
För att börja, låt oss importera de nödvändiga paketen. Dessa importer inkluderar:
- Aspose.Cells: Huvudbiblioteket för att manipulera Excel-filer.
- System.Threading: För att hantera trådar, eftersom detta exempel kommer att köra två parallella processer.
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using System.IO;
```
Låt oss dela upp processen i detaljerade steg. Varje steg hjälper dig att förstå vikten av att ställa in och använda Interrupt Monitor för att hantera Excel-arbetsbokkonvertering.
## Steg 1: Skapa Class and Set Output Directory
Först behöver vi en klass för att kapsla in våra funktioner, tillsammans med en katalog där utdatafilen kommer att sparas.
```csharp
class StopConversionOrLoadingUsingInterruptMonitor
{
    static string outputDir = "Your Document Directory";
}
```
 Ersätta`"Your Document Directory"` med den faktiska sökvägen där du vill att PDF-filen ska sparas.
## Steg 2: Instantiera avbrottsmonitorn
Skapa sedan ett InterruptMonitor-objekt. Denna monitor hjälper till att kontrollera processen genom att ställa in möjligheten att avbryta den vid en given punkt.
```csharp
InterruptMonitor im = new InterruptMonitor();
```
Denna avbrottsmonitor kommer att bifogas vår arbetsbok, så att vi kan hantera konverteringsprocessen.
## Steg 3: Ställ in arbetsboken för konvertering
Låt oss nu skapa ett arbetsboksobjekt, tilldela InterruptMonitor till det och sedan gå till det första kalkylbladet för att infoga lite exempeltext.
```csharp
void CreateWorkbookAndConvertItToPdfFormat()
{
    Workbook wb = new Workbook();
    wb.InterruptMonitor = im;
    Worksheet ws = wb.Worksheets[0];
    Cell cell = ws.Cells["J1000000"];
    cell.PutValue("This is text.");
}
```
Koden ovan skapar en arbetsbok, ställer in InterruptMonitor för den och placerar text i en avlägsen cell (`J1000000`). Genom att placera text i denna cellposition säkerställs att bearbetningen av arbetsboken blir mer tidskrävande, vilket ger InterruptMonitor tillräckligt med tid att ingripa.
## Steg 4: Spara arbetsboken som PDF och hantera avbrott
 Låt oss nu försöka spara arbetsboken som en PDF. Vi använder en`try-catch` blockera för att hantera eventuella avbrott som kan uppstå.
```csharp
try
{
    wb.Save(outputDir + "output_InterruptMonitor.pdf");
}
catch (Aspose.Cells.CellsException ex)
{
    Console.WriteLine("Process Interrupted - Message: " + ex.Message);
}
```
Om processen avbryts kommer undantaget att fånga det och visa ett lämpligt meddelande. Annars sparas arbetsboken som en PDF.
## Steg 5: Avbryt konverteringsprocessen
 Huvudfunktionen här är möjligheten att avbryta processen. Vi lägger till en fördröjning med hjälp av`Thread.Sleep` och ring sedan`Interrupt()` metod för att stoppa konverteringen efter 10 sekunder.
```csharp
void WaitForWhileAndThenInterrupt()
{
    Thread.Sleep(1000 * 10);
    im.Interrupt();
}
```
Denna fördröjning ger arbetsboken tid att börja konvertera till PDF innan avbrottssignalen skickas.
## Steg 6: Kör trådarna samtidigt
För att få ihop allt måste vi starta båda funktionerna i separata trådar. På så sätt kan arbetsbokskonverteringen och avbrottsväntningen ske samtidigt.
```csharp
public void TestRun()
{
    ThreadStart ts1 = new ThreadStart(this.CreateWorkbookAndConvertItToPdfFormat);
    Thread t1 = new Thread(ts1);
    t1.Start();
    ThreadStart ts2 = new ThreadStart(this.WaitForWhileAndThenInterrupt);
    Thread t2 = new Thread(ts2);
    t2.Start();
    t1.Join();
    t2.Join();
}
```
 Koden ovan körs`CreateWorkbookAndConvertItToPdfFormat` och`WaitForWhileAndThenInterrupt` i parallella trådar, förenar dem när båda processerna har avslutats.
## Steg 7: Slutlig exekvering
 Slutligen lägger vi till en`Run()` metod för att exekvera koden.
```csharp
public static void Run()
{
    new StopConversionOrLoadingUsingInterruptMonitor().TestRun();
    Console.WriteLine("StopConversionOrLoadingUsingInterruptMonitor executed successfully.");
}
```
 Detta`Run` metoden är startpunkten för att starta och observera avbrottet i aktion.
## Slutsats
I den här handledningen undersökte vi hur man avbryter konverteringsprocessen i Aspose.Cells för .NET. Interrupt Monitor är ett användbart verktyg när du arbetar med stora Excel-filer, vilket gör att du kan stoppa processer utan att vänta på att de ska slutföras. Detta är särskilt användbart i scenarier där tid och resurser är värdefulla och snabb feedback behövs.
## FAQ's
### Vad är en avbrottsövervakning i Aspose.Cells för .NET?  
Avbrottsövervakningen låter dig stoppa en arbetsbokskonvertering eller laddningsprocess halvvägs.
### Kan jag använda Interrupt Monitor för andra format än PDF?  
Ja, du kan avbryta konverteringar till andra format som stöds också.
### Hur påverkar Thread.Sleep() tidpunkten för avbrott?  
Thread.Sleep() skapar en fördröjning innan avbrottet utlöses, vilket ger tid för konverteringen att starta.
### Kan jag avbryta processen innan 10 sekunder?  
 Ja, ändra fördröjningen`WaitForWhileAndThenInterrupt()` till kortare tid.
### Kommer avbrottsprocessen att påverka prestandan?  
Effekten är minimal och det är mycket fördelaktigt för att hantera långvariga processer.
 För mer information, se[Aspose.Cells för .NET-dokumentation](https://reference.aspose.com/cells/net/) . Om du behöver hjälp, kolla in[Supportforum](https://forum.aspose.com/c/cells/9)eller skaffa en[Gratis provperiod](https://releases.aspose.com/).