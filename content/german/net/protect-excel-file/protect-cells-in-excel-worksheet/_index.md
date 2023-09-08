---
title: Schützen Sie Zellen im Excel-Arbeitsblatt
linktitle: Schützen Sie Zellen im Excel-Arbeitsblatt
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie bestimmte Zellen in Excel mit Aspose.Cells für .NET schützen. Schritt-für-Schritt-Anleitung in C#.
type: docs
weight: 30
url: /de/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
Microsoft Excel ist ein weit verbreitetes Tool zum Erstellen und Verwalten von Tabellenkalkulationen. Eine der Kernfunktionen von Excel ist die Möglichkeit, bestimmte Zellen zu schützen, um die Datenintegrität zu wahren. In diesem Tutorial führen wir Sie Schritt für Schritt durch den Schutz bestimmter Zellen in einer Excel-Tabelle mit Aspose.Cells für .NET. Aspose.Cells für .NET ist eine leistungsstarke Programmierbibliothek, die die Bearbeitung von Excel-Dateien mit großer Flexibilität und erweiterten Funktionen erleichtert. Befolgen Sie die bereitgestellten Schritte, um zu erfahren, wie Sie Ihre wichtigen Zellen schützen und Ihre Daten schützen.

## Schritt 1: Einrichten der Umgebung

Stellen Sie sicher, dass Aspose.Cells für .NET in Ihrer Entwicklungsumgebung installiert ist. Laden Sie die Bibliothek von der offiziellen Website von Aspose herunter und überprüfen Sie die Dokumentation auf Installationsanweisungen.

## Schritt 2: Arbeitsmappe und Arbeitsblatt initialisieren

Zunächst müssen wir eine neue Arbeitsmappe erstellen und den Verweis auf das Arbeitsblatt abrufen, in dem wir die Zellen schützen möchten. Verwenden Sie den folgenden Code:

```csharp
// Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Erstellen Sie das Verzeichnis, falls es noch nicht vorhanden ist.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Erstellen Sie eine neue Arbeitsmappe
Workbook workbook = new Workbook();

// Holen Sie sich das erste Arbeitsblatt
Worksheet sheet = workbook.Worksheets[0];
```

 In diesem Codeausschnitt definieren wir zunächst den Pfad zu dem Verzeichnis, in dem die Excel-Datei gespeichert wird. Als nächstes erstellen wir eine neue Instanz von`Workbook` Klasse und rufen Sie den Verweis auf das erste Arbeitsblatt mithilfe von ab`Worksheets` Eigentum.

## Schritt 3: Zellenstil definieren

Jetzt müssen wir den Stil der Zellen definieren, die wir schützen möchten. Verwenden Sie den folgenden Code:

```csharp
// Definieren Sie das Stilobjekt
Styling styling;

// Gehen Sie alle Spalten im Arbeitsblatt durch und entsperren Sie sie
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

 In diesem Code verwenden wir eine Schleife, um alle Spalten im Arbeitsblatt zu durchlaufen und ihre Zellen zu entsperren, indem wir die Stile festlegen`IsLocked` Eigentum zu`false` . Wir verwenden dann die`ApplyStyle` Methode zum Anwenden des Stils auf die Spalten mit dem`StyleFlag` Flag, um die Zellen zu sperren.

## Schritt 4: Bestimmte Zellen schützen

Jetzt werden wir die spezifischen Zellen schützen, die wir sperren möchten. Verwenden Sie den folgenden Code:

```csharp
// Sperren Sie die drei Zellen: A1, B1, C1
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

 In diesem Code erhalten wir den Stil jeder einzelnen Zelle mithilfe von`GetStyle` Methode, und dann legen wir die fest`IsLocked` Eigenschaft des Stils zu`true`um die Zelle zu verschließen. Abschließend wenden wir den aktualisierten Stil mithilfe von auf jede Zelle an`SetStyle` Methode.

## Schritt 5: Schützen des Arbeitsblatts

Nachdem wir nun die zu schützenden Zellen definiert haben, können wir das Arbeitsblatt selbst schützen. Verwenden Sie den folgenden Code:

```csharp
// Schützen Sie das Arbeitsblatt
leaf.Protect(ProtectionType.All);
```

 Dieser Code verwendet die`Protect` Methode, um das Arbeitsblatt in diesem Fall mit dem angegebenen Schutztyp zu schützen`ProtectionType.All` Dadurch werden alle Elemente im Arbeitsblatt geschützt.

## Schritt 6: Speichern Sie die Excel-Datei

Abschließend speichern wir die Excel-Datei mit den vorgenommenen Änderungen. Verwenden Sie den folgenden Code:

```csharp
// Speichern Sie die Excel-Datei
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

 In diesem Code verwenden wir die`Save` Methode zum Speichern der Arbeitsmappe im angegebenen Verzeichnis mit`Excel97To2003` Format.

### Beispielquellcode für „Zellen im Excel-Arbeitsblatt schützen“ mit Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Erstellen Sie ein Verzeichnis, falls es noch nicht vorhanden ist.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Erstellen Sie eine neue Arbeitsmappe.
Workbook wb = new Workbook();
// Erstellen Sie ein Arbeitsblattobjekt und rufen Sie das erste Blatt ab.
Worksheet sheet = wb.Worksheets[0];
// Definieren Sie das Stilobjekt.
Style style;
// Definieren Sie das Styleflag-Objekt
StyleFlag styleflag;
// Gehen Sie alle Spalten im Arbeitsblatt durch und entsperren Sie sie.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Sperren Sie die drei Zellen ... also A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Zum Schluss schützen Sie das Blatt jetzt.
sheet.Protect(ProtectionType.All);
// Speichern Sie die Excel-Datei.
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## Abschluss

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie mit Aspose.Cells für .NET bestimmte Zellen in einer Excel-Tabelle schützen. Sie können diese Technik jetzt in Ihren eigenen Projekten anwenden und die Sicherheit Ihrer Excel-Dateien verbessern.


### FAQs

#### F: Warum sollte ich Aspose.Cells für .NET verwenden, um Zellen in einer Excel-Tabelle zu schützen?

A: Aspose.Cells für .NET ist eine leistungsstarke Bibliothek, die die Arbeit mit Excel-Dateien erleichtert. Es bietet erweiterte Funktionen zum Schutz von Zellen, zum Entsperren von Bereichen usw.

#### F: Ist es möglich, Zellbereiche statt einzelner Zellen zu schützen?

 A: Ja, Sie können bestimmte zu schützende Zellbereiche definieren`ApplyStyle` Methode mit einem geeigneten`StyleFlag`.

#### F: Wie kann ich die geschützte Excel-Datei öffnen, nachdem ich sie gespeichert habe?

A: Wenn Sie die geschützte Excel-Datei öffnen, müssen Sie das beim Schutz des Arbeitsblatts angegebene Passwort angeben.

#### F: Gibt es andere Arten von Schutz, die ich auf eine Excel-Tabelle anwenden kann?

A: Ja, Aspose.Cells für .NET unterstützt mehrere Schutzarten, z. B. Strukturschutz, Fensterschutz usw. Sie können die geeignete Schutzart entsprechend Ihren Anforderungen auswählen.