---
title: Externe Verbindung der XLSB-Datei lesen und schreiben
linktitle: Externe Verbindung der XLSB-Datei lesen und schreiben
second_title: Aspose.Cells für .NET API-Referenz
description: Erfahren Sie, wie Sie die externen Verbindungen einer XLSB-Datei mit Aspose.Cells für .NET lesen und ändern.
type: docs
weight: 130
url: /de/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Das Lesen und Schreiben externer Verbindungen in eine XLSB-Datei ist für die Bearbeitung von Daten aus externen Quellen in Ihren Excel-Arbeitsmappen unerlässlich. Mit Aspose.Cells für .NET können Sie externe Verbindungen mithilfe der folgenden Schritte einfach lesen und schreiben:

## Schritt 1: Geben Sie das Quellverzeichnis und das Ausgabeverzeichnis an

Zunächst müssen Sie das Quellverzeichnis angeben, in dem sich die XLSB-Datei mit der externen Verbindung befindet, sowie das Ausgabeverzeichnis, in dem Sie die geänderte Datei speichern möchten. So machen Sie es mit Aspose.Cells:

```csharp
// Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();

// Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
```

## Schritt 2: Laden Sie die Excel-XLSB-Quelldatei

Als Nächstes müssen Sie die Excel-XLSB-Quelldatei laden, für die Sie Lese- und Schreibvorgänge für externe Verbindungen durchführen möchten. Hier ist ein Beispielcode:

```csharp
// Laden Sie die Excel-XLSB-Quelldatei
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Schritt 3: Lesen und ändern Sie die externe Verbindung

Nach dem Laden der Datei können Sie auf die erste externe Verbindung zugreifen, bei der es sich eigentlich um eine Datenbankverbindung handelt. Sie können verschiedene Eigenschaften der externen Verbindung lesen und ändern. Hier ist wie:

```csharp
// Lesen Sie die erste externe Verbindung, bei der es sich um eine Datenbankverbindung handelt
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Zeigt den Datenbankverbindungsnamen, den Befehl und die Verbindungsinformationen an
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Ändern Sie den Namen der Verbindung
dbCon.Name = "NewCustomer";
```

## Schritt 4: Speichern Sie die ausgegebene Excel XLSB-Datei

Sobald Sie die erforderlichen Änderungen vorgenommen haben, können Sie die geänderte Excel XLSB-Datei im angegebenen Ausgabeverzeichnis speichern. So geht's:

```csharp
// Speichern Sie die ausgegebene Excel-XLSB-Datei
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Beispielquellcode für das Lesen und Schreiben einer externen Verbindung einer XLSB-Datei mit Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string sourceDir = RunExamples.Get_SourceDirectory();
//Ausgabe Verzeichnis
string outputDir = RunExamples.Get_OutputDirectory();
//Laden Sie die Excel-XLSB-Quelldatei
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Lesen Sie die erste externe Verbindung, die eigentlich eine DB-Verbindung ist
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Drucken Sie den Namen, den Befehl und die Verbindungsinformationen der DB-Verbindung aus
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Ändern Sie den Verbindungsnamen
dbCon.Name = "NewCust";
//Speichern Sie die Excel-XLSB-Datei
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Abschluss

Durch das Lesen und Schreiben externer Verbindungen in eine XLSB-Datei können Sie Daten aus externen Quellen in Ihren Excel-Arbeitsmappen bearbeiten. Mit Aspose.Cells für .NET können Sie problemlos auf externe Verbindungen zugreifen, Verbindungsinformationen lesen und ändern sowie Änderungen speichern. Experimentieren Sie mit Ihren eigenen XLSB-Dateien und nutzen Sie die Leistungsfähigkeit externer Verbindungen in Ihren Excel-Anwendungen.

### FAQs

#### F: Was ist eine externe Verbindung in einer XLSB-Datei?
    
A: Eine externe Verbindung in einer XLSB-Datei bezieht sich auf eine Verbindung, die mit einer externen Datenquelle wie einer Datenbank hergestellt wird. Es ermöglicht Ihnen, Daten aus dieser externen Quelle in die Excel-Arbeitsmappe zu importieren.

#### F: Kann ich in einer XLSB-Datei mehrere externe Verbindungen haben?
     
A: Ja, Sie können mehrere externe Verbindungen in einer XLSB-Datei haben. Sie können sie einzeln verwalten, indem Sie auf jedes Verbindungsobjekt zugreifen.

#### F: Wie kann ich mit Aspose.Cells die Details einer externen Verbindung in einer XLSB-Datei lesen?
     
A: Sie können die von Aspose.Cells bereitgestellte Funktionalität verwenden, um auf Eigenschaften einer externen Verbindung zuzugreifen, wie z. B. Verbindungsname, zugehöriger Befehl und Verbindungsinformationen.

#### F: Ist es möglich, eine externe Verbindung in einer XLSB-Datei mit Aspose.Cells zu ändern?
     
A: Ja, Sie können die Eigenschaften einer externen Verbindung, z. B. den Verbindungsnamen, ändern, um sie an Ihre spezifischen Anforderungen anzupassen. Aspose.Cells stellt Methoden zum Vornehmen dieser Änderungen bereit.

#### F: Wie kann ich mit Aspose.Cells an einer externen Verbindung vorgenommene Änderungen in einer XLSB-Datei speichern?
     
A: Sobald Sie die erforderlichen Änderungen an einer externen Verbindung vorgenommen haben, können Sie die geänderte Excel XLSB-Datei einfach mit der entsprechenden von Aspose.Cells bereitgestellten Methode speichern.