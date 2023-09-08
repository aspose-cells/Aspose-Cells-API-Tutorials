---
title: Weberweiterung hinzufügen
linktitle: Weberweiterung hinzufügen
second_title: Aspose.Cells für .NET API-Referenz
description: Fügen Sie mit Aspose.Cells für .NET ganz einfach eine Weberweiterung zu Ihren Excel-Arbeitsmappen hinzu.
type: docs
weight: 40
url: /de/net/excel-workbook/add-web-extension/
---
In diesem Schritt-für-Schritt-Tutorial erklären wir den bereitgestellten C#-Quellcode, der es Ihnen ermöglicht, eine Weberweiterung mit Aspose.Cells für .NET hinzuzufügen. Führen Sie die folgenden Schritte aus, um Ihrer Excel-Arbeitsmappe eine Weberweiterung hinzuzufügen.

## Schritt 1: Ausgabeverzeichnis festlegen

```csharp
// Ausgabe Verzeichnis
string outDir = RunExamples.Get_OutputDirectory();
```

In diesem ersten Schritt definieren wir das Ausgabeverzeichnis, in dem die geänderte Excel-Arbeitsmappe gespeichert wird.

## Schritt 2: Erstellen Sie eine neue Arbeitsmappe

```csharp
// Erstellen Sie eine neue Arbeitsmappe
Workbook workbook = new Workbook();
```

Hier erstellen wir eine neue Excel-Arbeitsmappe mit`Workbook` Klasse von Aspose.Cells.

## Schritt 3: Greifen Sie auf die Web Extensions Collection zu

```csharp
// Greifen Sie auf die Sammlung von Weberweiterungen zu
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 Wir greifen auf die Weberweiterungssammlung der Excel-Arbeitsmappe über zu`WebExtensions` Eigentum der`Worksheets` Objekt.

## Schritt 4: Fügen Sie eine neue Weberweiterung hinzu

```csharp
// Fügen Sie eine neue Weberweiterung hinzu
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

Wir fügen der Erweiterungssammlung eine neue Web-Erweiterung hinzu. Wir definieren die Referenz-ID, den Geschäftsnamen und den Geschäftstyp der Erweiterung.

## Schritt 5: Greifen Sie auf die Web Extension-Aufgabenbereichssammlung zu

```csharp
// Greifen Sie auf die Aufgabenbereichssammlung der Weberweiterung zu
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 Wir greifen auf die Aufgabenbereichssammlung der Excel-Arbeitsmappen-Weberweiterung über zu`WebExtensionTaskPanes` Eigentum der`Worksheets` Objekt.

## Schritt 6: Fügen Sie einen neuen Aufgabenbereich hinzu

```csharp
// Fügen Sie einen neuen Aufgabenbereich hinzu
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

Wir fügen der Aufgabenbereichssammlung einen neuen Aufgabenbereich hinzu. Wir legen die Sichtbarkeit des Bereichs, seinen Andockstatus und die zugehörige Weberweiterung fest.

## Schritt 7: Speichern und schließen Sie die Arbeitsmappe

```csharp
// Speichern und schließen Sie die Arbeitsmappe
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

Wir speichern die geänderte Arbeitsmappe im angegebenen Ausgabeverzeichnis und schließen sie dann.

### Beispielquellcode für das Hinzufügen einer Weberweiterung mit Aspose.Cells für .NET 
```csharp
//Quellverzeichnis
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## Abschluss

Herzlichen Glückwunsch! Sie haben jetzt gelernt, wie Sie mit Aspose.Cells für .NET eine Weberweiterung hinzufügen. Experimentieren Sie mit Code und erkunden Sie zusätzliche Funktionen von Aspose.Cells, um das Beste aus der Bearbeitung von Weberweiterungen in Ihren Excel-Arbeitsmappen herauszuholen.

## FAQs

#### F: Was ist eine Weberweiterung in einer Excel-Arbeitsmappe?

A: Eine Weberweiterung in einer Excel-Arbeitsmappe ist eine Komponente, die es Ihnen ermöglicht, durch die Integration von Webanwendungen zusätzliche Funktionen zu Excel hinzuzufügen. Es kann interaktive Funktionen, benutzerdefinierte Dashboards, externe Integrationen und mehr bieten.

#### F: Wie füge ich mit Aspose.Cells eine Weberweiterung zu einer Excel-Arbeitsmappe hinzu?

 A: Um mit Aspose.Cells eine Weberweiterung zu einer Excel-Arbeitsmappe hinzuzufügen, können Sie die Schritte in unserer Schritt-für-Schritt-Anleitung befolgen. Benutzen Sie die`WebExtensionCollection` Und`WebExtensionTaskPaneCollection` Klassen zum Hinzufügen und Konfigurieren der Weberweiterung und des zugehörigen Aufgabenbereichs.

#### F: Welche Informationen sind zum Hinzufügen einer Weberweiterung erforderlich?

A: Beim Hinzufügen einer Web-Erweiterung müssen Sie die SKU-ID der Erweiterung, den Shop-Namen und den Shop-Typ angeben. Diese Informationen helfen dabei, die Erweiterung korrekt zu identifizieren und zu laden.

#### F: Kann ich einer einzelnen Excel-Arbeitsmappe mehrere Weberweiterungen hinzufügen?

 A: Ja, Sie können einer einzelnen Excel-Arbeitsmappe mehrere Weberweiterungen hinzufügen. Benutzen Sie die`Add` Methode der Web-Erweiterungssammlung, um jede Erweiterung hinzuzufügen und sie dann den entsprechenden Aufgabenbereichen zuzuordnen.