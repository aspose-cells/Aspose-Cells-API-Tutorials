---
title: Optionen für „An Excel-Seiten anpassen“.
linktitle: Optionen für „An Excel-Seiten anpassen“.
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie Seiten in einer Excel-Tabelle mit Aspose.Cells für .NET automatisch anpassen.
type: docs
weight: 30
url: /de/net/excel-page-setup/fit-to-excel-pages-options/
---
In diesem Artikel erklären wir Ihnen Schritt für Schritt den folgenden C#-Quellcode: „An Excel-Seiten anpassen“-Optionen mit Aspose.Cells für .NET. Wir werden die Aspose.Cells-Bibliothek für .NET verwenden, um diesen Vorgang auszuführen. Führen Sie die folgenden Schritte aus, um die Seitenanpassung in Excel zu konfigurieren.

## Schritt 1: Erstellen einer Arbeitsmappe
Der erste Schritt besteht darin, eine Arbeitsmappe zu erstellen. Wir werden ein Workbook-Objekt instanziieren. Hier ist der Code zum Erstellen einer Arbeitsmappe:

```csharp
// Der Pfad zum Dokumentenverzeichnis
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Instanziieren Sie ein Workbook-Objekt
Workbook workbook = new Workbook();
```

## Schritt 2: Zugriff auf das Arbeitsblatt
Nachdem wir die Arbeitsmappe erstellt haben, müssen wir zum ersten Arbeitsblatt navigieren. Wir werden den Index 0 verwenden, um auf das erste Blatt zuzugreifen. Hier ist der Code für den Zugriff:

```csharp
// Zugriff auf das erste Arbeitsblatt in der Arbeitsmappe
Worksheet worksheet = workbook.Worksheets[0];
```

## Schritt 3: Anpassen an Seiten festlegen
 In diesem Schritt konfigurieren wir die Anpassung an die Seiten des Arbeitsblatts. Wir werden das verwenden`FitToPagesTall` Und`FitToPagesWide` Eigenschaften der`PageSetup` -Objekt, um die gewünschte Anzahl von Seiten für die Höhe und Breite des Arbeitsblatts anzugeben. Hier ist der Code dafür:

```csharp
// Konfigurieren Sie die Anzahl der Seiten für die Höhe des Arbeitsblatts
worksheet.PageSetup.FitToPagesTall = 1;

// Konfigurieren Sie die Anzahl der Seiten für die Breite des Arbeitsblatts
worksheet.PageSetup.FitToPagesWide = 1;
```

## Schritt 4: Speichern der Arbeitsmappe
 Nachdem wir nun „An Seiten anpassen“ konfiguriert haben, können wir die Arbeitsmappe speichern. Wir werden das verwenden`Save` Methode des Workbook-Objekts. Hier ist der Code zum Speichern der Arbeitsmappe:

```csharp
// Speichern Sie die Arbeitsmappe
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Beispielquellcode für „An Excel-Seiten anpassen“-Optionen mit Aspose.Cells für .NET 
```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanziieren eines Workbook-Objekts
Workbook workbook = new Workbook();
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei
Worksheet worksheet = workbook.Worksheets[0];
// Festlegen der Anzahl der Seiten, über die sich die Länge des Arbeitsblatts erstrecken soll
worksheet.PageSetup.FitToPagesTall = 1;
//Legen Sie die Anzahl der Seiten fest, die die Breite des Arbeitsblatts umfassen soll
worksheet.PageSetup.FitToPagesWide = 1;
// Speichern Sie die Arbeitsmappe.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Abschluss
In diesem Artikel haben wir gelernt, wie man mit Aspose.Cells für .NET die Anpassung an Seiten in Excel konfiguriert. Wir haben die folgenden Schritte durchlaufen: Arbeitsmappe erstellen, auf das Arbeitsblatt zugreifen, die Seitenanpassung konfigurieren und die Arbeitsmappe speichern. Jetzt können Sie dieses Wissen nutzen, um Ihre Tabellenkalkulationen an die gewünschten Seiten anzupassen.

### FAQs

#### F: Wie kann ich Aspose.Cells für .NET installieren?

A: Um Aspose.Cells für .NET zu installieren, können Sie den NuGet-Paketmanager in Visual Studio verwenden. Suchen Sie das Paket „Aspose.Cells“ und installieren Sie es in Ihrem Projekt.

#### F: Kann ich Seiten sowohl in der Höhe als auch in der Breite anpassen?

 A: Ja, Sie können sowohl die Höhe als auch die Breite des Arbeitsblatts anpassen`FitToPagesTall` Und`FitToPagesWide` Eigenschaften. Sie können für jede Dimension die gewünschte Anzahl an Seiten angeben.

#### F: Wie kann ich die Optionen „An Seiten anpassen“ anpassen?

A: Zusätzlich zur Angabe der Anzahl der Seiten können Sie auch andere Optionen zur Seitenanpassung anpassen, z. B. den Arbeitsblattmaßstab, die Papierausrichtung, die Ränder und mehr. Nutzen Sie die in der verfügbaren Eigenschaften`PageSetup` Einspruch hierfür einlegen.

#### F: Kann ich Aspose.Cells für .NET verwenden, um vorhandene Arbeitsmappen zu verarbeiten?

A: Ja, Sie können Aspose.Cells für .NET verwenden, um vorhandene Arbeitsmappen zu öffnen und zu bearbeiten. Sie können auf Arbeitsblätter, Zellen, Formeln, Stile und andere Arbeitsmappenelemente zugreifen, um verschiedene Vorgänge auszuführen.