---
title: Bildlaufleisten des Arbeitsblatts anzeigen und ausblenden
linktitle: Bildlaufleisten des Arbeitsblatts anzeigen und ausblenden
second_title: Aspose.Cells für .NET API-Referenz
description: Blenden Sie Bildlaufleisten im Excel-Arbeitsblatt mit Aspose.Cells für .NET ein oder aus.
type: docs
weight: 50
url: /de/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
In diesem Tutorial zeigen wir Ihnen, wie Sie mithilfe von C#-Quellcode mit Aspose.Cells für .NET vertikale und horizontale Bildlaufleisten in einem Excel-Arbeitsblatt ein- oder ausblenden. Befolgen Sie die nachstehenden Schritte, um das gewünschte Ergebnis zu erzielen.

## Schritt 1: Importieren Sie die erforderlichen Bibliotheken

Stellen Sie sicher, dass Sie die Aspose.Cells-Bibliothek für .NET installiert haben und importieren Sie die erforderlichen Bibliotheken in Ihr C#-Projekt.

```csharp
using Aspose.Cells;
using System.IO;
```

## Schritt 2: Verzeichnispfad festlegen und Excel-Datei öffnen

 Legen Sie den Pfad zu dem Verzeichnis fest, das Ihre Excel-Datei enthält, und öffnen Sie dann die Datei, indem Sie einen Dateistream erstellen und a instanziieren`Workbook` Objekt.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Schritt 3: Bildlaufleisten ausblenden

 Benutzen Sie die`IsVScrollBarVisible` Und`IsHScrollBarVisible` Eigenschaften der`Workbook.Settings` Objekt, um die vertikalen und horizontalen Bildlaufleisten des Arbeitsblatts auszublenden.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## Schritt 4: Änderungen speichern

 Nachdem Sie die notwendigen Änderungen vorgenommen haben, speichern Sie die geänderte Excel-Datei mit`Save` Methode der`Workbook` Objekt.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Beispielquellcode für das Anzeigen und Ausblenden von Bildlaufleisten im Arbeitsblatt mit Aspose.Cells für .NET 

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Erstellen eines Dateistreams, der die zu öffnende Excel-Datei enthält
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanziieren eines Workbook-Objekts
// Öffnen der Excel-Datei über den Dateistream
Workbook workbook = new Workbook(fstream);
// Ausblenden der vertikalen Bildlaufleiste der Excel-Datei
workbook.Settings.IsVScrollBarVisible = false;
// Ausblenden der horizontalen Bildlaufleiste der Excel-Datei
workbook.Settings.IsHScrollBarVisible = false;
// Speichern der geänderten Excel-Datei
workbook.Save(dataDir + "output.xls");
// Schließen des Dateistreams, um alle Ressourcen freizugeben
fstream.Close();
```

### Abschluss

Diese Schritt-für-Schritt-Anleitung zeigte Ihnen, wie Sie mit Aspose.Cells für .NET vertikale und horizontale Bildlaufleisten in einer Excel-Tabelle ein- oder ausblenden. Mithilfe des bereitgestellten C#-Quellcodes können Sie die Anzeige von Bildlaufleisten in Ihren Excel-Dateien ganz einfach anpassen.

### Häufig gestellte Fragen (FAQ)

#### Was ist Aspose.Cells für .NET?

Aspose.Cells für .NET ist eine leistungsstarke Bibliothek zum Bearbeiten von Excel-Dateien in .NET-Anwendungen.

#### Wie kann ich Aspose.Cells für .NET installieren?

 Um Aspose.Cells für .NET zu installieren, müssen Sie das entsprechende Paket von herunterladen[Aspose-Veröffentlichungen](https://releases/aspose.com/cells/net/) und fügen Sie es Ihrem .NET-Projekt hinzu.

#### Wie kann ich mit Aspose.Cells für .NET Bildlaufleisten in einer Excel-Tabelle anzeigen oder ausblenden?

 Du kannst den ... benutzen`IsVScrollBarVisible` Und`IsHScrollBarVisible` Eigenschaften der`Workbook.Settings` Objekt zum Anzeigen bzw. Ausblenden der vertikalen und horizontalen Bildlaufleiste in einem Excel-Arbeitsblatt.

#### Welche anderen Excel-Dateiformate werden von Aspose.Cells für .NET unterstützt?

Aspose.Cells für .NET unterstützt eine Vielzahl von Excel-Dateiformaten wie XLS, XLSX, CSV, HTML, PDF usw.