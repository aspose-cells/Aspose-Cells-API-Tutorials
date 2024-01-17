---
title: Legen Sie den Excel-Drucktitel fest
linktitle: Legen Sie den Excel-Drucktitel fest
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie Excel-Dateien einfach bearbeiten und Druckoptionen mit Aspose.Cells für .NET anpassen.
type: docs
weight: 170
url: /de/net/excel-page-setup/set-excel-print-title/
---
In dieser Anleitung zeigen wir Ihnen, wie Sie mit Aspose.Cells für .NET Drucktitel in einer Excel-Tabelle festlegen. Führen Sie die folgenden Schritte aus, um diese Aufgabe auszuführen.

## Schritt 1: Einrichten der Umgebung

Stellen Sie sicher, dass Sie Ihre Entwicklungsumgebung eingerichtet und Aspose.Cells für .NET installiert haben. Sie können die neueste Version der Bibliothek von der offiziellen Website von Aspose herunterladen.

## Schritt 2: Erforderliche Namespaces importieren

Importieren Sie in Ihrem C#-Projekt die erforderlichen Namespaces, um mit Aspose.Cells zu arbeiten:

```csharp
using Aspose.Cells;
```

## Schritt 3: Legen Sie den Pfad zum Dokumentenverzeichnis fest

 Erkläre a`dataDir` Variable, um den Pfad zu dem Verzeichnis anzugeben, in dem Sie die generierte Excel-Datei speichern möchten:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Unbedingt austauschen`"YOUR_DOCUMENT_DIRECTORY"` mit dem richtigen Pfad auf Ihrem System.

## Schritt 4: Erstellen eines Arbeitsmappenobjekts

Instanziieren Sie ein Workbook-Objekt, das die Excel-Arbeitsmappe darstellt, die Sie erstellen möchten:

```csharp
Workbook workbook = new Workbook();
```

## Schritt 5: Zugriff auf das erste Arbeitsblatt

Navigieren Sie mit dem folgenden Code zum ersten Arbeitsblatt in der Excel-Arbeitsmappe:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Schritt 6: Titelspalten definieren

Definieren Sie die Titelspalten mit dem folgenden Code:

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

Hier haben wir die Spalten A und B als Titelspalten definiert. Sie können diesen Wert Ihren Bedürfnissen entsprechend anpassen.

## Schritt 7: Titelzeilen definieren

Definieren Sie die Titelzeilen mit dem folgenden Code:

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

Wir haben die Zeilen 1 und 2 als Titelzeilen definiert. Sie können diese Werte entsprechend Ihren Bedürfnissen anpassen.

## Schritt 8: Speichern der Excel-Arbeitsmappe

 Um die Excel-Arbeitsmappe mit den definierten Drucktiteln zu speichern, verwenden Sie die`Save` Methode des Workbook-Objekts:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

Dadurch wird die Excel-Arbeitsmappe mit dem Dateinamen „SetPrintTitle_out.xls“ im angegebenen Verzeichnis gespeichert.

### Beispielquellcode für „Excel-Drucktitel festlegen“ mit Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanziieren eines Workbook-Objekts
Workbook workbook = new Workbook();
// Abrufen der Referenz des PageSetup des Arbeitsblatts
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Definieren der Spaltennummern A und B als Titelspalten
pageSetup.PrintTitleColumns = "$A:$B";
// Definieren der Zeilennummern 1 und 2 als Titelzeilen
pageSetup.PrintTitleRows = "$1:$2";
// Speichern Sie die Arbeitsmappe.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie mit Aspose.Cells für .NET Drucktitel in einer Excel-Tabelle festlegen. Mit Drucktiteln können Sie bestimmte Zeilen und Spalten auf jeder gedruckten Seite anzeigen und so die Daten leichter lesbar und referenzierbar machen.

### FAQs

#### 1. Kann ich Drucktitel für bestimmte Spalten in Excel festlegen?

 Ja, mit Aspose.Cells für .NET können Sie mithilfe von bestimmte Spalten als Drucktitel festlegen`PrintTitleColumns` Eigentum der`PageSetup` Objekt.

#### 2. Ist es möglich, sowohl Spalten- als auch Druckzeilentitel zu definieren?

 Ja, Sie können mit dem sowohl Spalten- als auch Zeilentitel zum Drucken festlegen`PrintTitleColumns` Und`PrintTitleRows` Eigenschaften der`PageSetup` Objekt.

#### 3. Welche anderen Layouteinstellungen kann ich mit Aspose.Cells für .NET anpassen?

Mit Aspose.Cells für .NET können Sie verschiedene Seitenlayouteinstellungen anpassen, z. B. Ränder, Seitenausrichtung, Druckmaßstab und mehr.