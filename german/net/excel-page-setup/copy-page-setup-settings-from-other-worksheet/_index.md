---
title: Kopieren Sie die Seiteneinrichtungseinstellungen von einem anderen Arbeitsblatt
linktitle: Kopieren Sie die Seiteneinrichtungseinstellungen von einem anderen Arbeitsblatt
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET Seitenkonfigurationseinstellungen von einer Tabelle in eine andere kopieren. Eine Schritt-für-Schritt-Anleitung zur Optimierung der Nutzung dieser Bibliothek.
type: docs
weight: 10
url: /de/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
In diesem Artikel erklären wir Ihnen Schritt für Schritt den folgenden C#-Quellcode: Kopieren Sie Seitenkonfigurationseinstellungen aus einer anderen Tabelle mit Aspose.Cells für .NET. Wir werden die Aspose.Cells-Bibliothek für .NET verwenden, um diesen Vorgang auszuführen. Wenn Sie Seiteneinrichtungseinstellungen von einem Arbeitsblatt in ein anderes kopieren möchten, führen Sie die folgenden Schritte aus.

## Schritt 1: Erstellen der Arbeitsmappe
Der erste Schritt besteht darin, eine Arbeitsmappe zu erstellen. In unserem Fall verwenden wir die Workbook-Klasse, die von der Aspose.Cells-Bibliothek bereitgestellt wird. Hier ist der Code zum Erstellen einer Arbeitsmappe:

```csharp
Workbook wb = new Workbook();
```

## Schritt 2: Testarbeitsblätter hinzufügen
Nachdem wir die Arbeitsmappe erstellt haben, müssen wir Testarbeitsblätter hinzufügen. In diesem Beispiel fügen wir zwei Arbeitsblätter hinzu. Hier ist der Code zum Hinzufügen von zwei Arbeitsblättern:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Schritt 3: Zugriff auf Arbeitsblätter
Nachdem wir die Arbeitsblätter hinzugefügt haben, müssen wir auf sie zugreifen, um ihre Einstellungen ändern zu können. Wir greifen über deren Namen auf die Arbeitsblätter „TestSheet1“ und „TestSheet2“ zu. Hier ist der Code für den Zugriff:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Schritt 4: Papierformat einstellen
 In diesem Schritt legen wir das Papierformat des Arbeitsblatts „TestSheet1“ fest. Wir werden das verwenden`PageSetup.PaperSize` Eigenschaft, um das Papierformat festzulegen. Beispielsweise stellen wir das Papierformat auf „PaperA3ExtraTransverse“ ein. Hier ist der Code dafür:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Schritt 5: Kopieren der Seiteneinrichtungseinstellungen
Jetzt kopieren wir die Seitenkonfigurationseinstellungen vom Arbeitsblatt „TestSheet1“ nach „TestSheet2“. Wir werden das verwenden`PageSetup.Copy` Methode zum Ausführen dieser Operation. Hier ist der Code dafür:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Schritt 6: Papierformate drucken
 Nach dem Kopieren der Seiteneinrichtungseinstellungen drucken wir die Papierformate der beiden Arbeitsblätter. Wir werden verwenden`Console.WriteLine` um die Papierformate anzuzeigen. Hier ist der Code dafür:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Beispielquellcode zum Kopieren von Seiteneinrichtungseinstellungen aus einem anderen Arbeitsblatt mit Aspose.Cells für .NET 
```csharp
//Arbeitsmappe erstellen
Workbook wb = new Workbook();
//Fügen Sie zwei Testarbeitsblätter hinzu
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Greifen Sie auf beide Arbeitsblätter als TestSheet1 und TestSheet2 zu
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Legen Sie das Papierformat von TestSheet1 auf PaperA3ExtraTransverse fest
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Drucken Sie das Papierformat beider Arbeitsblätter aus
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Kopieren Sie das PageSetup von TestSheet1 nach TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Drucken Sie das Papierformat beider Arbeitsblätter aus
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Abschluss
In diesem Artikel haben wir gelernt, wie man mit Aspose.Cells für .NET Seitenkonfigurationseinstellungen von einem Arbeitsblatt in ein anderes kopiert. Wir haben die folgenden Schritte durchlaufen: Arbeitsmappe erstellen, Testarbeitsblätter hinzufügen, auf die Arbeitsblätter zugreifen, Papierformat festlegen, Seiteneinrichtungseinstellungen kopieren und Papierformate drucken. Jetzt können Sie dieses Wissen nutzen, um Seitenkonfigurationseinstellungen in Ihre eigenen Projekte zu kopieren.

### FAQs

#### F: Kann ich Seitenkonfigurationseinstellungen zwischen verschiedenen Arbeitsmappeninstanzen kopieren?

 A: Ja, Sie können Seiteneinrichtungseinstellungen zwischen verschiedenen Arbeitsmappeninstanzen kopieren`PageSetup.Copy` Methode der Aspose.Cells-Bibliothek.

#### F: Kann ich andere Seiteneinrichtungseinstellungen kopieren, z. B. Ausrichtung oder Ränder?

 A: Ja, Sie können andere Seiteneinrichtungseinstellungen mit kopieren`PageSetup.Copy` Methode mit den entsprechenden Optionen. Beispielsweise können Sie die Ausrichtung mit kopieren`CopyOptions.Orientation` und Ränder verwenden`CopyOptions.Margins`.

#### F: Woher weiß ich, welche Optionen für das Papierformat verfügbar sind?

A: Sie können in der API-Referenz der Aspose.Cells-Bibliothek nach verfügbaren Optionen für das Papierformat suchen. Es gibt eine Enumeration namens`PaperSizeType` Hier sind die verschiedenen unterstützten Papierformate aufgeführt.

#### F: Wie kann ich die Aspose.Cells-Bibliothek für .NET herunterladen?

 A: Sie können die Aspose.Cells-Bibliothek für .NET unter herunterladen[Aspose-Veröffentlichungen](https://releases.aspose.com/cells/net). Es stehen kostenlose Testversionen sowie kostenpflichtige Lizenzen für die kommerzielle Nutzung zur Verfügung.

#### F: Unterstützt die Aspose.Cells-Bibliothek andere Programmiersprachen?

A: Ja, die Aspose.Cells-Bibliothek unterstützt mehrere Programmiersprachen, darunter C#, Java, Python und viele mehr.