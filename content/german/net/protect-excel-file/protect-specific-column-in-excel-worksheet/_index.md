---
title: Schützen Sie eine bestimmte Spalte im Excel-Arbeitsblatt
linktitle: Schützen Sie eine bestimmte Spalte im Excel-Arbeitsblatt
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET eine bestimmte Spalte in einer Excel-Tabelle schützen. Schritt-für-Schritt-Anleitung in C#.
type: docs
weight: 80
url: /de/net/protect-excel-file/protect-specific-column-in-excel-worksheet/
---
Beim Arbeiten mit Excel-Arbeitsblättern in C# ist es häufig erforderlich, bestimmte Spalten zu schützen, um versehentliche Änderungen zu verhindern. In diesem Tutorial führen wir Sie durch den Prozess des Schutzes einer bestimmten Spalte in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells für .NET-Bibliothek. Wir erklären Ihnen Schritt für Schritt den für diese Aufgabe erforderlichen C#-Quellcode. Also lasst uns anfangen!

## Übersicht über den Schutz bestimmter Spalten in einem Excel-Arbeitsblatt

Durch den Schutz bestimmter Spalten in einem Excel-Arbeitsblatt wird sichergestellt, dass diese Spalten gesperrt bleiben und nicht ohne entsprechende Autorisierung geändert werden können. Dies ist besonders nützlich, wenn Sie den Bearbeitungszugriff auf bestimmte Daten oder Formeln einschränken und Benutzern gleichzeitig die Interaktion mit dem Rest des Arbeitsblatts ermöglichen möchten. Die Aspose.Cells for .NET-Bibliothek bietet einen umfassenden Satz an Funktionen zur programmgesteuerten Bearbeitung von Excel-Dateien, einschließlich Spaltenschutz.

## Einrichten der Umgebung

Bevor wir beginnen, stellen Sie sicher, dass die Aspose.Cells for .NET-Bibliothek in Ihrer Entwicklungsumgebung installiert ist. Sie können die Bibliothek von der offiziellen Aspose-Website herunterladen und mit dem bereitgestellten Installationsprogramm installieren.

## Erstellen einer neuen Arbeitsmappe und eines neuen Arbeitsblatts

Um mit dem Schutz bestimmter Spalten zu beginnen, müssen wir mit Aspose.Cells für .NET eine neue Arbeitsmappe und ein neues Arbeitsblatt erstellen. Hier ist der Codeausschnitt:

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
```

Stellen Sie sicher, dass Sie „IHR DOKUMENTVERZEICHNIS“ durch den tatsächlichen Verzeichnispfad ersetzen, in dem Sie die Excel-Datei speichern möchten.

## Definieren der Stil- und Stilflaggenobjekte

Um bestimmte Stile und Schutzflags für die Spalten festzulegen, müssen wir die Stil- und Stilflagobjekte definieren. Hier ist der Codeausschnitt:

```csharp
// Definieren Sie das Stilobjekt.
Style style;

// Definieren Sie das Style-Flag-Objekt.
StyleFlag flag;
```

## Spalten durchlaufen und entsperren

Als nächstes müssen wir alle Spalten im Arbeitsblatt durchlaufen und sie entsperren. Dadurch wird sichergestellt, dass alle Spalten bearbeitet werden können, mit Ausnahme der Spalte, die wir schützen möchten. Hier ist der Codeausschnitt:

```csharp
// Gehen Sie alle Spalten im Arbeitsblatt durch und entsperren Sie sie.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Sperren einer bestimmten Spalte

Lassen Sie uns nun eine bestimmte Spalte sperren. In diesem Beispiel sperren wir die erste Spalte (Spaltenindex 0). Hier ist der Codeausschnitt:

```csharp
// Holen Sie sich den Stil der ersten Spalte.
style = sheet.Cells.Columns[0].Style;

// Verschließe es.
style.IsLocked = true;
```

## Anwenden von Stilen auf Spalten

Nachdem wir die spezifische Spalte gesperrt haben, müssen wir den Stil und das Flag auf diese Spalte anwenden. Hier ist der Codeausschnitt:

```csharp
//Instanziieren Sie die Flagge.
flag = new StyleFlag();

// Legen Sie die Sperreinstellung fest.
flag.Locked = true;

// Wenden Sie den Stil auf die erste Spalte an.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

## Schutz des Arbeitsblatts

Um den Schutz abzuschließen, müssen wir das Arbeitsblatt schützen, um sicherzustellen, dass die gesperrten Spalten nicht geändert werden können. Hier ist der Codeausschnitt:

```csharp
// Schützen Sie das Blatt.
sheet.Protect(ProtectionType.All);
```

## Speichern der Excel-Datei

Abschließend speichern wir die geänderte Excel-Datei am gewünschten Ort. Hier ist der Codeausschnitt:

```csharp
// Speichern Sie die Excel-Datei.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Stellen Sie sicher, dass Sie „output.out.xls“ durch den gewünschten Dateinamen und die gewünschte Erweiterung ersetzen.

### Beispielquellcode für „Spezifische Spalte im Excel-Arbeitsblatt schützen“ mit Aspose.Cells für .NET 
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
// Holen Sie sich den Stil der ersten Spalte.
style = sheet.Cells.Columns[0].Style;
// Verschließe es.
style.IsLocked = true;
//Instanziieren Sie die Flagge.
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

In diesem Tutorial haben wir den Schritt-für-Schritt-Prozess zum Schutz einer bestimmten Spalte in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells für .NET-Bibliothek erklärt. Wir begannen damit, eine neue Arbeitsmappe und ein neues Arbeitsblatt zu erstellen, den Stil und die Stilflagobjekte zu definieren und gingen dann dazu über, bestimmte Spalten zu entsperren und zu sperren. Schließlich haben wir das Arbeitsblatt geschützt und die geänderte Excel-Datei gespeichert. Wenn Sie dieser Anleitung folgen, sollten Sie nun in der Lage sein, bestimmte Spalten in Excel-Arbeitsblättern mit C# und Aspose.Cells für .NET zu schützen.

### Häufig gestellte Fragen (FAQs)

#### Kann ich mit dieser Methode mehrere Spalten schützen?

Ja, Sie können mehrere Spalten schützen, indem Sie den Code entsprechend ändern. Gehen Sie einfach den gewünschten Spaltenbereich durch und wenden Sie die Sperrstile und Flags an.

#### Ist es möglich, das geschützte Arbeitsblatt mit einem Passwort zu schützen?

 Ja, Sie können dem geschützten Arbeitsblatt einen Passwortschutz hinzufügen, indem Sie beim Aufrufen das Passwort angeben`Protect` Methode.

#### Unterstützt Aspose.Cells für .NET andere Excel-Dateiformate?

Ja, Aspose.Cells für .NET unterstützt verschiedene Excel-Dateiformate, darunter XLS, XLSX, XLSM und mehr.

#### Kann ich bestimmte Zeilen anstelle von Spalten schützen?

Ja, Sie können den Code ändern, um bestimmte Zeilen statt Spalten zu schützen, indem Sie die Stile und Flags auf Zeilenzellen statt auf Spaltenzellen anwenden.