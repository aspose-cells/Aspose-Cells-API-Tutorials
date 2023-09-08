---
title: Bild in Kopf- und Fußzeile einfügen
linktitle: Bild in Kopf- und Fußzeile einfügen
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET ein Bild in die Kopf- oder Fußzeile eines Excel-Dokuments einfügen. Schritt-für-Schritt-Anleitung mit Quellcode in C#.
type: docs
weight: 60
url: /de/net/excel-page-setup/insert-image-in-header-footer/
---
Die Möglichkeit, ein Bild in die Kopf- oder Fußzeile eines Excel-Dokuments einzufügen, kann sehr nützlich sein, um Ihre Berichte anzupassen oder Firmenlogos hinzuzufügen. In diesem Artikel führen wir Sie Schritt für Schritt durch das Einfügen eines Bildes in die Kopf- oder Fußzeile eines Excel-Dokuments mit Aspose.Cells für .NET. Sie erfahren, wie Sie dies mithilfe von C#-Quellcode erreichen.

## Schritt 1: Einrichten der Umgebung

Bevor Sie beginnen, stellen Sie sicher, dass Aspose.Cells für .NET auf Ihrem Computer installiert ist. Erstellen Sie außerdem ein neues Projekt in Ihrer bevorzugten Entwicklungsumgebung.

## Schritt 2: Erforderliche Bibliotheken importieren

Importieren Sie in Ihre Codedatei die Bibliotheken, die für die Arbeit mit Aspose.Cells erforderlich sind. Hier ist der entsprechende Code:

```csharp
using Aspose.Cells;
```

## Schritt 3: Dokumentverzeichnis festlegen

Legen Sie das Verzeichnis fest, in dem sich das Excel-Dokument befindet, mit dem Sie arbeiten möchten. Verwenden Sie den folgenden Code, um das Verzeichnis festzulegen:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Geben Sie unbedingt den vollständigen Verzeichnispfad an.

## Schritt 4: Erstellen eines Arbeitsmappenobjekts

Das Workbook-Objekt stellt das Excel-Dokument dar, mit dem Sie arbeiten werden. Sie können es mit dem folgenden Code erstellen:

```csharp
Workbook workbook = new Workbook();
```

Dadurch wird ein neues leeres Workbook-Objekt erstellt.

## Schritt 5: Speichern der Bild-URL

Definieren Sie die URL oder den Pfad des Bildes, das Sie in die Kopf- oder Fußzeile einfügen möchten. Verwenden Sie den folgenden Code, um die Bild-URL zu speichern:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Stellen Sie sicher, dass der angegebene Pfad korrekt ist und das Bild an diesem Speicherort vorhanden ist.

## Schritt 6: Öffnen der Bilddatei

Um die Bilddatei zu öffnen, verwenden wir ein FileStream-Objekt und lesen die Binärdaten aus dem Bild. Hier ist der entsprechende Code:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Stellen Sie sicher, dass der Bildpfad korrekt ist und Sie über die richtigen Zugriffsberechtigungen verfügen.

## Schritt 7: Konfigurieren des PageSetup

Das PageSetup-Objekt wird verwendet, um die Seiteneinstellungen des Excel-Dokuments einschließlich der Kopf- und Fußzeile festzulegen. Verwenden Sie den folgenden Code, um das PageSetup-Objekt des ersten Arbeitsblatts abzurufen:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

Dadurch können Sie auf die Seiteneinstellungen für das erste Arbeitsblatt in der Arbeitsmappe zugreifen.

## Schritt 8: Das Bild zur Kopfzeile hinzufügen

Verwenden Sie die SetHeaderPicture()-Methode des PageSetup-Objekts, um das Bild im mittleren Abschnitt des Seitenkopfs festzulegen. Hier ist der entsprechende Code:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Dadurch wird das angegebene Bild zum Seitenkopf hinzugefügt.

## Schritt 9: Hinzufügen eines Skripts zum Header

Um dem Seitenkopf ein Skript hinzuzufügen, verwenden Sie die SetHeader()-Methode des PageSetup-Objekts. Hier ist der entsprechende Code:

```csharp
pageSetup.SetHeader(1, "&G");
```

Dadurch wird das angegebene Skript zum Seitenkopf hinzugefügt. In diesem Beispiel zeigt das „&G“-Skript die Seitenzahl an.

## Schritt 10: Blattnamen zur Kopfzeile hinzufügen

Um den Blattnamen im Seitenkopf anzuzeigen, verwenden Sie erneut die SetHeader()-Methode des PageSetup-Objekts. Hier ist der entsprechende Code:

```csharp
pageSetup.SetHeader(2, "&A");
```

Dadurch wird der Blattname zum Seitenkopf hinzugefügt. Zur Darstellung des Blattnamens wird das „&A“-Skript verwendet.

## Schritt 11: Speichern der Arbeitsmappe

Um Änderungen an der Arbeitsmappe zu speichern, verwenden Sie die Save()-Methode des Workbook-Objekts. Hier ist der entsprechende Code:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Dadurch wird die Arbeitsmappe mit den Änderungen im angegebenen Verzeichnis gespeichert.

## Schritt 12: Schließen des FileStream

Stellen Sie nach dem Lesen der Binärdaten aus dem Bild sicher, dass Sie FileStream schließen, um die Ressourcen freizugeben. Verwenden Sie den folgenden Code, um den FileStream zu schließen:

```csharp
inFile.Close();
```

Stellen Sie sicher, dass Sie FileStreams immer schließen, wenn Sie sie nicht mehr verwenden.

### Beispielquellcode für „Bild in Kopf- und Fußzeile einfügen“ mit Aspose.Cells für .NET 
```csharp
//Der Pfad zum Dokumentenverzeichnis.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Erstellen eines Workbook-Objekts
Workbook workbook = new Workbook();
// Erstellen einer String-Variable zum Speichern der URL des Logos/Bildes
string logo_url = dataDir + "aspose-logo.jpg";
// Deklarieren eines FileStream-Objekts
FileStream inFile;
// Deklarieren eines Byte-Arrays
byte[] binaryData;
// Erstellen der Instanz des FileStream-Objekts, um das Logo/Bild im Stream zu öffnen
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// Instanziieren des Byte-Arrays der Größe des FileStream-Objekts
binaryData = new Byte[inFile.Length];
// Liest einen Block von Bytes aus dem Stream und schreibt Daten in einen bestimmten Puffer eines Byte-Arrays.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Erstellen eines PageSetup-Objekts, um die Seiteneinstellungen des ersten Arbeitsblatts der Arbeitsmappe abzurufen
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Setzen des Logos/Bildes im zentralen Bereich des Seitenkopfes
pageSetup.SetHeaderPicture(1, binaryData);
// Festlegen des Skripts für das Logo/Bild
pageSetup.SetHeader(1, "&G");
// Festlegen des Blattnamens im rechten Abschnitt des Seitenkopfs mit dem Skript
pageSetup.SetHeader(2, "&A");
// Speichern der Arbeitsmappe
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//Schließen des FileStream-Objekts
inFile.Close();       
```
## Abschluss

Herzlichen Glückwunsch! Sie wissen jetzt, wie Sie mit Aspose.Cells für .NET ein Bild in die Kopf- oder Fußzeile eines Excel-Dokuments einfügen. Dieses Tutorial führte Sie durch jeden Schritt des Prozesses, von der Einrichtung der Umgebung bis zum Speichern der geänderten Arbeitsmappe. Experimentieren Sie gerne weiter mit den Funktionen von Aspose.Cells, um personalisierte und professionelle Excel-Dokumente zu erstellen.

### FAQs

#### F1: Ist es möglich, mehrere Bilder in die Kopf- oder Fußzeile eines Excel-Dokuments einzufügen?

A1: Ja, Sie können mehrere Bilder in die Kopf- oder Fußzeile eines Excel-Dokuments einfügen, indem Sie die Schritte 8 und 9 für jedes weitere Bild wiederholen.

#### F2: Welche Bildformate werden zum Einfügen in Kopf- oder Fußzeilen unterstützt?
A2: Aspose.Cells unterstützt eine Vielzahl gängiger Bildformate wie JPEG, PNG, GIF, BMP usw.

#### F3: Kann ich das Erscheinungsbild der Kopf- oder Fußzeile weiter anpassen?

A3: Ja, Sie können spezielle Skripte und Codes verwenden, um das Erscheinungsbild der Kopf- oder Fußzeile weiter zu formatieren und anzupassen. Weitere Informationen zu Anpassungsoptionen finden Sie in der Aspose.Cells-Dokumentation.

#### F4: Funktioniert Aspose.Cells mit verschiedenen Excel-Versionen?

A4: Ja, Aspose.Cells ist mit verschiedenen Versionen von Excel kompatibel, einschließlich Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 und Excel 2019.

#### F5: Ist es möglich, Bilder in andere Teile des Excel-Dokuments einzufügen, beispielsweise in Zellen oder Diagramme?

A5: Ja, Aspose.Cells bietet umfangreiche Funktionen zum Einfügen von Bildern in verschiedene Teile des Excel-Dokuments, einschließlich Zellen, Diagramme und Zeichnungsobjekte.