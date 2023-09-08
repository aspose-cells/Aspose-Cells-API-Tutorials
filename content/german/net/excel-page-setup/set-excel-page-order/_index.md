---
title: Legen Sie die Excel-Seitenreihenfolge fest
linktitle: Legen Sie die Excel-Seitenreihenfolge fest
second_title: Aspose.Cells für .NET API-Referenz
description: Schritt-für-Schritt-Anleitung zum Festlegen der Seitenreihenfolge in Excel mit Aspose.Cells für .NET. Detaillierte Anweisungen und Quellcode enthalten.
type: docs
weight: 120
url: /de/net/excel-page-setup/set-excel-page-order/
---
In diesem Artikel erklären wir Ihnen Schritt für Schritt den folgenden C#-Quellcode zum Festlegen der Excel-Seitenreihenfolge mithilfe von Aspose.Cells für .NET. Wir zeigen Ihnen, wie Sie das Dokumentenverzeichnis einrichten, ein Workbook-Objekt instanziieren, die PageSetup-Referenz abrufen, die Seitendruckreihenfolge festlegen und die Arbeitsmappe speichern.

## Schritt 1: Einrichten des Dokumentenverzeichnisses

 Bevor Sie beginnen, müssen Sie das Dokumentverzeichnis konfigurieren, in dem Sie die Excel-Datei speichern möchten. Sie können den Verzeichnispfad angeben, indem Sie den Wert von ersetzen`dataDir` Variable mit Ihrem eigenen Pfad.

```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## Schritt 2: Instanziieren eines Arbeitsmappenobjekts

Der erste Schritt besteht darin, ein Workbook-Objekt zu instanziieren. Dies stellt die Excel-Arbeitsmappe dar, mit der wir arbeiten werden.

```csharp
// Instanziieren Sie ein Workbook-Objekt
Workbook workbook = new Workbook();
```

## Schritt 3: Abrufen der PageSetup-Referenz

Als nächstes müssen wir die PageSetup-Objektreferenz des Arbeitsblatts abrufen, für das wir die Seitenreihenfolge festlegen möchten.

```csharp
// Rufen Sie die PageSetup-Referenz des Arbeitsblatts ab
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Schritt 4: Festlegen der Druckreihenfolge der Seiten

Jetzt können wir die Druckreihenfolge der Seiten festlegen. In diesem Beispiel verwenden wir die Option „OverThenDown“, was bedeutet, dass die Seiten von links nach rechts und dann von oben nach unten gedruckt werden.

```csharp
// Stellen Sie die Seitendruckreihenfolge auf „OverThenDown“ ein.
pageSetup.Order = PrintOrderType.OverThenDown;
```

## Schritt 5: Speichern der Arbeitsmappe

Abschließend speichern wir die Excel-Arbeitsmappe mit den Änderungen in der Seitenreihenfolge.

```csharp
// Speichern Sie die Arbeitsmappe
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### Beispielquellcode zum Festlegen der Excel-Seitenreihenfolge mit Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanziieren eines Workbook-Objekts
Workbook workbook = new Workbook();
// Abrufen der Referenz des PageSetup des Arbeitsblatts
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Stellen Sie die Druckreihenfolge der Seiten auf „Über“ und dann „Ab“ ein
pageSetup.Order = PrintOrderType.OverThenDown;
// Speichern Sie die Arbeitsmappe.
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## Abschluss

In diesem Tutorial haben wir erklärt, wie man mit Aspose.Cells für .NET die Seitenreihenfolge in einer Excel-Datei festlegt. Wenn Sie die bereitgestellten Schritte ausführen, können Sie das Dokumentverzeichnis einfach konfigurieren, ein Arbeitsmappenobjekt instanziieren, die PageSetup-Referenz abrufen, die Seitendruckreihenfolge festlegen und die Arbeitsmappe speichern.

### FAQs

#### F1: Warum ist es wichtig, die Seitenreihenfolge in einer Excel-Datei festzulegen?

Das Definieren der Reihenfolge der Seiten in einer Excel-Datei ist wichtig, da sie bestimmt, wie die Seiten gedruckt oder angezeigt werden. Durch die Angabe einer bestimmten Reihenfolge können Sie die Daten logisch organisieren und die Datei leichter lesbar oder ausdruckbar machen.

#### F2: Kann ich mit Aspose.Cells für .NET andere Seitendruckaufträge verwenden?

Ja, Aspose.Cells für .NET unterstützt mehrere Seitendruckreihenfolgen wie „DownThenOver“, „OverThenDown“, „DownThenOverThenDownAgain“ usw. Sie können diejenige auswählen, die Ihren Anforderungen am besten entspricht.

#### F3: Kann ich mit Aspose.Cells für .NET zusätzliche Optionen zum Drucken von Seiten festlegen?

Ja, Sie können mithilfe der Eigenschaften des PageSetup-Objekts in Aspose.Cells für .NET verschiedene Seitendruckoptionen wie Skalierung, Ausrichtung, Ränder usw. festlegen.

#### F4: Unterstützt Aspose.Cells für .NET andere Excel-Dateiformate?

Ja, Aspose.Cells für .NET unterstützt eine Vielzahl von Excel-Dateiformaten wie XLSX, XLS, CSV, HTML, PDF usw. Mit den von der Bibliothek bereitgestellten Funktionen können Sie problemlos zwischen diesen Formaten konvertieren.