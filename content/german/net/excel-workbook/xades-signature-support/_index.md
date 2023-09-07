---
title: Xades-Signaturunterstützung
linktitle: Xades-Signaturunterstützung
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET eine Xades-Signatur zu einer Excel-Datei hinzufügen.
type: docs
weight: 190
url: /de/net/excel-workbook/xades-signature-support/
---
In diesem Artikel erklären wir Ihnen Schritt für Schritt den folgenden C#-Quellcode, der sich mit der Xades-Signaturunterstützung mithilfe der Aspose.Cells-Bibliothek für .NET befasst. Sie erfahren, wie Sie mit dieser Bibliothek eine digitale Xades-Signatur zu einer Excel-Datei hinzufügen. Außerdem geben wir Ihnen einen Überblick über den Unterzeichnungsprozess und dessen Durchführung. Befolgen Sie die nachstehenden Schritte, um aussagekräftige Ergebnisse zu erhalten.

## Schritt 1: Definieren Sie Quell- und Ausgabeverzeichnisse
Zunächst müssen wir die Quell- und Ausgabeverzeichnisse in unserem Code definieren. Diese Verzeichnisse geben an, wo sich die Quelldateien befinden und wo die Ausgabedatei gespeichert wird. Hier ist der entsprechende Code:

```csharp
// Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();
// Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
```

Passen Sie die Verzeichnispfade unbedingt nach Bedarf an.

## Schritt 2: Laden der Excel-Arbeitsmappe
Der nächste Schritt besteht darin, die Excel-Arbeitsmappe zu laden, zu der wir die digitale Xades-Signatur hinzufügen möchten. Hier ist der Code zum Laden der Arbeitsmappe:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Stellen Sie sicher, dass Sie den Namen der Quelldatei im Code korrekt angeben.

## Schritt 3: Konfigurieren der digitalen Signatur
Jetzt konfigurieren wir die digitale Signatur von Xades, indem wir die erforderlichen Informationen bereitstellen. Wir müssen die PFX-Datei angeben, die das digitale Zertifikat enthält, sowie das zugehörige Passwort. Hier ist der entsprechende Code:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Ersetzen Sie unbedingt „pfxPassword“ durch Ihr tatsächliches Passwort und „pfxFile“ durch den Pfad zur PFX-Datei.

## Schritt 4: Hinzufügen der digitalen Signatur
Nachdem wir nun die digitale Signatur konfiguriert haben, können wir sie der Excel-Arbeitsmappe hinzufügen. Hier ist der entsprechende Code:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

In diesem Schritt wird die digitale Signatur von Xades zur Excel-Arbeitsmappe hinzugefügt.

## Schritt 5: Speichern der Arbeitsmappe mit der Signatur
Abschließend speichern wir die Excel-Arbeitsmappe mit der hinzugefügten digitalen Signatur. Hier ist der entsprechende Code:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Passen Sie den Namen der Ausgabedatei unbedingt Ihren Bedürfnissen an.

### Beispielquellcode für Xades Signature Support mit Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();
//Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## Abschluss
Herzlichen Glückwunsch! Sie haben gelernt, wie Sie mit der Aspose.Cells-Bibliothek für .NET einer Excel-Datei eine digitale Xades-Signatur hinzufügen. Wenn Sie die in diesem Artikel beschriebenen Schritte befolgen, können Sie diese Funktionalität in Ihren eigenen Projekten implementieren. Fühlen Sie sich frei, mehr mit der Bibliothek zu experimentieren und andere leistungsstarke Funktionen zu entdecken, die sie bietet.

### FAQs

#### F: Was ist Xades?

A: Xades ist ein fortschrittlicher Standard für elektronische Signaturen, der die Integrität und Authentizität digitaler Dokumente gewährleistet.

#### F: Kann ich mit Aspose.Cells andere Arten digitaler Signaturen verwenden?

A: Ja, Aspose.Cells unterstützt auch andere Arten digitaler Signaturen, wie XMLDSig-Signaturen und PKCS#7-Signaturen.

#### F: Kann ich eine Signatur auf andere Dateitypen als Excel-Dateien anwenden?
 
A: Ja, Aspose.Cells ermöglicht auch die Anwendung digitaler Signaturen auf andere unterstützte Dateitypen wie Word-, PDF- und PowerPoint-Dateien.