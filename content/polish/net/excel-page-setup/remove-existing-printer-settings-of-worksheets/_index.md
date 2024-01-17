---
title: Usuń istniejące ustawienia drukarki z arkuszy kalkulacyjnych
linktitle: Usuń istniejące ustawienia drukarki z arkuszy kalkulacyjnych
second_title: Aspose.Cells dla .NET API odniesienia
description: Dowiedz się, jak usunąć istniejące ustawienia drukarki z arkuszy kalkulacyjnych Excel za pomocą Aspose.Cells dla .NET.
type: docs
weight: 80
url: /pl/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
W tym samouczku przeprowadzimy Cię krok po kroku, jak usunąć istniejące ustawienia drukarki z arkuszy kalkulacyjnych w programie Excel za pomocą Aspose.Cells dla .NET. Do zilustrowania procesu użyjemy kodu źródłowego C#.

## Krok 1: Konfigurowanie środowiska

Upewnij się, że masz zainstalowany Aspose.Cells for .NET na swoim komputerze. Utwórz także nowy projekt w preferowanym środowisku programistycznym.

## Krok 2: Zaimportuj niezbędne biblioteki

W pliku kodu zaimportuj biblioteki potrzebne do pracy z Aspose.Cells. Oto odpowiedni kod:

```csharp
using Aspose.Cells;
```

## Krok 3: Ustaw katalogi źródłowe i wyjściowe

Ustaw odpowiednio katalogi źródłowy i wyjściowy, w których znajduje się oryginalny plik Excel i gdzie chcesz zapisać zmodyfikowany plik. Użyj następującego kodu:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Pamiętaj, aby podać pełne ścieżki katalogów.

## Krok 4: Ładowanie źródłowego pliku Excel

Załaduj źródłowy plik Excel, używając następującego kodu:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Spowoduje to załadowanie określonego pliku Excel do obiektu Workbook.

## Krok 5: Poruszaj się po arkuszach

Wykonaj iterację po wszystkich arkuszach w skoroszycie, używając pętli. Użyj następującego kodu:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // Pozostała część kodu zostanie dodana w następnym kroku.
}
```

## Krok 6: Usuń istniejące ustawienia drukarki

Sprawdź, czy dla każdego arkusza istnieją ustawienia drukarki i usuń je, jeśli to konieczne. Użyj następującego kodu:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## Krok 7: Zapisywanie zmodyfikowanego skoroszytu

Zapisz zmodyfikowany skoroszyt, używając następującego kodu:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Spowoduje to zapisanie zmodyfikowanego skoroszytu w określonym katalogu wyjściowym.

### Przykładowy kod źródłowy narzędzia Usuń istniejące ustawienia drukarki z arkuszy przy użyciu Aspose.Cells dla platformy .NET 
```csharp
//Katalog źródłowy
string sourceDir = RunExamples.Get_SourceDirectory();
//Katalog wyjściowy
string outputDir = RunExamples.Get_OutputDirectory();
//Załaduj źródłowy plik Excel
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Uzyskaj liczbę arkuszy skoroszytu
int sheetCount = wb.Worksheets.Count;
//Iteruj wszystkie arkusze
for (int i = 0; i < sheetCount; i++)
{
    //Uzyskaj dostęp do i-tego arkusza
    Worksheet ws = wb.Worksheets[i];
    //Uzyskaj dostęp do ustawień strony arkusza
    PageSetup ps = ws.PageSetup;
    //Sprawdź, czy istnieją ustawienia drukarki dla tego arkusza
    if (ps.PrinterSettings != null)
    {
        //Wydrukuj poniższą wiadomość
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Wydrukuj nazwę arkusza i jego rozmiar papieru
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Usuń ustawienia drukarki, ustawiając je na wartość null
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//Jeśli
}//Do
//Zapisz skoroszyt
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Wniosek

Nauczyłeś się teraz, jak usunąć istniejące ustawienia drukarki z arkuszy kalkulacyjnych w programie Excel przy użyciu Aspose.Cells dla .NET. Ten samouczek przeprowadził Cię przez każdy etap procesu, od konfiguracji środowiska po nawigację po arkuszach kalkulacyjnych i czyszczenie ustawień drukarki. Możesz teraz wykorzystać tę wiedzę do zarządzania ustawieniami drukarki w plikach Excel.

### Często zadawane pytania

#### P1: Skąd mam wiedzieć, czy arkusz kalkulacyjny ma istniejące ustawienia drukarki?

 O1: Możesz sprawdzić, czy istnieją ustawienia drukarki dla arkusza, uzyskując dostęp do pliku`PrinterSettings` własność`PageSetup` obiekt. Jeśli wartość nie jest równa null, oznacza to, że istnieją ustawienia drukarki.

#### P2: Czy mogę usunąć ustawienia drukarki tylko dla określonego arkusza kalkulacyjnego?

 Odpowiedź 2: Tak, możesz zastosować tę samą metodę, aby usunąć ustawienia drukarki dla określonego arkusza, uzyskując dostęp do jego`PageSetup` obiekt.

#### P3: Czy ta metoda usuwa również inne ustawienia układu?

O3: Nie, ta metoda usuwa jedynie ustawienia drukarki. Pozostałe ustawienia układu, takie jak marginesy, orientacja papieru itp. pozostają niezmienione.

#### P4: Czy ta metoda działa w przypadku wszystkich formatów plików Excel, takich jak .xls i .xlsx?

O4: Tak, ta metoda działa dla wszystkich formatów plików Excel obsługiwanych przez Aspose.Cells, w tym .xls i .xlsx.

#### P5: Czy zmiany w ustawieniach drukarki są trwałe w edytowanym pliku Excel?

O5: Tak, zmiany w ustawieniach drukarki są trwale zapisywane w edytowanym pliku Excel.