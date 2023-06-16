---
title: Spalte im Excel-Arbeitsblatt schützen
linktitle: Spalte im Excel-Arbeitsblatt schützen
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie eine bestimmte Spalte in Excel mit Aspose.Cells für .NET schützen. Detaillierte Schritte und Quellcode enthalten.
type: docs
weight: 40
url: /de/net/protect-excel-file/protect-column-in-excel-worksheet/
---
Microsoft Excel ist eine beliebte Anwendung zum Verwalten und Analysieren von Daten in Form von Tabellenkalkulationen. Der Schutz sensibler Daten ist unerlässlich, um die Integrität und Vertraulichkeit von Informationen zu gewährleisten. In diesem Tutorial führen wir Sie Schritt für Schritt durch den Schutz einer bestimmten Spalte in einer Excel-Tabelle mithilfe der Bibliothek Aspose.Cells für .NET. Aspose.Cells für .NET bietet leistungsstarke Funktionen für die Handhabung und den Schutz von Excel-Dateien. Befolgen Sie die angegebenen Schritte, um zu erfahren, wie Sie Ihre Daten in einer bestimmten Spalte und Ihre Excel-Tabelle schützen.
## Schritt 1: Verzeichniseinrichtung

Definieren Sie zunächst das Verzeichnis, in dem Sie die Excel-Datei speichern möchten. Verwenden Sie den folgenden Code:

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Erstellen Sie das Verzeichnis, falls es nicht vorhanden ist.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);
```

Dieser Code prüft, ob das Verzeichnis bereits existiert und erstellt es, falls nicht.

## Schritt 2: Erstellen einer neuen Arbeitsmappe

Als nächstes erstellen wir eine neue Excel-Arbeitsmappe und erhalten das erste Arbeitsblatt. Verwenden Sie den folgenden Code:

```csharp
// Erstellen Sie eine neue Arbeitsmappe.
Workbook workbook = new Workbook();
// Erstellen Sie ein Tabellenkalkulationsobjekt und holen Sie sich das erste Blatt.
Worksheet sheet = workbook.Worksheets[0];
```

 Dieser Code erstellt einen neuen`Workbook` Objekt und ruft das erste Arbeitsblatt mit ab`Worksheets[0]`.

## Schritt 3: Spalten entsperren

Um alle Spalten im Arbeitsblatt zu entsperren, verwenden wir eine Schleife, um alle Spalten zu durchlaufen und einen Entsperrstil anzuwenden. Verwenden Sie den folgenden Code:

```csharp
// Stilobjekt festlegen.
Styling styling;
// Legen Sie das Styleflag-Objekt fest.
StyleFlag flag;
// Gehen Sie alle Spalten im Arbeitsblatt durch und entsperren Sie sie.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

 Dieser Code durchläuft jede Spalte im Arbeitsblatt und entsperrt den Stil durch Einstellung`IsLocked` Zu`false`.

## Schritt 4: Sperren einer bestimmten Spalte

Jetzt werden wir eine bestimmte Spalte sperren, indem wir einen gesperrten Stil anwenden. Verwenden Sie den folgenden Code:

```csharp
// Holen Sie sich den Stil der ersten Spalte.
style = sheet.Cells.Columns[0].Style;
// Verschließe es.
style. IsLocked = true;
// Instanziieren Sie das Flag-Objekt.
flag = new StyleFlag();
// Legen Sie den Sperrparameter fest.
flag. Locked = true;
// Wenden Sie den Stil auf die erste Spalte an.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

 Dieser Code wählt die erste Spalte mit aus`Columns[0]` , legt dann den Stil fest`IsLocked` Zu`true` um die Spalte zu sperren. Schließlich wenden wir den Stil mithilfe von auf die erste Spalte an`ApplyStyle` Methode.

## Schritt 5: Schützen des Arbeitsblatts

Nachdem wir nun die spezifische Spalte gesperrt haben, können wir das Arbeitsblatt selbst schützen. Verwenden Sie den folgenden Code:



```csharp
// Schützen Sie das Arbeitsblatt.
leaf.Protect(ProtectionType.All);
```

 Dieser Code verwendet die`Protect` Methode zum Schutz des Arbeitsblatts durch Angabe des Schutztyps.

## Schritt 6: Speichern der Excel-Datei

Abschließend speichern wir die Excel-Datei unter dem gewünschten Verzeichnispfad und Dateinamen. Verwenden Sie den folgenden Code:

```csharp
// Speichern Sie die Excel-Datei.
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

 Dieser Code verwendet die`Save` Methode der`Workbook` Objekt, um die Excel-Datei mit dem angegebenen Namen und Dateiformat zu speichern.

### Beispielquellcode für „Spalte im Excel-Arbeitsblatt schützen“ mit Aspose.Cells für .NET 
```csharp
// Der Pfad zum Dokumentenverzeichnis.
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
//Definieren Sie das Styleflag-Objekt.
StyleFlag flag;
// Gehen Sie alle Spalten im Arbeitsblatt durch und entsperren Sie sie.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Holen Sie sich den Stil der ersten Spalte.
style = sheet.Cells.Columns[0].Style;
// Verschließe es.
style.IsLocked = true;
// Instanziieren Sie die Flagge.
flag = new StyleFlag();
// Legen Sie die Sperreinstellung fest.
flag.Locked = true;
// Wenden Sie den Stil auf die erste Spalte an.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
// Schützen Sie das Blatt.
sheet.Protect(ProtectionType.All);
// Speichern Sie die Excel-Datei.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Abschluss

Sie haben gerade eine Schritt-für-Schritt-Anleitung zum Schützen einer Spalte in einer Excel-Tabelle mit Aspose.Cells für .NET befolgt. Sie haben gelernt, wie Sie alle Spalten entsperren, eine bestimmte Spalte sperren und das Arbeitsblatt selbst schützen. Jetzt können Sie diese Konzepte auf Ihre eigenen Projekte anwenden und Ihre Excel-Daten sichern.

## Häufig gestellte Fragen

#### F: Warum ist es wichtig, bestimmte Spalten in einer Excel-Tabelle zu schützen?

A: Der Schutz bestimmter Spalten in einer Excel-Tabelle trägt dazu bei, den Zugriff und die Änderung vertraulicher Daten einzuschränken und so die Integrität und Vertraulichkeit der Informationen sicherzustellen.

#### F: Unterstützt Aspose.Cells für .NET andere Funktionen zur Verarbeitung von Excel-Dateien?

A: Ja, Aspose.Cells für .NET bietet eine breite Palette von Funktionen, darunter das Erstellen, Bearbeiten, Konvertieren und Berichten von Excel-Dateien.

#### F: Wie kann ich alle Spalten in einer Excel-Tabelle entsperren?

A: In Aspose.Cells für .NET können Sie eine Schleife verwenden, um alle Spalten zu durchlaufen, und den Sperrstil auf „false“ setzen, um alle Spalten zu entsperren.

#### F: Wie kann ich eine Excel-Tabelle mit Aspose.Cells für .NET schützen?

 A: Sie können das verwenden`Protect` Methode des Arbeitsblattobjekts zum Schutz des Blatts mit verschiedenen Schutzstufen wie Strukturschutz, Zellschutz usw.

#### F: Kann ich diese Spaltenschutzkonzepte in anderen Arten von Excel-Dateien anwenden?

A: Ja, die Spaltenschutzkonzepte in Aspose.Cells für .NET gelten für alle Arten von Excel-Dateien, z. B. Excel 97-2003-Dateien (.xls) und neuere Excel-Dateien (.xlsx).