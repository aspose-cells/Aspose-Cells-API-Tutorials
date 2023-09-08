---
title: Linktypen erkennen
linktitle: Linktypen erkennen
second_title: Aspose.Cells für .NET API-Referenz
description: Erkennen Sie Linktypen in einer Excel-Arbeitsmappe mit Aspose.Cells für .NET.
type: docs
weight: 80
url: /de/net/excel-workbook/detect-link-types/
---
In diesem Tutorial führen wir Sie Schritt für Schritt durch den bereitgestellten C#-Quellcode, der es Ihnen ermöglicht, Linktypen in einer Excel-Arbeitsmappe mithilfe von Aspose.Cells für .NET zu erkennen. Befolgen Sie die nachstehenden Schritte, um diesen Vorgang auszuführen.

## Schritt 1: Quellverzeichnis festlegen

```csharp
// Quellverzeichnis
string SourceDir = RunExamples.Get_SourceDirectory();
```

In diesem ersten Schritt definieren wir das Quellverzeichnis, in dem sich die Excel-Arbeitsmappe mit den Links befindet.

## Schritt 2: Excel-Arbeitsmappe laden

```csharp
// Laden Sie die Excel-Arbeitsmappe
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
```

Wir laden die Excel-Arbeitsmappe mithilfe des Quelldateipfads.

## Schritt 3: Holen Sie sich die Tabelle

```csharp
// Erstes Arbeitsblatt abrufen (Standard)
Worksheet worksheet = workbook.Worksheets[0];
```

 Wir erhalten das erste Arbeitsblatt der Arbeitsmappe. Sie können das ändern`[0]` index, um bei Bedarf auf ein bestimmtes Arbeitsblatt zuzugreifen.

## Schritt 4: Erstellen Sie einen Zellbereich

```csharp
// Erstellen Sie einen Zellbereich A1:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
```

Wir erstellen einen Zellbereich, in diesem Beispiel von Zelle A1 bis Zelle A7. Sie können Zellbezüge nach Bedarf anpassen.

## Schritt 5: Bringen Sie die Hyperlinks in Reichweite

```csharp
// Holen Sie sich die Hyperlinks im Bereich
Hyperlink[] hyperlinks = range.Hyperlinks;
```

Wir erhalten alle im angegebenen Bereich vorhandenen Hyperlinks.

## Schritt 6: Durchsuchen Sie Hyperlinks und zeigen Sie Linktypen an

```csharp
foreach (Hyperlink link in hyperlinks)
{
Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
```

Wir durchlaufen jeden Link und zeigen den Anzeigetext und den zugehörigen Linktyp an.

### Beispielquellcode für die Erkennung von Linktypen mithilfe von Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
// Rufen Sie das erste (Standard-)Arbeitsblatt ab
Worksheet worksheet = workbook.Worksheets[0];
// Erstellen Sie einen Bereich A2:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
// Holen Sie sich Hyperlinks in Reichweite
Hyperlink[] hyperlinks = range.Hyperlinks;
foreach (Hyperlink link in hyperlinks)
{
	Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
Console.WriteLine("DetectLinkTypes executed successfully.");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie mit Aspose.Cells für .NET Linktypen in einer Excel-Arbeitsmappe erkennen. Mit dieser Funktion können Sie mit den in Ihren Excel-Arbeitsmappen vorhandenen Hyperlinks arbeiten. Erkunden Sie weiterhin die Funktionen von Aspose.Cells, um die Verarbeitungsmöglichkeiten Ihrer Excel-Arbeitsmappe zu erweitern.

### FAQs

#### F: Wie kann ich Aspose.Cells für .NET in meinem Projekt installieren?

 A: Sie können Aspose.Cells für .NET mit dem NuGet-Paketmanager installieren. Suchen nach[Aspose-Veröffentlichungen](https://releases.aspose.com/cells/net) in der NuGet Package Manager-Konsole und installieren Sie die neueste Version.

#### F: Kann ich Linktypen in bestimmten Arbeitsblättern und nicht im ersten Blatt erkennen?

 A: Ja, Sie können das ändern`workbook.Worksheets[0]` index, um auf ein bestimmtes Arbeitsblatt zuzugreifen. Um beispielsweise auf das zweite Blatt zuzugreifen, verwenden Sie`workbook.Worksheets[1]`.

#### F: Ist es möglich, die im Bereich erkannten Linktypen zu ändern?

A: Ja, Sie können Hyperlinks durchsuchen und Bearbeitungsvorgänge durchführen, z. B. URLs aktualisieren oder unerwünschte Links entfernen.

#### F: Welche Arten von Links sind in Aspose.Cells für .NET möglich?

A: Zu den möglichen Linktypen gehören Hyperlinks, Links zu anderen Arbeitsblättern, Links zu externen Dateien, Links zu Websites usw.

#### F: Unterstützt Aspose.Cells für .NET das Erstellen neuer Links in einer Tabelle?

 A: Ja, Aspose.Cells für .NET unterstützt das Erstellen neuer Links mithilfe von`Hyperlink` Klasse und die damit verbundenen Eigenschaften. Sie können Hyperlinks, Links zu URLs, Links zu anderen Tabellenkalkulationen usw. hinzufügen.

#### F: Kann ich Aspose.Cells für .NET in Webanwendungen verwenden?

A: Ja, Aspose.Cells für .NET kann in Webanwendungen verwendet werden. Sie können es in ASP.NET, ASP.NET Core und andere .NET-basierte Web-Frameworks einbetten.

#### F: Gibt es Dateigrößenbeschränkungen bei der Verwendung von Aspose.Cells für .NET?

A: Aspose.Cells für .NET kann ohne besondere Einschränkung große Excel-Arbeitsmappen verarbeiten. Die tatsächliche Dateigröße kann jedoch durch die verfügbaren Systemressourcen begrenzt sein.