---
title: Excel-Kopierarbeitsblatt
linktitle: Excel-Kopierarbeitsblatt
second_title: Aspose.Cells für .NET API-Referenz
description: Kopieren Sie mit Aspose.Cells für .NET ein Excel-Arbeitsblatt in ein anderes.
type: docs
weight: 20
url: /de/net/excel-copy-worksheet/excel-copy-worksheet/
---

In dieser Anleitung erklären wir, wie Sie ein Excel-Arbeitsblatt mithilfe der Aspose.Cells-Bibliothek für .NET kopieren. Wir stellen Ihnen C#-Quellcode zur Verfügung und führen Sie durch die Schritte, die zum Ausführen dieser Aufgabe erforderlich sind. Am Ende zeigen wir Ihnen das erwartete Ergebnis. Befolgen Sie die nachstehenden Anweisungen, um zu beginnen.

## Schritt 1: Vorbereitung

Bevor Sie beginnen, stellen Sie sicher, dass Sie Aspose.Cells für .NET installiert und ein C#-Projekt in Ihrer bevorzugten integrierten Entwicklungsumgebung (IDE) erstellt haben. Stellen Sie außerdem sicher, dass Sie über eine Kopie der Excel-Datei verfügen, die Sie bearbeiten möchten.

## Schritt 2: Erforderliche Bibliotheken importieren

 Importieren Sie in Ihrer C#-Quelldatei die erforderlichen Bibliotheken aus Aspose.Cells mithilfe von`using` Direktive:

```csharp
using Aspose.Cells;
```

## Schritt 3: Legen Sie den Dateipfad fest

 Erkläre a`dataDir` Variable und initialisieren Sie sie mit dem Verzeichnis, das Ihre Excel-Datei enthält. Zum Beispiel :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Unbedingt austauschen`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` mit dem tatsächlichen Pfad zu Ihrem Verzeichnis.

## Schritt 4: Vorhandene Excel-Datei laden

 Benutzen Sie die`Workbook`Klasse aus Aspose.Cells, um die vorhandene Excel-Datei zu öffnen. Benutzen Sie die`InputPath` Variable zur Angabe des Dateipfads:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Stellen Sie sicher, dass Sie ersetzt haben`"book1.xls"` mit dem tatsächlichen Namen Ihrer Excel-Datei.

## Schritt 5: Kopieren Sie das Arbeitsblatt

 Jetzt kopieren wir das vorhandene Arbeitsblatt in ein neues Arbeitsblatt. Benutzen Sie die`Worksheets` Eigentum der`Workbook` Objekt für den Zugriff auf die Sammlung von Arbeitsblättern:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Dann nutzen Sie die`AddCopy` Methode zum Kopieren des angegebenen Arbeitsblatts. Um beispielsweise „Sheet1“ zu kopieren:

```csharp
sheets.AddCopy("Sheet1");
```

## Schritt 6: Speichern Sie die Excel-Datei

 Benutzen Sie die`Save` Methode der`Workbook` Objekt zum Speichern von Änderungen in einer neuen Datei:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Geben Sie unbedingt den gewünschten Pfad und Dateinamen für die Ausgabedatei an.

### Beispielquellcode für Excel Copy Worksheet mit Aspose.Cells für .NET 

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Öffnen Sie eine vorhandene Excel-Datei.
Workbook wb = new Workbook(InputPath);
// Erstellen Sie ein Worksheets-Objekt mit Verweis auf
// die Blätter des Arbeitsbuches.
WorksheetCollection sheets = wb.Worksheets;
// Kopieren Sie Daten von einem vorhandenen in ein neues Blatt
// Blatt innerhalb der Arbeitsmappe.
sheets.AddCopy("Sheet1");
// Speichern Sie die Excel-Datei.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben jetzt gelernt, wie Sie ein Excel-Arbeitsblatt mit Aspose.Cells für .NET kopieren. Diese Schritt-für-Schritt-Anleitung zeigte, wie Sie die erforderlichen Bibliotheken importieren, eine vorhandene Excel-Datei laden, das Arbeitsblatt kopieren und die geänderte Datei speichern. Nutzen Sie diese Methode gerne in Ihren eigenen Projekten, um Excel-Dateien effizient zu bearbeiten.

### FAQs

#### F. Ist Aspose.Cells mit anderen Programmiersprachen kompatibel?

A. Ja, Aspose.Cells unterstützt mehrere Programmiersprachen, darunter C#, Java, Python und viele mehr.

#### F. Kann ich ein Arbeitsblatt in eine andere Excel-Arbeitsmappe kopieren?

A.  Ja, Sie können das verwenden`AddCopy` Methode zum Kopieren eines Arbeitsblatts in eine andere Excel-Arbeitsmappe.

#### F. Behält Aspose.Cells beim Kopieren des Arbeitsblatts Formeln und Formatierungen bei?

A. Ja, Aspose.Cells behält beim Kopieren eines Arbeitsblatts Formeln, Formatierungen und andere Eigenschaften bei.

#### F. Benötigt Aspose.Cells eine Lizenz für die kommerzielle Nutzung?

A. Ja, Aspose.Cells ist ein kommerzielles Produkt und erfordert den Erwerb einer Lizenz für die kommerzielle Nutzung. Weitere Lizenzinformationen finden Sie auf der offiziellen Website von Aspose.