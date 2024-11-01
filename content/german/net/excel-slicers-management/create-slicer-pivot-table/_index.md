---
title: Erstellen Sie einen Slicer für eine Pivot-Tabelle in Aspose.Cells .NET
linktitle: Erstellen Sie einen Slicer für eine Pivot-Tabelle in Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel-Verarbeitungs-API
description: Erfahren Sie mit unserer Schritt-für-Schritt-Anleitung, wie Sie in Aspose.Cells .NET einen Slicer für Pivot-Tabellen erstellen. Verbessern Sie Ihre Excel-Berichte.
type: docs
weight: 12
url: /de/net/excel-slicers-management/create-slicer-pivot-table/
---
## Einführung
In der heutigen datengesteuerten Welt sind Pivot-Tabellen für die Analyse und Zusammenfassung großer Datensätze von unschätzbarem Wert. Aber warum sollten Sie sich bei der bloßen Zusammenfassung begnügen, wenn Sie Ihre Pivot-Tabellen interaktiver gestalten können? Betreten Sie die Welt der Slicer! Sie sind wie die Fernbedienung für Ihre Excel-Berichte und ermöglichen Ihnen die schnelle und einfache Filterung von Daten. In dieser Anleitung zeigen wir Ihnen, wie Sie mit Aspose.Cells für .NET einen Slicer für eine Pivot-Tabelle erstellen. Also, schnappen Sie sich eine Tasse Kaffee, machen Sie es sich bequem und legen Sie los!
## Voraussetzungen
Bevor Sie beginnen, müssen Sie einige Voraussetzungen beachten:
1.  Aspose.Cells für .NET: Stellen Sie sicher, dass Sie Aspose.Cells in Ihrem Projekt installiert haben. Sie erhalten es von[Download-Seite](https://releases.aspose.com/cells/net/).
2. Visual Studio oder eine andere IDE: Sie benötigen eine IDE, in der Sie Ihre .NET-Projekte erstellen und ausführen können. Visual Studio ist eine beliebte Wahl.
3. Grundkenntnisse in C#: Wenn Sie ein wenig C# kennen, können Sie die Codierungsteile problemlos bewältigen.
4. Beispiel-Excel-Datei: Für dieses Tutorial benötigen Sie eine Beispiel-Excel-Datei mit einer Pivot-Tabelle. Wir verwenden eine Datei namens`sampleCreateSlicerToPivotTable.xlsx`.
Nachdem Sie nun alle Kästchen aktiviert haben, importieren wir die erforderlichen Pakete!
## Pakete importieren
Um Aspose.Cells effektiv zu nutzen, müssen Sie die folgenden Pakete in Ihr Projekt importieren:
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
Stellen Sie sicher, dass Sie dies oben in Ihrer Codedatei hinzufügen. Mit dieser Importanweisung können Sie auf alle von der Aspose.Cells-Bibliothek angebotenen Funktionen zugreifen.
Kommen wir nun zum Wesentlichen. Wir unterteilen es in überschaubare Schritte, damit Sie es leicht nachvollziehen können. 
## Schritt 1: Quell- und Ausgabeverzeichnisse definieren
Als Erstes müssen wir definieren, wo sich Ihre Eingabe- und Ausgabedateien befinden. Dadurch wird sichergestellt, dass unser Code weiß, wo unsere Excel-Datei zu finden ist und wo die Ergebnisse gespeichert werden sollen.
```csharp
// Quellverzeichnis
string sourceDir = "Your Document Directory"; // Geben Sie Ihren Quellverzeichnispfad an
// Ausgabeverzeichnis
string outputDir = "Your Document Directory"; // Geben Sie Ihren Ausgabeverzeichnispfad an
```
 Erklärung: In diesem Schritt deklarieren Sie einfach Variablen für die Quell- und Ausgabeverzeichnisse. Ersetzen Sie`"Your Document Directory"`mit dem tatsächlichen Verzeichnis, in dem sich Ihre Dateien befinden.
## Schritt 2: Laden Sie die Arbeitsmappe
Als Nächstes laden wir die Excel-Arbeitsmappe, die die Pivot-Tabelle enthält. 
```csharp
// Laden Sie eine Beispiel-Excel-Datei mit einer Pivot-Tabelle.
Workbook wb = new Workbook(sourceDir + "sampleCreateSlicerToPivotTable.xlsx");
```
 Erklärung: Hier erstellen wir eine Instanz des`Workbook` Klasse, wobei der Pfad zur Excel-Datei übergeben wird. Mit dieser Codezeile können wir auf die Arbeitsmappe zugreifen und sie bearbeiten.
## Schritt 3: Zugriff auf das erste Arbeitsblatt
Nachdem wir die Arbeitsmappe geladen haben, müssen wir auf das Arbeitsblatt zugreifen, in dem sich unsere Pivot-Tabelle befindet.
```csharp
// Greifen Sie auf das erste Arbeitsblatt zu.
Worksheet ws = wb.Worksheets[0];
```
Erklärung: Arbeitsblätter in Aspose.Cells sind nullindiziert, was bedeutet, dass das erste Blatt den Index 0 hat. Mit dieser Zeile erhalten wir unser Arbeitsblattobjekt zur weiteren Bearbeitung.
## Schritt 4: Zugriff auf die Pivot-Tabelle
Wir kommen näher! Nehmen wir die Pivot-Tabelle, mit der wir den Slicer verknüpfen möchten.
```csharp
// Greifen Sie auf die erste Pivot-Tabelle im Arbeitsblatt zu.
Aspose.Cells.Pivot.PivotTable pt = ws.PivotTables[0];
```
Erklärung: Ähnlich wie Arbeitsblätter werden auch Pivot-Tabellen indiziert. Diese Zeile zieht die erste Pivot-Tabelle aus dem Arbeitsblatt, damit wir unseren Slicer hinzufügen können.
## Schritt 5: Einen Slicer hinzufügen
Jetzt kommt der spannende Teil – das Hinzufügen des Slicers! Dieser Schritt bindet den Slicer an unser PivotTable-Basisfeld.
```csharp
// Fügen Sie einen Slicer zur Pivot-Tabelle mit dem ersten Basisfeld in Zelle B22 hinzu.
int idx = ws.Slicers.Add(pt, "B22", pt.BaseFields[0]);
```
 Erklärung: Hier fügen wir den Slicer hinzu, indem wir die Position (Zelle B22) und das Basisfeld aus der Pivot-Tabelle (das erste) angeben. Die Methode gibt einen Index zurück, den wir speichern in`idx` zum späteren Nachschlagen.
## Schritt 6: Zugriff auf den neu hinzugefügten Slicer
Sobald der Slicer erstellt ist, empfiehlt es sich, einen Verweis darauf zu haben, insbesondere wenn Sie später weitere Änderungen vornehmen möchten.
```csharp
// Greifen Sie über die Slicer-Sammlung auf den neu hinzugefügten Slicer zu.
Aspose.Cells.Slicers.Slicer slicer = ws.Slicers[idx];
```
Erklärung: Mit dem Index des neu erstellten Slicers können wir nun direkt aus der Slicer-Sammlung des Arbeitsblattes darauf zugreifen.
## Schritt 7: Speichern Sie die Arbeitsmappe
Endlich ist es Zeit, Ihre harte Arbeit zu speichern! Sie können die Arbeitsmappe in verschiedenen Formaten speichern.
```csharp
// Speichern Sie die Arbeitsmappe im Ausgabeformat XLSX.
wb.Save(outputDir + "outputCreateSlicerToPivotTable.xlsx", SaveFormat.Xlsx);
// Speichern Sie die Arbeitsmappe im Ausgabeformat XLSB.
wb.Save(outputDir + "outputCreateSlicerToPivotTable.xlsb", SaveFormat.Xlsb);
```
Erklärung: In diesem Schritt speichern wir die Arbeitsmappe sowohl im XLSX- als auch im XLSB-Format. Dadurch haben Sie je nach Bedarf verschiedene Optionen.
## Schritt 8: Ausführen des Codes
Als Sahnehäubchen teilen wir dem Benutzer mit, dass alles erfolgreich ausgeführt wurde!
```csharp
Console.WriteLine("CreateSlicerToPivotTable executed successfully.");
```
Erklärung: Eine einfache Konsolenmeldung, um den Benutzer zu versichern, dass alles ohne Fehler abgeschlossen wurde.
## Abschluss
Und da haben Sie es! Sie haben erfolgreich einen Slicer für eine Pivot-Tabelle mit Aspose.Cells für .NET erstellt. Diese kleine Funktion kann die Interaktivität Ihrer Excel-Berichte erheblich steigern und sie benutzerfreundlich und optisch ansprechend machen.
Wenn Sie mitgelesen haben, sollte das Erstellen und Bearbeiten von Pivot-Tabellen mit Slicern jetzt ein Kinderspiel für Sie sein. Hat Ihnen dieses Tutorial gefallen? Ich hoffe, es hat Ihr Interesse geweckt, die Funktionen von Aspose.Cells näher zu erkunden!
## Häufig gestellte Fragen
### Was ist ein Slicer in Excel?
Ein Slicer ist ein visueller Filter, mit dem Benutzer Daten schnell aus einer Pivot-Tabelle filtern können.
### Kann ich einer Pivot-Tabelle mehrere Slicer hinzufügen?
Ja, Sie können einer Pivot-Tabelle für verschiedene Felder beliebig viele Slicer hinzufügen.
### Ist die Nutzung von Aspose.Cells kostenlos?
Aspose.Cells ist eine kostenpflichtige Bibliothek, Sie können sie jedoch während der Testphase kostenlos ausprobieren.
### Wo finde ich weitere Aspose.Cells-Dokumentation?
 Sie können die[Aspose.Cells-Dokumentation](https://reference.aspose.com/cells/net/) für weitere Details.
### Gibt es eine Möglichkeit, Support für Aspose.Cells zu erhalten?
 Auf jeden Fall! Sie erreichen uns unter[Asposes Forum](https://forum.aspose.com/c/cells/9).