---
title: Seitenumbruchvorschau des Arbeitsblatts
linktitle: Seitenumbruchvorschau des Arbeitsblatts
second_title: Aspose.Cells für .NET API-Referenz
description: Schritt-für-Schritt-Anleitung zum Anzeigen der Seitenumbruchvorschau des Arbeitsblatts mit Aspose.Cells für .NET.
type: docs
weight: 110
url: /de/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
In diesem Tutorial erklären wir, wie Sie mit Aspose.Cells für .NET die Seitenumbruchvorschau eines Arbeitsblatts anzeigen. Befolgen Sie diese Schritte, um das gewünschte Ergebnis zu erhalten:

## Schritt 1: Einrichten der Umgebung

Stellen Sie sicher, dass Sie Aspose.Cells für .NET installiert und Ihre Entwicklungsumgebung eingerichtet haben. Stellen Sie außerdem sicher, dass Sie über eine Kopie der Excel-Datei verfügen, in der Sie die Seitenumbruchvorschau anzeigen möchten.

## Schritt 2: Importieren Sie die erforderlichen Abhängigkeiten

Fügen Sie die erforderlichen Anweisungen hinzu, um die Klassen von Aspose.Cells zu verwenden:

```csharp
using Aspose.Cells;
using System.IO;
```

## Schritt 3: Code-Initialisierung

Beginnen Sie mit der Initialisierung des Pfads zu dem Verzeichnis, das Ihre Excel-Dokumente enthält:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Schritt 4: Öffnen der Excel-Datei

 Ein ... kreieren`FileStream` Objekt, das die zu öffnende Excel-Datei enthält:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Instanziieren Sie a`Workbook` Objekt und öffnen Sie die Excel-Datei mit dem Dateistream:

```csharp
Workbook workbook = new Workbook(fstream);
```

## Schritt 5: Zugriff auf die Tabelle

Navigieren Sie zum ersten Arbeitsblatt in der Excel-Datei:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Schritt 6: Anzeigen der Page-By-Vorschau

Aktivieren Sie die Page-by-Vorschau für die Tabelle:

```csharp
worksheet. IsPageBreakPreview = true;
```

## Schritt 7: Änderungen speichern

Speichern Sie die an der Excel-Datei vorgenommenen Änderungen:

```csharp
workbook.Save(dataDir + "output.xls");
```

## Schritt 8: Schließen des Dateistreams

Schließen Sie den Dateistream, um alle Ressourcen freizugeben:

```csharp
fstream.Close();
```

### Beispielquellcode für die Seitenumbruchvorschau des Arbeitsblatts mit Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Erstellen eines Dateistreams, der die zu öffnende Excel-Datei enthält
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanziieren eines Workbook-Objekts
// Öffnen der Excel-Datei über den Dateistream
Workbook workbook = new Workbook(fstream);
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei
Worksheet worksheet = workbook.Worksheets[0];
// Anzeigen des Arbeitsblatts in der Seitenumbruchvorschau
worksheet.IsPageBreakPreview = true;
// Speichern der geänderten Excel-Datei
workbook.Save(dataDir + "output.xls");
// Schließen des Dateistreams, um alle Ressourcen freizugeben
fstream.Close();
```

## Abschluss

In diesem Tutorial haben Sie gelernt, wie Sie mit Aspose.Cells für .NET die Seitenumbruchvorschau eines Arbeitsblatts anzeigen. Indem Sie die beschriebenen Schritte befolgen, können Sie das Erscheinungsbild und Layout Ihrer Excel-Dateien ganz einfach steuern.

### Häufig gestellte Fragen (FAQ)

#### Was ist Aspose.Cells für .NET?

Aspose.Cells für .NET ist eine beliebte Softwarebibliothek zum Bearbeiten von Excel-Dateien in .NET-Anwendungen.

#### Kann ich die Page-By-Vorschau für ein bestimmtes Arbeitsblatt anstelle des gesamten Arbeitsblatts anzeigen?

Ja, mit Aspose.Cells können Sie die Seitenumbruchvorschau für ein bestimmtes Arbeitsblatt aktivieren, indem Sie auf das entsprechende Arbeitsblattobjekt zugreifen.

#### Unterstützt Aspose.Cells andere Funktionen zur Bearbeitung von Excel-Dateien?

Ja, Aspose.Cells bietet eine breite Palette von Funktionen zum Bearbeiten und Bearbeiten von Excel-Dateien, z. B. zum Hinzufügen von Daten, Formatieren, Erstellen von Diagrammen usw.

#### Funktioniert Aspose.Cells nur mit Excel-Dateien im XLS-Format?

Nein, Aspose.Cells unterstützt verschiedene Excel-Dateiformate, einschließlich .xls und .xlsx.
	