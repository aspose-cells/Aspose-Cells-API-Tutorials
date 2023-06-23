---
title: Zeile im Excel-Arbeitsblatt schützen
linktitle: Zeile im Excel-Arbeitsblatt schützen
second_title: Aspose.Cells für .NET API-Referenz
description: Entdecken Sie in diesem Tutorial, wie Sie die Zeilen einer Excel-Tabelle mit Aspose.Cells für .NET schützen. Schritt-für-Schritt-Anleitung in C#.
type: docs
weight: 60
url: /de/net/protect-excel-file/protect-row-in-excel-worksheet/
---
In diesem Tutorial schauen wir uns einen C#-Quellcode an, der die Aspose.Cells-Bibliothek verwendet, um Zeilen in einer Excel-Tabelle zu schützen. Wir gehen jeden Schritt des Codes durch und erklären, wie er funktioniert. Befolgen Sie die Anweisungen sorgfältig, um die gewünschten Ergebnisse zu erzielen.

## Schritt 1: Voraussetzungen

Stellen Sie vor dem Start sicher, dass Sie die Aspose.Cells-Bibliothek für .NET installiert haben. Sie können es von der offiziellen Website von Aspose erhalten. Stellen Sie außerdem sicher, dass Sie über eine aktuelle Version von Visual Studio oder einer anderen C#-Entwicklungsumgebung verfügen.

## Schritt 2: Erforderliche Namespaces importieren

Um die Aspose.Cells-Bibliothek verwenden zu können, müssen wir die erforderlichen Namespaces in unseren Code importieren. Fügen Sie oben in Ihrer C#-Quelldatei die folgenden Zeilen hinzu:

```csharp
using Aspose.Cells;
```

## Schritt 3: Erstellen einer Excel-Arbeitsmappe

In diesem Schritt erstellen wir eine neue Excel-Arbeitsmappe. Verwenden Sie den folgenden Code, um eine Excel-Arbeitsmappe zu erstellen:

```csharp
// Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Erstellen Sie eine neue Arbeitsmappe.
Workbook wb = new Workbook();
```

 Unbedingt austauschen`"YOUR_DOCUMENTS_DIR"` mit dem entsprechenden Pfad zu Ihrem Dokumentenverzeichnis.

## Schritt 4: Erstellen einer Tabelle

Nachdem wir nun die Excel-Arbeitsmappe erstellt haben, erstellen wir ein Arbeitsblatt und erhalten das erste Blatt. Verwenden Sie den folgenden Code:

```csharp
// Erstellen Sie ein Tabellenkalkulationsobjekt und holen Sie sich das erste Blatt.
Worksheet sheet = wb.Worksheets[0];
```

## Schritt 5: Definieren des Stils

In diesem Schritt definieren wir den Stil, der auf die Zeilen der Tabelle angewendet werden soll. Verwenden Sie den folgenden Code:

```csharp
// Definition des Stilobjekts.
Styling styling;
```

## Schritt 6: Schleife, um alle Spalten zu entsperren

Jetzt durchlaufen wir alle Spalten im Arbeitsblatt und entsperren sie. Verwenden Sie den folgenden Code:

```csharp
// Gehen Sie alle Spalten im Arbeitsblatt durch und entsperren Sie sie.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Schritt 7: Sperren der ersten Zeile

In diesem Schritt sperren wir die erste Zeile des Arbeitsblatts. Verwenden Sie den folgenden Code:

```csharp
// Holen Sie sich den Stil der ersten Zeile.
style = sheet.Cells.Rows[0].Style;
// Sperren Sie den Stil.
style. IsLocked = true;
// Wenden Sie den Stil auf die erste Zeile an.
sheet.Cells.ApplyRowStyle(0, style);
```

## Schritt 8: Schützen des Arbeitsblatts

Nachdem wir nun die Stile festgelegt und die Zeilen gesperrt haben, schützen wir die Tabelle. Verwenden Sie den folgenden Code:

```csharp
// Schützen Sie das Arbeitsblatt.
sheet.Protect(ProtectionType.All);
```

## Schritt 9: Speichern der Excel-Datei

Abschließend speichern wir die geänderte Excel-Datei. Verwenden Sie den folgenden Code:

```csharp
// Speichern Sie die Excel-Datei.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Stellen Sie sicher, dass Sie den richtigen Pfad zum Speichern der geänderten Excel-Datei angeben.

### Beispielquellcode für „Zeile im Excel-Arbeitsblatt schützen“ mit Aspose.Cells für .NET 
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
// Definieren Sie das Styleflag-Objekt.
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
// Holen Sie sich den Stil der ersten Zeile.
style = sheet.Cells.Rows[0].Style;
// Verschließe es.
style.IsLocked = true;
//Instanziieren Sie die Flagge.
flag = new StyleFlag();
// Legen Sie die Sperreinstellung fest.
flag.Locked = true;
// Wenden Sie den Stil auf die erste Zeile an.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Schützen Sie das Blatt.
sheet.Protect(ProtectionType.All);
// Speichern Sie die Excel-Datei.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Abschluss

Herzlichen Glückwunsch! Sie verfügen jetzt über C#-Quellcode, der es Ihnen ermöglicht, Zeilen in einer Excel-Tabelle mithilfe der Aspose.Cells-Bibliothek für .NET zu schützen. Befolgen Sie die Schritte sorgfältig und passen Sie den Code an Ihre spezifischen Bedürfnisse an.

### FAQs (häufig gestellte Fragen)

#### Funktioniert dieser Code mit neueren Versionen von Excel?

Ja, dieser Code funktioniert mit neueren Versionen von Excel, einschließlich Dateien im Format Excel 2010 und höher.

#### Kann ich nur bestimmte Zeilen statt aller Zeilen im Arbeitsblatt schützen?

Ja, Sie können den Code ändern, um die spezifischen Zeilen anzugeben, die Sie schützen möchten. Sie müssen die Schleife und die Indizes entsprechend anpassen.

#### Wie kann ich gesperrte Leitungen wieder entsperren?

 Du kannst den ... benutzen`IsLocked` Methode der`Style` Objekt, auf das der Wert gesetzt werden soll`false` und entsperren Sie die Reihen.

#### Ist es möglich, mehrere Arbeitsblätter in derselben Excel-Arbeitsmappe zu schützen?

Ja, Sie können die Schritte zum Erstellen eines Arbeitsblatts, Festlegen des Stils und Schützen für jedes Arbeitsblatt in der Arbeitsmappe wiederholen.

#### Wie kann ich das Passwort für den Tabellenkalkulationsschutz ändern?

 Sie können das Passwort mit ändern`Protect` -Methode und Angabe eines neuen Passworts als Argument.