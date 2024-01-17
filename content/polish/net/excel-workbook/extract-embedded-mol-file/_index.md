---
title: Wyodrębnij osadzony plik Mol
linktitle: Wyodrębnij osadzony plik Mol
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak łatwo wyodrębnić osadzone pliki MOL ze skoroszytu programu Excel za pomocą Aspose.Cells dla .NET.
type: docs
weight: 90
url: /pl/net/excel-workbook/extract-embedded-mol-file/
---
W tym samouczku przeprowadzimy Cię krok po kroku przez proces wyodrębniania osadzonego pliku MOL ze skoroszytu programu Excel przy użyciu biblioteki Aspose.Cells dla platformy .NET. Dowiesz się, jak przeglądać arkusze skoroszytu, wyodrębniać odpowiednie obiekty OLE i zapisywać wyodrębnione pliki MOL. Aby pomyślnie ukończyć to zadanie, wykonaj poniższe czynności.

## Krok 1: Zdefiniuj katalogi źródłowe i wyjściowe
Najpierw musimy zdefiniować katalogi źródłowe i wyjściowe w naszym kodzie. Katalogi te wskazują, gdzie znajduje się źródłowy skoroszyt programu Excel i gdzie zostaną zapisane wyodrębnione pliki MOL. Oto odpowiedni kod:

```csharp
// Katalogi
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

W razie potrzeby pamiętaj o określeniu odpowiednich ścieżek.

## Krok 2: Ładowanie skoroszytu programu Excel
Następnym krokiem jest załadowanie skoroszytu programu Excel zawierającego osadzone obiekty OLE i pliki MOL. Oto kod ładujący skoroszyt:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Upewnij się, że nazwa pliku źródłowego została poprawnie określona w kodzie.

## Krok 3: Przejdź przez arkusze i wyodrębnij pliki MOL
Teraz przejdziemy przez każdy arkusz skoroszytu i wyodrębnimy odpowiednie obiekty OLE, które zawierają pliki MOL. Oto odpowiedni kod:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Ten kod przechodzi przez każdy arkusz skoroszytu, pobiera obiekty OLE i zapisuje wyodrębnione pliki MOL w katalogu wyjściowym.

### Przykładowy kod źródłowy dla ekstraktu osadzonego pliku Mol przy użyciu Aspose.Cells dla .NET 
```csharp
//katalogi
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Wniosek
Gratulacje! Nauczyłeś się, jak wyodrębnić osadzony plik MOL ze skoroszytu programu Excel przy użyciu Aspose.Cells dla .NET. Możesz teraz zastosować tę wiedzę do wyodrębnienia plików MOL z własnych skoroszytów programu Excel. Zachęcamy do dalszego eksplorowania biblioteki Aspose.Cells i poznania jej innych zaawansowanych funkcji.

### Często zadawane pytania

#### P: Co to jest plik MOL?
 
Odp.: Plik MOL to format pliku używany do reprezentowania struktur chemicznych w chemii obliczeniowej. Zawiera informacje o atomach, wiązaniach i innych właściwościach molekularnych.

#### P: Czy ta metoda działa ze wszystkimi typami plików Excel?

Odp.: Tak, ta metoda działa ze wszystkimi typami plików Excel obsługiwanymi przez Aspose.Cells.

#### P: Czy mogę wyodrębnić wiele plików MOL jednocześnie?

Odp.: Tak, możesz wyodrębnić wiele plików MOL jednocześnie, iterując po obiektach OLE na każdym arkuszu skoroszytu.