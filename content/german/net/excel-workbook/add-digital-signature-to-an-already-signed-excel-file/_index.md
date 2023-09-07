---
title: Fügen Sie einer bereits signierten Excel-Datei eine digitale Signatur hinzu
linktitle: Fügen Sie einer bereits signierten Excel-Datei eine digitale Signatur hinzu
second_title: Aspose.Cells für .NET API-Referenz
description: Fügen Sie mit Aspose.Cells für .NET ganz einfach digitale Signaturen zu vorhandenen Excel-Dateien hinzu.
type: docs
weight: 30
url: /de/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
In dieser Schritt-für-Schritt-Anleitung erklären wir den bereitgestellten C#-Quellcode, der es Ihnen ermöglicht, mit Aspose.Cells für .NET eine digitale Signatur zu einer bereits signierten Excel-Datei hinzuzufügen. Führen Sie die folgenden Schritte aus, um einer vorhandenen Excel-Datei eine neue digitale Signatur hinzuzufügen.

## Schritt 1: Quell- und Ausgabeverzeichnis festlegen

```csharp
// Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();

// Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
```

In diesem ersten Schritt definieren wir die Quell- und Ausgabeverzeichnisse, die zum Laden der vorhandenen Excel-Datei verwendet werden und speichern die Datei mit der neuen digitalen Signatur.

## Schritt 2: Vorhandene Excel-Datei laden

```csharp
// Laden Sie die bereits signierte Excel-Arbeitsmappe
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Hier laden wir die bereits signierte Excel-Datei mit`Workbook` Klasse von Aspose.Cells.

## Schritt 3: Erstellen Sie die Sammlung digitaler Signaturen

```csharp
// Erstellen Sie die Sammlung digitaler Signaturen
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 Wir erstellen eine neue Sammlung digitaler Signaturen mit`DigitalSignatureCollection` Klasse.

## Schritt 4: Erstellen Sie ein neues Zertifikat

```csharp
// Erstellen Sie ein neues Zertifikat
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Hier erstellen wir aus der bereitgestellten Datei und dem Passwort ein neues Zertifikat.

## Schritt 5: Fügen Sie der Sammlung eine neue digitale Signatur hinzu

```csharp
// Erstellen Sie eine neue digitale Signatur
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Fügen Sie die digitale Signatur zur Sammlung hinzu
dsCollection.Add(signature);
```

 Wir erstellen eine neue digitale Signatur mit dem`DigitalSignature` Klasse und fügen Sie sie der Sammlung digitaler Signaturen hinzu.

## Schritt 6: Fügen Sie die Sammlung digitaler Signaturen zur Arbeitsmappe hinzu

```csharp
//Fügen Sie die Sammlung digitaler Signaturen zur Arbeitsmappe hinzu
workbook.AddDigitalSignature(dsCollection);
```

 Wir fügen die Sammlung digitaler Signaturen mithilfe von der vorhandenen Excel-Arbeitsmappe hinzu`AddDigitalSignature()` Methode.

## Schritt 7: Speichern und schließen Sie die Arbeitsmappe

```csharp
// Speichern Sie die Arbeitsmappe und schließen Sie sie
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Wir speichern die Arbeitsmappe mit der neuen digitalen Signatur im angegebenen Ausgabeverzeichnis, schließen sie anschließend und geben die zugehörigen Ressourcen frei.

### Beispielquellcode für das Hinzufügen einer digitalen Signatur zu einer bereits signierten Excel-Datei mit Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();
//Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
//Zertifikatsdatei und ihr Passwort
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Laden Sie die Arbeitsmappe, die bereits digital signiert ist, um eine neue digitale Signatur hinzuzufügen
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Erstellen Sie die Sammlung digitaler Signaturen
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Neues Zertifikat erstellen
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Erstellen Sie eine neue digitale Signatur und fügen Sie sie der Sammlung digitaler Signaturen hinzu
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Fügen Sie der Arbeitsmappe eine Sammlung digitaler Signaturen hinzu
workbook.AddDigitalSignature(dsCollection);
//Speichern Sie die Arbeitsmappe und entsorgen Sie sie.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben jetzt erfahren, wie Sie mit Aspose.Cells für .NET eine digitale Signatur zu einer bereits signierten Excel-Datei hinzufügen. Digitale Signaturen verleihen Ihren Excel-Dateien eine zusätzliche Sicherheitsebene und stellen deren Authentizität und Integrität sicher.

### Häufig gestellte Fragen

#### F: Was ist Aspose.Cells für .NET?

A: Aspose.Cells für .NET ist eine leistungsstarke Klassenbibliothek, die es .NET-Entwicklern ermöglicht, Excel-Dateien problemlos zu erstellen, zu ändern, zu konvertieren und zu manipulieren.

#### F: Was ist eine digitale Signatur in einer Excel-Datei?

A: Eine digitale Signatur in einer Excel-Datei ist ein elektronisches Zeichen, das die Authentizität, Integrität und Herkunft des Dokuments garantiert. Damit wird überprüft, ob die Datei seit der Signatur nicht verändert wurde und aus einer zuverlässigen Quelle stammt.

#### F: Welche Vorteile bietet das Hinzufügen einer digitalen Signatur zu einer Excel-Datei?

A: Das Hinzufügen einer digitalen Signatur zu einer Excel-Datei bietet mehrere Vorteile, darunter Schutz vor unbefugten Änderungen, Gewährleistung der Datenintegrität, Authentifizierung des Autors des Dokuments und Schaffung von Vertrauen in die darin enthaltenen Informationen.

#### F: Kann ich einer Excel-Datei mehrere digitale Signaturen hinzufügen?

A: Ja, mit Aspose.Cells können Sie einer Excel-Datei mehrere digitale Signaturen hinzufügen. Sie können eine Sammlung digitaler Signaturen erstellen und diese in einem Vorgang zur Datei hinzufügen.

#### F: Welche Voraussetzungen gelten für das Hinzufügen einer digitalen Signatur zu einer Excel-Datei?

A: Um einer Excel-Datei eine digitale Signatur hinzuzufügen, benötigen Sie ein gültiges digitales Zertifikat, das zum Signieren des Dokuments verwendet wird. Stellen Sie sicher, dass Sie über das richtige Zertifikat und Passwort verfügen, bevor Sie die digitale Signatur hinzufügen.