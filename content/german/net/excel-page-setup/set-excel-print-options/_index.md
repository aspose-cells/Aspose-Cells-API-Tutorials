---
title: Legen Sie die Excel-Druckoptionen fest
linktitle: Legen Sie die Excel-Druckoptionen fest
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET ganz einfach Excel-Dateien bearbeiten und Druckoptionen anpassen.
type: docs
weight: 150
url: /de/net/excel-page-setup/set-excel-print-options/
---
In dieser Anleitung zeigen wir Ihnen, wie Sie mit Aspose.Cells für .NET Druckoptionen für eine Excel-Arbeitsmappe festlegen. Wir führen Sie Schritt für Schritt durch den bereitgestellten C#-Quellcode, um diese Aufgabe zu erfüllen.

## Schritt 1: Einrichten der Umgebung

Bevor Sie beginnen, stellen Sie sicher, dass Sie Ihre Entwicklungsumgebung eingerichtet und Aspose.Cells für .NET installiert haben. Sie können die neueste Version der Bibliothek von der offiziellen Website von Aspose herunterladen.

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

 Unbedingt ersetzen`"YOUR_DOCUMENT_DIRECTORY"` mit dem richtigen Pfad auf Ihrem System.

## Schritt 4: Erstellen eines Arbeitsmappenobjekts

Instanziieren Sie ein Workbook-Objekt, das die Excel-Arbeitsmappe darstellt, die Sie erstellen möchten:

```csharp
Workbook workbook = new Workbook();
```

## Schritt 5: Abrufen der PageSetup-Referenz des Arbeitsblatts

Um die Druckoptionen festzulegen, müssen wir zunächst die PageSetup-Referenz aus dem Arbeitsblatt abrufen. Verwenden Sie den folgenden Code, um die Referenz zu erhalten:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Schritt 6: Aktivieren Sie das Drucken von Rasterlinien

Um das Drucken von Gitterlinien zu ermöglichen, verwenden Sie den folgenden Code:

```csharp
pageSetup. PrintGridlines = true;
```

## Schritt 7: Aktivieren Sie das Drucken von Zeilen-/Spaltenköpfen

Um das Drucken von Zeilen- und Spaltenüberschriften zu aktivieren, verwenden Sie den folgenden Code:

```csharp
pageSetup.PrintHeadings = true;
```

## Schritt 8: Schwarzweiß-Druckmodus aktivieren

Um das Drucken des Arbeitsblatts im Schwarzweißmodus zu ermöglichen, verwenden Sie den folgenden Code:

```csharp
pageSetup.BlackAndWhite = true;
```

## Schritt 9: Aktivieren des Feedback-Drucks

Um zu ermöglichen, dass Kommentare so gedruckt werden, wie sie in der Tabelle erscheinen, verwenden Sie den folgenden Code:

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## Schritt 10: Aktivieren Sie das Drucken im Entwurfsmodus

Um das Drucken der Tabelle im Entwurfsmodus zu aktivieren, verwenden Sie den folgenden Code:

```csharp
pageSetup.PrintDraft = true;
```

## Schritt 11: Aktivieren Sie das Drucken von Zellfehlern als N/A

Damit Zellfehler gedruckt werden können als

  als N/A, verwenden Sie den folgenden Code:

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## Schritt 12: Speichern der Excel-Arbeitsmappe

 Um die Excel-Arbeitsmappe mit den eingestellten Druckoptionen zu speichern, verwenden Sie die`Save` Methode des Workbook-Objekts:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

Dadurch wird die Excel-Arbeitsmappe mit dem Dateinamen „OtherPrintOptions_out.xls“ im angegebenen Verzeichnis gespeichert.

### Beispielquellcode für „Excel-Druckoptionen festlegen“ mit Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanziieren eines Workbook-Objekts
Workbook workbook = new Workbook();
// Abrufen der Referenz des PageSetup des Arbeitsblatts
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Ermöglicht das Drucken von Gitterlinien
pageSetup.PrintGridlines = true;
// Ermöglicht das Drucken von Zeilen-/Spaltenüberschriften
pageSetup.PrintHeadings = true;
// Ermöglicht das Drucken von Arbeitsblättern im Schwarzweißmodus
pageSetup.BlackAndWhite = true;
// Ermöglicht das Drucken von Kommentaren, wie sie im Arbeitsblatt angezeigt werden
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// Ermöglicht das Drucken von Arbeitsblättern in Entwurfsqualität
pageSetup.PrintDraft = true;
// Ermöglicht das Drucken von Zellenfehlern als N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// Speichern Sie die Arbeitsmappe.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## Abschluss

Sie haben jetzt erfahren, wie Sie mit Aspose.Cells für .NET Druckoptionen für eine Excel-Arbeitsmappe festlegen. Mit dieser leistungsstarken und benutzerfreundlichen Bibliothek können Sie die Druckeinstellungen Ihrer Excel-Arbeitsmappen auf einfache und effiziente Weise anpassen.

### FAQs


#### 1. Kann ich Druckoptionen wie Ränder oder Seitenausrichtung weiter anpassen?

Ja, Aspose.Cells für .NET bietet eine breite Palette anpassbarer Druckoptionen, wie z. B. Ränder, Seitenausrichtung, Skalierung usw.

#### 2. Unterstützt Aspose.Cells für .NET andere Excel-Dateiformate?

Ja, Aspose.Cells für .NET unterstützt eine Vielzahl von Excel-Dateiformaten wie XLSX, XLS, CSV, HTML, PDF usw.

#### 3. Ist Aspose.Cells für .NET mit allen Versionen von .NET Framework kompatibel?

Aspose.Cells für .NET ist mit .NET Framework 2.0 oder höher kompatibel, einschließlich der Versionen 3.5, 4.0, 4.5, 4.6 usw.