---
title: Legen Sie Excel-Kopf- und -Fußzeilen fest
linktitle: Legen Sie Excel-Kopf- und -Fußzeilen fest
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET Kopf- und Fußzeilen in Excel festlegen.
type: docs
weight: 100
url: /de/net/excel-page-setup/set-excel-headers-and-footers/
---

In diesem Tutorial zeigen wir Ihnen Schritt für Schritt, wie Sie mit Aspose.Cells für .NET Kopf- und Fußzeilen in Excel festlegen. Wir werden C#-Quellcode verwenden, um den Prozess zu veranschaulichen.

## Schritt 1: Einrichten der Umgebung

Stellen Sie sicher, dass Aspose.Cells für .NET auf Ihrem Computer installiert ist. Erstellen Sie außerdem ein neues Projekt in Ihrer bevorzugten Entwicklungsumgebung.

## Schritt 2: Erforderliche Bibliotheken importieren

Importieren Sie in Ihre Codedatei die Bibliotheken, die für die Arbeit mit Aspose.Cells erforderlich sind. Hier ist der entsprechende Code:

```csharp
using Aspose.Cells;
```

## Schritt 3: Datenverzeichnis festlegen

Legen Sie das Datenverzeichnis fest, in dem Sie die geänderte Excel-Datei speichern möchten. Verwenden Sie den folgenden Code:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Geben Sie unbedingt den vollständigen Verzeichnispfad an.

## Schritt 4: Arbeitsmappe und Arbeitsblatt erstellen

Erstellen Sie ein neues Arbeitsmappenobjekt und navigieren Sie mit dem folgenden Code zum ersten Arbeitsblatt in der Arbeitsmappe:

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Dadurch wird eine leere Arbeitsmappe mit einem Arbeitsblatt erstellt und Zugriff auf das PageSetup-Objekt dieses Arbeitsblatts gewährt.

## Schritt 5: Header festlegen

 Legen Sie die Tabellenkopfzeilen mit fest`SetHeader` Methoden des PageSetup-Objekts. Hier ist ein Beispielcode:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Dadurch werden der Arbeitsblattname, das aktuelle Datum und die aktuelle Uhrzeit sowie der Dateiname in den Kopfzeilen festgelegt.

## Schritt 6: Fußzeilen definieren

 Legen Sie Tabellenfußzeilen mit fest`SetFooter` Methoden des PageSetup-Objekts. Hier ist ein Beispielcode:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Dadurch werden jeweils eine Textzeichenfolge, die aktuelle Seitenzahl und die Gesamtzahl der Seiten in den Fußzeilen festgelegt.

## Schritt 7: Speichern der geänderten Arbeitsmappe

Speichern Sie die geänderte Arbeitsmappe mit dem folgenden Code:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Dadurch wird die geänderte Arbeitsmappe im angegebenen Datenverzeichnis gespeichert.

### Beispielquellcode für das Festlegen von Excel-Kopf- und -Fußzeilen mit Aspose.Cells für .NET 
```csharp
// Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanziieren eines Workbook-Objekts
Workbook excel = new Workbook();
// Abrufen der Referenz des PageSetup des Arbeitsblatts
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Festlegen des Arbeitsblattnamens im linken Abschnitt der Kopfzeile
pageSetup.SetHeader(0, "&A");
//Aktuelles Datum und aktuelle Uhrzeit im mittleren Bereich der Kopfzeile einstellen
// und Ändern der Schriftart der Kopfzeile
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Festlegen des aktuellen Dateinamens im rechten Abschnitt der Kopfzeile und Ändern des
// Schriftart der Kopfzeile
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Legen Sie im linken Bereich der Fußzeile eine Zeichenfolge fest und ändern Sie die Schriftart
// eines Teils dieser Zeichenfolge ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Festlegen der aktuellen Seitenzahl im mittleren Bereich der Fußzeile
pageSetup.SetFooter(1, "&P");
// Festlegen der Seitenanzahl im rechten Bereich der Fußzeile
pageSetup.SetFooter(2, "&N");
// Speichern Sie die Arbeitsmappe.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Abschluss

Sie haben jetzt gelernt, wie Sie mit Aspose.Cells für .NET Kopf- und Fußzeilen in Excel festlegen. Dieses Tutorial führte Sie durch jeden Schritt des Prozesses, von der Einrichtung der Umgebung bis zum Speichern der geänderten Arbeitsmappe. Erkunden Sie die Funktionen von Aspose.Cells weiter, um weitere Manipulationen an Ihren Excel-Dateien vorzunehmen.

### Häufig gestellte Fragen (FAQ)

#### 1. Wie kann ich Aspose.Cells für .NET auf meinem System installieren?
Um Aspose.Cells für .NET zu installieren, müssen Sie das Installationspaket von der offiziellen Website von Aspose herunterladen und den Anweisungen in der Dokumentation folgen.

#### 2. Funktioniert diese Methode mit allen Excel-Versionen?
Ja, die Methode zum Festlegen von Kopf- und Fußzeilen mit Aspose.Cells für .NET funktioniert mit allen unterstützten Versionen von Excel.

#### 3. Kann ich Kopf- und Fußzeilen weiter anpassen?
Ja, Aspose.Cells bietet umfangreiche Funktionen zum Anpassen von Kopf- und Fußzeilen, einschließlich Textplatzierung, Farbe, Schriftart, Seitenzahlen und mehr.

#### 4. Wie kann ich Kopf- und Fußzeilen dynamische Informationen hinzufügen?
Mithilfe spezieller Variablen und Formatierungscodes können Sie Kopf- und Fußzeilen dynamische Informationen wie aktuelles Datum, Uhrzeit, Dateiname, Seitenzahl usw. hinzufügen.

#### 5. Kann ich Kopf- und Fußzeilen entfernen, nachdem ich sie festgelegt habe?
 Ja, Sie können Kopf- und Fußzeilen mit entfernen`ClearHeaderFooter` Methode der`PageSetup` Objekt. Dadurch werden die Standardkopf- und -fußzeilen wiederhergestellt.