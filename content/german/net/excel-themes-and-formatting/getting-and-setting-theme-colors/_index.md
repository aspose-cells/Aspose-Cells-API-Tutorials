---
title: Abrufen und Festlegen von Designfarben in Excel
linktitle: Abrufen und Festlegen von Designfarben in Excel
second_title: Aspose.Cells .NET Excel-Verarbeitungs-API
description: Erfahren Sie in diesem leicht verständlichen Tutorial, wie Sie mit Aspose.Cells für .NET Designfarben in Excel abrufen und festlegen. Vollständige Schritt-für-Schritt-Anleitung und Codebeispiele enthalten.
type: docs
weight: 11
url: /de/net/excel-themes-and-formatting/getting-and-setting-theme-colors/
---
## Einführung
Das Anpassen des Erscheinungsbilds einer Excel-Arbeitsmappe kann bei der Datenpräsentation einen großen Unterschied machen. Ein wichtiger Aspekt der Anpassung ist die Steuerung der Designfarben in Ihren Excel-Dateien. Wenn Sie mit .NET arbeiten, ist Aspose.Cells eine unglaublich leistungsstarke API, mit der Sie Excel-Dateien mühelos programmgesteuert bearbeiten können. In diesem Tutorial werden wir uns mit dem Abrufen und Festlegen von Designfarben in Excel mithilfe von Aspose.Cells für .NET befassen.
Klingt das kompliziert? Keine Sorge, ich kümmere mich darum! Wir werden es Schritt für Schritt durchgehen, sodass Sie am Ende dieser Anleitung die Farben ganz einfach anpassen können. Lassen Sie uns anfangen!
## Voraussetzungen
Bevor wir uns in den Code vertiefen, schauen wir uns an, was Sie benötigen, damit alles reibungslos läuft:
1. Aspose.Cells für .NET – Stellen Sie sicher, dass Sie die neueste Version installiert haben. Wenn Sie sie noch nicht haben, können Sie[Laden Sie es hier herunter](https://releases.aspose.com/cells/net/).
2. .NET-Entwicklungsumgebung – Sie können Visual Studio oder eine andere IDE Ihrer Wahl verwenden.
3. Grundkenntnisse in C# – Dies wird Ihnen helfen, den Codierungsbeispielen zu folgen.
4. Excel-Datei – Eine Beispiel-Excel-Datei, die Sie bearbeiten möchten.
 Sie erhalten auch eine[vorläufige Lizenz](https://purchase.aspose.com/temporary-license/) um die volle Funktionalität von Aspose.Cells kostenlos zu erkunden, bevor Sie sich festlegen.
## Namespaces importieren
Stellen Sie zunächst sicher, dass Sie die erforderlichen Namespaces in Ihr Projekt importieren. Dadurch können Sie auf alle Klassen und Methoden zugreifen, die Sie zum Bearbeiten der Excel-Designfarben benötigen.
```csharp
using System.IO;
using Aspose.Cells;
using System.Drawing;
using System;
```
Lassen Sie uns nun in den eigentlichen Prozess des Abrufens und Festlegens von Designfarben in Ihrer Excel-Arbeitsmappe eintauchen. Ich werde den Code zum besseren Verständnis in einfache Schritte aufteilen.
## Schritt 1: Laden Sie Ihre Excel-Datei
Als Erstes müssen Sie die Excel-Datei laden, die Sie ändern möchten. Wir verwenden die Klasse Workbook, um eine vorhandene Excel-Datei zu öffnen.
Sie initialisieren ein neues Arbeitsmappenobjekt und laden Ihre Excel-Datei hinein. Dadurch können Sie Änderungen an der Arbeitsmappe vornehmen.
```csharp
// Der Pfad zum Dokumentverzeichnis.
string dataDir = "Your Document Directory";
// Instanziieren Sie das Workbook-Objekt, um eine vorhandene Excel-Datei zu öffnen.
Workbook workbook = new Workbook(dataDir + "book1.xlsx");
```
Hier beginnt die Magie! Wir haben jetzt die Datei geöffnet und können mit der Anpassung der Designfarben beginnen.
## Schritt 2: Aktuelle Designfarben abrufen
Bevor wir Farben ändern, überprüfen wir zunächst die aktuellen Designfarben. In diesem Beispiel konzentrieren wir uns auf Hintergrund1 und Akzent2.
Sie verwenden die Methode GetThemeColor, um die aktuelle Designfarbe für Hintergrund1 und Akzent2 abzurufen.
```csharp
// Holen Sie sich die Designfarbe „Hintergrund1“.
Color c = workbook.GetThemeColor(ThemeColorType.Background1);
// Drucken Sie die Farbe.
Console.WriteLine("Theme color Background1: " + c);
// Holen Sie sich die Themenfarbe Accent2.
c = workbook.GetThemeColor(ThemeColorType.Accent2);
// Drucken Sie die Farbe.
Console.WriteLine("Theme color Accent2: " + c);
```
Wenn Sie dies ausführen, werden die aktuell im Design verwendeten Farben gedruckt. Dies ist nützlich, wenn Sie die Standardeinstellungen kennen möchten, bevor Sie Änderungen vornehmen.
## Schritt 3: Neue Designfarben festlegen
Jetzt kommt der lustige Teil! Wir ändern die Farben für Hintergrund1 und Akzent2. Ändern wir Hintergrund1 in Rot und Akzent2 in Blau. Dies verleiht der Arbeitsmappe ein neues, auffälliges Aussehen!
Sie verwenden die Methode SetThemeColor, um die Designfarben für Hintergrund1 und Akzent2 zu ändern.
```csharp
// Ändern Sie die Designfarbe von Hintergrund1 in Rot.
workbook.SetThemeColor(ThemeColorType.Background1, Color.Red);
// Ändern Sie die Designfarbe von Accent2 in Blau.
workbook.SetThemeColor(ThemeColorType.Accent2, Color.Blue);
```
Sehen Sie, was wir da gemacht haben? Wir haben einfach die gewünschte Farbe eingegeben und zack! Die Designfarben haben sich jetzt geändert. Aber warten Sie, woher wissen wir, ob es funktioniert hat? Das kommt als Nächstes.
## Schritt 4: Überprüfen der Änderungen
Wir wollen nicht einfach davon ausgehen, dass die Änderungen vorgenommen wurden. Lassen Sie uns die neuen Farben überprüfen, indem wir sie erneut abrufen und ausdrucken.
Sie rufen die aktualisierten Designfarben erneut mit der Methode GetThemeColor ab, um zu bestätigen, dass die Änderungen angewendet wurden.
```csharp
// Holen Sie sich die aktualisierte Designfarbe „Hintergrund1“.
c = workbook.GetThemeColor(ThemeColorType.Background1);
// Drucken Sie die aktualisierte Farbe zur Bestätigung.
Console.WriteLine("Theme color Background1 changed to: " + c);
// Holen Sie sich die aktualisierte Accent2-Designfarbe.
c = workbook.GetThemeColor(ThemeColorType.Accent2);
// Drucken Sie die aktualisierte Farbe zur Bestätigung.
Console.WriteLine("Theme color Accent2 changed to: " + c);
```
Auf diese Weise können Sie sicher sein, dass Ihre Änderungen wie erwartet funktionieren. Sobald Sie überprüft haben, dass alles in Ordnung ist, können wir mit dem letzten Schritt fortfahren.
## Schritt 5: Speichern Sie die geänderte Excel-Datei
Vergessen Sie nach all diesen spannenden Änderungen nicht, Ihre Arbeit zu speichern! Dieser Schritt stellt sicher, dass die aktualisierten Designfarben auf Ihre Excel-Datei angewendet werden.
Sie verwenden die Methode „Speichern“, um die Arbeitsmappe mit den von Ihnen vorgenommenen Änderungen zu speichern.
```csharp
// Speichern Sie die aktualisierte Datei.
workbook.Save(dataDir + "output.out.xlsx");
```
Und das war’s! Sie haben gerade erfolgreich die Designfarben Ihrer Excel-Datei mit Aspose.Cells für .NET geändert. High Five!
## Abschluss
Das Ändern der Designfarben in einer Excel-Datei mit Aspose.Cells für .NET ist unkompliziert, wenn Sie den Dreh erst einmal raus haben. Mit nur wenigen Codezeilen können Sie das Erscheinungsbild Ihrer Arbeitsmappe vollständig ändern und ihr ein individuelles und professionelles Aussehen verleihen. Egal, ob Sie Ihre Tabellenkalkulation an das Branding Ihres Unternehmens anpassen oder einfach nur aufpeppen möchten, Aspose.Cells bietet die Tools dafür.
## Häufig gestellte Fragen
### Kann ich neben den vordefinierten Designfarben auch benutzerdefinierte Farben festlegen?
Ja, mit Aspose.Cells können Sie für jeden Teil Ihrer Excel-Arbeitsmappe benutzerdefinierte Farben festlegen, nicht nur die vordefinierten Designfarben.
### Benötige ich eine kostenpflichtige Lizenz, um Aspose.Cells zu verwenden?
 Sie können beginnen mit einem[Kostenlose Testversion](https://releases.aspose.com/)oder erhalten Sie eine[vorläufige Lizenz](https://purchase.aspose.com/temporary-license/). Um die volle Funktionalität freizuschalten, wird eine kostenpflichtige Lizenz empfohlen.
### Kann ich auf einzelne Blätter unterschiedliche Designfarben anwenden?
Ja, Sie können die Designfarben einzelner Blätter in der Arbeitsmappe bearbeiten, indem Sie sie separat laden und die gewünschten Farben anwenden.
### Ist es möglich, zu den ursprünglichen Designfarben zurückzukehren?
Ja, wenn Sie zu den Standarddesignfarben zurückkehren möchten, können Sie diese mit denselben Methoden GetThemeColor und SetThemeColor abrufen und zurücksetzen.
### Kann ich diesen Vorgang für mehrere Arbeitsmappen automatisieren?
Auf jeden Fall! Mit Aspose.Cells können Sie Designänderungen programmgesteuert in einem Stapelprozess auf mehrere Arbeitsmappen anwenden.