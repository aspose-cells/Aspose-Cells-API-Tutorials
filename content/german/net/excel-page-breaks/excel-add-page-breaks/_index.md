---
title: Excel Seitenumbrüche hinzufügen
linktitle: Excel Seitenumbrüche hinzufügen
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET Seitenumbrüche in Excel hinzufügen. Schritt-für-Schritt-Anleitung zur Erstellung gut strukturierter Berichte.
type: docs
weight: 10
url: /de/net/excel-page-breaks/excel-add-page-breaks/
---
Das Hinzufügen von Seitenumbrüchen in einer Excel-Datei ist eine wesentliche Funktion beim Erstellen großer Berichte oder Dokumente. In diesem Tutorial erfahren Sie, wie Sie mithilfe der Aspose.Cells-Bibliothek für .NET Seitenumbrüche in eine Excel-Datei einfügen. Wir begleiten Sie Schritt für Schritt dabei, den bereitgestellten C#-Quellcode zu verstehen und umzusetzen.

## Schritt 1: Vorbereiten der Umgebung

 Bevor Sie beginnen, stellen Sie sicher, dass Aspose.Cells für .NET auf Ihrem Computer installiert ist. Sie können die Bibliothek unter herunterladen[Aspose-Veröffentlichungen](https://releases.aspose.com/cells/net)und installieren Sie es, indem Sie den bereitgestellten Anweisungen folgen.

Erstellen Sie nach Abschluss der Installation ein neues C#-Projekt in Ihrer bevorzugten integrierten Entwicklungsumgebung (IDE) und importieren Sie die Aspose.Cells-Bibliothek für .NET.

## Schritt 2: Konfigurieren des Dokumentverzeichnispfads

 Im bereitgestellten Quellcode müssen Sie den Verzeichnispfad angeben, in dem Sie die generierte Excel-Datei speichern möchten. Modifiziere den`dataDir` Variable, indem Sie „IHR DOKUMENTVERZEICHNIS“ durch den absoluten Pfad des Verzeichnisses auf Ihrem Computer ersetzen.

```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## Schritt 3: Erstellen eines Arbeitsmappenobjekts

Zunächst müssen wir ein Workbook-Objekt erstellen, das unsere Excel-Datei darstellt. Dies kann mithilfe der von Aspose.Cells bereitgestellten Workbook-Klasse erreicht werden.

```csharp
// Instanziieren eines Workbook-Objekts
Workbook workbook = new Workbook();
```

## Schritt 4: Hinzufügen eines horizontalen Seitenumbruchs

Fügen wir nun unserem Excel-Arbeitsblatt einen horizontalen Seitenumbruch hinzu. Im Beispielcode fügen wir der Zelle „Y30“ des ersten Arbeitsblatts einen horizontalen Seitenumbruch hinzu.

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
```

## Schritt 5: Einen vertikalen Seitenumbruch hinzufügen

Ebenso können wir mit dem einen vertikalen Seitenumbruch hinzufügen`VerticalPageBreaks.Add()` Methode. In unserem Beispiel fügen wir der Zelle „Y30“ des ersten Arbeitsblatts einen vertikalen Seitenumbruch hinzu.

```csharp
workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");
```

## Schritt 6: Speichern der Excel-Datei

 Nachdem wir nun die Seitenumbrüche hinzugefügt haben, müssen wir die endgültige Excel-Datei speichern. Benutzen Sie die`Save()` -Methode, um den vollständigen Pfad der Ausgabedatei anzugeben.

```csharp
// Speichern Sie die Excel-Datei.
workbook.Save(dataDir + "AddingPageBreaks_out.xls");
```
### Beispielquellcode für Excel: Hinzufügen von Seitenumbrüchen mit Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanziieren eines Workbook-Objekts
Workbook workbook = new Workbook();
// Fügen Sie bei Zelle Y30 einen Seitenumbruch hinzu
workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");
// Speichern Sie die Excel-Datei.
workbook.Save(dataDir + "AddingPageBreaks_out.xls");
```

## Abschluss

In diesem Tutorial haben wir gelernt, wie man Pausen hinzufügt

  Seite in einer Excel-Datei mit Aspose.Cells für .NET. Wenn Sie die bereitgestellten Schritte befolgen, können Sie ganz einfach horizontale und vertikale Seitenumbrüche in Ihre dynamisch generierten Excel-Dateien einfügen. Experimentieren Sie gerne weiter mit der Aspose.Cells-Bibliothek, um weitere leistungsstarke Funktionen zu entdecken.

### FAQs

#### F: Ist Aspose.Cells für .NET eine kostenlose Bibliothek?

A: Aspose.Cells für .NET ist eine kommerzielle Bibliothek, bietet jedoch eine kostenlose Testversion, mit der Sie die Funktionalität testen können.

#### F: Kann ich in einer Excel-Datei mehrere Seitenumbrüche hinzufügen?

A: Ja, Sie können in verschiedenen Teilen Ihrer Tabelle so viele Seitenumbrüche wie nötig hinzufügen.

#### F: Ist es möglich, einen zuvor hinzugefügten Seitenumbruch zu entfernen?

A: Ja, mit Aspose.Cells können Sie vorhandene Seitenumbrüche mithilfe der entsprechenden Methoden des Worksheet-Objekts entfernen.

#### F: Funktioniert diese Methode auch mit anderen Excel-Dateiformaten wie XLSX oder XLSM?

A: Ja, die in diesem Tutorial beschriebene Methode funktioniert mit verschiedenen Excel-Dateiformaten, die von Aspose.Cells unterstützt werden.

#### F: Kann ich das Erscheinungsbild von Seitenumbrüchen in Excel anpassen?

A: Ja, Aspose.Cells bietet eine Reihe von Funktionen zum Anpassen von Seitenumbrüchen, wie z. B. Stil, Farbe und Abmessungen.
