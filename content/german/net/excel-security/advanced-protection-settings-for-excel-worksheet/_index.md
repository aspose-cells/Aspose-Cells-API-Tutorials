---
title: Erweiterte Schutzeinstellungen für Excel-Arbeitsblätter
linktitle: Erweiterte Schutzeinstellungen für Excel-Arbeitsblätter
second_title: Aspose.Cells für .NET API-Referenz
description: Schützen Sie Ihre Excel-Dateien, indem Sie mit Aspose.Cells für .NET erweiterte Schutzeinstellungen festlegen.
type: docs
weight: 10
url: /de/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
In diesem Tutorial führen wir Sie durch die Schritte zum Festlegen erweiterter Schutzeinstellungen für eine Excel-Tabelle mithilfe der Aspose.Cells-Bibliothek für .NET. Befolgen Sie die nachstehenden Anweisungen, um diese Aufgabe abzuschließen.

## Schritt 1: Vorbereitung

Stellen Sie sicher, dass Sie Aspose.Cells für .NET installiert und ein C#-Projekt in Ihrer bevorzugten integrierten Entwicklungsumgebung (IDE) erstellt haben.

## Schritt 2: Legen Sie den Dokumentverzeichnispfad fest

 Erkläre a`dataDir` Variable und initialisieren Sie sie mit dem Pfad zu Ihrem Dokumentenverzeichnis. Zum Beispiel :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Unbedingt austauschen`"YOUR_DOCUMENTS_DIRECTORY"` mit dem tatsächlichen Pfad zu Ihrem Verzeichnis.

## Schritt 3: Erstellen Sie einen Dateistream, um die Excel-Datei zu öffnen

 Ein ... kreieren`FileStream` Objekt, das die zu öffnende Excel-Datei enthält:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Stellen Sie sicher, dass Sie über die Excel-Datei verfügen`book1.xls` in Ihrem Dokumentenverzeichnis oder geben Sie den korrekten Dateinamen und Speicherort an.

## Schritt 4: Instanziieren Sie ein Arbeitsmappenobjekt und öffnen Sie die Excel-Datei

 Benutzen Sie die`Workbook`Klasse von Aspose.Cells, um ein Workbook-Objekt zu instanziieren und die angegebene Excel-Datei über den Dateistream zu öffnen:

```csharp
Workbook excel = new Workbook(fstream);
```

## Schritt 5: Greifen Sie auf das erste Arbeitsblatt zu

Navigieren Sie zum ersten Arbeitsblatt der Excel-Datei:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Schritt 6: Legen Sie die Arbeitsblattschutzeinstellungen fest

Verwenden Sie die Eigenschaften des Arbeitsblattobjekts, um die Arbeitsblattschutzeinstellungen nach Bedarf festzulegen. Zum Beispiel :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Legen Sie bei Bedarf weitere Schutzeinstellungen fest ...
```

## Schritt 7: Speichern Sie die geänderte Excel-Datei

 Speichern Sie die geänderte Excel-Datei mit`Save` Methode des Workbook-Objekts:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Geben Sie unbedingt den gewünschten Pfad und Dateinamen für die Ausgabedatei an.

## Schritt 8: Schließen Sie den Dateistream

Schließen Sie nach dem Speichern den Dateistream, um alle zugehörigen Ressourcen freizugeben:

```csharp
fstream.Close();
```
	
### Beispielquellcode für erweiterte Schutzeinstellungen für Excel-Arbeitsblätter mit Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Erstellen eines Dateistreams, der die zu öffnende Excel-Datei enthält
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanziieren eines Workbook-Objekts
// Öffnen der Excel-Datei über den Dateistream
Workbook excel = new Workbook(fstream);
// Zugriff auf das erste Arbeitsblatt in der Excel-Datei
Worksheet worksheet = excel.Worksheets[0];
// Beschränken Sie Benutzer darauf, Spalten des Arbeitsblatts zu löschen
worksheet.Protection.AllowDeletingColumn = false;
// Beschränken Sie Benutzer darauf, Zeilen des Arbeitsblatts zu löschen
worksheet.Protection.AllowDeletingRow = false;
// Einschränken der Bearbeitung von Inhalten des Arbeitsblatts durch Benutzer
worksheet.Protection.AllowEditingContent = false;
// Beschränken Sie die Bearbeitung von Objekten des Arbeitsblatts durch Benutzer
worksheet.Protection.AllowEditingObject = false;
// Einschränken der Bearbeitung von Szenarien des Arbeitsblatts durch Benutzer
worksheet.Protection.AllowEditingScenario = false;
//Beschränken der Filterung durch Benutzer
worksheet.Protection.AllowFiltering = false;
// Ermöglicht Benutzern das Formatieren von Zellen des Arbeitsblatts
worksheet.Protection.AllowFormattingCell = true;
// Ermöglicht Benutzern das Formatieren von Zeilen des Arbeitsblatts
worksheet.Protection.AllowFormattingRow = true;
// Benutzern das Einfügen von Spalten in das Arbeitsblatt ermöglichen
worksheet.Protection.AllowFormattingColumn = true;
// Benutzern das Einfügen von Hyperlinks in das Arbeitsblatt ermöglichen
worksheet.Protection.AllowInsertingHyperlink = true;
// Benutzern erlauben, Zeilen in das Arbeitsblatt einzufügen
worksheet.Protection.AllowInsertingRow = true;
// Benutzern erlauben, gesperrte Zellen des Arbeitsblatts auszuwählen
worksheet.Protection.AllowSelectingLockedCell = true;
// Ermöglichen, dass Benutzer nicht gesperrte Zellen des Arbeitsblatts auswählen
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Benutzern das Sortieren ermöglichen
worksheet.Protection.AllowSorting = true;
// Benutzern die Verwendung von Pivot-Tabellen im Arbeitsblatt ermöglichen
worksheet.Protection.AllowUsingPivotTable = true;
// Speichern der geänderten Excel-Datei
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Schließen des Dateistreams, um alle Ressourcen freizugeben
fstream.Close();
```

## Abschluss

Herzlichen Glückwunsch! Sie haben jetzt gelernt, wie Sie mit Aspose.Cells für .NET erweiterte Schutzeinstellungen für eine Excel-Tabelle festlegen. Nutzen Sie dieses Wissen, um Ihre Excel-Dateien zu sichern und Benutzeraktionen einzuschränken.

### FAQs

#### F: Wie kann ich in meiner IDE ein neues C#-Projekt erstellen?

A: Die Schritte zum Erstellen eines neuen C#-Projekts können je nach verwendeter IDE variieren. Ausführliche Anweisungen finden Sie in der Dokumentation Ihrer IDE.

#### F: Ist es möglich, andere benutzerdefinierte Schutzeinstellungen als die im Tutorial erwähnten festzulegen?

A: Ja, Aspose.Cells bietet eine breite Palette an Schutzeinstellungen, die Sie an Ihre spezifischen Bedürfnisse anpassen können. Weitere Informationen finden Sie in der Aspose.Cells-Dokumentation.

#### F: Welches Dateiformat wird zum Speichern der geänderten Excel-Datei im Beispielcode verwendet?

A: Im Beispielcode wird die geänderte Excel-Datei im Excel 97-2003-Format (.xls) gespeichert. Bei Bedarf können Sie andere von Aspose.Cells unterstützte Formate auswählen.

#### F: Wie kann ich auf andere Arbeitsblätter in der Excel-Datei zugreifen?

 A: Sie können über den Index oder den Blattnamen auf andere Arbeitsblätter zugreifen, zum Beispiel:`Worksheet worksheet = excel.Worksheets[1];` oder`Worksheet worksheet = excel.Worksheets[" SheetName"];`.