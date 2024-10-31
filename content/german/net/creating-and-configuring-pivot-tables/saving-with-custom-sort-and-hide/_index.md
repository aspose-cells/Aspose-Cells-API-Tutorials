---
title: Speichern von Pivot-Tabellen mit benutzerdefiniertem Sortieren und Ausblenden in .NET
linktitle: Speichern von Pivot-Tabellen mit benutzerdefiniertem Sortieren und Ausblenden in .NET
second_title: Aspose.Cells .NET Excel-Verarbeitungs-API
description: Erfahren Sie, wie Sie Pivot-Tabellen mit benutzerdefinierter Sortierung und Ausblenden von Zeilen mithilfe von Aspose.Cells für .NET speichern. Schritt-für-Schritt-Anleitung mit praktischen Beispielen.
type: docs
weight: 26
url: /de/net/creating-and-configuring-pivot-tables/saving-with-custom-sort-and-hide/
---
## Einführung
In der Welt der Datenanalyse sind Pivot-Tabellen eines der leistungsstärksten Tools zum Zusammenfassen, Analysieren und Präsentieren von Daten in einem verständlichen Format. Wenn Sie mit .NET arbeiten und nach einer einfachen Möglichkeit suchen, Pivot-Tabellen zu bearbeiten – insbesondere, um sie mit benutzerdefinierter Sortierung und Ausblenden bestimmter Zeilen zu speichern –, sind Sie hier richtig! Heute werden wir die Technik zum Speichern von Pivot-Tabellen mit Aspose.Cells für .NET erläutern. Dieser Leitfaden führt Sie durch alles von den Voraussetzungen bis hin zu praktischen Beispielen und stellt sicher, dass Sie in der Lage sind, ähnliche Aufgaben selbst zu bewältigen. Also, legen wir gleich los!
## Voraussetzungen
Bevor Sie sich in die Details der Codierung stürzen, stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:
1. Visual Studio: Idealerweise möchten Sie eine solide IDE zur Abwicklung Ihrer .NET-Projekte. Visual Studio ist eine gute Wahl.
2.  Aspose.Cells für .NET: Sie benötigen Zugriff auf die Aspose-Bibliothek, um Excel-Dateien programmgesteuert verwalten zu können. Sie können[Laden Sie Aspose.Cells für .NET hier herunter](https://releases.aspose.com/cells/net/).
3. Grundkenntnisse in C#: Die Vertrautheit mit den grundlegenden Programmierkonzepten und der Syntax in C# erleichtert den Prozess.
4.  Beispiel-Excel-Datei: Wir verwenden eine Beispieldatei namens`PivotTableHideAndSortSample.xlsx`. Stellen Sie sicher, dass Sie diese Datei in Ihrem angegebenen Dokumentverzeichnis haben.
Sobald Sie Ihre Entwicklungsumgebung eingerichtet und Ihre Beispieldatei bereit haben, können Sie loslegen!
## Pakete importieren
Nachdem wir nun die Voraussetzungen abgehakt haben, importieren wir die erforderlichen Pakete. Verwenden Sie in Ihrer C#-Datei die folgende Anweisung, um Aspose.Cells einzubinden:
```csharp
using System;
using Aspose.Cells.Pivot;
```
Mit dieser Anweisung können Sie auf die Klassen und Methoden zugreifen, die von der Aspose.Cells-Bibliothek bereitgestellt werden. Stellen Sie sicher, dass Sie die Aspose.Cells.dll zu Ihren Projektreferenzen hinzugefügt haben.
## Schritt 1: Einrichten der Arbeitsmappe
Als erstes müssen wir unsere Arbeitsmappe laden. Dies geschieht mit dem folgenden Codeausschnitt:
```csharp
// Verzeichnisse für Quell- und Ausgabedateien
string sourceDir = "Your Document Directory";
string outputDir = "Your Document Directory";
// Laden der Arbeitsmappe
Workbook workbook = new Workbook(sourceDir + "PivotTableHideAndSortSample.xlsx");
```
 In diesem Schritt definieren Sie die Verzeichnisse, in denen Ihre Quell- und Ausgabedateien gespeichert werden.`Workbook`Der Konstruktor lädt Ihre vorhandene Excel-Datei und macht sie zur Bearbeitung bereit.
## Schritt 2: Zugriff auf das Arbeitsblatt und die Pivot-Tabelle
Greifen wir nun auf das spezifische Arbeitsblatt in der Arbeitsmappe zu und wählen die Pivot-Tabelle aus, mit der wir arbeiten möchten.
```csharp
// Greifen Sie auf das erste Arbeitsblatt zu
Worksheet worksheet = workbook.Worksheets[0];
// Greifen Sie auf die erste Pivot-Tabelle im Arbeitsblatt zu
var pivotTable = worksheet.PivotTables[0];
```
 In diesem Snippet`Worksheets[0]` wählt das erste Blatt in Ihrem Excel-Dokument aus und`PivotTables[0]` ruft die erste Pivot-Tabelle ab. So können Sie gezielt die Pivot-Tabelle auswählen, die Sie ändern möchten.
## Schritt 3: PivotTable-Zeilen sortieren
Als Nächstes implementieren wir eine benutzerdefinierte Sortierung, um unsere Daten zu organisieren. Insbesondere sortieren wir die Ergebnisse in absteigender Reihenfolge.
```csharp
// Sortieren des ersten Zeilenfelds in absteigender Reihenfolge
PivotField field = pivotTable.RowFields[0];
field.IsAutoSort = true;
field.IsAscendSort = false;  // false für absteigend
field.AutoSortField = 0;     // Sortieren basierend auf der ersten Spalte
```
 Hier verwenden wir die`PivotField` um die Sortierparameter festzulegen. Dadurch wird die Pivot-Tabelle angewiesen, das angegebene Zeilenfeld basierend auf der ersten Spalte zu sortieren und dies in absteigender Reihenfolge zu tun. 
## Schritt 4: Daten aktualisieren und berechnen
Nach dem Anwenden der Sortierung ist es wichtig, die Daten der Pivot-Tabelle zu aktualisieren, um sicherzustellen, dass sie unsere Änderungen widerspiegeln.
```csharp
// Aktualisieren und Berechnen der PivotTable-Daten
pivotTable.RefreshData();
pivotTable.CalculateData();
```
Dieser Schritt synchronisiert die Pivot-Tabelle mit Ihren aktuellen Daten und wendet alle Sortier- oder Filteränderungen an, die Sie bisher vorgenommen haben. Stellen Sie es sich so vor, als würden Sie auf „Aktualisieren“ klicken, um die neue Organisation Ihrer Daten anzuzeigen!
## Schritt 5: Bestimmte Zeilen ausblenden
Lassen Sie uns nun die Zeilen ausblenden, die Werte unter einem bestimmten Schwellenwert enthalten, beispielsweise weniger als 60. Hier können wir die Daten noch weiter filtern.
```csharp
// Festlegen der Startzeile für die Punkteabfrage
int currentRow = 3;
int rowsUsed = pivotTable.DataBodyRange.EndRow;
// Zeilen mit einer Punktzahl unter 60 ausblenden
while (currentRow < rowsUsed)
{
    Cell cell = worksheet.Cells[currentRow, 1]; // Vorausgesetzt, die Punktzahl steht in der ersten Spalte
    double score = Convert.ToDouble(cell.Value);
    if (score < 60)
    {
        worksheet.Cells.HideRow(currentRow);  // Zeile ausblenden, wenn die Punktzahl unter 60 liegt
    }
    currentRow++;
}
```
In dieser Schleife überprüfen wir jede Zeile im Datenbereich der Pivot-Tabelle. Wenn ein Wert unter 60 liegt, wird die Zeile ausgeblendet. Das ist, als würden Sie Ihren Arbeitsbereich aufräumen – Sie entfernen das Durcheinander, das Ihnen nicht hilft, das Gesamtbild zu sehen!
## Schritt 6: Abschließendes Aktualisieren und Speichern der Arbeitsmappe
Bevor wir zum Abschluss kommen, aktualisieren wir die Pivot-Tabelle ein letztes Mal, um sicherzustellen, dass das Ausblenden der Zeilen wirksam wird. Anschließend speichern wir die Arbeitsmappe in einer neuen Datei.
```csharp
// Daten ein letztes Mal aktualisieren und berechnen
pivotTable.RefreshData();
pivotTable.CalculateData();
// Speichern der geänderten Arbeitsmappe
workbook.Save(outputDir + "PivotTableHideAndSort_out.xlsx");
```
Durch diese letzte Aktualisierung wird sichergestellt, dass alles auf dem neuesten Stand ist. Durch das Speichern der Arbeitsmappe erstellen Sie eine neue Datei, die alle von uns vorgenommenen Änderungen widerspiegelt.
## Schritt 7: Erfolg bestätigen
Abschließend drucken wir eine Erfolgsmeldung aus, um zu bestätigen, dass unser Vorgang reibungslos abgeschlossen wurde.
```csharp
Console.WriteLine("PivotTableSortAndHide executed successfully.");
```
Diese Zeile dient sowohl der Erfolgsbestätigung als auch der Bereitstellung von Feedback in Ihrer Konsole, wodurch der Vorgang etwas interaktiver und benutzerfreundlicher wird.
## Abschluss
Und da haben Sie es! Sie haben erfolgreich gelernt, wie Sie Pivot-Tabellen mit benutzerdefinierten Sortier- und Ausblendfunktionen mithilfe von Aspose.Cells für .NET speichern. Vom Laden Ihrer Arbeitsmappe über das Sortieren von Daten bis hin zum Ausblenden unnötiger Details bieten diese Schritte einen strukturierten Ansatz zur programmgesteuerten Verwaltung Ihrer Pivot-Tabellen. Egal, ob Sie Verkaufsdaten analysieren, die Teamleistung verfolgen oder einfach Informationen organisieren, das Erlernen dieser Fähigkeiten mit Aspose.Cells kann Ihnen wertvolle Zeit sparen und Ihren Datenanalyse-Workflow verbessern.
## Häufig gestellte Fragen
### Was ist Aspose.Cells für .NET?
Aspose.Cells für .NET ist eine .NET-Bibliothek, mit der Entwickler Excel-Tabellen erstellen, bearbeiten und konvertieren können, ohne auf Microsoft Excel angewiesen zu sein. Sie eignet sich perfekt zum Automatisieren von Aufgaben in Excel-Dokumenten.
### Kann ich Aspose.Cells verwenden, ohne dass Microsoft Office installiert ist?
Auf jeden Fall! Aspose.Cells ist eine eigenständige Bibliothek, sodass Sie Microsoft Office nicht auf Ihrem System installieren müssen, um mit Excel-Dateien arbeiten zu können.
### Wie kann ich eine temporäre Lizenz für Aspose.Cells erhalten?
 Sie können eine vorläufige Lizenz beantragen über das[Seite mit der temporären Lizenz](https://purchase.aspose.com/temporary-license/).
### Wo finde ich Unterstützung bei Aspose.Cells-Problemen?
 Bei Fragen oder Problemen können Sie die[Aspose-Forum](https://forum.aspose.com/c/cells/9), wo Sie Unterstützung von der Community und dem Aspose-Team finden.
### Gibt es eine kostenlose Testversion für Aspose.Cells?
 Ja! Sie können eine kostenlose Testversion von Aspose.Cells herunterladen, um die Funktionen vor dem Kauf zu testen. Besuchen Sie die[Seite zur kostenlosen Testversion](https://releases.aspose.com/) um loszulegen.