---
title: Legen Sie die erste Seitenzahl von Excel fest
linktitle: Legen Sie die erste Seitenzahl von Excel fest
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET die erste Seitenzahl in Excel festlegen.
type: docs
weight: 90
url: /de/net/excel-page-setup/set-excel-first-page-number/
---
In diesem Tutorial zeigen wir Ihnen, wie Sie mit Aspose.Cells für .NET die erste Seitenzahl in Excel festlegen. Wir werden C#-Quellcode verwenden, um den Prozess zu veranschaulichen.

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
Worksheet worksheet = workbook.Worksheets[0];
```

Dadurch wird eine leere Arbeitsmappe mit einem Arbeitsblatt erstellt.

## Schritt 5: Nummer der ersten Seite festlegen

Legen Sie die Nummer der ersten Seite der Arbeitsblattseiten mit dem folgenden Code fest:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Dadurch wird die erste Seitenzahl auf 2 gesetzt.

## Schritt 6: Speichern der geänderten Arbeitsmappe

Speichern Sie die geänderte Arbeitsmappe mit dem folgenden Code:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Dadurch wird die geänderte Arbeitsmappe im angegebenen Datenverzeichnis gespeichert.

### Beispielquellcode für „Erste Seitenzahl in Excel festlegen“ mit Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanziieren eines Workbook-Objekts
Workbook workbook = new Workbook();
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei
Worksheet worksheet = workbook.Worksheets[0];
// Festlegen der ersten Seitenzahl der Arbeitsblattseiten
worksheet.PageSetup.FirstPageNumber = 2;
// Speichern Sie die Arbeitsmappe.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Abschluss

Sie haben jetzt gelernt, wie Sie mit Aspose.Cells für .NET die erste Seitenzahl in Excel festlegen. Dieses Tutorial führte Sie durch jeden Schritt des Prozesses, von der Einrichtung der Umgebung bis zum Festlegen der ersten Seitenzahl. Mit diesem Wissen können Sie nun die Seitennummerierung in Ihren Excel-Dateien anpassen.

### FAQs

#### F1: Kann ich für jedes Arbeitsblatt eine andere erste Seitenzahl festlegen?

 A1: Ja, Sie können für jedes Arbeitsblatt eine andere erste Seitenzahl festlegen, indem Sie auf zugreifen`FirstPageNumber`Eigentum des jeweiligen Arbeitsblattes`PageSetup` Objekt.

#### F2: Wie kann ich die erste Seitenzahl einer vorhandenen Tabelle überprüfen?

 A2: Sie können die erste Seitenzahl eines vorhandenen Arbeitsblatts überprüfen, indem Sie auf zugreifen`FirstPageNumber` Eigentum der`PageSetup` Objekt, das diesem Arbeitsblatt entspricht.

#### F3: Beginnt die Seitennummerierung standardmäßig immer bei 1?

A3: Ja, die Seitennummerierung beginnt in Excel standardmäßig bei 1. Sie können jedoch den in diesem Tutorial gezeigten Code verwenden, um eine andere erste Seitenzahl festzulegen.

#### F4: Sind Änderungen an der ersten Seitenzahl in der bearbeiteten Excel-Datei dauerhaft?

A4: Ja, die an der ersten Seitenzahl vorgenommenen Änderungen werden dauerhaft in der geänderten Excel-Datei gespeichert.

#### F5: Funktioniert diese Methode für alle Excel-Dateiformate wie .xls und .xlsx?

A5: Ja, diese Methode funktioniert für alle von Aspose.Cells unterstützten Excel-Dateiformate, einschließlich .xls und .xlsx.