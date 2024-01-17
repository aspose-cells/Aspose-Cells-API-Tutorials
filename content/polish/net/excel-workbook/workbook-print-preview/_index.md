---
title: Podgląd wydruku skoroszytu
linktitle: Podgląd wydruku skoroszytu
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak wygenerować podgląd wydruku skoroszytu za pomocą Aspose.Cells dla .NET.
type: docs
weight: 170
url: /pl/net/excel-workbook/workbook-print-preview/
---
Podgląd wydruku skoroszytu jest niezbędną funkcją podczas pracy z plikami Excel za pomocą Aspose.Cells dla .NET. Możesz łatwo wygenerować podgląd wydruku, wykonując następujące kroki:

## Krok 1: Określ katalog źródłowy

Najpierw musisz określić katalog źródłowy, w którym znajduje się plik Excel, którego podgląd chcesz wyświetlić. Oto jak to zrobić:

```csharp
// katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Krok 2: Załaduj skoroszyt

Następnie musisz załadować skoroszyt skoroszytu z określonego pliku Excel. Oto jak to zrobić:

```csharp
// Załaduj skoroszyt skoroszytu
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Krok 3: Skonfiguruj opcje obrazu i drukowania

Przed wygenerowaniem podglądu wydruku możesz odpowiednio skonfigurować obraz i opcje drukowania. W tym przykładzie używamy opcji domyślnych. Oto jak to zrobić:

```csharp
// Opcje obrazu i druku
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Krok 4: Wygeneruj podgląd wydruku skoroszytu

Teraz możesz wygenerować podgląd wydruku skoroszytu Workbook przy użyciu klasy WorkbookPrintingPreview. Oto jak to zrobić:

```csharp
// Podgląd wydruku skoroszytu
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Krok 5: Wygeneruj podgląd wydruku arkusza

Jeśli chcesz wygenerować podgląd wydruku konkretnego arkusza, możesz skorzystać z klasy SheetPrintingPreview. Oto przykład :

```csharp
// Podgląd wydruku arkusza
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Przykładowy kod źródłowy dla podglądu wydruku skoroszytu przy użyciu Aspose.Cells dla .NET 
```csharp
//Katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Wniosek

Generowanie podglądu wydruku skoroszytu to zaawansowana funkcja oferowana przez Aspose.Cells dla .NET. Wykonując powyższe kroki, możesz łatwo wyświetlić podgląd skoroszytu programu Excel i uzyskać informacje o liczbie stron do wydrukowania.

### Często zadawane pytania

#### P: Jak mogę określić inny katalog źródłowy do załadowania skoroszytu?
    
 Odp.: Możesz użyć`Set_SourceDirectory` metoda określenia innego katalogu źródłowego. Na przykład:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### P: Czy mogę dostosować opcje obrazu i wydruku podczas generowania podglądu wydruku?
    
 O: Tak, możesz dostosować opcje obrazu i drukowania, zmieniając właściwości pliku`ImageOrPrintOptions` obiekt. Można na przykład ustawić rozdzielczość obrazu, format pliku wyjściowego itp.

#### P: Czy można wygenerować podgląd wydruku dla wielu arkuszy w skoroszycie?
    
Odp.: Tak, możesz przeglądać różne arkusze w skoroszycie i generować podgląd wydruku dla każdego arkusza za pomocą`SheetPrintingPreview` klasa.

#### P: Jak zapisać podgląd wydruku jako obraz lub plik PDF?
    
 Odp.: możesz użyć`ToImage` Lub`ToPdf` metoda`WorkbookPrintingPreview` Lub`SheetPrintingPreview` obiekt, aby zapisać podgląd wydruku jako obraz lub plik PDF.

#### P: Co mogę zrobić z wygenerowanym podglądem wydruku?
    
O: Po wygenerowaniu podglądu wydruku możesz go wyświetlić na ekranie, zapisać jako obraz lub plik PDF albo użyć go do innych operacji, takich jak wysłanie pocztą e-mail lub wydruk.
	