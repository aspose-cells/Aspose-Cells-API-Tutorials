---
title: Legen Sie den Excel-Druckbereich fest
linktitle: Legen Sie den Excel-Druckbereich fest
second_title: Aspose.Cells für .NET API-Referenz
description: Schritt-für-Schritt-Anleitung zum Festlegen des Excel-Druckbereichs mit Aspose.Cells für .NET. Optimieren und passen Sie Ihre Excel-Arbeitsmappen ganz einfach an.
type: docs
weight: 140
url: /de/net/excel-page-setup/set-excel-print-area/
---
Die Verwendung von Aspose.Cells für .NET kann die Verwaltung und Bearbeitung von Excel-Dateien in .NET-Anwendungen erheblich erleichtern. In dieser Anleitung zeigen wir Ihnen, wie Sie den Druckbereich einer Excel-Arbeitsmappe mithilfe von Aspose.Cells für .NET festlegen. Wir führen Sie Schritt für Schritt durch den bereitgestellten C#-Quellcode, um diese Aufgabe zu erfüllen.

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

 Unbedingt austauschen`"YOUR_DOCUMENT_DIRECTORY"` mit dem richtigen Pfad auf Ihrem System.

## Schritt 4: Erstellen eines Arbeitsmappenobjekts

Instanziieren Sie ein Workbook-Objekt, das die Excel-Arbeitsmappe darstellt, die Sie erstellen möchten:

```csharp
Workbook workbook = new Workbook();
```

## Schritt 5: Abrufen der PageSetup-Referenz des Arbeitsblatts

Um den Druckbereich festzulegen, müssen wir zunächst die Referenz aus dem PageSetup des Arbeitsblatts abrufen. Verwenden Sie den folgenden Code, um die Referenz zu erhalten:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Schritt 6: Angeben des Druckbereichs-Zellenbereichs

Nachdem wir nun die PageSetup-Referenz haben, können wir den Zellbereich angeben, aus dem der Druckbereich besteht. In diesem Beispiel legen wir den Zellbereich von A1 bis T35 als Druckbereich fest. Verwenden Sie den folgenden Code:

```csharp
pageSetup.PrintArea = "A1:T35";
```

Sie können den Zellbereich entsprechend Ihren Bedürfnissen anpassen.

## Schritt 7: Speichern der Excel-Arbeitsmappe

 Um die Excel-Arbeitsmappe mit dem definierten Druckbereich zu speichern, verwenden Sie die`Save` Methode des Workbook-Objekts:

```csharp
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

Dadurch wird die Excel-Arbeitsmappe mit dem Dateinamen „SetPrintArea_out.xls“ im angegebenen Verzeichnis gespeichert.

### Beispielquellcode für „Excel-Druckbereich festlegen“ mit Aspose.Cells für .NET 
```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanziieren eines Workbook-Objekts
Workbook workbook = new Workbook();
// Abrufen der Referenz des PageSetup des Arbeitsblatts
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Angabe des Zellbereichs (von A1-Zelle bis T35-Zelle) des Druckbereichs
pageSetup.PrintArea = "A1:T35";
// Speichern Sie die Arbeitsmappe.
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben jetzt gelernt, wie Sie den Druckbereich einer Excel-Arbeitsmappe mithilfe von Aspose.Cells für .NET festlegen. Diese leistungsstarke und benutzerfreundliche Bibliothek erleichtert die Arbeit mit Excel-Dateien in Ihren .NET-Anwendungen erheblich. Wenn Sie weitere Fragen haben oder auf Schwierigkeiten stoßen, können Sie sich gerne die offizielle Aspose.Cells-Dokumentation ansehen, um weitere Informationen und Ressourcen zu erhalten.

### FAQs

#### 1. Kann ich das Layout des Druckbereichs weiter anpassen, z. B. Ausrichtung und Ränder?

Ja, Sie können auf andere PageSetup-Eigenschaften wie Seitenausrichtung, Ränder, Skalierung usw. zugreifen, um das Layout Ihres Druckbereichs weiter anzupassen.

#### 2. Unterstützt Aspose.Cells für .NET andere Excel-Dateiformate wie XLSX und CSV?

Ja, Aspose.Cells für .NET unterstützt eine Vielzahl von Excel-Dateiformaten, darunter XLSX, XLS, CSV, HTML, PDF und viele mehr.

#### 3. Ist Aspose.Cells für .NET mit allen Versionen von .NET Framework kompatibel?

Aspose.Cells für .NET ist mit .NET Framework 2.0 oder höher kompatibel, einschließlich der Versionen 3.5, 4.0, 4.5, 4.6 usw.