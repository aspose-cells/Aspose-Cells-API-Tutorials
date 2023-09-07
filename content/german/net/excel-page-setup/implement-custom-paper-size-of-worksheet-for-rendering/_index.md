---
title: Implementieren Sie eine benutzerdefinierte Papiergröße des Arbeitsblatts zum Rendern
linktitle: Implementieren Sie eine benutzerdefinierte Papiergröße des Arbeitsblatts zum Rendern
second_title: Aspose.Cells für .NET API-Referenz
description: Schritt-für-Schritt-Anleitung zum Implementieren einer benutzerdefinierten Arbeitsblattgröße mit Aspose.Cells für .NET. Legen Sie die Abmessungen fest, fügen Sie eine Nachricht hinzu und speichern Sie sie als PDF.
type: docs
weight: 50
url: /de/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
Das Implementieren einer benutzerdefinierten Größe für Ihr Arbeitsblatt kann sehr nützlich sein, wenn Sie ein PDF-Dokument mit einer bestimmten Größe erstellen möchten. In diesem Tutorial erfahren Sie, wie Sie mit Aspose.Cells für .NET eine benutzerdefinierte Größe für ein Arbeitsblatt festlegen und das Dokument dann als PDF speichern.

## Schritt 1: Erstellen des Ausgabeordners

Bevor Sie beginnen, müssen Sie einen Ausgabeordner erstellen, in dem die generierte PDF-Datei gespeichert wird. Sie können einen beliebigen Pfad für Ihren Ausgabeordner verwenden.

```csharp
// Ausgabeverzeichnisse
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Stellen Sie sicher, dass Sie den richtigen Pfad zu Ihrem Ausgabeordner angeben.

## Schritt 2: Erstellen des Workbook-Objekts

Um zu beginnen, müssen Sie mit Aspose.Cells ein Workbook-Objekt erstellen. Dieses Objekt repräsentiert Ihre Tabelle.

```csharp
// Erstellen Sie das Workbook-Objekt
Workbook wb = new Workbook();
```

## Schritt 3: Zugriff auf das erste Arbeitsblatt

Nachdem Sie das Workbook-Objekt erstellt haben, können Sie auf das erste darin enthaltene Arbeitsblatt zugreifen.

```csharp
// Zugriff auf das erste Arbeitsblatt
Worksheet ws = wb.Worksheets[0];
```

## Schritt 4: Benutzerdefinierte Arbeitsblattgröße festlegen

 Jetzt können Sie mit die benutzerdefinierte Arbeitsblattgröße festlegen`CustomPaperSize(width, height)` Methode der PageSetup-Klasse.

```csharp
// Benutzerdefinierte Arbeitsblattgröße festlegen (in Zoll)
ws.PageSetup.CustomPaperSize(6, 4);
```

In diesem Beispiel haben wir die Arbeitsblattgröße auf 6 Zoll Breite und 4 Zoll Höhe festgelegt.

## Schritt 5: Zugriff auf Zelle B4

Danach können wir auf eine bestimmte Zelle im Arbeitsblatt zugreifen. In diesem Fall greifen wir auf Zelle B4 zu.

```csharp
// Zugang zur Zelle B4
Cell b4 = ws.Cells["B4"];
```

## Schritt 6: Hinzufügen der Nachricht in Zelle B4

 Wir können jetzt mit dem eine Nachricht zu Zelle B4 hinzufügen`PutValue(value)` Methode.

```csharp
// Fügen Sie die Nachricht in Zelle B4 hinzu
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

In diesem Beispiel haben wir in Zelle B4 die Meldung „PDF-Seitengröße: 6,00“ x 4,00“ eingefügt.

## Schritt 7: Speichern des Arbeitsblatts im PDF-Format

 Schließlich können wir das Arbeitsblatt mit dem im PDF-Format speichern`Save(filePath)` Methode des Workbook-Objekts.

```csharp
// Speichern Sie das Arbeitsblatt im PDF-Format
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Geben Sie den gewünschten Pfad zur generierten PDF-Datei an, indem Sie den zuvor erstellten Ausgabeordner verwenden.

### Beispielquellcode für die Implementierung einer benutzerdefinierten Papiergröße des Arbeitsblatts zum Rendern mit Aspose.Cells für .NET 
```csharp
//Ausgabe Verzeichnis
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Arbeitsmappenobjekt erstellen
Workbook wb = new Workbook();
//Greifen Sie auf das erste Arbeitsblatt zu
Worksheet ws = wb.Worksheets[0];
//Legen Sie das benutzerdefinierte Papierformat in der Einheit Zoll fest
ws.PageSetup.CustomPaperSize(6, 4);
//Greifen Sie auf Zelle B4 zu
Cell b4 = ws.Cells["B4"];
//Fügen Sie die Nachricht in Zelle B4 hinzu
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Speichern Sie die Arbeitsmappe im PDF-Format
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## Schlussfolgerungen

In diesem Tutorial haben Sie gelernt, wie Sie mit Aspose.Cells für .NET eine benutzerdefinierte Größe eines Arbeitsblatts implementieren. Mit diesen Schritten können Sie bestimmte Abmessungen für Ihre Arbeitsblätter festlegen und die Dokumente anschließend im PDF-Format speichern. Wir hoffen, dass dieser Leitfaden hilfreich war, um den Prozess der Implementierung einer benutzerdefinierten Tabellengröße zu verstehen.

### Häufig gestellte Fragen (FAQ)

#### Frage 1: Kann ich das Tabellenlayout weiter anpassen?

Ja, Aspose.Cells bietet viele Optionen zum Anpassen Ihres Arbeitsblattlayouts. Sie können benutzerdefinierte Abmessungen, Seitenausrichtung, Ränder, Kopf- und Fußzeilen und vieles mehr festlegen.

#### Frage 2: Welche anderen Ausgabeformate unterstützt Aspose.Cells?

Aspose.Cells unterstützt viele verschiedene Ausgabeformate, darunter PDF, XLSX, XLS, CSV, HTML, TXT und viele mehr. Sie können das gewünschte Ausgabeformat entsprechend Ihren Anforderungen auswählen.