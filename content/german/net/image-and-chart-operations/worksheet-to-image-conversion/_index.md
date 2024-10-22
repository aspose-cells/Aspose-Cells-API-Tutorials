---
title: Konvertierung von Arbeitsblättern in Bilder in .NET
linktitle: Konvertierung von Arbeitsblättern in Bilder in .NET
second_title: Aspose.Cells .NET Excel-Verarbeitungs-API
description: Erfahren Sie in unserer Schritt-für-Schritt-Anleitung, wie Sie mit Aspose.Cells Excel-Arbeitsblätter in .NET in Bilder konvertieren. Optimieren Sie Ihre Datenvisualisierung.
type: docs
weight: 11
url: /de/net/image-and-chart-operations/worksheet-to-image-conversion/
---
## Einführung
Wenn es um die Bearbeitung von Excel-Dateien in .NET geht, ist Aspose.Cells eine zuverlässige und robuste Bibliothek. Eine der häufigen Aufgaben, die Ihnen begegnen könnten, ist die Konvertierung eines Excel-Arbeitsblatts in ein Bild. Egal, ob Sie das Blatt auf einer Webseite anzeigen, in einen Bericht aufnehmen oder die Daten einfach visuell teilen möchten, diese Schritt-für-Schritt-Anleitung führt Sie durch den gesamten Prozess. Am Ende verfügen Sie über alles, was Sie brauchen, um Arbeitsblätter nahtlos in Bilder umzuwandeln. Also tauchen wir ein!
## Voraussetzungen
Bevor wir mit der Konvertierung beginnen, müssen Sie unbedingt sicherstellen, dass Sie alles richtig eingerichtet haben. Hier sind die Voraussetzungen, die Sie benötigen:
1. Visual Studio: Stellen Sie sicher, dass Visual Studio auf Ihrem Computer installiert ist. Mit dieser IDE können Sie Ihre .NET-Projekte reibungslos ausführen.
2. Aspose.Cells für .NET-Bibliothek: Sie müssen diese Bibliothek erwerben. Sie können[Laden Sie es hier herunter](https://releases.aspose.com/cells/net/) oder beginnen Sie mit einem[Kostenlose Testversion](https://releases.aspose.com/).
3. Grundkenntnisse in C#: Kenntnisse in der C#-Programmierung sind von Vorteil, da unsere Beispiele und Erklärungen in dieser Sprache geschrieben sind.
4.  Eine Excel-Beispieldatei: Erstellen oder laden Sie zur Demonstration eine Excel-Datei herunter. Speichern Sie sie als`MyTestBook1.xls` in Ihrem Projektverzeichnis.
5. Grundlegendes Verständnis von .NET-Projekten: Wenn Sie wissen, wie man ein einfaches .NET-Projekt erstellt, wird dies einfacher, aber keine Sorge – wir führen Sie durch die einzelnen Schritte.
## Pakete importieren
Der erste Schritt auf unserem Weg besteht darin, die erforderlichen Aspose.Cells-Pakete in unser Projekt zu importieren. Dies ist wichtig, da wir so alle Funktionen nutzen können, die Aspose.Cells bietet.
## Schritt 1: Neues Projekt erstellen 
Erstellen Sie zunächst ein neues .NET-Projekt in Visual Studio:
- Öffnen Sie Visual Studio.
- Klicken Sie auf „Neues Projekt erstellen“.
- Wählen Sie je nach Wunsch „Konsolen-App (.NET Framework)“ oder „Konsolen-App (.NET Core)“ aus.
- Geben Sie Ihrem Projekt einen Namen (z. B. WorksheetToImage) und klicken Sie auf „Erstellen“.
## Schritt 2: Aspose.Cells-Referenz hinzufügen
Jetzt, da wir unser Projekt haben, müssen wir Aspose.Cells hinzufügen:
- Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf Ihr Projekt.
- Wählen Sie „NuGet-Pakete verwalten“ aus.
- Suchen Sie nach „Aspose.Cells“ und installieren Sie die neueste Version.
```csharp
using System.IO;
using System.Drawing;
using Aspose.Cells;
using Aspose.Cells.Rendering;
```
Sie sind bereit für den Codierungsteil!

Lassen Sie uns nun den eigentlichen Konvertierungsprozess Schritt für Schritt durchgehen. Wir verwenden ein einfaches C#-Programm, das eine Excel-Datei öffnet, ein Arbeitsblatt in ein Bild konvertiert und dieses Bild in einem angegebenen Verzeichnis speichert.
## Schritt 3: Einrichten der Umgebung
Richten Sie zunächst Ihre Umgebung ein, indem Sie den Pfad zu Ihrem Dokumentverzeichnis definieren:
```csharp
// Der Pfad zum Dokumentverzeichnis.
string dataDir = "Your Document Directory";
```
 Hier definieren wir eine Variable namens`dataDir` das den Pfad zum Verzeichnis enthält, in dem unsere Dateien gespeichert werden. Ersetzen Sie`"Your Document Directory"` durch den tatsächlichen Pfad auf Ihrem System (z. B. "C:\\MeineDateien\\").
## Schritt 4: Öffnen Sie die Excel-Arbeitsmappe
 Als nächstes öffnen wir die Excel-Datei mit dem`Workbook` Klasse von Aspose.Cells:
```csharp
// Öffnen Sie eine Excel-Vorlagendatei.
Workbook book = new Workbook(dataDir + "MyTestBook1.xls");
```
 In diesem Schritt erstellen wir eine Instanz des`Workbook`Klasse und übergeben Sie den Pfad zu unserer Excel-Datei. Dadurch können wir programmgesteuert mit dem Inhalt der Datei interagieren.
## Schritt 5: Zugriff auf das Arbeitsblatt
Nachdem wir nun die Arbeitsmappe geöffnet haben, greifen wir auf das erste Arbeitsblatt zu:
```csharp
// Holen Sie sich das erste Arbeitsblatt.
Worksheet sheet = book.Worksheets[0];
```
 Hier holen wir uns das erste Arbeitsblatt (Index`0` ) aus der Arbeitsmappe. Aspose.Cells-Arrays sind nullindiziert, was bedeutet, dass das erste Blatt`0`.
## Schritt 6: Bild- oder Druckoptionen festlegen
 Bevor wir das Bild rendern, müssen wir angeben, wie es aussehen soll, indem wir`ImageOrPrintOptions`:
```csharp
// ImageOrPrintOptions definieren
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
// Geben Sie das Bildformat an
imgOptions.ImageType = Drawing.ImageType.Jpeg;
// Es wird nur eine Seite für das gesamte Blatt gerendert
imgOptions.OnePagePerSheet = true;
```
 In diesem Schritt erstellen wir eine Instanz von`ImageOrPrintOptions` . Wir geben an, dass wir die Ausgabe als JPEG-Bild speichern möchten und setzen`OnePagePerSheet` Zu`true` um sicherzustellen, dass das gesamte Blatt in einem Bild erfasst wird.
## Schritt 7: Rendern des Arbeitsblatts
Mit den vorhandenen Optionen können wir jetzt das Arbeitsblatt rendern:
```csharp
// Rendern Sie das Blatt unter Berücksichtigung der angegebenen Bild-/Druckoptionen
SheetRender sr = new SheetRender(sheet, imgOptions);
// Rendern Sie das Bild für das Blatt
Bitmap bitmap = sr.ToImage(0);
```
 Der`SheetRender`Klasse hilft, das Arbeitsblatt in ein Bitmap-Bild umzuwandeln. Wir nennen`ToImage(0)` um die Nullseite (unser erstes Blatt) in eine Bitmap zu rendern.
## Schritt 8: Speichern des Bildes
Nach dem Rendern müssen wir das Bild im angegebenen Verzeichnis speichern:
```csharp
// Speichern Sie die Bilddatei unter Angabe des Bildformats.
bitmap.Save(dataDir + "SheetImage.out.jpg");
```
 Hier speichern wir das von uns erzeugte Bitmap-Bild. Diese Zeile schreibt das Bild in den`dataDir` location mit dem Dateinamen`SheetImage.out.jpg`.
## Schritt 9: Abschlussbenachrichtigung
Um sicherzustellen, dass der Vorgang abgeschlossen ist, fügen wir eine einfache Konsolennachricht hinzu:
```csharp
// Zeigen Sie das Ergebnis an, damit der Benutzer weiß, dass die Verarbeitung abgeschlossen ist.
System.Console.WriteLine("Conversion to Image(s) completed.");
```
Diese Zeile gibt eine Bestätigungsmeldung an die Konsole aus und informiert den Benutzer darüber, dass die Konvertierung erfolgreich war.
## Abschluss
Und da haben Sie es! In nur wenigen einfachen Schritten haben Sie gelernt, wie Sie mit Aspose.Cells für .NET ein Excel-Arbeitsblatt in ein Bild konvertieren. Dieser Vorgang ist nicht nur schnell, sondern auch leistungsstark und ermöglicht es Ihnen, mühelos visuelle Darstellungen Ihrer Tabellendaten zu erstellen.
## Häufig gestellte Fragen
### Was ist Aspose.Cells?
Aspose.Cells ist eine .NET-Bibliothek, die es Entwicklern ermöglicht, Excel-Dateien programmgesteuert zu erstellen, zu bearbeiten, zu konvertieren und zu verarbeiten.
### Kann ich Aspose.Cells kostenlos nutzen?
 Ja, Sie können Aspose.Cells verwenden, indem Sie eine kostenlose Testversion von deren[Webseite](https://releases.aspose.com/).
### Welche Bildformate unterstützt Aspose.Cells für den Export?
Aspose.Cells unterstützt verschiedene Bildformate, darunter JPEG, PNG, BMP und GIF.
### Wo finde ich zusätzliche Unterstützung für Aspose.Cells?
 Sie können auf das Support-Forum für Aspose.Cells zugreifen[Hier](https://forum.aspose.com/c/cells/9).
### Wie erhalte ich eine temporäre Lizenz für Aspose.Cells?
 Eine temporäre Lizenz erhalten Sie bei[Seite mit der temporären Lizenz](https://purchase.aspose.com/temporary-license/).