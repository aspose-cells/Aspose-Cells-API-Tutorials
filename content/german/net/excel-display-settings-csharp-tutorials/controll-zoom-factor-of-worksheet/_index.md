---
title: Steuern Sie den Zoomfaktor des Arbeitsblatts
linktitle: Steuern Sie den Zoomfaktor des Arbeitsblatts
second_title: Aspose.Cells für .NET API-Referenz
description: Steuern Sie den Zoomfaktor des Excel-Arbeitsblatts mit Aspose.Cells für .NET.
type: docs
weight: 20
url: /de/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
Die Steuerung des Zoomfaktors eines Arbeitsblatts ist eine wesentliche Funktion beim Arbeiten mit Excel-Dateien mithilfe der Aspose.Cells-Bibliothek für .NET. In dieser Anleitung zeigen wir Ihnen Schritt für Schritt, wie Sie mit Aspose.Cells den Zoomfaktor eines Arbeitsblatts mithilfe von C#-Quellcode steuern.

## Schritt 1: Erforderliche Bibliotheken importieren

Bevor Sie beginnen, stellen Sie sicher, dass Sie die Aspose.Cells-Bibliothek für .NET installiert haben und importieren Sie die erforderlichen Bibliotheken in Ihr C#-Projekt.

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## Schritt 2: Verzeichnispfad festlegen und Excel-Datei öffnen

 Legen Sie zunächst den Pfad zu dem Verzeichnis fest, das Ihre Excel-Datei enthält, und öffnen Sie sie dann mit a`FileStream` Objekt und instanziieren a`Workbook` Objekt zur Darstellung der Excel-Arbeitsmappe.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Schritt 3: Greifen Sie auf die Tabelle zu und ändern Sie den Zoomfaktor

In diesem Schritt greifen wir über den Index auf das erste Arbeitsblatt der Excel-Arbeitsmappe zu`0` und stellen Sie den Zoomfaktor des Arbeitsblatts auf ein`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## Schritt 4: Änderungen speichern und die Datei schließen

 Sobald wir den Zoomfaktor des Arbeitsblatts ändern, speichern wir die Änderungen mithilfe von in der Excel-Datei`Save` Methode der`Workbook` Objekt. Anschließend schließen wir den Dateistream, um alle verwendeten Ressourcen freizugeben.

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### Beispielquellcode für „Controll Zoom Factor Of Worksheet“ mit Aspose.Cells für .NET 

```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Erstellen eines Dateistreams, der die zu öffnende Excel-Datei enthält
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanziieren eines Workbook-Objekts
// Öffnen der Excel-Datei über den Dateistream
Workbook workbook = new Workbook(fstream);
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei
Worksheet worksheet = workbook.Worksheets[0];
// Stellen Sie den Zoomfaktor des Arbeitsblatts auf 75 ein
worksheet.Zoom = 75;
// Speichern der geänderten Excel-Datei
workbook.Save(dataDir + "output.xls");
// Schließen des Dateistreams, um alle Ressourcen freizugeben
fstream.Close();
```

## Abschluss

Diese Schritt-für-Schritt-Anleitung zeigte Ihnen, wie Sie den Zoomfaktor eines Arbeitsblatts mit Aspose.Cells für .NET steuern. Mithilfe des bereitgestellten C#-Quellcodes können Sie den Zoomfaktor eines Arbeitsblatts in Ihren .NET-Anwendungen einfach anpassen.

### Häufig gestellte Fragen (FAQ)

#### Was ist Aspose.Cells für .NET?

Aspose.Cells für .NET ist eine funktionsreiche Ablagebibliothek zum Bearbeiten von Excel-Dateien in .NET-Anwendungen.

#### Wie kann ich Aspose.Cells für .NET installieren?

 Um Aspose.Cells für .NET zu installieren, müssen Sie das entsprechende NuGet-Paket von herunterladen[Aspose-Veröffentlichungen](https://releases/aspose.com/cells/net/) und fügen Sie es Ihrem .NET-Projekt hinzu.

#### Welche Funktionen bietet Aspose.Cells für .NET?

Aspose.Cells für .NET bietet Funktionen wie das Erstellen, Bearbeiten, Konvertieren und erweiterte Bearbeiten von Excel-Dateien.

#### Welche Dateiformate werden von Aspose.Cells für .NET unterstützt?

Aspose.Cells für .NET unterstützt mehrere Dateiformate, darunter XLSX, XLSM, CSV, HTML, PDF und viele mehr.
