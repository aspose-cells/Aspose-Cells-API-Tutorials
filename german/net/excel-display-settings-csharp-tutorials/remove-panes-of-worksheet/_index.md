---
title: Entfernen Sie Bereiche des Arbeitsblatts
linktitle: Entfernen Sie Bereiche des Arbeitsblatts
second_title: Aspose.Cells für .NET API-Referenz
description: Schritt-für-Schritt-Anleitung zum Entfernen von Bereichen aus einem Excel-Arbeitsblatt mit Aspose.Cells für .NET.
type: docs
weight: 120
url: /de/net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
In diesem Tutorial erklären wir, wie Sie mit Aspose.Cells für .NET Bereiche aus einem Excel-Arbeitsblatt entfernen. Befolgen Sie diese Schritte, um das gewünschte Ergebnis zu erhalten:

## Schritt 1: Einrichten der Umgebung

Stellen Sie sicher, dass Sie Aspose.Cells für .NET installiert und Ihre Entwicklungsumgebung eingerichtet haben. Stellen Sie außerdem sicher, dass Sie über eine Kopie der Excel-Datei verfügen, aus der Sie die Fenster entfernen möchten.

## Schritt 2: Importieren Sie die erforderlichen Abhängigkeiten

Fügen Sie die erforderlichen Anweisungen hinzu, um die Klassen von Aspose.Cells zu verwenden:

```csharp
using Aspose.Cells;
```

## Schritt 3: Code-Initialisierung

Beginnen Sie mit der Initialisierung des Pfads zu dem Verzeichnis, das Ihre Excel-Dokumente enthält:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Schritt 4: Öffnen der Excel-Datei

 Instanziieren Sie eine neue`Workbook` Objekt und öffnen Sie die Excel-Datei mit dem`Open` Methode:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Schritt 5: Definieren Sie die aktive Zelle

 Legen Sie die aktive Zelle des Arbeitsblatts mit fest`ActiveCell` Eigentum:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Schritt 6: Löschen der Fenster

 Entfernen Sie mithilfe von Fensterbereiche aus dem Arbeitsblattfenster`RemoveSplit` Methode:

```csharp
book.Worksheets[0].RemoveSplit();
```

## Schritt 7: Änderungen speichern

Speichern Sie die an der Excel-Datei vorgenommenen Änderungen:

```csharp
book.Save(dataDir + "output.xls");
```

### Beispielquellcode zum Entfernen von Arbeitsblattbereichen mit Aspose.Cells für .NET 
```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Instanziieren Sie eine neue Arbeitsmappe und öffnen Sie eine Vorlagendatei
Workbook book = new Workbook(dataDir + "Book1.xls");
// Legen Sie die aktive Zelle fest
book.Worksheets[0].ActiveCell = "A20";
// Teilen Sie das Arbeitsblattfenster
book.Worksheets[0].RemoveSplit();
// Speichern Sie die Excel-Datei
book.Save(dataDir + "output.xls");
```

## Abschluss

In diesem Tutorial haben Sie gelernt, wie Sie mit Aspose.Cells für .NET Bereiche aus einem Excel-Arbeitsblatt entfernen. Indem Sie die beschriebenen Schritte befolgen, können Sie das Erscheinungsbild und Verhalten Ihrer Excel-Dateien ganz einfach anpassen.

### Häufig gestellte Fragen (FAQ)

#### Was ist Aspose.Cells für .NET?

Aspose.Cells für .NET ist eine beliebte Softwarebibliothek zum Bearbeiten von Excel-Dateien in .NET-Anwendungen.

#### Wie kann ich die aktive Zelle eines Arbeitsblatts in Aspose.Cells festlegen?

 Sie können die aktive Zelle mit festlegen`ActiveCell` Eigenschaft des Worksheet-Objekts.

#### Kann ich nur horizontale oder vertikale Bereiche aus dem Arbeitsblattfenster entfernen?

 Ja, mit Aspose.Cells können Sie nur horizontale oder vertikale Fenster mit den entsprechenden Methoden entfernen, z`RemoveHorizontalSplit` oder`RemoveVerticalSplit`.

#### Funktioniert Aspose.Cells nur mit Excel-Dateien im XLS-Format?

Nein, Aspose.Cells unterstützt verschiedene Excel-Dateiformate, einschließlich .xls und .xlsx.
	