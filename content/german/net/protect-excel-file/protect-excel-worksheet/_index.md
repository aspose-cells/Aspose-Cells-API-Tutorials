---
title: Schützen Sie das Excel-Arbeitsblatt
linktitle: Schützen Sie das Excel-Arbeitsblatt
second_title: Aspose.Cells für .NET API-Referenz
description: Entdecken Sie in diesem Tutorial, wie Sie eine Excel-Tabelle mit Aspose.Cells für .NET schützen. Schritt-für-Schritt-Anleitung in C#.
type: docs
weight: 50
url: /de/net/protect-excel-file/protect-excel-worksheet/
---
In diesem Tutorial sehen wir uns einen C#-Quellcode an, der die Aspose.Cells-Bibliothek zum Schutz einer Excel-Tabelle verwendet. Wir gehen jeden Schritt des Codes durch und erklären, wie er funktioniert. Befolgen Sie unbedingt die Anweisungen sorgfältig, um die gewünschten Ergebnisse zu erzielen.

## Schritt 1: Voraussetzungen

Stellen Sie vor dem Start sicher, dass Sie die Aspose.Cells-Bibliothek für .NET installiert haben. Sie können es von der offiziellen Website von Aspose erhalten. Stellen Sie außerdem sicher, dass Sie über eine aktuelle Version von Visual Studio oder einer anderen C#-Entwicklungsumgebung verfügen.

## Schritt 2: Erforderliche Namespaces importieren

Um die Aspose.Cells-Bibliothek verwenden zu können, müssen wir die erforderlichen Namespaces in unseren Code importieren. Fügen Sie oben in Ihrer C#-Quelldatei die folgenden Zeilen hinzu:

```csharp
using Aspose.Cells;
using System.IO;
```

## Schritt 3: Laden Sie die Excel-Datei

In diesem Schritt laden wir die Excel-Datei, die wir schützen möchten. Stellen Sie sicher, dass Sie den korrekten Pfad zum Verzeichnis angeben, das die Excel-Datei enthält. Verwenden Sie den folgenden Code, um die Datei hochzuladen:

```csharp
// Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Erstellen Sie einen Dateistrom, der die zu öffnende Excel-Datei enthält.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Instanziieren Sie ein Workbook-Objekt.
//Excel-Datei per Dateistream öffnen.
Workbook excel = new Workbook(fstream);
```

 Unbedingt austauschen`"YOUR_DOCUMENTS_DIR"` mit dem entsprechenden Pfad zu Ihrem Dokumentenverzeichnis.

## Schritt 4: Greifen Sie auf die Tabelle zu

Nachdem wir nun die Excel-Datei geladen haben, können wir auf das erste Arbeitsblatt zugreifen. Verwenden Sie den folgenden Code, um auf das erste Arbeitsblatt zuzugreifen:

```csharp
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei.
Worksheet worksheet = excel.Worksheets[0];
```

## Schritt 5: Schützen Sie das Arbeitsblatt

In diesem Schritt schützen wir die Tabelle mit einem Passwort. Verwenden Sie den folgenden Code, um die Tabelle zu schützen:

```csharp
// Schützen Sie das Arbeitsblatt mit einem Passwort.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 Ersetzen`"YOUR_PASSWORD"` mit dem Passwort, das Sie zum Schutz der Tabelle verwenden möchten.

## Schritt 6: Speichern Sie die geänderte Excel-Datei, nachdem wir sie geschützt haben

In der Tabelle speichern wir die geänderte Excel-Datei im Standardformat. Verwenden Sie den folgenden Code, um die Excel-Datei zu speichern:

```csharp
// Speichern Sie die geänderte Excel-Datei im Standardformat.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Stellen Sie sicher, dass Sie den richtigen Pfad zum Speichern der geänderten Excel-Datei angeben.

## Schritt 7: Dateistream schließen

Um alle Ressourcen freizugeben, müssen wir den Dateistream schließen, der zum Laden der Excel-Datei verwendet wird. Verwenden Sie den folgenden Code, um den Dateistream zu schließen:

```csharp
// Schließen Sie den Dateistream, um alle Ressourcen freizugeben.
fstream.Close();
```

Fügen Sie diesen Schritt unbedingt am Ende Ihres Codes ein.


### Beispielquellcode für Protect Excel Worksheet mit Aspose.Cells für .NET 
```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Erstellen eines Dateistreams, der die zu öffnende Excel-Datei enthält
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanziieren eines Workbook-Objekts
// Öffnen der Excel-Datei über den Dateistream
Workbook excel = new Workbook(fstream);
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei
Worksheet worksheet = excel.Worksheets[0];
// Schützen Sie das Arbeitsblatt mit einem Passwort
worksheet.Protect(ProtectionType.All, "aspose", null);
// Speichern der geänderten Excel-Datei im Standardformat
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// Schließen des Dateistreams, um alle Ressourcen freizugeben
fstream.Close();
```

## Abschluss

Herzlichen Glückwunsch! Sie verfügen jetzt über C#-Quellcode, mit dem Sie eine Excel-Tabelle mithilfe der Aspose.Cells-Bibliothek für .NET schützen können. Befolgen Sie die Schritte sorgfältig und passen Sie den Code an Ihre spezifischen Bedürfnisse an.

### FAQs (häufig gestellte Fragen)

#### Ist es möglich, mehrere Arbeitsblätter in einer Excel-Datei zu schützen?

A: Ja, Sie können mehrere Arbeitsblätter in einer Excel-Datei schützen, indem Sie die Schritte 4 bis 6 für jedes Arbeitsblatt wiederholen.

#### Wie kann ich bestimmte Berechtigungen für autorisierte Benutzer festlegen?

 A: Sie können die zusätzlichen Optionen nutzen, die von bereitgestellt werden`Protect`Methode zum Festlegen spezifischer Berechtigungen für autorisierte Benutzer. Weitere Informationen finden Sie in der Aspose.Cells-Dokumentation.

#### Kann ich die Excel-Datei selbst mit einem Passwort schützen?

A: Ja, Sie können die Excel-Datei selbst mit anderen Methoden der Aspose.Cells-Bibliothek mit einem Passwort schützen. Spezifische Beispiele finden Sie in der Dokumentation.

#### Unterstützt die Aspose.Cells-Bibliothek andere Excel-Dateiformate?

A: Ja, die Aspose.Cells-Bibliothek unterstützt eine Vielzahl von Excel-Dateiformaten, einschließlich XLSX, XLSM, XLSB, CSV usw.