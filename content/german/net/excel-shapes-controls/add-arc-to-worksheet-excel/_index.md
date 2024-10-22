---
title: Fügen Sie dem Arbeitsblatt in Excel einen Bogen hinzu
linktitle: Fügen Sie dem Arbeitsblatt in Excel einen Bogen hinzu
second_title: Aspose.Cells .NET Excel-Verarbeitungs-API
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET Bögen zu Excel-Arbeitsblättern hinzufügen. Folgen Sie unserer Schritt-für-Schritt-Anleitung, um Ihre Tabellenkalkulationsdesigns zu verbessern.
type: docs
weight: 16
url: /de/net/excel-shapes-controls/add-arc-to-worksheet-excel/
---
## Einführung
Das Erstellen optisch ansprechender Excel-Tabellen ist für die Datenpräsentation von entscheidender Bedeutung, und die Aspose.Cells-Bibliothek bietet Entwicklern robuste Tools zur Erledigung dieser Aufgabe. Eine interessante Funktion, die Sie möglicherweise in Ihre Excel-Dokumente integrieren möchten, ist die Möglichkeit, Formen wie Bögen hinzuzufügen. In diesem Tutorial erfahren Sie Schritt für Schritt, wie Sie mit Aspose.Cells für .NET Bögen zu einem Excel-Arbeitsblatt hinzufügen. Am Ende dieses Artikels lernen Sie nicht nur, wie Sie Bögen hinzufügen, sondern erhalten auch Einblicke in die Verwaltung von Formen im Allgemeinen.
## Voraussetzungen
Bevor wir uns mit den Feinheiten des Hinzufügens von Bögen zu Ihrem Arbeitsblatt befassen, müssen Sie unbedingt sicherstellen, dass einige Dinge vorhanden sind. Hier sind die Voraussetzungen, die Sie für den Einstieg benötigen:
1. Visual Studio: Sie müssen Visual Studio auf Ihrem Computer installiert haben, da wir C# als Programmiersprache verwenden.
2. .NET Framework: Stellen Sie sicher, dass Sie das .NET Framework oder .NET Core installiert haben. Aspose.Cells unterstützt beides.
3. Aspose.Cells für .NET: Sie benötigen die Aspose.Cells-Bibliothek. Sie können sie von der[Aspose.Cells Downloads](https://releases.aspose.com/cells/net/) Seite.
4. Grundlegende Kenntnisse in C#: Wenn Sie mit C# vertraut sind, können Sie den Codeausschnitten ohne großen Aufwand folgen.
## Pakete importieren
Um mit Aspose.Cells in Ihrem Projekt arbeiten zu können, müssen Sie die erforderlichen Pakete importieren. So geht's:
### Neues Projekt erstellen
- Öffnen Sie Visual Studio.
- Wählen Sie „Neues Projekt erstellen“.
- Wählen Sie eine Vorlage aus, die mit .NET funktioniert (z. B. eine Konsolenanwendung).
  
### Aspose.Cells-Referenzen hinzufügen
- Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf Ihr Projekt.
- Wählen Sie „NuGet-Pakete verwalten“ aus.
- Suchen Sie nach „Aspose.Cells“ und installieren Sie es.
Jetzt können Sie mit der Codierung der Bogenaddition beginnen.
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
```
Hier ist eine schrittweise Aufschlüsselung des Codes, der zeigt, wie einem Arbeitsblatt in Excel Bögen hinzugefügt werden.
## Schritt 1: Einrichten des Verzeichnisses
Der erste Schritt besteht darin, ein Verzeichnis einzurichten, in dem Sie Ihre Excel-Datei speichern. Dies erleichtert die Verwaltung Ihrer Ausgabedateien.
```csharp
string dataDir = "Your Document Directory";
//Erstellen Sie ein Verzeichnis, falls es noch nicht vorhanden ist.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
In diesem Codeausschnitt geben wir den Pfad zum Dokumentverzeichnis an. Wir prüfen auch, ob das Verzeichnis existiert. Wenn nicht, erstellen wir es. Damit wird die Grundlage für unsere Ausgabe gelegt.
## Schritt 2: Instanziieren einer Arbeitsmappe
Als Nächstes erstellen wir eine neue Arbeitsmappeninstanz.
```csharp
// Instanziieren Sie eine neue Arbeitsmappe.
Workbook excelbook = new Workbook();
```
Diese Zeile erstellt eine neue Excel-Arbeitsmappe. Stellen Sie sich das als eine leere Leinwand vor, auf der wir Formen, Daten und mehr hinzufügen können.
## Schritt 3: Fügen Sie die erste Bogenform hinzu
Fügen wir nun unsere erste Bogenform zum Arbeitsblatt hinzu.
```csharp
// Fügen Sie eine Bogenform hinzu.
Aspose.Cells.Drawing.ArcShape arc1 = excelbook.Worksheets[0].Shapes.AddArc(2, 0, 2, 0, 130, 130);
```
 Hier fügen wir dem ersten Arbeitsblatt einen Bogen hinzu. Die Parameter definieren die Position und Größe des Bogens:`(left, top, width, height, startAngle, endAngle)`. Es ist, als würde man einen Kreisabschnitt aufzeichnen!
## Schritt 4: Passen Sie den ersten Bogen an
Nachdem Sie den Bogen hinzugefügt haben, möchten Sie möglicherweise sein Erscheinungsbild anpassen.
```csharp
// Festlegen der Farbe für die Füllform
arc1.Fill.FillType = FillType.Solid;
arc1.Fill.SolidFill.Color = Color.Blue;
// Legen Sie die Platzierung des Bogens fest.
arc1.Placement = PlacementType.FreeFloating;           
// Stellen Sie die Linienstärke ein.
arc1.Line.Weight = 1;      
// Legen Sie den Strichstil des Bogens fest.
arc1.Line.DashStyle = MsoLineDashStyle.Solid;
```
In diesem Abschnitt passen wir den Bogen an. Wir stellen den Fülltyp auf Vollfarbe (in diesem Fall Blau) ein, definieren, wie er platziert wird, legen die Linienstärke fest und wählen einen Strichstil. Im Grunde verschönern wir unseren Bogen, um ihn optisch ansprechend zu gestalten!
## Schritt 5: Fügen Sie eine zweite Bogenform hinzu
Fügen wir eine weitere Bogenform hinzu, um mehr Kontext zu bieten.
```csharp
// Fügen Sie eine weitere Bogenform hinzu.
Aspose.Cells.Drawing.ArcShape arc2 = excelbook.Worksheets[0].Shapes.AddArc(9, 0, 2, 0, 130, 130);
```
Ähnlich wie beim ersten Bogen fügen wir einen zweiten Bogen auf demselben Arbeitsblatt hinzu. Die Koordinaten werden hier etwas verschoben, um ihn anders zu positionieren.
## Schritt 6: Passen Sie den zweiten Bogen an
Genau wie beim ersten Bogen werden wir auch den zweiten anpassen.
```csharp
// Festlegen der Linienfarbe
arc2.Line.FillType = FillType.Solid;
arc2.Line.SolidFill.Color = Color.Blue;
// Legen Sie die Platzierung des Bogens fest.
arc2.Placement = PlacementType.FreeFloating;          
// Stellen Sie die Linienstärke ein.
arc2.Line.Weight = 1;           
// Legen Sie den Strichstil des Bogens fest.
arc2.Line.DashStyle = MsoLineDashStyle.Solid;
```
Hier geben wir dem zweiten Bogen das gleiche Styling wie dem ersten. Sie können die Farbe oder das Styling nach Wunsch ändern, um Einzigartigkeit oder thematische Aspekte zu erzielen.
## Schritt 7: Speichern Sie die Arbeitsmappe
Schließlich ist es an der Zeit, Ihre neu erstellte Arbeitsmappe mit den Bögen zu speichern.
```csharp
// Speichern Sie die Excel-Datei.
excelbook.Save(dataDir + "book1.out.xls");
```
Diese Zeile funktioniert wie das Drücken der Schaltfläche „Speichern“. Wir speichern unsere Arbeit am angegebenen Ort unter einem bestimmten Dateinamen. Überprüfen Sie unbedingt Ihr Verzeichnis, um Ihr Meisterwerk im Excel-Format anzuzeigen!
## Abschluss
In diesem Tutorial haben wir den Prozess des Hinzufügens von Bogenformen zu einem Excel-Arbeitsblatt mithilfe von Aspose.Cells für .NET untersucht. In einer einfachen Schritt-für-Schritt-Anleitung haben Sie gelernt, wie Sie eine neue Arbeitsmappe erstellen, Bögen hinzufügen, ihr Erscheinungsbild anpassen und Ihr Dokument speichern. Diese Funktion verbessert nicht nur die visuelle Attraktivität Ihrer Tabellen, sondern macht Ihre Datenpräsentationen auch informativer. Egal, ob Sie Diagramme oder Berichte erstellen oder einfach nur experimentieren, die Verwendung von Formen wie Bögen kann Ihren Projekten eine kreative Note verleihen.
## Häufig gestellte Fragen
### Was ist Aspose.Cells?
Aspose.Cells ist eine leistungsstarke Bibliothek, mit der Entwickler Excel-Dateien programmgesteuert erstellen, bearbeiten und konvertieren können, ohne Microsoft Excel zu benötigen.
### Muss ich Microsoft Excel installieren, um Aspose.Cells zu verwenden?
Nein, Aspose.Cells ist völlig unabhängig und erfordert keine Installation von Microsoft Excel.
### Kann ich Aspose.Cells kostenlos testen?
Ja, Sie können Aspose.Cells mit ihren[Kostenlose Testversion](https://releases.aspose.com/).
### Welche Programmiersprachen unterstützt Aspose.Cells?
Aspose.Cells unterstützt mehrere Sprachen, darunter C#, VB.NET und mehr.
### Wo erhalte ich Support für Aspose.Cells?
 Unterstützung erhalten Sie durch die[Aspose Forum](https://forum.aspose.com/c/cells/9).