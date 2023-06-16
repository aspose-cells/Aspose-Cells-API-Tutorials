---
title: Legen Sie Excel-Ränder fest
linktitle: Legen Sie Excel-Ränder fest
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET Ränder in Excel festlegen. Schritt-für-Schritt-Anleitung in C#.
type: docs
weight: 110
url: /de/net/excel-page-setup/set-excel-margins/
---
In diesem Tutorial führen wir Sie Schritt für Schritt durch das Festlegen von Rändern in Excel mithilfe von Aspose.Cells für .NET. Wir werden C#-Quellcode verwenden, um den Prozess zu veranschaulichen.

## Schritt 1: Einrichten der Umgebung

Stellen Sie sicher, dass Aspose.Cells für .NET auf Ihrem Computer installiert ist. Erstellen Sie außerdem ein neues Projekt in Ihrer bevorzugten Entwicklungsumgebung.

## Schritt 2: Erforderliche Bibliotheken importieren

Importieren Sie in Ihre Codedatei die Bibliotheken, die für die Arbeit mit Aspose.Cells erforderlich sind. Hier ist der entsprechende Code:

```csharp
using Aspose.Cells;
```

## Schritt 3: Datenverzeichnis festlegen

Legen Sie das Datenverzeichnis fest, in dem Sie die geänderte Excel-Datei speichern möchten. Verwenden Sie den folgenden Code:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Geben Sie unbedingt den vollständigen Verzeichnispfad an.

## Schritt 4: Arbeitsmappe und Arbeitsblatt erstellen

Erstellen Sie ein neues Arbeitsmappenobjekt und navigieren Sie mit dem folgenden Code zum ersten Arbeitsblatt in der Arbeitsmappe:

```csharp
Workbook workbook = new Workbook();
WorksheetCollection worksheets = workbook. Worksheets;
Worksheet worksheet = worksheets[0];
```

Dadurch wird eine leere Arbeitsmappe mit einem Arbeitsblatt erstellt und der Zugriff auf dieses Arbeitsblatt ermöglicht.

## Schritt 5: Ränder festlegen

Greifen Sie auf das PageSetup-Objekt des Arbeitsblatts zu und legen Sie die Ränder mithilfe der Eigenschaften BottomMargin, LeftMargin, RightMargin und TopMargin fest. Hier ist ein Beispielcode:

```csharp
PageSetup pageSetup = worksheet.PageSetup;
pageSetup.BottomMargin = 2;
pageSetup.LeftMargin = 1;
pageSetup.RightMargin = 1;
pageSetup.TopMargin = 3;
```

Dadurch werden der untere, linke, rechte und obere Rand des Arbeitsblatts festgelegt.

## Schritt 6: Speichern der geänderten Arbeitsmappe

Speichern Sie die geänderte Arbeitsmappe mit dem folgenden Code:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Dadurch wird die geänderte Arbeitsmappe im angegebenen Datenverzeichnis gespeichert.

### Beispielquellcode zum Festlegen von Excel-Rändern mit Aspose.Cells für .NET 
```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Erstellen Sie ein Arbeitsmappenobjekt
Workbook workbook = new Workbook();
// Holen Sie sich die Arbeitsblätter in die Arbeitsmappe
WorksheetCollection worksheets = workbook.Worksheets;
// Rufen Sie das erste (Standard-)Arbeitsblatt ab
Worksheet worksheet = worksheets[0];
// Rufen Sie das pagesetup-Objekt ab
PageSetup pageSetup = worksheet.PageSetup;
// Legen Sie den unteren, linken, rechten und oberen Seitenrand fest
pageSetup.BottomMargin = 2;
pageSetup.LeftMargin = 1;
pageSetup.RightMargin = 1;
pageSetup.TopMargin = 3;
// Speichern Sie die Arbeitsmappe.
workbook.Save(dataDir + "SetMargins_out.xls");
```

## Abschluss

Sie haben jetzt gelernt, wie Sie mit Aspose.Cells für .NET Ränder in Excel festlegen. Dieses Tutorial führte Sie durch jeden Schritt des Prozesses, von der Einrichtung der Umgebung bis zum Speichern der geänderten Arbeitsmappe. Erkunden Sie die Funktionen von Aspose.Cells weiter, um weitere Manipulationen an Ihren Excel-Dateien vorzunehmen.

### FAQ (häufig gestellte Fragen)

#### 1. Wie kann ich benutzerdefinierte Ränder für meine Tabelle festlegen?

 Mit können Sie benutzerdefinierte Ränder festlegen`BottomMargin`, `LeftMargin`, `RightMargin` , Und`TopMargin` Eigenschaften der`PageSetup` Objekt. Legen Sie einfach die gewünschten Werte für jede Eigenschaft fest, um die Ränder nach Bedarf anzupassen.

#### 2. Kann ich für verschiedene Arbeitsblätter in derselben Arbeitsmappe unterschiedliche Ränder festlegen?

 Ja, Sie können für jedes Arbeitsblatt in derselben Arbeitsmappe unterschiedliche Ränder festlegen. Greifen Sie einfach auf die zu`PageSetup` Objekt jedes Arbeitsblatts einzeln und legen Sie die spezifischen Ränder für jedes Arbeitsblatt fest.

#### 3. Gelten die definierten Ränder auch für den Druck der Arbeitsmappe?

Ja, die mit Aspose.Cells festgelegten Ränder gelten auch beim Drucken der Arbeitsmappe. Die angegebenen Ränder werden beim Generieren der Druckausgabe der Arbeitsmappe berücksichtigt.

#### 4. Kann ich die Ränder einer vorhandenen Excel-Datei mit Aspose.Cells ändern?

 Ja, Sie können die Ränder einer vorhandenen Excel-Datei ändern, indem Sie die Datei mit Aspose.Cells laden und auf die einzelnen Arbeitsblätter zugreifen`PageSetup` Objekt und Ändern der Werte der Margin-Eigenschaften. Speichern Sie dann die geänderte Datei, um die neuen Ränder anzuwenden.

#### 5. Wie entferne ich Ränder aus einer Tabelle?

 Um die Ränder aus einem Arbeitsblatt zu entfernen, können Sie einfach die Werte festlegen`BottomMargin`, `LeftMargin`, `RightMargin` Und`TopMargin` Eigenschaften auf Null. Dadurch werden die Ränder auf ihren Standardwert (normalerweise Null) zurückgesetzt.