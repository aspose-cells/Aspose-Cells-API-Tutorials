---
title: Arbeitsblatt ein- und ausblenden
linktitle: Arbeitsblatt ein- und ausblenden
second_title: Aspose.Cells für .NET API-Referenz
description: Eine leistungsstarke Bibliothek für die Arbeit mit Excel-Dateien, einschließlich der Erstellung, Änderung und Bearbeitung von Daten.
type: docs
weight: 90
url: /de/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
In diesem Tutorial erklären wir Ihnen Schritt für Schritt den folgenden C#-Quellcode, der zum Ein- und Ausblenden eines Arbeitsblatts mit Aspose.Cells für .NET verwendet wird. Folgen Sie den unteren Schritten:

## Schritt 1: Vorbereiten der Umgebung

Bevor Sie beginnen, stellen Sie sicher, dass Aspose.Cells für .NET auf Ihrem System installiert ist. Wenn Sie es noch nicht installiert haben, können Sie es von der offiziellen Website von Aspose herunterladen. Nach der Installation können Sie ein neues Projekt in Ihrer bevorzugten integrierten Entwicklungsumgebung (IDE) erstellen.

## Schritt 2: Erforderliche Namespaces importieren

Fügen Sie in Ihrer C#-Quelldatei die erforderlichen Namespaces hinzu, um die Funktionen von Aspose.Cells zu nutzen. Fügen Sie am Anfang Ihrer Datei die folgenden Zeilen hinzu:

```csharp
using Aspose.Cells;
using System.IO;
```

## Schritt 3: Laden Sie die Excel-Datei

Bevor Sie ein Arbeitsblatt ein- oder ausblenden, müssen Sie die Excel-Datei in Ihre Anwendung laden. Stellen Sie sicher, dass sich die Excel-Datei, die Sie verwenden möchten, im selben Verzeichnis wie Ihr Projekt befindet. Verwenden Sie den folgenden Code, um die Excel-Datei zu laden:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

Stellen Sie sicher, dass Sie „PFAD ZU IHREM DOKUMENTENVERZEICHNIS“ durch den tatsächlichen Pfad zu dem Verzeichnis ersetzen, das Ihre Excel-Datei enthält.

## Schritt 4: Greifen Sie auf die Tabelle zu

Sobald die Excel-Datei geladen ist, können Sie zu dem Arbeitsblatt navigieren, das Sie ein- oder ausblenden möchten. Verwenden Sie den folgenden Code, um auf das erste Arbeitsblatt in der Datei zuzugreifen:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Schritt 5: Arbeitsblatt ausblenden

 Nachdem Sie nun auf das Arbeitsblatt zugegriffen haben, können Sie es mithilfe von ausblenden`IsVisible` Eigentum. Verwenden Sie den folgenden Code, um das erste Arbeitsblatt in der Datei auszublenden:

```csharp
worksheet. IsVisible = false;
```

## Schritt 6: Zeigen Sie das Arbeitsblatt erneut an

 Wenn Sie das zuvor ausgeblendete Arbeitsblatt erneut anzeigen möchten, können Sie denselben Code verwenden, indem Sie den Wert von ändern`IsVisible` Eigentum. Verwenden Sie den folgenden Code, um das erste Arbeitsblatt erneut anzuzeigen:

```csharp
worksheet. IsVisible = true;
```

## Schritt 7: Änderungen speichern

Wenn du

  Wenn Sie das Arbeitsblatt nach Bedarf ausgeblendet oder eingeblendet haben, müssen Sie die Änderungen in der Excel-Datei speichern. Verwenden Sie den folgenden Code, um Änderungen zu speichern:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Stellen Sie sicher, dass Sie den richtigen Ausgabepfad angeben, um die geänderte Excel-Datei zu speichern.

### Beispielquellcode für das Ausblenden und Einblenden von Arbeitsblättern mit Aspose.Cells für .NET 

```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Erstellen eines Dateistreams, der die zu öffnende Excel-Datei enthält
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanziieren eines Arbeitsmappenobjekts durch Öffnen der Excel-Datei über den Dateistream
Workbook workbook = new Workbook(fstream);
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei
Worksheet worksheet = workbook.Worksheets[0];
// Das erste Arbeitsblatt der Excel-Datei ausblenden
worksheet.IsVisible = false;
// Zeigt das erste Arbeitsblatt der Excel-Datei
//Worksheet.IsVisible = true;
// Speichern der geänderten Excel-Datei im Standardformat (d. h. Excel 2003).
workbook.Save(dataDir + "output.out.xls");
// Schließen des Dateistreams, um alle Ressourcen freizugeben
fstream.Close();
```

## Abschluss

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie mit Aspose.Cells für .NET eine Tabelle ein- und ausblenden. Mit dieser Funktion können Sie jetzt die Sichtbarkeit Ihrer Tabellenkalkulationen in Ihren Excel-Dateien steuern.

### Häufig gestellte Fragen (FAQ)

#### Wie kann ich Aspose.Cells für .NET installieren?

 Sie können Aspose.Cells für .NET installieren, indem Sie das entsprechende NuGet-Paket von herunterladen[Aspose-Veröffentlichungen](https://releases/aspose.com/cells/net/) und fügen Sie es Ihrem Visual Studio-Projekt hinzu.

#### Was ist die mindestens erforderliche Version von .NET Framework, um Aspose.Cells für .NET zu verwenden?

Aspose.Cells für .NET unterstützt .NET Framework 2.0 und höher.

#### Kann ich vorhandene Excel-Dateien mit Aspose.Cells für .NET öffnen und bearbeiten?

Ja, Sie können vorhandene Excel-Dateien mit Aspose.Cells für .NET öffnen und bearbeiten. Sie können auf Arbeitsblätter, Zellen, Formeln und andere Elemente der Excel-Datei zugreifen.

#### Unterstützt Aspose.Cells für .NET die Berichterstellung und den Export in andere Dateiformate?

Ja, Aspose.Cells für .NET unterstützt die Berichterstellung und den Export in Formate wie PDF, HTML, CSV, TXT usw.

#### Ist die Änderung der Excel-Datei dauerhaft?

Ja, die Bearbeitung der Excel-Datei ist dauerhaft, sobald Sie sie speichern. Speichern Sie unbedingt eine Sicherungskopie, bevor Sie Änderungen an der Originaldatei vornehmen.