---
title: Einen Kommentar mit Bild in Excel hinzufügen
linktitle: Einen Kommentar mit Bild in Excel hinzufügen
second_title: Aspose.Cells .NET Excel-Verarbeitungs-API
description: Erfahren Sie, wie Sie mit Aspose.Cells für .NET Kommentare mit Bildern in Excel hinzufügen. Verbessern Sie Ihre Tabellen mit personalisierten Anmerkungen.
type: docs
weight: 10
url: /de/net/excel-comment-annotation/add-comment-with-image-excel/
---
## Einführung
Excel ist ein leistungsstarkes Tool für die Datenverwaltung und -analyse, aber manchmal müssen Sie Ihren Tabellenkalkulationen eine persönliche Note verleihen, oder? Vielleicht möchten Sie Daten mit Anmerkungen versehen, Feedback geben oder sogar mit Bildern etwas Flair verleihen. Hier kommen Kommentare ins Spiel! In diesem Tutorial erfahren Sie, wie Sie mithilfe der Aspose.Cells-Bibliothek für .NET einen Kommentar mit einem Bild in Excel hinzufügen. Dieser Ansatz kann besonders nützlich sein, um interaktivere und optisch ansprechendere Tabellenkalkulationen zu erstellen.
## Voraussetzungen
Bevor wir uns mit den Einzelheiten des Hinzufügens von Kommentaren mit Bildern in Excel befassen, stellen wir sicher, dass Sie alles haben, was Sie für den Einstieg benötigen:
1. Visual Studio: Stellen Sie sicher, dass Visual Studio auf Ihrem Computer installiert ist. Hier schreiben und führen Sie Ihren Code aus.
2.  Aspose.Cells für .NET: Sie benötigen die Aspose.Cells-Bibliothek. Wenn Sie sie noch nicht installiert haben, können Sie sie hier herunterladen:[Hier](https://releases.aspose.com/cells/net/).
3. Grundkenntnisse in C#: Wenn Sie mit der C#-Programmierung vertraut sind, verstehen Sie die Codeausschnitte besser.
4. Eine Bilddatei: Halten Sie eine Bilddatei (z. B. ein Logo) bereit, die Sie in Ihren Excel-Kommentar einbetten möchten. Für dieses Tutorial gehen wir davon aus, dass Sie eine Datei mit dem Namen`logo.jpg`.
5. .NET Framework: Stellen Sie sicher, dass Sie das .NET Framework installiert haben, da Aspose.Cells es für die ordnungsgemäße Funktion benötigt.
Nachdem wir nun unsere Voraussetzungen abgedeckt haben, können wir mit der eigentlichen Codierung fortfahren!
## Pakete importieren
Als Erstes müssen wir die erforderlichen Pakete importieren. Stellen Sie in Ihrem C#-Projekt sicher, dass Sie einen Verweis auf die Aspose.Cells-Bibliothek hinzufügen. Sie können dies mithilfe des NuGet-Paket-Managers in Visual Studio tun. So geht's:
1. Öffnen Sie Visual Studio.
2. Erstellen Sie ein neues Projekt oder öffnen Sie ein vorhandenes.
3. Klicken Sie im Projektmappen-Explorer mit der rechten Maustaste auf Ihr Projekt.
4. Wählen Sie „NuGet-Pakete verwalten“ aus.
5. Suchen Sie nach Aspose.Cells und installieren Sie es.

```csharp
using System.IO;
using Aspose.Cells;
using System.Drawing;
```

Sobald Sie die Bibliothek installiert haben, können Sie mit dem Schreiben Ihres Codes beginnen. Hier erfahren Sie Schritt für Schritt, wie Sie dabei vorgehen.
## Schritt 1: Richten Sie Ihr Dokumentverzeichnis ein
Zu Beginn müssen wir ein Verzeichnis einrichten, in dem wir unsere Excel-Dateien speichern können. Dies ist ein entscheidender Schritt, da wir unsere Arbeit organisiert halten möchten.
```csharp
// Der Pfad zum Dokumentverzeichnis.
string dataDir = "Your Document Directory";
//Erstellen Sie ein Verzeichnis, falls es noch nicht vorhanden ist.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
-  dataDir: Diese Variable enthält den Pfad zu Ihrem Dokumentenverzeichnis. Ersetzen Sie`"Your Document Directory"` durch den tatsächlichen Pfad, in dem Sie Ihre Excel-Datei speichern möchten.
- Directory.Exists: Dies prüft, ob das Verzeichnis bereits existiert.
- Directory.CreateDirectory: Wenn das Verzeichnis nicht existiert, wird es erstellt.
## Schritt 2: Instanziieren einer Arbeitsmappe
 Als nächstes müssen wir eine Instanz des`Workbook` Klasse. Diese Klasse stellt eine Excel-Arbeitsmappe im Speicher dar.
```csharp
//Instanziieren einer Arbeitsmappe
Workbook workbook = new Workbook();
```
- Arbeitsmappe: Dies ist die Hauptklasse in Aspose.Cells, mit der Sie Excel-Dateien erstellen und bearbeiten können. Indem Sie sie instanziieren, erstellen Sie im Wesentlichen eine neue Excel-Arbeitsmappe.
## Schritt 3: Holen Sie sich die Kommentarsammlung
Nachdem wir nun unsere Arbeitsmappe haben, greifen wir auf die Kommentarsammlung des ersten Arbeitsblatts zu.
```csharp
// Erhalten Sie mit dem ersten Blatt eine Referenz der Kommentarsammlung
CommentCollection comments = workbook.Worksheets[0].Comments;
```
- Arbeitsblätter[ 0]: Dies greift auf das erste Arbeitsblatt in der Arbeitsmappe zu. Denken Sie daran, dass der Index nullbasiert ist, also`[0]` bezieht sich auf das erste Blatt.
- Kommentare: Diese Eigenschaft gibt uns Zugriff auf die Kommentarsammlung in diesem Arbeitsblatt.
## Schritt 4: Einen Kommentar zu einer Zelle hinzufügen
Fügen wir einer bestimmten Zelle einen Kommentar hinzu. In diesem Fall fügen wir der Zelle A1 einen Kommentar hinzu.
```csharp
// Einen Kommentar zur Zelle A1 hinzufügen
int commentIndex = comments.Add(0, 0);
Comment comment = comments[commentIndex];
comment.Note = "First note.";
comment.Font.Name = "Times New Roman";
```
- comments.Add(0, 0): Diese Methode fügt der Zelle A1 (Zeile 0, Spalte 0) einen Kommentar hinzu.
- Kommentar.Hinweis: Hier legen wir den Text des Kommentars fest.
- comment.Font.Name: Hiermit wird die Schriftart des Kommentartextes festgelegt.
## Schritt 5: Laden Sie ein Bild in einen Stream
 Jetzt ist es an der Zeit, das Bild zu laden, das wir in unseren Kommentar einbetten möchten. Wir verwenden ein`MemoryStream` um die Bilddaten zu speichern.
```csharp
// Laden Sie ein Bild in den Stream
Bitmap bmp = new Bitmap(dataDir + "logo.jpg");
MemoryStream ms = new MemoryStream();
bmp.Save(ms, System.Drawing.Imaging.ImageFormat.Png);
```
- Bitmap: Diese Klasse wird zum Laden der Bilddatei verwendet. Stellen Sie sicher, dass der Pfad korrekt ist.
- MemoryStream: Dies ist ein Stream, den wir verwenden, um das Bild im Speicher zu speichern.
- bmp.Save: Dies speichert das Bitmap-Bild im PNG-Format im Speicherstream.
## Schritt 6: Bilddaten auf Kommentarform setzen
Jetzt müssen wir die Bilddaten auf die Form einstellen, die mit dem zuvor erstellten Kommentar verknüpft ist.
```csharp
// Stellen Sie die Bilddaten auf die mit dem Kommentar verknüpfte Form ein
comment.CommentShape.Fill.ImageData = ms.ToArray();
```
-  comment.CommentShape.Fill.ImageData: Mit dieser Eigenschaft können Sie das Bild für die Kommentarform festlegen. Wir konvertieren das`MemoryStream` in ein Byte-Array mit`ms.ToArray()`.
## Schritt 7: Speichern Sie die Arbeitsmappe
Zum Schluss speichern wir unsere Arbeitsmappe mit dem Kommentar und dem Bild.
```csharp
// Speichern der Arbeitsmappe
workbook.Save(dataDir + "book1.out.xlsx", Aspose.Cells.SaveFormat.Xlsx);
```
- workbook.Save: Diese Methode speichert die Arbeitsmappe im angegebenen Pfad. Wir speichern sie als XLSX-Datei.
## Abschluss
Und da haben Sie es! Sie haben mithilfe von Aspose.Cells für .NET erfolgreich einen Kommentar mit einem Bild zu einer Excel-Datei hinzugefügt. Mit dieser Funktion können Sie Ihre Tabellen informativer und optisch ansprechender gestalten. Egal, ob Sie Daten kommentieren, Feedback geben oder einfach eine persönliche Note hinzufügen möchten, Kommentare mit Bildern können das Benutzererlebnis erheblich verbessern.
## Häufig gestellte Fragen
### Kann ich derselben Zelle mehrere Kommentare hinzufügen?
Nein, Excel erlaubt nicht mehrere Kommentare in derselben Zelle. Sie können nur einen Kommentar pro Zelle haben.
### Welche Bildformate werden unterstützt?
Aspose.Cells unterstützt verschiedene Bildformate, darunter PNG, JPEG und BMP.
### Benötige ich eine Lizenz, um Aspose.Cells zu verwenden?
Aspose.Cells bietet eine kostenlose Testversion an, für die volle Funktionalität müssen Sie jedoch eine Lizenz erwerben.
### Kann ich das Erscheinungsbild des Kommentars anpassen?
Ja, Sie können Schriftart, Größe und Farbe des Kommentartextes anpassen und auch Form und Größe des Kommentars selbst ändern.
### Wo finde ich weitere Dokumentation zu Aspose.Cells?
 Eine ausführliche Dokumentation finden Sie auf Aspose.Cells[Hier](https://reference.aspose.com/cells/net/).