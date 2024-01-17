---
title: Schützen Sie bestimmte Zellen in einem Excel-Arbeitsblatt
linktitle: Schützen Sie bestimmte Zellen in einem Excel-Arbeitsblatt
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie bestimmte Zellen in Excel mit Aspose.Cells für .NET schützen. Schritt-für-Schritt-Anleitung in C#.
type: docs
weight: 70
url: /de/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
In diesem Tutorial schauen wir uns den C#-Quellcode an, der die Aspose.Cells-Bibliothek verwendet, um bestimmte Zellen in einer Excel-Tabelle zu schützen. Wir gehen jeden Schritt des Codes durch und erklären, wie er funktioniert. Befolgen Sie die Anweisungen sorgfältig, um die gewünschten Ergebnisse zu erzielen.

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

In diesem Schritt definieren wir den Stil, der auf bestimmte Zellen angewendet werden soll. Verwenden Sie den folgenden Code:

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

## Schritt 7: Bestimmte Zellen sperren

In diesem Schritt werden wir bestimmte Zellen sperren. Verwenden Sie den folgenden Code:

```csharp
//Sperren aller drei Zellen ... also A1, B1, C1.
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

## Schritt 8: Schützen des Arbeitsblatts

Abschließend schützen wir das Arbeitsblatt, um zu verhindern, dass bestimmte Zellen geändert werden. Verwenden Sie den folgenden Code:

```csharp
// Schützen Sie das Arbeitsblatt.
sheet.Protect(ProtectionType.All);
```

## Schritt 9: Speichern der Excel-Datei

Wir speichern nun die geänderte Excel-Datei. Verwenden Sie den folgenden Code:

```csharp
// Speichern Sie die Excel-Datei.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Stellen Sie sicher, dass Sie den richtigen Pfad zum Speichern der geänderten Excel-Datei angeben.

### Beispielquellcode zum Schützen bestimmter Zellen in einem Excel-Arbeitsblatt mit Aspose.Cells für .NET 
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
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Abschluss

Herzlichen Glückwunsch! Sie verfügen jetzt über C#-Quellcode, der es Ihnen ermöglicht, bestimmte Zellen in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells-Bibliothek für .NET zu schützen. Sie können den Code gerne an Ihre spezifischen Bedürfnisse anpassen.

### FAQs (häufig gestellte Fragen)

#### Funktioniert dieser Code mit neueren Versionen von Excel?

Ja, dieser Code funktioniert mit neueren Versionen von Excel, einschließlich Dateien im Format Excel 2010 und höher.

#### Kann ich neben A1, B1 und C1 auch andere Zellen schützen?

Ja, Sie können den Code ändern, um andere bestimmte Zellen zu sperren, indem Sie die Zellbezüge in den entsprechenden Codezeilen anpassen.

#### Wie kann ich gesperrte Zellen wieder entsperren?

 Sie können verwenden`SetStyle` Methode mit`IsLocked` einstellen`false` um Zellen zu entsperren.

#### Kann ich der Arbeitsmappe weitere Arbeitsblätter hinzufügen?

 Ja, Sie können der Arbeitsmappe weitere Arbeitsblätter hinzufügen`Worksheets.Add()`Methode und wiederholen Sie die Zellschutzschritte für jedes Arbeitsblatt.

#### Wie kann ich das Speicherformat der Excel-Datei ändern?

 Sie können das Speicherformat mit ändern`SaveFormat` Methode mit dem gewünschten Format, zum Beispiel`SaveFormat.Xlsx` für Excel 2007 und höher.