---
title: Erlauben Sie dem Benutzer, Bereiche im Excel-Arbeitsblatt zu bearbeiten
linktitle: Erlauben Sie dem Benutzer, Bereiche im Excel-Arbeitsblatt zu bearbeiten
second_title: Aspose.Cells für .NET API-Referenz
description: Ermöglichen Sie Benutzern das Bearbeiten bestimmter Bereiche in einer Excel-Tabelle mit Aspose.Cells für .NET. Schritt-für-Schritt-Anleitung mit Quellcode in C#.
type: docs
weight: 10
url: /de/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
In diesem Leitfaden führen wir Sie durch die Verwendung von Aspose.Cells für .NET, damit der Benutzer bestimmte Bereiche in einer Excel-Tabelle bearbeiten kann. Führen Sie die folgenden Schritte aus, um diese Aufgabe auszuführen.

## Schritt 1: Einrichten der Umgebung

Stellen Sie sicher, dass Sie Ihre Entwicklungsumgebung eingerichtet und Aspose.Cells für .NET installiert haben. Sie können die neueste Version der Bibliothek von der offiziellen Website von Aspose herunterladen.

## Schritt 2: Erforderliche Namespaces importieren

Importieren Sie in Ihrem C#-Projekt die erforderlichen Namespaces, um mit Aspose.Cells zu arbeiten:

```csharp
using Aspose.Cells;
```

## Schritt 3: Legen Sie den Pfad zum Dokumentenverzeichnis fest

 Erkläre a`dataDir` Variable, um den Pfad zu dem Verzeichnis anzugeben, in dem Sie die generierte Excel-Datei speichern möchten:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Unbedingt ersetzen`"YOUR_DOCUMENT_DIRECTORY"` mit dem richtigen Pfad auf Ihrem System.

## Schritt 4: Erstellen eines Arbeitsmappenobjekts

Instanziieren Sie ein neues Workbook-Objekt, das die Excel-Arbeitsmappe darstellt, die Sie erstellen möchten:

```csharp
Workbook book = new Workbook();
```

## Schritt 5: Zugriff auf das erste Arbeitsblatt

Navigieren Sie mit dem folgenden Code zum ersten Arbeitsblatt in der Excel-Arbeitsmappe:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Schritt 6: Autorisierte Änderungsbereiche abrufen

 Rufen Sie die Sammlung der zulässigen Bearbeitungsbereiche mithilfe von ab`AllowEditRanges` Eigentum:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Schritt 7: Definieren Sie einen geschützten Bereich

 Definieren Sie einen geschützten Bereich mithilfe von`Add` Methode der`AllowEditRanges` Sammlung:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Hier haben wir einen geschützten Bereich „r2“ erstellt, der sich von Zelle A1 bis Zelle C3 erstreckt.

## Schritt 8: Passwort festlegen

 Geben Sie mithilfe von ein Passwort für den geschützten Bereich an`Password` Eigentum:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Unbedingt ersetzen`"YOUR_PASSWORD"` mit dem gewünschten Passwort.

## Schritt 9: Schützen des Arbeitsblatts

 Schützen Sie das Arbeitsblatt mit dem`Protect` Methode der`Worksheet` Objekt:

```csharp
sheet.Protect(ProtectionType.All);
```

Dadurch wird die Tabelle geschützt, indem jegliche Änderung außerhalb der zulässigen Bereiche verhindert wird.

## Schritt 10: Registrieren des

  Excel-Datei

 Speichern Sie die generierte Excel-Datei mit`Save` Methode der`Workbook` Objekt:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Geben Sie unbedingt den gewünschten Dateinamen und den richtigen Pfad an.

### Beispielquellcode für „Benutzer darf Bereiche in Excel-Arbeitsblättern bearbeiten“ mithilfe von Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
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
proteced_range.Password = "123";
// Schützen Sie das Blatt
sheet.Protect(ProtectionType.All);
// Speichern Sie die Excel-Datei
book.Save(dataDir + "protectedrange.out.xls");
```

## Abschluss

Sie haben nun gelernt, wie Sie Aspose.Cells für .NET verwenden, um dem Benutzer die Bearbeitung bestimmter Bereiche in einer Excel-Tabelle zu ermöglichen. Fühlen Sie sich frei, die von Aspose.Cells angebotenen Funktionen weiter zu erkunden, um Ihren spezifischen Anforderungen gerecht zu werden.


### FAQs

#### 1. Wie kann ein Benutzer bestimmte Bereiche in einer Excel-Tabelle bearbeiten?

 Du kannst den ... benutzen`ProtectedRangeCollection` Klasse, um zulässige Änderungsbereiche zu definieren. Benutzen Sie die`Add` Methode zum Erstellen eines neuen geschützten Bereichs mit den gewünschten Zellen.

#### 2. Kann ich für autorisierte Änderungsbereiche ein Passwort festlegen?

 Ja, Sie können mit dem ein Passwort festlegen`Password` Eigentum der`ProtectedRange` Objekt. Dadurch wird der Zugriff nur auf Benutzer mit Passwort beschränkt.

#### 3. Wie schütze ich die Tabelle, nachdem die zulässigen Bereiche festgelegt wurden?

 Benutzen Sie die`Protect` Methode der`Worksheet` Objekt zum Schutz des Arbeitsblatts. Dadurch wird verhindert, dass Änderungen außerhalb der zulässigen Bereiche erfolgen und möglicherweise zur Eingabe eines Kennworts aufgefordert werden, sofern Sie eines angegeben haben.