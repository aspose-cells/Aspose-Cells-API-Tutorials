---
title: Legen Sie die Excel-Seitenausrichtung fest
linktitle: Legen Sie die Excel-Seitenausrichtung fest
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie Schritt für Schritt, wie Sie mit Aspose.Cells für .NET die Excel-Seitenausrichtung festlegen. Erhalten Sie optimierte Ergebnisse.
type: docs
weight: 130
url: /de/net/excel-page-setup/set-excel-page-orientation/
---
Im heutigen digitalen Zeitalter spielen Excel-Tabellen eine wichtige Rolle bei der Organisation und Analyse von Daten. Manchmal ist es notwendig, das Layout und Erscheinungsbild von Excel-Dokumenten an bestimmte Anforderungen anzupassen. Eine dieser Anpassungen ist das Festlegen der Seitenausrichtung, die bestimmt, ob die gedruckte Seite im Hoch- oder Querformat angezeigt wird. In diesem Tutorial werden wir den Prozess der Festlegung der Excel-Seitenausrichtung mithilfe von Aspose.Cells, einer leistungsstarken Bibliothek für die .NET-Entwicklung, Schritt für Schritt durchgehen. Lass uns eintauchen!

## Verstehen, wie wichtig es ist, die Ausrichtung der Excel-Seite festzulegen

Die Seitenausrichtung eines Excel-Dokuments beeinflusst die Darstellung des Inhalts beim Drucken. Standardmäßig verwendet Excel die Hochformatausrichtung, bei der die Seite höher als breit ist. In bestimmten Szenarien kann jedoch die Ausrichtung im Querformat, bei der die Seite breiter als hoch ist, besser geeignet sein. Wenn Sie beispielsweise breite Tabellen, Diagramme oder Diagramme drucken, sorgt die Ausrichtung im Querformat für eine bessere Lesbarkeit und visuelle Darstellung.

## Erkundung der Aspose.Cells-Bibliothek für .NET

Aspose.Cells ist eine funktionsreiche Bibliothek, die es Entwicklern ermöglicht, Excel-Dateien programmgesteuert zu erstellen, zu bearbeiten und zu konvertieren. Es bietet eine breite Palette von APIs zur Ausführung verschiedener Aufgaben, einschließlich der Festlegung der Seitenausrichtung. Bevor wir uns mit dem Code befassen, stellen Sie sicher, dass Sie die Aspose.Cells-Bibliothek zu Ihrem .NET-Projekt hinzugefügt haben.

## Schritt 1: Einrichten des Dokumentenverzeichnisses

Bevor wir mit der Excel-Datei arbeiten, müssen wir das Dokumentenverzeichnis einrichten. Ersetzen Sie den Platzhalter „IHR DOKUMENTVERZEICHNIS“ im Codeausschnitt durch den tatsächlichen Pfad zu dem Verzeichnis, in dem Sie die Ausgabedatei speichern möchten.

```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Schritt 2: Instanziieren eines Arbeitsmappenobjekts

Um mit einer Excel-Datei zu arbeiten, müssen wir eine Instanz der von Aspose.Cells bereitgestellten Workbook-Klasse erstellen. Diese Klasse stellt die gesamte Excel-Datei dar und stellt Methoden und Eigenschaften zur Bearbeitung ihres Inhalts bereit.

```csharp
// Instanziieren eines Workbook-Objekts
Workbook workbook = new Workbook();
```

## Schritt 3: Zugriff auf das Arbeitsblatt in der Excel-Datei

Als nächstes müssen wir auf das Arbeitsblatt in der Excel-Datei zugreifen, in dem wir die Seitenausrichtung festlegen möchten. In diesem Beispiel arbeiten wir mit dem ersten Arbeitsblatt (Index 0) der Arbeitsmappe.

```csharp
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei
Worksheet worksheet = workbook.Worksheets[0];
```

## Schritt 4: Seitenausrichtung auf Hochformat einstellen

Jetzt ist es an der Zeit, die Seitenausrichtung festzulegen. Aspose.Cells stellt die PageSetup-Eigenschaft für jedes Arbeitsblatt bereit, mit der wir verschiedene seitenbezogene Einstellungen anpassen können. Um die Seitenausrichtung festzulegen, müssen wir der Orientation-Eigenschaft des PageSetup-Objekts den Wert PageOrientationType.Portrait zuweisen.

```csharp
// Stellen Sie die Ausrichtung auf Hochformat ein
worksheet.PageSetup.Orientation = PageOrientationType.Portrait;
```

## Schritt 5: Speichern der Arbeitsmappe

Sobald wir die erforderlichen Änderungen am Arbeitsblatt vorgenommen haben, können wir das geänderte Arbeitsmappenobjekt in einer Datei speichern. Die Save-Methode der Workbook-Klasse akzeptiert den Dateipfad, in dem die Ausgabedatei gespeichert wird

.

```csharp
// Speichern Sie die Arbeitsmappe.
workbook.Save(dataDir + "PageOrientation_out.xls");
```

### Beispielquellcode zum Festlegen der Excel-Seitenausrichtung mit Aspose.Cells für .NET 

```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanziieren eines Workbook-Objekts
Workbook workbook = new Workbook();
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei
Worksheet worksheet = workbook.Worksheets[0];
// Stellen Sie die Ausrichtung auf Hochformat ein
worksheet.PageSetup.Orientation = PageOrientationType.Portrait;
// Speichern Sie die Arbeitsmappe.
workbook.Save(dataDir + "PageOrientation_out.xls");
```

## Abschluss

In diesem Tutorial haben wir gelernt, wie man die Excel-Seitenausrichtung mithilfe von Aspose.Cells für .NET festlegt. Wenn Sie der Schritt-für-Schritt-Anleitung folgen, können Sie die Seitenausrichtung von Excel-Dateien ganz einfach an Ihre spezifischen Anforderungen anpassen. Aspose.Cells bietet einen umfassenden Satz an APIs zur Bearbeitung von Excel-Dokumenten und gibt Ihnen die volle Kontrolle über deren Aussehen und Inhalt. Entdecken Sie die Möglichkeiten mit Aspose.Cells und verbessern Sie Ihre Excel-Automatisierungsaufgaben.

## FAQs

#### F1: Kann ich die Seitenausrichtung auf Querformat statt auf Hochformat einstellen?

 A1: Ja, absolut! Anstatt die zuzuweisen`PageOrientationType.Portrait` Wert, den Sie verwenden können`PageOrientationType.Landscape` , um die Seitenausrichtung auf Querformat einzustellen.

#### F2: Unterstützt Aspose.Cells neben Excel auch andere Dateiformate?

A2: Ja, Aspose.Cells unterstützt eine Vielzahl von Dateiformaten, darunter XLS, XLSX, CSV, HTML, PDF und viele mehr. Es bietet APIs zum Erstellen, Bearbeiten und Konvertieren von Dateien in verschiedenen Formaten.

#### F3: Kann ich für verschiedene Arbeitsblätter innerhalb derselben Excel-Datei unterschiedliche Seitenausrichtungen festlegen?

 A3: Ja, Sie können unterschiedliche Seitenausrichtungen für verschiedene Arbeitsblätter festlegen, indem Sie auf zugreifen`PageSetup` Objekt jedes Arbeitsblatts einzeln bearbeiten und ändern`Orientation` Eigentum entsprechend.

#### F4: Ist Aspose.Cells sowohl mit .NET Framework als auch mit .NET Core kompatibel?

A4: Ja, Aspose.Cells ist sowohl mit .NET Framework als auch mit .NET Core kompatibel. Es unterstützt eine Vielzahl von .NET-Versionen und ermöglicht Ihnen den Einsatz in verschiedenen Entwicklungsumgebungen.
