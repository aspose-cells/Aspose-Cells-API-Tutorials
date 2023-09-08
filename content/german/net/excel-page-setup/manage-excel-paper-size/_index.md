---
title: Verwalten Sie die Excel-Papiergröße
linktitle: Verwalten Sie die Excel-Papiergröße
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie die Papiergröße in Excel mit Aspose.Cells für .NET verwalten. Schritt-für-Schritt-Anleitung mit Quellcode in C#.
type: docs
weight: 70
url: /de/net/excel-page-setup/manage-excel-paper-size/
---
In diesem Tutorial führen wir Sie Schritt für Schritt durch die Verwaltung der Papiergröße in Excel-Dokumenten mit Aspose.Cells für .NET. Wir zeigen Ihnen, wie Sie das Papierformat mithilfe des C#-Quellcodes konfigurieren.

## Schritt 1: Einrichten der Umgebung

Stellen Sie sicher, dass Aspose.Cells für .NET auf Ihrem Computer installiert ist. Erstellen Sie außerdem ein neues Projekt in Ihrer bevorzugten Entwicklungsumgebung.

## Schritt 2: Erforderliche Bibliotheken importieren

Importieren Sie in Ihre Codedatei die Bibliotheken, die für die Arbeit mit Aspose.Cells erforderlich sind. Hier ist der entsprechende Code:

```csharp
using Aspose.Cells;
```

## Schritt 3: Dokumentverzeichnis festlegen

Legen Sie das Verzeichnis fest, in dem sich das Excel-Dokument befindet, mit dem Sie arbeiten möchten. Verwenden Sie den folgenden Code, um das Verzeichnis festzulegen:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Geben Sie unbedingt den vollständigen Verzeichnispfad an.

## Schritt 4: Erstellen eines Arbeitsmappenobjekts

Das Workbook-Objekt stellt das Excel-Dokument dar, mit dem Sie arbeiten werden. Sie können es mit dem folgenden Code erstellen:

```csharp
Workbook workbook = new Workbook();
```

Dadurch wird ein neues leeres Workbook-Objekt erstellt.

## Schritt 5: Zugriff auf das erste Arbeitsblatt

Um auf die erste Tabelle des Excel-Dokuments zuzugreifen, verwenden Sie den folgenden Code:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

Dadurch können Sie mit dem ersten Arbeitsblatt in der Arbeitsmappe arbeiten.

## Schritt 6: Papierformat einrichten

Verwenden Sie die PageSetup.PaperSize-Eigenschaft des Worksheet-Objekts, um das Papierformat festzulegen. In diesem Beispiel stellen wir das Papierformat auf A4 ein. Hier ist der entsprechende Code:

```csharp
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
```

Dadurch wird das Tabellenpapierformat auf A4 eingestellt.

## Schritt 7: Speichern der Arbeitsmappe

Um Änderungen an der Arbeitsmappe zu speichern, verwenden Sie die Save()-Methode des Workbook-Objekts. Hier ist der entsprechende Code:

```csharp
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```

Dadurch wird die Arbeitsmappe mit den Änderungen im angegebenen Verzeichnis gespeichert.

### Beispielquellcode für „Excel-Papiergröße verwalten“ mit Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanziieren eines Workbook-Objekts
Workbook workbook = new Workbook();
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei
Worksheet worksheet = workbook.Worksheets[0];
// Stellen Sie das Papierformat auf A4 ein
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
// Speichern Sie die Arbeitsmappe.
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```
## Abschluss

Sie haben jetzt gelernt, wie Sie die Papiergröße in einem Excel-Dokument mit Aspose.Cells für .NET verwalten. Dieses Tutorial führte Sie durch jeden Schritt des Prozesses, von der Einrichtung der Umgebung bis zum Speichern von Änderungen. Mit diesem Wissen können Sie nun das Papierformat Ihrer Excel-Dokumente anpassen.

### FAQs

#### F1: Kann ich ein anderes benutzerdefiniertes Papierformat als A4 festlegen?

A1: Ja, Aspose.Cells unterstützt eine Vielzahl vordefinierter Papierformate sowie die Möglichkeit, durch Angabe der gewünschten Abmessungen ein benutzerdefiniertes Papierformat festzulegen.

#### F2: Wie kann ich das aktuelle Papierformat in einem Excel-Dokument ermitteln?

 A2: Sie können das verwenden`PageSetup.PaperSize` Eigentum der`Worksheet` Objekt, um das aktuell eingestellte Papierformat zu erhalten.

#### F3: Ist es möglich, zusätzliche Seitenränder für das Papierformat festzulegen?

 A3: Ja, Sie können es verwenden`PageSetup.LeftMargin`, `PageSetup.RightMargin`, `PageSetup.TopMargin` Und`PageSetup.BottomMargin` Eigenschaften, um neben der Papiergröße weitere Seitenränder festzulegen.

#### F4: Funktioniert diese Methode für alle Excel-Dateiformate wie .xls und .xlsx?

A4: Ja, diese Methode funktioniert sowohl für die Dateiformate .xls als auch .xlsx.

#### F5: Kann ich auf verschiedene Arbeitsblätter in derselben Arbeitsmappe unterschiedliche Papierformate anwenden?

 A5: Ja, Sie können unterschiedliche Papierformate auf verschiedene Arbeitsblätter in derselben Arbeitsmappe anwenden, indem Sie verwenden`PageSetup.PaperSize` Eigenschaft jedes Arbeitsblatts.