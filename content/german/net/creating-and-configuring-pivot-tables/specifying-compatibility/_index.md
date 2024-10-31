---
title: Kompatibilität von Excel-Dateien programmgesteuert in .NET angeben
linktitle: Kompatibilität von Excel-Dateien programmgesteuert in .NET angeben
second_title: Aspose.Cells .NET Excel-Verarbeitungs-API
description: Erfahren Sie, wie Sie Excel-Pivot-Tabellen mit Aspose.Cells für .NET bearbeiten, einschließlich Datenaktualisierungen, Kompatibilitätseinstellungen und Zellenformatierung.
type: docs
weight: 23
url: /de/net/creating-and-configuring-pivot-tables/specifying-compatibility/
---
## Einführung

In der heutigen datengesteuerten Welt ist die programmgesteuerte Verwaltung und Bearbeitung von Excel-Dateien für viele Entwickler unverzichtbar geworden. Wenn Sie mit Excel in .NET arbeiten, ist Aspose.Cells eine leistungsstarke Bibliothek, die das Erstellen, Lesen, Ändern und Speichern von Excel-Dateien erleichtert. Eine wichtige Funktion dieser Bibliothek ermöglicht es Ihnen, die Kompatibilität von Excel-Dateien programmgesteuert festzulegen. In diesem Tutorial erfahren Sie, wie Sie Excel-Dateien bearbeiten können, wobei wir uns insbesondere auf die Verwaltung der Kompatibilität mit Aspose.Cells für .NET konzentrieren. Am Ende werden Sie verstehen, wie Sie die Kompatibilität für Excel-Dateien, insbesondere für Pivot-Tabellen, festlegen, während Sie Daten aktualisieren und verwalten.

## Voraussetzungen

Bevor Sie mit der Codierungsphase beginnen, stellen Sie sicher, dass Sie über Folgendes verfügen:

1. Grundkenntnisse in C#: Da wir Code in C# schreiben, hilft Ihnen die Vertrautheit mit der Sprache dabei, das Tutorial besser zu verstehen.
2.  Aspose.Cells für .NET-Bibliothek: Sie können es herunterladen von der[Aspose Cells veröffentlicht Seite](https://releases.aspose.com/cells/net/)Wenn Sie dies noch nicht getan haben, sollten Sie zunächst eine kostenlose Testversion erwerben, um die Funktionen kennenzulernen.
3. Visual Studio: Eine IDE, in der Sie Ihren C#-Code effektiv schreiben und testen können.
4.  Beispiel-Excel-Datei: Stellen Sie sicher, dass Sie eine Beispiel-Excel-Datei haben, vorzugsweise eine, die eine Pivot-Tabelle für die Demo enthält. Für unser Beispiel verwenden wir`sample-pivot-table.xlsx`.

Nachdem diese Voraussetzungen erfüllt sind, können wir mit dem Codierungsprozess beginnen.

## Pakete importieren

Bevor Sie mit dem Schreiben Ihrer Anwendung beginnen, müssen Sie die erforderlichen Namespaces in Ihren Code aufnehmen, um die Aspose.Cells-Bibliothek effektiv nutzen zu können. So geht's.

### Aspose.Cells-Namespace importieren

```csharp
using System.IO;
using System;
using Aspose.Cells;
using Aspose.Cells.Pivot;
using System.Drawing;
```

Diese Codezeile stellt sicher, dass Sie auf alle Klassen und Methoden innerhalb der Aspose.Cells-Bibliothek zugreifen können.

Lassen Sie uns nun den Prozess im Detail aufschlüsseln, um sicherzustellen, dass alles klar und verständlich ist.

## Schritt 1: Richten Sie Ihr Verzeichnis ein

Richten Sie zunächst das Verzeichnis ein, in dem sich Ihre Excel-Dateien befinden. Es ist wichtig, den richtigen Dateipfad anzugeben.

```csharp
// Der Pfad zum Dokumentverzeichnis.
string dataDir = "Your Document Directory";
```

 Ersetzen Sie hier`"Your Document Directory"`durch den tatsächlichen Pfad zu Ihren Excel-Dateien. Hier sollte sich Ihre Beispiel-PivotTable-Datei befinden.

## Schritt 2: Laden Sie die Excel-Quelldatei

Als Nächstes müssen wir die Excel-Datei laden, die die Beispiel-Pivot-Tabelle enthält. 

```csharp
// Quell-Excel-Datei mit Beispiel-Pivot-Tabelle laden
Workbook wb = new Workbook(dataDir + "sample-pivot-table.xlsx");
```

 In diesem Schritt erstellen wir eine Instanz des`Workbook` Klasse, die die angegebene Excel-Datei lädt. 

## Schritt 3: Zugriff auf die Arbeitsblätter

Nachdem die Arbeitsmappe geladen ist, müssen Sie auf das Arbeitsblatt zugreifen, das die PivotTable-Daten enthält.

```csharp
// Greifen Sie auf das erste Arbeitsblatt zu, das PivotTable-Daten enthält
Worksheet dataSheet = wb.Worksheets[0];
```

Hier greifen wir auf das erste Arbeitsblatt zu, in dem sich die Pivot-Tabelle befindet. Sie können je nach Ihrer Excel-Struktur auch eine Schleife durchlaufen oder weitere Arbeitsblätter angeben.

## Schritt 4: Zelldaten manipulieren

Als Nächstes ändern Sie einige Zellenwerte im Arbeitsblatt. 

### Schritt 4.1: Zelle A3 ändern

Beginnen wir mit dem Zugriff auf Zelle A3 und dem Festlegen ihres Werts.

```csharp
// Greifen Sie auf Zelle A3 zu und legen Sie deren Daten fest
Cells cells = dataSheet.Cells;
Cell cell = cells["A3"];
cell.PutValue("FooBar");
```

Dieser Codeausschnitt aktualisiert Zelle A3 mit dem Wert „FooBar“.

### Schritt 4.2: Zelle B3 mit langer Zeichenfolge ändern

Lassen Sie uns nun eine lange Zeichenfolge in Zelle B3 einfügen, die die Standardzeichenbegrenzungen von Excel überschreitet.

```csharp
// Greifen Sie auf Zelle B3 zu, setzen Sie deren Daten
string longStr = "Very long text 1. very long text 2.... [continue your long string]";
cell = cells["B3"];
cell.PutValue(longStr);
```

Dieser Code ist wichtig, da er Ihre Erwartungen hinsichtlich der Datengrenzen festlegt, insbesondere beim Arbeiten mit Kompatibilitätseinstellungen in Excel.

## Schritt 5: Überprüfen Sie die Länge der Zelle B3

Außerdem muss unbedingt die Länge der eingegebenen Zeichenfolge bestätigt werden.

```csharp
// Drucken Sie die Länge der Zeichenfolge in Zelle B3
Console.WriteLine("Length of original data string: " + cell.StringValue.Length);
```

Dies dient lediglich zur Überprüfung, um anzuzeigen, wie viele Zeichen auf Ihrem Handy gespeichert sind.

## Schritt 6: Andere Zellenwerte festlegen

Jetzt greifen wir auf weitere Zellen zu und legen einige Werte fest.

```csharp
// Greifen Sie auf Zelle C3 zu und legen Sie deren Daten fest
cell = cells["C3"];
cell.PutValue("closed");

// Greifen Sie auf Zelle D3 zu und legen Sie deren Daten fest
cell = cells["D3"];
cell.PutValue("2016/07/21");
```

Jeder dieser Snippets aktualisiert mehrere zusätzliche Zellen im Arbeitsblatt.

## Schritt 7: Zugriff auf die Pivot-Tabelle

Als Nächstes greifen Sie auf das zweite Arbeitsblatt zu, das aus den PivotTable-Daten besteht.

```csharp
//Greifen Sie auf das zweite Arbeitsblatt zu, das die Pivot-Tabelle enthält
Worksheet pivotSheet = wb.Worksheets[1];

// Zugriff auf die Pivot-Tabelle
PivotTable pivotTable = pivotSheet.PivotTables[0];
```

Mit diesem Snippet können Sie die Pivot-Tabelle hinsichtlich der Kompatibilitätseinstellungen bearbeiten.

## Schritt 8: Kompatibilität für Excel 2003 festlegen

Es ist wichtig festzulegen, ob Ihre Pivot-Tabelle mit Excel 2003 kompatibel ist oder nicht. 

```csharp
// Die Eigenschaft IsExcel2003Compatible gibt an, ob PivotTable beim Aktualisieren der PivotTable mit Excel2003 kompatibel ist.
pivotTable.IsExcel2003Compatible = true;
pivotTable.RefreshData();
pivotTable.CalculateData();
```

 Hier beginnt die eigentliche Transformation. Indem wir`IsExcel2003Compatible` Zu`true`, begrenzen Sie die Zeichenlänge beim Aktualisieren auf 255.

## Schritt 9: Länge nach Kompatibilitätseinstellung prüfen

Nachdem wir die Kompatibilität eingestellt haben, sehen wir uns an, welche Auswirkungen dies auf die Daten hat.

```csharp
// Überprüfen Sie den Wert der Zelle B5 des Pivot-Sheets.
Cell b5 = pivotSheet.Cells["B5"];
Console.WriteLine("Length of cell B5 after setting IsExcel2003Compatible property to True: " + b5.StringValue.Length);
```

Wenn die ursprünglichen Daten mehr als 255 Zeichen umfassen, wird wahrscheinlich eine Ausgabe angezeigt, die den Kürzungseffekt bestätigt.

## Schritt 10: Kompatibilitätseinstellungen ändern

Ändern wir jetzt die Kompatibilitätseinstellung und überprüfen Sie es erneut.

```csharp
//Setzen Sie nun die Eigenschaft IsExcel2003Compatible auf false und aktualisieren Sie erneut
pivotTable.IsExcel2003Compatible = false;
pivotTable.RefreshData();
pivotTable.CalculateData();
```

Dadurch wird die ursprüngliche Länge Ihrer Daten ohne die vorherigen Einschränkungen wiedergegeben.

## Schritt 11: Länge erneut überprüfen 

Lassen Sie uns überprüfen, ob die Daten jetzt ihre tatsächliche Länge genau wiedergeben.

```csharp
// Jetzt wird die ursprüngliche Länge der Zellendaten gedruckt. Die Daten wurden jetzt nicht abgeschnitten.
b5 = pivotSheet.Cells["B5"];
Console.WriteLine("Length of cell B5 after setting IsExcel2003Compatible property to False: " + b5.StringValue.Length);
```

Sie sollten sehen, dass die Ausgabe die Entfernung der Kürzung bestätigt.

## Schritt 12: Formatieren Sie die Zellen

Um das visuelle Erlebnis zu verbessern, möchten Sie möglicherweise die Zellen formatieren. 

```csharp
// Legen Sie die Zeilenhöhe und Spaltenbreite der Zelle B5 fest und umbrechen Sie deren Text
pivotSheet.Cells.SetRowHeight(b5.Row, 100);
pivotSheet.Cells.SetColumnWidth(b5.Column, 65);
Style st = b5.GetStyle();
st.IsTextWrapped = true;
b5.SetStyle(st);
```

Diese Codezeilen erleichtern die Lesbarkeit der Daten, indem sie die Zellenabmessungen anpassen und den Textumbruch aktivieren.

## Schritt 13: Speichern Sie die Arbeitsmappe

Speichern Sie abschließend Ihre Arbeitsmappe mit den vorgenommenen Änderungen.

```csharp
// Arbeitsmappe im XLSX-Format speichern
wb.Save(dataDir + "SpecifyCompatibility_out.xlsx", SaveFormat.Xlsx);
```

 Die Wahl eines geeigneten Dateiformats ist beim Speichern von Excel-Dateien von entscheidender Bedeutung.`Xlsx`Das Format wird häufig verwendet und ist mit vielen Excel-Versionen kompatibel.

## Abschluss

Herzlichen Glückwunsch! Sie haben jetzt Kompatibilitätseinstellungen für Excel-Dateien mit Aspose.Cells für .NET programmiert. In diesem Tutorial wurde jeder Schritt beschrieben, vom Einrichten Ihrer Umgebung bis zum Ändern der Kompatibilitätseinstellungen für Pivot-Tabellen. Wenn Sie jemals mit Daten gearbeitet haben, die bestimmte Einschränkungen oder Kompatibilität erforderten, ist dies eine Fähigkeit, die Sie nicht missen möchten.

## Häufig gestellte Fragen

### Was ist Aspose.Cells?  
Aspose.Cells ist eine .NET-Bibliothek, die Entwicklern das nahtlose Erstellen, Bearbeiten und Konvertieren von Excel-Dateien erleichtern soll.

### Warum ist Excel-Kompatibilität wichtig?  
Die Excel-Kompatibilität ist von entscheidender Bedeutung, um sicherzustellen, dass Dateien in den vorgesehenen Excel-Versionen geöffnet und verwendet werden können, insbesondere wenn sie Funktionen oder Formate enthalten, die in früheren Versionen nicht unterstützt wurden.

### Kann ich mit Aspose.Cells programmgesteuert Pivot-Tabellen erstellen?  
Ja, Sie können Pivot-Tabellen programmgesteuert mit Aspose.Cells erstellen und bearbeiten. Die Bibliothek bietet verschiedene Methoden zum Hinzufügen von Datenquellen, Feldern und Funktionen, die mit Pivot-Tabellen verknüpft sind.

### Wie überprüfe ich die Länge einer Zeichenfolge in einer Excel-Zelle?  
Sie können die`StringValue` Eigentum eines`Cell` Objekt, um den Inhalt der Zelle zu erhalten und dann den`.Length` -Eigenschaft, um die Länge der Zeichenfolge herauszufinden.

### Kann ich die Zellenformatierung über Zeilenhöhe und -breite hinaus anpassen?  
 Absolut! Aspose.Cells ermöglicht eine umfangreiche Zellformatierung. Sie können Schriftarten, Farben, Rahmen, Zahlenformate und vieles mehr über das`Style` Klasse.