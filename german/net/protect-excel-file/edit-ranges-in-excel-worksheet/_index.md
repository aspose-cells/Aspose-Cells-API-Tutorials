---
title: Bearbeiten Sie Bereiche im Excel-Arbeitsblatt
linktitle: Bearbeiten Sie Bereiche im Excel-Arbeitsblatt
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET bestimmte Bereiche in einer Excel-Tabelle bearbeiten. Schritt-für-Schritt-Anleitung in C#.
type: docs
weight: 20
url: /de/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
Microsoft Excel ist ein leistungsstarkes Tool zum Erstellen und Verwalten von Tabellenkalkulationen und bietet zahlreiche Funktionen zur Kontrolle und Sicherung von Daten. Eine dieser Funktionen besteht darin, Benutzern die Bearbeitung bestimmter Bereiche in einem Arbeitsblatt zu ermöglichen und gleichzeitig andere Teile zu schützen. In diesem Tutorial führen wir Sie Schritt für Schritt durch die Implementierung dieser Funktionalität mithilfe von Aspose.Cells für .NET, einer beliebten Bibliothek für die programmgesteuerte Arbeit mit Excel-Dateien.

Die Verwendung von Aspose.Cells für .NET ermöglicht Ihnen die einfache Bearbeitung von Bereichen in einer Excel-Tabelle und bietet eine benutzerfreundliche Oberfläche und erweiterte Funktionen. Führen Sie die folgenden Schritte aus, um Benutzern das Bearbeiten bestimmter Bereiche in einer Excel-Tabelle mit Aspose.Cells für .NET zu ermöglichen.
## Schritt 1: Einrichten der Umgebung

Stellen Sie sicher, dass Aspose.Cells für .NET in Ihrer Entwicklungsumgebung installiert ist. Laden Sie die Bibliothek von der offiziellen Website von Aspose herunter und überprüfen Sie die Dokumentation auf Installationsanweisungen.

## Schritt 2: Arbeitsmappe und Arbeitsblatt initialisieren

Zunächst müssen wir eine neue Arbeitsmappe erstellen und den Verweis auf das Arbeitsblatt abrufen, in dem wir die Änderung von Bereichen zulassen möchten. Verwenden Sie dazu den folgenden Code:

```csharp
// Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Erstellen Sie das Verzeichnis, falls es noch nicht vorhanden ist.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Instanziieren Sie eine neue Arbeitsmappe
Workbook workbook = new Workbook();

// Erstes Arbeitsblatt abrufen (Standard)
Worksheet sheet = workbook.Worksheets[0];
```

 In diesem Codeausschnitt definieren wir zunächst den Pfad zu dem Verzeichnis, in dem die Excel-Datei gespeichert wird. Als nächstes erstellen wir eine neue Instanz von`Workbook` Klasse und rufen Sie den Verweis auf das erste Arbeitsblatt mithilfe von ab`Worksheets`Eigentum.

## Schritt 3: Bearbeitbare Bereiche abrufen

Jetzt müssen wir die Bereiche abrufen, in denen wir Änderungen zulassen möchten. Verwenden Sie den folgenden Code:

```csharp
// Rufen Sie die veränderbaren Bereiche ab
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## Schritt 4: Geschützten Bereich festlegen

Bevor wir die Änderung von Bereichen zulassen, müssen wir einen geschützten Bereich definieren. Hier ist wie:

```csharp
// Definieren Sie einen geschützten Bereich
ProtectedRange ProtectedRange;

// Erstellen Sie den Bereich
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

 In diesem Code erstellen wir eine neue Instanz von`ProtectedRange` Klasse und nutzen Sie die`Add` -Methode, um den zu schützenden Bereich anzugeben.

## Schritt 5: Passwort angeben

Um die Sicherheit zu erhöhen, können Sie für den geschützten Bereich ein Passwort festlegen. Hier ist wie:

```csharp
// Passwort angeben
protectedBeach.Password = "YOUR_PASSWORD";
```

## Schritt 6: Schützen Sie das Arbeitsblatt

Nachdem wir nun den geschützten Bereich festgelegt haben, können wir das Arbeitsblatt schützen, um unbefugte Änderungen zu verhindern. Verwenden Sie den folgenden Code:

```csharp
// Schützen Sie das Arbeitsblatt
leaf.Protect(ProtectionType.All);
```

## Schritt 7: Speichern Sie die Excel-Datei

Abschließend speichern wir die Excel-Datei mit den vorgenommenen Änderungen. Hier ist der notwendige Code:

```csharp
// Speichern Sie die Excel-Datei
workbook.Save(dataDir + "protectedrange.out.xls");
```

### Beispielquellcode für „Bereiche im Excel-Arbeitsblatt bearbeiten“ mit Aspose.Cells für .NET 
```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Erstellen Sie ein Verzeichnis, falls es noch nicht vorhanden ist.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// Instanziieren Sie eine neue Arbeitsmappe
Workbook book = new Workbook();

// Rufen Sie das erste (Standard-)Arbeitsblatt ab
Worksheet sheet = book.Worksheets[0];

// Rufen Sie „Bearbeitungsbereiche zulassen“ ab
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;

// Definieren Sie ProtectedRange
ProtectedRange proteced_range;

// Erstellen Sie den Bereich
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];

// Geben Sie das Passwort an
proteced_range.Password = "YOUR_PASSWORD";

// Schützen Sie das Blatt
sheet.Protect(ProtectionType.All);

// Speichern Sie die Excel-Datei
book.Save(dataDir + "protectedrange.out.xls");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben gelernt, wie Sie Benutzern mit Aspose.Cells für .NET das Bearbeiten bestimmter Bereiche in einer Excel-Tabelle ermöglichen. Sie können diese Technik jetzt in Ihren eigenen Projekten anwenden und die Sicherheit Ihrer Excel-Dateien verbessern.


#### FAQs

#### F: Warum sollte ich Aspose.Cells für .NET verwenden, um Bereiche in einer Excel-Tabelle zu bearbeiten?
A: Aspose.Cells für .NET bietet eine leistungsstarke und benutzerfreundliche API für die Arbeit mit Excel-Dateien. Es bietet erweiterte Funktionen wie Bereichsmanipulation, Arbeitsblattschutz usw.

#### F: Kann ich in einem Arbeitsblatt mehrere bearbeitbare Bereiche festlegen?
 A: Ja, Sie können mit dem mehrere bearbeitbare Bereiche definieren`Add` Methode der`ProtectedRangeCollection` Sammlung. Jeder Bereich kann seine eigenen Schutzeinstellungen haben.

####  F: Ist es möglich, einen bearbeitbaren Bereich zu löschen, nachdem er definiert wurde?
 A: Ja, Sie können das verwenden`RemoveAt` Methode der`ProtectedRangeCollection` -Sammlung, um einen bestimmten bearbeitbaren Bereich durch Angabe seines Index zu entfernen.

#### F: Wie kann ich die geschützte Excel-Datei öffnen, nachdem ich sie gespeichert habe?
A: Sie müssen das beim Erstellen des geschützten Bereichs angegebene Passwort angeben, um die geschützte Excel-Datei zu öffnen. Bewahren Sie das Passwort unbedingt an einem sicheren Ort auf, um einen Verlust des Zugriffs auf die Daten zu verhindern.