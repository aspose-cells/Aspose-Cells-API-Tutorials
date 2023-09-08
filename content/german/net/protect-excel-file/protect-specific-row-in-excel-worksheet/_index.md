---
title: Schützen Sie eine bestimmte Zeile im Excel-Arbeitsblatt
linktitle: Schützen Sie eine bestimmte Zeile im Excel-Arbeitsblatt
second_title: Aspose.Cells für .NET API-Referenz
description: Schützen Sie eine bestimmte Zeile in Excel mit Aspose.Cells für .NET. Schritt-für-Schritt-Anleitung zum Schutz Ihrer vertraulichen Daten.
type: docs
weight: 90
url: /de/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
Der Schutz vertraulicher Daten in einer Excel-Tabelle ist für die Gewährleistung der Informationssicherheit von entscheidender Bedeutung. Aspose.Cells für .NET bietet eine leistungsstarke Lösung zum Schutz bestimmter Zeilen in einer Excel-Tabelle. In dieser Anleitung erfahren Sie, wie Sie eine bestimmte Zeile in einem Excel-Arbeitsblatt mithilfe des bereitgestellten C#-Quellcodes schützen. Befolgen Sie diese einfachen Schritte, um den Zeilenschutz in Ihren Excel-Dateien einzurichten.

## Schritt 1: Erforderliche Bibliotheken importieren

Stellen Sie zunächst sicher, dass Aspose.Cells für .NET auf Ihrem System installiert ist. Sie müssen außerdem die entsprechenden Referenzen in Ihrem C#-Projekt hinzufügen, um die Funktionalität von Aspose.Cells nutzen zu können. Hier ist der Code zum Importieren der erforderlichen Bibliotheken:

```csharp
// Fügen Sie die erforderlichen Referenzen hinzu
using Aspose.Cells;
```

## Schritt 2: Erstellen einer Excel-Arbeitsmappe und einer Excel-Tabelle

Nach dem Importieren der erforderlichen Bibliotheken können Sie eine neue Excel-Arbeitsmappe und ein neues Arbeitsblatt erstellen. So geht's:

```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// Erstellen Sie ein Verzeichnis, falls es noch nicht vorhanden ist.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// Erstellen Sie eine neue Arbeitsmappe.
Workbook wb = new Workbook();

// Erstellen Sie ein Tabellenkalkulationsobjekt und holen Sie sich das erste Blatt.
Worksheet sheet = wb.Worksheets[0];
```

## Schritt 3: Stil und Stil-Flag festlegen

Jetzt legen wir den Zellenstil und das Stil-Flag fest, um alle Spalten im Arbeitsblatt zu entsperren. Hier ist der notwendige Code:

```csharp
// Legen Sie das Stilobjekt fest.
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
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Schritt 4: Schützen Sie die spezifische Leitung

Jetzt schützen wir die spezifische Zeile im Arbeitsblatt. Wir werden die erste Zeile sperren, um Änderungen zu verhindern. Hier ist wie:

```csharp
// Holen Sie sich den Stil der ersten Zeile.
style = sheet.Cells.Rows[0].Style;

// Verschließe es.
style. IsLocked = true;

//Instanziieren Sie die Flagge.
flag = new StyleFlag();

// Legen Sie den Sperrparameter fest.
flag. Locked = true;

// Wenden Sie den Stil auf die erste Zeile an.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## Schritt 5: Schützen des Arbeitsblatts

Schließlich schützen wir das gesamte Excel-Arbeitsblatt, um unbefugte Änderungen zu verhindern. Hier ist wie:

```csharp
// Schützen Sie das Arbeitsblatt.
sheet.Protect(ProtectionType.All);
```

## Schritt 6: Speichern Sie die geschützte Excel-Datei

Sobald Sie mit dem Schützen der spezifischen Zeile im Excel-Arbeitsblatt fertig sind, können Sie die geschützte Excel-Datei auf Ihrem System speichern. Hier ist wie:

```csharp
// Speichern Sie die Excel-Datei.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Nachdem Sie diese Schritte ausgeführt haben, haben Sie eine bestimmte Zeile in Ihrer Excel-Tabelle erfolgreich mit Aspose.Cells für .NET geschützt.

### Beispielquellcode für „Spezifische Zeile im Excel-Arbeitsblatt schützen“ mit Aspose.Cells für .NET 
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

Der Schutz von Daten in Excel-Dateien ist von entscheidender Bedeutung, um unbefugten Zugriff oder unerwünschte Änderungen zu verhindern. Mit der Aspose.Cells-Bibliothek für .NET können Sie mithilfe des bereitgestellten C#-Quellcodes ganz einfach bestimmte Zeilen in einer Excel-Tabelle schützen. Befolgen Sie diese Schritt-für-Schritt-Anleitung, um Ihren Excel-Dateien eine zusätzliche Sicherheitsebene hinzuzufügen.

### FAQs

#### Funktioniert der spezifische Zeilenschutz in allen Excel-Versionen?

Ja, der spezifische Zeilenschutz mit Aspose.Cells für .NET funktioniert in allen unterstützten Versionen von Excel.

#### Kann ich mehrere bestimmte Zeilen in einer Excel-Tabelle schützen?

Ja, Sie können mehrere bestimmte Zeilen mit ähnlichen, in diesem Handbuch beschriebenen Methoden schützen.

#### Wie kann ich eine bestimmte Zeile in einer Excel-Tabelle entsperren?

 Um eine bestimmte Zeile zu entsperren, müssen Sie den Quellcode mithilfe von entsprechend ändern`IsLocked` Methode der`Style` Objekt.