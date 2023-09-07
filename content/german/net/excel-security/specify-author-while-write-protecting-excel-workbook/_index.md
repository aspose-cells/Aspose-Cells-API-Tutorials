---
title: Geben Sie beim Schreibschutz der Excel-Arbeitsmappe den Autor an
linktitle: Geben Sie beim Schreibschutz der Excel-Arbeitsmappe den Autor an
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie Ihre Excel-Arbeitsmappen mit Aspose.Cells für .NET schützen und anpassen. Schritt-für-Schritt-Anleitung in C#.
type: docs
weight: 30
url: /de/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

In diesem Tutorial zeigen wir Ihnen, wie Sie den Autor beim Schreibschutz einer Excel-Arbeitsmappe mithilfe der Aspose.Cells-Bibliothek für .NET angeben.

## Schritt 1: Vorbereiten der Umgebung

Bevor Sie beginnen, stellen Sie sicher, dass Aspose.Cells für .NET auf Ihrem Computer installiert ist. Laden Sie die Bibliothek von der offiziellen Website von Aspose herunter und befolgen Sie die bereitgestellten Installationsanweisungen.

## Schritt 2: Quell- und Ausgabeverzeichnisse konfigurieren

Im bereitgestellten Quellcode müssen Sie die Quell- und Ausgabeverzeichnisse angeben. Modifiziere den`sourceDir` Und`outputDir` Variablen, indem Sie „IHR QUELLENVERZEICHNIS“ und „IHR AUSGABEVERZEICHNIS“ durch die jeweiligen absoluten Pfade auf Ihrem Computer ersetzen.

```csharp
// Quellverzeichnis
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Ausgabe Verzeichnis
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Schritt 3: Erstellen einer leeren Excel-Arbeitsmappe

Zunächst erstellen wir ein Workbook-Objekt, das eine leere Excel-Arbeitsmappe darstellt.

```csharp
// Erstellen Sie eine leere Arbeitsmappe.
Workbook wb = new Workbook();
```

## Schritt 4: Schreibschutz mit Passwort

 Als nächstes legen wir ein Passwort fest, um die Excel-Arbeitsmappe mit dem Schreibschutz zu schützen`WriteProtection.Password` Eigenschaft des Workbook-Objekts.

```csharp
// Schreibschutz der Arbeitsmappe mit Passwort.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Schritt 5: Angabe des Autors

 Jetzt geben wir den Autor der Excel-Arbeitsmappe mit an`WriteProtection.Author` Eigenschaft des Workbook-Objekts.

```csharp
// Geben Sie beim Schreibschutz der Arbeitsmappe den Autor an.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Schritt 6: Sichern Sie die geschützte Excel-Arbeitsmappe

 Sobald der Schreibschutz und der Autor festgelegt sind, können wir die Excel-Arbeitsmappe im XLSX-Format speichern`Save()` Methode.

```csharp
// Speichern Sie die Arbeitsmappe im XLSX-Format.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Beispielquellcode für Specify Author While Write Protecting Excel Workbook mit Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string sourceDir = "YOUR SOURCE DIRECTORY";

//Ausgabe Verzeichnis
string outputDir = "YOUR OUTPUT DIRECTORY";

// Erstellen Sie eine leere Arbeitsmappe.
Workbook wb = new Workbook();

// Schreibschutz der Arbeitsmappe mit Passwort.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Geben Sie beim Schreibschutz der Arbeitsmappe den Autor an.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Speichern Sie die Arbeitsmappe im XLSX-Format.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Abschluss

Herzlichen Glückwunsch! Sie haben jetzt erfahren, wie Sie den Autor angeben, wenn Sie eine Excel-Arbeitsmappe mit Aspose.Cells für .NET schreibgeschützt machen. Sie können diese Schritte auf Ihre eigenen Projekte anwenden, um Ihre Excel-Arbeitsmappen zu schützen und anzupassen.

Erkunden Sie gerne die Funktionen von Aspose.Cells für .NET für erweiterte Vorgänge an Excel-Dateien.

## FAQs

#### F: Kann ich eine Excel-Arbeitsmappe mit einem Schreibschutz versehen, ohne ein Passwort anzugeben?

 A: Ja, Sie können die Workbook-Objekte verwenden`WriteProtect()` Methode ohne Angabe eines Kennworts zum Schreibschutz einer Excel-Arbeitsmappe. Dadurch werden Änderungen an der Arbeitsmappe eingeschränkt, ohne dass ein Kennwort erforderlich ist.

#### F: Wie entferne ich den Schreibschutz aus einer Excel-Arbeitsmappe?

 A: Um den Schreibschutz aus einer Excel-Arbeitsmappe zu entfernen, können Sie Folgendes verwenden`Unprotect()` Methode des Worksheet-Objekts oder des`RemoveWriteProtection()` Methode des Workbook-Objekts, abhängig von Ihrem spezifischen Anwendungsfall. .

#### F: Ich habe das Passwort zum Schutz meiner Excel-Arbeitsmappe vergessen. Was kann ich machen ?

A: Wenn Sie das Passwort zum Schutz Ihrer Excel-Arbeitsmappe vergessen haben, können Sie es nicht direkt entfernen. Sie können jedoch versuchen, spezielle Tools von Drittanbietern zu verwenden, die Funktionen zur Kennwortwiederherstellung für geschützte Excel-Dateien bereitstellen.

#### F: Ist es möglich, beim Schreibschutz einer Excel-Arbeitsmappe mehrere Autoren anzugeben?

A: Nein, die Aspose.Cells for .NET-Bibliothek ermöglicht die Angabe eines einzelnen Autors beim Schreibschutz einer Excel-Arbeitsmappe. Wenn Sie mehrere Autoren angeben möchten, müssen Sie benutzerdefinierte Lösungen in Betracht ziehen, indem Sie die Excel-Datei direkt bearbeiten.