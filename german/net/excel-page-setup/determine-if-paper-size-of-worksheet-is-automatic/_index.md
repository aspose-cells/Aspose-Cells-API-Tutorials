---
title: Stellen Sie fest, ob die Papiergröße des Arbeitsblatts automatisch eingestellt wird
linktitle: Stellen Sie fest, ob die Papiergröße des Arbeitsblatts automatisch eingestellt wird
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET feststellen können, ob die Papiergröße einer Tabelle automatisch eingestellt wird.
type: docs
weight: 20
url: /de/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
In diesem Artikel erklären wir Ihnen Schritt für Schritt den folgenden C#-Quellcode: Bestimmen Sie mithilfe von Aspose.Cells für .NET, ob die Papiergröße eines Arbeitsblatts automatisch eingestellt wird. Wir werden die Aspose.Cells-Bibliothek für .NET verwenden, um diesen Vorgang auszuführen. Führen Sie die folgenden Schritte aus, um festzustellen, ob das Papierformat eines Arbeitsblatts automatisch eingestellt wird.

## Schritt 1: Arbeitsmappen laden
Der erste Schritt besteht darin, die Arbeitsmappen zu laden. Wir werden zwei Arbeitsmappen haben: eine mit deaktivierter automatischer Papiergröße und die andere mit aktivierter automatischer Papiergröße. Hier ist der Code zum Laden der Arbeitsmappen:

```csharp
// Quellverzeichnis
string sourceDir = "YOUR_SOURCE_DIR";
// Ausgabe Verzeichnis
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Laden Sie die erste Arbeitsmappe mit deaktivierter automatischer Papiergröße
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Laden Sie die zweite Arbeitsmappe mit aktivierter automatischer Papiergröße
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Schritt 2: Zugriff auf Tabellenkalkulationen
Nachdem wir die Arbeitsmappen geladen haben, müssen wir auf die Arbeitsblätter zugreifen, damit wir das automatische Papierformat überprüfen können. Wir gehen zum ersten Arbeitsblatt der beiden Arbeitsmappen. Hier ist der Code für den Zugriff:

```csharp
//Gehen Sie zum ersten Arbeitsblatt der ersten Arbeitsmappe
Worksheet ws11 = wb1.Worksheets[0];

// Gehen Sie zum ersten Arbeitsblatt der zweiten Arbeitsmappe
Worksheet ws12 = wb2.Worksheets[0];
```

## Schritt 3: Überprüfen Sie das automatische Papierformat
 In diesem Schritt prüfen wir, ob die Papiergröße des Arbeitsblatts automatisch eingestellt wird. Wir werden das verwenden`PageSetup.IsAutomaticPaperSize` Eigenschaft, um diese Informationen zu erhalten. Wir zeigen Ihnen dann das Ergebnis an. Hier ist der Code dafür:

```csharp
// Zeigen Sie die IsAutomaticPaperSize-Eigenschaft des ersten Arbeitsblatts in der ersten Arbeitsmappe an
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Zeigen Sie die IsAutomaticPaperSize-Eigenschaft des ersten Arbeitsblatts in der zweiten Arbeitsmappe an
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Beispielquellcode für „Bestimmen, ob die Papiergröße des Arbeitsblatts automatisch ist“ mithilfe von Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Ausgabe Verzeichnis
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Laden Sie die erste Arbeitsmappe mit der automatischen Papiergröße „Falsch“.
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Laden Sie die zweite Arbeitsmappe mit der automatischen Papiergröße True
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Greifen Sie auf das erste Arbeitsblatt beider Arbeitsmappen zu
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Drucken Sie die PageSetup.IsAutomaticPaperSize-Eigenschaft beider Arbeitsblätter
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Abschluss
In diesem Artikel haben wir erfahren, wie Sie mithilfe von Aspose.Cells für .NET feststellen können, ob die Papiergröße eines Arbeitsblatts automatisch erfolgt. Wir haben die folgenden Schritte ausgeführt: Laden der Arbeitsmappen,

Zugriff auf Tabellenkalkulationen und automatische Überprüfung der Papiergröße. Jetzt können Sie dieses Wissen nutzen, um festzustellen, ob die Papiergröße Ihrer Tabellenkalkulationen automatisch erfolgt.

### FAQs

F: Wie kann ich Arbeitsmappen mit Aspose.Cells für .NET laden?
A: Sie können Arbeitsmappen mit der Workbook-Klasse aus der Aspose.Cells-Bibliothek laden. Verwenden Sie die Workbook.Load-Methode, um eine Arbeitsmappe aus einer Datei zu laden.

F: Kann ich das automatische Papierformat für andere Tabellenkalkulationen überprüfen?
A: Ja, Sie können die automatische Papiergröße für jedes Arbeitsblatt überprüfen, indem Sie auf die PageSetup.IsAutomaticPaperSize-Eigenschaft des entsprechenden Worksheet-Objekts zugreifen.

F: Wie kann ich das automatische Papierformat einer Tabellenkalkulation ändern?
A: Um die automatische Papiergröße eines Arbeitsblatts zu ändern, können Sie die Eigenschaft PageSetup.IsAutomaticPaperSize verwenden und sie auf den gewünschten Wert (wahr oder falsch) setzen.

F: Welche weiteren Funktionen bietet Aspose.Cells für .NET?
A: Aspose.Cells für .NET bietet viele Funktionen für die Arbeit mit Tabellenkalkulationen, z. B. das Erstellen, Ändern und Konvertieren von Arbeitsmappen sowie das Bearbeiten von Daten, Formeln und Formatierungen.