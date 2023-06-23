---
title: Freigegebene Arbeitsmappe mit Passwort schützen oder Schutz aufheben
linktitle: Freigegebene Arbeitsmappe mit Passwort schützen oder Schutz aufheben
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie eine freigegebene Arbeitsmappe mit Aspose.Cells für .NET mit einem Kennwort schützen oder den Schutz aufheben.
type: docs
weight: 120
url: /de/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Der Schutz einer freigegebenen Arbeitsmappe mit einem Passwort ist wichtig, um den Datenschutz zu gewährleisten. Mit Aspose.Cells für .NET können Sie eine freigegebene Arbeitsmappe ganz einfach mithilfe von Kennwörtern schützen oder den Schutz aufheben. Befolgen Sie die folgenden Schritte, um die gewünschten Ergebnisse zu erzielen:

## Schritt 1: Ausgabeverzeichnis angeben

Zunächst müssen Sie das Ausgabeverzeichnis angeben, in dem die geschützte Excel-Datei gespeichert werden soll. So machen Sie es mit Aspose.Cells:

```csharp
// Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
```

## Schritt 2: Erstellen Sie eine leere Excel-Datei

Anschließend können Sie eine leere Excel-Datei erstellen, auf die Sie den Schutz anwenden oder den Schutz aufheben möchten. Hier ist ein Beispielcode:

```csharp
// Erstellen Sie eine leere Excel-Arbeitsmappe
Workbook wb = new Workbook();
```

## Schritt 3: Schützen Sie die freigegebene Arbeitsmappe oder heben Sie den Schutz auf

Nach dem Erstellen der Arbeitsmappe können Sie die freigegebene Arbeitsmappe durch Angabe des entsprechenden Kennworts schützen oder den Schutz aufheben. Hier ist wie:

```csharp
// Schützen Sie die freigegebene Arbeitsmappe mit einem Passwort
wb.ProtectSharedWorkbook("1234");

// Kommentieren Sie diese Zeile aus, um den Schutz der freigegebenen Arbeitsmappe aufzuheben
// wb.UnprotectSharedWorkbook("1234");
```

## Schritt 4: Speichern Sie die ausgegebene Excel-Datei

Sobald Sie den Schutz anwenden oder den Schutz aufheben, können Sie die geschützte Excel-Datei im angegebenen Ausgabeverzeichnis speichern. So geht's:

```csharp
// Speichern Sie die ausgegebene Excel-Datei
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Beispielquellcode für den Passwortschutz oder die Aufhebung des Schutzes einer freigegebenen Arbeitsmappe mit Aspose.Cells für .NET 
```csharp
//Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
//Erstellen Sie eine leere Excel-Datei
Workbook wb = new Workbook();
//Schützen Sie die freigegebene Arbeitsmappe mit einem Passwort
wb.ProtectSharedWorkbook("1234");
//Kommentieren Sie diese Zeile aus, um den Schutz der freigegebenen Arbeitsmappe aufzuheben
//wb.UnprotectSharedWorkbook("1234");
//Speichern Sie die ausgegebene Excel-Datei
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Abschluss

Das Schützen oder Aufheben des Schutzes einer freigegebenen Arbeitsmappe mit einem Passwort ist für die Gewährleistung der Datensicherheit unerlässlich. Mit Aspose.Cells für .NET können Sie diese Funktionalität ganz einfach zu Ihren Excel-Dateien hinzufügen. Indem Sie die Schritte in dieser Anleitung befolgen, können Sie Ihre freigegebenen Arbeitsmappen mithilfe von Kennwörtern effektiv schützen oder den Schutz aufheben. Experimentieren Sie mit Ihren eigenen Excel-Dateien und achten Sie auf die Sicherheit Ihrer sensiblen Daten.

### FAQs

#### F: Welche Arten von Schutz kann ich auf eine mit Aspose.Cells freigegebene Arbeitsmappe anwenden?
    
A: Mit Aspose.Cells können Sie eine freigegebene Arbeitsmappe durch die Angabe eines Passworts schützen, um unbefugten Zugriff, Änderung oder Löschung von Daten zu verhindern.

#### F: Kann ich eine freigegebene Arbeitsmappe schützen, ohne ein Passwort anzugeben?
    
A: Ja, Sie können eine freigegebene Arbeitsmappe schützen, ohne ein Kennwort anzugeben. Aus Sicherheitsgründen wird jedoch empfohlen, ein sicheres Passwort zu verwenden.

#### F: Wie kann ich den Schutz einer mit Aspose.Cells freigegebenen Arbeitsmappe aufheben?
    
A: Um den Schutz einer freigegebenen Arbeitsmappe aufzuheben, müssen Sie dasselbe Kennwort angeben, das zum Schutz der Arbeitsmappe verwendet wurde. Dadurch kann der Schutz aufgehoben werden und der Zugriff auf die Daten ist frei.

#### F: Hat der Schutz einer freigegebenen Arbeitsmappe Auswirkungen auf die Funktionen und Formeln in der Arbeitsmappe?
    
A: Wenn Sie eine freigegebene Arbeitsmappe schützen, können Benutzer weiterhin auf die in der Arbeitsmappe vorhandenen Funktionen und Formeln zugreifen. Der Schutz betrifft nur strukturelle Änderungen an der Arbeitsmappe.