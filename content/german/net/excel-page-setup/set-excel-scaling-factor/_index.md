---
title: Legen Sie den Excel-Skalierungsfaktor fest
linktitle: Legen Sie den Excel-Skalierungsfaktor fest
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie Excel-Dateien einfach bearbeiten und den Skalierungsfaktor mit Aspose.Cells für .NET anpassen.
type: docs
weight: 180
url: /de/net/excel-page-setup/set-excel-scaling-factor/
---
In dieser Anleitung zeigen wir Ihnen, wie Sie mit Aspose.Cells für .NET den Skalierungsfaktor in einer Excel-Tabelle festlegen. Führen Sie die folgenden Schritte aus, um diese Aufgabe auszuführen.

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

 Unbedingt ersetzen`"YOUR_DOCUMENT_DIRECTORY"` mit dem richtigen Pfad auf Ihrem System.

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

## Schritt 6: Skalierungsfaktor festlegen

Legen Sie den Skalierungsfaktor mit dem folgenden Code fest:

```csharp
worksheet.PageSetup.Zoom = 100;
```

Hier haben wir den Skalierungsfaktor auf 100 eingestellt, was bedeutet, dass die Tabelle beim Drucken in 100 % der Normalgröße angezeigt wird.

## Schritt 7: Speichern der Excel-Arbeitsmappe

 Um die Excel-Arbeitsmappe mit dem definierten Skalierungsfaktor zu speichern, verwenden Sie die`Save` Methode des Workbook-Objekts:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

Dadurch wird die Excel-Arbeitsmappe mit dem Dateinamen „ScalingFactor_out.xls“ im angegebenen Verzeichnis gespeichert.

### Beispielquellcode für „Set Excel Scaling Factor“ mit Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanziieren eines Workbook-Objekts
Workbook workbook = new Workbook();
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei
Worksheet worksheet = workbook.Worksheets[0];
// Skalierungsfaktor auf 100 setzen
worksheet.PageSetup.Zoom = 100;
// Speichern Sie die Arbeitsmappe.
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie mit Aspose.Cells für .NET den Skalierungsfaktor in einer Excel-Tabelle festlegen. Mit dem Skalierungsfaktor können Sie die Größe der Tabelle beim Drucken für eine optimale Darstellung anpassen.

### FAQs

#### 1. Wie stelle ich den Skalierungsfaktor in einer Excel-Tabelle mit Aspose.Cells für .NET ein?

 Benutzen Sie die`Zoom` Eigentum der`PageSetup`Objekt zum Festlegen des Skalierungsfaktors. Zum Beispiel,`worksheet.PageSetup.Zoom = 100;` setzt den Skalierungsfaktor auf 100 %.

#### 2. Kann ich den Skalierungsfaktor an meine Bedürfnisse anpassen?

 Ja, Sie können den Skalierungsfaktor anpassen, indem Sie den dem zugewiesenen Wert ändern`Zoom` Eigentum. Zum Beispiel,`worksheet.PageSetup.Zoom = 75;` setzt den Skalierungsfaktor auf 75 %.

#### 3. Ist es möglich, die Excel-Arbeitsmappe mit dem definierten Skalierungsfaktor zu speichern?

 Ja, Sie können das verwenden`Save` Methode der`Workbook` -Objekt, um die Excel-Arbeitsmappe mit dem definierten Skalierungsfaktor zu speichern.