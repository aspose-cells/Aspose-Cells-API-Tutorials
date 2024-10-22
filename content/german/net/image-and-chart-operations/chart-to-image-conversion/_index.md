---
title: Konvertierung von Diagrammen in Bilder in .NET
linktitle: Konvertierung von Diagrammen in Bilder in .NET
second_title: Aspose.Cells .NET Excel-Verarbeitungs-API
description: Erfahren Sie in dieser Schritt-für-Schritt-Anleitung, wie Sie mit Aspose.Cells Diagramme in .NET in Bilder konvertieren. Wandeln Sie Excel-Diagramme ganz einfach in hochwertige Bilder um.
type: docs
weight: 10
url: /de/net/image-and-chart-operations/chart-to-image-conversion/
---
## Einführung
Das Konvertieren eines Diagramms aus Excel in ein Bild kann eine entscheidende Voraussetzung beim Erstellen von Berichtssystemen oder beim Teilen visueller Datendarstellungen sein. Glücklicherweise ist dieser Vorgang mit Aspose.Cells für .NET kinderleicht! Egal, ob Sie Berichte erstellen oder einfach Excel-Diagramme zur besseren Anzeige in Bilder konvertieren, diese Anleitung führt Sie Schritt für Schritt durch den Vorgang.
## Voraussetzungen
Bevor wir beginnen, stellen wir sicher, dass Sie alles haben, um diesem Tutorial folgen zu können.
### Aspose.Cells für .NET-Bibliothek
Zuerst müssen Sie die Aspose.Cells-Bibliothek für .NET herunterladen und in Ihrem Projekt referenzieren. Sie können die neueste Version hier herunterladen:
- [Laden Sie Aspose.Cells für .NET herunter](https://releases.aspose.com/cells/net/)
### .NET-Umgebung
Stellen Sie sicher, dass das .NET-Framework auf Ihrem System installiert ist. Sie können Visual Studio oder eine andere .NET-Entwicklungsumgebung verwenden, um dieses Beispiel auszuführen.
### Lizenz-Setup (optional)
 Obwohl Sie Aspose.Cells mit einer kostenlosen Testversion verwenden können, sollten Sie für die volle Funktionalität ohne Einschränkungen eine[vorläufige Lizenz](https://purchase.aspose.com/temporary-license/) oder kaufen Sie eines bei[Hier](https://purchase.aspose.com/buy).

## Pakete importieren
Um loszulegen, importieren wir die erforderlichen Namespaces, um mit der Aspose.Cells-Bibliothek zu arbeiten. Dadurch können wir Excel-Dateien bearbeiten und Bilder generieren.
```csharp
using System.IO;
using System.Drawing;
using Aspose.Cells;
```
Stellen Sie sicher, dass Sie diese Pakete bereit haben, bevor Sie mit dem Codierungsteil beginnen.

Lassen Sie uns nun den Vorgang der Konvertierung eines Diagramms in ein Bild in einfache Schritte aufschlüsseln.
## Schritt 1: Richten Sie Ihr Projektverzeichnis ein
Sie benötigen einen Ort, an dem Sie die generierten Bilder speichern können, oder? Lassen Sie uns zunächst ein Verzeichnis erstellen, in dem die Ausgabebilder gespeichert werden.

Wir beginnen damit, den Pfad für unser Dokumentverzeichnis zu definieren und sicherzustellen, dass der Ordner existiert. Wenn nicht, erstellen wir einen.
```csharp
// Definieren Sie das Verzeichnis zum Speichern von Bildern
string dataDir = "Your Document Directory";
// Überprüfen Sie, ob das Verzeichnis existiert
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
Mit diesem Schritt können Sie Ihre Diagrammbilder generieren und in diesem Verzeichnis speichern.
## Schritt 2: Erstellen Sie eine neue Arbeitsmappe
Hier instanziieren wir ein Workbook-Objekt. Dies stellt unsere Excel-Datei dar, in die das Diagramm eingebettet wird.

Eine Arbeitsmappe ist wie eine Excel-Datei, die Blätter enthält. Indem wir eine neue Arbeitsmappe erstellen, beginnen wir mit einer leeren Excel-Datei.
```csharp
// Erstellen eines neuen Workbook-Objekts
Workbook workbook = new Workbook();
```
## Schritt 3: Neues Arbeitsblatt hinzufügen
Jede Excel-Datei hat Arbeitsblätter (oder Registerkarten). Fügen wir unserer Arbeitsmappe eines hinzu.

Das Hinzufügen eines neuen Arbeitsblatts ist wichtig, da wir unsere Daten und Diagramme in dieses Blatt einfügen. Sobald das Blatt hinzugefügt ist, rufen wir seine Referenz ab.
```csharp
// Hinzufügen eines neuen Arbeitsblatts zur Arbeitsmappe
int sheetIndex = workbook.Worksheets.Add();
// Abrufen des neu hinzugefügten Arbeitsblatts
Worksheet worksheet = workbook.Worksheets[sheetIndex];
```
## Schritt 4: Füllen Sie das Arbeitsblatt mit Daten
Um ein aussagekräftiges Diagramm zu erstellen, benötigen wir einige Daten, oder? Füllen wir einige Zellen mit Beispielwerten aus.

Wir werden Daten zu bestimmten Zellen im Arbeitsblatt hinzufügen. Diese Daten werden später zum Generieren unseres Diagramms verwendet.
```csharp
// Hinzufügen von Beispieldaten zu Zellen
worksheet.Cells["A1"].PutValue(50);
worksheet.Cells["A2"].PutValue(100);
worksheet.Cells["A3"].PutValue(150);
worksheet.Cells["B1"].PutValue(4);
worksheet.Cells["B2"].PutValue(20);
worksheet.Cells["B3"].PutValue(50);
```
## Schritt 5: Dem Arbeitsblatt ein Diagramm hinzufügen
Erstellen wir nun ein Säulendiagramm, das die gerade hinzugefügten Daten visualisiert.

Wir geben den Diagrammtyp (Säulendiagramm) an und definieren seine Größe und Position innerhalb des Arbeitsblatts.
```csharp
// Hinzufügen eines Säulendiagramms zum Arbeitsblatt
int chartIndex = worksheet.Charts.Add(Aspose.Cells.Charts.ChartType.Column, 5, 0, 15, 5);
```
## Schritt 6: Definieren Sie die Diagrammdatenquelle
Und jetzt geschieht die Magie: die Verknüpfung des Diagramms mit den Daten im Arbeitsblatt!

Wir verknüpfen das Diagramm mit den Daten in den Spalten A1 bis B3. Dadurch wird dem Diagramm mitgeteilt, woher die Daten stammen sollen.
```csharp
// Verknüpfen Sie das Diagramm mit den Daten im Bereich A1 bis B3
Aspose.Cells.Charts.Chart chart = worksheet.Charts[chartIndex];
chart.NSeries.Add("A1:B3", true);
```
## Schritt 7: Konvertieren Sie das Diagramm in ein Bild
Der Moment der Wahrheit: Wir werden dieses Diagramm in eine Bilddatei konvertieren!

 Hier verwenden wir die`ToImage`Methode, um das Diagramm in ein Bildformat Ihrer Wahl zu konvertieren. In diesem Fall konvertieren wir es in ein EMF-Format (Enhanced Metafile).
```csharp
// Konvertieren Sie das Diagramm in ein Bild und speichern Sie es im Verzeichnis
chart.ToImage(dataDir + "Chart.emf", ImageFormat.Emf);
```
Und das war’s! Ihr Diagramm wurde nun als Bild gespeichert. Zeit, sich selbst auf die Schulter zu klopfen.
## Schritt 8: Erfolgsmeldung anzeigen
Zum Abschluss zeigen wir eine Meldung zur Bestätigung der Bildgenerierung an.
```csharp
// Zeigen Sie eine Meldung an, die den Erfolg bestätigt
System.Console.WriteLine("Image generated successfully.");
```
## Abschluss
Boom! So einfach ist es, mit Aspose.Cells für .NET ein Diagramm aus Excel in ein Bild umzuwandeln. Dieser Prozess vereinfacht nicht nur die Darstellung von Daten, sondern erhöht auch die Flexibilität von Berichten oder Dashboards, bei denen Bilder eingebetteten Diagrammen vorgezogen werden.
Indem Sie die in diesem Handbuch beschriebenen Schritte befolgen, können Sie jetzt jedes Excel-Diagramm in ein Bild umwandeln und so visuelle Daten nahtlos in verschiedene Anwendungen integrieren.
## Häufig gestellte Fragen
### Kann ich mit dieser Methode verschiedene Diagrammtypen konvertieren?
Ja, Sie können jeden von Aspose.Cells unterstützten Diagrammtyp konvertieren, einschließlich Kreisdiagramme, Balkendiagramme, Liniendiagramme und mehr!
### Ist es möglich, das Bildformat zu ändern?
 Absolut! Obwohl wir in diesem Beispiel EMF verwendet haben, können Sie das Bildformat in PNG, JPEG, BMP und andere ändern, indem Sie einfach die`ImageFormat` Parameter.
### Unterstützt Aspose.Cells hochauflösende Bilder?
Ja, Aspose.Cells ermöglicht Ihnen die Steuerung der Bildauflösung und der Qualitätseinstellungen beim Exportieren von Diagrammen in Bilder.
### Kann ich mehrere Diagramme auf einmal in Bilder umwandeln?
Ja, Sie können mehrere Diagramme in einer Arbeitsmappe durchlaufen und sie alle mit nur wenigen Codezeilen in Bilder umwandeln.
### Gibt es eine Begrenzung für die Anzahl der Diagramme, die ich konvertieren kann?
Aspose.Cells setzt keine inhärenten Grenzen, die Verarbeitung großer Datenmengen kann jedoch vom Arbeitsspeicher und der Leistungsfähigkeit Ihres Systems abhängen.